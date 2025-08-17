Dada una reacción química genérica:
$$
\ce{ \nu_{A} A + \nu_{B} B -> \nu_{C} C + \nu_{D} D }
$$
podemos determinar que:

|         |        $\nu_{A}A$         |  +  |        $\nu_{B}B$         | $\to$ |        $\nu_{C} C$        |  +  |        $\nu_{D} D$        |
| :-----: | :-----------------------: | :-: | :-----------------------: | :---: | :-----------------------: | :-: | :-----------------------: |
| inicial |        $n_{A}^{0}$        |     |        $n_{B}^{0}$        |       |        $n_{C}^{0}$        |     |        $n_{D}^{0}$        |
|   $t$   | $n_{A}^{0} - \nu_{A} \xi$ |     | $n_{B}^{0} - \nu_{B} \xi$ |       | $n_{C}^{0} + \nu_{C} \xi$ |     | $n_{D}^{0} + \nu_{D} \xi$ |
De donde se desprende que: 
$$
\begin{align}
n_{r}&=n_{r}^{0} - \nu_{r} \xi \Leftrightarrow \xi = -\frac{n_{r}-n_{r}^{0}}{\nu_{r}} \\
n_{p}&=n_{p}^{0} - \nu_{p} \xi \Leftrightarrow \xi = \frac{n_{p}-n_{p}^{0}}{\nu_{p}}
\end{align}
$$
donde $r$ hace referencia a un reactivo arbitrario y $p$ a un producto arbitrario.

Podemos ver que $\xi$ , da una idea de cuánto avanzó la reacción y por eso se lo conoce como grado de avance de la reacción. En particular, el caso más común es empezar sin productos ($n_{p}^{0}=0$) y si además se trabaja en proporciones estequiométricas, puede verse que $0<\xi<1$ . 

Dado a que el $\xi$ es proporcional al número de partículas del sistema, para la definición de velocidad se divide por el volumen, de forma tal que:
$$
\begin{equation}
\boxed{
v = \frac{1}{V} \frac{d\xi}{dt} = - \frac{1}{\nu_{r} V} \frac{dn_{r}}{dt} = \frac{1}{\nu_{p} V} \frac{dn_{p}}{dt} 
}
\end{equation}
$$
Sabiendo que:
$$
\begin{align}
n = C V \implies dn = V dC + C dV
\end{align}
$$
por lo tanto:
$$
\begin{equation}
v = -\frac{1}{\nu_{r}V} \left( V\frac{dC}{dt} + C \frac{dV}{dt}  \right)
\end{equation}
$$
que en el caso de que el volumen sea constante, se reduce a la ecuación comúnmente utilizada:
$$
\begin{equation}
v = -\frac{1}{\nu_{r}} \frac{dC_{r}}{dt} = \frac{1}{\nu_{p}} \frac{dC_{p}}{dt} 
\end{equation}
$$
