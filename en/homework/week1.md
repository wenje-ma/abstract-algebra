# Assignment 1

> **Definition 1.1.4** (Semigroup and Monoid) Let $S$ be a nonempty set on which a binary operation $*$ satisfying the associative law is defined; then $\left[S;*\right]$ is called a semigroup. If there exists an identity element $e$ in the semigroup, i.e. $a\in S$ for any $ea=ae=a$, then the semigroup is called a monoid; if the operation also satisfies the commutative law, it is called a commutative monoid.

> **Definition 1.1.10** (Inverse Element) Let $S$ be a monoid, $e$ its identity element, and $a\in S$. If there exists $b\in S$ such that $ba=e$ ($ab=e$), then $b$ is called a left (right) inverse of $a$; if $ba=ab=e$, then $b$ is called an inverse of $a$, and in this case $a$ is called an invertible element.

> **Definition 1.1.14** (Group and Abelian Group) If every element of a monoid $G$ is invertible, then $G$ is called a group. If the operation in the group also satisfies the commutative law, then $G$ is called a commutative group, or an abelian group.

> **Lemma 1.1.17** (Cancellation Law) The operation of a group $G$ satisfies the left (right) cancellation law, i.e. for any $a,b,c\in G$, $ab=ac$ ($ba=ca$) implies $b=c$.

> **Example 1.1.7** (Transformation Monoid) Let $X$ be a nonempty set and $M\left(X\right)$ the set of all transformations on $X$. Then $M\left(X\right)$ forms a monoid under composition of transformations, with the identity transformation of $X$ as its identity element.

> **Basic Knowledge** (Symmetric Difference) For any $A,B\in\mathcal P\left(X\right)$, the symmetric difference is defined as
> $$
> A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right).
> $$

> **Basic Knowledge** (Dirichlet Convolution) For $f,g\in S$, the Dirichlet convolution is defined as
>
> $$
> \begin{aligned}\left(f*g\right)\left(n\right)&=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)\\&=\sum_{ab=n}f\left(a\right)g\left(b\right).\end{aligned}
> $$
>

### Problem 1

(Problem 1.1-8) Give an example of an infinite commutative semigroup that has an identity element and satisfies the cancellation law, but is not a group.

### Solution to Problem 1

Take $S=\mathbb N$ (the set of nonnegative integers) with the usual addition $+$.

First, addition is associative and commutative, so by **Definition 1.1.4** (Semigroup and Monoid), $\left(\mathbb N,+\right)$ is a commutative semigroup.

Second, $0\in\mathbb N$, and for any $a\in\mathbb N$ we have $a+0=0+a=a$, so $0$ is an identity element; hence $\left(\mathbb N,+\right)$ is a commutative monoid.

Third, for any $a,b,c\in\mathbb N$, $a+c=b+c$ implies, by transposition within $\mathbb N$, that $a=b$; hence $\left(\mathbb N,+\right)$ satisfies the left (right) cancellation law.

Finally, the element $1\in\mathbb N$ has no additive inverse, i.e. there is no $b\in\mathbb N$ with $1+b=0$, so not every element is invertible. By **Definition 1.1.14** (Group and Abelian Group), $\left(\mathbb N,+\right)$ is not a group.

In summary, $\left(\mathbb N,+\right)$ is an infinite commutative semigroup with an identity element that satisfies the cancellation law, but is not a group. $\blacksquare$

### Problem 2

(Problem 1.1-9) Let $\mathcal P\left(X\right)$ be the power set of a nonempty set $X$. For any $A,B\in\mathcal P\left(X\right)$, the symmetric difference of $A$ and $B$ is defined as

$$
A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right).
$$

Prove that $\left(\mathcal P\left(X\right),\triangle\right)$ is a group. When $X$ has exactly two elements, give the group table of this group; in this case the group is called the Klein group.

### Solution to Problem 2

For any $A\in\mathcal P\left(X\right)$, characterize $\chi_A:X\to\left\{0,1\right\}$ by its indicator function $A$. Since $A\triangle B$ consists precisely of those elements belonging to exactly one of $A,B$, we have

$$
\chi_{A\triangle B}=\chi_A+\chi_B\pmod 2.
$$

We now verify the four group axioms one by one.

**Closure** For any $A,B\in\mathcal P\left(X\right)$, clearly $A\triangle B\in\mathcal P\left(X\right)$, so $\triangle$ is a binary operation on $\mathcal P\left(X\right)$.

