# Assignment 15

> **Definition 2.5.2** (Associates) Let $R$ be an integral domain and $a,b\in R$. If there exists a unit $R$ in $u$ such that $a=ub$, then $a$ and $b$ are called associates, denoted $a\sim b$.

> **Definition 2.5.6** (Irreducible Elements) Let $R$ be an integral domain and $\alpha\in R^*\setminus U$. If $\alpha$ has no nontrivial factors, then $\alpha$ is called an irreducible element; otherwise it is called a reducible element.$\alpha$ be an integral domain and 

 $R$. If $a_1,a_2,\cdots,a_n\in R$ divides all the $c\in R$, then $a_i$ is called a common divisor of them; if a common divisor $c$ is divisible by any common divisor, then $d$ is called a greatest common divisor.$d$ is a unique factorization domain if and only if 

 $R$ satisfies the divisor chain condition and the prime condition, i.e. in a unique factorization domain every irreducible element is prime: $R$ implies $p\mid ab$ or $p\mid a$.$p\mid b$.

(1) Prove that if 

 $R=\mathbb Z\left[\sqrt{-5}\right]$, then 
 $a^2+5b^2=9$ is an irreducible element;$a+b\sqrt{-5}$ and 
 $\alpha=6+3\sqrt{-5}$ have no greatest common divisor in $\beta=9$.$R$ by

 

 $R$Then 

$$
N\left(x+y\sqrt{-5}\right)=x^2+5y^2,
$$

, and $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$ is a unit if and only if $\xi$.$N\left(\xi\right)=1$; then 

 $\gamma=a+b\sqrt{-5}$, so $N\left(\gamma\right)=a^2+5b^2=9\ne1$ is not a unit, i.e. $\gamma$. Suppose, for contradiction, that $\gamma\in R^*\setminus U$ is a nontrivial decomposition. Then$\gamma=\xi\eta$The norm takes values in nonnegative integers of the form 

$$
\begin{aligned}N\left(\xi\right)N\left(\eta\right)&=N\left(\gamma\right)\\&=9.\end{aligned}
$$

. There is no element of norm $x^2+5y^2$: $3$ requires $x^2+5y^2=3$ when $y=0$, which is not a square; when $x^2=3$, $\left|y\right|\ge1$. Hence $5>3$ can only be $N\left(\xi\right),N\left(\eta\right)$ or $1$. If $9$, then $N\left(\xi\right)=1$ is a unit; if $\xi$, then $N\left(\xi\right)=9$ and $N\left(\eta\right)=1$ is a unit.$\eta$, one factor must be a unit. By **Definition 2.5.6** (Irreducible Elements), 

 $\gamma$ is irreducible.$\gamma$and

 

$$
\begin{aligned}\beta&=9\\&=\left(2+\sqrt{-5}\right)\left(2-\sqrt{-5}\right),\end{aligned}
$$

$$
\begin{aligned}\alpha&=6+3\sqrt{-5}\\&=3\left(2+\sqrt{-5}\right).\end{aligned}
$$

,$N\left(3\right)=9$and by (1), both are irreducible.

$$
N\left(2+\sqrt{-5}\right)=N\left(2-\sqrt{-5}\right)=9,
$$

 and 

$3$ divide $\alpha$ and $\beta$, so both are common divisors. But $2+\sqrt{-5}$ does not divide $\alpha$: if there existed $\beta$ with $2-\sqrt{-5}$, then$\alpha$Also, $\gamma\in R$ (otherwise $\gamma\left(2-\sqrt{-5}\right)=\alpha$), and 

$$
\begin{aligned}\gamma&=\frac{3\left(2+\sqrt{-5}\right)}{2-\sqrt{-5}}\\&=\frac{3\left(2+\sqrt{-5}\right)^2}{9}\\&=3+\frac{4}{3}\sqrt{-5}\\&\notin R.\end{aligned}
$$

 $3\nmid\left(2+\sqrt{-5}\right)$so the two do not divide each other.$\left(2+\sqrt{-5}\right)/3\notin R$ is a greatest common divisor of $\left(2+\sqrt{-5}\right)\nmid 3$

