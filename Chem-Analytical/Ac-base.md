# Definiciones
**Arrehnius:**
- Ácido: sustancia que se ioniza en agua y genera $\ce{ H+ }$.
- Base: sustancia que se disocia en agua y genera $\ce{ HO- }$.

**Bronsted-Lowry:**
- Ácido: aquel que dona un $\ce{ H+ }$.
- Base: aquella que recibe un $\ce{ H+ }$.
Esta forma más generalizada implica que todo ácido reacciona con una base y además posea una base conjugada, generada en la reacción ácido base, ya que la reacción vista a la inversa muestra que la base conjugada toma un protón.
$$
\ce{$\underset{\text{ácido}}{HA}$ + $\underset{\text{base}}{B}$ <=> $\underset{\text{base conjugada}}{A^{-}}$ + $\underset{\text{ácido conjugado}}{BH}$}
$$

**Lewis:**
- Ácido: aquel que recibe un par electrónico.
- Base: aquella que dona el par electrónico.
En esta definición, sustancias como el $\ce{ BF_{3} }$ son ácidos de Lewis, pues son capaces de aceptar un par electrónico, por ejemplo:
$$
\ce{ BF_{3} + F- -> BF_{4}- }
$$

# Constante de acidez
La constante de acidez suele estar definida para una sustancia en agua. Se define entonces, de acuerdo a [[Equilibrio químico]] como:
$$
\ce{ HA(aq) + H_{2}O(l) <=> H_{3}O+(aq) + A-(aq)}  
$$
$$
\begin{equation}
Ka = \frac{a_{H_{3}O+} a_{A^{-}}}{a_{HA} a_{H_{2}O} }
\end{equation}
$$
Es común en el área de analítica o química general hacer las siguientes aproximaciones, que pueden ser relativamente buenas a bajas concentraciones (del orden de $10^{-3}$M):
- Considerar que $x_{H_{2}O}\approx 1$ y por lo tanto: $a_{H_{2}O} = x_{H_{2}O} \gamma_{H_{2}O} \approx 1$
- Soluciones ideales, con lo que $\gamma_{H_{3}O^{+}} = \gamma_{HA} = \gamma_{A^{-}}=1$

De esta forma se llega a la típica expresión:
$$
\begin{equation}
\boxed{
Ka = \frac{[A^{-}][H_{3}O^{+}]}{[HA]}
}
\end{equation}
$$

# Acidez
La acidez se mide en función de la constante $Ka$, por lo que es un parámetro termodinámico que analiza la entalpía libre, de acuerdo a la ecuación:
$$
\begin{equation}
\Delta G^{\theta} = - RT \ln Ka
\end{equation}
$$
Por lo que se ve que a mayor estabilidad termodinámica de los productos, mayor será su fuerza ácida. Debemos recordar que $\Delta G^{\theta} = \Delta H^{\theta} - T \Delta S^{\theta}$, por lo tanto la estabilidad termodinámica depende de:
* El cambio de entalpía, que puede aproximarse en fases condensadas al cambio de energía.
* El cambio de entropía, que suele ser bastante complejo de evaluar y en los análisis suele dejarse de lado.
Muchas tendencias en acidez, pueden explicarse por cuestiones de estabilidad energética, que es en lo que se basan la mayoría de los análisis cualitativos. 

**Ácidos binarios (HA)**:
- En un período, la acidez aumenta hacia la derecha. Esto se debe a que el aumento de electronegatividad estabiliza a la base conjugada $\ce{ A- }$.  
  Ejemplo: $\ce{ CH_{4} < NH_{3} <  H_{2}O < HF }$
- En un mismo grupo, la acidez aumenta al bajar en la tabla periódica. Esto se debe a que la unión H-A se debilita. 
  Ejemplo: $\ce{ HF < HCl < HBr < HI }$

**Oxoácidos (H-O-Y)**, donde Y es el átomo central:
- A mayor cantidad de oxígenos, mayor acidez ya que la base conjugada está mejor estabilizada por resonancia.
  Ejemplo: $\ce{ HClO < HClO_{2} < HClO_{3} < HClO_{4} }$

