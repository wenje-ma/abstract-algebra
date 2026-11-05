# week7

> **Lemma 1.7.7**
> 
> Let $A,B$ be subgroups of $G$ with $G=AB$ and $A\cap{B}=\left\{e\right\}$. Then $A$ and $B$ are both normal subgroups of $G$ if and only if $ab=ba$ for all $a\in{A}$ and $b\in{B}$.

> **Lemma 1.8.8 (Heredity of Solvability)**
> 
> Subgroups and quotient groups of a solvable group are solvable; conversely, if $N\trianglelefteq{G}$ and both $N$ and $G/N$ are solvable, then $G$ is solvable.

> **Theorem 1.10.8 (Sylow's Second Theorem)**
> 
> Let $P$ be a Sylow $p$-subgroup of $G$, and let $H$ be a subgroup of $G$ of order $p^{k}$, $k\le{l}$ (where $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$). Then there exists $g\in{G}$ with $H\subseteq{g}Pg^{-1}$. In particular, the Sylow $p$-subgroups of $G$ are conjugate to one another.

> **Theorem 1.10.10 (Sylow's Third Theorem)**
> 
> Let $n_{p}$ be the number of Sylow $p$-subgroups of $G$. Then (1) a Sylow $p$-subgroup $P$ of $G$ satisfies $P\triangleleft{G}$ if and only if $n_{p}=1$; (2) $n_{p}\mid{m}$ and $n_{p}\equiv1\pmod{p}$, where $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$.

$$
\left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}.
$$

$$
\left(a-b\right)^{n}=\sum_{k=0}^{n}\binom{n}{k}a^{k}\left(-b\right)^{n-k},
$$
and the commutativity of $R$ allows the terms to be collected.

> **Definition 2.1.1 (Ring)**
> 
> Let $R$ be a nonempty set on which two binary operations $+$ and $\cdot$ are defined, satisfying: (1) $\left[R;+\right]$ is an abelian group; (2) $\left[R;\cdot\right]$ is a semigroup; (3) multiplication distributes over addition on both sides: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$. Then $R$ is called a ring.

> **Definition 2.1.8 (Ring Without Zero Divisors)**
> 
> If a ring $R$ is not the zero ring and has no zero divisors, then $R$ is called a ring without zero divisors.

> **Proposition 2.2.11 (Criterion for Ideals)**
> 
> Let $R$ be a ring and $I$ a nonempty subset of $R$. Then $I$ is an ideal of $R$ if and only if $a-b\in{I}$ and $ax,ya\in{I}$ for all $a,b\in{I}$ and $x,y\in{R}$.

> **Theorem 2.2.16 (Quotient Ring)**
> 
> Let $R$ be a ring and $I$ an ideal of $R$. Then the quotient additive group $R/I$ becomes a ring under the multiplication $\left(a+I\right)\left(b+I\right)=ab+I$, called the quotient ring of $R$ by $I$.

> **Definition 2.2.20 (Integral Domain, Division Ring, and Field)**
> 
> A commutative unital ring without zero divisors is called an integral domain; if a unital ring $R$ satisfies that $R^{*}$ forms a group under multiplication (where $R^{*}=R\setminus\left\{0\right\}$), then $R$ is called a division ring; a commutative division ring is called a field.

## 1.10-20

Prove that a non-abelian finite simple group of order $60$ is isomorphic to $A_5$.

### Solution to 1.10-20

Let $G$ be a non-abelian simple group of order $60$. First compute the number $n_{5}$ of Sylow $5$-subgroups. By **Theorem 1.10.10 (Sylow's Third Theorem)**, $n_{5}\mid12$ and $n_{5}\equiv1\pmod5$, so $n_{5}=1$ or $6$. By Sylow Subgroups and Element Counting, since $G$ is simple, $n_{5}\ne1$; hence $n_{5}=6$.

Each Sylow $5$-subgroup is a cyclic group of order $5$ and, by Sylow Subgroups and Element Counting, contains $4$ elements of order $5$; two distinct Sylow $5$-subgroups intersect in $\left\{e\right\}$ (the order of the intersection divides $5$, so it must be $1$). Hence $G$ contains $6\times4=24$ elements of order $5$.

Now consider the number $n_{2}$ of Sylow $2$-subgroups. By **Theorem 1.10.10 (Sylow's Third Theorem)**, $n_{2}\mid15$ and $n_{2}\equiv1\pmod2$, so $n_{2}\in\left\{1,3,5,15\right\}$. By Sylow Subgroups and Element Counting, since $G$ is simple, $n_{2}\ne1$.

Exclude $n_{2}=3$. By Actions on Coset Spaces, $G$ acts by conjugation on the $3$ Sylow $2$-subgroups, giving a homomorphism $\pi:G\to{S}_3$. Its kernel $\ker\pi$ is a normal subgroup of $G$. Since $G$ is simple, $\ker\pi=\left\{e\right\}$ or $G$. The action is transitive, hence nontrivial, so $\ker\pi\ne{G}$; if $\ker\pi=\left\{e\right\}$, then $G$ is isomorphic to a subgroup of $S_3$, but $\left|S_3\right|=6<60$, a contradiction. Hence $n_{2}\ne3$.

Handle $n_{2}=5$. By Actions on Coset Spaces, $G$ acts by conjugation on the $5$ Sylow $2$-subgroups, giving a homomorphism $\pi:G\to{S}_5$. Similarly $\ker\pi$ is a normal subgroup and is not $G$; if $\ker\pi=\left\{e\right\}$, then $G$ is isomorphic to a subgroup of $S_5$ of order $60$. Since $\left|S_5\right|=120$, this subgroup of order $60$ has index $2$, so by Index-Two Subgroups and the Alternating Subgroup of $S_n$ it must be the unique index-two subgroup, namely $A_5$. Hence $G\cong{A}_5$, and the conclusion holds.

Exclude $n_{2}=15$. If any two distinct Sylow $2$-subgroups intersected in $\left\{e\right\}$, then each $4$-order Sylow $2$-subgroup contributes $3$ non-identity elements (by Groups of Order Four Are Abelian and Sylow Subgroups and Element Counting), giving $15\times3=45$ elements of order $2$ or $4$; together with the $24$ elements of order $5$, the total is $45+24=69>60$, a contradiction. Hence there exist two distinct Sylow $2$-subgroups $P,Q$ with $\left|P\cap{Q}\right|=2$.

Write $P\cap{Q}=\left\langle{x}\right\rangle$, where $x$ has order $2$. Since $P,Q$ are groups of order $4$, by Groups of Order Four Are Abelian they are abelian, and $x\in{P}\cap{Q}$, so $P,Q\subseteq{N}_{G}\left(\left\langle{x}\right\rangle\right)$. Since $P\ne{Q}$, we have $\left|N_{G}\left(\left\langle{x}\right\rangle\right)\right|>4$. Moreover $\left|N_{G}\left(\left\langle{x}\right\rangle\right)\right|\mid60$ and is divisible by $4$ (it contains the order-$4$ subgroup $P$), so it can only be $12,20$ or $60$. If it were $60$, then $\left\langle{x}\right\rangle\triangleleft{G}$, contradicting the simplicity of $G$. Hence $\left|N_{G}\left(\left\langle{x}\right\rangle\right)\right|=12$ or $20$, corresponding to index $5$ or $3$.

If the index is $3$, then by Actions on Coset Spaces, $G$ acting on $3$ cosets by left translation gives a homomorphism $G\to{S}_3$, leading to the same contradiction as in the $n_{2}=3$ case. Hence the index must be $5$. Thus $G$ has a subgroup $N_{G}\left(\left\langle{x}\right\rangle\right)$ of index $5$; by Actions on Coset Spaces, $G$ acting by left translation on the $5$ cosets gives a homomorphism $G\to{S}_5$ whose kernel is a normal subgroup different from $G$; since $G$ is simple, the kernel is $\left\{e\right\}$, yielding a monomorphism $G\hookrightarrow{S}_5$. As before, the order-$60$ subgroup of $S_5$ must be $A_5$, so $G\cong{A}_5$. $\blacksquare$

## 2.1-3

Let $R=\left\{a,b,c\right\}$ be a set on which addition and multiplication are defined. Suppose the operation tables of addition $+$ and multiplication $\cdot$ are

$$
\begin{array}{c\left|ccc}
+&a&b&c\\\hline
a&a&b&c\\
b&b&c&a\\
c&c&a&b
\end{array}
\qquad
\begin{array}{c\right|ccc}
\cdot&a&b&c\\\hline
a&a&a&a\\
b&a&a&a\\
c&a&b&a
\end{array}
$$

Is $R$ a ring?

### Solution to 2.1-3

From the addition table, $a$ is the additive zero, and $\left(R,+\right)\cong\mathbb{Z}_3$ (under $a\mapsto0$, $b\mapsto1$, $c\mapsto2$); hence $\left(R,+\right)$ is an abelian group, satisfying condition (1) of **Definition 2.1.1 (Ring)**.

Next we check the distributive law. Take $x=b$, $y=c$, $z=b$. From the addition table, $b+c=a$; from the multiplication table, $a\cdot{b}=a$, $b\cdot{b}=a$, $c\cdot{b}=b$.

Compute the left-hand side:

$$
\left(x+y\right)z=\left(b+c\right)b=a\cdot{b}=a.
$$

Compute the right-hand side:

$$
xz+yz=b\cdot{b}+c\cdot{b}=a+b=b.
$$

Since $a\ne{b}$,

$$
\left(b+c\right)b\ne{b}\cdot{b}+c\cdot{b}.
$$

The left distributive law fails.

Moreover, associativity of multiplication also fails: take $x=c$, $y=c$, $z=b$. From the multiplication table, $c\cdot{c}=a$, $c\cdot{b}=b$, $a\cdot{b}=a$, so

$$
\left(c\cdot{c}\right)\cdot{b}=a\cdot{b}=a,
$$

whereas

$$
c\cdot\left(c\cdot{b}\right)=c\cdot{b}=b.
$$

The two are unequal.

Therefore $R$ fails the associativity of multiplication and the distributive law required by **Definition 2.1.1 (Ring)**, so $R$ is not a ring. $\blacksquare$

## 2.1-5

Let $R$ be a unital ring with identity $e$, and let $a\in{R}$. If there exists $m\in\mathbb{N}$ such that $a^{m}=0$, then $a$ is called a nilpotent element. Prove: if $a$ is nilpotent, then $e+a$ is invertible.

### Solution to 2.1-5

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

Hence $b$ is an inverse of $e+a$, so $e+a$ is invertible. This agrees with Nilpotent Elements and Finite Geometric Series. $\blacksquare$

## 2.1-15

(Hua) Let $R$ be a unital ring with identity $e$, and let $a\in{R}$. If an element $c$ satisfies $ca=e$ ($ac=e$), then $c$ is called a left inverse (right inverse) of $a$. If $c$ is both a left inverse and a right inverse of $a$, then $c$ is called an inverse of $a$, and $a$ is said to be invertible. Prove: for any $a,b\in{R}$, $e-ab$ is invertible if and only if $e-ba$ is invertible.

### Solution to 2.1-15

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

## 2.1-16

(Hua) Let $R$ be a unital ring with identity $e$, and let $a,b\in{R}$. Prove: if $ab$ and $ab-e$ are both invertible, then $a-b^{-1}$ is invertible, and $\left(a-b^{-1}\right)^{-1}-a^{-1}$ is also invertible, with

$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

### Solution to 2.1-16

Since $b^{-1}$ is invertible (the conclusion involves $b^{-1}$, so $b$ is invertible by hypothesis) and $ab$ is invertible, by Properties of Invertible Elements in a Unital Ring, $a=\left(ab\right)b^{-1}$ is a product of invertible elements, so $a$ is invertible and $a^{-1}$ exists.

Also, since $b^{-1}$ is invertible, by the distributive law of **Definition 2.1.1 (Ring)**,

$$
a-b^{-1}=\left(ab-e\right)b^{-1}.
$$

Since $ab-e$ is invertible by hypothesis and $b^{-1}$ is invertible, by Properties of Invertible Elements in a Unital Ring, the product of invertible elements is invertible, so $a-b^{-1}$ is invertible, and

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
\left(bX^{-1}-a^{-1}\right)\cdot{a}\left(ba-e\right)=bX^{-1}a\left(ba-e\right)-a^{-1}a\left(ba-e\right)=\left[bX^{-1}a-e\right]\left(ba-e\right).
$$

By the Hua identity from Problem 2.1-15,

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

## 2.2-3

Let $R$ be a ring without zero divisors and $I$ an ideal of $R$. Is the quotient ring $R/I$ necessarily a ring without zero divisors?

### Solution to 2.2-3

Not necessarily. We give a counterexample below.

Take the integer ring $R=\mathbb{Z}$. By The Integer Ring $\mathbb{Z}$ Is an Integral Domain, $\mathbb{Z}$ is an integral domain, hence satisfies **Definition 2.1.8 (Ring Without Zero Divisors)**. Take the ideal $I=6\mathbb{Z}$. By **Theorem 2.2.16 (Quotient Ring)**, the quotient ring is

$$
R/I=\mathbb{Z}/6\mathbb{Z}=\mathbb{Z}_6.
$$

In $\mathbb{Z}_6$,

$$
\left(2+6\mathbb{Z}\right)\left(3+6\mathbb{Z}\right)=6+6\mathbb{Z}=0+6\mathbb{Z},
$$

but $2\notin6\mathbb{Z}$ and $3\notin6\mathbb{Z}$; hence $2+6\mathbb{Z}$ and $3+6\mathbb{Z}$ are both nonzero zero divisors. By **Definition 2.1.8 (Ring Without Zero Divisors)**, $R/I$ is not a ring without zero divisors.

Therefore $R/I$ is not necessarily a ring without zero divisors. $\blacksquare$

## 2.2-6

Let $R$ be a ring without zero divisors with only finitely many ideals (including left ideals, right ideals and two-sided ideals). Prove that $R$ is a division ring.

### Solution to 2.2-6

First prove that $R$ has an identity. Since $R$ is a ring without zero divisors, by **Definition 2.1.8 (Ring Without Zero Divisors)** $R$ is not the zero ring, so there exists $0\ne{a}\in{R}$. Consider the descending chain of left ideals

$$
R\supseteq{R}a\supseteq{R}a^{2}\supseteq\cdots.
$$

Since $R$ has only finitely many left ideals, this chain must stabilize, i.e. there exists $m$ with $Ra^{m}=Ra^{m+1}$. Hence $a^{m}\in{R}a^{m+1}$, so there exists $b\in{R}$ with $a^{m}=ba^{m+1}$. Put $e=ba$; then $ea^{m}=a^{m}$.

For any $x\in{R}$,

$$
\left(xe-x\right)a^{m}=x\left(ea^{m}\right)-xa^{m}=xa^{m}-xa^{m}=0.
$$

Since $a^{m}\ne0$ (from $a\ne0$ and **Definition 2.1.8 (Ring Without Zero Divisors)**, $a^{m}\ne0$), by Cancellation with Nonzero Elements we get $xe-x=0$, i.e. $xe=x$ for all $x\in{R}$. Hence $e$ is a right identity of $R$, and $e\ne0$ (otherwise $xe=x$ would give $x=0$ for all $x$, contradicting that $R$ is not the zero ring).

Also, for any $x\in{R}$,

$$
e\left(ex-x\right)=e^{2}x-ex=ex-ex=0,
$$

where we used that the right identity gives $e^{2}=e\cdot{e}=e$. Since $e\ne0$ and $e\left(ex-x\right)=0$, by Cancellation with Nonzero Elements we get $ex-x=0$, i.e. $ex=x$. Hence $e$ is also a left identity, so $e$ is the identity of $R$.

Next prove that every nonzero element is invertible. Take any $0\ne{x}\in{R}$. Similarly, the descending chain of left ideals $Rx\supseteq{R}x^{2}\supseteq\cdots$ stabilizes because there are only finitely many left ideals; there exists $n$ with $Rx^{n}=Rx^{n+1}$. Hence there exists $y\in{R}$ with $x^{n}=yx^{n+1}=\left(yx\right)x^{n}$, i.e. $\left(e-yx\right)x^{n}=0$. Since $x^{n}\ne0$, by Cancellation with Nonzero Elements we get $e-yx=0$, i.e. $yx=e$. Hence $y$ is a left inverse of $x$.

Moreover,

$$
\left(xy-e\right)x=xyx-ex=x\left(yx\right)-x=xe-x=0,
$$

and since $x\ne0$, by Cancellation with Nonzero Elements we get $xy=e$. Hence $x$ also has the right inverse $y$, i.e. $x$ is invertible.

Thus every element of $R^{*}=R\setminus\left\{0\right\}$ is invertible, so $R^{*}$ forms a group under multiplication. By **Definition 2.2.20 (Integral Domain, Division Ring, and Field)**, $R$ is a division ring. $\blacksquare$

## 2.2-11

Let $R$ be a commutative ring and $I$ an ideal of $R$. Define

$$
\sqrt{I}=\left\{a\in{R}\mid\exists\,n\in\mathbb{N},\;a^{n}\in{I}\right\}.
$$

Prove that $\sqrt{I}$ is also an ideal of $R$, called the radical of the ideal $I$. In particular, the set of all nilpotent elements of $R$ (i.e. the radical of the ideal $\left\{0\right\}$) is an ideal of $R$, called the nilradical of $R$, denoted $\mathrm{Rad}\,R$. Prove that for every ideal $I$ of $R$, $\sqrt{\sqrt{I}}=\sqrt{I}$.

### Solution to 2.2-11

First prove that $\sqrt{I}$ is an ideal. We verify using **Proposition 2.2.11 (Criterion for Ideals)**.

First, $0\in\sqrt{I}$ (take $n=1$; $0\in{I}$), so $\sqrt{I}$ is nonempty.

Let $a,b\in\sqrt{I}$; then there exist $m,n\in\mathbb{N}$ with $a^{m}\in{I}$ and $b^{n}\in{I}$. Since $R$ is commutative, by Binomial Theorem in a Commutative Ring,

$$
\left(a-b\right)^{m+n-1}=\sum_{k=0}^{m+n-1}\binom{m+n-1}{k}a^{k}\left(-b\right)^{m+n-1-k}.
$$

For any term on the right: if $k\ge{m}$, then $a^{k}=a^{m}a^{k-m}\in{I}$; if $k<{}m$, then $m+n-1-k\ge{n}$, so $\left(-b\right)^{m+n-1-k}=b^{m+n-1-k}\in{I}$ (because $b^{n}\in{I}$). Hence every term belongs to $I$, i.e. $\left(a-b\right)^{m+n-1}\in{I}$, so $a-b\in\sqrt{I}$.

Next let $a\in\sqrt{I}$, $r\in{R}$ with $a^{n}\in{I}$; then $\left(ra\right)^{n}=r^{n}a^{n}\in{I}$ ($R$ is commutative and $I$ is an ideal, by **Proposition 2.2.11 (Criterion for Ideals)**), so $ra\in\sqrt{I}$.

By **Proposition 2.2.11 (Criterion for Ideals)**, $\sqrt{I}$ is an ideal of $R$. Taking $I=\left\{0\right\}$, $\sqrt{\left\{0\right\}}$ is exactly the set of all nilpotent elements of $R$ (i.e. elements satisfying $a^{n}=0$); it is an ideal, namely the nilradical $\mathrm{Rad}\,R$.

Next prove $\sqrt{\sqrt{I}}=\sqrt{I}$.

First prove $\sqrt{I}\subseteq\sqrt{\sqrt{I}}$: let $a\in\sqrt{I}$; then $a^{n}\in{I}$ for some $n$. Since $I\subseteq\sqrt{I}$ (for $x\in{I}$, $x^{1}\in{I}$, so $x\in\sqrt{I}$), we have $a^{n}\in\sqrt{I}$, i.e. $a\in\sqrt{\sqrt{I}}$.

Next prove $\sqrt{\sqrt{I}}\subseteq\sqrt{I}$: let $a\in\sqrt{\sqrt{I}}$; then $a^{n}\in\sqrt{I}$ for some $n$, so there exists $m$ with $\left(a^{n}\right)^{m}=a^{nm}\in{I}$, hence $a\in\sqrt{I}$.

In conclusion, $\sqrt{\sqrt{I}}=\sqrt{I}$. $\blacksquare$

## 2.2-13

Let $R$ be a commutative ring, and define an operation on $R$ by $a\circ{b}=a+b-ab$.

(1) Prove that $\circ$ is associative, and $0\circ{a}=a$ for all $a\in{R}$;

(2) Prove that $R$ is a field if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group, where $e$ is the identity of $R$.

### Solution to 2.2-13

Part (1). For any $a,b,c\in{R}$, expanding by the distributive law of **Definition 2.1.1 (Ring)**:

$$
\left(a\circ{b}\right)\circ{c}=\left(a+b-ab\right)\circ{c}=\left(a+b-ab\right)+c-\left(a+b-ab\right)c=a+b+c-ab-ac-bc+abc,
$$

and

$$
a\circ\left(b\circ{c}\right)=a\circ\left(b+c-bc\right)=a+\left(b+c-bc\right)-a\left(b+c-bc\right)=a+b+c-ab-ac-bc+abc.
$$

The two are equal, so $\circ$ is associative. Moreover,

$$
0\circ{a}=0+a-0\cdot{a}=a.
$$

Also, since $R$ is commutative, $a\circ{b}=a+b-ab=b+a-ba=b\circ{a}$, so $\circ$ is commutative.

Part (2). Consider the map $\psi:R\to{R}$, $\psi\left(x\right)=e-x$. Clearly $\psi$ is bijective (it is its own inverse), with $\psi\left(0\right)=e$ and $\psi\left(e\right)=0$. For any $a,b\in{R}$,

$$
\psi\left(a\right)\circ\psi\left(b\right)=\left(e-a\right)\circ\left(e-b\right)=\left(e-a\right)+\left(e-b\right)-\left(e-a\right)\left(e-b\right)=e-ab=\psi\left(ab\right).
$$

Hence $\psi$ transfers the multiplication of $R$ homomorphically to the operation $\circ$, and $\psi$ restricts to a bijection from $R\setminus\left\{0\right\}$ to $R\setminus\left\{e\right\}$ ($\psi\left(x\right)=e$ if and only if $x=0$). Therefore $\left(R\setminus\left\{0\right\},\cdot\right)$ is an abelian group if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group.

By **Definition 2.2.20 (Integral Domain, Division Ring, and Field)**, a commutative unital ring $R$ is a field if and only if $R\setminus\left\{0\right\}$ forms an abelian group under multiplication. Hence $R$ is a field if and only if $\left(R\setminus\left\{e\right\},\circ\right)$ is an abelian group. $\blacksquare$
