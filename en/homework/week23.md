# Assignment 23

> **Theorem 3.6.3** (Jordan Canonical Form) Let $F$ be an algebraically closed field of characteristic zero, let $V$ be an $n$-dimensional vector space over $F$, and let $A$ be a linear transformation on $V$. Then there exists a basis of $V$ in which the matrix of $A$ is a block-diagonal matrix $\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, where each $J_i$ is a Jordan block. Two $n\times n$ matrices over $F$ are similar if and only if they have the same Jordan canonical form.

> **Basic Knowledge** (Reverse Transpose Matrix) Let $P$ be the $n\times n$ reversal matrix, i.e. $P_{i,n+1-i}=1$ and all other entries $0$. Then $P$ is symmetric, $P^2=I_n$, and $P^{-1}=P$. If $N$ is the $n\times n$ nilpotent shift matrix (i.e. $N_{i,i+1}=1$ and all other entries $0$), then $PNP=N^T$, and hence $PN$ is symmetric.

> **Basic Knowledge** (Nilpotent Kernel and Count of Jordan Blocks) Let $A$ be an $n\times n$ matrix, and let $a$ be an eigenvalue of $A$. Write
> 
> $$
> \begin{aligned}\nu_k&=\dim\ker\left(aI_n-A\right)^k\\&=n-\mathrm{rank}\left(aI_n-A\right)^k,\end{aligned}
> $$
> 
> with the convention $\nu_0=0$. Then the number of Jordan blocks of $A$ with eigenvalue $a$ and size at least $s$ is $\nu_s-\nu_{s-1}$. Hence the sequence $\left\{\nu_k\right\}_{k\geqslant0}$ completely determines the sizes and number of Jordan blocks at $a$.

### Problem 1

(Problem 3.6-9) Let $F$ be an algebraically closed field of characteristic zero. Prove that every Jordan block over $F$ can be written as a product of two symmetric matrices.

### Solution to Problem 1

Let $J$ be an $n\times n$ Jordan block over $F$, with eigenvalue $\lambda\in F$. Then $J=\lambda I_n+N$, where $N$ is the $n\times n$ nilpotent shift matrix.

Let $P$ be the $n\times n$ reversal matrix. By **Basic Knowledge** (Reverse Transpose Matrix), $P$ is symmetric, $P^2=I_n$, and $PN$ is symmetric. Set

$$
\begin{aligned}A&=PJ\\&=\lambda P+PN.\end{aligned}
$$

Since both $P$ and $PN$ are symmetric, $A$ is symmetric. Also $P^2=I_n$, so $P^{-1}=P$, and hence

$$
\begin{aligned}J&=P^{-1}A\\&=PA.\end{aligned}
$$

Here both $P$ and $A$ are symmetric matrices over $F$. Hence every Jordan block can be written as a product of two symmetric matrices. $\blacksquare$

### Problem 2

(Problem 3.6-10) Prove that every square matrix over an algebraically closed field $F$ of characteristic zero can be written as a product of two symmetric matrices over $F$.

### Solution to Problem 2

Let $A$ be an $n\times n$ matrix over $F$. By **Theorem 3.6.3** (Jordan Canonical Form), there exists an invertible matrix $S$ such that

$$
\begin{aligned}S^{-1}AS&=J\\&=\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right),\end{aligned}
$$

where $J_1,J_2,\cdots,J_s$ are all Jordan blocks.

By the conclusion of **Problem 1**, each Jordan block $J_i$ can be written as $J_i=P_iQ_i$, where both $P_i,Q_i$ are symmetric. Set

$$
P=\mathrm{diag}\left(P_1,P_2,\cdots,P_s\right),
$$

$$
Q=\mathrm{diag}\left(Q_1,Q_2,\cdots,Q_s\right).
$$

Then both $P,Q$ are symmetric, and $J=PQ$.

Hence

$$
\begin{aligned}A&=SJS^{-1}\\&=SPQS^{-1}\\&=\left(SPS^T\right)\left(S^{-T}QS^{-1}\right).\end{aligned}
$$

Here $SPS^T$ is symmetric, since its transpose is

$$
\left(SPS^T\right)^T=SP^TS^T=SPS^T;
$$

similarly,

$$
S^{-T}QS^{-1}=\left(S^{-1}\right)^TQS^{-1}
$$

is also symmetric. Hence $A$ is a product of two symmetric matrices. $\blacksquare$

### Problem 3

(Problem 3.6-11) Let $A$ be a linear transformation on a real vector space $V$. Prove that there exists a basis of $V$ in which the matrix of $A$ has the block form

$$
\begin{bmatrix}B_1&B_2\\0&B_3\end{bmatrix}
$$

where $B_1$ is a $1\times1$ or $2\times2$ block.

### Solution to Problem 3

We induct on $\dim V=n$. When $n=1$, the conclusion is clear. Assume the conclusion holds in dimensions less than $n$, and consider the $n$-dimensional case.