**Ácidos orgánicos:**
* Por efecto inductivo, con un alcance de 2-3 átomos de C, aquellos grupos que substraigan electrones, pueden estabilizar al producto y por ende, aumentar la fuerza del ácido.
  Ejemplo: 
![[Pasted image 20250724164254.png|center]]
- También es posible la estabilización por resonancia del producto, como es el caso del fenol.

Otras moléculas orgánicas no ácidas con sus $pKa$ son: 

|   $pKa$   |          50           |              44               |       36        |          25           |      15.7       |
| :-------: | :-------------------: | :---------------------------: | :-------------: | :-------------------: | :-------------: |
| Compuesto | $\ce{ CH_{3}CH_{3} }$ | $\ce{ H_{2}C\bond{=}CH_{2} }$ | $\ce{ NH_{3} }$ | $\ce{ HC\bond{#}CH }$ | $\ce{ H_{2}O }$ |
# Cálculo de pH en soluciones puras:
### Base fuerte:
Los balances de masa y carga son:
$$
\begin{align}
BM) \ 
&C_{NaOH} = [Na^{+}] \\
BQ) \  
& [Na^{+}] + [H^{ +}] = [HO^{-}]
\end{align}
$$
combinando ambas ecuaciones se tiene que:
$$
\begin{equation}
\boxed{C_{NaOH} + [H^{+}] = [HO^{-}]}
\end{equation}
$$
Para todos los cálculos se considera que $Kw = 10^{-14}$.

Despejando:
$$
\begin{align}
[H^{+}] = [HO^{-}] - C_{NaOH}
\end{align}
$$
1) Considerando un medio fuertemente básico, para lo cuál $[H^{+}] \ll C_{NaOH}$, se obtiene simplemente:
$$
\begin{align}
&pOH = -\log C_{NaOH}^{0}  \\
&\boxed{pH = 14 + \log C_{NaOH}^{0}}
\end{align}
$$
2) Si no se considera despreciable, se tiene que: 
$$
\begin{align}
C_{NaOH}^{0} + [H^{+}] = \frac{Kw}{[H^{+}]}  \\
[H^{+}]^2 + [H^{+}] C_{NaOH}^{0} - Kw = 0
\end{align}
$$
El resolviendo el polinomio, podemos hallar el $pH$. 

En la figura ([[main]]) se muestran los pH calculados por ambos métodos.
![[Pasted image 20250801212024.png|center]]
- Cómo es de esperarse, el pH se plancha en 7 para el cálculo exacto.
- Es posible apreciar el absurdo de la aproximación, de que a concentraciones menores a $10^{-7}M$ se tienen $pH<7$, lo que implicaría una solución ácida. 
- Puede verse que alrededor de un pH de $10^{-6.75} M = 1.78\times10^{-7} M$ se tiene una diferencia de pH de 0.1, que es aproximadamente la sensibilidad de un pHmetro. En el inset se ve la diferencia de pH. 

### Ácido débil
Los balances son:
$$
\begin{align}
BM)\ & C_{HA} = [HA] + [A^{-}] \\
BQ)\ & [H^{+}] = [HO^{-}] + [A^{-}]
\end{align}
$$
Tenemos además el dato de:
$$
\begin{equation}
Ka = \frac{[H^{+}][A^{-}]}{[HA]} \qquad 
K_{W} = [H^{+}][HO^{-}]
\end{equation}
$$
- **Forma Exacta:**
Combinando el BM con la ecuación de la constante de acidez.
$$
\begin{align}
C_{HA} &= \frac{[H^{+}][A^{-}]}{Ka} + [A^{-}] = [A^{-}]\left( 1 + \frac{[H^{+}]}{Ka} \right) \\
[A^{-}] &= \frac{C_{HA}}{1 + [H^{+}] / Ka}  \\
\end{align}
$$
colocando el resultado en el BQ:
$$
\begin{align}
[H^{+}] &= \frac{K_{W}}{[H^{+}] } + \frac{C_{HA}}{1 + [H^{+}] / Ka}  \\
[H^{+}]^2 \left( 1 + \frac{[H^{+}]}{Ka} \right) &= K_{W} \left( 1 + \frac{[H^{+}]}{Ka} \right) + C_{HA} [H^{+}]  \\
[H^{+}]^2 + \frac{[H^{+}]^3}{Ka} &= K_{W} + \frac{K_{W}}{Ka}[H^{+}] + C_{HA}[H^{+}]  \\
0 &= [H^{+}]^3 + Ka [H^{+}]^2 - (K_{W} + C_{HA} Ka) [H^{+}] - K_{W}Ka
\end{align}
$$
Resolviendo el polinomio de orden 3 es posible hallar los pHs de forma exacta.

