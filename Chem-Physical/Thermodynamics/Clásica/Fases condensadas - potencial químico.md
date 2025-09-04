# Escalas
Para definir el potencial químico de una fase condensada se puede partir de la ley de Raoult o la de Henry. Según esta elección, se define la escala en la que está escrito el potencial químico. 

## Raoult ideal
En la escala de Raoult se utiliza la ley de Raoult que establece que:
$$
\begin{equation*}
p_{i} = p_{i}^{*} x_{i}
\end{equation*}
$$
donde $p_i^*$ es la presión de vapor de la fase condensada pura y $x_i$ la fracción molar del $i$-ésimo componente en la fase condensada. Esta ley se cumple a bajas presiones de vapor y para componentes aproximadamente puros ($x_{i}\to1$). 

Para poder definir el potencial químico de una fase condensada, imaginamos un sistema en el que este se encuentra en contacto con su vapor. Por lo tanto, en equilibrio, puedo igualar sus potenciales químicos. 
$$
\begin{equation*}
\mu_{i}^{vap} = \mu_{i}^{fc}
\end{equation*}
$$
donde $\mu_i^{fc}$ es el potencial químico de la fase condensada correspondiente. Dado a que conocemos como se escribe el potencial químico de un gas ideal ([[Gases - potencial químico]]), la ecuación resulta:
$$
\begin{align*}
\mu_{i}^{fc} &= \mu_{i}^{vap}
= \mu_{i}^{\theta} + RT \ln \frac{p_{i}}{p^{\theta}}
\\
\mu_{i}^{fc} &= \mu_{i}^{\theta} + RT \ln \frac{p_{i}^{*}x_{i}}{p^{\theta}}
\\
\mu_{i}^{fc} &= \mu_{i}^{\theta} + RT \ln \frac{p_{i}^{*}}{p^{\theta}} + RT \ln x_{i}
\end{align*}
$$
El motivo de escribir $p_i$ utilizando la ley de Raoult, es dejar expresado el potencial químico en función de la fracción molar del $i$-ésimo componente en la fase condensada. Además, notamos que $\mu_i^\theta + RT \ln p_{i}^{*}/p^{\theta}$ es el potencial químico del $i$-ésimo componente en otro sistema, un sistema en donde él está puro y solo, en contacto con su vapor. Por lo que podemos escribir:
$$
\begin{equation}
\boxed{
\mu_{i}^{fc} = \mu_{i}^{*} + RT \ln x_{i} \qquad 
\mu_{i}^{*} = \mu_{i}^{\theta} + RT \ln \frac{p_{i}^{*}}{p^{\theta}}
}
\end{equation}
$$
donde $\mu_i^*$ es el potencial químico del vapor en contacto con la fase condensada pura. 

## Henry ideal
Se parte de la ley de Henry, que establece:
$$
\begin{equation*}
p_{i} = K_{i}^{H}(p_{j}) x_{i}
\end{equation*}
$$
donde $K_i^H(p_j)$ es la constante de Henry, la cuál depende de las presiones de vapor de los otros componentes en la mezcla. La ley de Henry es válida para compuestos que estén muy diluidos ($x_{i}\to0$) en la mezcla, luego presenta desviaciones. 
El razonamiento es similar al de Raoult, con lo que se llega a:
$$
\begin{equation}
\boxed{
\mu_{i}^{fc} = \mu_{i}^{\infty} + RT \ln x_{i} \qquad 
\mu_{i}^{\infty} = \mu_{i}^{\theta} + RT \ln \frac{K_{i}^{H}(p_{j})}{p^{\theta}}
}
\end{equation}
$$
donde esta vez, el $\mu_i^\infty$ representa el potencial químico que tendría el $i$-ésimo componente si estuviera en dilución infinita, en una mezcla donde lo que predomina son todo el resto de los componentes $j$. 