**Case 1: $A$ has a real eigenvalue $\lambda$.** Take a corresponding real eigenvector $v_1$, and extend it to a basis $v_1,v_2,\cdots,v_n$ of $V$. Since the one-dimensional subspace spanned by $v_1$ is $A$-invariant, the matrix of $A$ in this basis has the form

$$
\begin{bmatrix}\lambda&*\\0&A'\end{bmatrix},
$$

where $\lambda$ is a $1\times1$ block and $A'$ is an $\left(n-1\right)\times\left(n-1\right)$ real matrix. By the induction hypothesis, $A'$ can be put in the required block upper-triangular form, and hence so can $A$.

**Case 2: $A$ has no real eigenvalues.** Then the characteristic polynomial of $A$ has no linear factors over $\mathbb R\left[x\right]$, so it factors as a product of irreducible quadratic polynomials with negative discriminant. Take one of them, $p\left(x\right)=x^2+bx+c$, with $b^2-4c< 0$.

By the structure theory of finitely generated torsion modules over the principal ideal domain $\mathbb R\left[x\right]$ (i.e. the primary decomposition of $V$ as an $\mathbb R\left[x\right]$-module), the primary subspace corresponding to $p\left(x\right)$ is nonzero. Take a vector $u$ in it such that $p\left(A\right)u=0$ and $u\ne0$. Since $p\left(x\right)$ has no real roots, $u$ and $Au$ must be linearly independent (otherwise $Au=au$ with $a\in\mathbb R$, and then $a$ would be a real root of $p$, a contradiction). Let $W=\mathrm{span}\left\{u,Au\right\}$. From $p\left(A\right)u=0$, i.e. $A^2u+bAu+cu=0$, we get

$$
\begin{aligned}A\left(Au\right)&=A^2u\\&=-cu-bAu\in W,\end{aligned}
$$

so $W$ is a two-dimensional $A$-invariant subspace. Take a basis of $W$ and extend it to a basis of $V$; then the matrix of $A$ in this basis has the form

$$
\begin{bmatrix}B_1&B_2\\0&A'\end{bmatrix},
$$

where $B_1$ is a $2\times2$ block (the restriction of $A$ to $W$) and $A'$ is an $\left(n-2\right)\times\left(n-2\right)$ real matrix. By the induction hypothesis, $A'$ can be put in the required block upper-triangular form, and hence so can $A$.

In summary, by induction there exists a basis of $V$ in which the matrix of $A$ has the required block upper-triangular form. $\blacksquare$

### Problem 4

(Problem 3.6-12) (Wedderburn's theorem) Prove that two $n\times n$ matrices $A,B$ over an algebraically closed field $F$ of characteristic zero are similar if and only if, for every $a\in F$ and $k\in\mathbb N$, the matrices $\left(aI_n-A\right)^k$ and $\left(aI_n-B\right)^k$ have the same rank.

### Solution to Problem 4

**Necessity.** If $A$ and $B$ are similar, then there exists an invertible matrix $P$ such that $B=P^{-1}AP$. Hence

$$
\begin{aligned}\left(aI_n-B\right)^k&=\left(aI_n-P^{-1}AP\right)^k\\&=P^{-1}\left(aI_n-A\right)^kP.\end{aligned}
$$

Similar matrices have the same rank, so

$$
\mathrm{rank}\left(aI_n-A\right)^k=\mathrm{rank}\left(aI_n-B\right)^k.
$$

**Sufficiency.** Suppose that for every $a\in F$ and $k\in\mathbb N$, the corresponding powers of the two matrices have the same rank. By **Theorem 3.6.3** (Jordan Canonical Form), both $A$ and $B$ are similar to their Jordan canonical forms; it suffices to prove that their Jordan canonical forms are the same.

For any $a\in F$, write

$$
\begin{aligned}\nu_k\left(A\right)&=\dim\ker\left(aI_n-A\right)^k\\&=n-\mathrm{rank}\left(aI_n-A\right)^k,\end{aligned}
$$

with the convention $\nu_0\left(A\right)=0$. By hypothesis, $\nu_k\left(A\right)=\nu_k\left(B\right)$ for all $k$. By **Basic Knowledge** (Nilpotent Kernel and Count of Jordan Blocks), the number of Jordan blocks of $A$ with eigenvalue $a$ and size at least $s$ is $\nu_s\left(A\right)-\nu_{s-1}\left(A\right)$, and similarly for $B$. Hence the sizes and number of Jordan blocks at $a$ agree completely for $A$ and $B$.

Since $F$ is algebraically closed, all eigenvalues of $A,B$ lie in $F$, and the above conclusion holds for every eigenvalue $a$. Therefore the Jordan canonical forms of $A$ and $B$ are identical, and hence $A$ and $B$ are similar. $\blacksquare$
