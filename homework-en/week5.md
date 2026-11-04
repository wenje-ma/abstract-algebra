# week5

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

> **Theorem 1.4.23 (3) (Second Isomorphism Theorem)**
> 
> Let $G$ be a group, $N\triangleleft G$, and $H< G$. Then $HN/N\cong H/\left(H\cap N\right)$.

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

> **Definition 1.7.9 (Subnormal Series and Composition Series)**
> 
> A sequence of subgroups $G=G_1\trianglerighteq G_2\trianglerighteq\cdots\trianglerighteq G_t\trianglerighteq G_{t+1}=\left\{e\right\}$ of a group $G$ is called a subnormal series if $G_{i+1}\trianglelefteq G_i$ for $i=1,\cdots,t$; the quotient $G_i/G_{i+1}$ is called a factor of this series. If all factors $G_i/G_{i+1}$ are simple groups, then this subnormal series is called a composition series of $G$, and the $G_i/G_{i+1}$ are called composition factors of $G$.

> **Definition 1.7.12 (Isomorphic Series)**
> 
> Two subnormal series $G=G_1\supset G_2\supset\cdots\supset G_t=\left\{e\right\}$ and $G=H_1\supset H_2\supset\cdots\supset H_s=\left\{e\right\}$ of a group $G$ are called isomorphic if there is a bijection between the two sets of factors such that the corresponding factors are isomorphic.

> **Theorem 1.7.13 (Jordan-Holder Theorem)**
> 
> If a group $G$ has a composition series, then any two composition series of $G$ are isomorphic. In particular, any two principal series of $G$ are isomorphic.

> **Lemma 1.8.3 (Properties of Commutators)**
> 
> (1) $\left[g,h\right]^{-1}=\left[h,g\right]$, and $\left[g,h\right]=e$ if and only if $gh=hg$. (2) If $\varphi:G\to H$ is a group homomorphism, then $\varphi\left(\left[g,h\right]\right)=\left[\varphi\left(g\right),\varphi\left(h\right)\right]$; in particular, if $\varphi\in\mathrm{Aut}\left(G\right)$, then $\varphi\left(\left[g,h\right]\right)=\left[\varphi\left(g\right),\varphi\left(h\right)\right]$.

> **Lemma 1.8.5**
> 
> Let $N\triangleleft G$. Then $G/N$ is an Abelian group if and only if $\left[G,G\right]\subseteq N$. In particular, $G/\left[G,G\right]$ is an Abelian group.

> **Definition 1.8.7 (Solvable and Nilpotent Groups)**
> 
> In a group $G$, define inductively the derived series $G^{\left(0\right)}=G$, $G^{\left(k+1\right)}=\left[G^{\left(k\right)},G^{\left(k\right)}\right]$. If there exists $t$ with $G^{\left(t\right)}=\left\{e\right\}$, then $G$ is called solvable. Define inductively the lower central series $G^{1}=G$, $G^{k+1}=\left[G,G^{k}\right]$; if there exists $t$ with $G^{t}=\left\{e\right\}$, then $G$ is called nilpotent.

> **Lemma 1.8.8 (Heredity of Solvability)**
> 
> Subgroups and quotient groups of a solvable group are solvable; conversely, if $N\trianglelefteq G$ and both $N$ and $G/N$ are solvable, then $G$ is solvable.

> **Definition 1.9.1 (Group Action)**
> 
> Let $G$ be a group and $X$ a nonempty set. If a map $f:G\times X\to X$ satisfies $f\left(e,x\right)=x$ and $f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right)$, then $f$ is said to determine an action of $G$ on $X$, written $f\left(g,x\right)=gx$.

> **Definition 1.9.7 (Transitive and Effective Actions)**
> 
> If for any $x,y\in X$ there exists $g\in G$ with $gx=y$, the action of $G$ on $X$ is called transitive and $X$ is called a homogeneous space of $G$. If $gx=x$ for all $x\in X$ implies $g=e$, the action is called effective. If $gx=x$ for all $g\in G$ and $x\in X$, the action is called trivial.

> **Definition 1.9.9 (Orbits and Stabilizers)**
> 
> Let $G$ act on $X$ and $x\in X$. The set $O_x=\left\{gx\mid g\in G\right\}$ is called the orbit of $x$. The set $F_x=\left\{g\in G\mid gx=x\right\}$ is called the stabilizer (isotropy subgroup) of $x$.

