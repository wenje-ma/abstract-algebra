# week1

> **Basic Knowledge: Basic Properties of Addition on Nonnegative Integers**<br>$\mathbb N=\left\{0,1,2,\cdots\right\}$ is closed under the usual addition, which is associative and commutative; $0\in\mathbb N$ is the additive identity, i.e. $0+a=a+0=a$ for every $a\in\mathbb N$; addition satisfies the cancellation law, i.e. $a+c=b+c$ implies $a=b$; and $1+a\ge1>0$ for every $a\in\mathbb N$, so no $b\in\mathbb N$ satisfies $1+b=0$.

> **Basic Knowledge: Power Set, Indicator Functions and Symmetric Difference**<br>Let $X$ be a nonempty set and $P\left(X\right)$ the set of all subsets of $X$ (the power set). For $A\subseteq X$, the indicator function $\chi_A:X\to\left\{0,1\right\}$ is defined by $\chi_A\left(x\right)=1$ if and only if $x\in A$; the map $A\mapsto\chi_A$ is injective. The symmetric difference is defined by $A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right)$, and $\chi_{A\triangle B}=\chi_A+\chi_B\pmod2$.

> **Basic Knowledge: Addition Modulo 2**<br>Addition modulo 2 on $\left\{0,1\right\}$ is associative and commutative, $0$ is its identity, and every element is self-inverse, i.e. $x+x=0\pmod2$ for every $x\in\left\{0,1\right\}$.

> **Basic Knowledge: Invertibility of Square Matrices and Determinants**<br>For $A\in\mathbb R^{n\times n}$, $A$ is invertible if and only if $\left|A\right|\ne0$; the determinant is multiplicative, i.e. $\left|AC\right|=\left|A\right|\left|C\right|$; if $A$ is invertible, then $A^{-1}$ is also invertible and $\left|A^{-1}\right|\ne0$.

> **Basic Knowledge: Associativity of Matrix Multiplication**<br>Matrix multiplication is associative, i.e. $\left(AB\right)C=A\left(BC\right)$ for all $A,B,C\in\mathbb R^{n\times n}$.

> **Basic Knowledge: Number-Theoretic Functions and Dirichlet Convolution**<br>A number-theoretic function is a map $\mathbb N^*\to\mathbb C$. For $f,g\in S$, the Dirichlet convolution is defined by $\left(f*g\right)\left(n\right)=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)=\sum_{ab=n}f\left(a\right)g\left(b\right)$; define $e\in S$ by $e\left(1\right)=1$ and $e\left(n\right)=0$ for $n>1$. Finite sums may be rearranged, i.e. $\sum_{d\mid n}\sum_{e\mid\frac{n}{d}}f\left(d\right)g\left(e\right)h\left(\frac{n}{de}\right)=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right)$.

> **Basic Knowledge: Unique Decomposition of Coprime Factors**<br>If $\left(m,n\right)=1$, then $d\mid mn$ decomposes uniquely as $d=d_1d_2$, where $d_1\mid m$, $d_2\mid n$, and in this case $\left(d_1,d_2\right)=1$ and $\left(\frac{m}{d_1},\frac{n}{d_2}\right)=1$.

> **Basic Knowledge: Multiplicative and Completely Multiplicative Functions**<br>A number-theoretic function $f$ is called multiplicative if $f\left(mn\right)=f\left(m\right)f\left(n\right)$ whenever $\left(m,n\right)=1$; $f$ is called completely multiplicative if $f\left(mn\right)=f\left(m\right)f\left(n\right)$ for all $m,n\in\mathbb N^*$.

> **Basic Knowledge: The Divisor Counting Function**<br>Let $\tau\left(n\right)=\sum_{d\mid n}1$ be the number of positive divisors of $n$; in particular, $\tau\left(2\right)=2$ and $\tau\left(4\right)=3$.

> **Definition 1.1.4 (Semigroup and Monoid)**<br>If a binary operation $*$ satisfying the associative law is defined on a nonempty set $S$, then $\left\{S;*\right\}$ is called a semigroup, and $a*b$ is abbreviated as $ab$. If there exists an element $e$ in the semigroup $S$ such that $ea=a$ (or $ae=a$) for every $a\in S$, then $e$ is called a left (right) identity of $S$; if $e$ is both a left and a right identity, then $e$ is called the identity of $S$, and a semigroup with an identity is called a monoid; if the operation in $S$ also satisfies the commutative law, then $S$ is called a commutative monoid.

