[[classes]]

The bare minimum for everything to run. Always run this block of code:

```python
import micropip 
await micropip.install('numpy')
import numpy as np
await micropip.install('matplotlib')
import matplotlib.pyplot as plt
print('Libraries loaded')
```

# Scripts para Ac-base
### Base fuerte pura:
```python
log_CNaOHs = np.linspace(-6,-8, 1000)    #M 
Kw = 1e-14

pHs = []
for log_CNaOH in log_CNaOHs:
	CNaOH = 10**(log_CNaOH)
	singleHs = np.roots([1,CNaOH, -Kw])
	singleH = singleHs[singleHs > 0][0]
	singlepH = -np.log10(singleH)
	pHs.append(singlepH)

pH_approx = 14 + log_CNaOHs

fig, ax = plt.subplots()
ax.plot(log_CNaOHs, pHs, label = 'exacto')
ax.plot(log_CNaOHs, pH_approx, label = 'aproximado')
ax.set_xlabel('log($C_{NaOH}$)')
ax.set_ylabel('pH')
ax.legend()
plt.show()

fig, ax = plt.subplots()
ax.plot(log_CNaOHs, pHs-pH_approx)
ax.hlines(0.1, log_CNaOHs[-1], log_CNaOHs[0], linestyle = '--', color = 'black')
ax.set_xlabel('log($C_{NaOH}$)')
ax.set_ylabel('$pH_{exac} - pH_{aprox}$')
plt.show()

```

### Ácido debil puro:
```python
log_CHAs = np.linspace(-1,-8, 1000)    #M 
Kw = 1e-14
#Ka = 10**(-4.75)
Ka = 1e-6


pHs = []
for log_CHA in log_CHAs:
	CHA = 10**(log_CHA)
	singleHs = np.roots([1,Ka, -(Kw+Ka*CHA), -Kw*Ka])
	singleH = singleHs[singleHs > 0][0]
	singlepH = -np.log10(singleH)
	pHs.append(singlepH)

pH_approx1s = []
for log_CHA in log_CHAs:
	CHA = 10**(log_CHA)
	singleHs = np.roots([1,Ka,-Ka*CHA])
	singleH = singleHs[singleHs > 0][0]
	singlepH = -np.log10(singleH)
	pH_approx1s.append(singlepH)

pH_approx2s = -np.log10(np.sqrt(Ka*10**(log_CHAs)))

fig, ax = plt.subplots()
ax.plot(log_CHAs, pH_approx1s, label = '$[HO^-]$ despreciable')
ax.plot(log_CHAs, pH_approx2s, label = '$pH = log(Ka.C_{HA})/2$')
ax.plot(log_CHAs, pHs, label = 'exacto')
ax.set_xlabel('log($C_{HA}$)')
ax.set_ylabel('pH')
ax.legend(loc='lower left')
plt.show()

fig, ax = plt.subplots()
ax.plot(log_CHAs, np.array(pHs)-np.array(pH_approx1s), label = '$[HO^-]$ despreciable')
ax.plot(log_CHAs, np.array(pHs)-np.array(pH_approx2s), label = '$pH = log(Ka.C_{HA})/2$')
ax.hlines(0, log_CHAs[-1], log_CHAs[0], linestyle = '--', color = 'black')
ax.set_xlabel('log($C_{HA}$)')
ax.set_ylabel('$pH_{exac} - pH_{aprox}$')
ax.legend()
plt.show()

```


