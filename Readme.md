# Bitácora 1

Faise unha presentación sobre a materia e sobre os criterios de evaluación desta
<br><br><br>


# Bitácora 2

### Busqueda de raices en sist. lineales

En ecuacións de primeiro e de segundo grado, resólvense con normalidade

### Teorema do valor medio

Se f(x) no intervalo [a,b] e continua, para todo valor $f(a) < z < f(b)$, existe un valor c no intervalo que cumpre $f(c) = z$

Se aplicamos ao caso particular onde $f(a)*f(b) < 0$, obtemos que no intervalo ten que haber unha raíz $(f(x)=0)$

### Método de bisección/dicotomía

Usando o teorema anterior:
Repítese en forma de buúsqueda binaria $x_r = \frac{a+b}{2}$, con 3 posibles casos:
1. $f(a)*f(x_r) = 0$: Entón $x_r$ é a raiz, e finalízase o proceso
2. $f(a)*f(x_r) < 0$: Significa que hai unha raiz ainda no intervalo $[a,x_r]$, polo que repítese o proceso con $b=x_r$
3. $f(a)*f(x_r) = 0$: Significa que hai unha raiz ainda no intervalo $[x_r,b]$, polo que repítese o proceso con $a=x_r$

Sendo k o numero de pasos realizados, a cota de error deste método é: $e_k = |\alpha-x_k|=<(\frac{1}{2})²*(b-a)$, entón sendo $\alpha$ a raiz que procuramos, $\alpha = \lim_{k \to \infty} x_k$

Este método pódese repetir ata que o erro $e_k$ sea menor que unha cota dada, ou cando $f(x_k)$ sea moi próximo a 0

##### Modelo de exercicio:
Atopar o k necesario para queo erro cometido sea menor que $\epsilon$:

Resólvemos a inecuación $\frac{b-a}{\epsilon}<2^k$:

$log_2 (\frac{b-a}{\epsilon})<k log_2(2)$

$k > log_2(\frac{b-a}{\epsilon})$

Este método e lento, pero de converxencia garantizada.
<br><br><br>


# Bitácora 3

### Métodos de converxencia veloz

A orde de converxencia dun 

??????????????????????????????????

### Método de Newton-Raphson

Consiste en, empezando por un $x_0$ calquera, calcular a recta tangente nese punto, e mirando onde corta o eixo $x$. Logo, repítese ese proceso usando a $x$ do punto de corte.
Para calcular a recta tanxente a gráfica, usamos a seguinte fórmula

$y = f(x_k) + f'(x_k)*(x-x_0)$

Para calcular o punto de corte, simplemente se substitue a $y$ por $0$.

Este método no e de converxencia garantida, xxa que se unha recta apunta cara outra raíz, non atpoará a que nos buscamos.

#### Teorema 1

Se temos unha funcion con unha raíz no intervalo $(a,b)$, e sexa $m_1$ =< ao valor de $f'(x)$ nese intervalo, e $M_2$ => ao máximo valor de $f(x)$ nese intervalo. Supoñemos que $m_1>0$, e dado $x_0 \in [a,b],$ sexa ${x_k} k\in N$ a sucesión obtida polo método de Newton, e supoñendo que $x_k\in[a,b]$ para todo $N$, entón: 

$|a-x_{k+1} \leq \frac{M_2}{2m_1}|\alpha - x_k|^2$

E dicir, a distancia entre a raiz e o iterante seguinte é menor ou igual a unha constante polo erro na etapa K elevado ao cadrado

Se esto se da, asegurase a converxencia $\lim_{k \to \infty} x_k = \alpha$ con p=2 e a nosa constante C pasa a ser coñecida: $C = \frac{M_2}{2m_1}$

#### Teorema 2

Se temos unha función cunha raiz nun intervalo $(a,b)$, e sexan $m_1$ e $M_2$ os mismos que o teorema anterior:

$|a-x_{k+1} \leq \frac{M_2}{2m_1}|x_{k+1} - x_k|^2 \qquad k=0,1,2$

Neste caso, o erro non queda en función da raiz, se non en función de duas iteracións, poidendo saber asi cantas itercions precisamos para que o erro sexa menor que certa constante.