**Associativity** By the associativity of addition modulo $2$,

$$
\begin{aligned}\chi_{\left(A\triangle B\right)\triangle C}&=\left(\chi_A+\chi_B\right)+\chi_C\\&=\chi_A+\left(\chi_B+\chi_C\right)\\&=\chi_{A\triangle\left(B\triangle C\right)},\end{aligned}
$$

hence

$$
\left(A\triangle B\right)\triangle C=A\triangle\left(B\triangle C\right).
$$

**Identity** For any $A\in\mathcal P\left(X\right)$, we have $A\triangle\varnothing=\varnothing\triangle A=A$, so $\varnothing$ is the identity element.

**Inverse** For any $A\in\mathcal P\left(X\right)$, we have $A\triangle A=\varnothing$, so the inverse of every element is itself.

By **Definition 1.1.14** (Group and Abelian Group), $\left(\mathcal P\left(X\right),\triangle\right)$ is a group.

When $X=\left\{1,2\right\}$,

$$
\mathcal P\left(X\right)=\left\{\varnothing,\left\{1\right\},\left\{2\right\},\left\{1,2\right\}\right\}.
$$

Write $0=\varnothing$, $a=\left\{1\right\}$, $b=\left\{2\right\}$, $c=\left\{1,2\right\}$. Each element is its own inverse, and the group table of this group is

$$
\begin{array}{c|cccc}
\triangle & 0 & a & b & c\\hline
0 & 0 & a & b & c\\
a & a & 0 & c & b\\
b & b & c & 0 & a\\
c & c & b & a & 0
\end{array}
$$

This is the Klein four-group. $\blacksquare$

### Problem 3

(Problem 1.1-16) Let $A\in\mathbb R^{n\times n}$ and $B\in\mathbb R^n$. Define a transformation $\mathbb R^n$ on $T\left(A,B\right)$ by

$$
T\left(A,B\right)\left(\alpha\right)=A\alpha+B,\forall\alpha\in\mathbb R^n.
$$

(1) Prove that when $\left|A\right|\ne0$, $T\left(A,B\right)$ is a bijection;

(2) Prove that

$$
\mathrm{Aff}\left(n,\mathbb R\right)=\left\{T\left(A,B\right)\mid\left|A\right|\ne0\right\}
$$

forms a group under composition of maps, called the affine transformation group of $\mathbb R^n$.

### Solution to Problem 3

(1) Suppose $\left|A\right|\ne0$. Then $A$ is invertible.

**Injectivity** If

$$
T\left(A,B\right)\left(\alpha_1\right)=T\left(A,B\right)\left(\alpha_2\right),
$$

then

$$
A\alpha_1+B=A\alpha_2+B,
$$

i.e. $A\left(\alpha_1-\alpha_2\right)=0$. Since $A$ is invertible, multiplying on the left by $A^{-1}$ gives $\alpha_1-\alpha_2=0$, hence $\alpha_1=\alpha_2$.

**Surjectivity** For any $\beta\in\mathbb R^n$, take $\alpha=A^{-1}\left(\beta-B\right)$. Then

$$
\begin{aligned}T\left(A,B\right)\left(\alpha\right)&=A\left(A^{-1}\left(\beta-B\right)\right)+B\\&=\beta.\end{aligned}
$$

Hence $T\left(A,B\right)$ is a bijection.

(2) We verify axioms for $\mathrm{Aff}\left(n,\mathbb R\right)$ under composition one by one.

**Closure** For

$$
T\left(A,B\right),T\left(C,D\right)\in\mathrm{Aff}\left(n,\mathbb R\right),
$$

and any $\alpha\in\mathbb R^n$,

$$
\begin{aligned}T\left(A,B\right)\circ T\left(C,D\right)\left(\alpha\right)&=A\left(C\alpha+D\right)+B\\&=\left(AC\right)\alpha+\left(AD+B\right)\\&=T\left(AC,AD+B\right)\left(\alpha\right).\end{aligned}
$$

Moreover, $\left|AC\right|=\left|A\right|\left|C\right|\ne0$, so

$$
T\left(AC,AD+B\right)\in\mathrm{Aff}\left(n,\mathbb R\right),
$$

i.e. the operation is closed.

**Associativity** Composition of maps is associative.

