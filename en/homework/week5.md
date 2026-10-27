# week5

> **Basic Knowledge: The Additive Group of Residue Classes Modulo $n$**<br>$\mathbb Z_n=\left\{\overline{0},\overline{1},\cdots,\overline{n-1}\right\}$ is a cyclic group of order $n$ under addition, with generator $\overline{1}$; for an integer $k$, $k\overline{1}=\overline{0}$ if and only if $n\mid k$. For $\left(\overline{x},\overline{y}\right)\in\mathbb Z_m\times\mathbb Z_n$, $k\left(\overline{x},\overline{y}\right)=\left(\overline{0},\overline{0}\right)$ if and only if $m\mid kx$ and $n\mid ky$.

> **Basic Knowledge: Number of Generators of a Cyclic Group**<br>If $C$ is a cyclic group of order $d$, then $C$ has exactly $\varphi\left(d\right)$ elements of order $d$ (i.e. generators), where $\varphi$ is the Euler totient function.

> **Basic Knowledge: Euler's Totient Function and the Divisibility Identity**<br>$\varphi\left(n\right)$ is the number of positive integers not exceeding $n$ that are coprime to $n$; for a positive integer $n$, $\sum_{d\mid n}\varphi\left(d\right)=n$.

> **Basic Knowledge: Greatest Common Divisor and Least Common Multiple**<br>For positive integers $m,n$, if $\left(m,n\right)=1$, then $m\mid k$ and $n\mid k$ if and only if $mn\mid k$.

