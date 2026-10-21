# Assignment 11

> **Definition 2.1.1** (Ring) Let $R$ be a nonempty set on which two binary operations $+$ and $\cdot$ are defined, satisfying:
> (1) $\left[R;+\right]$ is an abelian group;
> (2) $\left[R;\cdot\right]$ is a semigroup (multiplication is associative);
> (3) multiplication is left and right distributive over addition: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$.
> Then $R$ is called a ring.

> **Basic Knowledge** (Properties of Invertible Elements in a Ring with Identity) Let $R$ be a ring with identity and $e$ its identity element. If $u,v\in R$ are invertible, then $uv$ is invertible and $\left(uv\right)^{-1}=v^{-1}u^{-1}$. If $x^{m}=0$, the finite geometric series gives
> $$
> \left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}.
> $$

### Problem 1

(Problem 2.1-3) Let $R=\left\{a,b,c\right\}$ be a set on which addition and multiplication are defined. If the addition $+$ and multiplication $\cdot$ tables are respectively
$$
\begin{array}{c\left|ccc}
+ & a & b & c\\hline
a & a & b & c\\
b & b & c & a\\
c & c & a & b
\end{array}
\begin{array}{c\right|ccc}
\cdot & a & b & c\\hline
a & a & a & a\\
b & a & a & a\\
c & a & b & a
\end{array}
$$
determine whether $R$ forms a ring.

### Solution to Problem 1

From the addition table, $a$ is the additive identity, and $\left(R,+\right)\cong\mathbb Z_3$ (under $a\mapsto0$, $b\mapsto1$, $c\mapsto2$), so $\left(R,+\right)$ is an abelian group, satisfying condition (1) of **Definition 2.1.1** (Ring).

We now check the distributive law. Take $x=b$, $y=c$, $z=b$. From the addition table, $b+c=a$. From the multiplication table, $a\cdot b=a$, $b\cdot b=a$, $c\cdot b=b$.

First compute the left-hand side:
$$
\begin{aligned}\left(x+y\right)z&=\left(b+c\right)b\\&=a\cdot b\\&=a.\end{aligned}
$$

Next compute the right-hand side:
$$
\begin{aligned}xz+yz&=bb+cb\\&=a+b\\&=b.\end{aligned}
$$

Since $a\ne b$,
$$
\left(b+c\right)b\ne bb+cb.
$$
Left distributivity fails. Moreover, multiplication is also not associative: take $x=c$, $y=c$, $z=b$; from the multiplication table $c\cdot c=a$, $c\cdot b=b$, $a\cdot b=a$, so
$$
\begin{aligned}\left(c\cdot c\right)\cdot b&=a\cdot b\\&=a,\end{aligned}
$$
whereas
$$
\begin{aligned}c\cdot\left(c\cdot b\right)&=c\cdot b\\&=b.\end{aligned}
$$
The two are unequal.

Hence $R$ satisfies neither the distributive law nor the associativity of multiplication, and $R$ does not form a ring. $\blacksquare$

### Problem 2

(Problem 2.1-5) Let $R$ be a ring with identity, $e$ its identity element, and $a\in R$. If there exists $m\in\mathbb N$ such that $a^{m}=0$, then $a$ is called nilpotent. Prove that if $a$ is nilpotent, then $e+a$ is invertible.

### Solution to Problem 2

Assume $a^{m}=0$. Construct
$$
b=e-a+a^{2}-a^{3}+\cdots+\left(-1\right)^{m-1}a^{m-1}.
$$

Compute the product:
$$
\begin{aligned}\left(e+a\right)b&=\left(e+a\right)\left(e-a+a^{2}-\cdots+\left(-1\right)^{m-1}a^{m-1}\right)\\&=e+\left(-1\right)^{m-1}a^{m}\\&=e,\end{aligned}
$$
where all intermediate terms cancel and $a^{m}=0$. Similarly,
$$
\begin{aligned}b\left(e+a\right)&=e+\left(-1\right)^{m-1}a^{m}\\&=e.\end{aligned}
$$

Hence $b$ is the inverse of $e+a$, i.e. $e+a$ is invertible. $\blacksquare$

### Problem 3

