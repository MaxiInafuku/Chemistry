# Ideales
Son gases cuya ecuación de estados está dada por:
$$
\begin{equation*}
pV = nRT
\end{equation*}
$$
Un gas ideal:
- No tiene interacción a larga distancia entre partículas
- La colisión entre sus partículas es elástica
- El volumen de cada partícula es despreciable frente al del recipiente
## Puro Ideal
Para un único gas el diferencial del potencial químico está dado por [[Potencial Químico]]:
$$
\begin{align*}
\mu &= \bar{G} 
\\ 
d\mu &= -\bar{S}dT + \bar{V}dp + \frac{\partial \bar{G}}{\partial n} dn
\end{align*}
$$
por lo tanto,
$$
\begin{align*}
\left( \frac{\partial \mu}{\partial p} \right)_{T,n} = \bar{V} = \frac{RT}{p}
\end{align*}
$$
Integrando a ambos lados con $T$ constante:
$$
\begin{align*}
\mu(p) - \mu(p^{\theta}) = RT\ln\left( \frac{p}{p^\theta} \right)
\end{align*}
$$
$$
\begin{equation*}
\boxed{
\mu(p,T) = \mu(p^\theta,T) + RT \ln \left( \frac{p}{p^\theta} \right)
}
\end{equation*}
$$
por convención se toma $p^\theta=1$bar.
## Mezcla ideal
Para un sistema multicomponente vale que ([[Potencial Químico]]):
$$
\begin{equation*}
d\mu_{i} = -\bar{S}_{i} dT + \bar{V}_{i} dp +\sum_{j} \frac{ \partial \mu_{i} }{ \partial n_{j} } dn_{j}
\end{equation*}
$$
con lo que:
$$
\begin{equation*}
\left( \frac{ \partial \mu_{i} }{ \partial p }  \right)_{T,n_{j}} = \bar{V}_{i} = \left( \frac{ \partial V }{ \partial n_{i} }  \right)_{T,p.n_{j\neq i}}
\end{equation*}
$$
<u>Nota</u>: también puede derivarse esta igualdad por Maxwell, en base al potencial termodinámico $G$. 

Para gases ideales vale que:
$$
\begin{align*}
p &= \frac{\sum_{i} n_{i}RT}{V} \Leftrightarrow V = \frac{\sum_{i} n_{i}RT}{p}
\Rightarrow 
\bar{V}_{i} = \frac{RT}{p}
\end{align*}
$$
Por lo tanto, tenemos que:
$$
\begin{equation*}
\left( \frac{ \partial \mu_{i} }{ \partial p }  \right)_{T,n_{j}} = \frac{RT}{p}
\end{equation*}
$$
en general, se busca expresar el potencial de un gas en función de su presión parcial. Para eso buscamos la derivada respecto a la presión parcial:
$$
\begin{align*}
\left( \frac{ \partial \mu_{i} }{ \partial p }  \right)_{T,n_{j}} =
\left( \frac{ \partial \mu_{i} }{ \partial p_{i} }  \right)_{T,n_{j}} \left( \frac{ \partial p_{i} }{ \partial p }  \right)_{T,n_{j}} =
\left( \frac{ \partial \mu_{i} }{ \partial p_{i} }  \right)_{T,n_{j}} y_{i}
\end{align*}
$$
donde se utilizó que $p_i = p y_i$. 

Se tiene entonces que:
$$
\begin{align*}
\left( \frac{ \partial \mu_{i} }{ \partial p_{i} }  \right)_{T,n_{j}} y_{i} &= 
\frac{RT}{p} 
\\
\left( \frac{ \partial \mu_{i} }{ \partial p_{i} }  \right)_{T,n_{j}} &= 
\frac{RT}{py_{i}} =
\frac{RT}{p_{i}}
\\
\mu_{i}(T,p) - \mu_{i}(T,p^{\theta}) &= \int_{0}^{p_{i}} \frac{RT}{p_{i}} dp_{i}
\\
\mu_{i}(T,p) &= \mu_{i}(T,p^{\theta}) + RT \ln \frac{p_{i}}{p_{i}^{\theta}}
\end{align*} 
$$
donde por convención se suele tomar $p_{i}^{\theta} = p^{\theta} = 1$ bar.
$$
\begin{equation}
\boxed{
\mu_{i}(T,p) = \mu_{i}(T,p^{\theta}) + RT \ln \frac{p_{i}}{p^{\theta}}
}
\end{equation}
$$

