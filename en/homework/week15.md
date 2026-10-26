# Assignment 15

> **Definition 2.5.2** (Associates) Let $R$ be an integral domain and $a,b\in R$. If there exists a unit $u$ in $R$ such that $a=ub$, then $a$ and $b$ are called associates, denoted $a\sim b$.

> **Definition 2.5.6** (Irreducible Elements) Let $R$ be an integral domain and $\alpha\in R^*\setminus U$. If $\alpha$ has no nontrivial factors, then $\alpha$ is called an irreducible element; otherwise it is called a reducible element.

> **Definition 2.5.14** (Common Divisor and Greatest Common Divisor) Let $R$ be an integral domain and $a_1,a_2,\cdots,a_n\in R$. If $c\in R$ divides every $a_i$, then $c$ is called a common divisor of them; if a common divisor $d$ is divisible by every common divisor, then $d$ is called a greatest common divisor.

> **Theorem 2.5.15** (Equivalent Conditions for a Unique Factorization Domain) An integral domain $R$ is a unique factorization domain if and only if $R$ satisfies the divisor chain condition and the prime condition; that is, in a unique factorization domain every irreducible element is prime: $p\mid ab$ implies $p\mid a$ or $p\mid b$.

### Problem 1

(Problem 2.5-8) Let $R=\mathbb Z\left[\sqrt{-5}\right]$.
(1) Prove that if $a^2+5b^2=9$, then $a+b\sqrt{-5}$ is an irreducible element;
(2) Prove that the elements $\alpha=6+3\sqrt{-5}$ and $\beta=9$ have no greatest common divisor in $R$.

### Solution to Problem 1

Define the norm on $R$ by
$$
N\left(x+y\sqrt{-5}\right)=x^2+5y^2,
$$
so that $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$, and $\xi$ is a unit if and only if $N\left(\xi\right)=1$.

(1) Let $\gamma=a+b\sqrt{-5}$; then $N\left(\gamma\right)=a^2+5b^2=9\ne1$, so $\gamma$ is not a unit, i.e. $\gamma\in R^*\setminus U$. Suppose, for contradiction, that $\gamma=\xi\eta$ is a nontrivial decomposition. Then
$$
N\left(\xi\right)N\left(\eta\right)=N\left(\gamma\right)=9.
$$

The norm takes values among the nonnegative integers $x^2+5y^2$. There is no element of norm $3$: the equation $x^2+5y^2=3$ requires $x^2=3$ when $y=0$, which is not a square; and when $\left|y\right|\ge1$, we have $5> 3$. Hence $N\left(\xi\right),N\left(\eta\right)$ can only be $1$ or $9$. If $N\left(\xi\right)=1$, then $\xi$ is a unit; if $N\left(\xi\right)=9$, then $N\left(\eta\right)=1$ and $\eta$ is a unit.

Thus in any decomposition of $\gamma$, one factor must be a unit. By **Definition 2.5.6** (Irreducible Elements), $\gamma$ is irreducible.

(2) First make the decompositions:
$$
\beta=9=\left(2+\sqrt{-5}\right)\left(2-\sqrt{-5}\right),
$$
$$
\alpha=6+3\sqrt{-5}=3\left(2+\sqrt{-5}\right).
$$

Here $N\left(3\right)=9$ and
$$
N\left(2+\sqrt{-5}\right)=N\left(2-\sqrt{-5}\right)=9,
$$
so by (1) both are irreducible.

Both $3$ and $2+\sqrt{-5}$ divide $\alpha$ and $\beta$, so both are common divisors. But $2-\sqrt{-5}$ does not divide $\alpha$: if there existed $\gamma\in R$ with $\gamma\left(2-\sqrt{-5}\right)=\alpha$, then
$$
\gamma=\frac{3\left(2+\sqrt{-5}\right)}{2-\sqrt{-5}}=\frac{3\left(2+\sqrt{-5}\right)^2}{9}=3+\frac{4}{3}\sqrt{-5}\notin R.
$$

Also $3\nmid\left(2+\sqrt{-5}\right)$ (otherwise $\left(2+\sqrt{-5}\right)/3\notin R$), and $\left(2+\sqrt{-5}\right)\nmid 3$
$$
\left(\text{otherwise }3/\left(2+\sqrt{-5}\right)=\left(2-\sqrt{-5}\right)/3\notin R\right),
$$
so the two do not divide each other.