## Relación de escalas ideales
Para relacionar ambas escalas en el caso de Raoult y Herny ideales, se parte de las leyes:
$$
\begin{align*}
\text{Raoult } p_{i} &= p_{i}^{*}x_{i} 
\\
\text{Henry } p_{i} &= K_{i}^{H,id}x_{i}
\end{align*}
$$
Asumiendo que estas leyes son válidas para todo el intervalo de $x_i \in [0,1]$, tenemos que:
$$
\begin{equation*}
p_{i}^{*}x_{i} = K_{i}^{H} x_{i} \Rightarrow p^{*}_{i} = K_{i}^{H,id}
\end{equation*}
$$
Esto lleva a que 
$$
\begin{equation*}
\mu_{i}^{*,id} = \mu_{i}^{\theta} + RT \ln \frac{p_{i}^{*}}{p^{\theta}} = 
\mu_{i}^{\theta} + RT \ln \frac{K_{i}^{H,id}}{p^{\theta}} = 
\mu_{i}^{\infty,id} \Rightarrow 
\boxed{
\mu_{i}^{*,id} = \mu_{i}^{\infty,id}
}
\end{equation*}
$$
## Raoult no ideal
Para el caso no ideal, simplemente se modifica la ley de Raoult de forma tal que ahora se escribe:
$$
\begin{equation}
\boxed{
f_{i} = f_{i}^{*} a_{i}^{R} \qquad 
a_{i}^{R} = x_{i} \gamma_{i}^{R}
}
\end{equation}
$$
de la misma forma que se hizo para el caso de Raoult ideal, pero pensando ahora que mi fase condensada se encuentra en equilibrio con su vapor de fugacidad $f_i$, puede llegarse a que:
$$
\begin{equation}
\boxed{
\mu_{i} = \mu_{i}^{*} + RT \ln a_{i}^{R} \qquad 
\mu_{i}^{*} = \mu_{i}^{\theta} + RT \ln \frac{f_{i}^{*}}{p^{\theta}}
}
\end{equation}
$$
donde $f_i^*$ es la fugacidad del vapor del que se encontraría en equilibrio con el $i$-ésimo componente si este estuviera puro. Debe notarse que en principio, el $\mu_i^{*,id}$ difiere del $\mu_i^*$. 
$$
\begin{equation*}
\mu_{i}^{*} - \mu_{i}^{*,id} = \mu_{i}^{\theta} + RT \ln \frac{f_{i}^{*}}{p^{\theta}} - \mu_{i}^{\theta} + RT \ln p_{i}^{*} = 
RT \ln \varphi_{i}^{*}
\end{equation*}
$$
## Henry no ideal
La ley de Henry no ideal se escribe como:
$$
\begin{equation}
\boxed{
f_{i} = K_{i}^{H}(f_{j}) a_{i}^{H} \qquad 
a_{i}^{H} = x_{i} \gamma_{i}^{H}
}
\end{equation}
$$
si se sigue el mismo razonamiento que para el caso de Raoult ideal, pero considerando que la fase condensada se encuentra en equilibrio con su vapor de fugacidad $f_i$, se llega a:
$$
\begin{equation}
\boxed{
\mu_{i} = \mu_{i}^{\infty} + RT \ln a_{i}^{H} \qquad 
\mu_{i}^{\infty} = \mu_{i}^{\theta} + RT \ln \frac{K_{i}^{H}(f_{j})}{p^\theta}
}
\end{equation}
$$
una vez más, la constante de Henry no ideal y la del caso ideal no son iguales:
$$
\begin{equation*}
\mu_{i}^{\infty} - \mu_{i}^{\infty,id} = 
\mu_{i}^{\theta} + RT \ln \frac{K_{i}^{H}}{p^{\theta}} - \mu_{i}^{\theta} + RT \ln \frac{K_{i}^{H,id}}{p^{\theta}} = 
RT \ln \frac{K_{i}^{H}}{K_{i}^{H,id}}
\end{equation*}
$$
recordando que $K_i^{H,id} = p_i^*$ podemos llegar a:
$$
\begin{equation*}
\mu_{i}^{\infty} - \mu_{i}^{\infty,id} = RT \ln \frac{K_{i}^{H}}{p_{i}^{*}}
\end{equation*}
$$
## Relación de escalas no ideales
Para el caso no ideal, comparando ambas leyes puede obtenerse:
$$
\begin{align*}
\text{Raoult } f_{i}&= f_{i}^{*} \gamma_{i}^{R} x_{i} 
\\
\text{Henry } f_{i} &= K_{i}^{H} \gamma_{i}^{H} x_{i}
\end{align*}
$$
Igualando ambas expresiones:
$$
\begin{equation}
\boxed{
f_{i}^{*} \gamma_{i}^{R} = K_{i}^{H} \gamma_{i}^{H}
}
\end{equation}
$$