# Scripts UNSAM - Inorgánica - TP1
```python
pKa1 = 6.4
pKa2 = 10.3
MrNaOH = 39.9971      #g/mol
MrNaHCO3 = 84.007     #g/mol
MrK2CO3 = 138.21      #g/mol

#1.38 es 0.01M de K2CO3
#0.84 es 0.01M de NaHCO3
#0.4 es 0.01M de NaOH

#sample = [1.3, 0, 0]    #masses in g
#sample = [1.3, 0.5, 0] #masses in g
#sample = [1.3, 0, 0.2] #masses in g
sample = [1.3,0,0]

mK2CO3 = sample[0]    #g
mNaHCO3 = sample[1]   #g
mNaOH = sample[2]     #g
V = 100               #mL
V = V/1000            #L

Ka1 = 10**(-pKa1)
Ka2 = 10**(-pKa2)
Kw = 1e-14
CK2CO3 = mK2CO3/(MrK2CO3*V)
CNaHCO3 = mNaHCO3/(MrNaHCO3*V)
CNaOH = mNaOH/(MrNaOH*V)  

print('C(NaOH): {:.4g} M, C(NaHCO3):{:.4g} M, C(K2CO3):{:.4g} M' .format(CNaOH, CNaHCO3, CK2CO3))

C10analito = CNaOH + CNaHCO3 + 2*CK2CO3
C20 = CNaHCO3 + CK2CO3
  
Va = 5        #mL de analito
CHCl0 = 0.15
Vfinal = 10   #mL de titulante
  
step = int(Vfinal/0.1)
#VHCls = np.linspace(0, Vfinal, step)  #Este es la posta de cómo les da
VHCls = np.linspace(0, Vfinal, 1000)   #Este es para gráfico de muestra
  
pHs = []
for VHCl in VHCls:
	Vtot = VHCl+Va
	C1analito = C10analito*Va/Vtot
	CHCl = CHCl0*VHCl/Vtot
	C1 = C1analito - CHCl
	C2 = C20*Va/Vtot
	coeff = [1/Ka1, 1+C1/Ka1, C1 - Kw/Ka1 + Ka2 - C2, C1*Ka2-Kw-2*C2*Ka2, -Kw*Ka2]
	roots = np.roots(coeff)
	H = roots[roots>0][0]
	pH = -np.log10(H)
	pHs.append(pH)
  
Figure, ax = plt.subplots()
#ax.scatter(VHCls, pHs)   #Este es la posta de cómo les da
ax.plot(VHCls, pHs)       #Este es para gráfico de muestra
ax.axhspan(8,10, color = 'violet', alpha = 0.5)    #Este es fenolftaleína
ax.axhspan(3,5, color = 'red', alpha = 0.3)       #Este es el rojo congo
ax.set_xlabel('$V_{HCl}$ (mL)', fontsize = 15)
ax.set_ylabel('pH', fontsize = 15)
plt.show()
  
VHCl_to_NaOH = Va*CNaOH/CHCl0
VHCl_to_NaHCO3 = Va*CNaHCO3/CHCl0
VHCl_to_K2CO3 = Va*CK2CO3/CHCl0
  
print('Los volumenes de HCl para el primer punto de equivalencia son:')
print('NaOH:{:.4g} mL, NaHCO3:{:.4g} mL, K2CO3:{:.4g} mL' .format(VHCl_to_NaOH, VHCl_to_NaHCO3, VHCl_to_K2CO3))
```

```python
dpH_dVs = []
V_avgs = []
#derivada primera
for i in range(len(pHs)-1):
	Vavg = (VHCls[i+1] + VHCls[i])/2
	V_avgs.append(Vavg)
	dV = VHCls[i+1] - VHCls[i]
	dpH = pHs[i+1] - pHs[i]
	dpH_dV = dpH/dV
	dpH_dVs.append(dpH_dV)

d2pH_dV2s = []
V_avg2s = []
for i in range(len(dpH_dVs)-1):
	Vavg2 = (V_avgs[i+1] + V_avgs[i])/2
	V_avg2s.append(Vavg2)
	dV2 = V_avgs[i+1] - V_avgs[i]
	d2pH = dpH_dVs[i+1] - dpH_dVs[i]
	d2pH_dV2 = d2pH/dV2
	d2pH_dV2s.append(d2pH_dV2)

Figure, ax = plt.subplots()
ax.plot(V_avgs, dpH_dVs)
ax.set_xlabel('$V_{HCl}$ (mL)')
ax.set_ylabel('$\partial pH/\partial V (mL^{-1})$')
plt.show()

Figure, ax = plt.subplots()
ax.plot(V_avg2s, d2pH_dV2s)
ax.set_xlabel('$V_{HCl}$ (mL)')
ax.set_ylabel('$\partial^2 pH/\partial V^2 (mL^{-2})$')
plt.show()
```