Suppose, for contradiction, that $d$ is a greatest common divisor of $\alpha,\beta$. By **Definition 2.5.14** (Common Divisor and Greatest Common Divisor), every common divisor divides $d$; in particular, $3\mid d$ and $\left(2+\sqrt{-5}\right)\mid d$. But $d\mid\beta=9$, and the divisors of $9$ up to associates are only $1,3,2+\sqrt{-5},2-\sqrt{-5},9$ (there is no element of norm $3$). None of these is divisible by both $3$ and $2+\sqrt{-5}$, a contradiction.

Hence $\alpha,\beta$ have no greatest common divisor in $R$. $\blacksquare$

### Problem 2

(Problem 2.5-10) Let $R=\mathbb Z\left[\omega\right]$, where $\omega=\frac{1+\sqrt{-3}}{2}$ (i.e. the ring of algebraic integers in $\mathbb Q\left(\sqrt{-3}\right)$).
(1) Prove that $R$ forms an integral domain under ordinary addition and multiplication;
(2) Prove that all the units of $R$ are $\pm1$ and $\frac{\pm1\pm\sqrt{-3}}{2}$;
(3) Prove that in $R$, $2$ and $1+\sqrt{-3}$ are associates.

### Solution to Problem 2

Note that $\omega^2=\omega-1$, so
$$
R=\left\{m+n\omega\mid m,n\in\mathbb Z\right\}
$$
is closed under multiplication (since $\omega^2=\omega-1\in R$).

(1) Since $R\subseteq\mathbb C$, it is closed under addition and multiplication and contains the identity $1$; and $\mathbb C$ has no zero divisors. Hence $R$ is a commutative ring with identity and without zero divisors, i.e. an integral domain.

(2) Define the norm
$$
N\left(m+n\omega\right)=\left(m+n\omega\right)\left(m+n\bar\omega\right)=m^2+mn+n^2,
$$
where $\bar\omega=\frac{1-\sqrt{-3}}{2}$. Then $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$, and $\xi$ is a unit if and only if $N\left(\xi\right)=1$. Solving $m^2+mn+n^2=1$ gives
$$
\left(m,n\right)=\left(\pm1,0\right),\;\left(0,\pm1\right),\;\left(1,-1\right),\;\left(-1,1\right).
$$

The corresponding elements are $\pm1$, $\pm\omega=\frac{\pm1\pm\sqrt{-3}}{2}$, and $\pm\left(1-\omega\right)=\frac{\pm1\mp\sqrt{-3}}{2}$. Hence all units of $R$ are $\pm1$ together with $\frac{\pm1\pm\sqrt{-3}}{2}$.

(3) Since $1+\sqrt{-3}=2\omega$, and $\omega$ is a unit, by **Definition 2.5.2** (Associates), $2$ and $1+\sqrt{-3}$ are associates. $\blacksquare$

### Problem 3

(Problem 2.5-15) It is known that $\mathbb Q\left[x,y\right]$ forms a ring under polynomial addition and multiplication. Prove that $x$ and $y$ are coprime. Does there exist $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ such that $r\left(x,y\right)x+s\left(x,y\right)y=1$?

### Solution to Problem 3

$\mathbb Q\left[x,y\right]$ is a unique factorization domain. Both $x$ and $y$ are irreducible and not associates (the only possible unit relating them is a nonzero constant in $\mathbb Q^*$, but $x\ne cy$). By **Definition 2.5.14** (Common Divisor and Greatest Common Divisor), the common divisors of $x,y$ can only be units, so their greatest common divisor is a unit, i.e. $x$ and $y$ are coprime.

However, no such $r,s$ exist. Suppose, for contradiction, that they did; evaluating the identity at $\left(0,0\right)$ gives
$$
r\left(0,0\right)\cdot0+s\left(0,0\right)\cdot0=1,
$$
i.e. $0=1$, a contradiction.

Thus although $x$ and $y$ are coprime, there do not exist $r,s$ with $rx+sy=1$. $\blacksquare$