### Criterio de detención
Tendo en conta $|x_{k+1} - x_k| = -\frac{f(x_k)}{f'(x_k)}$, se a distancia é moi pequena, a fracción tamén.
?¿?¿?¿?¿?¿?¿?¿?

### Método da secante

Este método e parecido ao de Newton. Úsase cando é dificil avaliar $f'(x_k)$ xa que se substitue por un cociente incremental -> $\frac{f(x_k)-f(x_{k-1})}{x_k-x{k-1}}$

$x_{k+1} = x_k - f(x_k)\frac{x_k-x{k_1}}{f(x_k)-f(x_{k-1})}$

Este método é mais lento que o de newton, xa que ten complexidade áurea ($p = \frac{1+\sqrt{5}}{2}$).
<br><br><br>


# Bitácora 4

### Funcións con varias variables

Se denotamos o número de variables por $n$, as funcións atópanse definidas nun subconxunto de $R^n$, e retornan un escalar, e decir, a todo elemento do subconxunto asignaraselle un R.

A imaxe e o dominio e igual que anteriormente.

Exemplo: $f(x,y,z) = \frac{xy}{z}$

$Dom(f) = {(x,y,z) \in \mathbb{R}^3 \ (x,y,0)}$

ou equivalentemente, 

$\text{Dom}(f) = \{(x, y, z) \in \mathbb{R}^3 \ | \ z = 0, \ x, y \in \mathbb{R}\}$

#### Exemplos de funcións:

##### Paraboloide

$f(x,y) = x^2 + y^2$

$Dom(f) = \mathbb{R}^2$

$R(f) = [0, +\infty)$


##### Sela de montar

$f(x,y) = x^2 - y^2$

$\text{Dom}(f) = (\mathbb{R}^3)^2$

$R(f) = \mathbb{R}$
<br><br><br>


# Bitácora 5

#### Semiesfera

$z = +\sqrt{\mathbb{R}^2-x^2-y^2}$ => $f(x,y) = +\sqrt{\mathbb{R}^2-x^2-y^2}$

A función depende de x e y, sendo R un parámetro que denota o radio da semiesfera. O signo faina positiva ou negativa.


### Conxuntos de nivel

Un conxunto de nivel é un subconxunto do seu dominio onde a función toma un valor constante, e defínese como $L_c$.


#### Exercicio de EXAME

Sea $f(x,y) = \ln(1-x^2-y^2)$. Calcula o dominio de $f$ e define os conxuntos de nivel $L_{-1}, L_0, L_1$.

Como sabemos que o logaritmo ten que ser maior ou igual a 0, a condición é:
$Dom(f) =$ {$(x,y) \in \mathbb{R}^2 / 1-x^2-y^2 < 0$}, ou o que é equivalente: $Dom(f) =$ {$(x,y) \in \mathbb{R}^2 / x^2+y^2 < 1$}

Para $L_{-1}$:

$L_{-1}$ = ${\{(x, y) \in D(f) \ | \ \ln(1 - x^2 - y^2) < 0\}}$

$e^{-1} = 1-x^2-y^2 => x^2 + y^2 = 1-1/e => R^2 = \sqrt{1-1/e}\approx 0.795$

$L_{-1} = \{ (x, y) \in D(f) \ | \ x^2 + y^2 = (\sqrt{\frac{e-1}{e}})^2 \}$


Este procéso é análogo para o resto de conxuntos de nivel.
<br><br><br>


# Bitácora 6
------------
<br><br><br>


# Bitácora 7

### Derivación de funcións de unha variable

A derivación dunha soa variable $f'(x)$ correspóndese co cálculo da pendente da recta tanxente a curva no punto $x_0$.

A definición de derivada é $\lim_{{h \to 0}} \frac{{f(x+h) - f(x)}}{h}$

Sea $f(x)= x^3 +x^2 +x +2$.

A sua derivada correspóndese con $f'(x)=3x^2+2x+1$



### Derivación de funcións de duas variables

#### Derivada parcial respecto de $x$

A función $f$ é derivable respecto de $x$ no punto $(x_0, y_0)$ se existe y é un número o seguinte límite: 
$\lim_{{h \to 0}} \frac{{f(x_0 + h, y_0) - f(x_0, y_0)}}{h}$.

Para derivar respecto dunha variable, considéranse o resto como constantes, facendo unha derivada normal.
O proceso é análogo para $y$.

Exemplo: $f(x,y)=x^2-2xy-3y^2$

$\frac{\partial f(x,y)}{\partial x} = 2x -2y$

$\frac{\partial f(x,y)}{\partial y} = 2x -6y$

#### Interpretacion xeométrica

$f_x(x,y)=\frac{\partial f}{\partial x}(x_0, y_0)$ é a pendente da recta tanxente no punto $P(x_0, y_0, f(x_0, y_0))$ da curva obtida de intersecar a superficie $z = f(x,y)$ co plano $y = y_0$. Mesma forma, ocurre con $f_y(x,y).$


### Plano tanxente

Para unha superficie $z = f(x,y)$, o plano tanxente ao punto $P(x_0, y_0, f(x_0, y_0))$ queda definido pola seguinte ecuación:

$z = f(x_0, y_0) + f_x(x_0, y_0)(x-x_0) + f_y(x_0, y_0)(y-y_0)$

Exemplo: $f(x,y)=x^2-2xy-3y^2$

(As parciales calculadas antes)

$z = f(x_0, y_0) + f_x(x_0, y_0)(x-x_0) + f_y(x_0, y_0)(y-y_0)$

$z = 0 + 4(x-3) - 12(y-1)$

$z = 4x - 12y$
<br><br><br>


# Bitácora 8

### Método de Newton

Supoñemos que temos unha función non lineal $f:D\subseteq R \to R$ diferenciable en D, e queremos atopar $\alpha$ tales que $f(\alpha)=0$.

Para resolver este problema, construimos unha sucesión de puntos $x^k$ de forma que se van achegando a $\alpha$, co cal podemos deter a sucesión cando nos acheguemos o suficinente a 0.

1. Escóllese un primeiro iterante $x^0$
2. Partindo de $x^k$, constrúese $x^{k+1}$ da seguinte forma: $x^{k+1}=x^k - \frac{f(x^k)}{f'(x^k)}$
3. Detémosnos se $|x^{k+1} -x|<\epsilon$ ou tamén se $|f(x^k+1)|<\epsilon$, sendo $\epsilon$ unha tolerancia definida.
4. Dado que o algoritmo pode non converxer, hai que considerar un número máximo de iteracións

### Método de Newton (2D)

Ahora, en vez de contar con unha soa función, contamos con duas.

$f_1:D\subseteq R^2 \to R \qquad$  e  $\qquad f_2:D\subseteq R^2 \to R$

Igual que no caso anterior, queremos topar valores de $\alpha$ para os cales:

$f_1(\alpha_1, \alpha_2)=0 \qquad$   e  $\qquad f_2(\alpha_1, \alpha_2)=0$

Unha forma de simplificar esto, e facer uso dunha función vectorial:

$f(x_1, x_2):=(f_1(x_1, x_2), f_2(x_1, x_2))$

Ahora, hai que atopar os valores de $\alpha$ para os que:

$f(\alpha_1, \alpha_2):=(f_1(\alpha_1, \alpha_2), f_2(\alpha_1, \alpha_2)) = (0,0)$

Esta vez a sucesión de valores $x^k$ será $(x_1^k, x_2^k), a cal se vai achegando a (\alpha_1, \alpha_2).$

### Método de Newton-Raphson

Xeneralizando o anterior, querese atopar $f(x)=0$ para unha $f:R^n \to R^n$. Supoñemos que $\alpha = (\alpha_1, \alpha_2, ..., \alpha_n)t \in R^n$ é unha solución do sistema, e que $f=(f_1, f_2, ..., f_n)$ é duas veces diferenciable.

Empregando o desenvolvemento de Taylor para variables e funcións na contorna do punto $x^k=(x^k_1, x^k_2, ..., x^k_n)$ para obter:

$0 = f(\alpha)=f(x^k)+Df(x^k)(\alpha-x^k)+O(|\alpha -x^k|^2)$

$Df(x^k)$ corresponde a matriz de derivadas parciais ou Matriz Jacobiana.


$$ Df(x^k) =
\left(\begin{array}{cc} 
\frac{\partial f_1}{\partial x_1}(x^k) & ··· & \frac{\partial f_1}{\partial x_n}(x^k)\\
· &  ·   & · \\
· &   ·  & · \\
· &    · & · \\
\frac{\partial f_n}{\partial x_1}(x^k) & ··· & \frac{\partial f_n}{\partial x_n}(x^k)\\
\end{array}\right)
$$ 

Para duas incógnitas, a matriz Jacobiana vese asi:

$$ Df(x^k) =
\left(\begin{array}{cc} 
\frac{\partial f_1}{\partial x_1}(x^k) & ··· & \frac{\partial f_1}{\partial x_2}(x^k)\\
\frac{\partial f_2}{\partial x_1}(x^k) & ··· & \frac{\partial f_2}{\partial x_2}(x^k)\\
\end{array}\right)
$$ 

Cando o termo $|\alpha - x^k|$ é moi pequeno, $O(|\alpha -x^k|^2)$ pode desperdiciarse.
Por tanto, o resultado para duas variables, é o seguinte:

$0 = f_1(x^k)+\frac{\partial f_1}{\partial x_1}(x^k)(\alpha_1-x^k_1)+\frac{\partial f_1}{\partial x_2}(x^k)(\alpha_2-x^k_2)$

$0 = f_2(x^k)+\frac{\partial f_2}{\partial x_1}(x^k)(\alpha_1-x^k_1)+\frac{\partial f_2}{\partial x_2}(x^k)(\alpha_2-x^k_2)$

Se a matriz $Df(x)$ é invertible, pódese extraer o valor da raíz $\alpha$ de dito sistema, sendo o resultado:

$Df(x^k)(\alpha - x^k) \approx -f(x^k) \to \alpha -x^k \approx -Df(x^k)^{-1}f(x^k) \to \alpha \approx x^k -Df(x^k){-1}f(x^k)$

Polo tanto, o método de Newton consiste na aproximación da solución $x^{k+1}:=x^k -Df(x^k){-1}f(x^k), \qquad k=0,1,2...$
<br><br><br>


# Bitácora 9

### Método de Newton (continuación)

Se a matriz $Df(x^k)$ é invertible, entón podemos aproximar a raíz $\alpha$ despexándoa da seguinte relación:
$Df(x^k)(\alpha - x^k) \approx -f(x^k) \to Df(x^k)(x^{k+1}-x^k) \approx -f(x^k)$

A nosa incógnita é $x^{k+1}$ que se corresponde co seguinte termo:

$x^{x+1}=x^k-(Df^{-1}(x^k)f(x^k))$

Esta ecoacuón final, aseméllase coa ecuación do método para unha incógnita: $x^{k+1}=x^k-\frac{f(x^k)}{f'(x^k)}$, solo que en vez de dividir pola derivada de $f(x)$, multiplicamos pola inversa da matriz Jacobiana, polo que esta debe ser invertible.

???????? Algoritmo para invertir a matriz ¿¿¿¿¿¿¿¿¿¿¿¿¿

### Derivadas parciais de segunda orde

As derivadas parciais de segunda orde, fanse con respecto as derivadas parciais de x e de y:

$\frac{\partial^2f}{\partial x^2}(x,y)=\frac{\alpha}{\alpha x}(\frac{\alpha f}{\partial x}(x,y))=f_{xx}(x,y)$

$\frac{\partial^2f}{\partial y \partial x}(x,y)=\frac{\alpha}{\alpha y}(\frac{\alpha f}{\partial x}(x,y))=f_{xy}(x,y)$

$\frac{\partial^2f}{\partial y^2}(x,y)=\frac{\alpha}{\alpha y}(\frac{\alpha f}{\partial x}(x,y))=f_{yy}(x,y)$

$\frac{\partial^2f}{\partial x \partial y}(x,y)=\frac{\alpha}{\alpha x}(\frac{\alpha f}{\partial y}(x,y))=f_{yx}(x,y)$

### Teorema das derivadas parcias mixtas e Matriz Hessiana

Se $f(x,y)$ e as súas derivadas parciais están definidas nunha rexion aberta que conten o unto (a,b) e son continuas en (a,b), entón cumprese o dito anteriormente.

$\frac{\alpha}{\alpha x}(\frac{\alpha f}{\alpha y}(x,y))=\frac{\alpha}{\alpha y}(\frac{\alpha f}{\alpha x}(x,y))$

A partir das derivdas segundas da función f, podemos construir a Matriz Hessiana:

$$ Hf(x^k) =
\left(\begin{array}{cc} 
f_{xx}(x,y) & f_{xy}(x,y)\\
f_{yx}(x,y) & f_{yy}(x,y)\\
\end{array}\right)
$$ 

### Vector gradiente

Sexa $f(x,y) unha función para a que existen as derivadas parciais $\frac{\alpha f}{\alpha x}(x,y),\frac{\alpha f}{\alpha y}(x,y)$ e son continuas, o vector gradiente defínese como: 

$\nabla f(x,y)=(\frac{\alpha f}{\alpha x}(x,y),\frac{\alpha f}{\alpha y}(x,y))$

##### Exemplo de vector gradiente

$T(x,y)=100 - x^2 -y^2$

$\nabla T(x,y)=(\frac{\alpha T}{\alpha x}(x,y),\frac{\alpha T}{\alpha y}(x,y))= (-2x,-2y)$

### Función vectorial

Cando temos máis variables, en vez de ter un vector gradiente, temos unha función vectorial que sigue a seguinte definicion:

$f:x\in Dom(f) \subseteq R^n \to f(x)=(f_1(x),...mf_m(x))\in R^ m$

### Matriz Xacobiana (xeral)

Esta matriz caracterízase por ter tantas filas como compoñentes da imaxe, e tantas columnas como variables independientes. No caso particular de funcións escalares (m=1), a matriz Jacobiana coincide co vector gradiente, como por exemplo:

$f(x,y)=ln(x^2+y^2)$

$Df(x,y)=(\frac{2x}{x^2+y^2} \frac{2y}{x^+y^2})= \nabla f(x,y)$
<br><br><br>


# Bitácora 10

### Regra da cadea

#### Caso 1
Supoñendo dúas funcións tal que 

$g: Dom(g) \subseteq R^n\to R^m$
$f: Dom(f) \subseteq R^m\to R^p$

pódense compoñer as dúas funcións $[R^n \to g \to R^m \to f \to R^p]$ tendo todas as derivadas parciais contínuas. Verifícase entón: 

$D(g \circ f)(x) = Df(g(x))Dg(x)$  

#### Caso 2

No caso 2, vólvese a ter unha función $f(x,y)$ de dúas variables, pero estas en vez de depender dunha única variable, dependen de 2:
$x=x(u,v), y=y(u,v)$

A composición:

$w(u,v):= (f \circ r)(u,v) = f(r(u,v)) = f(x(u,v),y(u,v))$

É unha función de dúas variables que ten como derivadas parciais:

$\frac{\partial w}{\partial u}=\frac{\partial f}{\partial x}(r(u,v))\frac{\partial x}{\partial u} + \frac{\partial f}{\partial y}(r(u,v))\frac{\partial y}{\partial u}$

$\frac{\partial w}{\partial v}=\frac{\partial f}{\partial x}(r(u,v))\frac{\partial x}{\partial v} + \frac{\partial f}{\partial y}(r(u,v))\frac{\partial y}{\partial v}$

que compoñen a matriz resultante da derivada da composición:

$D(f\circ r)=Df(r(u,v))Dr(u,v)=(\frac{\partial w}{\partial u}  \frac{\partial w}{\partial v})$
<br><br><br>


# Bitácora 11

### Derivación implícita

Para unha gráfica $f(x,y)$, a variable y pode estar definida de forma implíciat como un conxunto de nivel de valor 0: $f(x,y)=0$

Se F permite derivadas parciais e estas son continuas ¡, entón:

$\frac{dy}{dx}=-\frac{F_x(x,y)}{F_y(x,y)}; \forall F_y(x,y)\not ={0}$

Este método é equivalente á derivación implícita, que consiste en:

1. Derivación de ambos membros da ecuaación
2. Despexe de $y'(x)$

##### Exemplo

Calcular $\frac{dy}{dx}$ en: $y^5-2y-x=0$

Definimos as derivadas parciais:

$F_x(x,y)=-1 \qquad F_y(x,y)=5y^4-2$

$\frac{dy}{dx}=-\frac{F_x(x,y)}{F_y(x,y)} = -\frac{-1}{5y^4-2} = \frac{1}{5y^4-2}$

Se en vez de empregar a fórmula, derivamos implícitamente, obtemos os mesmos resultados.

$y(x)^5-2y(x)-x=0; \qquad 5y(x)^4\frac{dy}{dx}-2\frac{dy}{dx}-1=0$

$\frac{dy}{dx}(5y(x)^4-2)=1; \qquad \frac{dy}{dx}=\frac{1}{5y^4-2}$
<br><br><br>