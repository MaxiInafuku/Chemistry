El potencial químico se define como la derivada de la energía interna, respecto del número de moles, su definición parte de la relación fundamental:
$$
\begin{align}
dU& = TdS - pdV + \sum_{i} \mu_{i} dn_{i} + \sum_{j} P_{j} dX_{j} & 
\mu_{i} &= \left( \frac{ \partial U }{ \partial n_{i} } \right)_{S,V}
\end{align}
$$
donde $P_{j}$ representa otras posibles variables intensivas con sus respectivas variables extensivas $X_{j}$ conjugadas, siendo estos posibles términos de trabajo adicional. 

A partir de las distintas transformadas de Legendre de la energía interna [[Potenciales termodinámicos]], se pueden obtener los otros potenciales termodinámicos:
$$
\begin{align}
dH& = TdS + Vdp + \sum_{i} \mu_{i} dn_{i} + \sum_{j} P_{j} dX_{j} & 
\mu_{i} &= \left( \frac{ \partial H }{ \partial n_{i} } \right)_{S,p}  \\
dF& = -SdT - pdV + \sum_{i} \mu_{i} dn_{i} + \sum_{j} P_{j} dX_{j} & 
\mu_{i} &= \left( \frac{ \partial F }{ \partial n_{i} } \right)_{T,V}   \\
dG& = -SdT + Vdp + \sum_{i} \mu_{i} dn_{i} + \sum_{j} P_{j} dX_{j} & 
\mu_{i} &= \left( \frac{ \partial G }{ \partial n_{i} } \right)_{T,p}
\end{align}
$$
Partiendo de la igualdad con el $dG$, sabemos que:
$$
\begin{equation*}
\mu_{i} = \left( \frac{ \partial G }{ \partial n_{i} }  \right)_{T,p} = f(T,p,n_{i})
\end{equation*}
$$
Por lo tanto, vale que:
$$
\begin{align*}
	d\mu_{i} = \left( \frac{ \partial \mu_{i} }{ \partial T }  \right)_{p,n_{i}} dT + \left( \frac{ \partial \mu_{i} }{ \partial p }  \right)_{T,n_{i}} dp + 
	\sum_{j} \left( \frac{ \partial \mu_{i} }{ \partial n_{j} }  \right)_{p,n_{k\neq j}} dn_{j}
\end{align*}
$$
Utilizando que
$$
\begin{align*}
\left( \frac{ \partial \mu_{i} }{ \partial T }  \right)_{p,n_{i}} &= 
\frac{ \partial^{2} G }{ \partial n_{i} \partial T } = 
\frac{ \partial^{2} G }{ \partial T \partial n_{i} } = 
\frac{ \partial  }{ \partial n_{i} } \left( \frac{ \partial G }{ \partial T} \right) & 
-S &= \left( \frac{ \partial G }{ \partial T } \right)_{p,n_{i}} 
\\
\left( \frac{ \partial \mu_{i} }{ \partial p }  \right)_{T,n_{i}} &= 
\frac{ \partial^{2} G }{ \partial n_{i} \partial p } = 
\frac{ \partial^{2} G }{ \partial p \partial n_{i} } = 
\frac{ \partial  }{ \partial n_{i} } \left( \frac{ \partial G }{ \partial p} \right) &
V &= \left( \frac{ \partial G }{ \partial p }  \right)_{T,n_{i}}
\end{align*}
$$
se obtiene
$$
\begin{align*}

\left( \frac{ \partial \mu_{i} }{ \partial T }  \right)_{p,n_{i}} &= 
-\left( \frac{ \partial S }{ \partial n_{i} }  \right)_{T,p,n_{j\neq i}} = 
-\bar{S}_{i}
\\
\left( \frac{ \partial \mu_{i} }{ \partial p }  \right)_{p,n_{i}} &= 
\left( \frac{ \partial V }{ \partial n_{i} }  \right)_{T,p,n_{j\neq i}} = 
\bar{V}_{i}
\end{align*}
$$
por lo que puede escribirse el diferencial del potencial químico en término de propiedades parciales molares como:
$$
\begin{equation*}
\boxed{
d\mu_{i} = -\bar{S}_{i} dT + \bar{V}_{i} dp + \sum_{j} \left( \frac{ \partial \mu_{i} }{ \partial n_{j} }  \right) dn_{j}
}
\end{equation*}
$$
Para el caso particular de un compuesto puro, por integración de Euler ([[Integración de Euler#Potenciales termodinámicos]]) se tiene que:
$$
\begin{align*}
G &= \mu n \Rightarrow
\frac{G}{n} := \bar{G} = \mu 
\end{align*}
$$
