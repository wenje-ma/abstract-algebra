# week23

> **Basic Knowledge: Reversal Matrix and Transpose**<br>Let $P$ be the $n\times n$ reversal matrix, i.e. $P_{i,n+1-i}=1$ and all other entries $0$. Then $P$ is symmetric, $P^2=I_n$, and $P^{-1}=P$. If $N$ is the $n\times n$ nilpotent shift matrix (i.e. $N_{i,i+1}=1$ and all other entries $0$), then $PNP=N^\top$, so $PN$ is symmetric.

> **Basic Knowledge: Nullity and Counting Jordan Blocks**<br>Let $A$ be an $n\times n$ matrix and $a$ an eigenvalue of $A$. Set $\nu_k=\dim\ker\left(aI_n-A\right)^k=n-\mathrm{rank}\left(aI_n-A\right)^k$, with $\nu_0=0$. Then the number of Jordan blocks of $A$ with eigenvalue $a$ and size at least $s$ is $\nu_s-\nu_{s-1}$. Hence the sequence $\left\{\nu_k\right\}_{k\ge0}$ completely determines the sizes and number of Jordan blocks at $a$.

> **Theorem 3.6.3 (Jordan Normal Form)**<br>Let $F$ be an algebraically closed field of characteristic zero, $V$ an $n$-dimensional vector space over $F$, and $A$ a linear operator on $V$. Then there is a basis of $V$ in which the matrix of $A$ is a block-diagonal matrix $\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, where each $J_i$ is a Jordan block. Two $n\times n$ matrices over $F$ are similar iff they have the same Jordan normal form.

---

## 3.6-9

Let $F$ be an algebraically closed field of characteristic zero. Prove that every Jordan block over $F$ can be written as a product of two symmetric matrices over $F$.

### Solution 3.6-9

Let $J$ be an $n\times n$ Jordan block over $F$ with eigenvalue $\lambda\in F$; then $J=\lambda I_n+N$, where $N$ is the $n\times n$ nilpotent shift matrix.

Let $P$ be the $n\times n$ reversal matrix. By **Basic Knowledge: Reversal Matrix and Transpose**, $P$ is symmetric, $P^2=I_n$, and $PN$ is symmetric. Set $A=PJ=\lambda P+PN$. Since both $P$ and $PN$ are symmetric, $A$ is symmetric. Also $P^2=I_n$, so $P^{-1}=P$, and hence $J=P^{-1}A=PA$.

Here both $P$ and $A$ are symmetric matrices over $F$. Thus every Jordan block is a product of two symmetric matrices. $\blacksquare$

---

## 3.6-10

Prove that every square matrix over an algebraically closed field $F$ of characteristic zero can be written as a product of two symmetric matrices over $F$.

### Solution 3.6-10

Let $A$ be an $n\times n$ matrix over $F$. By **Theorem 3.6.3 (Jordan Normal Form)**, there is an invertible matrix $S$ such that $S^{-1}AS=J=\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, where $J_1,J_2,\cdots,J_s$ are Jordan blocks.

By the result of **3.6-9**, each Jordan block $J_i$ can be written as $J_i=P_iQ_i$ with $P_i,Q_i$ symmetric. Set $P=\mathrm{diag}\left(P_1,P_2,\cdots,P_s\right)$ and $Q=\mathrm{diag}\left(Q_1,Q_2,\cdots,Q_s\right)$; then $P,Q$ are symmetric and $J=PQ$.

Hence $A=SJS^{-1}=SPQS^{-1}=\left(SPS^\top\right)\left(S^{-T}QS^{-1}\right)$. Here $SPS^\top$ is symmetric, since its transpose is $\left(SPS^\top\right)^\top=SP^\topS^\top=SPS^\top$; similarly $S^{-T}QS^{-1}=\left(S^{-1}\right)^\topQS^{-1}$ is symmetric. Thus $A$ is a product of two symmetric matrices. $\blacksquare$

---

## 3.6-11

Let $A$ be a linear operator on a real vector space $V$. Prove that there is a basis of $V$ in which the matrix of $A$ has block form $\begin{bmatrix}B_1&B_2\\0&B_3\end{bmatrix}$, where $B_1$ is a $1\times1$ or $2\times2$ matrix.

### Solution 3.6-11

Induct on $\dim V=n$. The case $n=1$ is immediate. Assume the result holds in dimension less than $n$, and consider the $n$-dimensional case.

