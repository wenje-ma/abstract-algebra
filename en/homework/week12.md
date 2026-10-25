# Assignment 12

> **Definition 2.1.8** (Ring Without Zero Divisors) If a ring $R$ is not the zero ring and has no zero divisors, then $R$ is called a ring without zero divisors.

> **Proposition 2.2.11** (Ideal Criterion) Let $R$ be a ring and $I$ a nonempty subset of $R$. Then $I$ is an ideal of $R$ if and only if $a-b\in I$ whenever $a,b\in I$, and $\alpha a,a\gamma\in I$ whenever $a\in I$ and $\alpha,\gamma\in R$.

> **Theorem 2.2.16** (Quotient Ring) Let $R$ be a ring and $I$ an ideal of $R$. Then the quotient additive group $R/I$ forms a ring under the multiplication $\left(a+I\right)\left(b+I\right)=ab+I$, called the quotient ring of $R$ by $I$.

> **Definition 2.2.20** (Integral Domain, Division Ring, and Field) A commutative ring with identity and without zero divisors is called an integral domain; if a ring with identity $R$ satisfies that $R^*$ forms a group under multiplication ($R^*=R\setminus\left\{0\right\}$), then $R$ is called a division ring; a commutative division ring is called a field.

### Problem 1

(Problem 2.2-3) Let $R$ be a ring without zero divisors and $I$ an ideal of $R$. Is the quotient ring $R/I$ necessarily a ring without zero divisors?

### Solution to Problem 1

Not necessarily. We give a counterexample.

Take the ring of integers $R=\mathbb Z$, which is an integral domain and hence satisfies **Definition 2.1.8** (Ring Without Zero Divisors). Take the ideal $I=6\mathbb Z$. By **Theorem 2.2.16** (Quotient Ring), the quotient ring is
$$
R/I=\mathbb Z/6\mathbb Z.
$$

In $\mathbb Z/6\mathbb Z$,
$$
\begin{aligned}\left(2+6\mathbb Z\right)\left(3+6\mathbb Z\right)&=6+6\mathbb Z\\&=0+6\mathbb Z,\end{aligned}
$$
but $2\notin 6\mathbb Z$ and $3\notin 6\mathbb Z$. Hence both $2+6\mathbb Z$ and $3+6\mathbb Z$ are nonzero zero divisors.

Therefore $R/I$ need not be a ring without zero divisors. $\blacksquare$

### Problem 2

(Problem 2.2-6) Let $R$ be a ring without zero divisors and have only finitely many ideals (including left ideals, right ideals and two-sided ideals). Prove that $R$ is a division ring.

### Solution to Problem 2

We first prove that $R$ has an identity. Take any $0\ne a\in R$ and consider the descending chain of left ideals
$$
R\supseteq Ra\supseteq Ra^2\supseteq\cdots.
$$

Since $R$ has only finitely many left ideals, this chain must stabilize, i.e. there exists $m$ with $Ra^m=Ra^{m+1}$. Then $a^m\in Ra^{m+1}$, so there exists $b\in R$ with $a^m=ba^{m+1}$. Set $e=ba$; then $ea^m=a^m$.

For any $x\in R$,
$$
\begin{aligned}\left(xe-x\right)a^m&=x\left(ea^m\right)-xa^m\\&=xa^m-xa^m\\&=0.\end{aligned}
$$

Since $a^m\ne0$ and $R$ has no right zero divisors, $xe-x=0$, i.e. $xe=x$ for all $x\in R$. Hence $e$ is a right identity of $R$, and $e\ne0$.

Also, for any $x\in R$,
$$
\begin{aligned}e\left(ex-x\right)&=e^2x-ex\\&=ex-ex\\&=0,\end{aligned}
$$
where we used that the right identity gives $e^2=e$. Since $e\ne0$ and $R$ has no left zero divisors, $ex-x=0$, i.e. $ex=x$. Hence $e$ is the identity element of $R$.

Now prove that every nonzero element is invertible. Take any $0\ne x\in R$; similarly the descending chain of left ideals $Rx\supseteq Rx^2\supseteq\cdots$ stabilizes, so there exists $n$ with $Rx^n=Rx^{n+1}$. Then there exists $y\in R$ with $x^n=yx^{n+1}=\left(yx\right)x^n$, i.e. $\left(e-yx\right)x^n=0$. Cancelling $x^n\ne0$ gives $yx=e$, i.e. $y$ is a left inverse of $x$. Also,
$$
\begin{aligned}\left(xy-e\right)x&=xyx-ex\\&=x\left(yx\right)-x\\&=xe-x\\&=0,\end{aligned}
$$
and $x\ne0$ gives $xy=e$. Hence $x$ has a two-sided inverse.

Thus $R^*=R\setminus\left\{0\right\}$ forms a group under multiplication. By **Definition 2.2.20** (Integral Domain, Division Ring, and Field), $R$ is a division ring. $\blacksquare$

### Problem 3

(Problem 2.2-11) Let $R$ be a commutative ring and $I$ an ideal of $R$. Define
$$
\sqrt{I}=\left\{a\in R\mid\exists\,n\in\mathbb N,\;a^n\in I\right\}.
$$