- **Despreciando $[HO^{-}]$:**
Si por otro lado, consideramos que la solución es lo suficientemente ácida como para despreciar los $[HO^-]$ se tiene:
$$
\begin{align}
[H^{+}] = [A^{-}] &= {\frac{C_{HA}}{1+\frac{[H^{+}]}{Ka}}}  \\
[H^{+}] + \frac{[H^{+}]^2}{Ka} &= C_{HA} \\
[H^{+}]^2 + Ka[H^{+}] - KaC_{HA} &= 0
\end{align}
$$
Podemos ver que este polinomio, es similar a la solución exacta, pero considerando despreciable el $K_W$. Justamente, porque estamos despreciando la autoprotólisis del agua.

- **Aproximación a $C_{HA} \gg [H^{+}]$:**
Viendo el polinomio anterior, y considerando que $C_{HA} \gg [H^{+}]$:
$$
\begin{align}
[H^{+}]^2 + \cancel{ Ka[H^{+}] } - KaC_{HA} &= 0 \\
[H^{+}] = \sqrt{ Ka C_{HA} }
\end{align}
$$
Pese a ser una aproximación bastante burda, es buena para estimar rápidamente el pH de soluciones de ácidos débil a altas concentraciones. Vemos que por autoconsitencia debe ser entonces:
$$
\begin{equation}
C_{HA} \gg \sqrt{ Ka C_{HA} } \implies C_{HA} \gg Ka
\end{equation}
$$

La siguiente figura muestra el pH resultante de los tres cálculos para el caso del ácido acético ($pKa = 4.75$). 
![[Pasted image 20250804141035.png|center]]
- Se observa que al despreciar la autoprotólisis del agua, de nuevo se permiten pHs absurdos (mayores a 7), cuando la concentración de ácido es baja. Esta aproximación resulta válida hasta que $C_{HA} \sim 10^{-7}$, como para el caso del ácido fuerte.
- Para el caso en donde se toma $C_{HA} \gg Ka$ vemos desviaciones a concentraciones aún más altas. 

