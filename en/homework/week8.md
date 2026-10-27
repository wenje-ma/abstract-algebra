# week8

> **Basic Knowledge: Faithful Representations via Permutation Matrices**<br>Let $G$ be a group of order $n$. By Cayley's theorem, left translation gives a monomorphism $G\to S_G\cong S_n$; embedding through permutation matrices, $G$ is isomorphic to a subgroup of $\mathrm{GL}\left(n,\mathbb C\right)$, so we may regard $G$ as a group of linear transformations of $V=\mathbb C^{n}$.

> **Basic Knowledge: Solvability Is Preserved under Isomorphism**<br>If two groups are isomorphic, then they are solvable or non-solvable simultaneously; the same holds for nilpotency.

> **Basic Knowledge: Characters and Common Eigenspaces**<br>Let $N\triangleleft G$ act on $V$, and let $v\in V$ be a common eigenvector of $N$ with character $\lambda$, i.e. $\sigma v=\lambda\left(\sigma\right)v$ for all $\sigma\in N$. Then for any $\tau\in G$, $\tau v\in V_{\lambda^{\tau}}$, where $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$ and $V_{\lambda}=\left\{v\mid\sigma v=\lambda\left(\sigma\right)v,\ \forall\sigma\in N\right\}$.

> **Basic Knowledge: Common Eigenvectors of Commuting Families of Linear Transformations**<br>A family of commuting linear transformations over $\mathbb C$ (i.e. a linear representation of an Abelian group) can be simultaneously diagonalized; in particular it has a common eigenvector.

> **Basic Knowledge: Nilpotent Matrices and Elements of Finite Order**<br>If $M$ is a strictly upper triangular $n\times n$ matrix, then $M$ is nilpotent, i.e. there exists $r$ with $M^{r}=0$. If $A=I+M$ has finite order, i.e. there exists a positive integer $k$ with $A^{k}=I$, then $M=0$ and hence $A=I$: since $\left(I+M\right)^{k}-I=kM+\binom{k}{2}M^{2}+\cdots+M^{k}=0$, let $s$ be the smallest positive integer with $M^{s}\ne0$; the lowest-degree term on the left is $kM^{s}$, and since $k\ne0$ is invertible in $\mathbb C$, we get $M^{s}=0$, a contradiction.

> **Basic Knowledge: Elements of a Finite Group Have Finite Order**<br>For any element $g$ of a finite group $G$, there exists a positive integer $k$ with $g^{k}=e$, i.e. $g$ has finite order.

