El cambio de una propiedad $X$ por el mezclado, está dado por la cantidad:
$$
\begin{equation}
\Delta_{mix}X = X - \sum_{i} X_{i}^{*}
\end{equation}
$$
donde $\ce{ X }$ hace referencia al valor de la propiedad en la mezcla y $X_{i}$ hace referencia a la propiedad de la $i$-ésima sustancia pura. 

Se define también el exceso de la propiedad como su desviación respecto a la idealidad:
$$
\begin{equation*}
X^{ex} = X - X^{id}
\end{equation*}
$$
donde $X$ representa la propiedad de la mezcla y $X^{id}$ la propiedad, si esta fuera ideal. 

# Volumen
El volumen está definido de por [[Integración de Euler]] por:
$$
\begin{equation*}
V = \sum_{i} n_{i} \bar{V}_{i}
\end{equation*}
$$
Por otro lado, para una sustancia pura, el volumen parcial molar es directamente el volumen molar, ya que por Euler $V = n \frac{ \partial V }{ \partial n }$. Tenemos entonces que:
$$
\Delta_{mix} V = \sum_{i} n_{i} \bar{V}_{i} - \sum_{i} n_{i} \bar{V}_{i}^{*}
$$
donde $\bar{V}_{i}^{*}$ es el volumen molar de la $i$-ésima sustancia pura y $\bar{V}_{i} = \partial V/\partial n_{i}$.

Para una mezcla ideal los volúmenes son aditivos, con lo que la mezcla ideal tienen que:
$$
\begin{equation*}
V^{id} = \sum_{i} n_{i} \bar{V}_{i}^{*}
\end{equation*}
$$
Por lo tanto, el exceso también se calcularía como:
$$
\begin{equation*}
V^{ex} = \sum_{i} n_{i} \bar{V}_{i} - \sum_{i} n_{i} \bar{V}_{i}^{*}
\end{equation*}
$$
Es decir que en este caso particular, la cantidad de mezcla y de exceso coinciden. 

# Entalpía libre
La entalpía libre o energía libre de un sistema está dada por [[Integración de Euler]]: 
$$
\begin{equation*}
G = \sum_{i} n_{i} \mu_{i}
\end{equation*}
$$
mientras que la entalpía libre de los compuestos puros por separado, puede calcularse como la suma de cada $G_i$ individual, pero por ser estos compuestos puros, $G_{i} = n \bar{G}_{i}$ y recordando que para un compuesto puro $\bar{G} = \mu$ podemos escribir:
$$
\begin{equation*}
G^{*} = \sum_{i} n_{i} \mu_{i}^{*}
\end{equation*}
$$
Por lo tanto, se tiene que:
$$
\begin{equation}
\Delta_{mix}G = \sum_{i} n_{i} \mu_{i} - \sum_{i} n_{i} \mu_{i}^{*} = \sum_{i} n_{i} (\mu_{i} - \mu_{i}^{*})
\end{equation}
$$

Por otro lado, el $G^{ex}$ se calcula como:
$$
\begin{equation}
G^{ex} = \sum_{i} n_{i} \mu_{i} - n_{i} \mu_{i}^{id} = \sum_{i} n_{i} (\mu_{i}-\mu_{i}^{id})
\end{equation}
$$
donde podemos ver que en este caso, no necesariamente existe una coincidencia entre la entalpía libre de exceso y la de mezcla.

A partir del $G^{ex}$ es posible también definir las entropías y entalpías de exceso. 
$$
\begin{align*}
-S^{ex} &= \left( \frac{ \partial G^{ex} }{ \partial T }  \right)_{p,n_{i}} = 
\left( \frac{ \partial (G-G^{id}) }{ \partial T }  \right)_{p,n_{i}} = 
-(S-S^{id})
\\
H^{ex} &= G^{ex} + TS^{ex} = (G-G^{id}) + T(S-S^{id}) =H-H^{id}
\end{align*}
$$

## Mezcla ideal
La definición de una mezcla ideal, parte de la mezcla de gases ideales. Sin embargo, existen modelos de mezclas no ideales que aún así cumplen las condiciones de mezcla ideal. 