> **Theorem 1.2.22 (Lagrange's Theorem)**<br>Let $G$ be a finite group and $H<G$. Then $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, where $\left[G:H\right]$ is the index of $H$ in $G$. Hence the order of the subgroup $H$ is a divisor of the order of the group $G$; in particular, the order of any element is also a divisor of $\left|G\right|$.

> **Theorem 1.5.5 (Classification of Cyclic Groups)**<br>Let $G$ be a cyclic group. If $G$ is infinite, then $G$ is isomorphic to $\left(\mathbb Z,+\right)$; if $G$ is a group of order $n$, then $G$ is isomorphic to $\left(\mathbb Z_n,+\right)$. Hence two cyclic groups are isomorphic if and only if they have the same order.

---

## 1.5-3

Let $\left(m,n\right)=1$. Prove that $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$.

### Solution 1.5-3

Consider the element $\left(\overline{1},\overline{1}\right)$ of $\mathbb Z_m\times\mathbb Z_n$. Let its order be $d$. By **Basic Knowledge: The Additive Group of Residue Classes Modulo $n$**, $d\left(\overline{1},\overline{1}\right)=\left(d\overline{1},d\overline{1}\right)=\left(\overline{0},\overline{0}\right)$ if and only if $m\mid d$ and $n\mid d$. By the definition of order, $d\left(\overline{1},\overline{1}\right)=\left(\overline{0},\overline{0}\right)$, so $m\mid d$ and $n\mid d$. Since $\left(m,n\right)=1$, by **Basic Knowledge: Greatest Common Divisor and Least Common Multiple**, $mn\mid d$.

On the other hand, $mn\left(\overline{1},\overline{1}\right)=\left(mn\overline{1},mn\overline{1}\right)=\left(\overline{0},\overline{0}\right)$, so $d\mid mn$.

Hence $d=mn$, i.e. $\left(\overline{1},\overline{1}\right)$ has order $mn$.

Therefore $\left\langle\left(\overline{1},\overline{1}\right)\right\rangle$ is a cyclic subgroup of $\mathbb Z_m\times\mathbb Z_n$ of order $mn$. Since $\left|\mathbb Z_m\times\mathbb Z_n\right|=\left|\mathbb Z_m\right|\left|\mathbb Z_n\right|=mn$, we have $\mathbb Z_m\times\mathbb Z_n=\left\langle\left(\overline{1},\overline{1}\right)\right\rangle$, i.e. $\mathbb Z_m\times\mathbb Z_n$ is a cyclic group of order $mn$.

By **Theorem 1.5.5 (Classification of Cyclic Groups)**, cyclic groups of the same order are isomorphic, so $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$. $\blacksquare$

---

## 1.5-15

Prove the converse of Theorem 1.5.8, i.e.: let $G$ be a group of order $n$, and suppose that for every divisor $m$ of $n$ there exists a unique subgroup of $G$ of order $m$. Then $G$ is cyclic.

### Solution 1.5-15

Let $G$ be a group of order $n$, and suppose that for every divisor $d$ of $n$ there exists a unique subgroup $H_d$ of order $d$. For each $d\mid n$, let $f\left(d\right)$ be the number of elements of $G$ of order exactly $d$.

**Claim: $f\left(d\right)$ is either $0$ or $\varphi\left(d\right)$.** If $f\left(d\right)=0$, the claim is clear. If $f\left(d\right)>0$, take $a\in G$ of order $d$; then $\left\langle a\right\rangle$ is a subgroup of $G$ of order $d$, and by uniqueness $\left\langle a\right\rangle=H_d$, so $H_d$ is a cyclic group of order $d$. For any element $b\in G$ of order $d$, $\left\langle b\right\rangle$ is also a subgroup of $G$ of order $d$, so by uniqueness $\left\langle b\right\rangle=H_d$; hence $b$ is a generator of the cyclic group $H_d$ of order $d$. By **Basic Knowledge: Number of Generators of a Cyclic Group**, a cyclic group of order $d$ has exactly $\varphi\left(d\right)$ generators, so $f\left(d\right)=\varphi\left(d\right)$. The claim is proved.

Hence $f\left(d\right)\le\varphi\left(d\right)$ for every $d\mid n$.

On the other hand, by **Theorem 1.2.22 (Lagrange's Theorem)**, the order of every element of $G$ is a divisor of $n$, so

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

By **Basic Knowledge: Euler's Totient Function and the Divisibility Identity**, $\sum_{d\mid n}\varphi\left(d\right)=n$, hence

$$
\sum_{d\mid n}f\left(d\right)=\sum_{d\mid n}\varphi\left(d\right)=n.
$$

Since $f\left(d\right)\le\varphi\left(d\right)$ for every $d\mid n$ and the two sums are equal, we must have $f\left(d\right)=\varphi\left(d\right)$ for every $d\mid n$.

In particular, $f\left(n\right)=\varphi\left(n\right)>0$, so $G$ contains an element $a$ of order $n$; then $\left\langle a\right\rangle$ is a subgroup of $G$ of order $n$, and since $\left|G\right|=n$, we have $G=\left\langle a\right\rangle$, i.e. $G$ is cyclic. $\blacksquare$

---

## 1.5-16

Let $G$ be a finite group whose distinct subgroups have distinct orders. Prove that $G$ is cyclic.

### Solution 1.5-16

Write $\left|G\right|=n$. By the hypothesis, for every positive integer $d$, $G$ has at most one subgroup of order $d$ (if there were two subgroups of order $d$, they would have the same order, contradicting the hypothesis). For each $d\mid n$, let $f\left(d\right)$ be the number of elements of $G$ of order exactly $d$.

**Claim: $f\left(d\right)\le\varphi\left(d\right)$ for every $d\mid n$.** If $f\left(d\right)=0$, the claim is clear. If $f\left(d\right)>0$, take $a\in G$ of order $d$; then $\left\langle a\right\rangle$ is a cyclic subgroup of $G$ of order $d$. By the hypothesis, $G$ has at most one subgroup of order $d$, so every element $b\in G$ of order $d$ satisfies $\left\langle b\right\rangle=\left\langle a\right\rangle$, i.e. $b$ is a generator of the cyclic group $\left\langle a\right\rangle$ of order $d$. By **Basic Knowledge: Number of Generators of a Cyclic Group**, a cyclic group of order $d$ has exactly $\varphi\left(d\right)$ generators, so $f\left(d\right)=\varphi\left(d\right)\le\varphi\left(d\right)$. The claim is proved.

By **Theorem 1.2.22 (Lagrange's Theorem)**, the order of every element of $G$ divides $n$, so every element of $G$ is counted in exactly one $f\left(d\right)$ with $d\mid n$, i.e.

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

By **Basic Knowledge: Euler's Totient Function and the Divisibility Identity**, $\sum_{d\mid n}\varphi\left(d\right)=n$. Combined with the claim,

$$
n=\sum_{d\mid n}f\left(d\right)\le\sum_{d\mid n}\varphi\left(d\right)=n.
$$

The two ends are equal, so we must have $f\left(d\right)=\varphi\left(d\right)$ for every $d\mid n$.

In particular, $f\left(n\right)=\varphi\left(n\right)>0$, so $G$ contains an element $a$ of order $n$, and hence $G=\left\langle a\right\rangle$ is cyclic. $\blacksquare$