$$
\left(\text{否则 }3/\left(2+\sqrt{-5}\right)=\left(2-\sqrt{-5}\right)/3\notin R\right),
$$

; in particular, 

 $d$ and $\alpha,\beta$. But $d$, and the divisors of $3\mid d$ up to associates are only $\left(2+\sqrt{-5}\right)\mid d$ (there is no element of norm $d\mid\beta=9$). None of these is divisible by both $9$ and $1,3,2+\sqrt{-5},2-\sqrt{-5},9$, a contradiction.$3$ have no greatest common divisor in $3$. $2+\sqrt{-5}$### Problem 2

(Problem 2.5-10) Let $\alpha,\beta$, where $R$ (i.e. the ring of algebraic integers in $\blacksquare$

).

(1) Prove that $R=\mathbb Z\left[\omega\right]$ forms an integral domain under ordinary addition and multiplication;$\omega=\frac{1+\sqrt{-3}}{2}$ are $\mathbb Q\left(\sqrt{-3}\right)$ and 
 $R$;
(3) Prove that in $R$, $\pm1$ and $\frac{\pm1\pm\sqrt{-3}}{2}$ are associates.
### Solution to Problem 2$R$, so$2$is closed under multiplication ($1+\sqrt{-3}$).

(1) 

 $\omega^2=\omega-1$, is closed under addition and multiplication, contains the identity 

$$
R=\left\{m+n\omega\mid m,n\in\mathbb Z\right\}
$$

, and $\omega^2=\omega-1\in R$ has no zero divisors; hence 

 $R\subseteq\mathbb C$ is a commutative ring with identity and without zero divisors, i.e. an integral domain.$1$where $\mathbb C$. Then $R$, and 

 

$$
\begin{aligned}N\left(m+n\omega\right)&=\left(m+n\omega\right)\left(m+n\bar\omega\right)\\&=m^2+mn+n^2,\end{aligned}
$$

 is a unit if and only if $\bar\omega=\frac{1-\sqrt{-3}}{2}$. Solving $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$ gives$\xi$The corresponding elements are $N\left(\xi\right)=1$, $m^2+mn+n^2=1$, and 

$$
\left(m,n\right)=\left(\pm1,0\right),\;\left(0,\pm1\right),\;\left(1,-1\right),\;\left(-1,1\right).
$$

. Hence all units of $\pm1$ are $\pm\omega=\frac{\pm1\pm\sqrt{-3}}{2}$ and $\pm\left(1-\omega\right)=\frac{\pm1\mp\sqrt{-3}}{2}$.$R$ and $\pm1$ is a unit, by **Definition 2.5.2** (Associates), $\frac{\pm1\pm\sqrt{-3}}{2}$ and 

 $1+\sqrt{-3}=2\omega$ are associates. $\omega$### Problem 3$2$ forms a ring under polynomial addition and multiplication. Prove that $1+\sqrt{-3}$ and $\blacksquare$

 are coprime. Does there exist 

 $\mathbb Q\left[x,y\right]$ such that $x$?$y$ is a unique factorization domain. Both $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ are irreducible and not associates (the only units are nonzero constants in $r\left(x,y\right)x+s\left(x,y\right)y=1$, and 

 

$\mathbb Q\left[x,y\right]$). By **Definition 2.5.14** (Common Divisor and Greatest Common Divisor), the common divisors of $x,y$ can only be units, so their greatest common divisor is a unit, i.e. $\mathbb Q^*$ are coprime.$x\ne cy$ exist. Suppose, for contradiction, that they did; evaluating the identity at $x,y$ gives$x,y$i.e. 
 $r,s$, a contradiction.$\left(0,0\right)$ are coprime, there do not exist 
$$
r\left(0,0\right)\cdot0+s\left(0,0\right)\cdot0=1,
$$
 with $0=1$. 
 $x,y$ $r x+s y=1$. $\blacksquare$
