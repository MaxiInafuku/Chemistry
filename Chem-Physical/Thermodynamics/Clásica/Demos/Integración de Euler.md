Se define una propiedad extensiva $X$ como aquella que cumple con:
$$
\begin{equation*}
k X(p,q,x,y) = X(p,q,kx,ky)
\end{equation*}
$$
dónde $p,q$ son propiedades intensivas y $x,y$ extensivas.

Por integración de Euler se tiene que:
$$
\begin{equation*}
\boxed{X(p,q,x,y) = \frac{ \partial X }{ \partial x } x + \frac{ \partial X }{ \partial y } y }
\end{equation*}
$$
### Demo:
Partiendo de la definición de función extensiva, basta con derivar respecto a $k$ a ambos lados:
$$
\begin{align*}
	X(p,q,x,y) &= \frac{ \partial X }{ \partial (kx) } x + \frac{ \partial X }{ \partial (ky) } y
\end{align*}
$$
donde dado a que $k$ es una variable auxiliar arbitraria, basta con tomar $k=1$ para llegar a la expresión dada por la integración de Euler. 

### Aplicaciones:
El volumen $V$ es una función extensiva que depende de $T,p,n_i$. Por lo tanto,
$$
\begin{equation*}
V(T,p,n_{i}) = \sum_{i} \bar{V}_{i} n_{i} \qquad 
\bar{V}_{i} := \left( \frac{ \partial V }{ \partial n_{i} } \right)_{T,p,n_{j\neq i}}
\end{equation*}
$$
La energía interna, así como todos los potenciales termodinámicos son funciones extensivas, por lo tanto:
$$
\begin{align*}
U &= TS - pV + \sum_{i} \mu_{i} n_{i} & 
T &= \left( \frac{ \partial U }{ \partial S }  \right)_{V,n_{i}} &
p &= -\left( \frac{ \partial U }{ \partial V } \right)_{S,n_{i}} &
\mu_{i} &= \left( \frac{ \partial U }{ \partial n_{i} }  \right)_{S,V,n_{i\neq j}}
\\
H &= TS + \sum_{i} \mu_{i} n_{i} & 
T &= \left( \frac{ \partial H }{ \partial S }  \right)_{p,n_{i}} & 
\mu_{i} &= \left( \frac{ \partial H }{ \partial n_{i} }  \right)_{S,p,n_{i\neq j}}
\\
F &= -pV + \sum_{i} \mu_{i} n_{i} & 
p &= -\left( \frac{ \partial U }{ \partial V } \right)_{T,n_{i}} &
\mu_{i} &= \left( \frac{ \partial U }{ \partial n_{i} }  \right)_{T,V,n_{i\neq j}}
\\
G &= \sum_{i} \mu_{i} n_{i} & 
\mu_{i} &= \left( \frac{ \partial U }{ \partial n_{i} }  \right)_{T,p, n_{j\neq i}}
\end{align*}
$$
donde se obviaron el resto de las variables extensivas $X_j$ y sus conjugadas $P_j$, pero si se las quisiera tener en cuenta, basta con agregar el término:
$$
\begin{equation*}
\sum_{j} P_{j}X_{j} \qquad P_{j} = \frac{ \partial \Phi }{ \partial X_{j} } 
\end{equation*}
$$
siendo $\Phi$ el potencial termodinámico correspondiente. 