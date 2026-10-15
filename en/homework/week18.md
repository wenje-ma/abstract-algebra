# Assignment 18

> **Basic Knowledge** (Polynomial Division with Remainder) Let $R$ be a commutative ring with identity, $f\left(x\right),g\left(x\right)\in R\left[x\right]$, and suppose the leading coefficient of $g\left(x\right)$ is a unit in $R$. Then there exist unique $q\left(x\right),r\left(x\right)\in R\left[x\right]$ such that $f\left(x\right)=q\left(x\right)g\left(x\right)+r\left(x\right)$, where $r=0$ or $\deg r<\deg g$. In particular, when the divisor is a monic linear polynomial $x-a$, the remainder is a constant.

> **Basic Knowledge** (Unique Factorization Domain) An integral domain $R$ is called a unique factorization domain if every nonzero, non-unit element of $R$ can be factored as a finite product of irreducible elements, and the factorization is unique up to associates.

> **Basic Knowledge** (Ring of Formal Power Series) The ring of formal power series $k$ over a field $k\left[\!\left[t\right]\!\right]$ consists of all $\sum_{n=0}^{\infty}a_nt^n$, and its units are precisely the power series with nonzero constant term.

### Problem 1

(Problem 2.9-3) Let $R$ be an integral domain and $f\left(x\right)\in R\left[x\right]$. Prove that $a\in R$ is a root of $f\left(x\right)$ if and only if $\left(x-a\right)$ divides $f\left(x\right)$.

### Solution to Problem 1

Perform division of $f\left(x\right)$ by the monic polynomial $x-a$. By polynomial division with remainder, there exist $q\left(x\right)\in R\left[x\right]$ and a constant $c\in R$ such that

$$
f\left(x\right)=q\left(x\right)\left(x-a\right)+c,
$$

where the remainder has degree less than $1$, hence is a constant. Substituting $x=a$, and noting that $a\in R$ induces the evaluation homomorphism on $R\left[x\right]$, gives

$$
\begin{aligned}f\left(a\right)&=q\left(a\right)\cdot0+c\\&=c.\end{aligned}
$$

Hence $a$ is a root of $f\left(x\right)$, i.e. $f\left(a\right)=0$, if and only if $c=0$, which holds if and only if $f\left(x\right)=q\left(x\right)\left(x-a\right)$, i.e. $\left(x-a\right)\mid f\left(x\right)$. $\blacksquare$

### Problem 2

(Problem 2.9-4) Let $R$ be an integral domain, $f\left(x\right)\in R\left[x\right]$, and let $a_1,a_2,\cdots,a_s$ be distinct roots of $f\left(x\right)$. Then

$$
\left(x-a_1\right)\left(x-a_2\right)\cdots\left(x-a_s\right)
$$

divides $f\left(x\right)$. Use this to prove that a nonzero polynomial of degree $m$ over an integral domain has at most $m$ distinct roots.

### Solution to Problem 2

We induct on $s$. When $s=1$, this is the conclusion of Problem 1.

Assume the conclusion holds for $s-1$, i.e. $\prod_{i=1}^{s-1}\left(x-a_i\right)\mid f\left(x\right)$. Write

$$
f\left(x\right)=g\left(x\right)\prod_{i=1}^{s-1}\left(x-a_i\right).
$$

Substituting $x=a_s$, since $a_s$ is a root of $f$, $f\left(a_s\right)=0$, and so

$$
0=g\left(a_s\right)\prod_{i=1}^{s-1}\left(a_s-a_i\right).
$$

Since $a_1,\cdots,a_s$ are pairwise distinct, $a_s-a_i\ne0$ for $1\le i\le s-1$. Also $R$ is an integral domain with no zero divisors, so $g\left(a_s\right)=0$. By Problem 1, $\left(x-a_s\right)\mid g\left(x\right)$; write $g\left(x\right)=h\left(x\right)\left(x-a_s\right)$. Hence

$$
f\left(x\right)=h\left(x\right)\prod_{i=1}^{s}\left(x-a_i\right),
$$

i.e. $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. This completes the induction.

Now let $f\left(x\right)\ne0$ have degree $m$ and $s$ distinct roots $a_1,\cdots,a_s$. By the above, $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. This product is a polynomial of degree $s$, and it divides a polynomial of degree $m$, so $s\le m$. Hence a nonzero polynomial of degree $m$ over an integral domain has at most $m$ distinct roots. $\blacksquare$

### Problem 3

(Problem 2.9-11) Prove that the ring of formal power series $\mathbb R$ over the real field $\mathbb R\left[\!\left[t\right]\!\right]$ is a unique factorization domain.

### Solution to Problem 3

Write $R=\mathbb R\left[\!\left[t\right]\!\right]$. Take any nonzero power series $f\left(t\right)=\sum_{n=0}^{\infty}a_nt^n\in R$. Let $a_k$ be its first nonzero coefficient, i.e. $a_0=\cdots=a_{k-1}=0$, $a_k\ne0$; call $k$ the order of $f$, denoted $\operatorname{ord}\left(f\right)=k$. Then

$$
\begin{aligned}f\left(t\right)&=t^k\cdot\left(a_k+a_{k+1}t+\cdots\right)\\&=t^k\,u\left(t\right),\end{aligned}
$$

where the constant term of $u\left(t\right)=a_k+a_{k+1}t+\cdots$ is $a_k\ne0$. By the properties of the ring of formal power series, $u\left(t\right)$ is a unit (nonzero constant term implies invertibility).

First determine the irreducible elements of $R$. If $f$ is nonzero and not a unit, then $k=\operatorname{ord}\left(f\right)\ge1$, and $f=t^ku$. If $k=1$, $f=t\,u$ with $u$ a unit, so $f$ is an associate of $t$. Now $t$ is irreducible: if $t=\alpha\beta$, then

$$
1=\operatorname{ord}\left(t\right)=\operatorname{ord}\left(\alpha\right)+\operatorname{ord}\left(\beta\right),
$$

so one of $\operatorname{ord}\left(\alpha\right),\operatorname{ord}\left(\beta\right)$ is $0$ and the other is $1$, i.e. one of them is a unit. Hence $t$ is irreducible.

Thus any nonzero, non-unit element $f$ can be written as

$$
f=t^k\,u, u\text{ 为单位},
$$

where $k=\operatorname{ord}\left(f\right)$ is uniquely determined by $f$. That is, $f$ factors uniquely up to associates as the $t$-th power of the irreducible element $k$ times a unit. Also $t$ is prime (since

$$
t\mid fg\Rightarrow\operatorname{ord}\left(fg\right)\ge1\Rightarrow\operatorname{ord}\left(f\right)\ge1
$$

or $\operatorname{ord}\left(g\right)\ge1$, i.e. $t\mid f$ or $t\mid g$).

By the definition of a unique factorization domain, $R=\mathbb R\left[\!\left[t\right]\!\right]$ is a unique factorization domain. $\blacksquare$
