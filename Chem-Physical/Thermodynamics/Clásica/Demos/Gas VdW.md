# Modelo:
- Esferas rígidas de radio $r$
- Potencial de interacción tipo dipolo-dipolo
- Aproximación de campo medio
El volumen excluido es aquel volumen que se excluye cuando dos partículas colisionan, por unidad de partícula. En un gas ideal no hay volumen excluido, ya que al ser las partículas puntuales, ambas "colisionan" solo cuando se encuentran en el mismo punto. Sin embargo, en un gas de VdW (y de esféras rígidas también), cuando dos partículas se encuentran, lo hacen a una distancia de $2R$. 
![[Pasted image 20250826131443.png|center|450]]
Por lo tanto, el volumen "ocupado" en esta colisión es de $4/3 \pi (2R)^3 = 8(4/3 \pi R^{3}) =8V_{esf}$, dado a que en el choque participan dos partículas, el volumen excluido (que se cuenta por unidad de partícula) es:
$$
\begin{equation*}
b' = \frac{8}{2}V_{esf} = 4 V_{esf} = 4 \left( \frac{4}{3} \pi R^{3} \right)
\end{equation*}
$$
Así, el volumen excluido para $N$ partículas es simplemente $Nb'$.
Experimentalmente, el parámetro $b'$ suele ser menor al calculado y a veces esto se atribuye a que las moléculas no son esferas rígidas, sino que poseen cierta capacidad de deformarse. 