# Gases no ideal
## Gas no ideal puro
Para un "gas real" se parte de la definición del potencial químico de gas ideal y simplemente se agrega un factor de corrección empírico a la presión, conocido como coeficiente de fugacidad $\varphi$.  Se expresa entonces el potencial químico de un gas no ideal como:
$$
\begin{equation*}
\boxed{
\mu(T,p) = \mu(T,p^{\theta}) + RT \ln \frac{f}{p^{\theta}} \qquad 
f = p\varphi
}
\end{equation*}
$$
donde el estado estándar está dado por $p^{\theta} = 1$ bar de gas ideal. 

La idea de llegar a esta expresión, desde gases ideales, se basa en la ecuación:
$$
\begin{align*}
\left( \frac{ \partial \mu }{ \partial p }  \right)_{T,n} = \bar{V}
\end{align*}
$$
La integración se realiza en dos partes:
- La primera desde la presión del estado estándar $p^{\theta}$ hasta $p\to 0$, pero a lo largo de la curva ideal. 
- La segunda desde $p \to 0$ a lo largo de la curva real. 
$$
\begin{align*}
\mu(T,p) - \mu(T,p^{\theta}) = \int_{p^{\theta}}^{p\to0} \bar{V}_{id} dp + \int_{p\to0}^{p} \bar{V} dp = RT \ln \frac{f}{p^{\theta}}
\end{align*}
$$
El "truco" está en que el $\bar{V}_{id}$ y $\bar{V}$ convergen al mismo punto cuando $p\to0$, ya que a presiones bajas, todo gas se tiende a comportar de forma ideal. Por ejemplo, si la siguiente curva representa el volumen molar de un gas ideal (la gris) y otro real (la roja), se integraría por la gris desde 1 bar hasta $p\to 0$ y luego desde $p\to 0$ hasta la presión deseada por la curva roja. Esquemáticamente, el término $RT\ln(f/p^{\theta})$ se correspondería a la resta entre el área bajo la curva roja hasta la presión $p$ menos el área bajo la curva gris hasta la presión $p^{\theta}$. 
![[Pasted image 20250827144109.png|center]]

Es común calcular coeficientes de fugacidad en base a el factor de compresibilidad [[Z]]. Partiendo de la igualdad anterior:
$$
\begin{align*}
\int_{p^{\theta}}^{p\to0} \bar{V}_{id} dp + \int_{p\to0}^{p} \bar{V} dp &= RT \ln \frac{f}{p^{\theta}} 
= RT \ln \frac{p}{p^{\theta}} + RT \ln \varphi 
\end{align*}
$$
Sabiendo que:
$$
\begin{equation*}
RT\ln \frac{p}{p^{\theta}} = \mu_{id}(T,p)-\mu_{id}(T,p^{\theta}) =\int_{p^{\theta}}^{p} \bar{V}_{id} 
\end{equation*}
$$
podemos escribir:
$$
\begin{align*}
\int_{p^{\theta}}^{p} \bar{V}_{id} + RT \ln \varphi &= \int_{p^{\theta}}^{p\to0} \bar{V}_{id} dp + \int_{p\to0}^{p} \bar{V} dp
\\
RT \ln\varphi &= \int_{p\to 0}^{p} (\bar{V} - \bar{V}_{id} ) dp
\end{align*}
$$
Finalmente, para dejar el resultado expresado en función de $Z$ escribimos:
$$
\begin{align*}
\bar{V} &= \frac{RTZ}{p} &
\bar{V}_{id} &= \frac{RT}{p} &\Rightarrow 
RT \ln \varphi &= \int_{p\to0}^{p} \frac{RT}{p} (Z-1) dp 
\end{align*}
$$
Dado a que consideramos $T$ constante en todo el proceso (esto viene de haber usado la derivada a $T$ y $n$ constantes), se obtiene:
$$
\begin{equation}
\boxed{
\ln \varphi = \int_{p\to0}^{p} \frac{Z-1}{p}dp
}
\end{equation}
$$


