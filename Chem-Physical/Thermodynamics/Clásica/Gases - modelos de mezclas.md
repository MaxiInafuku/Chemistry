# Virial a primer orden
Para mezclas, el desarrollo del virial se escribe en función de los volúmenes molares y la presión del sistema, pero los coeficientes tiene una dependencia con la fracción molar de los componentes de la mezcla. En FQ2, tan solo se ve el primer coeficiente del virial, tal que:
$$
\begin{equation}
\boxed{
Z = 1 + B \frac{1}{\bar{V}} \qquad 
B = x_{1}^2 B_{11} + 2x_{1}x_{2} B_{12} + x_{2}^2 B_{22}
}
\end{equation}
$$
donde $B_{ij}$ representa el término de interacción entre las partículas $i,j$. 

En este modelo simple, $x_i$ es proporcional a la probabilidad de encontrar a la $i$-ésima partícula. Es por eso que siempre se encuentra de forma cuadrática, ya que esto implica la probabilidad de el encuentro entre las partículas. En el término $2 x_1 x_2 B_{12}$, el 2 se debe a que puede darse el encuentro de $1,2$ o $2,1$ y en ambos la interacción es entre las partículas de tipo 1 y 2. 

Es común también trabajar con $B$ expresado en función de $\Delta_{12}$, definido como:
$$
\begin{equation}
\boxed{
\Delta_{12} = 2B_{12} - B_{11} - B_{22}
}
\end{equation}
$$
esta cantidad muestra cómo se compara la interacción $1,2$ respecto al promedio entre las interacciones $1,1$ y $2,2$. 
- $\Delta_{1,2} > 0 \Rightarrow B_{12} > (B_{11} + B_{22})/2$, por lo que las interacciones cruzadas son mayores al promedio de las interacciones entre partículas del mismo tipo. Dado a que estamos hablando de energías, que son más favorables cuanto más bajas son, en este caso las interacciones cruzadas son desfavorables respecto a las interacciones entre partículas de igual tipo.
- $\Delta_{1,2} < 0 \Rightarrow B_{12} < (B_{11} + B_{22})/2$, las interacciones entre partículas son menores al promedio de interacciones entre partículas de igual tipo. Lo que indica que las interacciones cruzadas son más favorables. 
- $\Delta_{1,2} = 0 \Rightarrow B_{12} = (B_{11} + B_{22})/2$, las interacciones entre partículas del mismo tipo son, en promedio, igual a la interacción cruzada. 
- Los términos $B_{ij}$ son independientes de la temperatura, dado a que son interacciones. 

