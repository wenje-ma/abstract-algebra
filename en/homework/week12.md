# week12

> **Basic Knowledge: Binomial Theorem in a Commutative Ring**<br>Let $R$ be a commutative ring, $a,b\in R$, and $n$ a positive integer. Then
$$
\left(a-b\right)^{n}=\sum_{k=0}^{n}\binom{n}{k}a^{k}\left(-b\right)^{n-k},
$$
and the commutativity of $R$ allows the terms to be collected.

> **Basic Knowledge: The Integer Ring $\mathbb Z$ Is an Integral Domain**<br>The integer ring $\mathbb Z$ is an integral domain, hence satisfies **Definition 2.1.8 (Ring Without Zero Divisors)**; moreover, for every $m\ge0$, $m\mathbb Z$ is an ideal of $\mathbb Z$, and the quotient ring $\mathbb Z/m\mathbb Z$ is written $\mathbb Z_m$.

> **Basic Knowledge: Cancellation with Nonzero Elements**<br>In a ring $R$ without zero divisors, if $ab=0$ and $a\ne0$, then $b=0$; if $ba=0$ and $a\ne0$, then $b=0$ (otherwise a zero divisor would occur).

> **Definition 2.1.1 (Ring)**<br>Let $R$ be a nonempty set on which two binary operations $+$ and $\cdot$ are defined, satisfying: (1) $\left[R;+\right]$ is an abelian group; (2) $\left[R;\cdot\right]$ is a semigroup; (3) multiplication distributes over addition on both sides: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$. Then $R$ is called a ring.

> **Definition 2.1.8 (Ring Without Zero Divisors)**<br>If a ring $R$ is not the zero ring and has no zero divisors, then $R$ is called a ring without zero divisors.

> **Proposition 2.2.11 (Criterion for Ideals)**<br>Let $R$ be a ring and $I$ a nonempty subset of $R$. Then $I$ is an ideal of $R$ if and only if $a-b\in I$ and $ax,ya\in I$ for all $a,b\in I$ and $x,y\in R$.

> **Theorem 2.2.16 (Quotient Ring)**<br>Let $R$ be a ring and $I$ an ideal of $R$. Then the quotient additive group $R/I$ becomes a ring under the multiplication $\left(a+I\right)\left(b+I\right)=ab+I$, called the quotient ring of $R$ by $I$.

> **Definition 2.2.20 (Integral Domain, Division Ring, and Field)**<br>A commutative unital ring without zero divisors is called an integral domain; if a unital ring $R$ satisfies that $R^{*}$ forms a group under multiplication (where $R^{*}=R\setminus\left\{0\right\}$), then $R$ is called a division ring; a commutative division ring is called a field.

---

## 2.2-3

Let $R$ be a ring without zero divisors and $I$ an ideal of $R$. Is the quotient ring $R/I$ necessarily a ring without zero divisors?

### Solution 2.2-3

Not necessarily. We give a counterexample below.

Take the integer ring $R=\mathbb Z$. By **Basic Knowledge: The Integer Ring $\mathbb Z$ Is an Integral Domain**, $\mathbb Z$ is an integral domain, hence satisfies **Definition 2.1.8 (Ring Without Zero Divisors)**. Take the ideal $I=6\mathbb Z$. By **Theorem 2.2.16 (Quotient Ring)**, the quotient ring is

$$
R/I=\mathbb Z/6\mathbb Z=\mathbb Z_6.
$$

In $\mathbb Z_6$,

$$
\left(2+6\mathbb Z\right)\left(3+6\mathbb Z\right)=6+6\mathbb Z=0+6\mathbb Z,
$$

but $2\notin6\mathbb Z$ and $3\notin6\mathbb Z$; hence $2+6\mathbb Z$ and $3+6\mathbb Z$ are both nonzero zero divisors. By **Definition 2.1.8 (Ring Without Zero Divisors)**, $R/I$ is not a ring without zero divisors.

Therefore $R/I$ is not necessarily a ring without zero divisors. $\blacksquare$

---

## 2.2-6

Let $R$ be a ring without zero divisors with only finitely many ideals (including left ideals, right ideals and two-sided ideals). Prove that $R$ is a division ring.

### Solution 2.2-6

**First prove that $R$ has an identity.** Since $R$ is a ring without zero divisors, by **Definition 2.1.8 (Ring Without Zero Divisors)** $R$ is not the zero ring, so there exists $0\ne a\in R$. Consider the descending chain of left ideals

