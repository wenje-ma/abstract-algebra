# week11

> **Theorem 2.7.7 (Bezout Identity)**
> 
> Let $R$ be a principal ideal domain, $a,b\in{R}$, and $d$ a greatest common divisor of $a,b$. Then there exist $u,v\in{R}$ such that $d=ua+vb$.

> **Theorem 3.4.5 (Structure Theorem for Finitely Generated Modules over a PID)**
> 
> Every finitely generated module $M$ over a principal ideal domain $D$ has a decomposition $M=Dy_1\oplus\cdots\oplus{D}y_s$ with $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$ and $y_j\ne0$. The $d_i$ for which $\operatorname{ann}\left(y_i\right)=\left(d_i\right)$ with nonzero annihilator are called invariant factors; those factored into powers of irreducibles are called elementary divisors.

> **Theorem 3.4.9 ($p$-Primary Decomposition of Torsion Modules)**
> 
> Let $M$ be a finitely generated torsion module over a principal ideal domain $D$. Then there exist finitely many pairwise nonassociate irreducibles $p_1,\cdots,p_m$ such that $M=M_{p_1}\oplus\cdots\oplus{M}_{p_m}$, where $M_p=\left\{x\in{M}\mid\exists{e},p^ex=0\right\}$ is the $p$-primary component. In particular, if $\operatorname{ann}\left(y\right)=\left(ab\right)$ with $a,b$ coprime, then $Dy=Dy_1\oplus{D}y_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$.

> **Corollary 3.4.12 (Isomorphism Criterion for Finitely Generated Modules)**
> 
> Let $M_1,M_2$ be finitely generated modules over a principal ideal domain $D$. Then $M_1\cong{M}_2$ iff they have the same rank and invariant factors, iff they have the same rank and elementary divisors.

> **Theorem 3.5.2 (Number of Isomorphism Classes of Finite Abelian Groups)**
> 
> Let $n=p_1^{m_1}p_2^{m_2}\cdots{p}_s^{m_s}$ be the prime factorization of $n$, with $p_1,p_2,\cdots,p_s$ distinct primes and $m_i>0$. Then the number of isomorphism classes of abelian groups of order $n$ is $\prod_{i=1}^sp\left(m_i\right)$, where $p\left(m\right)$ is the number of distinct partitions of the natural number $m$.

> **Theorem 3.6.3 (Jordan Normal Form)**
> 
> Let $F$ be an algebraically closed field of characteristic zero, $V$ an $n$-dimensional vector space over $F$, and $A$ a linear operator on $V$. Then there is a basis of $V$ in which the matrix of $A$ is a block-diagonal matrix $\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, where each $J_i$ is a Jordan block. Two $n\times{n}$ matrices over $F$ are similar iff they have the same Jordan normal form.

## 3.4-6

Let $D$ be a principal ideal domain and $M$ a finitely generated torsion $D$-module. For $a\in{D}$, set $M\left(a\right)=\left\{x\in{M}\mid{a}x=0\right\}$. Prove:

(1) $M\left(a\right)$ is a submodule of $M$, and if $a$ is invertible then $M\left(a\right)=\left\{0\right\}$;

(2) if $a\mid{b}$, then $M\left(a\right)\subset{M}\left(b\right)$;

(3) for $a,b\in{D}$, $M\left(a\right)\cap{M}\left(b\right)=M\left(\left(a,b\right)\right)$, where $\left(a,b\right)$ is a gcd of $a,b$;

(4) if $a,b$ are coprime, then $M\left(ab\right)=M\left(a\right)\oplus{M}\left(b\right)$.

### Solution to 3.4-6

(1) $M\left(a\right)$ is nonempty (contains $0$). If $x,y\in{M}\left(a\right)$, then $a\left(x-y\right)=ax-ay=0$; for $r\in{D}$, $a\left(rx\right)=r\left(ax\right)=0$. Hence $M\left(a\right)$ is a submodule. If $a$ is invertible, multiplying $ax=0$ by $a^{-1}$ gives $x=0$, so $M\left(a\right)=\left\{0\right\}$.

(2) Write $b=ac$. If $x\in{M}\left(a\right)$ and $ax=0$, then $bx=cax=0$, so $x\in{M}\left(b\right)$. Hence $M\left(a\right)\subset{M}\left(b\right)$.