> **Theorem 1.4.10 (Cayley's Theorem)**<br>Every group $G$ is isomorphic to a subgroup of the symmetric group $S_G$; in fact the map $L:G\to L_G$, $a\mapsto L_a$ is a monomorphism.

> **Lemma 1.8.3 (Properties of Commutators)**<br>(1) $\left[g,h\right]^{-1}=\left[h,g\right]$, and $\left[g,h\right]=e$ if and only if $gh=hg$. (2) If $\varphi:G\to H$ is a group homomorphism, then $\varphi\left(\left[g,h\right]\right)=\left[\varphi\left(g\right),\varphi\left(h\right)\right]$; in particular, if $\varphi\in\mathrm{Aut}\left(G\right)$, then $\varphi\left(\left[g,h\right]\right)=\left[\varphi\left(g\right),\varphi\left(h\right)\right]$.

> **Lemma 1.8.5**<br>Let $N\triangleleft G$. Then $G/N$ is an Abelian group if and only if $\left[G,G\right]\subseteq N$. In particular, $G/\left[G,G\right]$ is an Abelian group.

> **Definition 1.8.7 (Solvable and Nilpotent Groups)**<br>In a group $G$, define inductively the derived series $G^{\left(0\right)}=G$, $G^{\left(k+1\right)}=\left[G^{\left(k\right)},G^{\left(k\right)}\right]$. If there exists $t$ with $G^{\left(t\right)}=\left\{e\right\}$, then $G$ is called solvable. Define inductively the lower central series $G^{1}=G$, $G^{k+1}=\left[G,G^{k}\right]$; if there exists $t$ with $G^{t}=\left\{e\right\}$, then $G$ is called nilpotent.

> **Lemma 1.8.8 (Heredity of Solvability)**<br>Subgroups and quotient groups of a solvable group are solvable; conversely, if $N\trianglelefteq G$ and both $N$ and $G/N$ are solvable, then $G$ is solvable.

---

## 1.8-12

Let $G$ be a solvable group of order $n$, and let $B$ be the set of all invertible complex upper triangular matrices. Prove that $G$ is isomorphic to a subgroup of $B$. If $G$ is a nilpotent group of order $n$ and $N$ is the set of all complex upper triangular matrices whose diagonal entries are all $1$, is $G$ isomorphic to a subgroup of $N$?

### Solution 1.8-12

**First prove the first part.** By **Basic Knowledge: Faithful Representations via Permutation Matrices** and **Theorem 1.4.10 (Cayley's Theorem)**, the solvable group $G$ of order $n$ is isomorphic to a subgroup of $\mathrm{GL}\left(V\right)$, where $V=\mathbb C^{n}$; by **Basic Knowledge: Solvability Is Preserved under Isomorphism**, we may assume $G$ itself is a solvable subgroup of $\mathrm{GL}\left(V\right)$. We now induct on $\dim V$ to prove that $G$ can be simultaneously triangularized, i.e. $G$ is conjugate to a subgroup of the upper triangular matrix group $B$.

**Base case**: When $\dim V=1$, $\mathrm{GL}\left(V\right)\cong\mathbb C^{*}$ is itself the upper triangular matrix group, so the conclusion holds.

**Inductive step**: Let $\dim V=n>1$. By **Definition 1.8.7 (Solvable and Nilpotent Groups)**, the commutator subgroup $G^{\prime}=\left[G,G\right]$ is a proper normal subgroup of $G$; by **Lemma 1.8.5**, $G/G^{\prime}$ is an Abelian group. By **Lemma 1.8.8 (Heredity of Solvability)**, $G^{\prime}$ is solvable. By the induction hypothesis (repeatedly applying the base-case result to $G^{\prime}$ acting on $V$), $G^{\prime}$ has a common eigenvector in $V$; let $\lambda$ be a character of $G^{\prime}$, and write its eigenspace as

$$
V_{\lambda}=\left\{v\in V\mid\sigma v=\lambda\left(\sigma\right)v,\ \forall\sigma\in G^{\prime}\right\}.
$$

Since $G^{\prime}\trianglelefteq G$, for any $\tau\in G$, $\sigma\in G^{\prime}$ and $v\in V_{\lambda}$, by **Lemma 1.8.3 (Properties of Commutators)** (2) (taking $\varphi=\mathrm{Ad}_{\tau}$), we have $\tau\sigma\tau^{-1}\in G^{\prime}$, and

$$
\sigma\left(\tau v\right)=\tau\left(\tau^{-1}\sigma\tau\right)v=\tau\lambda\left(\tau^{-1}\sigma\tau\right)v=\lambda\left(\tau^{-1}\sigma\tau\right)\tau v,
$$

so by **Basic Knowledge: Characters and Common Eigenspaces**, $\tau v\in V_{\lambda^{\tau}}$, where $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$. Since $G/G^{\prime}$ is an Abelian group, the conjugacy action of $G$ on the set of characters of $G^{\prime}$ has a finite orbit; taking the sum of the eigenspaces corresponding to one orbit yields a nonzero $G$-invariant subspace $W$.

On $W$, since $G/G^{\prime}$ is Abelian while $G^{\prime}$ acts by scalars on $W$, the image of $G$ in $\mathrm{GL}\left(W\right)$ is abelianized; by **Basic Knowledge: Common Eigenvectors of Commuting Families of Linear Transformations**, $W$ contains a common eigenvector of $G$, i.e. there exists a one-dimensional $G$-invariant subspace $L\subseteq V$.

Hence $G$ induces a solvable subgroup on the quotient space $V/L$ (by **Basic Knowledge: Solvability Is Preserved under Isomorphism** and the solvability of quotients, or **Lemma 1.8.8 (Heredity of Solvability)**); by the induction hypothesis, $G$ can be triangularized on $V/L$. Thus we may choose a basis of $V$ in which $L$ is spanned by the first basis vector, and the triangularization of the quotient gives an upper triangular matrix representation of $G$ on $V$. Hence $G$ is conjugate to a subgroup of $B$, i.e. $G$ is isomorphic to a subgroup of $B$. $\blacksquare$

**Then answer the second part.** The answer is no: a nontrivial finite nilpotent group $G$ cannot be isomorphic to a subgroup of $N$.

Indeed, let $A\in N$, i.e. $A$ is a complex upper triangular matrix whose diagonal entries are all $1$; then $A=I+M$, where $M$ is strictly upper triangular. By **Basic Knowledge: Nilpotent Matrices and Elements of Finite Order**, $M$ is nilpotent, and if $A$ has finite order then $M=0$, i.e. $A=I$. This shows that the only element of finite order in $N$ is the identity matrix $I$ itself.

Therefore the only finite subgroup of $N$ is the trivial group $\left\{I\right\}$. But $G$ is a finite nontrivial nilpotent group, and by **Basic Knowledge: Elements of a Finite Group Have Finite Order**, $G$ contains a non-identity element of finite order; hence $G$ cannot be isomorphic to a subgroup of $N$. $\blacksquare$
