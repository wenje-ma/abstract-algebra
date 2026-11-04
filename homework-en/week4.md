# week4

> **Theorem 1.2.22 (Lagrange's Theorem)**
> 
> Let $G$ be a finite group and $H< G$. Then $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, where $\left[G:H\right]$ is the index of $H$ in $G$. Hence the order of the subgroup $H$ is a divisor of the order of the group $G$; in particular, the order of any element is also a divisor of $\left|G\right|$.

> **Theorem 1.4.10 (Cayley's Theorem)**
> 
> Every group $G$ is isomorphic to a subgroup of the symmetric group $S_G$; in fact the map $L:G\to L_G$, $a\mapsto L_a$ is a monomorphism.

> **Lemma 1.4.13**
> 
> Let $f:G\to G'$ be a group homomorphism. Then $\mathrm{Im}\,f< G'$ and $\ker f\triangleleft G$.

> **Example 1.4.17**
> 
> Let $V$ be an $n$-dimensional vector space over a field $P$. Then the map $\det\circ\pi:S_n\to P^{*}$, $\sigma\mapsto\det\left(\pi_\sigma\right)$ is a group homomorphism whose image is $\left\{1,-1\right\}$ (for $n> 1$); its kernel is denoted $A_n$.

> **Theorem 1.4.19 (Fundamental Theorem of Group Homomorphisms)**
> 
> Let $f:G\to G'$ be a surjective group homomorphism. Then $G/\ker f\cong G'$.

> **Theorem 1.5.5 (Classification of Cyclic Groups)**
> 
> Let $G$ be a cyclic group. If $G$ is infinite, then $G$ is isomorphic to $\left(\mathbb Z,+\right)$; if $G$ is a group of order $n$, then $G$ is isomorphic to $\left(\mathbb Z_n,+\right)$. Hence two cyclic groups are isomorphic if and only if they have the same order.

> **Definition 1.6.1 (Cycle)**
> 
> Let $\left\{i_1,i_2,\cdots,i_r\right\}\subseteq\left\{1,2,\cdots,n\right\}$. If $\sigma\in S_n$ satisfies $\sigma\left(i_1\right)=i_2$, $\sigma\left(i_2\right)=i_3$, ..., $\sigma\left(i_r\right)=i_1$ and fixes all other letters, then $\sigma$ is called an $r$-cycle, denoted $\sigma=\left(i_1i_2\cdots i_r\right)$. In particular, a $2$-cycle is called a transposition.

> **Theorem 1.6.4 (Cycle Decomposition)**
> 
> Every element $\sigma$ of $S_n$ can be written as a product of some disjoint cycles of $S_n$; disregarding order, this representation is unique.

> **Lemma 1.6.7 (Decomposition of a Cycle into Transpositions)**
> 
> Every $r$-cycle can be written as a product of $r-1$ transpositions: $\left(i_1i_2\cdots i_r\right)=\left(i_1i_r\right)\left(i_1i_{r-1}\right)\cdots\left(i_1i_3\right)\left(i_1i_2\right)$.

> **Proposition 1.6.8**
> 
> Every permutation of $n$ elements can be written as a product of transpositions.

> **Theorem 1.6.9 (Simplicity of the Alternating Group)**
> 
> For $n\ge5$, $A_n$ is a simple group.

## 1.5-3

Let $\left(m,n\right)=1$. Prove that $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$.

### Solution to 1.5-3

Consider the element $\left(\overline{1},\overline{1}\right)$ of $\mathbb Z_m\times\mathbb Z_n$. Let its order be $d$. By The Additive Group of Residue Classes Modulo $n$, $d\left(\overline{1},\overline{1}\right)=\left(d\overline{1},d\overline{1}\right)=\left(\overline{0},\overline{0}\right)$ if and only if $m\mid d$ and $n\mid d$. By the definition of order, $d\left(\overline{1},\overline{1}\right)=\left(\overline{0},\overline{0}\right)$, so $m\mid d$ and $n\mid d$. Since $\left(m,n\right)=1$, by Greatest Common Divisor and Least Common Multiple, $mn\mid d$.

On the other hand, $mn\left(\overline{1},\overline{1}\right)=\left(mn\overline{1},mn\overline{1}\right)=\left(\overline{0},\overline{0}\right)$, so $d\mid mn$.

Hence $d=mn$, i.e. $\left(\overline{1},\overline{1}\right)$ has order $mn$.

Therefore $\left\langle\left(\overline{1},\overline{1}\right)\right\rangle$ is a cyclic subgroup of $\mathbb Z_m\times\mathbb Z_n$ of order $mn$. Since $\left|\mathbb Z_m\times\mathbb Z_n\right|=\left|\mathbb Z_m\right|\left|\mathbb Z_n\right|=mn$, we have $\mathbb Z_m\times\mathbb Z_n=\left\langle\left(\overline{1},\overline{1}\right)\right\rangle$, i.e. $\mathbb Z_m\times\mathbb Z_n$ is a cyclic group of order $mn$.

By **Theorem 1.5.5 (Classification of Cyclic Groups)**, cyclic groups of the same order are isomorphic, so $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$. $\blacksquare$

## 1.5-15

Prove the converse of Theorem 1.5.8, i.e.: let $G$ be a group of order $n$, and suppose that for every divisor $m$ of $n$ there exists a unique subgroup of $G$ of order $m$. Then $G$ is cyclic.

### Solution to 1.5-15

Let $G$ be a group of order $n$, and suppose that for every divisor $d$ of $n$ there exists a unique subgroup $H_d$ of order $d$. For each $d\mid n$, let $f\left(d\right)$ be the number of elements of $G$ of order exactly $d$.

**Claim: $f\left(d\right)$ is either $0$ or $\varphi\left(d\right)$.** If $f\left(d\right)=0$, the claim is clear. If $f\left(d\right)> 0$, take $a\in G$ of order $d$; then $\left\langle a\right\rangle$ is a subgroup of $G$ of order $d$, and by uniqueness $\left\langle a\right\rangle=H_d$, so $H_d$ is a cyclic group of order $d$. For any element $b\in G$ of order $d$, $\left\langle b\right\rangle$ is also a subgroup of $G$ of order $d$, so by uniqueness $\left\langle b\right\rangle=H_d$; hence $b$ is a generator of the cyclic group $H_d$ of order $d$. By Number of Generators of a Cyclic Group, a cyclic group of order $d$ has exactly $\varphi\left(d\right)$ generators, so $f\left(d\right)=\varphi\left(d\right)$. The claim is proved.

Hence $f\left(d\right)\le\varphi\left(d\right)$ for every $d\mid n$.

On the other hand, by **Theorem 1.2.22 (Lagrange's Theorem)**, the order of every element of $G$ is a divisor of $n$, so

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

By Euler's Totient Function and the Divisibility Identity, $\sum_{d\mid n}\varphi\left(d\right)=n$, hence

$$
\sum_{d\mid n}f\left(d\right)=\sum_{d\mid n}\varphi\left(d\right)=n.
$$

Since $f\left(d\right)\le\varphi\left(d\right)$ for every $d\mid n$ and the two sums are equal, we must have $f\left(d\right)=\varphi\left(d\right)$ for every $d\mid n$.

In particular, $f\left(n\right)=\varphi\left(n\right)> 0$, so $G$ contains an element $a$ of order $n$; then $\left\langle a\right\rangle$ is a subgroup of $G$ of order $n$, and since $\left|G\right|=n$, we have $G=\left\langle a\right\rangle$, i.e. $G$ is cyclic. $\blacksquare$

## 1.5-16

Let $G$ be a finite group whose distinct subgroups have distinct orders. Prove that $G$ is cyclic.

### Solution to 1.5-16

Write $\left|G\right|=n$. By the hypothesis, for every positive integer $d$, $G$ has at most one subgroup of order $d$ (if there were two subgroups of order $d$, they would have the same order, contradicting the hypothesis). For each $d\mid n$, let $f\left(d\right)$ be the number of elements of $G$ of order exactly $d$.

**Claim: $f\left(d\right)\le\varphi\left(d\right)$ for every $d\mid n$.** If $f\left(d\right)=0$, the claim is clear. If $f\left(d\right)> 0$, take $a\in G$ of order $d$; then $\left\langle a\right\rangle$ is a cyclic subgroup of $G$ of order $d$. By the hypothesis, $G$ has at most one subgroup of order $d$, so every element $b\in G$ of order $d$ satisfies $\left\langle b\right\rangle=\left\langle a\right\rangle$, i.e. $b$ is a generator of the cyclic group $\left\langle a\right\rangle$ of order $d$. By Number of Generators of a Cyclic Group, a cyclic group of order $d$ has exactly $\varphi\left(d\right)$ generators, so $f\left(d\right)=\varphi\left(d\right)\le\varphi\left(d\right)$. The claim is proved.

By **Theorem 1.2.22 (Lagrange's Theorem)**, the order of every element of $G$ divides $n$, so every element of $G$ is counted in exactly one $f\left(d\right)$ with $d\mid n$, i.e.

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

By Euler's Totient Function and the Divisibility Identity, $\sum_{d\mid n}\varphi\left(d\right)=n$. Combined with the claim,

$$
n=\sum_{d\mid n}f\left(d\right)\le\sum_{d\mid n}\varphi\left(d\right)=n.
$$

The two ends are equal, so we must have $f\left(d\right)=\varphi\left(d\right)$ for every $d\mid n$.

In particular, $f\left(n\right)=\varphi\left(n\right)> 0$, so $G$ contains an element $a$ of order $n$, and hence $G=\left\langle a\right\rangle$ is cyclic. $\blacksquare$

## 1.6-5

Prove that

$$
S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle,\quad A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle.
$$

### Solution to 1.6-5

**Part 1: prove that $S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$.** By **Proposition 1.6.8**, $S_n$ is generated by all transpositions. For any transposition $\left(ij\right)$ with $i\ne1$, $j\ne1$, by Conjugation of Cycles, taking $\sigma=\left(1i\right)$ gives $\left(1i\right)\left(1j\right)\left(1i\right)=\left(\sigma\left(1\right)\sigma\left(j\right)\right)=\left(i,j\right)=\left(ij\right)$. Hence every transposition $\left(ij\right)$ can be expressed in terms of $\left(12\right),\left(13\right),\cdots,\left(1n\right)$, so $S_n\subseteq\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$; the reverse inclusion is clear, so $S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$.

**Part 2: prove that $S_n=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle$.** Write $\sigma=\left(12\cdots n\right)$. By Conjugation of Cycles, for $k=1,2,\cdots,n-1$,

$$
\sigma^{k-1}\left(12\right)\sigma^{-\left(k-1\right)}=\left(\sigma^{k-1}\left(1\right)\sigma^{k-1}\left(2\right)\right)=\left(k,k+1\right),
$$

so the adjacent transpositions $\left(12\right),\left(23\right),\cdots,\left(n-1,n\right)$ all belong to $\left\langle\left(12\right),\sigma\right\rangle$. Since the adjacent transpositions generate $S_n$ (by **Proposition 1.6.8**, any transposition $\left(ij\right)$ can be written as a product of adjacent transpositions), we have $S_n\subseteq\left\langle\left(12\right),\sigma\right\rangle$; the reverse inclusion is clear, so $S_n=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle$.

**Part 3: prove that $A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$.** By The Alternating Group Is Generated by 3-Cycles, $A_n$ is generated by all 3-cycles. We show that every 3-cycle belongs to $\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$.

(1) A 3-cycle containing $1$ and $2$ is $\left(12k\right)$ or its inverse, which is in the generating set.

(2) A 3-cycle $\left(1jk\right)$ containing $1$ but not $2$ ($j,k\ne2$): a direct computation gives $\left(12k\right)\left(12j\right)^{-1}=\left(12k\right)\left(1j2\right)=\left(1jk\right)$, so $\left(1jk\right)$ belongs to the generated group.

(3) A 3-cycle $\left(ijk\right)$ not containing $1$: by (2), both $\left(1ij\right)$ and $\left(1ik\right)$ belong to the generated group, and hence $\left(1ij\right)^{-1}\left(1ik\right)=\left(1ji\right)\left(1ik\right)=\left(ikj\right)$. Since $\left(ikj\right)=\left(ijk\right)^{-1}$, we have $\left(ijk\right)$ in the generated group.

Hence all 3-cycles belong to $\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$, so $A_n\subseteq\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$. Conversely, each generator $\left(12k\right)$ is a 3-cycle, hence an even permutation (Even and Odd Permutations, the Alternating Group), so it belongs to $A_n$; the reverse inclusion holds. Therefore $A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$. $\blacksquare$

## 1.6-6

Prove that the nontrivial normal subgroups of $S_n$ are $A_n$ or $K_4$ (when $n=4$).

### Solution to 1.6-6

Let $N\triangleleft S_n$, $N\ne\left\{e\right\}$, $N\ne S_n$.

**Case $n\ge5$.** By **Theorem 1.6.9 (Simplicity of the Alternating Group)**, $A_n$ is simple. Since $N\triangleleft S_n$ and $A_n\triangleleft S_n$ (by Even and Odd Permutations, the Alternating Group), the intersection $N\cap A_n\triangleleft A_n$, so by the simplicity of $A_n$ we have $N\cap A_n=\left\{e\right\}$ or $A_n$.

If $N\cap A_n=A_n$, then $A_n\subseteq N$. Since $\left|A_n\right|=\frac{n!}{2}$, the index of $A_n$ in $S_n$ is $2$ (Even and Odd Permutations, the Alternating Group), so any subgroup containing $A_n$ is $A_n$ or $S_n$; since $N\ne S_n$, we have $N=A_n$.

If $N\cap A_n=\left\{e\right\}$, then for any $x,y\in N\setminus\left\{e\right\}$, since $x,y$ are both odd permutations, $xy$ is an even permutation, so $xy\in N\cap A_n=\left\{e\right\}$, hence $y=x^{-1}$, i.e. $\left|N\right|\le2$, and the non-identity element of $N$ has order two. By A Normal Subgroup Is a Union of Conjugacy Classes, $N$ is a union of conjugacy classes; since the center of $S_n$ is trivial for $n\ge3$ (The Center and Inner Automorphisms of a Group), the conjugacy class of the non-identity element $x\ne e$ has size greater than $1$, contradicting $\left|N\right|\le2$. Hence $N\cap A_n=\left\{e\right\}$ is impossible.

Therefore, for $n\ge5$, the only nontrivial normal subgroup of $S_n$ is $A_n$.

**Case $n=4$.** $\left|S_4\right|=24$ and $\left|A_4\right|=12$, with $A_4\triangleleft S_4$. By The Conjugacy Classes of $S_4$, the conjugacy class sizes of $S_4$ are $1,6,3,8,6$; by A Normal Subgroup Is a Union of Conjugacy Classes and **Theorem 1.2.22 (Lagrange's Theorem)**, the order of a normal subgroup must be a sum of some conjugacy class sizes and must divide $24$, so the possible orders are $1,4,12,24$, corresponding to the normal subgroups $\left\{e\right\}$, $K_4$, $A_4$, $S_4$. Hence the nontrivial normal subgroups are $A_4$ and $K_4$.

**Case $n=3$.** $\left|S_3\right|=6$ and $\left|A_3\right|=3$, with $A_3\triangleleft S_3$ of index $2$. By A Normal Subgroup Is a Union of Conjugacy Classes, the conjugacy class sizes of $S_3$ are $1,3,2$, so the possible orders of a normal subgroup are $1,3,6$; hence the normal subgroups are $\left\{e\right\},A_3,S_3$, and the nontrivial one is $A_3$.

**Case $n\le2$.** $S_n$ has no nontrivial normal subgroups.

In summary, the nontrivial normal subgroups of $S_n$ are $A_n$ (for all $n\ge3$) and $K_4$ when $n=4$. $\blacksquare$

## 1.6-11

Let $\left|G\right|=2n$, where $n$ is odd. Prove that $G$ has a normal subgroup of index $2$.

### Solution to 1.6-11

**Step 1: construct the group homomorphism $\psi:G\to\left\{1,-1\right\}$.** By **Theorem 1.4.10 (Cayley's Theorem)**, the left regular representation $\lambda:G\to S_G$, $g\mapsto L_g$ (where $L_g\left(x\right)=gx$) is a monomorphism; regard $S_G$ as $S_{2n}$ (since $\left|G\right|=2n$). By **Example 1.4.17** and The Sign Homomorphism, the sign homomorphism $\mathrm{sgn}:S_{2n}\to\left\{1,-1\right\}$ is a group homomorphism. The composition $\psi=\mathrm{sgn}\circ\lambda:G\to\left\{1,-1\right\}$ is a group homomorphism.

**Step 2: prove that $\psi$ is surjective.** By A Finite Group of Even Order Has an Element of Order Two, $G$ contains an element $a$ of order two (since $\left|G\right|=2n$ is even). Then $\lambda\left(a\right)=L_a$, and for any $x\in G$, $L_a^2\left(x\right)=a^2x=x$, so $L_a$ is an involution; moreover, since $a\ne e$, if $L_a\left(x\right)=x$, i.e. $ax=x$, then $a=e$, a contradiction, so $L_a$ has no fixed points. Hence $L_a$ is a product of $n$ disjoint transpositions on the $2n$ letters of $G$, and by The Sign Homomorphism, $\mathrm{sgn}\left(L_a\right)=\left(-1\right)^{n}=-1$ (since $n$ is odd). Therefore $\psi\left(a\right)=-1$, while $\psi\left(e\right)=1$, so $\psi:G\to\left\{1,-1\right\}$ is a surjective homomorphism.

**Step 3: take the kernel to obtain a normal subgroup of index $2$.** Let $H=\ker\psi$. By **Lemma 1.4.13**, $H\triangleleft G$. By **Theorem 1.4.19 (Fundamental Theorem of Group Homomorphisms)**, $G/H\cong\left\{1,-1\right\}$, so $\left|G/H\right|=2$, i.e. $\left[G:H\right]=2$. Hence $G$ has a normal subgroup $H$ of index $2$. $\blacksquare$