(3) Let $d=\left(a,b\right)$ be a gcd. Since $d\mid{a}$ and $d\mid{b}$, by (2) we have $M\left(d\right)\subset{M}\left(a\right)$ and $M\left(d\right)\subset{M}\left(b\right)$, so $M\left(d\right)\subset{M}\left(a\right)\cap{M}\left(b\right)$.

Conversely, if $x\in{M}\left(a\right)\cap{M}\left(b\right)$, then $ax=bx=0$. By **Theorem 2.7.7 (Bezout Identity)**, there exist $u,v\in{D}$ with $d=ua+vb$. Then $dx=\left(ua+vb\right)x=uax+vbx=0$, so $x\in{M}\left(d\right)$. Hence $M\left(a\right)\cap{M}\left(b\right)=M\left(d\right)=M\left(\left(a,b\right)\right)$.

(4) Let $a,b$ be coprime, i.e. $\left(a,b\right)=1$. By (2), $a\mid{a}b$ and $b\mid{a}b$, so $M\left(a\right)\subset{M}\left(ab\right)$ and $M\left(b\right)\subset{M}\left(ab\right)$, hence $M\left(a\right)+M\left(b\right)\subset{M}\left(ab\right)$.

Now the intersection. By (3), $M\left(a\right)\cap{M}\left(b\right)=M\left(\left(a,b\right)\right)=M\left(1\right)=\left\{0\right\}$ (using (1)).

Finally show $M\left(ab\right)\subset{M}\left(a\right)+M\left(b\right)$. Since $\left(a,b\right)=1$, by **Theorem 2.7.7 (Bezout Identity)** there exist $u,v$ with $ua+vb=1$. For any $x\in{M}\left(ab\right)$, $abx=0$. Write $x=\left(ua+vb\right)x=uax+vbx$. Set $x_1=vbx$ and $x_2=uax$. Then $ax_1=avbx=vabx=0$ and $bx_2=buax=uabx=0$, so $x_1\in{M}\left(a\right)$ and $x_2\in{M}\left(b\right)$, hence $x=x_1+x_2\in{M}\left(a\right)+M\left(b\right)$.

Thus $M\left(ab\right)=M\left(a\right)+M\left(b\right)$ and $M\left(a\right)\cap{M}\left(b\right)=\left\{0\right\}$, so $M\left(ab\right)=M\left(a\right)\oplus{M}\left(b\right)$. $\blacksquare$

## 3.4-10

Let $M$ be a torsion module over a principal ideal domain $D$. Prove that $M$ is simple iff $M=Dz$ with $\operatorname{ann}\left(z\right)=\left(p\right)$ for a prime element $p$; and $M$ is indecomposable iff $M=Dz$ with $\operatorname{ann}\left(z\right)=\left(p^e\right)$ for a prime $p$ and $e\in\mathbb{N}$. (The final formula in the original problem is damaged; it is completed above as $\left(p^e\right)$ according to the textbook context.)

### Solution to 3.4-10

Simple module case.

Necessity. Let $M$ be a simple torsion module. By **Theorem 3.4.5 (Structure Theorem for Finitely Generated Modules over a PID)**, $M=Dy_1\oplus\cdots\oplus{D}y_s$. If $s\ge2$, then $Dy_1$ is a nontrivial submodule of $M$, contradicting simplicity. Hence $s=1$, $M=Dz$, $\operatorname{ann}\left(z\right)=\left(d\right)$.

If $d$ is not prime, then $d$ has a nontrivial factorization $d=ab$ with $a,b$ both nonunits. By **Theorem 3.4.9 ($p$-Primary Decomposition of Torsion Modules)**, $Dz=Dy_1\oplus{D}y_2$ with $\operatorname{ann}\left(y_1\right)=\left(a\right)$ and $\operatorname{ann}\left(y_2\right)=\left(b\right)$, both nonzero submodules, again contradicting simplicity. Hence $d=p$ is prime.