**Identity** $T\left(I,0\right)$ is the identity transformation, and $\left|I\right|=1\ne0$, so $T\left(I,0\right)\in\mathrm{Aff}\left(n,\mathbb R\right)$. Moreover, for any $T\left(A,B\right)$,

$$
\begin{aligned}T\left(A,B\right)\circ T\left(I,0\right)&=T\left(AI,A\cdot0+B\right)\\&=T\left(A,B\right).\end{aligned}
$$

**Inverse** For $T\left(A,B\right)\in\mathrm{Aff}\left(n,\mathbb R\right)$, since $\left|A^{-1}\right|\ne0$, we have

$$
T\left(A^{-1},-A^{-1}B\right)\in\mathrm{Aff}\left(n,\mathbb R\right),
$$

and

$$
\begin{aligned}T\left(A^{-1},-A^{-1}B\right)\circ T\left(A,B\right)&=T\left(A^{-1}A,A^{-1}B-A^{-1}B\right)\\&=T\left(I,0\right),\end{aligned}
$$

so $T\left(A^{-1},-A^{-1}B\right)$ is the inverse of $T\left(A,B\right)$.

In summary, by **Definition 1.1.14** (Group and Abelian Group), $\mathrm{Aff}\left(n,\mathbb R\right)$ forms a group under composition of maps. $\blacksquare$

### Problem 4

(Problem 1.1-20) Let $S$ be the set of all number-theoretic functions (i.e. maps $\mathbb N\to\mathbb C$). For $f,g\in S$, the Dirichlet convolution is defined by

$$
\begin{aligned}\left(f*g\right)\left(n\right)&=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)\\&=\sum_{ab=n}f\left(a\right)g\left(b\right).\end{aligned}
$$

(1) Prove that $\left(S,*\right)$ is a commutative monoid;

(2) Prove that $f$ is invertible if and only if $f\left(1\right)\ne0$;

(3) Call $f$ multiplicative if $\left(m,n\right)=1$ implies $f\left(mn\right)=f\left(m\right)f\left(n\right)$. Prove that the set of all nonzero multiplicative functions forms an abelian group under the operation $*$;

(4) Call $f$ completely multiplicative if $m,n\in\mathbb N^+$ for any $f\left(mn\right)=f\left(m\right)f\left(n\right)$. Does the set of all nonzero completely multiplicative functions form an abelian group under the operation $*$?

### Solution to Problem 4

(1) We verify axioms for $\left(S,*\right)$ as a commutative monoid one by one.

**Closure** For any $f,g\in S$, by definition $f*g$ is a map $\mathbb N\to\mathbb C$, so $f*g\in S$.

**Commutativity** From

$$
\left(f*g\right)\left(n\right)=\sum_{ab=n}f\left(a\right)g\left(b\right)
$$

interchanging the roles of $a,b$ gives

$$
\begin{aligned}\left(f*g\right)\left(n\right)&=\sum_{ba=n}g\left(b\right)f\left(a\right)\\&=\left(g*f\right)\left(n\right),\end{aligned}
$$

so $f*g=g*f$.

**Associativity** For any $n$,

$$
\begin{aligned}\left(\left(f*g\right)*h\right)\left(n\right)&=\sum_{ab=n}\left(f*g\right)\left(a\right)h\left(b\right)\\&=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right),\end{aligned}
$$

and

$$
\begin{aligned}\left(f*\left(g*h\right)\right)\left(n\right)&=\sum_{ab=n}f\left(a\right)\left(g*h\right)\left(b\right)\\&=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right),\end{aligned}
$$

both equal the triple sum $\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right)$, so $\left(f*g\right)*h=f*\left(g*h\right)$.

**Identity** Define $e\in S$ by $e\left(1\right)=1$ and $n>1$ for $e\left(n\right)=0$. Then

$$
\begin{aligned}\left(e*f\right)\left(n\right)&=\sum_{d\mid n}e\left(d\right)f\left(\frac{n}{d}\right)\\&=e\left(1\right)f\left(n\right)\\&=f\left(n\right),\end{aligned}
$$

and similarly $f*e=f$. Hence $e$ is the identity element.

By **Definition 1.1.4** (Semigroup and Monoid), $\left(S,*\right)$ is a commutative monoid.

(2) **Necessity** If $f$ is invertible, there exists $g\in S$ such that $f*g=e$. Then

