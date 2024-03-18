# Bitácora 1

Faise unha presentación sobre a materia e sobre os criterios de evaluación desta

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

$log_2(\frac{b-a}{\epsilon})<k*log_2(2)$

$k > log_2(\frac{b-a}{\epsilon})$

Este método e lento, pero de converxencia garantizada.


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

# Bitácora 4

### Funcións con varias variables

Se denotamos o número de variables por $n$, as funcións atópanse definidas nun subconxunto de $R^n$, e retornan un escalar, e decir, a todo elemento do subconxunto asignaraselle un R.

A imaxe e o dominio e igual que anteriormente.

Exemplo: $f(x,y,z) = \frac{xy}{z}$

$Dom(f) = {(x,y,z) \in \mathbb{R}^3 \ (x,y,0)}$

ou equivalentemente, 

$Dom(f) = \{(x,y,z) \in \mathbb{R}^3 \ | \ (x,y,0)/x,y \in R}$

#### Exemplos de funcións:

##### Paraboloide

$f(x,y) = x^2 + y^2$

$Dom(f) = \mathbb{R}^2$

$R(f) = [0, +\infty)$


##### Sela de montar

$f(x,y) = x^2 - y^2$

$Dom(f) = \mathbb{R}^3^2$

$R(f) = \mathbb{R}$

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

$L_{-1}$ = ${$(x,y) \in D(f) / ln(1-x^2-y^2) < 0$}

$e^{-1} = 1-x^2-y^2 => x^2 + y^2 = 1-1/e => R^2 = \sqrt{1-1/e}\approx 0.795$

Este procéso é análogo para o resto de conxuntos de nivel.