### Ácido poliprótico puro
El caso de un ácido poliprótico es complejo, pero sistemático. Como siempre, se plantea el balance de masas, cargas y correspondientes constantes:
$$
\begin{align}
BM)& \ C_{HA} = [H_{2}A] + [HA^{-}] + [A^{-2}] \\
BQ)& \ [H^{+}] = [HO^{-}] + [HA^{-}] + 2 [A^{-2}] \\
Ka_1 &= \frac{[H^{+}][HA^{-}]}{[H_{2}A]} \qquad  
Ka_{2} = \frac{[H^{+}][A^{-2}]}{[HA^{-}]}
\end{align}
$$
Despejando de las constantes de acidez:
$$
\begin{align}
[H_{2}A] = \frac{[H^{+}]^2[A^{-2}]}{Ka_{1}Ka_{2}}
\begin{cases}
[H_{2}A] = \frac{[H^{+}][HA^{-}]}{Ka_{1}}  \\
[HA^{-}] = \frac{[H^{+}][A^{-2}]}{Ka_{2}}
\end{cases}
\end{align}
$$
Con estos resultados, volvemos al balance de masas:
$$
\begin{align}
C_{HA} &= \frac{[H^{+}]^2[A^{-2}]}{Ka_{1}Ka_{2}} + \frac{[H^{+}][A^{-2}]}{Ka_{2}} + [A^{-2}]  \\
[A^{-2}] &= \frac{C_{HA}}{1+[H^{+}]^2 / (Ka_{1}Ka_{2}) + [H^{+}] / Ka_{2}} 
\end{align}
$$
En el balance de cargas:
$$
\begin{align}
[H^{+}] &= \frac{K_{W}}{[H^{+}]} + \frac{[H^{+}]}{Ka_{2}}[A^{-2}] + 2[A^{-2}]  \\
[A^{-2}] &= \frac{[H^{+}] - K_{W} / [H^{+}]}{2 + [H^{+}] / Ka_{2}}
\end{align}
$$
Igualando ambas expresiones:
$$
\begin{align}
\frac{C_{HA}}{1+[H^{+}]^2 / (Ka_{1}Ka_{2}) + [H^{+}] / Ka_{2}}  &= \frac{[H^{+}] - K_{W} / [H^{+}]}{2 + [H^{+}] / Ka_{2}} \\
2C_{HA} + [H^{+}] \frac{C_{HA}}{Ka_{2}} &=  
\left( [H^{+}] - \frac{K_{W}}{[H^{+}]} \right) \left( 1 + \frac{[H^{+}]}{Ka_{2}} + \frac{[H^{+}]^2}{Ka_{1} Ka_{2}} \right)   
\\
2C_{HA} + [H^{+}] \frac{C_{HA}}{Ka_{2}} &=  
[H^{+}] + \frac{[H^{+}]^2}{Ka_{2}} + \frac{[H^{+}]^3}{Ka_{1} Ka_{2}} - \frac{K_{W}}{[H^{+}]} - \frac{K_{W}}{Ka_{2}} - [H^+] \frac{K_{W}}{Ka_{1}Ka_{2}}   \\
0 &= [H^{+}] + \frac{[H^{+}]^2}{Ka_{2}} + \frac{[H^{+}]^3}{Ka_{1} Ka_{2}} - \frac{K_{W}}{[H^{+}]} - \frac{K_{W}}{Ka_{2}} - [H^+] \frac{K_{W}}{Ka_{1}Ka_{2}} - 2C_{HA} - [H^{+}] \frac{C_{HA}}{Ka_{2}}
\end{align}
$$
Para que quede el polinomio, multiplicamos a ambos lados por $[H^+] Ka_1 Ka_2$:
$$
\begin{align}
0 = [H^{+}]^{4} + Ka_{1} [H^{+}]^3 + (Ka_{1} Ka_{2} - C_{HA}Ka_{1} - K_{W}) [H^{+}]^2 - (2C_{HA} + K_{W}Ka_{1}) [H^{+}] - K_{W}
\end{align}
$$

El método general para un ácido poliprótico $H_NA$ es:
1) Expresar cada concentración de ácido parcialmente protonado $[H_{N-k}A^{-k}]$  en función de $[A^{-N}]$, es decir, la especie completamente desprotonada. Esto resulta de forma genérica en:
$$
\begin{equation}
[H_{N-k}A^{k-}] = [A^{-N}] \frac{[H^{+}]^{k}}{Ka_{N-k+1} Ka_{N-k+2}\dots Ka_{N}}
\end{equation}
$$

# Titulación (soluciones ideales)
- **Punto de equivalencia:** punto en el que han reaccionado el ácido y base en cantidades estequiométricamente equivalentes. Para el caso de un ácido poliprótico, puede haber varios puntos de equivalencia, correspondientes a las reacciones estequiométricas de arrancar cada $\ce{ H+ }$.
$$
\begin{align}
\ce{ H_{2}A + B -> HA- + BH+ }  \\
\ce{ HA- + B -> A^{-2} + BH+}
\end{align}
$$
- **Punto final:** punto en el que se determina experimentalmente que se ha alcanzado el punto de equivalencia. 