Sufficiency. Let $M=Dz$ with $\operatorname{ann}\left(z\right)=\left(p\right)$, $p$ prime. Then $M\cong{D}/\left(p\right)$. Since $p$ is prime, $\left(p\right)$ is a maximal ideal, $D/\left(p\right)$ is a field, and as a $D$-module it has only the zero submodule and itself. Hence $M$ is simple.

Indecomposable module case.

Necessity. Let $M$ be indecomposable. By the structure theorem, $M=Dy_1\oplus\cdots\oplus{D}y_s$. If $s\ge2$, it is already a direct sum of two nonzero submodules, a contradiction. Hence $s=1$, $M=Dz$, $\operatorname{ann}\left(z\right)=\left(d\right)$.

If $d$ has two coprime nonunit factors, i.e. $d=ab$ with $\left(a,b\right)=1$ and $a,b$ both nonunits, then by **Theorem 3.4.9 ($p$-Primary Decomposition of Torsion Modules)**, $Dz=Dz_1\oplus{D}z_2$, both nonzero, a contradiction. Hence all irreducible factors of $d$ are associate, i.e. $d=p^e$ with $p$ prime and $e\in\mathbb{N}$.

Sufficiency. Let $M=Dz$ with $\operatorname{ann}\left(z\right)=\left(p^e\right)$. Then $M\cong{D}/\left(p^e\right)$. The submodules of $D/\left(p^e\right)$ correspond bijectively to the ideals of $D$ containing $\left(p^e\right)$, namely $\left(p^e\right)\subset\left(p^{e-1}\right)\subset\cdots\subset\left(p\right)\subset{D}$, a single chain. If $M=N_1\oplus{N}_2$ were a direct sum of two nonzero submodules, then $N_1,N_2$ would both be nonzero proper submodules in this chain, hence comparable, so $N_1\cap{N}_2\ne0$, contradicting the direct sum. Thus $M$ is indecomposable.

(Note: if one allows a free cyclic module $Dz$ of rank $1$ with $\operatorname{ann}\left(z\right)=0$, it is likewise indecomposable, since the integral domain $D$ has no nontrivial direct-sum decomposition of ideals.) $\blacksquare$

## 3.5-4

Determine the number of isomorphism classes of abelian groups of order $936$.

### Solution to 3.5-4

First factor $936$. Since $936=8\times117=2^3\times3^2\times13$, we have $936=2^3\cdot3^2\cdot13^1$.

Compute the partition numbers of the exponents. The partitions of $3$ are $3$, $2+1$, $1+1+1$, so $p\left(3\right)=3$; the partitions of $2$ are $2$, $1+1$, so $p\left(2\right)=2$; the only partition of $1$ is $1$, so $p\left(1\right)=1$.

By **Theorem 3.5.2 (Number of Isomorphism Classes of Finite Abelian Groups)**, the number of isomorphism classes of abelian groups of order $936$ is $p\left(3\right)p\left(2\right)p\left(1\right)=3\times2\times1=6$.

Hence there are $6$ isomorphism classes of abelian groups of order $936$. $\blacksquare$

## 3.5-8

(1) Let $G=\mathbb{Z}_{p^e}$, $p$ prime, $e>0$, and write $o\left(g\right)$ for the order of $g\in{G}$. Prove: if $l\le{e}$, then $\left|\left\{g\in{G}\mid{o}\left(g\right)\mid{p}^l\right\}\right|=p^l$; if $l>{}e$, then $\left|\left\{g\in{G}\mid{o}\left(g\right)\mid{p}^l\right\}\right|=p^e$.

(2) Let $H_1,H_2,\cdots,H_s$ be finite abelian groups, $q$ a natural number, and set $m_i=\left|\left\{h\in{H}_i\mid{o}\left(h\right)\mid{q}\right\}\right|$, $G=H_1\times{H}_2\times\cdots\times{H}_s$. Then $\left|\left\{g\in{G}\mid{o}\left(g\right)\mid{q}\right\}\right|=m_1m_2\cdots{m}_s$.

(3) Determine how many elements of $\mathbb{Z}_4\times\mathbb{Z}_8\times\mathbb{Z}_{16}$ have order dividing $4$.

### Solution to 3.5-8