> **Corollary 1.9.15 (Orbit-Stabilizer Theorem)**
> 
> Let a group $G$ act on $X$ and $x\in X$. Then $\left|O_x\right|=\left|G/F_x\right|=\left[G:F_x\right]$; hence $\left|O_x\right|\mid\left|G\right|$.

## 1.6-14

Prove that $\mathrm{Aut}\left(S_n\right)\cong S_n$ when $n\ne2,6$. Also find $\mathrm{Aut}\left(S_2\right)$ and $\mathrm{Aut}\left(S_6\right)$.

### Solution to 1.6-14

**First prove that $\mathrm{Aut}\left(S_n\right)\cong S_n$ for $n\ne2,6$.** By The Center and Inner Automorphisms of a Group, $\mathrm{Inn}\left(S_n\right)\cong S_n/C\left(S_n\right)$, and for $n\ge3$ we have $C\left(S_n\right)=\left\{e\right\}$, so $\mathrm{Inn}\left(S_n\right)\cong S_n$. It therefore suffices to prove $\mathrm{Aut}\left(S_n\right)=\mathrm{Inn}\left(S_n\right)$, i.e. every automorphism is inner.

Let $\varphi\in\mathrm{Aut}\left(S_n\right)$. An automorphism preserves the order of elements, so involutions are mapped to involutions. By Centralizers of Transpositions and Recognizing Transpositions, for $n\ne6$ the transpositions form the unique conjugacy class of involutions of this type (with centralizer size $2\left(n-2\right)!$), and an automorphism preserves conjugacy classes and centralizer sizes, so $\varphi$ maps transpositions to transpositions.

Let $\varphi\left(12\right)=\left(ab\right)$. Compose $\varphi$ with the inner automorphism $\mathrm{Ad}_{\sigma}$, where $\sigma\in S_n$ satisfies $\sigma\left(a\right)=1$, $\sigma\left(b\right)=2$; then $\mathrm{Ad}_{\sigma}\varphi\left(12\right)=\left(\sigma\left(a\right)\sigma\left(b\right)\right)=\left(12\right)$. Hence we may assume $\varphi\left(12\right)=\left(12\right)$.

For $k=3,\cdots,n$, since $\left(12\right)\left(1k\right)=\left(1k2\right)$ is a 3-cycle of order $3$, the transposition $\varphi\left(1k\right)$ must have product with $\varphi\left(12\right)=\left(12\right)$ being a 3-cycle; hence $\varphi\left(1k\right)$ must share exactly one letter with $\left(12\right)$, i.e. $\varphi\left(1k\right)=\left(1,j_k\right)$ or $\left(2,j_k\right)$ ($j_k\ne1,2$). If for some $k$ we have $\varphi\left(1k\right)=\left(2,j_k\right)$, composing with the inner automorphism $\mathrm{Ad}_{\left(12\right)}$ (which fixes $\left(12\right)$ and swaps the letters $1,2$) lets us uniformly write each $\varphi\left(1k\right)$ in the form $\left(1,\sigma\left(k\right)\right)$, where $\sigma\in S_{n-1}$ is a permutation of $\left\{3,\cdots,n\right\}$ (fixing $1,2$). Hence $\varphi$ acts on the generators $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ exactly as the inner automorphism $\mathrm{Ad}_{\sigma}$ does.

By **Exercise 1.6-5, Part 1**, $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ generate $S_n$, so $\varphi$ and $\mathrm{Ad}_{\sigma}$ agree on the generators and hence on all of $S_n$; thus $\varphi=\mathrm{Ad}_{\sigma}\in\mathrm{Inn}\left(S_n\right)$.

The above argument fails for $n=6$, because $S_6$ has outer automorphisms (by Centralizers of Transpositions and Recognizing Transpositions and The Outer Automorphisms of $S_6$). Hence, for $n\ne2,6$,

$$
\mathrm{Aut}\left(S_n\right)=\mathrm{Inn}\left(S_n\right)\cong S_n.
$$

**Find $\mathrm{Aut}\left(S_2\right)$.** $S_2=\left\{e,\left(12\right)\right\}$ is a cyclic group of order two, and an automorphism must fix the identity $e$, so $\mathrm{Aut}\left(S_2\right)=\left\{\mathrm{id}\right\}$ is the trivial group.

