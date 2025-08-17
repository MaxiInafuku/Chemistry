# Reglas de Hückel
Para determinar la aromaticidad de un compuesto, deben cumplirse las reglas de Hückel:
1) La molécula debe tener $4n+2$ con $n \in \mathbb{N}$ 
2) Debe ser plana (o casi plana), para permitir el solapamiento de los orbitales p
3) Debe ser cíclica
4) Debe tener un anillo de orbitales p continuos. 
El motivo, es que los compuestos cíclico (3) que cumplen la regla (2) y (4) tienen una configuración de sus orbitales moléculares simple de calcular por el método de Hückel, conocida como los círculos de Frost.

Para los círculos de Frost, basta con dibujar el polígono cuyo número de lados sea igual al número de C del ciclo y ubicarlo de forma tal que quede un único orbital como el de menor energía:
![[Pasted image 20250813185008.png|center]]

La estabilización viene del hecho de que se están llenando de forma completa, orbitales ligantes. Por ejemplo, con $n=1$ se tienen $6 e^- \pi$ y si colocamos esta cantidad de electrones en el benceno o el anión ciclopentadienilo, se logra la máxima estabilización respecto a los orbitales libres. 
Eigenvalues del anión ciclopentadienilo:
$$
\begin{align}
E_{0} &= \alpha + 2\beta &  
E_{1} &= \alpha + \frac{\sqrt{ 5 }-1}{2} \beta \approx \alpha + 1.24 \beta &  
E_{2} &= \alpha - \frac{\sqrt{ 5 }+1}{2} \beta
\end{align}
$$
dando una energía de con $6e^{-}$ de $E = 2E_0 + 4E_{1} \approx 6\alpha + 6.96\beta$. 

Mientras que el anión del pentadienilo $\ce{ H_{2}C\bond{=}CH-CH\bond{=}CH\bond{-}CH_{2}- }$ tiene energías:
$$
\begin{align}
E_{0} &= \alpha + \sqrt{ 3 }\beta \approx \alpha + 1.73\beta&  
E_{1} &= \alpha + \beta &  
E_{2} &= \alpha & 
E_{3} &= \alpha + \beta &  
E_{4} &= \alpha - \sqrt{ 3 }\beta
\end{align}
$$
dando una energía total con $6e^{-}$ de $E=2E_{0} + 2E_1 + 2E_2 \approx 6\alpha + 5.46\beta$. 

En cambio, si estuviéramos hablando del carbocatión ciclopentadienilo, que no es aromático, se tendría que su energía total es $E = 2E_0 + 2E_{1} \approx 6\alpha + 2.48\beta$. Que comparada con la del catión del pentadienilo se tiene $E=2E_{0} + 2E_1 \approx 4\alpha + 5.46\beta$. 
Esto muestra que en este caso no hay una estabilización adicional porque no es aromático.

Incluso en el caso del dianión ciclobutadienilo, que posee $6e^{-}$, pese a que estos se localizan en orbitales no ligantes, el análisis de las energías muestra que esto es más estable que el dianión del butadienilo, dónde se empiezan a llenar orbitales antiligantes. 

Para el caso de $4e^{-}$, de hecho el anillo se distorsiona y genera dos dobles enlaces relativamente independientes. Justamente, la distorsión se corresponde a dobles enlaces que son más cortos que los simples. 

Analizando la energía de los orbitales, tenemos que para el caso de los 2 enlaces conjugados, los eigenvalues son:
$$
\begin{align}
E_{0} &= \alpha+2\beta & 
E_{1} &= \alpha  &
E_{2} &= \alpha-2\beta
\end{align}
$$
dando una energía total de $E=2E_{0} + 2E_{1} = 4\alpha+4\beta$
Mientras que teniendo los dobles enlaces sin conjugar se obtiene una $E=4(\alpha+\beta)$. Por lo que Hückel no basta para explicar por qué se elige la configuración de "dobles enlaces aislados". La estabilidad de tener los dos enlaces aislados está explicada en los enlaces sigma. 
