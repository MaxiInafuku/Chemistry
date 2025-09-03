Se define una propiedad parcial molar como la variación infinitesimal de una función extensiva ($X$) al variar una de sus componentes $n_{i}$, a propiedades intensivas $(P_{l})$ constantes. 
$$
\begin{equation*}
\bar{X}_{i} := \left( \frac{ \partial X }{ \partial n_{i} }  \right)_{n_{j\neq i}, x_{k}, P_{l} }
\end{equation*}
$$
donde $x_k$ incluye al resto de las variables extensivas del sistema, además de $n_i$.

# Cálculo a partir de propiedades molares.
Es posible calcular una propiedad parcial molar a partir de la función por mol:
$$
\begin{equation}
\bar{X} = \frac{X}{n} \qquad n = \sum_{i} n_{i}
\end{equation}
$$
Para ello, basta partir de la definición:
$$
\begin{align*}
\bar{X}_{i} &= \frac{ \partial X }{ \partial n_{i} } =
\frac{ \partial (n \bar{X}) }{ \partial n_{i} } = 
\bar{X} + n \frac{ \partial \bar{X} }{ \partial n_{i} } = 
\bar{X} + n\frac{ \partial \bar{X} }{ \partial x_{i} } \frac{ \partial x_{i} }{ \partial n_{i} }  
\end{align*}
$$
Usando:
$$
\begin{equation*}
\frac{ \partial x_{i} }{ \partial n_{i} } = 
\frac{ \partial (n_{i}/n) }{ \partial n_{i} } =
\frac{n-n_{i}}{n^{2}} = 
\frac{1}{n} (1-x_{i})
\end{equation*}
$$
se obtiene:
$$
\begin{equation}
\boxed{
\bar{X}_{i} = \bar{X} + (1-x_{i}) \frac{ \partial \bar{X} }{ \partial x_{i} } 
}
\end{equation}
$$
Esta última ecuación, muestra de forma implícita que la propiedad parcial molar $\bar{X}_{i}$ tiene $N-1$ variables (considerando que la $X$ tienen $N$ variables), ya que solo depende de la propiedad molar $\bar{X}$. Como se vio en [[Integración de Euler#Propiedad molar]], $\bar{X}$ es función de $N-1$ variables. 
# Error en apunte viejo
Dice que una propiedad parcial molar es una propiedad intensiva. Para ver esto, parte de la definición de propiedad extensiva:
$$
\begin{align}
k X(n_{i},x_{j},P_{l}) &= X(kn_{i},kx_{j},P_{l})
\end{align}
$$
derivando a ambos lados respecto a $n_m$ particular obtenemos:
$$
\begin{align*}
\cancel{k} \frac{ \partial X }{ \partial n_{m} }(n_{i},x_{j},P_{l})  &= \frac{ \partial X }{ \partial kn_{m} }(kn_{i},kx_{j},P_{l}) \cancel{k} = f(kni,kx_{j},P_{l})
\end{align*}
$$
Se escoge $k=n = \sum_{i} n_{i}$, obtenemos:
$$
\begin{align*}
f(x_{i}, \bar{x}_{j}, P_{l}) = \frac{ \partial X }{ \partial n_{m} }(n_{i},x_{j},P_{l})
\end{align*}
$$
y esto pretende mostrar que como ahora la propiedad parcial $(\partial X / \partial n_{m})_{n_{i},x_{j},P_{l}}$ depende solo de las fracciones molares $x_i$ y las cantidades molares $\bar{x}_j=x_j/n$, como todas estas cantidades son cocientes de funciones extensivas, son cantidades intensivas. Así, la propiedad parcial $(\partial X / \partial n_{m})_{n_{i},x_{j},P_{l}}$ depende solamente de cantidades intensivas y esto la vuelva una función no extensiva. 
Esta demostración no es correcta porque si se establece $k=n$, como $n$ depende de $n_i$, habría que hacer la derivada correctamente, es decir, falta una derivada respecto a $k=n$ también.