**Find $\mathrm{Aut}\left(S_6\right)$.** By The Outer Automorphisms of $S_6$, $\mathrm{Out}\left(S_6\right)\cong\mathbb Z_2$ and $\left|\mathrm{Inn}\left(S_6\right)\right|=\left|S_6\right|=720$ (since $C\left(S_6\right)=\left\{e\right\}$), so $\left|\mathrm{Aut}\left(S_6\right)\right|=\left|\mathrm{Out}\left(S_6\right)\right|\cdot\left|\mathrm{Inn}\left(S_6\right)\right|=2\cdot720=1440$. $\blacksquare$

## 1.7-11

Let

$$
G=G_1\triangleright G_2\triangleright\cdots\triangleright G_t=\left\{e\right\}
$$

and

$$
G=H_1\triangleright H_2\triangleright\cdots\triangleright H_s=\left\{e\right\}
$$

be two composition series of $G$, with $G_2\ne H_2$. Let $K_3=G_2\cap H_2$. Take any composition series $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ of $K_3$. Prove that:

(1) both $G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ and $G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ are also composition series of $G$;

(2) the above four composition series of $G$ are equivalent to one another.

### Solution to 1.7-11

**Step 1: prove that $G_2H_2=G$.** Since $H_2\triangleleft G$, by Surjective Homomorphisms Preserve Normal Subgroups, the image $\pi\left(H_2\right)$ under the natural homomorphism $\pi:G\to G/G_2$ is a normal subgroup of $G/G_2$. Moreover $\pi\left(H_2\right)=\left\{hG_2\mid h\in H_2\right\}=\left(G_2H_2\right)/G_2$ (since $G_2\subseteq G_2H_2$), so $\left(G_2H_2\right)/G_2\triangleleft G/G_2$. Since $G/G_2$ is a composition factor and hence simple, $\left(G_2H_2\right)/G_2$ must be trivial or all of $G/G_2$, i.e. $G_2H_2=G_2$ or $G$.

Similarly, since $G_2\triangleleft G$, the image $\pi'\left(G_2\right)=\left(G_2H_2\right)/H_2$ under the natural homomorphism $\pi':G\to G/H_2$ is a normal subgroup of $G/H_2$; since $G/H_2$ is simple, $G_2H_2=H_2$ or $G$.

**Claim: $G_2H_2\ne G_2$.** If $G_2H_2=G_2$, then $H_2\subseteq G_2$. From the previous paragraph $G_2H_2\in\left\{H_2,G\right\}$, i.e. $G_2=H_2$ or $G_2=G$; the former contradicts $G_2\ne H_2$, and the latter contradicts the fact that $G_2$ is a proper subgroup of $G$ (since $G/G_2$ is a nontrivial simple group). Hence $G_2H_2\ne G_2$.

**Claim: $G_2H_2\ne H_2$.** If $G_2H_2=H_2$, then $G_2\subseteq H_2$. From $G_2H_2\in\left\{G_2,G\right\}$, we get $H_2=G_2$ or $H_2=G$; the former contradicts $G_2\ne H_2$, and the latter contradicts the fact that $H_2$ is a proper subgroup. Hence $G_2H_2\ne H_2$.

Therefore the only possibility is $G_2H_2=G$.

**Step for (1): prove that both refined series are composition series.** By **Theorem 1.4.23 (3) (Second Isomorphism Theorem)**, taking $H=G_2$ and $N=H_2$, we get

$$
G_2/K_3=G_2/\left(G_2\cap H_2\right)\cong G_2H_2/H_2=G/H_2,
$$

and $G/H_2$ is a composition factor, hence simple; so $G_2/K_3$ is simple.

Similarly, by **Theorem 1.4.23 (3) (Second Isomorphism Theorem)**, taking $H=H_2$ and $N=G_2$, we get

$$
H_2/K_3=H_2/\left(G_2\cap H_2\right)\cong G_2H_2/G_2=G/G_2,
$$

which is also simple.

Moreover $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ is a composition series of $K_3$, so each $K_i/K_{i+1}$ ($i=3,\cdots,r-1$) is simple. Hence all factors $G/G_2$, $G_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ of the series

$$
G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