Si queremos escribir $B$ en función de $\Delta_{12}$, basta con reemplazar $2B_{12} = \Delta_{12} + B_{11} + B_{22}$ en la ecuación de $B$:
$$
\begin{align*}
B &= x_{1}^2 B_{11} + x_{1}x_{2}(\Delta_{12} + B_{11} + B_{22}) + x_{2}^{2} B_{22} 
\\
&= x_{1}^2 B_{11} + x_{1}x_{2}\Delta_{12} + x_{1}x_{2}B_{11} + x_{1}x_{2}B_{22} + x_{2}^2 B_{22} 
\\
&= x_{1} B_{11} (x_{1}+x_{2}) + x_{1}x_{2}\Delta_{12} + x_{2}B_{22}(x_{1}+x_{2})
\end{align*} 
$$
Sabiendo que $x_1 + x_2 = 1$:
$$
\begin{equation}
\boxed{
B = x_{1}B_{11} + \Delta_{12} x_{1}x_{2} + x_{2} B_{22}
}
\end{equation}
$$
### Potencial químico
Para hallar la energía libre, recordamos que:
$$
\begin{align*}
Z &= \frac{p \bar{V}}{RT}
= 1 + \frac{B}{RT} p \Rightarrow 
V = \frac{nRT}{p} + nB
\\
\bar{V}_{i} &= \frac{RT}{p} + B + n\left( \frac{ \partial B }{ \partial n_{i} } \right)_{T,p,n_{j\neq i}} 
\end{align*}
$$
donde se utilizó la inversión de serie que dicta que $B' = B/(RT)$. Resolviendo la derivada en un cálculo auxiliar:
$$
\begin{align*}
\left( \frac{ \partial B }{ \partial n_{i} }  \right)_{T,p,n_{j\neq i}} &= 
\frac{ \partial B }{ \partial x_{i} }  \frac{ \partial x_{i} }{ \partial n_{i} } = 
\frac{ \partial B }{ \partial x_{i} } \frac{x_{j}}{n}
\\
\frac{ \partial B }{ \partial x_{i} } &= 
\frac{ \partial  }{ \partial x_{i} } (x_{i} B_{ii} + \Delta_{12} x_{i} (1-x_{i}) + (1-x_{i}) B_{jj}) 
\\
\frac{ \partial B }{ \partial x_{i}} &= B_{ii} + \Delta_{12} (1-2x_{i}) - B_{jj}
\end{align*}
$$
Por lo tanto,
$$
\begin{align*}
\bar{V}_{i} &= \frac{RT}{p} + B + n\left( \frac{ \partial B }{ \partial n_{i} } \right)_{T,p,n_{j\neq i}} 
\\
&= \frac{RT}{p} + x_{i}B_{ii} + \Delta_{12} x_{i} x_{j} + x_{j} B_{jj} + (B_{ii} + \Delta_{12}(1-2x_{i}) - B_{jj}) x_{j} 
\\
&= \frac{RT}{p} + B_{ii} (x_{i}+x_{j}) + \Delta_{12} (x_{i}x_{j} + x_{j} - 2x_{i}x_{j})
\\
&= \frac{RT}{p} + B_{ii} + \Delta_{12} (x_{j} - x_{i}x_{j}) 
\\
&= \frac{RT}{p} + B_{ii} + \Delta_{12} x_{j}(1-x_{i}) 
\\
&=  \frac{RT}{p} + B_{ii} + \Delta_{12} x_{j}^2
\end{align*}
$$
donde se utilizó que $x_i+x_j = 1$.