El potencial de interacción de una molécula está dado por:
$$
\begin{equation*}
u(r) = 
\begin{cases}
\infty & r<R  \\
- \epsilon \left( \frac{2R}{r} \right)^{6} & r \geq R
\end{cases}
\end{equation*}
$$
# Función de partición
Como se utiliza la aproximación de campo medio, primero calculamos cuál es la energía promedio para un par de partículas.
$$
\begin{align*}
\phi_{par} &= \frac{1}{V} \int_{V} u(r) dV 
\\
&= \frac{1}{V} \int_{0}^{2\pi} \int_{0}^{\pi} \int_{2R}^{\infty} -\epsilon \left( \frac{2R}{r} \right)^{6} r^{2} \sin(\theta) d\phi d\theta dr
\\
&= -\frac{\epsilon (2R)^{6}}{V} 4\pi  \bigg(\frac{1}{3r^{3}} \bigg|_{2R}^{\infty} 
= - \frac{\epsilon}{V} \left( \frac{4}{3} \pi (2R)^{3} \right) 
\\
&= - \frac{\epsilon}{V} 8 V_{esf}
\end{align*}
$$
notemos que se integra de 0 a $\infty$ y esto no produce tanto error, pese a tener un recipiente finito, porque en general, las moléculas dejarán de interactuar a distancias macroscópicas. Dicho de otro modo, tal vez lo correcto sería integrar de $0$ a $10$ cm, pero para lo que son distancias e interacciones intermoleculares, 10 cm es infinito. 

Entonces, la energía promedio, debido a la interacción de la partícula 1 con la 2, la 1 con la 3, la 1 con la 4, etc. es $(N-1)\phi_{par} / 2$, ya que tengo $N-1$ pares (no cuento 1 con 1). Como $N$ anda por el orden de moles, podemos aproximar que, la energía de interacción de una única partícula, con todo el resto de las partículas es en promedio:
$$
\begin{align*}
\phi = N \frac{\phi_{par}}{2}
= -N \frac{\varepsilon}{V} \frac{8}{2} V_{esf} = -N\varepsilon \frac{b'}{V}
\end{align*}
$$
se suele llamar al término de interacción $a' = \varepsilon b'$, con lo cuál:
$$
\begin{equation*}
\phi = -N \frac{a'}{V}
\end{equation*}
$$
Asumimos entonces que este término de interacción es el mismo para cada partícula individual, con lo cuál, la energía de una única partícula está dada, con el campo medio, por:
$$
\begin{equation*}
\varepsilon = \varepsilon_{tr} + \phi_{} 
\end{equation*}
$$

Tenemos entonces que:
- Para $N$ partículas el volumen excluido es $Nb' = N 4V_{esf} = 4N (4/3 \pi r^{3})$ 
- Para $N$ partículas la energía debido a la interacción dipolo dipolo es, en promedio, $\phi = N \phi_1 = -\epsilon N b'/V$

Así podemos escribir la función de partición de una partícula como:
$$
\begin{align*}
q = \sum_{i} e^{-\beta (\varepsilon_{i,tr} + \phi)} =
e^{-\beta \phi} \sum_{i} e^{-\beta \varepsilon_{tr,i}} =
q_{tr} e^{-\beta \phi}
\end{align*}
$$

El $q_{tr}$ será similar al del gas ideal, pero con la corrección de volumen, por lo que la función de partición unimolecular de un gas de VdW es:
$$
\begin{align*}
q &= e^{\beta Na'/V} \frac{V-Nb'}{\Lambda^{3}}  & 
a'&= \epsilon b' &
b'&= 4 \left( \frac{4}{3} \pi R^{3} \right) &
\Lambda =  \sqrt{\frac{h^{2}}{2\pi m k_{\text{B}}T}} 
\end{align*}
$$
- $R$ el radio de cada partícula
- $\epsilon$ es el valor del potencial dipolo dipolo en el momento en el que ambas moléculas se tocan.
- La aproximación de campo medio calcula la interacción promedio de un par de partículas y luego suma las interacciones de todos los pares. Esto hace que no tenga en cuenta la correlación entre partículas, esto es el hecho de que la presencia de una 3ra partícula pueda afectar la cómo el par se posiciona. Al tener en cuenta solo el par, respecto a la primer partícula, la 2da puede posicionarse en cualquier lugar del espacio, pero la 3ra (y 4ta y 5ta) podrían estar afectando, por una cuestión energética, la probabilidad de las distintas posiciones de la 2da partícula. 

Por lo tanto, para un sistema, la función de partición del gas de VdW es:
$$
\begin{align*}
Q = \frac{q^{N}}{N!} \Rightarrow 
\ln Q &\approx N \ln \frac{q}{N} + N
\\
\ln Q &= N \ln \left( e^{\beta N a'/V} \frac{V-Nb'}{N\Lambda^{3}} \right) + N
\end{align*}
$$
donde se utilizó la aproximación de Stirling y $e$ es simplemente el número de Euler.  Reordenando un poco:
$$
\begin{equation*}
\boxed{
\ln Q= \frac{N^{2}\beta a'}{V}  + N \ln \left( \frac{V-Nb'}{N\Lambda^{3}} \right) + N
} 
\end{equation*}
$$
# Ecuación de estado:
Para conseguir la ecuación de estado, se deriva respecto al volumen:
$$
\begin{align*}
p\beta = \frac{ \partial \ln Q }{ \partial V } &= 
\frac{ \partial  }{ \partial V } \left( \frac{N^{2}\beta a'}{V}  + N \ln \left( \frac{V-Nb'}{N\Lambda^{3}} \right) + N \right) 
\\
p \beta &= -\frac{N^{2} \beta a'}{V^{2}} + \frac{N}{V-Nb'}
\\
p &= \frac{N}{\beta (V-Nb')} - \frac{N^{2}a'}{V^{2}}
\end{align*}
$$
Reordenando:
$$
\begin{equation*}
p = \frac{Nk_{\text{B}}T}{V-Nb'} - a'\frac{N^{2}}{V^{2}}
\end{equation*}
$$
Si se quiere escribir en término de número de moles, usamos que $N=n N_{A}$.
$$
\begin{align*}
p = \frac{n N_{A} k_{\text{B}}T}{V-nN_{A}b'} - a' N_{A}^2 \frac{n^{2}}{V^{2}}
\end{align*}
$$
Notemos que:
$$
\begin{align*}
b &= N_{A}b' & 
a &= a' N_{A}^2 = \epsilon N_{A} b' N_{a} = \epsilon N_{A} b = E b
\end{align*}
$$
por lo tanto resulta la conocida:
$$
\begin{equation}
\boxed{
p = \frac{nRT}{V-nb} - a \frac{n^{2}}{V^{2}} = \frac{RT}{\bar{V}-b} - \frac{a}{\bar{V}^{2}}
}
\end{equation}
$$
Para tratamientos matemáticos, es útil tener expresada la ecuación de estado en su forma cúbica. Multiplicando a ambos lados por $\bar{V}^2 (\bar{V}-b)$ se obtiene:
$$
\begin{align*}
p \bar{V}^2 (\bar{V}-b) &= RT \bar{V}^2 - a(\bar{V}-b) 
\\
p \bar{V}^3 - pb \bar{V}^{2} &= RT \bar{V}^2 - a \bar{V} + ab
\\
p \bar{V}^3 - (pb + RT) \bar{V}^{2} +  a \bar{V} - ab &= 0
\end{align*}
$$

Para el caso de esferas rígidas $a=0$ y por ende:
$$
p = \frac{RT}{\bar{V}-b}
$$
# Energía interna
La energía se calcula como:
$$
\begin{align*}
U = - \frac{ \partial \ln Q }{ \partial \beta } &= 
-\frac{ \partial  }{ \partial \beta } \left( \frac{N^{2}\beta a'}{V}  + N \ln \left( \frac{V-Nb'}{N\Lambda^{3}} \right) + N \right) 
\\
U &= - \frac{N^{2}a'}{V} + \frac{3}{2} N k_{\text{B}} T
\end{align*}
$$
donde se utilizó que $\Lambda\sim \beta^{1/2}$. De forma análoga a lo anterior, usando que $a = a' N_{A}^{2}$ se obtiene:
$$
\begin{equation}
\boxed{
U_{VdW} = \frac{3}{2} n R T - \frac{a}{\bar{V}^2}
}
\end{equation}
$$
para un gas de VdW que tiene solo traslaciones. De aquí también se deriva que para el gas de esferas rígidas monoatómico:
$$
\begin{equation*}
U_{HS} = \frac{3}{2} nRT
\end{equation*}
$$

De esta ecuación también se deriva que para el gas de VdW monoatómico:
$$
\begin{equation*}
C_{V} = \frac{ \partial U }{ \partial T } = \frac{3}{2} nR
\end{equation*}
$$
# Potencial químico:
La energía libre de Helmholtz es:
$$
\begin{align*}
    F &= -k_{\text{B}} T \ln Q = -k_{\text{B}} T N \ln\left( \frac{(V-Nb')e}{N}  \left( \frac{2\pi m }{h^2 \beta} \right)^{3/2} \right) - \frac{a'\beta N^2k_{\text{B}} T}{V} 
    \\
    &= -k_{\text{B}} T \ln Q = -k_{\text{B}} T N \ln\left( \frac{(V-Nb')e}{N} \left( \frac{2\pi m }{h^2 \beta} \right)^{3/2} \right) - \frac{a' N^2 }{V} 
\end{align*}
$$
del cual puede derivarse el potencial químico:
$$
\begin{align*}
    \mu &= \left( \frac{\partial F}{\partial N} \right){T,V} = 
    -k_{\text{B}} T \ln\left( \frac{(V-Nb')e}{N} \left(\frac{2\pi m }{h^2 \beta} \right)^{3/2} \right) - N k_{\text{B}} T \frac{\partial }{\partial N}\left(\ln\frac{V-Nb'}{N} \right)- \frac{2a'N}{V}
    \\
    &= -k_{\text{B}} T \ln\left( \frac{(V-Nb')e}{N} \left(\frac{2\pi m }{h^2 \beta} \right)^{3/2} \right) + \frac{N k_{\text{B}} T b'}{V-Nb'} + k_{\text{B}} T - \frac{2a'N}{V}
    \\
    &= -k_{\text{B}} T \ln\left( \frac{(V-Nb')}{N} \left(\frac{2\pi m }{h^2 \beta} \right)^{3/2} \right) - k_{\text{B}} T \ln e + \frac{N k_{\text{B}} T b'}{V-Nb'} + k_{\text{B}} T - \frac{2a'N}{V}
    \\
    &= -k_{\text{B}} T \ln\left( \frac{(V-Nb')}{N} \left(\frac{2\pi m }{h^2 \beta} \right)^{3/2} \right) + \frac{N k_{\text{B}} T b'}{V-Nb'} - \frac{2a'N}{V}
\end{align*}
$$
Da bien:
\url{https://janheyda.wordpress.com/wp-content/uploads/2015/08/johnston-thermodynamic-properties-of-van-der-waals-fluid-iop-2014.pdf}

Si queremos que aparezca la presión, podemos calcular:
$$
\begin{align*}
    p &= \frac{Nk_{\text{B}} T}{V-Nb'} - \frac{a' N^2}{V^2} \Leftrightarrow 
    p + \frac{a'N^2}{V^2} = \frac{pV^2 + a'N^2}{V^2}= \frac{Nk_{\text{B}} T}{V-Nb'} 
    \\
    \frac{V-Nb'}{N} &= \frac{k_{\text{B}} T V^2}{pV^2 + a'N^2} \qquad 
    \frac{N k_{\text{B}}T}{V-Nb'} = p + \frac{a'N^{2}}{V}
\end{align*}
$$
Reemplazando en el potencial químico:
$$
\begin{align*}
    \mu &= -k_{\text{B}} T \ln \left(\frac{k_{\text{B}} T V^2}{pV^2 + a'N^2} \left(\frac{2\pi m k_{\text{B}} T}{h^2}\right)^{3/2} \right) + \left(p + \frac{a'N^2}{V^2}\right) b' - \frac{2a'N}{V} 
    \\
    \mu &= -k_{\text{B}} T \ln \left(\frac{V^2}{pV^2 + a'N^2}  (k_{\text{B}} T)^{5/2}\left(\frac{2\pi m}{h^2}\right)^{3/2} \right) + pb' + \frac{a'b'N^2}{V^2}\ - \frac{2a'N}{V} 
\end{align*}
$$
Recordando que para un GI monoatómico teníamos: 
$$
\begin{align*}
    \mu &= -k_{\text{B}} T \ln \left( \frac{(k_{\text{B}} T)^{5/2}}{p} \left(\frac{2m\pi}{h^2} \right)^{3/2} \right)
\end{align*}
$$
podemos reescribir:
$$
\begin{align*}
\mu &= -k_{\text{B}} T \ln \left(\frac{V^2}{pV^2 + a'N^2} \frac{p}{p} (k_{\text{B}} T)^{5/2}\left(\frac{2\pi m}{h^2}\right)^{3/2} \right) + pb' + \frac{a'b'N^2}{V^2}\ - \frac{2a'N}{V} 
\\
\mu &= \mu_{id} -k_{\text{B}} T \ln \left(\frac{pV^2}{pV^2 + a'N^2} \right) + pb' + \frac{a'N}{V^{2}} (Nb'-2V)
\end{align*}
$$
Este sería el potencial químico correspondiente a una única molécula. Si queremos el correspondiente molar, multiplicamos por $N_{A}$ y además $N=N_A$ a ambos lados, obteniendo:
$$
\begin{equation*}
\mu = \mu_{id} - N_{A}k_{\text{B}}T \ln \left(\frac{pV^2}{pV^2 + a'N_{A}^2} \right) + pN_{A}b' + \frac{a'N_{A}^{2}}{V^{2}} (N_{A}b'-2V)
\end{equation*}
$$
y utlizando que $R=N_{A}k_{\text{B}}$, $N_A b' = nb$ y $a' N_{A}^{2} = a$ se obtiene:
$$
\begin{equation*}
\mu = \mu_{id} - RT \ln \left(\frac{p\bar{V}^2}{p\bar{V}^2 + a} \right) + pb + \frac{a}{\bar{V}^{2}} (b-2\bar{V})
\end{equation*}
$$
dando vuelta el argumento del logaritmo:
$$
\begin{equation*}
\boxed{
\mu_{VdW} = \mu_{id} + RT \ln\left( 1+\frac{a}{p \bar{V}^{2}} \right) + pb + \frac{a}{\bar{V}^2} (b-2\bar{V})
}
\end{equation*}
$$
Por último, $\mu = \mu_{id} + RT\ln\phi$, por lo que:
$$
\begin{equation*}
RT\ln \phi = RT \ln\left( 1+\frac{a}{p \bar{V}^{2}} \right) + pb + \frac{a}{\bar{V}^2} (b-2\bar{V})
\end{equation*}
$$

Dada $p$ y $T$ puede resolverse el $\bar{V}$ con la cúbica, luego introducir los valores en la ecuación y calcular $\ln\phi$. 
$$
\begin{equation*}
    p \bar{V}^3 - (p b + RT) \bar{V}^2 + a \bar{V} - ab= 0
\end{equation*}
$$
Adicionalmente, notemos que para esferas rígidas ($a=0$) y por ende se obtiene que:
$$
\mu_{HS} = \mu_{id} + pb
$$