are simple; and $G_2\triangleright K_3$ is a valid subnormal step ($K_3=G_2\cap H_2$, $H_2\triangleleft G$, so $K_3\triangleleft G_2$). By **Definition 1.7.9 (Subnormal Series and Composition Series)**, it is a composition series of $G$.

Similarly, all factors $G/H_2$, $H_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ of the series

$$
G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

are simple, so by **Definition 1.7.9 (Subnormal Series and Composition Series)** it is also a composition series of $G$.

**Step for (2): prove that the four composition series are equivalent.** Write the four composition series as

$$
\begin{aligned}
S_1&:G\triangleright G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\},\\
S_2&:G\triangleright H_2\triangleright H_3\triangleright\cdots\triangleright H_s=\left\{e\right\},\\
S_3&:G\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\},\\
S_4&:G\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}.
\end{aligned}
$$

**First prove that $S_3$ and $S_4$ are isomorphic.** The factors of $S_3$ are $G/G_2$, $G_2/K_3\cong G/H_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$; the factors of $S_4$ are $G/H_2$, $H_2/K_3\cong G/G_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$. As multisets the two families differ only in the first two entries: $G/G_2$ and $G/H_2$ are interchanged, and all remaining factors are identical. Hence by **Definition 1.7.12 (Isomorphic Series)**, $S_3$ and $S_4$ are isomorphic.

**Next prove that $S_1$ and $S_3$ are isomorphic.** The first factors of $S_1$ and $S_3$ are both $G/G_2$. After removing the first term, the two tails

$$
G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\}
\quad\text{and}\quad
G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

are both composition series of $G_2$. By **Theorem 1.7.13 (Jordan-Holder Theorem)**, these two composition series of the group $G_2$ are isomorphic. After adding back their common first factor $G/G_2$, by **Definition 1.7.12 (Isomorphic Series)**, $S_1$ and $S_3$ are isomorphic.

**Similarly prove that $S_2$ and $S_4$ are isomorphic.** The first factors of $S_2$ and $S_4$ are both $G/H_2$; the tails $H_2\triangleright H_3\triangleright\cdots\triangleright\left\{e\right\}$ and $H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright\left\{e\right\}$ are both composition series of $H_2$, hence isomorphic by **Theorem 1.7.13 (Jordan-Holder Theorem)**; after adding back the common first factor $G/H_2$, $S_2$ and $S_4$ are isomorphic.

In summary, $S_1\cong S_3\cong S_4\cong S_2$, so the four composition series are equivalent. $\blacksquare$

## 1.8-12

Let $G$ be a solvable group of order $n$, and let $B$ be the set of all invertible complex upper triangular matrices. Prove that $G$ is isomorphic to a subgroup of $B$. If $G$ is a nilpotent group of order $n$ and $N$ is the set of all complex upper triangular matrices whose diagonal entries are all $1$, is $G$ isomorphic to a subgroup of $N$?

### Solution to 1.8-12

