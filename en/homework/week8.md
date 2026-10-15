# Assignment 8

> **Definition 1.8.1** (Commutator and Commutator Subgroup) Let $g,h\in G$. The element $g^{-1}h^{-1}gh$ is called the commutator of $g,h$, denoted $\left[g,h\right]$. If $H,K$ are both subgroups of $G$, then
> $$
> \left[H,K\right]=\left\langle\left[h,k\right]\mid h\in H,k\in K\right\rangle
> $$
> is called the commutator subgroup of $H,K$. In particular, $\left[G,G\right]$ is called the commutator subgroup of $G$.

> **Definition 1.8.7** (Solvable Groups and Nilpotent Groups) In a group $G$, the derived series is defined inductively by $G^{\left(0\right)}=G$, $G^{\left(k+1\right)}=\left[G^{\left(k\right)},G^{\left(k\right)}\right]$. If there exists $t$ such that $G^{\left(t\right)}=\left\{e\right\}$, then $G$ is called a solvable group. The lower central series is defined inductively by $G^{1}=G$, $G^{k+1}=\left[G,G^{k}\right]$; if there exists $t$ such that $G^{t}=\left\{e\right\}$, then $G$ is called a nilpotent group.

> **Lemma 1.8.8** (Heredity of Solvable Groups) Subgroups and quotient groups of a solvable group are solvable; conversely, if $N\trianglelefteq G$ and both $N$ and $G/N$ are solvable, then $G$ is solvable.

> **Basic Knowledge** (Key Lemma of Lie's Theorem) Let $G$ be a solvable subgroup of $\mathrm{GL}\left(V\right)$, where $V$ is a finite-dimensional vector space over the complex field. Then $G$ has a common eigenvector on $V$, i.e. there exists a one-dimensional subspace of $V$ invariant under the action of $G$. Repeated application of this conclusion shows that $G$ can be simultaneously upper-triangularized, i.e. $G$ is conjugate to a subgroup of the group $B$ of invertible upper-triangular matrices.

### Problem 1

(Problem 1.8-12) Let $G$ be a solvable group of order $n$, and let $B$ be the set of invertible complex upper-triangular matrices. Prove that $G$ is isomorphic to some subgroup of $B$. If $G$ is a nilpotent group of order $n$ and $N$ is the set of complex upper-triangular matrices with all diagonal entries equal to $1$, is $G$ isomorphic to some subgroup of $N$?

### Solution to Problem 1

We first prove the first part. Let $V$ be an $\mathbb C$-dimensional vector space over $n$ and $G$ a solvable subgroup of $\mathrm{GL}\left(V\right)$. We prove by induction on $\dim V$ that $G$ can be simultaneously upper-triangularized.

When $\dim V=1$, $\mathrm{GL}\left(V\right)$ itself is the group of upper-triangular matrices, so the conclusion is immediate.

Suppose $\dim V=n>1$. By **Definition 1.8.7** (Solvable Groups and Nilpotent Groups), the commutator subgroup $G$ of $G^{\prime}=\left[G,G\right]$ is a proper normal subgroup, and $G$ is abelian. By the induction hypothesis, $G/G^{\prime}$ has a common eigenvector on $G^{\prime}$. Let $V$ be a character of $\lambda$ and denote its eigenspace by$G^{\prime}$Since 
$$
V_{\lambda}=\left\{v\in V\mid\sigma v=\lambda\left(\sigma\right)v,\;\forall\sigma\in G^{\prime}\right\}.
$$
, for any $G^{\prime}\trianglelefteq G$, $\tau\in G$ and $\sigma\in G^{\prime}$, by **Lemma 1.8.3** (Properties of Commutators), $v\in V_{\lambda}$, and$\tau\sigma\tau^{-1}\in G^{\prime}$so 
$$
\begin{aligned}\sigma\left(\tau v\right)&=\tau\left(\tau^{-1}\sigma\tau\right)v\\&=\tau\lambda\left(\tau^{-1}\sigma\tau\right)v\\&=\lambda\left(\tau^{-1}\sigma\tau\right)\tau v,\end{aligned}
$$
, where $\tau v\in V_{\lambda^{\tau}}$. Since $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$ is abelian, the orbit of $G/G^{\prime}$ acting on the characters of $G$ is finite; taking the sum of the eigenspaces corresponding to one such orbit gives a nonzero $G^{\prime}$-invariant subspace $G$.$W$, 

 $W$ is abelian, and a commuting family of linear transformations over the complex field can be simultaneously diagonalized; hence there exists a common eigenvector of $G/G^{\prime}$ in $W$, i.e. there exists a one-dimensional $G$-invariant subspace $G$.$L\subseteq V$ induces a solvable subgroup on the quotient space 

 $G$, and by the induction hypothesis, $V/L$ can be upper-triangularized on $G$. Thus one can choose a basis of $V/L$ such that $V$ is spanned by the first basis vector, and the upper-triangularization on the quotient gives an upper-triangular matrix representation of $L$ on $G$. Hence $V$ is conjugate to a subgroup of $G$, i.e. $B$ is isomorphic to some subgroup of $G$.$B$.

Indeed, let $N$, i.e. 

 $A\in N$ is a complex upper-triangular matrix with all diagonal entries equal to $A$. Then $1$, where $A=I+M$ is strictly upper-triangular and hence nilpotent, i.e. there exists $M$ with $M$. If $r$ has finite order, i.e. there exists a positive integer $M^{r}=0$ with $A$, then$k$Let $A^{k}=I$ be the smallest positive integer with 
$$
\begin{aligned}\left(I+M\right)^{k}-I&=kM+\binom{k}{2}M^{2}+\cdots+M^{k}\\&=0.\end{aligned}
$$
; then the lowest-degree term on the left-hand side is $s$. Since $M^{s}\ne0$ is invertible in $kM^{s}$, we get $k\ne0$, a contradiction. Therefore $\mathbb C$, i.e. $M^{s}=0$.$M=0$ is the identity matrix $A=I$ itself. Hence the only finite subgroup of 

 $N$ is the trivial group $I$. Any nontrivial finite nilpotent group $N$ contains a nonidentity element of finite order, and so cannot be isomorphic to a subgroup of $\left\{I\right\}$. $G$subgroup of $N$. $\blacksquare$