$$
\begin{aligned}\left(f*g\right)\left(1\right)&=f\left(1\right)g\left(1\right)\\&=e\left(1\right)\\&=1,\end{aligned}
$$

so $f\left(1\right)g\left(1\right)=1$; in particular $f\left(1\right)\ne0$.

**Sufficiency** Suppose $f\left(1\right)\ne0$. Construct $g\in S$ inductively: set $g\left(1\right)=f\left(1\right)^{-1}$. For $n>1$, require $\left(f*g\right)\left(n\right)=0$, i.e.

$$
f\left(1\right)g\left(n\right)+\sum_{\substack{d\mid n\\d>1}}f\left(d\right)g\left(\frac{n}{d}\right)=0,
$$

which gives

$$
g\left(n\right)=-f\left(1\right)^{-1}\sum_{\substack{d\mid n\\d>1}}f\left(d\right)g\left(\frac{n}{d}\right).
$$

The right-hand side only involves $n/d<n$ already defined at the smaller subscripts $g$, so $g\in S$ can be defined recursively with $f*g=e$. By **Definition 1.1.10** (Inverse Element), $f$ is invertible.

(3) Let $F$ denote the set of all nonzero multiplicative functions.

First we show that a nonzero multiplicative function satisfies $f\left(1\right)=1$. Since $f\ne0$, there exists $m\in\mathbb N^+$ with $f\left(m\right)\ne0$. Also $\left(1,1\right)=1$, so multiplicativity gives $f\left(1\right)=f\left(1\cdot1\right)=f\left(1\right)^2$, hence $f\left(1\right)=0$ or $1$. If $f\left(1\right)=0$, then

$$
\begin{aligned}f\left(m\right)&=f\left(1\cdot m\right)\\&=f\left(1\right)f\left(m\right)\\&=0,\end{aligned}
$$

a contradiction. Hence $f\left(1\right)=1\ne0$.

**Closure** Let $f,g$ be multiplicative. For $\left(m,n\right)=1$, any $d\mid mn$ can be uniquely decomposed as $d=d_1d_2$ with $d_1\mid m$, $d_2\mid n$, in which case $\left(d_1,d_2\right)=1$ and $\left(m/d_1,n/d_2\right)=1$. Then

$$
\begin{aligned}\left(f*g\right)\left(mn\right)&=\sum_{d_1\mid m}\sum_{d_2\mid n}f\left(d_1\right)f\left(d_2\right)g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right)\\&=\left(f*g\right)\left(m\right)\left(f*g\right)\left(n\right),\end{aligned}
$$

so $f*g$ is multiplicative. Also,

$$
\left(f*g\right)\left(1\right)=f\left(1\right)g\left(1\right)=1\ne0,
$$

so $f*g\in F$.

**Identity** $e$ is a multiplicative function and $e\left(1\right)=1\ne0$, so $e\in F$.

**Inverse** By (2), $f\in F$ is invertible; write $f*g=e$. From the recursive construction in (3) and the multiplicativity of $f$, one can show that $g$ is also multiplicative; and $g\left(1\right)=f\left(1\right)^{-1}=1\ne0$, so $g\in F$.

**Commutativity** By (1), convolution is commutative.

In summary, by **Definition 1.1.14** (Group and Abelian Group), $F$ forms an abelian group under $*$.

(4) It does not. In fact, the set of nonzero completely multiplicative functions is not closed under convolution. Take $f\left(n\right)=1$ (the constant function). For any $m,n\in\mathbb N^+$, $f\left(mn\right)=1=f\left(m\right)f\left(n\right)$, so $f$ is completely multiplicative. But

$$
\begin{aligned}\left(f*f\right)\left(n\right)&=\sum_{d\mid n}1\\&=\tau\left(n\right),\end{aligned}
$$

where $\tau\left(n\right)$ is the number of positive divisors of $n$. Take $n=4$; then $\tau\left(4\right)=3$, while $\tau\left(2\right)\tau\left(2\right)=4$, so $\tau\left(4\right)\ne\tau\left(2\right)\tau\left(2\right)$.

Thus $f*f$ is not completely multiplicative, i.e. $f*f$ does not belong to the set of nonzero completely multiplicative functions. Therefore this set is not closed under convolution, and does not form a group, let alone an abelian group. $\blacksquare$