Utilizando lo visto en [[Gases - potencial químico#Mezcla de gases no ideales]]
$$
\begin{align*}
\ln\varphi_{i} &= \int_{p\to0}^{p} \left( \frac{\bar{V}_{i}}{RT} - \frac{1}{p} \right) dp
\\
&= \int_{p\to0}^{p} \left( \frac{1}{p} + \frac{B_{ii}+ \Delta_{12} x_{j}^2 }{RT} - \frac{1}{p} \right) dp
\\
&= \int_{p\to0}^{p} \frac{B_{ii}+ \Delta_{12} x_{j}^2 }{RT}dp
\end{align*}
$$
$$
\begin{equation}
\boxed{
\ln\varphi_{i} = \frac{p}{RT}(B_{ii}+x_{j}^2\Delta_{12})
}
\end{equation}
$$
Una forma de interpretar esta ecuación es que el primer término de la suma, marca la contribución al potencial químico de la interacción de las partículas del mismo tipo. Mientras que el segundo término, es aquel que da cuenta de la interacción con las partículas del segundo tipo. Es por eso que a $x_j\to0$ el potencial químico converge al de una única partícula. 
### Propiedades termodinámicas 
Dado el coeficiente de fugacidad, es posible calcular el $\Delta_{mix}G$ ([[Gases - potencial químico#Propiedades termodinámicas]]), que mide la desviación respecto a la idealidad.
$$
\begin{align*}
& & \Delta_{mix}G &= n_{1} RT \ln \frac{\varphi_{1}}{\varphi_{1}^{*}} + n_{2}RT \ln\frac{\varphi_{2}}{\varphi_{2}^{*}} + \Delta_{mix}^{id}G
\\
&\text{mezcla} & RT\ln\varphi_{i} &= p(B_{ii}+x_{j}^{2}\Delta_{12})
\\
&\text{puro} & RT \ln\varphi_{i}^{*} &= pB_{ii}
\end{align*}
$$
donde el del puro se calcula simplemente escogiendo $x_{j} = 0$. Resulta así entonces:
$$
\begin{equation}
\Delta_{mix} G = p(n_{1} x_{2}^2 \Delta_{12} + n_{2} x_{1}^2 \Delta_{12}) + RT (n_{1}\ln y_{1} + n_{2} \ln y_{2})
\end{equation}
$$
Sabiendo que los términos $B_{ij}$ no dependen de $T$ y que $\Delta_{mix}G = \Delta_{mix}H - T \Delta_{mix} S$ tenemos que:
$$
\begin{align*}
\Delta_{mix} H &= p(n_{1}x_{2}^2\Delta_{12} + n_{2}x_{1}^2\Delta_{12})  =
np\Delta_{12}(x_{1}x_{2}^2+x_{2}x_{1}^{2}) =
np \Delta_{12} x_{1}x_{2}(x_{1}+x_{2})
\\
\Delta_{mix} H &= np\Delta_{12}x_{1}x_{2}
\\
\Delta_{mix} S &= \Delta_{mix}^{id} S = RT (n_{1}\ln y_{1} + n_{2} \ln y_{2})
\end{align*}
$$
Por último, también podemos obtener el $\Delta_{mix}V$ ya que:
$$
\begin{align*}
&\text{mezcla} & V &= \frac{nRT}{p} + nB	= n\left( \frac{RT}{p} + B_{11}x_{1} + \Delta_{12}x_{1}x_{2} + B_{22}x_{2} \right)
\\
&\text{puro} & V_{i}^{*} &= n_{i}\left( \frac{RT}{p} + B_{ii} \right)
\\
& & \Delta_{mix}V &= \cancel{\frac{nRT}{p}} + n_{1} B_{11} + n\Delta_{12} x_{1}x_{2} + n_{2}B_{22} - n_{1} \left( \cancel{\frac{RT}{p}} + B_{11} \right) - n_{2} \left( \cancel{\frac{RT}{p}}+B_{22} \right)
\\
& & \Delta_{mix}V  &= n \Delta_{12}x_{1}x_{2}
\end{align*}
$$
donde el volumen del compuesto puro se haya igualando $x_j=0$. 

Notemos que alternativamente, podía calcularse:
$$
\begin{equation*}
\left( \frac{ \partial \Delta_{mix}G }{ \partial p } \right)_{T,n_{i}} = \Delta_{mix}V
\end{equation*}
$$
Los resultados obtenidos son:
$$
\begin{align*}
\Delta_{mix}G &= p(n_{1} x_{2}^2 \Delta_{12} + n_{2} x_{1}^2 \Delta_{12}) + RT (n_{1}\ln y_{1} + n_{2} \ln y_{2})
\\
\Delta_{mix} H &= np\Delta_{12}x_{1}x_{2}
\\
\Delta_{mix} S &= \Delta_{mix}^{id} S = RT (n_{1}\ln y_{1} + n_{2} \ln y_{2})
\\
\Delta_{mix}V  &= n \Delta_{12}x_{1}x_{2}
\end{align*}
$$
En particular, es posible apreciar que para una mezcla que cumpla $\Delta_{12}=0$, vale que:
$$
\begin{align*}
\Delta_{mix}H &= 0 &
\Delta_{mix}S &= \Delta_{mix}^{id}S & 
\Delta_{mix}V &= 0
\end{align*}
$$
Esto implica que si la mezcla cumple $\Delta_{12}=0$, la mezcla es ideal ([[Mezclas#Mezcla ideal]]), pese a que no sea una mezcla de gases ideales, ya que $\Delta_{12}=0$ solo implica que $B_{12} = (B_{11}+B_{22})/2$, o sea que el promedio de las interacciones individuales sea igual a la cruzada. 
# Van der Waals
Para el caso de un gas de VdW, la ecuación de estado sigue valiendo, 