**Case 1: $A$ has a real eigenvalue $\lambda$.** Take a corresponding real eigenvector $v_1$ and extend it to a basis $v_1,v_2,\cdots,v_n$ of $V$. Since the one-dimensional subspace spanned by $v_1$ is $A$-invariant, the matrix of $A$ in this basis is $\begin{bmatrix}\lambda&*\\0&A'\end{bmatrix}$, where $\lambda$ is a $1\times1$ block and $A'$ is an $(n-1)\times(n-1)$ real matrix. By the induction hypothesis, $A'$ can be put in the required block-upper-triangular form, and so can $A$.

**Case 2: $A$ has no real eigenvalue.** Then the characteristic polynomial of $A$ has no linear factor over $\mathbb R\left[x\right]$, so it factors as a product of quadratic irreducible polynomials with negative discriminant. Take one such $p\left(x\right)=x^2+bx+c$ with $b^2-4c< 0$.

By the structure theory of finitely generated torsion modules over the PID $\mathbb R\left[x\right]$ (i.e. the primary decomposition of $V$ as an $\mathbb R\left[x\right]$-module), the primary subspace corresponding to $p\left(x\right)$ is nonzero. Take a vector $u$ in it with $p\left(A\right)u=0$ and $u\ne0$. Since $p\left(x\right)$ has no real root, $u$ and $Au$ must be linearly independent (otherwise $Au=au$ with $a\in\mathbb R$, making $a$ a real root of $p$, a contradiction). Set $W=\mathrm{span}\left\{u,Au\right\}$. From $p\left(A\right)u=0$, i.e. $A^2u+bAu+cu=0$, we get $A\left(Au\right)=A^2u=-cu-bAu\in W$, so $W$ is a $2$-dimensional $A$-invariant subspace. Taking a basis of $W$ and extending it to a basis of $V$, the matrix of $A$ is $\begin{bmatrix}B_1&B_2\\0&A'\end{bmatrix}$, where $B_1$ is a $2\times2$ matrix (the restriction of $A$ to $W$) and $A'$ is an $(n-2)\times(n-2)$ real matrix. By the induction hypothesis, $A'$ can be put in the required block-upper-triangular form, and so can $A$.

Thus, by induction, there is a basis of $V$ in which the matrix of $A$ has the required block-upper-triangular form. $\blacksquare$

---

## 3.6-12

(Weyr's theorem) Prove that two $n\times n$ matrices $A,B$ over an algebraically closed field of characteristic zero are similar iff for every $a\in F$ and $k\in\mathbb N$, the powers $\left(aI_n-A\right)^k$ and $\left(aI_n-B\right)^k$ have the same rank.

### Solution 3.6-12

**Necessity.** If $A$ and $B$ are similar, there is an invertible matrix $P$ with $B=P^{-1}AP$. Then $\left(aI_n-B\right)^k=\left(aI_n-P^{-1}AP\right)^k=P^{-1}\left(aI_n-A\right)^kP$. Similar matrices have the same rank, so $\mathrm{rank}\left(aI_n-A\right)^k=\mathrm{rank}\left(aI_n-B\right)^k$.

**Sufficiency.** Assume that for every $a\in F$ and $k\in\mathbb N$, the corresponding powers have the same rank. By **Theorem 3.6.3 (Jordan Normal Form)**, both $A$ and $B$ are similar to their Jordan normal forms; it suffices to show that the two Jordan normal forms coincide.

For any $a\in F$, set $\nu_k\left(A\right)=\dim\ker\left(aI_n-A\right)^k=n-\mathrm{rank}\left(aI_n-A\right)^k$, with $\nu_0\left(A\right)=0$. By assumption, $\nu_k\left(A\right)=\nu_k\left(B\right)$ for all $k$. By **Basic Knowledge: Nullity and Counting Jordan Blocks**, the number of Jordan blocks of $A$ with eigenvalue $a$ and size at least $s$ is $\nu_s\left(A\right)-\nu_{s-1}\left(A\right)$, and similarly for $B$. Hence the sizes and number of Jordan blocks at $a$ agree completely.

Since $F$ is algebraically closed, all eigenvalues of $A,B$ lie in $F$, and the above holds for every eigenvalue $a$. Thus the Jordan normal forms of $A$ and $B$ coincide completely, and therefore $A$ and $B$ are similar. $\blacksquare$