> **Example 1.1.7 (Transformation Monoid)**<br>Let $M\left(X\right)$ be the set of all transformations of a nonempty set $X$. Then $M\left(X\right)$ forms a monoid under the multiplication of transformations (i.e. composition), whose identity is the identity transformation $\mathrm{id}_X$ of $X$.

> **Definition 1.1.10 (Inverse Element)**<br>Let $S$ be a monoid, $e$ its identity, and $a\in S$. If there exists $b\in S$ such that $ba=e$ ($ab=e$), then $b$ is called a left (right) inverse of $a$. If $b$ is both a left and a right inverse of $a$, i.e. $ba=ab=e$, then $b$ is called an inverse of $a$, and in this case $a$ is called an invertible element.

> **Definition 1.1.14 (Group and Abelian Group)**<br>If every element of a monoid $G$ is invertible, then $G$ is called a group. If the operation in the group also satisfies the commutative law, then $G$ is called a commutative group, or an abelian group.

---

## 1.1-8

Give an example of an infinite commutative semigroup that has an identity element and satisfies the cancellation law, but is not a group.

### Solution 1.1-8

Take $S=\mathbb N$ (the set of all nonnegative integers) with the usual operation of addition $+$.

**Step 1: verify that $\left(\mathbb N,+\right)$ is a commutative semigroup.** By **Basic Knowledge: Basic Properties of Addition on Nonnegative Integers**, $\mathbb N$ is closed under addition, and addition is associative and commutative. Thus a binary operation $+$ satisfying the associative and commutative laws is defined on $\mathbb N$, and by **Definition 1.1.4 (Semigroup and Monoid)**, $\left(\mathbb N,+\right)$ is a commutative semigroup.

**Step 2: verify that $\left(\mathbb N,+\right)$ is a commutative monoid.** By **Basic Knowledge: Basic Properties of Addition on Nonnegative Integers**, $0\in\mathbb N$ and $0+a=a+0=a$ for every $a\in\mathbb N$. Hence $0$ is the identity of $\left(\mathbb N,+\right)$, and by **Definition 1.1.4 (Semigroup and Monoid)**, a semigroup with an identity is a monoid, so $\left(\mathbb N,+\right)$ is a commutative monoid.

**Step 3: verify the cancellation law.** For any $a,b,c\in\mathbb N$, if $a+c=b+c$, then by **Basic Knowledge: Basic Properties of Addition on Nonnegative Integers** (the cancellation law for addition), $a=b$. Hence $\left(\mathbb N,+\right)$ satisfies the left (right) cancellation law.

**Step 4: verify that $\left(\mathbb N,+\right)$ is not a group.** By **Basic Knowledge: Basic Properties of Addition on Nonnegative Integers**, $1+b\ge1>0$ for every $b\in\mathbb N$, so no $b\in\mathbb N$ satisfies $1+b=0$. Therefore $1\in\mathbb N$ has no additive inverse, i.e. not every element is invertible. By **Definition 1.1.10 (Inverse Element)** and **Definition 1.1.14 (Group and Abelian Group)**, a group requires every element to be invertible, so $\left(\mathbb N,+\right)$ is not a group.

In summary, $\left(\mathbb N,+\right)$ is an infinite commutative semigroup with an identity element that satisfies the cancellation law, but is not a group. $\blacksquare$

---

## 1.1-9

Let $P\left(X\right)$ be the power set of a nonempty set $X$. For any $A,B\in P\left(X\right)$, the symmetric difference of $A$ and $B$ is defined by

$$
A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right).
$$

Here $A\setminus B=\left\{x\in A\mid x\notin B\right\}$. Prove that $\left(P\left(X\right),\triangle\right)$ is a group. When $X$ has exactly two elements, give the group table of this group; in this case the group is called the Klein group.

### Solution 1.1-9

For any $A\in P\left(X\right)$, describe $A$ by its indicator function $\chi_A:X\to\left\{0,1\right\}$. By **Basic Knowledge: Power Set, Indicator Functions and Symmetric Difference**, $A\mapsto\chi_A$ is injective and $\chi_{A\triangle B}=\chi_A+\chi_B\pmod2$.

