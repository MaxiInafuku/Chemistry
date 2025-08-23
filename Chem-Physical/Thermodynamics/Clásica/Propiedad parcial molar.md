Se define una propiedad parcial molar como la variación infinitesimal de una función extensiva ($X$) al variar una de sus componentes $n_{i}$, a propiedades intensivas $(P_{l})$ constantes. 
$$
\begin{equation*}
\bar{X}_{i} := \left( \frac{ \partial X }{ \partial n_{i} }  \right)_{n_{j\neq i}, x_{k}, P_{l} }
\end{equation*}
$$
donde $x_j$ incluye al resto de las variables extensivas del sistema, además de $n_i$.




### Error en apunte viejo
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
Esto no es especial por varios motivos:
1) Asume que $n$ será constante y eso puede no pasar en una reacción química, donde el número de moles totales no se conserva.
2) Es un razonamiento trivial, se puede simplemente partir de la definición de propiedad extensiva: $k X(n_{i},x_{j},P_{l}) = X(kn_{i},kx_{j},P_{l})$ y establecer $k=n$, con lo que se demuestra que cualquier propiedad molar es intensiva. 
3) Si se establece $k=n$, como $n$ depende de $n_i$, habría que hacer la derivada correctamente, es decir, falta una derivada respecto a $k=n$ también.

