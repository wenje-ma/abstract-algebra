# week11

> **Basic Knowledge: Properties of Invertible Elements in a Unital Ring**<br>Let $R$ be a unital ring with identity $e$. If $u,v\in R$ are both invertible, then $uv$ is invertible and $\left(uv\right)^{-1}=v^{-1}u^{-1}$.

> **Basic Knowledge: Nilpotent Elements and Finite Geometric Series**<br>Let $R$ be a unital ring with identity $e$. If $x^{m}=0$ ($m\in\mathbb N$), then the finite geometric series gives
$$
\left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}.
$$

> **Definition 2.1.1 (Ring)**<br>Let $R$ be a nonempty set on which two binary operations $+$ and $\cdot$ are defined, satisfying: (1) $\left[R;+\right]$ is an abelian group; (2) $\left[R;\cdot\right]$ is a semigroup (multiplication is associative); (3) multiplication distributes over addition on both sides: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$ (for all $a,b,c\in R$). Then $R$ is called a ring.

---

## 2.1-3

Let $R=\left\{a,b,c\right\}$ be a set on which addition and multiplication are defined. Suppose the operation tables of addition $+$ and multiplication $\cdot$ are

$$
\begin{array}{c|ccc}
+ & a & b & c\\\hline
a & a & b & c\\
b & b & c & a\\
c & c & a & b
\end{array}
\qquad
\begin{array}{c|ccc}
\cdot & a & b & c\\\hline
a & a & a & a\\
b & a & a & a\\
c & a & b & a
\end{array}
$$

Is $R$ a ring?

### Solution 2.1-3

From the addition table, $a$ is the additive zero, and $\left(R,+\right)\cong\mathbb Z_3$ (under $a\mapsto0$, $b\mapsto1$, $c\mapsto2$); hence $\left(R,+\right)$ is an abelian group, satisfying condition (1) of **Definition 2.1.1 (Ring)**.

Next we check the distributive law. Take $x=b$, $y=c$, $z=b$. From the addition table, $b+c=a$; from the multiplication table, $a\cdot b=a$, $b\cdot b=a$, $c\cdot b=b$.

Compute the left-hand side:

$$
\left(x+y\right)z=\left(b+c\right)b=a\cdot b=a.
$$

Compute the right-hand side:

$$
xz+yz=b\cdot b+c\cdot b=a+b=b.
$$

Since $a\ne b$,

$$
\left(b+c\right)b\ne b\cdot b+c\cdot b.
$$

The left distributive law fails.

Moreover, associativity of multiplication also fails: take $x=c$, $y=c$, $z=b$. From the multiplication table, $c\cdot c=a$, $c\cdot b=b$, $a\cdot b=a$, so

$$
\left(c\cdot c\right)\cdot b=a\cdot b=a,
$$

whereas

$$
c\cdot\left(c\cdot b\right)=c\cdot b=b.
$$

The two are unequal.

Therefore $R$ fails the associativity of multiplication and the distributive law required by **Definition 2.1.1 (Ring)**, so $R$ is not a ring. $\blacksquare$

---

## 2.1-5

Let $R$ be a unital ring with identity $e$, and let $a\in R$. If there exists $m\in\mathbb N$ such that $a^{m}=0$, then $a$ is called a nilpotent element. Prove: if $a$ is nilpotent, then $e+a$ is invertible.

### Solution 2.1-5

Suppose $a^{m}=0$. Construct

$$
b=e-a+a^{2}-a^{3}+\cdots+\left(-1\right)^{m-1}a^{m-1}.
$$

Compute the product (expanding by the distributive law of **Definition 2.1.1 (Ring)**):

$$
\left(e+a\right)b=\left(e+a\right)\left(e-a+a^{2}-\cdots+\left(-1\right)^{m-1}a^{m-1}\right)=e+\left(-1\right)^{m-1}a^{m}=e,
$$

the middle terms cancel out, and $a^{m}=0$. Similarly,

$$
b\left(e+a\right)=\left(e-a+a^{2}-\cdots+\left(-1\right)^{m-1}a^{m-1}\right)\left(e+a\right)=e+\left(-1\right)^{m-1}a^{m}=e.
$$

Hence $b$ is an inverse of $e+a$, so $e+a$ is invertible. This agrees with **Basic Knowledge: Nilpotent Elements and Finite Geometric Series**. $\blacksquare$

---

## 2.1-15

(Hua) Let $R$ be a unital ring with identity $e$, and let $a\in R$. If an element $c$ satisfies $ca=e$ ($ac=e$), then $c$ is called a left inverse (right inverse) of $a$. If $c$ is both a left inverse and a right inverse of $a$, then $c$ is called an inverse of $a$, and $a$ is said to be invertible. Prove: for any $a,b\in R$, $e-ab$ is invertible if and only if $e-ba$ is invertible.