**Step 1: closure.** For any $A,B\in P\left(X\right)$, by **Basic Knowledge: Power Set, Indicator Functions and Symmetric Difference**, $A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right)\subseteq X$, so $A\triangle B\in P\left(X\right)$. Hence $\triangle$ is a binary operation on $P\left(X\right)$.

**Step 2: associativity.** For any $A,B,C\in P\left(X\right)$, by **Basic Knowledge: Power Set, Indicator Functions and Symmetric Difference**, $\chi_{\left(A\triangle B\right)\triangle C}=\left(\chi_A+\chi_B\right)+\chi_C\pmod2$ and $\chi_{A\triangle\left(B\triangle C\right)}=\chi_A+\left(\chi_B+\chi_C\right)\pmod2$. By **Basic Knowledge: Addition Modulo 2** (associativity), $\left(\chi_A+\chi_B\right)+\chi_C=\chi_A+\left(\chi_B+\chi_C\right)\pmod2$. Hence $\chi_{\left(A\triangle B\right)\triangle C}=\chi_{A\triangle\left(B\triangle C\right)}$. Since $A\mapsto\chi_A$ is injective (**Basic Knowledge: Power Set, Indicator Functions and Symmetric Difference**), $\left(A\triangle B\right)\triangle C=A\triangle\left(B\triangle C\right)$. By **Definition 1.1.4 (Semigroup and Monoid)**, $\left(P\left(X\right),\triangle\right)$ is a semigroup.

**Step 3: identity.** For any $A\in P\left(X\right)$, by the definition of symmetric difference (**Basic Knowledge: Power Set, Indicator Functions and Symmetric Difference**), $A\triangle\varnothing=\left(A\setminus\varnothing\right)\cup\left(\varnothing\setminus A\right)=A$. Hence $\varnothing$ is the identity, and by **Definition 1.1.4 (Semigroup and Monoid)**, $\left(P\left(X\right),\triangle\right)$ is a monoid.

**Step 4: inverse.** For any $A\in P\left(X\right)$, by the definition of symmetric difference, $A\triangle A=\left(A\setminus A\right)\cup\left(A\setminus A\right)=\varnothing$. Hence $A\triangle A=\varnothing$, i.e. $A$ has itself as an inverse, and by **Definition 1.1.10 (Inverse Element)**, every element $A\in P\left(X\right)$ is invertible (with inverse equal to itself).

**Step 5: the group property.** By Steps 2 through 4, $\left(P\left(X\right),\triangle\right)$ is a monoid in which every element is invertible, and by **Definition 1.1.14 (Group and Abelian Group)**, $\left(P\left(X\right),\triangle\right)$ is a group.

When $X=\left\{1,2\right\}$, $P\left(X\right)=\left\{\varnothing,\left\{1\right\},\left\{2\right\},\left\{1,2\right\}\right\}$. Write $0=\varnothing$, $a=\left\{1\right\}$, $b=\left\{2\right\}$, $c=\left\{1,2\right\}$. By Step 4, every element has itself as its inverse. By the definition of symmetric difference (**Basic Knowledge: Power Set, Indicator Functions and Symmetric Difference**), computing term by term gives $a\triangle b=\left\{1,2\right\}=c$, $a\triangle c=\left\{2\right\}=b$, $b\triangle c=\left\{1\right\}=a$, whence the group table

$$
\begin{array}{c|cccc}
\triangle & 0 & a & b & c\\\hline
0 & 0 & a & b & c\\
a & a & 0 & c & b\\
b & b & c & 0 & a\\
c & c & b & a & 0
\end{array}
$$

This is the Klein four-group. $\blacksquare$

---

## 1.1-16

Let $A\in\mathbb R^{n\times n}$ and $\beta\in\mathbb R^n$. Define the transformation $T_{\left(A,\beta\right)}$ on $\mathbb R^n$ by

$$
T_{\left(A,\beta\right)}\left(\alpha\right)=A\alpha+\beta,\quad\forall\alpha\in\mathbb R^n.
$$

(1) Prove that $T_{\left(A,\beta\right)}$ is a bijection when $\left|A\right|\ne0$;