La titulación es una técnica que permite determinar la concentración de un analito en solución. En particular, la titulación ácido base se basa en el cambio abrupto de pH al alcanzar el punto de equivalencia. 

## Base fuerte titulado con ácido fuerte:
El balance de masas y carga generales son:
$$
\begin{align}
BM) \ 
&C_{NaOH} = [Na^{+}] \\
&C_{HCl} = [Cl^{-}]  \\
BQ) \  
& [Na^{+}] + [H^{ +}] = [HO^{-}] + [Cl^{-}]
\end{align}
$$
combinando ambas ecuaciones se tiene que:
$$
\begin{equation}
\boxed{C_{NaOH} + [H^{+}] = [HO^{-}] + C_{HCl}}
\end{equation}
$$
Para todos los cálculos se considera que $Kw = 10^{-14}$.
### $V_{HCl}=0$
Se procede igual que en la base fuerte pura. 

Considerando un medio fuertemente básico, para lo cuál $[H^{+}] \ll C_{NaOH}$, se obtiene simplemente:
$$
\begin{align}
C_{NaOH}^{0} &= [HO^{-}] \implies pOH = -\log C_{NaOH}^{0}  \\
&\boxed{pH = 14 + \log C_{NaOH}^{0}}
\end{align}
$$

### $V_{HCl}$ en $P_{eq}$:
En el punto de equivalencia se tiene:
$$
\begin{align}
n_{NaOH} &= n_{HCl}   \\
C_{NaOH} = \frac{n_{NaOH}}{V_T} &= \frac{n_{HCl}}{V_T} = C_{HCl} = C\\
\end{align}
$$
donde $V_{T}$ es el volumen total de la solución, es decir, la suma del volumen de NaOH y HCl.
De ahí se desprende, trivialmente que: 
$$
\begin{equation}
[H^{+}] = [HO^{-}] \implies pH = 7
\end{equation}
$$

### $V_{HCl}$ tal que $n_{NaOH} = \frac{3}{2} n_{HCl}$
El cálculo de las nuevas concentraciones es:
$$
\begin{align}
n_{NaOH} &= \frac{3}{2} n_{HCl}  \\
C_{NaOH}^{0} V_{NaOH} &= \frac{3}{2} C_{HCl}^{0} V_{HCl}  \\
C_{NaOH} &= \frac{n_{NaOH}}{V_{NaOH}+V_{HCl}} = \frac{C_{NaOH}^{0}V_{NaOH}}{V_{NaOH}+\frac{2}{3} \frac{C_{NaOH}^{0}}{C_{HCl}^{0}}V_{NaOH}}  \\
C_{NaOH} &= \frac{C_{NaOH}^{0}}{1+\frac{2}{3} \frac{C_{NaOH}^{0}}{C_{HCl}^{0}}} \\
C_{HCl} &= \frac{n_{HCl}}{V_{NaOH}+V_{HCl}}  \\
C_{HCl} &= \frac{C_{HCl}^{0}}{1+\frac{2}{3} \frac{C_{NaOH}^{0}}{C_{HCl}^{0}}}
\end{align}
$$
Por simplicidad, en las cuentas se procederá a usar $C_{NaOH}$ y $C_{HCl}$ en lugar de sus formas en base a datos iniciales. 
En este caso, el pH será muy ácido y por lo tanto $[H^{+}]\gg[HO^{-}]$ y por lo tanto se obtiene que:
$$
\begin{align}
[H^{+}] = C_{HCl}-C_{NaOH} \implies   
pH = -\log(C_{HCl}-C_{NaOH})
\end{align}
$$
o en su forma completa:
$$
\begin{equation}
pH = -\log\left( \frac{C_{HCl}^{0} - C_{NaOH}^{0}}{1+\frac{2}{3} \frac{C_{NaOH}^{0}}{C_{HCl}^{0}}} \right)
\end{equation}
$$

Finalmente, la curva de titulación tiene una apariencia similar a esta:
![[Pasted image 20250801141816.png|center|500]]
- La franja violeta muestra el indicador fenolftaleína. 


# Code

## Classes: