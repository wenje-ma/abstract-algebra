# Assignment 5

> **Theorem 1.5.5** (Classification of Cyclic Groups) Let $G$ be a cyclic group. If $G$ is infinite, then $G$ is isomorphic to $\left(\mathbb Z,+\right)$; if $G$ has order $n$, then $G$ is isomorphic to $\left(\mathbb Z_{n},+\right)$. Hence two cyclic groups are isomorphic if and only if they have the same order.

> **Lemma 1.5.7** (Subgroup Structure of Cyclic Groups) Every subgroup of a cyclic group $G=\left\langle a\right\rangle$ is of the form $\left\langle a^{l}\right\rangle$, $l\in\mathbb N$, and is therefore also cyclic.

> **Theorem 1.5.8** (Existence and Uniqueness of Subgroups of Cyclic Groups) Let $G$ be a cyclic group of order $n$ and $k\mid n$. Then there exists a unique subgroup of order $k$ of $G$.

> **Theorem 1.2.22** (Lagrange's Theorem) Let $G$ be a finite group and $H< G$. Then $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$. In particular, the order of any element also divides $\left|G\right|$.

> **Basic Knowledge** (Euler's Totient Function) $\varphi\left(n\right)$ is the number of positive integers coprime to $n$ and not exceeding $n$. For a positive integer $n$, $\sum_{d\mid n}\varphi\left(d\right)=n$. A cyclic group of order $n$ has exactly $\varphi\left(n\right)$ generators.

### Problem 1

(Problem 1.5-3) Let $\left(m,n\right)=1$. Prove that $\mathbb Z_{m}\times\mathbb Z_{n}\cong\mathbb Z_{mn}$.

### Solution to Problem 1

Consider the element $\left(1,1\right)$ in $\mathbb Z_{m}\times\mathbb Z_{n}$. Let its order be $d$. Then

$$
d\left(1,1\right)=\left(d\bmod m,d\bmod n\right)=\left(0,0\right),
$$

i.e. $m\mid d$ and $n\mid d$. Since $\left(m,n\right)=1$, $mn\mid d$.

On the other hand, $mn\left(1,1\right)=\left(0,0\right)$, so $d\mid mn$.

Therefore $d=mn$, i.e. the order of $\left(1,1\right)$ is $mn$.

Thus $\left\langle\left(1,1\right)\right\rangle$ is a cyclic subgroup of $\mathbb Z_{m}\times\mathbb Z_{n}$ of order $mn$. Since $\left|\mathbb Z_{m}\times\mathbb Z_{n}\right|=mn$, $\mathbb Z_{m}\times\mathbb Z_{n}=\left\langle\left(1,1\right)\right\rangle$ is a cyclic group of order $mn$.

By **Theorem 1.5.5** (Classification of Cyclic Groups), cyclic groups of the same order are isomorphic, so $\mathbb Z_{m}\times\mathbb Z_{n}\cong\mathbb Z_{mn}$. $\blacksquare$

### Problem 2

(Problem 1.5-15) Prove the converse of Theorem 1.5.8: if $G$ is a group of order $n$ and for every divisor $m$ of $n$ there exists a unique subgroup of order $m$ of $G$, then $G$ is cyclic.

### Solution to Problem 2

Let $G$ be a group of order $n$ such that for every divisor $d$ of $n$ there exists a unique subgroup of order $d$, denoted $H_{d}$.

For each $d\mid n$, let $f\left(d\right)$ be the number of elements in $G$ whose order is exactly $d$.

**Claim** $f\left(d\right)$ is either $0$ or $\varphi\left(d\right)$.

Indeed, if $f\left(d\right)=0$, the claim is immediate. If $f\left(d\right)> 0$, take $a\in G$ with $\mathrm{ord}\left(a\right)=d$; then $\left\langle a\right\rangle$ is a subgroup of $G$ of order $d$. By uniqueness, $\left\langle a\right\rangle=H_{d}$, so $H_{d}$ is cyclic. Also, any element $b\in G$ of order $d$ generates a subgroup $\left\langle b\right\rangle$ which is also of order $d$, so by uniqueness $\left\langle b\right\rangle=H_{d}$. Hence all elements of order $d$ in $G$ lie in $H_{d}$, and a cyclic group of order $d$ has exactly $\varphi\left(d\right)$ generators (i.e. elements of order $d$), so $f\left(d\right)=\varphi\left(d\right)$.

Thus for each $d\mid n$, $f\left(d\right)\le\varphi\left(d\right)$.

On the other hand, by **Theorem 1.2.22** (Lagrange's Theorem), the order of every element of $G$ divides $n$, so

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

Also, by the number-theoretic identity $\sum_{d\mid n}\varphi\left(d\right)=n$,

$$
\sum_{d\mid n}f\left(d\right)=\sum_{d\mid n}\varphi\left(d\right)=n.
$$

Since $f\left(d\right)\le\varphi\left(d\right)$ for every $d\mid n$ and the two sums are equal, we must have $f\left(d\right)=\varphi\left(d\right)$ for all $d\mid n$.

In particular, $f\left(n\right)=\varphi\left(n\right)> 0$, so $G$ contains an element of order $n$, and hence $G=\left\langle a\right\rangle$ is cyclic. $\blacksquare$

### Problem 3

(Problem 1.5-16) Let a finite group $G$ have subgroups of pairwise distinct orders. Prove that $G$ is cyclic.

### Solution to Problem 3

Let $\left|G\right|=n$. By the assumption, for each positive integer $d$, $G$ has at most one subgroup of order $d$ (if there were two subgroups of the same order, it would contradict the assumption).

For each $d\mid n$, let $f\left(d\right)$ be the number of elements in $G$ whose order is exactly $d$.

**Claim** $f\left(d\right)\le\varphi\left(d\right)$.

Indeed, if $f\left(d\right)=0$, the conclusion is immediate. If $f\left(d\right)> 0$, take $a\in G$ with $\mathrm{ord}\left(a\right)=d$; then $\left\langle a\right\rangle$ is a cyclic subgroup of $G$ of order $d$. By the assumption, this is the unique subgroup of $G$ of order $d$. Hence any element $b\in G$ of order $d$ satisfies $\left\langle b\right\rangle=\left\langle a\right\rangle$, i.e. $b$ is a generator of this cyclic group of order $d$. A cyclic group of order $d$ has exactly $\varphi\left(d\right)$ generators, so $f\left(d\right)=\varphi\left(d\right)$.

By **Theorem 1.2.22** (Lagrange's Theorem), the order of every element of $G$ divides $n$, so

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right)\le\sum_{d\mid n}\varphi\left(d\right)=n.
$$

The two sides of the inequality are equal, so for each $d\mid n$ we must have $f\left(d\right)=\varphi\left(d\right)$.

In particular, $f\left(n\right)=\varphi\left(n\right)> 0$, so $G$ contains an element of order $n$, and hence $G$ is cyclic. $\blacksquare$