(2) Prove that $\mathrm{Aff}\left(n,\mathbb R\right)=\left\{T_{\left(A,\beta\right)}\mid\left|A\right|\ne0\right\}$ forms a group under composition of maps, called the affine transformation group of $\mathbb R^n$.

### Solution 1.1-16

**(1) Prove that $T_{\left(A,\beta\right)}$ is a bijection.** Suppose $\left|A\right|\ne0$. By **Basic Knowledge: Invertibility of Square Matrices and Determinants**, $A$ is invertible.

**Injectivity**: If $T_{\left(A,\beta\right)}\left(\alpha_1\right)=T_{\left(A,\beta\right)}\left(\alpha_2\right)$, then $A\alpha_1+\beta=A\alpha_2+\beta$, hence $A\left(\alpha_1-\alpha_2\right)=0$. Since $A$ is invertible, multiplying on the left by $A^{-1}$ gives $\alpha_1-\alpha_2=0$, i.e. $\alpha_1=\alpha_2$. Hence $T_{\left(A,\beta\right)}$ is injective.

**Surjectivity**: For any $\gamma\in\mathbb R^n$, take $\alpha=A^{-1}\left(\gamma-\beta\right)$; then by the associativity of matrix multiplication and the definition of the inverse matrix (**Basic Knowledge: Associativity of Matrix Multiplication**, **Basic Knowledge: Invertibility of Square Matrices and Determinants**), $T_{\left(A,\beta\right)}\left(\alpha\right)=A\left(A^{-1}\left(\gamma-\beta\right)\right)+\beta=\left(\gamma-\beta\right)+\beta=\gamma$. Hence $T_{\left(A,\beta\right)}$ is surjective.

In summary, $T_{\left(A,\beta\right)}$ is a bijection.

**(2) Prove that $\mathrm{Aff}\left(n,\mathbb R\right)$ is a group.** By **Example 1.1.7 (Transformation Monoid)**, $M\left(\mathbb R^n\right)$ (the set of all transformations) is a monoid under composition, so composition is associative and the identity transformation is the identity. Since each $T_{\left(A,\beta\right)}$ is a transformation of $\mathbb R^n$, $\mathrm{Aff}\left(n,\mathbb R\right)\subseteq M\left(\mathbb R^n\right)$. We now verify one by one that $\mathrm{Aff}\left(n,\mathbb R\right)$ is a group under composition.

