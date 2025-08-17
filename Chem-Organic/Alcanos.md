Son hidrocarburos saturas, es decir, no poseen enláces múltiples. Su fórmula general es:
$$
\ce{ C_{n}H_{2n+2} }
$$
- Los carbonos que los componen tienen hibridación $\ce{ sp^{3} }$.
- Su $pKa \approx 50$ 
# Síntesis
### Reducción con Zn:
Para los orgánicos, pérdida de átomos de oxígeno o captura de H por parte de un átomo de C.
$$
\ce{ 2RX ->[Zn,HCl] 2RH + Zn^{+2} + 2X- \qquad X = Cl, Br}
$$
Se evita el F, por ser su enlace muy fuerte y el I, ya que puede reducirse a $\ce{ I_{2} }$, el cuál puede complicar la purificación del producto.
No se conoce el mecanismo. 

### Reactivo de Grignard:
El reactivo de Grignard se sintetiza a partir de un halogenuro de alquilo y un metal, comúnmente Mg.
$$
\boxed{\ce{ R-X + Mg -> R-MgX }}
$$
El **mecanismo** se basa en la trasferencia de un electrón:
$$
\begin{align}
\ce{ R-X + Mg &-> [R-X*]^{-} + [Mg*]^{+}  } \\
\ce{ [R-X*]^{-} &-> R* + X^{-} }  \\
\ce{ R* + [Mg*]^{+} &-> R - Mg^{+}}  \\
\ce{ R - Mg^{+} + X^{-} &-> R-MgX}
\end{align}
$$
Este reactivo se utiliza para la síntesis de muchos reactivos, en particular alcanos. Dada su alta reactividad, la presencia de una solución acuosa ácida o incluso neutra, es suficiente para dar como resultado el alcano. Por ejemplo:
$$
\ce{ R-MgX + H_{2}O -> R-H + Mg(OH)X }
$$
Esta reacción también es posible en medio acuoso, en presencia de cualquier ácido, que vuelve la reacción aún más rápida. 
Su alta reactividad se debe a la fuerza de la base conjugada del R-H:
$$
\ce{ R-H -> R- + H+ } \qquad Ka = 10^{-40}
$$

### Hidrogenación de alquenos y alquinos:
La hidrogenación es un proceso espontáneo, pero cinéticamente lento. Por lo tanto, requiere un catalizador metálico. 
![[Pasted image 20250806120139.png|center|500]]
![[Pasted image 20250806120503.png|center]]
- La catálisis cambia el mecanismo de reacción. En general, el $\ce{ H_{2} }$ se quimisorbe sobre el metal, rompiendo su enlace y luego el alqueno o alquino se hidrogena.
- La reacción es estereoselectiva y da el producto de la adición syn. 

### Síntesis de Wurtz:
Tiene la ventaja de alargar la cadena. 
$$
\begin{equation}
\ce{2R-X + 2 Na ->[THF] R-R + 2NaX }
\end{equation}
$$
El mecanismos es similar la formación de compuestos organometálicos, pero el intermediario es tan reactivo que reacciona con sí mismo. Esto es porque el $\ce{ Na }$ tiende a formar un enlace más iónico que otros metales como el $\ce{ Mg }$.
$$
\begin{align}
\ce{ R-X + 2Na &-> R- Na+ + NaX } \\
\ce{ R-X + R- Na+ &-> R-R + NaX}
\end{align}
$$

