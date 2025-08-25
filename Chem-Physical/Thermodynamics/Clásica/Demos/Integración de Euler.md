# Propiedad extensiva
La definición coloquial de una propiedad extensiva, es que esta depende de "la cantidad de materia". La formalización de este concepto dice que si "la cantidad de materia aumenta $k$ veces, así también lo hará la propiedad extensiva". Un ejemplo trivial es tener un volumen $V$ de un único componente, cuyo número de moles es $n$. Si aumentamos $n$ unas $k$ veces, el volumen también lo hará. De esta forma vale que:
$$
\begin{equation*}
kV(n,T,p) = V(kn, T, p)
\end{equation*}
$$
Podemos notar que el volumen depende también de $T,p$. Sin embargo, un aumento de $k$ veces de la $T$ o la $p$ no necesariamente aumenta $k$ veces el volumen, como lo haría aumentar la cantidad $n$. 

Se define una propiedad extensiva $X$ como aquella que cumple con:
$$
\begin{equation*}
\boxed{
k X(p,q,x,y) = X(p,q,kx,ky)
}
\end{equation*}
$$
dónde $p,q$ son propiedades intensivas y $x,y$ extensivas.

**Nota**: no todos los sistemas cumplen extensividad. Un caso extremo es un sistema con una única molécula. Si duplicamos la cantidad de moléculas, la interacción entre moléculas hará que la energía interna (en principio una propiedad extensiva) no se duplique ya que aparece el término de interacciones. Otro ejemplo más útil son nanopartículas. Si en una nanopartícula se duplica la cantidad de átomos, propiedades extensivas en macrosistemas, como su energía interna, pueden variar de forma no lineal con el número de partículas que conforman a la nanopartícula. 
## Propiedad molar:
La mayoría de las funciones extensivas depende del número de moles de sus componentes. Podemos escribir así:
$$
\begin{equation*}
kX(n_{i}, X_{j}, P_{k}) = X(kn_{i}, kX_{j}, P_{k})
\end{equation*}
$$
donde $X_j$ son otras propiedades extensivas y $P_k$ propiedades intensivas.

Si se elige $k=n= \sum_{i} n_{i}$:
$$
\begin{equation*}
\bar{X} := \frac{X}{n} = X(x_{i}, \bar{X_{j}}, P_{k}) \qquad 
x_{i} := \frac{n_{i}}{n} \qquad 
\bar{X}_{j} := \frac{X_{j}}{n}
\end{equation*}
$$
es fácil ver que:
$$
\begin{equation*}
\sum_{i} x_{i} = \sum_{i} \frac{n_{i}}{n} = 1
\end{equation*}
$$
por lo tanto, si se tienen $N$ componentes en el sistema, la cantidad de variables $x_i$ libres es $N-1$, ya que esta última ecuación restringe la cantidad de $x_N$ (o cualquier otra) a $x_{N} = 1-\sum_{i} n_{i\neq N}$. 
# Integración de Euler
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

# Aplicaciones:
### Volumen
El volumen $V$ es una función extensiva que depende de $T,p,n_i$. Por lo tanto,
$$
\begin{equation*}
V(T,p,n_{i}) = \sum_{i} \bar{V}_{i} n_{i} \qquad 
\bar{V}_{i} := \left( \frac{ \partial V }{ \partial n_{i} } \right)_{T,p,n_{j\neq i}}
\end{equation*}
$$
donde $\bar{V}_{i}$ son los volúmenes parciales molares ([[Propiedad parcial molar]]). Cabe destacar que si se divide a ambos lados por $n$, se obtiene:
$$
\begin{equation*}
\bar{V} := \frac{V}{n} = \sum_{i} \bar{V}_{i} x_{i} \qquad 
x_{i} := \frac{n_{i}}{n} \qquad 
n = \sum_{i} n_{i}
\end{equation*}
$$
podemos notar que al trabajar con fracciones molares, en lugar de número de moles, tenemos una ecuación más. Esto hace que la función $\bar{V}$ dependa de una variable menos. En el caso simple de dos componentes $\bar{V} = f(x_{1},T,p)$ y pierde la dependencia con $x_{2}$ ya que sabemos que $x_{1}+x_{2}=1$.

### Potenciales termodinámicos
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
Notemos que dividir por $n$ a ambos lados, en cada una de las ecuaciones, tiene el mismo efecto de reducir el número de variables libres en uno [[Integración de Euler#Propiedad molar]].
$$
\begin{align*}
\bar{U} &= T\bar{S} - p\bar{V} + \sum_{i} \mu_{i} x_{i} &
\bar{H} &= T\bar{S} + \sum_{i} \mu_{i} x_{i}
\\
\bar{F} &= -p\bar{V} + \sum_{i} \mu_{i} x_{i} &
\bar{G} &= \sum_{i} \mu_{i} x_{i}
\end{align*}
$$
donde $x_{i}=n_{i} / n$ y por ende $\sum_{i} x_{i} = 1$.

