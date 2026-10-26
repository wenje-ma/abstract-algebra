# Assignment 8

> **Definition 1.8.1** (Commutator and Commutator Subgroup) Let $g,h\in G$. The element $g^{-1}h^{-1}gh$ is called the commutator of $g,h$, denoted $\left[g,h\right]$. If $H,K$ are both subgroups of $G$, then
> $$
> \left[H,K\right]=\left\langle\left[h,k\right]\mid h\in H,k\in K\right\rangle
> $$
> is called the commutator subgroup of $H,K$. In particular, $\left[G,G\right]$ is called the commutator subgroup of $G$.

> **Definition 1.8.7** (Solvable Groups and Nilpotent Groups) In a group $G$, the derived series is defined inductively by $G^{\left(0\right)}=G$, $G^{\left(k+1\right)}=\left[G^{\left(k\right)},G^{\left(k\right)}\right]$. If there exists $t$ such that $G^{\left(t\right)}=\left\{e\right\}$, then $G$ is called a solvable group. The lower central series is defined inductively by $G^{1}=G$, $G^{k+1}=\left[G,G^{k}\right]$; if there exists $t$ such that $G^{\top}=\left\{e\right\}$, then $G$ is called a nilpotent group.

> **Lemma 1.8.8** (Heredity of Solvable Groups) Subgroups and quotient groups of a solvable group are solvable; conversely, if $N\trianglelefteq G$ and both $N$ and $G/N$ are solvable, then $G$ is solvable.

> **Basic Knowledge** (Key Lemma of Lie's Theorem) Let $G$ be a solvable subgroup of $\mathrm{GL}\left(V\right)$, where $V$ is a finite-dimensional vector space over the complex field. Then $G$ has a common eigenvector on $V$, i.e. there exists a one-dimensional subspace of $V$ invariant under the action of $G$. Repeated application of this conclusion shows that $G$ can be simultaneously upper-triangularized, i.e. $G$ is conjugate to a subgroup of the group $B$ of invertible upper-triangular matrices.

### Problem 1

(Problem 1.8-12) Let $G$ be a solvable group of order $n$, and let $B$ be the set of invertible complex upper-triangular matrices. Prove that $G$ is isomorphic to some subgroup of $B$. If $G$ is a nilpotent group of order $n$ and $N$ is the set of complex upper-triangular matrices with all diagonal entries equal to $1$, is $G$ isomorphic to some subgroup of $N$?

### Solution to Problem 1

We first prove the first part. Let $V$ be an $n$-dimensional vector space over $\mathbb C$ and $G$ a solvable subgroup of $\mathrm{GL}\left(V\right)$. We prove by induction on $\dim V$ that $G$ can be simultaneously upper-triangularized.

When $\dim V=1$, $\mathrm{GL}\left(V\right)$ itself is the group of upper-triangular matrices, so the conclusion is immediate.

Suppose $\dim V=n> 1$. By **Definition 1.8.7** (Solvable Groups and Nilpotent Groups), the commutator subgroup $G^{\prime}=\left[G,G\right]$ of $G$ is a proper normal subgroup, and $G/G^{\prime}$ is abelian. By the induction hypothesis, $G^{\prime}$ has a common eigenvector on $V$. Let $\lambda$ be a character of $G^{\prime}$ and denote its eigenspace by

$$
V_{\lambda}=\left\{v\in V\mid\sigma v=\lambda\left(\sigma\right)v,\;\forall\sigma\in G^{\prime}\right\}.
$$

Since $G^{\prime}\trianglelefteq G$, for any $\tau\in G$, $\sigma\in G^{\prime}$ and $v\in V_{\lambda}$, by **Lemma 1.8.3** (Properties of Commutators), $\tau\sigma\tau^{-1}\in G^{\prime}$, and

$$
\sigma\left(\tau v\right)=\tau\left(\tau^{-1}\sigma\tau\right)v=\tau\lambda\left(\tau^{-1}\sigma\tau\right)v=\lambda\left(\tau^{-1}\sigma\tau\right)\tau v,
$$

so $\tau v\in V_{\lambda^{\tau}}$, where $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$. Since $G/G^{\prime}$ is abelian, the orbit of $G$ acting on the characters of $G^{\prime}$ is finite; taking the sum of the eigenspaces corresponding to one such orbit gives a nonzero $G$-invariant subspace $W$.

On $W$, $G/G^{\prime}$ is abelian, and a commuting family of linear transformations over the complex field can be simultaneously diagonalized; hence there exists a common eigenvector of $G$ in $W$, i.e. there exists a one-dimensional $G$-invariant subspace $L\subseteq V$.

Then $G$ induces a solvable subgroup on the quotient space $V/L$, and by the induction hypothesis, $G$ can be upper-triangularized on $V/L$. Thus one can choose a basis of $V$ such that $L$ is spanned by the first basis vector, and the upper-triangularization on the quotient gives an upper-triangular matrix representation of $G$ on $V$. Hence $G$ is conjugate to a subgroup of $B$, i.e. $G$ is isomorphic to some subgroup of $B$.

We now answer the second part. The answer is negative, i.e. a nontrivial finite nilpotent group cannot be isomorphic to a subgroup of $N$.

Indeed, let $A\in N$, i.e. $A$ is a complex upper-triangular matrix with all diagonal entries equal to $1$. Then $A=I+M$, where $M$ is strictly upper-triangular and hence nilpotent, i.e. there exists $r$ with $M^{r}=0$. If $A$ has finite order, i.e. there exists a positive integer $k$ with $A^{k}=I$, then

$$
\left(I+M\right)^{k}-I=kM+\binom{k}{2}M^{2}+\cdots+M^{k}=0.
$$

Let $s$ be the smallest positive integer with $M^{s}\ne0$; then the lowest-degree term on the left-hand side is $kM^{s}$. Since $k\ne0$ is invertible in $\mathbb C$, we get $M^{s}=0$, a contradiction. Therefore $M=0$, i.e. $A=I$.

This shows that the only finite-order element in $N$ is the identity matrix $I$ itself. Hence the only finite subgroup of $N$ is the trivial group $\left\{I\right\}$. Any nontrivial finite nilpotent group $G$ contains a nonidentity element of finite order, and so cannot be isomorphic to a subgroup of $N$. $\blacksquare$