(1) View $G=\mathbb{Z}_{p^e}$ as an additive cyclic group with elements $0,1,2,\cdots,p^e-1$ modulo $p^e$. For $g=k\in\mathbb{Z}_{p^e}$, $o\left(g\right)=\frac{p^e}{\gcd\left(k,p^e\right)}$. Thus $o\left(g\right)\mid{p}^l$ iff $p^lg=0$, i.e. $p^lk\equiv0\pmod{p^e}$.

When $l\le{e}$, this is equivalent to $k$ being divisible by $p^{e-l}$. Among the residue classes modulo $p^e$, exactly $p^l$ are divisible by $p^{e-l}$, so $\left|\left\{g\in{G}\mid{o}\left(g\right)\mid{p}^l\right\}\right|=p^l$.

When $l>{}e$, $p^l$ is a multiple of $p^e$, and $p^lg=0$ holds automatically for every $g\in{G}$, so the set is all of $G$, with $p^e$ elements.

(2) Take any $g=\left(h_1,h_2,\cdots,h_s\right)\in{G}$. By Order of an Element in a Direct Product, $o\left(g\right)\mid{q}$ iff $o\left(h_i\right)\mid{q}$ for every $i$. Hence the $g$ satisfying the condition are exactly the direct product of the choices $\left\{h\in{H}_i\mid{o}\left(h\right)\mid{q}\right\}$, and by the multiplication principle,

$$
\left|\left\{g\in{G}\mid{o}\left(g\right)\mid{q}\right\}\right|=\prod_{i=1}^s\left|\left\{h\in{H}_i\mid{o}\left(h\right)\mid{q}\right\}\right|=m_1m_2\cdots{m}_s.
$$

(3) In $\mathbb{Z}_4\times\mathbb{Z}_8\times\mathbb{Z}_{16}$, requiring the order to divide $4$ means $4g=0$. Count the choices in each component.

For $\mathbb{Z}_4$, the group has order $4$, so $4g=0$ for all $4$ elements; $m_1=4$.

For $\mathbb{Z}_8$, $4k\equiv0\pmod8$ iff $k$ is even, i.e. $k\in\left\{0,2,4,6\right\}$, $4$ choices; $m_2=4$.

For $\mathbb{Z}_{16}$, $4k\equiv0\pmod{16}$ iff $k\equiv0\pmod4$, i.e. $k\in\left\{0,4,8,12\right\}$, $4$ choices; $m_3=4$.

By (2), the desired number is $m_1m_2m_3=4\times4\times4=64$.

Hence $64$ elements of $\mathbb{Z}_4\times\mathbb{Z}_8\times\mathbb{Z}_{16}$ have order dividing $4$. $\blacksquare$

## 3.5-12

Classify the abelian groups of order $8$, and determine all homomorphisms from each of these groups to $\mathbb{Q}^*$.

### Solution to 3.5-12

Since $8=2^3$, the partitions of $3$ are $3$, $2+1$, $1+1+1$, so $p\left(3\right)=3$. By **Theorem 3.5.2 (Number of Isomorphism Classes of Finite Abelian Groups)**, there are $3$ isomorphism classes of abelian groups of order $8$, namely $\mathbb{Z}_8$, $\mathbb{Z}_4\times\mathbb{Z}_2$, and $\mathbb{Z}_2\times\mathbb{Z}_2\times\mathbb{Z}_2$.

Now determine their homomorphisms to $\mathbb{Q}^*$. Let $\varphi:G\to\mathbb{Q}^*$ be a group homomorphism. Since $G$ is finite, $\varphi\left(G\right)$ is a finite subgroup of $\mathbb{Q}^*$. By Finite Subgroups of the Rational Multiplicative Group, the only finite subgroup of $\mathbb{Q}^*$ is $\left\{\pm1\right\}$, so $\varphi\left(G\right)\subseteq\left\{\pm1\right\}$, i.e. each generator maps to either $1$ or $-1$.

Case 1: $G=\mathbb{Z}_8$. Let $g$ be a generator of $G$, $o\left(g\right)=8$. The homomorphism $\varphi$ is determined by $\varphi\left(g\right)\in\left\{\pm1\right\}$, and $\varphi\left(g\right)^8=1$ holds automatically for $\pm1$. Hence there are $2$ homomorphisms.

