

```python
A = Solution(246, 'acid', pK=4.76)
A.K_from_pK()
print(A.K)
```

## Classes:
```python
class Solution:
    #Constructor
    def __init__(self, Mr, solutionType, pK='none', K='none',V=0, Cmolar=0, n=0, m=0):
        self.Mr = Mr
        self.solutionType = solutionType
        self.V = V
        self.Cmolar = Cmolar 
        self.n = n
        self.m = m
        self.pK = pK
        self.K = K

    #Methods
    def n_from_VCmolar(self):
        if self.Cmolar or self.V == 0:
            print('C(molar) or V are not defined.')
        else:
            self.n = self.Cmolar*self.V
            print('n:{:.4g} mol.' .format(self.n))
    
    def V_from_nCmolar(self):
        if self.n or self.Cmolar==0:
            print('C(molar) or n are not defined.')
        else:
            self.V = self.n/self.Cmolar
            print('V:{:.4g} L' .format(self.V))

    def Cmolar_from_nV(self):
        if self.n or self.V == 0:
            print('n or V are not defined.')
        else: 
            self.Cmolar = self.n/self.V
            print('C:{:.4g} M' .format(self.Cmolar))
    
    def K_from_pK(self):
        if self.pK == 'none':
            print('pKa is not defined')
        else: 
            self.K = 10**(-self.pK)
            print('Ka:{:.4g} ' .format(self.K))
    
    def pK_from_K(self):
        if self.K == 'none':
            print('Ka is not defined')
        else:
            self.pK = -np.log10(self.K)
            print('pKa:{:.4g} ' .format(self.pK))
        
class Pure:
    def __init__(self, solution:Solution, Kw = 1e-14, H=0):
        self.H = H
        self.solution = solution
        self.Kw = Kw
    
    def calculateH(self):
        if self.solution.K != 'none':
            Ka = self.solution.K
        
        elif self.solution.pK != 'none':
            self.solution.K_from_pK()

        C = self.solution.Cmolar
        Kw = self.Kw
        coeff = [1, Ka, -Ka*C-Kw]
        roots = np.roots(coeff)

        if isinstance(Ka, float):
            if Ka >= 1e-7:
                H = roots[(roots >= 1e-7)]
            
            elif Ka <= 1e-7:
                H = roots[(roots <= 1e-7) & (roots > 1e-14)]
        
            self.H = H[0]
            print('[H+]:{:.4e} M' .format(self.H))

        #TODO: multiproton acid
        #if isinstance(Ka, (list, np.ndarray)):

    def calculatepH(self):
        self.calculateH()
        pH = -np.log10(self.H)
        print('pH:{:.4g}' .format(pH))
        return pH


class Titration:
    def __init__(self, sample:Solution, titrant:Solution, Vtitrant, H=0, Kw=1e-14):
        self.H = H
        self.sample = sample
        self.titrant = titrant 
        self.Vtitrant = Vtitrant
        self.Kw = Kw
    
    def strongTitrantCalculateH(self):
        C0sample = self.sample.Cmolar
        Vsample = self.sample.V
        C0titrant = self.titrant.Cmolar
        Vtitrant = self.Vtitrant

        nSample = C0sample*Vsample
        nTitrant = C0titrant*Vtitrant
        Vtot = Vsample + Vtitrant
        Csample = C0sample*Vsample/Vtot
        Ctitrant = C0titrant*Vtitrant/Vtot 
        Ksample = self.sample.K

        if isinstance(self.Vtitrant, (list,np.ndarray)):
            Id = np.ones(len(self.Vtitrant))

            #print(Id.shape, (Ctitrant+Ksample).shape, (Ksample*(Ctitrant-Csample)-self.Kw).shape, )

            coeffs = np.stack((Id, Ctitrant+Ksample, Ksample*(Ctitrant-Csample)-self.Kw, -Ksample*self.Kw*Id), axis=1)
            roots = np.array([np.roots(eq) for eq in coeffs])

            if self.sample.solutionType == 'acid':
                self.H = roots[roots>0]
                
        else:
            coeff = [1, Ctitrant+Ksample, Ksample*(Ctitrant-Csample)-self.Kw, -Ksample*self.Kw]
            roots = np.roots(coeff)
            root = roots[(roots >= 0)]

            if self.sample.solutionType == 'acid':    
                H = root[0]
                pH = -np.log10(H)
                self.H = H 
                print('[H+]: {:.4e} M and pH:{:.4g}' .format(H, pH))

            elif self.sample.solutionType == 'base':
                OH = root[0]
                self.H = OH/self.Kw 
                pH = -np.log10(self.H)
                print('[H+]: {:.4e} M and pH: {:.4g}' .format(self.H, pH))

```