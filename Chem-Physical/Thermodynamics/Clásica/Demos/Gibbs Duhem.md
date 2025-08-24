- $X = f(X_{j}, P_{k})$
- $X_j$ las variables extensivas, siendo sus intensivas conjugadas $\partial X / \partial X_{j} = Q_{j}$
- $P_k$ las variables intensivas, siendo sus extensivas conjugadas $\partial X / \partial P_{k} = Y_{k}$
$$
\begin{equation*}
\boxed{
\sum_{k} Y_{k} dP_{k} = \sum_{j} X_{j} dQ_{j}
}
\end{equation*}
$$
### Demo:
Por ser $X = f(X_{j}, P_{l})$ se tiene que [[Integración de Euler#Propiedad extensiva]]:
$$
\begin{equation*}
dX = \sum_{j} \frac{ \partial X }{ \partial X_{j} } dX_{j} + \sum_{k} \frac{ \partial X }{ \partial P_{k} }  dP_{k} 
= \sum_{j} Q_{j} dX_{j} + \sum_{k} Y_{k} dP_{k}
\end{equation*}
$$
Por otro lado, por integración de Euler de la función extensiva podemos escribir:
$$
\begin{equation*}
X = \sum_{j} \frac{ \partial X }{ \partial X_{j} } X_{j} 
= \sum_{j} Q_{j} X_{j} 
\end{equation*}
$$
diferenciando a ambos lados obtenemos:
$$
\begin{align*}
dX = \sum_{j} Q_{j} dX_{j} + X_{j} dQ_{j} 
\end{align*}
$$

Igualando ambos diferenciales:
$$
\begin{align*}
\cancel{\sum_{j} Q_{j} dX_{j}} + \sum_{k} Y_{k} dP_{k} = \sum_{j} \cancel{Q_{j} dX_{j}} + X_{j} dQ_{j} 
\\
\sum_{k} Y_{k} dP_{k} = \sum_{j} X_{j} dQ_{j}
\end{align*}
$$
# Aplicación
Para el caso de $U(S,V,n_i)$, se tiene que:
$$
\begin{equation*}
0 = SdT - Vdp + \sum_{i} n_{i} d\mu_{i}
\end{equation*}
$$
Se puede partir de cualquier potencial termodinámico y el resultado será el mismo. Por ejemplo, partiendo de $G$:
$$
\begin{equation*}
-SdT + Vdp = \sum_{i} n_{i} d\mu_{i}
\end{equation*}
$$