### Solution 2.1-15

First suppose $e-ab$ is invertible, and let $c=\left(e-ab\right)^{-1}$. Construct

$$
d=e+bca.
$$

We verify that $d$ is an inverse of $e-ba$. Expanding by the distributive law of **Definition 2.1.1 (Ring)**:

$$
\left(e-ba\right)d=\left(e-ba\right)\left(e+bca\right)=e-ba+bca-babca=e-ba+b\left(e-ab\right)ca=e-ba+ba=e,
$$

where we used $\left(e-ab\right)c=e$. Similarly,

$$
d\left(e-ba\right)=\left(e+bca\right)\left(e-ba\right)=e-ba+bca-bcaba=e-ba+bc\left(e-ab\right)a=e-ba+ba=e,
$$

where we used $c\left(e-ab\right)=e$. Hence $d=e+bca$ is an inverse of $e-ba$, so $e-ba$ is invertible.

Conversely, if $e-ba$ is invertible, interchanging $a$ and $b$ in the above argument yields that $e-ab$ is invertible.

Therefore $e-ab$ is invertible if and only if $e-ba$ is invertible. $\blacksquare$

---

## 2.1-16

(Hua) Let $R$ be a unital ring with identity $e$, and let $a,b\in R$. Prove: if $ab$ and $ab-e$ are both invertible, then $a-b^{-1}$ is invertible, and $\left(a-b^{-1}\right)^{-1}-a^{-1}$ is also invertible, with

$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

### Solution 2.1-16

Since $b^{-1}$ is invertible (the conclusion involves $b^{-1}$, so $b$ is invertible by hypothesis) and $ab$ is invertible, by **Basic Knowledge: Properties of Invertible Elements in a Unital Ring**, $a=\left(ab\right)b^{-1}$ is a product of invertible elements, so $a$ is invertible and $a^{-1}$ exists.

Also, since $b^{-1}$ is invertible, by the distributive law of **Definition 2.1.1 (Ring)**,

$$
a-b^{-1}=\left(ab-e\right)b^{-1}.
$$

Since $ab-e$ is invertible by hypothesis and $b^{-1}$ is invertible, by **Basic Knowledge: Properties of Invertible Elements in a Unital Ring**, the product of invertible elements is invertible, so $a-b^{-1}$ is invertible, and

$$
\left(a-b^{-1}\right)^{-1}=b\left(ab-e\right)^{-1}.
$$

Write $X=ab-e$; then $X^{-1}$ exists. We need to show that

$$
\left(a-b^{-1}\right)^{-1}-a^{-1}=bX^{-1}-a^{-1}
$$

is invertible, with inverse $aba-a=a\left(ba-e\right)$.

Compute the product (by the distributive law of **Definition 2.1.1 (Ring)**):

$$
\left(bX^{-1}-a^{-1}\right)\cdot a\left(ba-e\right)=bX^{-1}a\left(ba-e\right)-a^{-1}a\left(ba-e\right)=\left[bX^{-1}a-e\right]\left(ba-e\right).
$$

By the Hua identity from **Problem 2.1-15**,

$$
\left(e-ba\right)^{-1}=e+b\left(e-ab\right)^{-1}a.
$$

Note that $X=ab-e=-\left(e-ab\right)$, so $X^{-1}=-\left(e-ab\right)^{-1}$; hence

$$
bX^{-1}a=-b\left(e-ab\right)^{-1}a=-\left[\left(e-ba\right)^{-1}-e\right]=e-\left(e-ba\right)^{-1}.
$$

Therefore

$$
bX^{-1}a-e=-\left(e-ba\right)^{-1}.
$$

Also $ba-e=-\left(e-ba\right)$, so

$$
\left[bX^{-1}a-e\right]\left(ba-e\right)=\left(-\left(e-ba\right)^{-1}\right)\cdot\left(-\left(e-ba\right)\right)=\left(e-ba\right)^{-1}\left(e-ba\right)=e.
$$

Similarly one verifies the other direction $\left(ba-e\right)\cdot\left(bX^{-1}-a^{-1}\right)=e$: since $\left(ba-e\right)=-\left(e-ba\right)$ and $bX^{-1}a-e=-\left(e-ba\right)^{-1}$, after exchanging positions in the same way the product is still $e$. Hence $a\left(ba-e\right)=aba-a$ is an inverse of

$$
bX^{-1}-a^{-1}=\left(a-b^{-1}\right)^{-1}-a^{-1},
$$

i.e.

$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

$\blacksquare$