(Problem 2.1-15) (Hua Loo-Keng) Let $R$ be a ring with identity, $e$ its identity element, and $a\in R$. If an element $c$ satisfies $ca=e$ ($ac=e$), then $c$ is called a right inverse (left inverse) of $a$. If $c$ is both a left and a right inverse of $a$, then $c$ is called the inverse of $a$, and $a$ is called invertible. Prove that for any $a,b\in R$, $e-ab$ is invertible if and only if $e-ba$ is invertible.

### Solution to Problem 3

First suppose $e-ab$ is invertible, and write its inverse as $c=\left(e-ab\right)^{-1}$. Construct
$$
d=e+bca.
$$

Verify that $d$ is the inverse of $e-ba$:
$$
\begin{aligned}\left(e-ba\right)d&=\left(e-ba\right)\left(e+bca\right)\\&=e-ba+bca-babca\\&=e-ba+b\left(e-ab\right)ca\\&=e-ba+ba\\&=e,\end{aligned}
$$
where we used $\left(e-ab\right)c=e$. Similarly,
$$
\begin{aligned}d\left(e-ba\right)&=\left(e+bca\right)\left(e-ba\right)\\&=e-ba+bca-bcaba\\&=e-ba+bc\left(e-ab\right)a\\&=e-ba+ba\\&=e,\end{aligned}
$$
where we used $c\left(e-ab\right)=e$. Hence $d=e+bca$ is the inverse of $e-ba$, so $e-ba$ is invertible.

Conversely, if $e-ba$ is invertible, interchanging $a$ and $b$ in the above argument shows that $e-ab$ is invertible.

Therefore $e-ab$ is invertible if and only if $e-ba$ is invertible. $\blacksquare$

### Problem 4

(Problem 2.1-16) (Hua Loo-Keng) Let $R$ be a ring with identity, $e$ its identity element, and $a,b\in R$. Prove that if both $ab$ and $ab-e$ are invertible, then $a-b^{-1}$ is invertible, and $\left(a-b^{-1}\right)^{-1}-a^{-1}$ is also invertible, with
$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

### Solution to Problem 4

Since $b$ is invertible,
$$
a-b^{-1}=\left(ab-e\right)b^{-1}.
$$

By assumption $ab-e$ is invertible, and $b^{-1}$ is invertible; by **Basic Knowledge** (Properties of Invertible Elements in a Ring with Identity), the product of invertible elements is invertible, so $a-b^{-1}$ is invertible, and
$$
\left(a-b^{-1}\right)^{-1}=b\left(ab-e\right)^{-1}.
$$

Set $X=ab-e$, so that $X^{-1}$ exists. We want to prove that
$$
\left(a-b^{-1}\right)^{-1}-a^{-1}=bX^{-1}-a^{-1}
$$
is invertible, with inverse $aba-a=a\left(ba-e\right)$.

Compute the product:
$$
\begin{aligned}\left(bX^{-1}-a^{-1}\right)\cdot a\left(ba-e\right)&=bX^{-1}a\left(ba-e\right)-a^{-1}a\left(ba-e\right)\\&=\left[bX^{-1}a-e\right]\left(ba-e\right).\end{aligned}
$$

By the Hua identity in Problem 3,
$$
\left(e-ba\right)^{-1}=e+b\left(e-ab\right)^{-1}a.
$$

Note that $X=ab-e=-\left(e-ab\right)$, so $X^{-1}=-\left(e-ab\right)^{-1}$, and hence
$$
\begin{aligned}bX^{-1}a&=-b\left(e-ab\right)^{-1}a\\&=-\left[\left(e-ba\right)^{-1}-e\right]\\&=e-\left(e-ba\right)^{-1}.\end{aligned}
$$

Therefore,
$$
bX^{-1}a-e=-\left(e-ba\right)^{-1}.
$$

Also $ba-e=-\left(e-ba\right)$, so
$$
\begin{aligned}\left[bX^{-1}a-e\right]\left(ba-e\right)&=\left(-\left(e-ba\right)^{-1}\right)\cdot\left(-\left(e-ba\right)\right)\\&=\left(e-ba\right)^{-1}\left(e-ba\right)\\&=e.\end{aligned}
$$

Symmetrically, the product in the other direction is also $e$. Hence $a\left(ba-e\right)=aba-a$ is the inverse of
$$
bX^{-1}-a^{-1}=\left(a-b^{-1}\right)^{-1}-a^{-1},
$$
i.e.
$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$
$\blacksquare$