**First prove the first part.** By Faithful Representations via Permutation Matrices and **Theorem 1.4.10 (Cayley's Theorem)**, the solvable group $G$ of order $n$ is isomorphic to a subgroup of $\mathrm{GL}\left(V\right)$, where $V=\mathbb C^{n}$; by Solvability Is Preserved under Isomorphism, we may assume $G$ itself is a solvable subgroup of $\mathrm{GL}\left(V\right)$. We now induct on $\dim V$ to prove that $G$ can be simultaneously triangularized, i.e. $G$ is conjugate to a subgroup of the upper triangular matrix group $B$.

**Base case**: When $\dim V=1$, $\mathrm{GL}\left(V\right)\cong\mathbb C^{*}$ is itself the upper triangular matrix group, so the conclusion holds.

**Inductive step**: Let $\dim V=n> 1$. By **Definition 1.8.7 (Solvable and Nilpotent Groups)**, the commutator subgroup $G^{\prime}=\left[G,G\right]$ is a proper normal subgroup of $G$; by **Lemma 1.8.5**, $G/G^{\prime}$ is an Abelian group. By **Lemma 1.8.8 (Heredity of Solvability)**, $G^{\prime}$ is solvable. By the induction hypothesis (repeatedly applying the base-case result to $G^{\prime}$ acting on $V$), $G^{\prime}$ has a common eigenvector in $V$; let $\lambda$ be a character of $G^{\prime}$, and write its eigenspace as

$$
V_{\lambda}=\left\{v\in V\mid\sigma v=\lambda\left(\sigma\right)v,\ \forall\sigma\in G^{\prime}\right\}.
$$

Since $G^{\prime}\trianglelefteq G$, for any $\tau\in G$, $\sigma\in G^{\prime}$ and $v\in V_{\lambda}$, by **Lemma 1.8.3 (Properties of Commutators)** (2) (taking $\varphi=\mathrm{Ad}_{\tau}$), we have $\tau\sigma\tau^{-1}\in G^{\prime}$, and

$$
\sigma\left(\tau v\right)=\tau\left(\tau^{-1}\sigma\tau\right)v=\tau\lambda\left(\tau^{-1}\sigma\tau\right)v=\lambda\left(\tau^{-1}\sigma\tau\right)\tau v,
$$

so by Characters and Common Eigenspaces, $\tau v\in V_{\lambda^{\tau}}$, where $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$. Since $G/G^{\prime}$ is an Abelian group, the conjugacy action of $G$ on the set of characters of $G^{\prime}$ has a finite orbit; taking the sum of the eigenspaces corresponding to one orbit yields a nonzero $G$-invariant subspace $W$.

On $W$, since $G/G^{\prime}$ is Abelian while $G^{\prime}$ acts by scalars on $W$, the image of $G$ in $\mathrm{GL}\left(W\right)$ is abelianized; by Common Eigenvectors of Commuting Families of Linear Transformations, $W$ contains a common eigenvector of $G$, i.e. there exists a one-dimensional $G$-invariant subspace $L\subseteq V$.

Hence $G$ induces a solvable subgroup on the quotient space $V/L$ (by Solvability Is Preserved under Isomorphism and the solvability of quotients, or **Lemma 1.8.8 (Heredity of Solvability)**); by the induction hypothesis, $G$ can be triangularized on $V/L$. Thus we may choose a basis of $V$ in which $L$ is spanned by the first basis vector, and the triangularization of the quotient gives an upper triangular matrix representation of $G$ on $V$. Hence $G$ is conjugate to a subgroup of $B$, i.e. $G$ is isomorphic to a subgroup of $B$. $\blacksquare$

**Then answer the second part.** The answer is no: a nontrivial finite nilpotent group $G$ cannot be isomorphic to a subgroup of $N$.

Indeed, let $A\in N$, i.e. $A$ is a complex upper triangular matrix whose diagonal entries are all $1$; then $A=I+M$, where $M$ is strictly upper triangular. By Nilpotent Matrices and Elements of Finite Order, $M$ is nilpotent, and if $A$ has finite order then $M=0$, i.e. $A=I$. This shows that the only element of finite order in $N$ is the identity matrix $I$ itself.

Therefore the only finite subgroup of $N$ is the trivial group $\left\{I\right\}$. But $G$ is a finite nontrivial nilpotent group, and by Elements of a Finite Group Have Finite Order, $G$ contains a non-identity element of finite order; hence $G$ cannot be isomorphic to a subgroup of $N$. $\blacksquare$

## 1.9-4

(1) Let $P^{n-1}\left(\mathbb R\right)$ denote the set of all $1$-dimensional subspaces of $\mathbb R^n$, called the real projective space. For any $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W\in P^{n-1}\left(\mathbb R\right)$, $\rho\left(W\right)$ is again a $1$-dimensional subspace. Verify that this is a transitive action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$, and find the stabilizer.

(2) Let $\mathrm{Gr}\left(k,n\right)$ denote the set of all $k$-dimensional subspaces of $\mathbb R^n$, called the Grassmannian. For any $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W\in\mathrm{Gr}\left(k,n\right)$, $\rho\left(W\right)$ is again a $k$-dimensional subspace. Verify that this is a transitive action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $\mathrm{Gr}\left(k,n\right)$, and find the stabilizer.

(3) Consider the actions of $\mathrm{SL}\left(n,\mathbb R\right)$, $O\left(n\right)$, $\mathrm{SO}\left(n\right)$ on the above sets and determine their transitivity.

### Solution to 1.9-4

**Part (1): the action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$.** By Linear Maps Preserve Dimension of Subspaces, for $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and a $1$-dimensional subspace $W=\mathbb Rv$, $\rho\left(W\right)$ is again a $1$-dimensional subspace. For $\rho,\tau\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W=\mathbb Rv$,

$$
\rho\left(\tau\left(W\right)\right)=\rho\left(\tau\left(\mathbb Rv\right)\right)=\rho\left(\mathbb R\tau\left(v\right)\right)=\mathbb R\rho\left(\tau\left(v\right)\right)=\left(\rho\tau\right)\left(W\right),
$$

and the identity matrix $I$ satisfies $I\left(W\right)=W$. By **Definition 1.9.1 (Group Action)**, this is an action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$.

**Transitivity**: Take any two lines $W_1=\mathbb Rv$, $W_2=\mathbb Rw$ ($v,w\ne0$). By Linear Maps Preserve Dimension of Subspaces, there exists an invertible matrix $\rho$ with $\rho v=w$, so $\rho\left(W_1\right)=W_2$. By **Definition 1.9.7 (Transitive and Effective Actions)**, the action is transitive.

**Stabilizer**: Take $W_0=\mathbb Re_1$, where $e_1=\left(1,0,\cdots,0\right)^{\top}$. The condition $\rho\left(W_0\right)=W_0$ is equivalent to $\rho e_1\in\mathbb Re_1$, i.e. the first column of $\rho$ is $\left(a,0,\cdots,0\right)^{\top}$ with $a\ne0$. Hence by **Definition 1.9.9 (Orbits and Stabilizers)**, the stabilizer of $W_0$ is

$$
F_{W_0}=\left\{\begin{bmatrix}a & *\\0 & A\end{bmatrix}\;\middle|\;a\in\mathbb R^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb R\right)\right\}.
$$