$$
R\supseteq Ra\supseteq Ra^{2}\supseteq\cdots.
$$

Since $R$ has only finitely many left ideals, this chain must stabilize, i.e. there exists $m$ with $Ra^{m}=Ra^{m+1}$. Hence $a^{m}\in Ra^{m+1}$, so there exists $b\in R$ with $a^{m}=ba^{m+1}$. Put $e=ba$; then $ea^{m}=a^{m}$.

For any $x\in R$,

$$
\left(xe-x\right)a^{m}=x\left(ea^{m}\right)-xa^{m}=xa^{m}-xa^{m}=0.
$$

Since $a^{m}\ne0$ (from $a\ne0$ and **Definition 2.1.8 (Ring Without Zero Divisors)**, $a^{m}\ne0$), by **Basic Knowledge: Cancellation with Nonzero Elements** we get $xe-x=0$, i.e. $xe=x$ for all $x\in R$. Hence $e$ is a right identity of $R$, and $e\ne0$ (otherwise $xe=x$ would give $x=0$ for all $x$, contradicting that $R$ is not the zero ring).

Also, for any $x\in R$,

$$
e\left(ex-x\right)=e^{2}x-ex=ex-ex=0,
$$

where we used that the right identity gives $e^{2}=e\cdot e=e$. Since $e\ne0$ and $e\left(ex-x\right)=0$, by **Basic Knowledge: Cancellation with Nonzero Elements** we get $ex-x=0$, i.e. $ex=x$. Hence $e$ is also a left identity, so $e$ is the identity of $R$.

**Next prove that every nonzero element is invertible.** Take any $0\ne x\in R$. Similarly, the descending chain of left ideals $Rx\supseteq Rx^{2}\supseteq\cdots$ stabilizes because there are only finitely many left ideals; there exists $n$ with $Rx^{n}=Rx^{n+1}$. Hence there exists $y\in R$ with $x^{n}=yx^{n+1}=\left(yx\right)x^{n}$, i.e. $\left(e-yx\right)x^{n}=0$. Since $x^{n}\ne0$, by **Basic Knowledge: Cancellation with Nonzero Elements** we get $e-yx=0$, i.e. $yx=e$. Hence $y$ is a left inverse of $x$.

Moreover,

$$
\left(xy-e\right)x=xyx-ex=x\left(yx\right)-x=xe-x=0,
$$

and since $x\ne0$, by **Basic Knowledge: Cancellation with Nonzero Elements** we get $xy=e$. Hence $x$ also has the right inverse $y$, i.e. $x$ is invertible.

Thus every element of $R^{*}=R\setminus\left\{0\right\}$ is invertible, so $R^{*}$ forms a group under multiplication. By **Definition 2.2.20 (Integral Domain, Division Ring, and Field)**, $R$ is a division ring. $\blacksquare$

---

## 2.2-11

Let $R$ be a commutative ring and $I$ an ideal of $R$. Define

$$
\sqrt{I}=\left\{a\in R\mid\exists\,n\in\mathbb N,\;a^{n}\in I\right\}.
$$

Prove that $\sqrt{I}$ is also an ideal of $R$, called the radical of the ideal $I$. In particular, the set of all nilpotent elements of $R$ (i.e. the radical of the ideal $\left\{0\right\}$) is an ideal of $R$, called the nilradical of $R$, denoted $\mathrm{Rad}\,R$. Prove that for every ideal $I$ of $R$, $\sqrt{\sqrt{I}}=\sqrt{I}$.

### Solution 2.2-11

**First prove that $\sqrt{I}$ is an ideal.** We verify using **Proposition 2.2.11 (Criterion for Ideals)**.

First, $0\in\sqrt{I}$ (take $n=1$; $0\in I$), so $\sqrt{I}$ is nonempty.

Let $a,b\in\sqrt{I}$; then there exist $m,n\in\mathbb N$ with $a^{m}\in I$ and $b^{n}\in I$. Since $R$ is commutative, by **Basic Knowledge: Binomial Theorem in a Commutative Ring**,

$$
\left(a-b\right)^{m+n-1}=\sum_{k=0}^{m+n-1}\binom{m+n-1}{k}a^{k}\left(-b\right)^{m+n-1-k}.
$$

