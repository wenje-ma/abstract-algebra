# week18

> **Basic Knowledge: Polynomial Division with Remainder**<br>Let $R$ be a commutative unital ring and $f\left(x\right),g\left(x\right)\in R\left[x\right]$, with the leading coefficient of $g\left(x\right)$ a unit in $R$. Then there exist unique $q\left(x\right),r\left(x\right)\in R\left[x\right]$ such that $f\left(x\right)=q\left(x\right)g\left(x\right)+r\left(x\right)$, where $r=0$ or $\deg r< \deg g$. In particular, when the divisor is a monic linear polynomial $x-a$, the remainder is a constant.

> **Basic Knowledge: Unique Factorization Domain**<br>An integral domain $R$ is called a unique factorization domain if every nonzero nonunit element of $R$ factors as a finite product of irreducible elements, and the factorization is unique up to associates.

> **Basic Knowledge: Formal Power Series Ring**<br>The formal power series ring $k\left[\!\left[t\right]\!\right]$ over a field $k$ consists of all $\sum_{n=0}^{\infty}a_nt^n$; its units are exactly the power series with nonzero constant term.

---

## 2.9-3

Let $R$ be an integral domain and $f\left(x\right)\in R\left[x\right]$. Then $a\in R$ is a root of $f\left(x\right)$ if and only if $\left(x-a\right)$ divides $f\left(x\right)$.

### Solution 2.9-3

Divide $f\left(x\right)$ by the monic polynomial $x-a$; by **Basic Knowledge: Polynomial Division with Remainder**, there exist $q\left(x\right)\in R\left[x\right]$ and a constant $c\in R$ such that $f\left(x\right)=q\left(x\right)\left(x-a\right)+c$, where the remainder has degree less than $1$, hence is a constant. Substituting $x=a$, using that $a\in R$ evaluates elements of $R\left[x\right]$, gives $f\left(a\right)=q\left(a\right)\cdot0+c=c$.

Thus $a$ is a root of $f\left(x\right)$, i.e. $f\left(a\right)=0$, iff $c=0$, iff $f\left(x\right)=q\left(x\right)\left(x-a\right)$, i.e. $\left(x-a\right)\mid f\left(x\right)$. $\blacksquare$

---

## 2.9-4

Let $R$ be an integral domain and $f\left(x\right)\in R\left[x\right]$, with $a_1,a_2,\cdots,a_s$ distinct roots of $f\left(x\right)$. Then $\left(x-a_1\right)\left(x-a_2\right)\cdots\left(x-a_s\right)$ divides $f\left(x\right)$. Deduce that a nonzero polynomial of degree $m$ over an integral domain has at most $m$ distinct roots.

### Solution 2.9-4

Induct on $s$. For $s=1$, this is the result of **2.9-3**.

Assume the result holds for $s-1$, i.e. $\prod_{i=1}^{s-1}\left(x-a_i\right)\mid f\left(x\right)$. Write $f\left(x\right)=g\left(x\right)\prod_{i=1}^{s-1}\left(x-a_i\right)$. Substituting $x=a_s$, since $a_s$ is a root of $f$, $f\left(a_s\right)=0$, gives $0=g\left(a_s\right)\prod_{i=1}^{s-1}\left(a_s-a_i\right)$.

Since $a_1,\cdots,a_s$ are pairwise distinct, $a_s-a_i\ne0$ for $1\le i\le s-1$. As $R$ is an integral domain with no zero divisors, $g\left(a_s\right)=0$. By **2.9-3**, $\left(x-a_s\right)\mid g\left(x\right)$; write $g\left(x\right)=h\left(x\right)\left(x-a_s\right)$. Then $f\left(x\right)=h\left(x\right)\prod_{i=1}^{s}\left(x-a_i\right)$, i.e. $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. This completes the induction.

Now let $f\left(x\right)\ne0$ have degree $m$ and $s$ distinct roots $a_1,\cdots,a_s$. By the above, $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. This product is degree $s$, and it divides a degree-$m$ polynomial, so $s\le m$. Thus a nonzero polynomial of degree $m$ over an integral domain has at most $m$ distinct roots. $\blacksquare$

---

## 2.9-11

Prove that the formal power series ring $\mathbb R\left[\!\left[t\right]\!\right]$ over the real field $\mathbb R$ is a unique factorization domain.

### Solution 2.9-11

Set $R=\mathbb R\left[\!\left[t\right]\!\right]$. Take any nonzero power series $f\left(t\right)=\sum_{n=0}^{\infty}a_nt^n\in R$. Let $a_k$ be its first nonzero coefficient, i.e. $a_0=\cdots=a_{k-1}=0$, $a_k\ne0$; call $k$ the order of $f$, written $\operatorname{ord}\left(f\right)=k$. Then $f\left(t\right)=t^k\cdot\left(a_k+a_{k+1}t+\cdots\right)=t^k\,u\left(t\right)$, where $u\left(t\right)=a_k+a_{k+1}t+\cdots$ has nonzero constant term $a_k$. By **Basic Knowledge: Formal Power Series Ring**, $u\left(t\right)$ is a unit (a power series with nonzero constant term is invertible).

First determine the irreducible elements of $R$. If $f$ is nonzero and a nonunit, then $k=\operatorname{ord}\left(f\right)\ge1$ and $f=t^ku$. If $k=1$, $f=t\,u$ with $u$ a unit, so $f$ is associate to $t$. And $t$ is irreducible: if $t=\alpha\beta$, then $1=\operatorname{ord}\left(t\right)=\operatorname{ord}\left(\alpha\right)+\operatorname{ord}\left(\beta\right)$, so one of $\operatorname{ord}\left(\alpha\right),\operatorname{ord}\left(\beta\right)$ is $0$ and the other $1$, i.e. one of them is a unit. Hence $t$ is irreducible.

Thus any nonzero nonunit $f$ can be written as $f=t^k\,u$ with $u$ a unit, where $k=\operatorname{ord}\left(f\right)$ is uniquely determined by $f$. That is, $f$ factors uniquely up to associates as the $k$-th power of the irreducible $t$ times a unit. Also $t$ is prime: $t\mid fg\Rightarrow\operatorname{ord}\left(fg\right)\ge1\Rightarrow\operatorname{ord}\left(f\right)\ge1$ or $\operatorname{ord}\left(g\right)\ge1$, i.e. $t\mid f$ or $t\mid g$.

By the definition in **Basic Knowledge: Unique Factorization Domain**, $R=\mathbb R\left[\!\left[t\right]\!\right]$ is a unique factorization domain. $\blacksquare$