**Part (2): the action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $\mathrm{Gr}\left(k,n\right)$.** Similarly $\rho\left(\tau\left(W\right)\right)=\left(\rho\tau\right)\left(W\right)$ and $I\left(W\right)=W$, so by **Definition 1.9.1 (Group Action)** this is an action.

**Transitivity**: Take two $k$-dimensional subspaces $W_1,W_2$ with bases $\left\{v_1,\cdots,v_k\right\}$ and $\left\{w_1,\cdots,w_k\right\}$; extend them to bases of $\mathbb R^n$. By Linear Maps Preserve Dimension of Subspaces, define an invertible linear map $\rho$ with $\rho v_i=w_i$ ($i=1,\cdots,k$); then $\rho\left(W_1\right)=W_2$. By **Definition 1.9.7 (Transitive and Effective Actions)**, the action is transitive.

**Stabilizer**: Take $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$. The condition $\rho\left(W_0\right)=W_0$ is equivalent to $\rho$ mapping each $e_i$ ($i\le k$) back into $W_0$, i.e. the first $k$ columns of $\rho$ have zero entries in rows $k+1,\cdots,n$, namely $\rho$ is a block upper triangular matrix. Hence by **Definition 1.9.9 (Orbits and Stabilizers)**, the stabilizer is

$$
F_{W_0}=\left\{\begin{bmatrix}A & B\\0 & C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb R\right),\;C\in\mathrm{GL}\left(n-k,\mathbb R\right),\;B\in\mathbb R^{k\times\left(n-k\right)}\right\}.
$$

**Part (3): determine transitivity.** The action of $\mathrm{SL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$ and on $\mathrm{Gr}\left(k,n\right)$ is transitive: in the map $\rho$ constructed in Parts (1)(2), if its determinant is not $1$, multiply the last row by a nonzero scalar to adjust the determinant to $1$, without changing the action on subspaces.

$O\left(n\right)$ acts transitively on $P^{n-1}\left(\mathbb R\right)$: by Orthogonal and Unitary Transformations, any two unit lines can be related by an orthogonal transformation. $O\left(n\right)$ also acts transitively on $\mathrm{Gr}\left(k,n\right)$: bases of two $k$-dimensional subspaces can be extended to two orthonormal bases, which are related by an orthogonal map by Orthogonal and Unitary Transformations.

$\mathrm{SO}\left(n\right)$ acts transitively on $P^{n-1}\left(\mathbb R\right)$ when $n\ge3$ (by a suitable rotation one can send any direction to any direction while keeping determinant $1$); it also acts transitively on $\mathrm{Gr}\left(k,n\right)$ when $n\ge3$. $\blacksquare$
