# Transformada de Legendre
Dada una función $f(x_{1},x_{2})$, podemos escribir su diferencia finita de acuerdo al teorema de Lagrange:
$$
\begin{align*}
f({x'_{1},x'_{2}})-f(x_{1},x_{2}) &= \frac{ \partial f }{ \partial x_{1} } (p_{1},p_{2}) (x_{1}'-x_{1}) + \frac{ \partial f }{ \partial x_{2} } (p_{1},p_{2}) (x_{2}'-x_{2}) 
\end{align*}
$$
Si se considera la $(x_{1}',x_{2}') \to (x_{1},x_{2})$ (y por ende $(p_{1},p_{2}) \to (x_{1},x_{2})$)se puede obtener la versión diferencial:
$$
\begin{align*}
df = \frac{ \partial f }{ \partial x_{1} } dx_1 + \frac{ \partial f }{ \partial x_{2} } dx_{2}
\end{align*}
$$
podemos ver que cada derivada parcial está acompañada de su variable correspondiente. 

Para conseguir una función $g$ que tenga como variables $x_{1}$ y $y_{2} = \partial f / \partial x_{2}$, se puede utilizar la transformada de Legendre. Esta nueva función $g$, que corresponde a la transformada de Legendre de $f$ se define como:
$$
\begin{align*}
\boxed{g(x_{1},y_{2}) = f(x_{1},x_{2}) - x_{2} y_{2} \qquad y_{2}:= \frac{ \partial f }{ \partial x_{2} } } 
\end{align*}
$$
Estudiando el diferencial de esta función $g$, podemos ver que:
$$
\begin{align*}
dg &= df - y_{2} dx_{2} - x_{2} dy_{2} 
\\
dg &= \frac{ \partial f }{ \partial x_{1} } dx_1 + \frac{ \partial f }{ \partial x_{2} } dx_{2} - y_{2} dx_{2} - x_{2} dy_{2} 
= \frac{ \partial f }{ \partial x_{1} } dx_1 + \cancel{y_{2} dx_{2}} - \cancel{y_{2} dx_{2}} - x_{2} dy_{2} 
\\
dg &= \frac{ \partial f }{ \partial x_{1} } dx_1 - x_{2} dy_{2} 
\end{align*}
$$
esta última ecuación muestra que $x_1$ e $y_2$ son las variables de la nueva función $g$ y además que:
$$
\begin{equation*}
\boxed{\frac{ \partial g }{ \partial y_{2} } = -x_{2}}
\end{equation*}
$$

Una propiedad útil es que:
$$
\begin{equation*}
\boxed{\frac{ \partial^{2} g }{ \partial y_{2}^{2} } 
= -\frac{ \partial x_{2} }{ \partial y_{2} } 
= -\frac{1}{\partial ^2 f / \partial x_{2}^2} }
\end{equation*}
$$
Demo:
Sabemos que
$$
\begin{equation*}
	\frac{ \partial f }{ \partial x_{2} } = y_{2} 
\end{equation*}
$$
derivando a ambos lados respecto a $y_2$:
$$
\begin{align*}
\frac{ \partial^{2} f(x_{1},x_{2}) }{ \partial x_{2}^{2} }  \frac{ \partial x_{2} }{ \partial y_{2} } &= 1
\\
\frac{ \partial x_{2} }{ \partial y_{2} } &= \frac{1}{\partial^{2}f / \partial x_{2}^{2}}
\end{align*}
$$
recordando que $\frac{ \partial g }{ \partial y_{2} } = -x_{2}$, se obtiene que:
$$
\begin{equation*}
-\frac{ \partial^{2} g }{ \partial y_{2} } = \frac{1}{\partial^{2}f / \partial x_{2}^{2}}
\end{equation*}
$$
# Transformadas de Legendre de $U$.
La entalpía, es la transformada de Legendre de $U$ respecto a $(-p)$.
$$
\begin{align*}
H&:= U + pV 
\\
dH &= TdS + V dp + \sum_{i} \mu_{i} dn_{i} + \sum_{j} P_{j} dX_{j}
\\
\frac{ \partial^{2} H }{ \partial p^{2} } &= 
\left( \frac{ \partial V }{ \partial p } \right)_{S,n_{i},X_{j}} =
-\frac{1}{(\partial^{2}U / \partial V^{2})_{S,n_{j},X_{j}}} 
\end{align*}
$$
La energía libre de Helmholtz es la transformada de Legendre respecto a $T$.
$$
\begin{align*}
F &:= U - TS 
\\ 
dF &= -S dT - p dV + \sum_{i} \mu_{i} dn_{i} + \sum_{j} P_{j} dX_{j}
\\
\frac{ \partial^{2} F }{ \partial T^{2} } &= -\left( \frac{ \partial S }{ \partial T }  \right)_{V,n_{i}, X_{j}} = - \frac{1}{(\partial^{2}U / \partial S^{2})_{V,n_{j},X_{j}}}
\end{align*}
$$
La entalpía libre o energía libre de Gibbs es la transformada de Legendre respecto a $T$ y $p$. 
$$
\begin{align*}
G &:= U + pV - TS = H - TS 
\\
dG &= -SdT + Vdp + \sum_{i} \mu_{i} dn_{i} + \sum_{j} P_{j} dX_{j}
\\
\frac{ \partial^{2}G }{ \partial p^{2} } &= \left( \frac{ \partial V }{ \partial T }  \right)_{T,n_{i},X_{j}} 
= - \kappa_{T} V 
= - \frac{1}{(\partial^{2}U / \partial V^{2})_{S,n_{j},X_{j}}}
\end{align*}
$$