Utilizar mezclas de halogenuros de alquilo como reactivo, resulta en todos los productos posibles:
$$
\begin{equation}
\ce{ R-X + R'-X ->[Na][THF]} 
\begin{cases}
R-R + 2NaX & 25\%  \\
R-R' + 2NaX & 50\%  \\ 
R'-R' + 2NaX & 25\%
\end{cases}
\end{equation}
$$
Los porcentajes son aproximados y se basan en el hecho de que la reacción del Na con cualquier halogenuro de alquilo es equiprobable. Por lo tanto, hay el doble de probabilidad de formar el producto cruzado, ya que puede ocurrir el ataque de $\ce{ R-Na }$ a  $\ce{ R'-X }$ como también $\ce{ R'-Na }$ a $\ce{ R-X }$.
### Síntesis de Corey-House
Es útil para acoplar dos cadenas distintas con mayor eficiencia que la síntesis de Wurtz.
$$
\begin{align}
\ce{ RX + 2Li &->  R-Li + LiX} \\
\ce{ 2R-Li + CuI &-> [R-Cu-R]- Li+ + LiI }  \\
\ce{ [R-Cu-R]- Li+ +R'-X &-> R'-R + 'RCu' + LiX}
\end{align}
$$
- De nuevo, una reacción que toma ventaja del hecho de que el $\ce{ Li }$ es más electropositivo que el $\ce{ Cu }$, Por lo tanto, en el $\ce{ R-Li }$, el grupo alquilo tiene una mayor densidad de carga negativa, lo que permite que ataque al $CuI$. 
- La sal $\ce{ [R-Cu-R]- Li+ }$ es relativamente estable, por lo que se puede hacer reaccionar luego con otro halogenuro de alquilo $\ce{ R'-X }$. 
- Tiene como desventaja de que tanto el $\ce{ R'-X }$, como el $\ce{ R-X }$ deben ser primarios para obtener un buen rendimiento. De otro modo el rendimiento de la reacción baja a menos del 50%. 

# Reacciones de Alcanos
Dado a su alta estabilidad, los alcanos solo sufren principalmente dos tipos de reacciones.
### Combustión:
Los productos producidos son altamente estables, dependiendo si esta es completa o incompleta se genera $\ce{ CO_{2} }$ o en el caso de una incompleta $\ce{ CO }$ o incluso C.
Las reacciones serían:
$$
\begin{align}
\ce{ C_{n}H_{2n+2} + \frac{3n + 1}{2} O_{2} &-> nCO_{2} + (n + 1) H_{2}O  & \text{{Completa}}}  \\
\ce{ C_{n}H_{2n+2} + \frac{2n + 1}{2} O_{2} &-> nCO + (n + 1) H_{2}O  & \text{{Incompleta}}} \\
\ce{ C_{n}H_{2n+2} + \frac{n + 1}{2} O_{2} &-> nC + (n + 1) H_{2}O  & \text{{Mínima}} }
\end{align}
$$
Cuánto menos moléculas de oxígeno se consuman, más incompleta es la reacción y menor energía se genera. 

### Halogenación vía radicalaria.
- Puede realizarse entregando la energía en forma de calor o luz.
- En el caso de entregar la energía en forma de luz, la longitud de onda debe ser la correspondiente para llevar la molécula al estado excitado electrónico disociativo correspondiente. 
- La estabilidad de los radicales, especies faltas de densidad electrónica, es 3°>2°>1°. 
- Sustituyentes que entreguen densidad electrónica por inducción puede estabilizar radicales.
- No se realiza con $\ce{ F_{2} }$, por ser este muy reactivo y la reacción ser explosiva.
- No ocurre con $\ce{ I_{2} }$ por ser el radical $\ce{ I* }$ poco reactivo e incapaz de formar el $\ce{ R* }$.

**Mecanismo**:

$$
\begin{align}
\text{Iniciación}
&\begin{cases}
\ce{ X-X ->[h\nu / \Delta] 2 X*} 
\end{cases} \\
\text{Propagación}  
&\begin{cases}
\ce{ X* + R-H -> R* + HX } \\
\ce{ R* + X_{2} -> R-X + X* }
\end{cases} \\
\text{Terminación}  
&\begin{cases}
\ce{ X* + X* -> X_{2} } \\
\ce{ R* + R* -> R-R }  \\
\ce{ R* + X* -> RX }
\end{cases}
\end{align}
$$
* Notar que en el primer paso de propagación, podría haberse formado también $\ce{ R-Cl + H*}$, pero dado a que el $\ce{ H* }$ es altamente inestable, su formación está desfavorecida. 
* También es posible que los radicales choquen contra la pared, finalizando así la reacción. 
* Puede haber policloración, si las concentraciones de $\ce{ Cl_{2} }$ son relativamente altas. 

La reactividad relativa para el $\ce{ Cl_{2} }$ es aproximadamente: 

| Primarios | Secundarios | Terciarios |
| :-------: | :---------: | :--------: |
|     1     |     3.8     |     5      |
Esto permite calcular la cantidad aproximada de producto en el caso de tener hidrógenos no equivalentes. Por ejemplo, para el propano $\ce{ C_{3}H_{8} }$ se tienen 6 hidrógenos primarios y 2 secundarios. Por lo tanto, se obtiene un $6 / (3.8 \cdot 2 + 6) = 0.44$ del primario y $2\cdot 3.8 / (3.8 \cdot 2 + 6) = 0.56$ del secundario. 

La reactividad relativa para el $\ce{ I_{2} }$ es aproximadamente: 

| Primarios | Secundarios | Terciarios |
| :-------: | :---------: | :--------: |
|     1     |     80      |    1600    |
El motivo de esta gran diferencia en reactividad, puede explicarse en base a la regla de Hammond. Esta establece que el estado de transición tendrá una estructura más similar al reactivo, para una reacción exotérmica y al producto, para una endotérmica. 
- El paso de propagación que genera el $\ce{ R* }$ es exotérmico en el caso de la cloración, por lo que el estado de transición se asemeja más al alcano que al radical libre.
- En cambio, la generación del $\ce{ R* }$ en la bromación es exotérmica y por lo tanto, el estado de transición se asemeja más al radical libre. Es por esto que la estabilización del radical es un factor predominante en la bromación. 
![[Pasted image 20250810003110.png|center]]
![[Pasted image 20250810004853.png|center]]