Case 2: $G=\mathbb{Z}_4\times\mathbb{Z}_2$. Let $g_1$ generate $\mathbb{Z}_4$ and $g_2$ generate $\mathbb{Z}_2$. The homomorphism is determined by $\varphi\left(g_1\right),\varphi\left(g_2\right)\in\left\{\pm1\right\}$, and the constraints $\varphi\left(g_1\right)^4=1$, $\varphi\left(g_2\right)^2=1$ hold automatically for $\pm1$. Hence there are $2\times2=4$ homomorphisms.

Case 3: $G=\mathbb{Z}_2\times\mathbb{Z}_2\times\mathbb{Z}_2$. Let $g_1,g_2,g_3$ be the three generators of order $2$. The homomorphism is determined by $\varphi\left(g_1\right),\varphi\left(g_2\right),\varphi\left(g_3\right)\in\left\{\pm1\right\}$, and all constraints hold automatically. Hence there are $2^3=8$ homomorphisms.

In summary, the abelian groups of order $8$ fall into $3$ classes, with $2$, $4$, and $8$ homomorphisms to $\mathbb{Q}^*$ respectively. $\blacksquare$

## 3.6-9

Let $F$ be an algebraically closed field of characteristic zero. Prove that every Jordan block over $F$ can be written as a product of two symmetric matrices over $F$.

### Solution to 3.6-9

Let $J$ be an $n\times{n}$ Jordan block over $F$ with eigenvalue $\lambda\in{F}$; then $J=\lambda{I}_n+N$, where $N$ is the $n\times{n}$ nilpotent shift matrix.

Let $P$ be the $n\times{n}$ reversal matrix. By Reversal Matrix and Transpose, $P$ is symmetric, $P^2=I_n$, and $PN$ is symmetric. Set $A=PJ=\lambda{P}+PN$. Since both $P$ and $PN$ are symmetric, $A$ is symmetric. Also $P^2=I_n$, so $P^{-1}=P$, and hence $J=P^{-1}A=PA$.

Here both $P$ and $A$ are symmetric matrices over $F$. Thus every Jordan block is a product of two symmetric matrices. $\blacksquare$

## 3.6-10

Prove that every square matrix over an algebraically closed field $F$ of characteristic zero can be written as a product of two symmetric matrices over $F$.

### Solution to 3.6-10

Let $A$ be an $n\times{n}$ matrix over $F$. By **Theorem 3.6.3 (Jordan Normal Form)**, there is an invertible matrix $S$ such that $S^{-1}AS=J=\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, where $J_1,J_2,\cdots,J_s$ are Jordan blocks.

By the result of 3.6-9, each Jordan block $J_i$ can be written as $J_i=P_iQ_i$ with $P_i,Q_i$ symmetric. Set $P=\mathrm{diag}\left(P_1,P_2,\cdots,P_s\right)$ and $Q=\mathrm{diag}\left(Q_1,Q_2,\cdots,Q_s\right)$; then $P,Q$ are symmetric and $J=PQ$.

Hence $A=SJS^{-1}=SPQS^{-1}=\left(SPS^{\top}\right)\left(S^{-T}QS^{-1}\right)$. Here $SPS^{\top}$ is symmetric, since its transpose is $\left(SPS^{\top}\right)^{\top}=SP^{\top}S^{\top}=SPS^{\top}$; similarly $S^{-T}QS^{-1}=\left(S^{-1}\right)^{\top}QS^{-1}$ is symmetric. Thus $A$ is a product of two symmetric matrices. $\blacksquare$

## 3.6-11

Let $A$ be a linear operator on a real vector space $V$. Prove that there is a basis of $V$ in which the matrix of $A$ has block form $\begin{bmatrix}B_1&B_2\\0&B_3\end{bmatrix}$, where $B_1$ is a $1\times1$ or $2\times2$ matrix.

### Solution to 3.6-11

Induct on $\dim{V}=n$. The case $n=1$ is immediate. Assume the result holds in dimension less than $n$, and consider the $n$-dimensional case.