**Closure**: For any $T_{\left(A,\beta\right)},T_{\left(C,\delta\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$ and any $\alpha\in\mathbb R^n$, by the associativity and distributivity of matrix multiplication (**Basic Knowledge: Associativity of Matrix Multiplication**),

$$
T_{\left(A,\beta\right)}\circ T_{\left(C,\delta\right)}\left(\alpha\right)=A\left(C\alpha+\delta\right)+\beta=\left(AC\right)\alpha+\left(A\delta+\beta\right)=T_{\left(AC,A\delta+\beta\right)}\left(\alpha\right).
$$

By **Basic Knowledge: Invertibility of Square Matrices and Determinants**, $\left|AC\right|=\left|A\right|\left|C\right|\ne0$, so $T_{\left(AC,A\delta+\beta\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$. Hence composition is closed on $\mathrm{Aff}\left(n,\mathbb R\right)$.

**Associativity**: By **Example 1.1.7 (Transformation Monoid)**, composition is associative.

**Identity**: The identity transformation $T_{\left(I,0\right)}$ satisfies $\left|I\right|=1\ne0$ (**Basic Knowledge: Invertibility of Square Matrices and Determinants**), so $T_{\left(I,0\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$. By **Example 1.1.7 (Transformation Monoid)**, the identity transformation is the identity for composition, so $T_{\left(A,\beta\right)}\circ T_{\left(I,0\right)}=T_{\left(A,\beta\right)}=T_{\left(I,0\right)}\circ T_{\left(A,\beta\right)}$ for every $T_{\left(A,\beta\right)}$.

**Inverse**: For $T_{\left(A,\beta\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$, since $\left|A\right|\ne0$, by **Basic Knowledge: Invertibility of Square Matrices and Determinants**, $A^{-1}$ is invertible and $\left|A^{-1}\right|\ne0$, so $T_{\left(A^{-1},-A^{-1}\beta\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$. For any $\alpha\in\mathbb R^n$, by the associativity and distributivity of matrix multiplication,

$$
T_{\left(A^{-1},-A^{-1}\beta\right)}\circ T_{\left(A,\beta\right)}\left(\alpha\right)=A^{-1}\left(A\alpha+\beta\right)-A^{-1}\beta=\alpha,
$$

and

$$
T_{\left(A,\beta\right)}\circ T_{\left(A^{-1},-A^{-1}\beta\right)}\left(\alpha\right)=A\left(A^{-1}\alpha-A^{-1}\beta\right)+\beta=\alpha,
$$

so $T_{\left(A^{-1},-A^{-1}\beta\right)}\circ T_{\left(A,\beta\right)}=T_{\left(I,0\right)}=T_{\left(A,\beta\right)}\circ T_{\left(A^{-1},-A^{-1}\beta\right)}$. By **Definition 1.1.10 (Inverse Element)**, $T_{\left(A^{-1},-A^{-1}\beta\right)}$ is the inverse of $T_{\left(A,\beta\right)}$.

Since closure, associativity, identity and inverse all hold, by **Definition 1.1.14 (Group and Abelian Group)**, $\mathrm{Aff}\left(n,\mathbb R\right)$ forms a group under composition of maps. $\blacksquare$

---

## 1.1-20

Let $S$ be the set of all number-theoretic functions (i.e. maps $\mathbb N^*\to\mathbb C$). For $f,g\in S$, define the Dirichlet convolution by

$$
f*g\left(n\right)=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)=\sum_{ab=n}f\left(a\right)g\left(b\right).
$$

(1) Prove that $\left(S,*\right)$ is a commutative monoid;

(2) Prove that $f$ is invertible if and only if $f\left(1\right)\ne0$;

(3) Call $f$ multiplicative if $f\left(mn\right)=f\left(m\right)f\left(n\right)$ whenever $\left(m,n\right)=1$; prove that the set of all nonzero multiplicative functions forms an abelian group under the operation $*$;

(4) Call $f$ completely multiplicative if $f\left(mn\right)=f\left(m\right)f\left(n\right)$ for all $m,n\in\mathbb N^*$; does the set of all nonzero completely multiplicative functions form an abelian group under the operation $*$?

### Solution 1.1-20

**(1) Prove that $\left(S,*\right)$ is a commutative monoid.** By **Definition 1.1.4 (Semigroup and Monoid)**, we verify the axioms one by one.

**Closure**: For any $f,g\in S$, by **Basic Knowledge: Number-Theoretic Functions and Dirichlet Convolution**, $\left(f*g\right)\left(n\right)=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)$ is the sum of finitely many complex numbers for each $n\in\mathbb N^*$, hence lies in $\mathbb C$, i.e. $f*g$ is a map $\mathbb N^*\to\mathbb C$, so $f*g\in S$.

**Commutativity**: For any $f,g\in S$ and $n\in\mathbb N^*$, by **Basic Knowledge: Number-Theoretic Functions and Dirichlet Convolution**, $\left(f*g\right)\left(n\right)=\sum_{ab=n}f\left(a\right)g\left(b\right)$. Interchanging the summation indices $a,b$ gives $\sum_{ab=n}f\left(a\right)g\left(b\right)=\sum_{ba=n}g\left(b\right)f\left(a\right)=\left(g*f\right)\left(n\right)$. Hence $f*g=g*f$, i.e. $*$ is commutative.

**Associativity**: For any $f,g,h\in S$ and $n\in\mathbb N^*$, by **Basic Knowledge: Number-Theoretic Functions and Dirichlet Convolution** and the rearrangement of finite sums,

$$
\left(\left(f*g\right)*h\right)\left(n\right)=\sum_{d\mid n}\left(f*g\right)\left(d\right)h\left(\frac{n}{d}\right)=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right),
$$

and

$$
\left(f*\left(g*h\right)\right)\left(n\right)=\sum_{d\mid n}f\left(d\right)\left(g*h\right)\left(\frac{n}{d}\right)=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right).
$$

Both equal the triple sum $\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right)$, so $\left(f*g\right)*h=f*\left(g*h\right)$, i.e. $*$ is associative.

**Identity**: By **Basic Knowledge: Number-Theoretic Functions and Dirichlet Convolution**, $e\left(1\right)=1$ and $e\left(n\right)=0$ for $n>1$, so $e\in S$. For any $f\in S$ and $n\in\mathbb N^*$, $\left(e*f\right)\left(n\right)=\sum_{d\mid n}e\left(d\right)f\left(\frac{n}{d}\right)$. Since $e\left(d\right)=0$ unless $d=1$, $\left(e*f\right)\left(n\right)=e\left(1\right)f\left(n\right)=f\left(n\right)$, i.e. $e*f=f$; similarly $f*e=f$. Hence $e$ is the identity.

Since closure, commutativity, associativity and identity all hold, by **Definition 1.1.4 (Semigroup and Monoid)**, $\left(S,*\right)$ is a commutative monoid.

**(2) Prove that $f$ is invertible if and only if $f\left(1\right)\ne0$.**

**Necessity**: If $f$ is invertible, by **Definition 1.1.10 (Inverse Element)**, there exists $g\in S$ such that $f*g=e$. Then $\left(f*g\right)\left(1\right)=\sum_{d\mid 1}f\left(d\right)g\left(\frac{1}{d}\right)=f\left(1\right)g\left(1\right)$, while $e\left(1\right)=1$, so $f\left(1\right)g\left(1\right)=1$, hence $f\left(1\right)\ne0$.

**Sufficiency**: Suppose $f\left(1\right)\ne0$. By **Basic Knowledge: Number-Theoretic Functions and Dirichlet Convolution**, construct $g\in S$ inductively: set $g\left(1\right)=f\left(1\right)^{-1}$; for $n>1$, require $\left(f*g\right)\left(n\right)=0$, i.e.

$$
f\left(1\right)g\left(n\right)+\sum_{\substack{d\mid n\\d>1}}f\left(d\right)g\left(\frac{n}{d}\right)=0,
$$

which gives

$$
g\left(n\right)=-f\left(1\right)^{-1}\sum_{\substack{d\mid n\\d>1}}f\left(d\right)g\left(\frac{n}{d}\right).
$$

The right-hand side involves only the values $g\left(\frac{n}{d}\right)$ at the smaller subscripts $\frac{n}{d}<n$ (since $d>1$) that have already been defined, so $g\in S$ can be defined recursively, and $\left(f*g\right)\left(1\right)=f\left(1\right)g\left(1\right)=1=e\left(1\right)$, while $\left(f*g\right)\left(n\right)=0=e\left(n\right)$ for $n>1$, i.e. $f*g=e$. By **Definition 1.1.10 (Inverse Element)**, $f$ is invertible.

**(3) Prove that the set $F$ of nonzero multiplicative functions forms an abelian group under $*$.**

First we show that every element of $F$ satisfies $f\left(1\right)=1$. For $f\in F$, since $f\ne0$, there exists $m\in\mathbb N^*$ with $f\left(m\right)\ne0$. Since $\left(1,1\right)=1$, multiplicativity (**Basic Knowledge: Multiplicative and Completely Multiplicative Functions**) gives $f\left(1\right)=f\left(1\cdot1\right)=f\left(1\right)f\left(1\right)$, so $f\left(1\right)=0$ or $1$. If $f\left(1\right)=0$, then $f\left(m\right)=f\left(1\cdot m\right)=f\left(1\right)f\left(m\right)=0$, contradicting $f\left(m\right)\ne0$. Hence $f\left(1\right)=1\ne0$.

**Closure**: For $f,g\in F$ and $\left(m,n\right)=1$, by **Basic Knowledge: Unique Decomposition of Coprime Factors**, $d\mid mn$ decomposes uniquely as $d=d_1d_2$, where $d_1\mid m$, $d_2\mid n$, and $\left(d_1,d_2\right)=1$, $\left(\frac{m}{d_1},\frac{n}{d_2}\right)=1$. By the multiplicativity of $f,g$, $f\left(d_1d_2\right)=f\left(d_1\right)f\left(d_2\right)$ and $g\left(\frac{mn}{d_1d_2}\right)=g\left(\frac{m}{d_1}\frac{n}{d_2}\right)=g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right)$. Hence

$$
\left(f*g\right)\left(mn\right)=\sum_{d_1\mid m}\sum_{d_2\mid n}f\left(d_1\right)f\left(d_2\right)g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right)=\left(f*g\right)\left(m\right)\left(f*g\right)\left(n\right),
$$

so $f*g$ is multiplicative. Also $\left(f*g\right)\left(1\right)=f\left(1\right)g\left(1\right)=1\ne0$, so $f*g\ne0$, hence $f*g\in F$.

**Identity**: By **Basic Knowledge: Number-Theoretic Functions and Dirichlet Convolution**, $e\left(1\right)=1$ and $e\left(n\right)=0$ for $n>1$. For $\left(m,n\right)=1$, if $mn=1$ then $m=n=1$; otherwise $mn>1$, $e\left(mn\right)=0$, while $e\left(m\right)e\left(n\right)=0$ (since at least one of $m,n$ exceeds $1$), so $e$ is multiplicative. Also $e\left(1\right)=1\ne0$, hence $e\in F$.

**Inverse**: For $f\in F$, by (2) and $f\left(1\right)=1\ne0$, $f$ is invertible in $S$; write $f*g=e$. We prove by strong induction that $g$ is multiplicative: for $\left(m,n\right)=1$, assume $g\left(kl\right)=g\left(k\right)g\left(l\right)$ for all $\left(k,l\right)=1$ with $kl<mn$, and prove $g\left(mn\right)=g\left(m\right)g\left(n\right)$. Since $mn>1$, $\left(f*g\right)\left(mn\right)=0$, and by **Basic Knowledge: Unique Decomposition of Coprime Factors** and the multiplicativity of $f$,

$$
0=\left(f*g\right)\left(mn\right)=\sum_{d_1\mid m}\sum_{d_2\mid n}f\left(d_1\right)f\left(d_2\right)g\left(\frac{m}{d_1}\frac{n}{d_2}\right).
$$

In the right-hand sum, when $\left(d_1,d_2\right)=\left(1,1\right)$ we have $\frac{m}{d_1}\frac{n}{d_2}=mn$; for all other terms $\frac{m}{d_1}\frac{n}{d_2}<mn$ and $\left(\frac{m}{d_1},\frac{n}{d_2}\right)=1$, so by the induction hypothesis $g\left(\frac{m}{d_1}\frac{n}{d_2}\right)=g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right)$. On the other hand, multiplying $\left(f*g\right)\left(m\right)=0$ by $\left(f*g\right)\left(n\right)=0$ gives

$$
0=\sum_{d_1\mid m}\sum_{d_2\mid n}f\left(d_1\right)f\left(d_2\right)g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right).
$$

The two right-hand sums agree term by term except for the leading terms, and $f\left(1\right)=1$, so $g\left(mn\right)=g\left(m\right)g\left(n\right)$. Hence $g$ is multiplicative. Also, since $f*g=e$, $\left(f*g\right)\left(1\right)=f\left(1\right)g\left(1\right)=1$, and $f\left(1\right)=1$, so $g\left(1\right)=1\ne0$, hence $g\in F$; that is, $f$ has the inverse $g$ in $F$.

**Commutativity**: By (1), $*$ is commutative.

Since closure, identity, inverse and commutativity all hold, by **Definition 1.1.14 (Group and Abelian Group)**, $F$ forms an abelian group under $*$.

**(4) Conclusion: it does not.** In fact, the set of nonzero completely multiplicative functions is not closed under $*$. Take $f\left(n\right)=1$ (the constant function); for all $m,n\in\mathbb N^*$, $f\left(mn\right)=1=f\left(m\right)f\left(n\right)$, so $f$ is completely multiplicative, and $f\ne0$. By **Basic Knowledge: Number-Theoretic Functions and Dirichlet Convolution**,

$$
\left(f*f\right)\left(n\right)=\sum_{d\mid n}1=\tau\left(n\right),
$$

where $\tau\left(n\right)$ is the number of positive divisors of $n$. Take $n=2$; then by **Basic Knowledge: The Divisor Counting Function**, $\tau\left(2\right)=2$ and $\tau\left(4\right)=3$. Hence $\tau\left(2\cdot2\right)=\tau\left(4\right)=3\ne4=\tau\left(2\right)\tau\left(2\right)$, so $\tau$ is not completely multiplicative. Thus $f*f=\tau$ is not completely multiplicative, i.e. $f*f$ does not belong to the set of nonzero completely multiplicative functions. Hence this set is not closed under $*$, and does not form an abelian group. $\blacksquare$