Prove that $\sqrt{I}$ is also an ideal of $R$, called the radical of the ideal $I$. In particular, the set of all nilpotent elements of $R$ (i.e. the radical of the ideal $\left\{0\right\}$) forms an ideal of $R$, called the nilradical of $R$ and denoted $\operatorname{Rad}R$. Prove that for any ideal $I$ of $R$, $\sqrt{\sqrt{I}}=\sqrt{I}$.

### Solution to Problem 3

**First prove that $\sqrt{I}$ is an ideal.** We verify using **Proposition 2.2.11** (Ideal Criterion).

First, $0\in\sqrt{I}$, so $\sqrt{I}$ is nonempty.

Let $a,b\in\sqrt{I}$; then there exist $m,n\in\mathbb N$ with $a^m\in I$, $b^n\in I$. Since $R$ is commutative, the binomial theorem gives
$$
\left(a-b\right)^{m+n-1}=\sum_{k=0}^{m+n-1}\binom{m+n-1}{k}a^k\left(-b\right)^{m+n-1-k}.
$$

For any term on the right-hand side: if $k\ge m$, then $a^k=a^m a^{k-m}\in I$; if $k< m$, then $m+n-1-k\ge n$, so $b^{m+n-1-k}=b^n b^{m-1-k}\in I$. Hence every term lies in $I$, i.e. $\left(a-b\right)^{m+n-1}\in I$, and thus $a-b\in\sqrt{I}$.

Now let $a\in\sqrt{I}$, $r\in R$, and $a^n\in I$; then $\left(ra\right)^n=r^n a^n\in I$ (since $R$ is commutative and $I$ is an ideal), so $ra\in\sqrt{I}$.

By **Proposition 2.2.11** (Ideal Criterion), $\sqrt{I}$ is an ideal of $R$. Taking $I=\left\{0\right\}$, $\sqrt{\left\{0\right\}}$ is precisely the set of all nilpotent elements of $R$ (i.e. elements $a$ with $a^n=0$), and it forms an ideal, namely the nilradical $\operatorname{Rad}R$.

**Now prove $\sqrt{\sqrt{I}}=\sqrt{I}$.**

First show $\sqrt{I}\subseteq\sqrt{\sqrt{I}}$. Let $a\in\sqrt{I}$; then $a^n\in I$. Since $I\subseteq\sqrt{I}$ (if $x\in I$, then $x^1\in I$, so $x\in\sqrt{I}$), we have $a^n\in\sqrt{I}$, i.e. $a\in\sqrt{\sqrt{I}}$.

Next show $\sqrt{\sqrt{I}}\subseteq\sqrt{I}$. Let $a\in\sqrt{\sqrt{I}}$; then there exists $n$ with $a^n\in\sqrt{I}$. Hence there exists $m$ with $\left(a^n\right)^m=a^{nm}\in I$, so $a\in\sqrt{I}$.

Therefore $\sqrt{\sqrt{I}}=\sqrt{I}$. $\blacksquare$

### Problem 4

(Problem 2.2-13) Let $R$ be a commutative ring, and define an operation on $R$ by
$$
a\circ b=a+b-ab.
$$
(1) Prove that $\circ$ is associative and that $0\circ a=a$ for all $a\in R$;
(2) Prove that $R$ is a field if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group, where $e$ is the identity element of $R$.

### Solution to Problem 4

(1) For any $a,b,c\in R$,
$$
\begin{aligned}\left(a\circ b\right)\circ c&=\left(a+b-ab\right)\circ c\\&=\left(a+b-ab\right)+c-\left(a+b-ab\right)c\\&=a+b+c-ab-ac-bc+abc,\end{aligned}
$$
and
$$
\begin{aligned}a\circ\left(b\circ c\right)&=a\circ\left(b+c-bc\right)\\&=a+\left(b+c-bc\right)-a\left(b+c-bc\right)\\&=a+b+c-ab-ac-bc+abc.\end{aligned}
$$

The two are equal, so $\circ$ is associative. Also $0\circ a=0+a-0\cdot a=a$. Moreover, since $R$ is commutative, $a\circ b=b\circ a$, so $\circ$ is commutative as well.

(2) Consider the map $\psi:R\to R$, $\psi\left(x\right)=e-x$. Clearly $\psi$ is a bijection, with $\psi\left(0\right)=e$ and $\psi\left(e\right)=0$. For any $a,b\in R$,
$$
\begin{aligned}\psi\left(a\right)\circ\psi\left(b\right)&=\left(e-a\right)\circ\left(e-b\right)\\&=\left(e-a\right)+\left(e-b\right)-\left(e-a\right)\left(e-b\right)\\&=e-ab\\&=\psi\left(ab\right).\end{aligned}
$$

Thus $\psi$ transports multiplication on $R$ homomorphically to the operation $\circ$, and $\psi$ restricts to a bijection from $R\setminus\left\{0\right\}$ to $R\setminus\left\{e\right\}$. Therefore $\left(R\setminus\left\{0\right\},\cdot\right)$ is an abelian group if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group.

By **Definition 2.2.20** (Integral Domain, Division Ring, and Field), the commutative ring with identity $R$ is a field if and only if $R\setminus\left\{0\right\}$ forms an abelian group under multiplication. Hence $R$ is a field if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group. $\blacksquare$