Case 1: $A$ has a real eigenvalue $\lambda$. Take a corresponding real eigenvector $v_1$ and extend it to a basis $v_1,v_2,\cdots,v_n$ of $V$. Since the one-dimensional subspace spanned by $v_1$ is $A$-invariant, the matrix of $A$ in this basis is $\begin{bmatrix}\lambda&*\\0&A'\end{bmatrix}$, where $\lambda$ is a $1\times1$ block and $A'$ is an $\left(n-1\right)\times\left(n-1\right)$ real matrix. By the induction hypothesis, $A'$ can be put in the required block-upper-triangular form, and so can $A$.

Case 2: $A$ has no real eigenvalue. Then the characteristic polynomial of $A$ has no linear factor over $\mathbb{R}\left[x\right]$, so it factors as a product of quadratic irreducible polynomials with negative discriminant. Take one such $p\left(x\right)=x^2+bx+c$ with $b^2-4c<0$.

By the structure theory of finitely generated torsion modules over the PID $\mathbb{R}\left[x\right]$ (i.e. the primary decomposition of $V$ as an $\mathbb{R}\left[x\right]$-module), the primary subspace corresponding to $p\left(x\right)$ is nonzero. Take a vector $u$ in it with $p\left(A\right)u=0$ and $u\ne0$. Since $p\left(x\right)$ has no real root, $u$ and $Au$ must be linearly independent (otherwise $Au=au$ with $a\in\mathbb{R}$, making $a$ a real root of $p$, a contradiction). Set $W=\mathrm{span}\left\{u,Au\right\}$. From $p\left(A\right)u=0$, i.e. $A^2u+bAu+cu=0$, we get $A\left(Au\right)=A^2u=-cu-bAu\in{W}$, so $W$ is a $2$-dimensional $A$-invariant subspace. Taking a basis of $W$ and extending it to a basis of $V$, the matrix of $A$ is $\begin{bmatrix}B_1&B_2\\0&A'\end{bmatrix}$, where $B_1$ is a $2\times2$ matrix (the restriction of $A$ to $W$) and $A'$ is an $\left(n-2\right)\times\left(n-2\right)$ real matrix. By the induction hypothesis, $A'$ can be put in the required block-upper-triangular form, and so can $A$.

Thus, by induction, there is a basis of $V$ in which the matrix of $A$ has the required block-upper-triangular form. $\blacksquare$

## 3.6-12

(Weyr's theorem) Prove that two $n\times{n}$ matrices $A,B$ over an algebraically closed field of characteristic zero are similar iff for every $a\in{F}$ and $k\in\mathbb{N}$, the powers $\left(aI_n-A\right)^k$ and $\left(aI_n-B\right)^k$ have the same rank.

### Solution to 3.6-12

Necessity. If $A$ and $B$ are similar, there is an invertible matrix $P$ with $B=P^{-1}AP$. Then $\left(aI_n-B\right)^k=\left(aI_n-P^{-1}AP\right)^k=P^{-1}\left(aI_n-A\right)^kP$. Similar matrices have the same rank, so $\mathrm{rank}\left(aI_n-A\right)^k=\mathrm{rank}\left(aI_n-B\right)^k$.

Sufficiency. Assume that for every $a\in{F}$ and $k\in\mathbb{N}$, the corresponding powers have the same rank. By **Theorem 3.6.3 (Jordan Normal Form)**, both $A$ and $B$ are similar to their Jordan normal forms; it suffices to show that the two Jordan normal forms coincide.

For any $a\in{F}$, set $\nu_k\left(A\right)=\dim\ker\left(aI_n-A\right)^k=n-\mathrm{rank}\left(aI_n-A\right)^k$, with $\nu_0\left(A\right)=0$. By assumption, $\nu_k\left(A\right)=\nu_k\left(B\right)$ for all $k$. By Nullity and Counting Jordan Blocks, the number of Jordan blocks of $A$ with eigenvalue $a$ and size at least $s$ is $\nu_s\left(A\right)-\nu_{s-1}\left(A\right)$, and similarly for $B$. Hence the sizes and number of Jordan blocks at $a$ agree completely.

Since $F$ is algebraically closed, all eigenvalues of $A,B$ lie in $F$, and the above holds for every eigenvalue $a$. Thus the Jordan normal forms of $A$ and $B$ coincide completely, and therefore $A$ and $B$ are similar. $\blacksquare$