Para la mezcla de gases ideales, se considera un compartimento de volumen $Vc_T$, donde en el estado inicial cada gas ideal se encuentra en un compartimento $Vc_i$. Todos los compartimentos se encuentran dividido por paredes móviles, de forma tal que se encuentran inicialmente en equilibrio mecánico. Esto da las condiciones inciales:
$$
\begin{align*}
n &= \sum_{i} n_{i} &
Vc_{T} &= \sum_{i} Vc_{i} & 
V_{i} &= Vc_{i} &
p_{i}^{ini} &= p^{0}
\end{align*}
$$
Para la mezcla, se remueven todas las paredes, de forma tal que todos los gases terminan ocupando el total del recipiente. Durante la mezcla, el sistema se mantiene a $T$ constante. Vale entonces para el estado final que:
$$
\begin{align*}
V_{i} &= Vc_{T} &
p_{i}^{f} &= p^{0} \frac{Vc_{i}}{Vc_{T}}
\end{align*}
$$
notemos que la presión total final es:
$$
\begin{equation*}
p = \sum_{i} p^{f}_{i} = \sum_{i} p^{0} \frac{Vc_{i}}{Vc_{T}} = p^{0} \frac{Vc_{T}}{Vc_{T}} = p^{0}
\end{equation*} 
$$
A partir de esto, podemos calcular el $\Delta_{mix}G$:
$$
\begin{align*}
\Delta_{mix}G &= \sum_{i} n_{i} (\mu_{i} - \mu_{i}^{*}) 
\\
&= \sum_{i} n_{i} \left( \mu_{i}^{\theta} + RT \ln \frac{p_{i}^{f}}{p^{\theta}} - \left( \mu_{i}^{\theta} + RT \ln \frac{p_{i}^{ini}}{p^{\theta}} \right) \right) 
\\
&= \sum_{i} n_{i} RT \ln \frac{p_{i}^{f}}{p_{i}^{ini}}
\end{align*}
$$
utilizando $p_{i}^{f} = p y_{i} = p^{0} y_{i}$ y $p_{i}^{ini} = p^{0}$ obtenemos:
$$
\begin{align*}
\Delta_{mix}G &= RT \sum_{i} n_{i} \ln \frac{p^{0}y_{i}}{p^{0}}
\\
\Delta_{mix} G &= RT \sum_{i} n_{i} \ln y_{i}
\end{align*}
$$
Sabiendo que $\Delta_{mix}G = \Delta_{mix}H - T\Delta_{mix}S$, ya que la mezcla se realiza a $T$ constante, podemos igualar lo obtenido término a término y notar que:
$$
\begin{align*}
\Delta_{mix}G &= \Delta_{mix} H - T \Delta_{mix}S = T \left( R \sum_{i} n_{i} \ln y_{i} \right) &\Rightarrow 
\Delta_{mix} H &= 0 &
\Delta_{mix} S &= -R\sum_{i} n_{i} \ln y_{i}
\end{align*}
$$
Por lo tanto, se define una mezcla ideal a aquella que cumple:
$$
\begin{equation}
\boxed{
\Delta_{mix}^{id}H = 0  \qquad 
\Delta_{mix}^{id}S = -R \sum_{i} n_{i} \ln y_{i}  \qquad 
\Delta_{mix}^{id} V = 0
}
\end{equation}
$$
donde la última igualdad sale de una de las condiciones iniciales, donde se estableció que $Vc_T = \sum_{i} Vc_{i}$.  De nuevo recordamos que hay mezclas que cumplen estas condiciones, pese a seguir el modelo de gases ideales. 

También es posible verificar que si $G^{ex}=0$, entonces la mezcla es ideal, ya que:
$$
\begin{align*}
G^{ex} = 0 = G-G^{id} \Rightarrow G=G^{id}
\end{align*}
$$
donde $G$ es la entalpía libre de la mezcla y $G^{id}$ es la entalpía libre de una mezcla ideal. 
### Nota adicional
Notemos que la entropía de mezcla no viene del hecho de "desordenar" al sistema, sino de que cada gas tiene un mayor volumen disponible. Esto hace que los niveles de energía estén más cerca y haya un mayor número de configuraciones accesibles. Para ver esto de forma práctica, podemos imaginar un proceso de mezclado diferente. Imaginamos dos pistones, cada uno de igual volumen $V$, donde están contenidos los gases 1 y 2. Ambos gases se introducen en un tercer recipiente, cuyo volumen también es $V$, donde se produce "el mezclado". 
En el sistema inicial, la presión de cada gas está dada por $p_i^{ini} = n_{i}RT/V$, mientras que en el sistema final, la presión final será la misma, puesto a que el $V$ es el mismo, con lo cuál $p_{i}^{f} = n_{i}RT/V$. Reemplazando estas presiones en el $\Delta_{mix}G$ se llega a que este debe ser nulo, demostrando que "mezclar cosas" no genera ningún en la entalpía libre. 