For any term on the right: if $k\ge m$, then $a^{k}=a^{m}a^{k-m}\in I$; if $k<m$, then $m+n-1-k\ge n$, so $\left(-b\right)^{m+n-1-k}=b^{m+n-1-k}\in I$ (because $b^{n}\in I$). Hence every term belongs to $I$, i.e. $\left(a-b\right)^{m+n-1}\in I$, so $a-b\in\sqrt{I}$.

Next let $a\in\sqrt{I}$, $r\in R$ with $a^{n}\in I$; then $\left(ra\right)^{n}=r^{n}a^{n}\in I$ ($R$ is commutative and $I$ is an ideal, by **Proposition 2.2.11 (Criterion for Ideals)**), so $ra\in\sqrt{I}$.

By **Proposition 2.2.11 (Criterion for Ideals)**, $\sqrt{I}$ is an ideal of $R$. Taking $I=\left\{0\right\}$, $\sqrt{\left\{0\right\}}$ is exactly the set of all nilpotent elements of $R$ (i.e. elements satisfying $a^{n}=0$); it is an ideal, namely the nilradical $\mathrm{Rad}\,R$.

**Next prove $\sqrt{\sqrt{I}}=\sqrt{I}$.**

First prove $\sqrt{I}\subseteq\sqrt{\sqrt{I}}$: let $a\in\sqrt{I}$; then $a^{n}\in I$ for some $n$. Since $I\subseteq\sqrt{I}$ (for $x\in I$, $x^{1}\in I$, so $x\in\sqrt{I}$), we have $a^{n}\in\sqrt{I}$, i.e. $a\in\sqrt{\sqrt{I}}$.

Next prove $\sqrt{\sqrt{I}}\subseteq\sqrt{I}$: let $a\in\sqrt{\sqrt{I}}$; then $a^{n}\in\sqrt{I}$ for some $n$, so there exists $m$ with $\left(a^{n}\right)^{m}=a^{nm}\in I$, hence $a\in\sqrt{I}$.

In conclusion, $\sqrt{\sqrt{I}}=\sqrt{I}$. $\blacksquare$

---

## 2.2-13

Let $R$ be a commutative ring, and define an operation on $R$ by $a\circ b=a+b-ab$.

(1) Prove that $\circ$ is associative, and $0\circ a=a$ for all $a\in R$;

(2) Prove that $R$ is a field if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group, where $e$ is the identity of $R$.

### Solution 2.2-13

**Part (1).** For any $a,b,c\in R$, expanding by the distributive law of **Definition 2.1.1 (Ring)**:

$$
\left(a\circ b\right)\circ c=\left(a+b-ab\right)\circ c=\left(a+b-ab\right)+c-\left(a+b-ab\right)c=a+b+c-ab-ac-bc+abc,
$$

and

$$
a\circ\left(b\circ c\right)=a\circ\left(b+c-bc\right)=a+\left(b+c-bc\right)-a\left(b+c-bc\right)=a+b+c-ab-ac-bc+abc.
$$

The two are equal, so $\circ$ is associative. Moreover,

$$
0\circ a=0+a-0\cdot a=a.
$$

Also, since $R$ is commutative, $a\circ b=a+b-ab=b+a-ba=b\circ a$, so $\circ$ is commutative.

**Part (2).** Consider the map $\psi:R\to R$, $\psi\left(x\right)=e-x$. Clearly $\psi$ is bijective (it is its own inverse), with $\psi\left(0\right)=e$ and $\psi\left(e\right)=0$. For any $a,b\in R$,

$$
\psi\left(a\right)\circ\psi\left(b\right)=\left(e-a\right)\circ\left(e-b\right)=\left(e-a\right)+\left(e-b\right)-\left(e-a\right)\left(e-b\right)=e-ab=\psi\left(ab\right).
$$

Hence $\psi$ transfers the multiplication of $R$ homomorphically to the operation $\circ$, and $\psi$ restricts to a bijection from $R\setminus\left\{0\right\}$ to $R\setminus\left\{e\right\}$ ($\psi\left(x\right)=e$ if and only if $x=0$). Therefore $\left(R\setminus\left\{0\right\},\cdot\right)$ is an abelian group if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group.

By **Definition 2.2.20 (Integral Domain, Division Ring, and Field)**, a commutative unital ring $R$ is a field if and only if $R\setminus\left\{0\right\}$ forms an abelian group under multiplication. Hence $R$ is a field if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group. $\blacksquare$
