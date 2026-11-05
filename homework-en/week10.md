# week10

> **Theorem 2.7.7 (Bezout Identity)**
> 
> Let $R$ be a principal ideal domain, $a,b\in R$, and $d$ a greatest common divisor of $a,b$. Then there exist $u,v\in R$ such that $d=ua+vb$.

> **Theorem 3.1.10 (Criterion for a Direct Sum)**
> 
> Let $M_1,\cdots,M_s$ be submodules of an $R$-module $M$. Then $M=M_1\oplus\cdots\oplus M_s$ iff: (1) $M=M_1+\cdots+M_s$; (2) for every $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

> **Proposition 3.1.16 (Kernel and Image of a Homomorphism)**
> 
> The kernel $\ker\phi$ of a module homomorphism $\phi:M_1\to M_2$ is a submodule of $M_1$, and the image $\operatorname{Im}\phi$ is a submodule of $M_2$.

> **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**
> 
> If $\phi:M_1\to M_2$ is a surjective module homomorphism, then the quotient module $M_1/\ker\phi$ is isomorphic to $M_2$; moreover, if $N_1$ is a submodule of $M_1$ containing $\ker\phi$, then $M_1/N_1\cong M_2/\phi\left(N_1\right)$.

> **Theorem 3.3.6 (Characterization of a Basis of a Free Module)**
> 
> Let $M$ be a module over a unital ring $R$, and let $u_1,\cdots,u_m\in M$. Then $M$ is free with $u_1,\cdots,u_m$ as a basis iff: (1) $u_1,\cdots,u_m$ generate $M$; (2) $u_1,\cdots,u_m$ are linearly independent.

> **Theorem 3.4.5 (Structure Theorem for Finitely Generated Modules over a PID)**
> 
> Every finitely generated module $M$ over a principal ideal domain $D$ has a decomposition $M=Dy_1\oplus\cdots\oplus Dy_s$ with $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$ and $y_j\ne0$. The $d_i$ for which $\operatorname{ann}\left(y_i\right)=\left(d_i\right)$ with nonzero annihilator are called invariant factors; those factored into powers of irreducibles are called elementary divisors.

> **Theorem 3.4.9 ($p$-Primary Decomposition of Torsion Modules)**
> 
> Let $M$ be a finitely generated torsion module over a principal ideal domain $D$. Then there exist finitely many pairwise nonassociate irreducibles $p_1,\cdots,p_m$ such that $M=M_{p_1}\oplus\cdots\oplus M_{p_m}$, where $M_p=\left\{x\in M\mid \exists e,p^ex=0\right\}$ is the $p$-primary component. In particular, if $\operatorname{ann}\left(y\right)=\left(ab\right)$ with $a,b$ coprime, then $Dy=Dy_1\oplus Dy_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$.

> **Corollary 3.4.12 (Isomorphism Criterion for Finitely Generated Modules)**
> 
> Let $M_1,M_2$ be finitely generated modules over a principal ideal domain $D$. Then $M_1\cong M_2$ iff they have the same rank and invariant factors, iff they have the same rank and elementary divisors.

## 2.9-3

Let $R$ be an integral domain and $f\left(x\right)\in R\left[x\right]$. Then $a\in R$ is a root of $f\left(x\right)$ if and only if $\left(x-a\right)$ divides $f\left(x\right)$.

### Solution to 2.9-3

Divide $f\left(x\right)$ by the monic polynomial $x-a$; by Polynomial Division with Remainder, there exist $q\left(x\right)\in R\left[x\right]$ and a constant $c\in R$ such that $f\left(x\right)=q\left(x\right)\left(x-a\right)+c$, where the remainder has degree less than $1$, hence is a constant. Substituting $x=a$, using that $a\in R$ evaluates elements of $R\left[x\right]$, gives $f\left(a\right)=q\left(a\right)\cdot0+c=c$.

Thus $a$ is a root of $f\left(x\right)$, i.e. $f\left(a\right)=0$, iff $c=0$, iff $f\left(x\right)=q\left(x\right)\left(x-a\right)$, i.e. $\left(x-a\right)\mid f\left(x\right)$. $\blacksquare$

## 2.9-4

Let $R$ be an integral domain and $f\left(x\right)\in R\left[x\right]$, with $a_1,a_2,\cdots,a_s$ distinct roots of $f\left(x\right)$. Then $\left(x-a_1\right)\left(x-a_2\right)\cdots\left(x-a_s\right)$ divides $f\left(x\right)$. Deduce that a nonzero polynomial of degree $m$ over an integral domain has at most $m$ distinct roots.

### Solution to 2.9-4

Induct on $s$. For $s=1$, this is the result of 2.9-3.

Assume the result holds for $s-1$, i.e. $\prod_{i=1}^{s-1}\left(x-a_i\right)\mid f\left(x\right)$. Write $f\left(x\right)=g\left(x\right)\prod_{i=1}^{s-1}\left(x-a_i\right)$. Substituting $x=a_s$, since $a_s$ is a root of $f$, $f\left(a_s\right)=0$, gives $0=g\left(a_s\right)\prod_{i=1}^{s-1}\left(a_s-a_i\right)$.

Since $a_1,\cdots,a_s$ are pairwise distinct, $a_s-a_i\ne0$ for $1\le i\le s-1$. As $R$ is an integral domain with no zero divisors, $g\left(a_s\right)=0$. By 2.9-3, $\left(x-a_s\right)\mid g\left(x\right)$; write $g\left(x\right)=h\left(x\right)\left(x-a_s\right)$. Then $f\left(x\right)=h\left(x\right)\prod_{i=1}^{s}\left(x-a_i\right)$, i.e. $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. This completes the induction.

Now let $f\left(x\right)\ne0$ have degree $m$ and $s$ distinct roots $a_1,\cdots,a_s$. By the above, $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. This product is degree $s$, and it divides a degree-$m$ polynomial, so $s\le m$. Thus a nonzero polynomial of degree $m$ over an integral domain has at most $m$ distinct roots. $\blacksquare$

## 2.9-11

Prove that the formal power series ring $\mathbb R\left[\!\left[t\right]\!\right]$ over the real field $\mathbb R$ is a unique factorization domain.

### Solution to 2.9-11

Set $R=\mathbb R\left[\!\left[t\right]\!\right]$. Take any nonzero power series $f\left(t\right)=\sum_{n=0}^{\infty}a_nt^n\in R$. Let $a_k$ be its first nonzero coefficient, i.e. $a_0=\cdots=a_{k-1}=0$, $a_k\ne0$; call $k$ the order of $f$, written $\operatorname{ord}\left(f\right)=k$. Then $f\left(t\right)=t^k\cdot\left(a_k+a_{k+1}t+\cdots\right)=t^k\,u\left(t\right)$, where $u\left(t\right)=a_k+a_{k+1}t+\cdots$ has nonzero constant term $a_k$. By Formal Power Series Ring, $u\left(t\right)$ is a unit (a power series with nonzero constant term is invertible).

First determine the irreducible elements of $R$. If $f$ is nonzero and a nonunit, then $k=\operatorname{ord}\left(f\right)\ge1$ and $f=t^ku$. If $k=1$, $f=t\,u$ with $u$ a unit, so $f$ is associate to $t$. And $t$ is irreducible: if $t=\alpha\beta$, then $1=\operatorname{ord}\left(t\right)=\operatorname{ord}\left(\alpha\right)+\operatorname{ord}\left(\beta\right)$, so one of $\operatorname{ord}\left(\alpha\right),\operatorname{ord}\left(\beta\right)$ is $0$ and the other $1$, i.e. one of them is a unit. Hence $t$ is irreducible.

Thus any nonzero nonunit $f$ can be written as $f=t^k\,u$ with $u$ a unit, where $k=\operatorname{ord}\left(f\right)$ is uniquely determined by $f$. That is, $f$ factors uniquely up to associates as the $k$-th power of the irreducible $t$ times a unit. Also $t$ is prime: $t\mid fg\Rightarrow\operatorname{ord}\left(fg\right)\ge1\Rightarrow\operatorname{ord}\left(f\right)\ge1$ or $\operatorname{ord}\left(g\right)\ge1$, i.e. $t\mid f$ or $t\mid g$.

By the definition in Unique Factorization Domain, $R=\mathbb R\left[\!\left[t\right]\!\right]$ is a unique factorization domain. $\blacksquare$

## 3.1-11

Let $M$ be a module and $M_1,M_2$ submodules of $M$. Prove:

(1) If $M_1\subset M_2$, then $M/M_2\cong\left(M/M_1\right)/\left(M_2/M_1\right)$;

(2) If $M=M_1\oplus M_2$, then $M_1\cong\left(M_1+M_2\right)/M_2$ and $M_2\cong\left(M_1+M_2\right)/M_1$.

### Solution to 3.1-11

(1) Define $\pi:M/M_1\to M/M_2$ by $\pi\left(m+M_1\right)=m+M_2$. It is well-defined: if $m+M_1=m'+M_1$, then $m-m'\in M_1\subset M_2$, so $m+M_2=m'+M_2$. It is plainly a surjective module homomorphism. Its kernel is $\ker\pi=\left\{m+M_1\mid m\in M_2\right\}=M_2/M_1$. By **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**,

$$
\left(M/M_1\right)/\left(M_2/M_1\right)=M/\ker\pi\cong\operatorname{Im}\pi=M/M_2.
$$

(2) Consider the quotient map $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$ restricted to the submodule $M_1$, i.e. $\rho|_{M_1}$. It is surjective: every coset $m_1+m_2+M_2=m_1+M_2$ is the image of $m_1\in M_1$. Its kernel is $\ker\rho|_{M_1}=\left\{m_1\in M_1\mid m_1\in M_2\right\}=M_1\cap M_2$. Since $M=M_1\oplus M_2$ is an internal direct sum, by **Theorem 3.1.10 (Criterion for a Direct Sum)**, $M_1\cap M_2=\left\{0\right\}$. By **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**,

$$
M_1/\left(M_1\cap M_2\right)=M_1\cong\left(M_1+M_2\right)/M_2.
$$

Similarly, $M_2\cong\left(M_1+M_2\right)/M_1$. $\blacksquare$

## 3.1-12

Let $M$ be a module and $M_1,M_2$ submodules of $M$. Prove that $\left(M_1+M_2\right)/M_2\cong M_1/\left(M_1\cap M_2\right)$.

### Solution to 3.1-12

Take the quotient map $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$, restricted to $M_1$ to give $\phi=\rho|_{M_1}:M_1\to\left(M_1+M_2\right)/M_2$. First show $\phi$ is surjective. Every coset of the form $m_1+m_2+M_2$ equals $m_1+M_2=\phi\left(m_1\right)$, so $\phi$ is onto.

Now find the kernel. By **Proposition 3.1.16 (Kernel and Image of a Homomorphism)**, $\ker\phi=\left\{m_1\in M_1\mid m_1\in M_2\right\}=M_1\cap M_2$. By **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**,

$$
M_1/\ker\phi=M_1/\left(M_1\cap M_2\right)\cong\left(M_1+M_2\right)/M_2.
$$

This is the second isomorphism theorem. $\blacksquare$

## 3.1-13

Let $M$ be a module and $M_1,M_2,\cdots,M_s$ submodules of $M$. Prove that $M=M_1\oplus\cdots\oplus M_s$ iff:

(1) $M=M_1+M_2+\cdots+M_s$;

(2) for every $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

### Solution to 3.1-13

Necessity. Suppose $M=M_1\oplus\cdots\oplus M_s$ is an internal direct sum. Then (1) is immediate. If $x\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)$, then $x$ is both an element of $M_j$ and a sum of elements of $M_1,\cdots,M_{j-1}$, which gives a nontrivial representation of $0$ (the components other than the $M_j$ component sum to $-x$), contradicting the uniqueness of the direct-sum decomposition. Hence $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

Sufficiency. Assume (1) and (2). It suffices to prove that the representation of $0$ in $M$ is unique. Suppose $m_1+m_2+\cdots+m_s=0$ with $m_i\in M_i$. Let $j$ be the largest index with $m_j\ne0$; then $j\ge2$ (otherwise $m_1=0$). Rearranging gives $m_j=-\left(m_1+\cdots+m_{j-1}\right)\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$, so $m_j=0$, a contradiction. Hence all $m_i=0$, and the representation of $0$ is unique. By **Theorem 3.1.10 (Criterion for a Direct Sum)**, $M=M_1\oplus\cdots\oplus M_s$. $\blacksquare$

## 3.1-14

If condition (2) above is replaced by $M_i\cap M_j=\left\{0\right\}$ for all $i\ne j$, does the conclusion still hold? Explain.

### Solution to 3.1-14

The conclusion does not hold. Pairwise zero intersections do not guarantee an internal direct-sum decomposition.

Counterexample. Take the two-dimensional vector space $M=\mathbb R^2$ over $\mathbb R$ as an $\mathbb R$-module, with basis $e_1,e_2$. Set $M_1=\mathbb R e_1$, $M_2=\mathbb R e_2$, $M_3=\mathbb R\left(e_1+e_2\right)$. These are all one-dimensional subspaces of $M$. The intersection of any two distinct one-dimensional subspaces is zero, i.e. $M_i\cap M_j=\left\{0\right\}$ for $i\ne j$. Also $M_1+M_2+M_3=\mathbb R e_1+\mathbb R e_2=M$, so condition (1) holds. But there is a nontrivial relation $e_1+e_2-\left(e_1+e_2\right)=0$, where $e_1\in M_1$, $e_2\in M_2$, and $-\left(e_1+e_2\right)\in M_3$, all three terms nonzero; hence the representation of $0$ is not unique, and $M\ne M_1\oplus M_2\oplus M_3$.

Thus pairwise zero intersection is only a necessary, not sufficient, condition for a direct sum, and cannot replace the nested-intersection condition above. $\blacksquare$

## 3.1-15

Let $M$ be a module and $M_1,M_2,\cdots,M_s$ submodules of $M$ with $M=M_1\oplus M_2\oplus\cdots\oplus M_s$. Let $N$ be a submodule of $M$ with $N=N_1\oplus N_2\oplus\cdots\oplus N_s$, where $N_i\subset M_i$ for $i=1,2,\cdots,s$. Prove that $M/N\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s$.

### Solution to 3.1-15

Every $m\in M$ can be uniquely written as $m=m_1+\cdots+m_s$ with $m_i\in M_i$. Define $\phi:M\to M_1/N_1\oplus\cdots\oplus M_s/N_s$ by $\phi\left(m_1+\cdots+m_s\right)=\left(m_1+N_1,\cdots,m_s+N_s\right)$. By the uniqueness of the direct-sum decomposition, $\phi$ is a well-defined module homomorphism.

It is surjective: given any $\left(m_1'+N_1,\cdots,m_s'+N_s\right)$, take $m=m_1'+\cdots+m_s'\in M$, and $\phi\left(m\right)$ is that element.

Find the kernel. By **Proposition 3.1.16 (Kernel and Image of a Homomorphism)**,

$$
\ker\phi=\left\{m_1+\cdots+m_s\mid m_i+N_i=0,1\le i\le s\right\}=\left\{m_1+\cdots+m_s\mid m_i\in N_i\right\}=N_1\oplus\cdots\oplus N_s=N.
$$

By **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**,

$$
M/N=M/\ker\phi\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s.
$$

$\blacksquare$

## 3.3-6

Let $R$ be a commutative unital ring such that every finitely generated $R$-module is free. Prove that $R$ is a field.

### Solution to 3.3-6

It suffices to show that every nonzero element of $R$ is a unit. Take any $a\in R$ with $a\ne0$. Consider the quotient module $R/\left(a\right)$; it is generated by $\overline 1=1+\left(a\right)$, hence is a finitely generated $R$-module. By assumption, $R/\left(a\right)$ is free.

Claim $R/\left(a\right)=0$. Otherwise it is a nonzero free module, and $\overline 1$ is a generator. By **Theorem 3.3.6 (Characterization of a Basis of a Free Module)**, if $\left\{\overline 1\right\}$ is a basis, then its annihilator is zero, i.e. $r\overline 1=0\Rightarrow r=0$. But $a\overline 1=a+\left(a\right)=0$ with $a\ne0$, a contradiction. Hence $R/\left(a\right)=0$.

$R/\left(a\right)=0$ is equivalent to $\left(a\right)=R$, i.e. $1\in\left(a\right)$, i.e. there exists $b\in R$ with $ab=1$. Thus $a$ is a unit.

By the arbitrariness of $a\ne0$, every nonzero element of $R$ is a unit, so $R$ is a field. $\blacksquare$

## 3.3-7

Let $R$ be a commutative unital ring and $\phi$ an endomorphism of the free module $R^m$. Prove that if $\phi$ is surjective, then $\phi$ is an isomorphism.

### Solution to 3.3-7

Take the standard basis $e_1,\cdots,e_m$ of $R^m$, and let $A\in R^{m\times m}$ be the matrix of the endomorphism $\phi$ in this basis.

Since $\phi$ is surjective, for each basis vector $e_j\in R^m$ there exists $x_j\in R^m$ with $\phi\left(x_j\right)=e_j$. Arranging $x_1,\cdots,x_m$ as columns gives a matrix $B$ with $AB=I_m$, where $I_m$ is the $m\times m$ identity matrix. Taking determinants of both sides and using multiplicativity, $\det\left(A\right)\det\left(B\right)=\det\left(I_m\right)=1$.

Hence $\det A$ is a unit in $R$. By Determinant and Invertibility, $A$ is invertible, i.e. there exists $A^{-1}$ with $AA^{-1}=I_m$. Thus $\phi$ is both surjective and injective ($\ker\phi=0$), hence bijective, and $\phi$ is a module isomorphism. $\blacksquare$

## 3.3-8

With the same setup as above, if $R$ is a field and $\phi$ is injective, prove that $\phi$ is an isomorphism. Does this conclusion hold for a general commutative unital ring?

### Solution to 3.3-8

When $R$ is a field, $R^m$ is an $m$-dimensional vector space. That $\phi$ is injective means the linear map $\phi$ has zero kernel. By linear algebra, an injective linear map on a finite-dimensional vector space is surjective, hence an isomorphism. Equivalently, in matrix terms, injectivity corresponds to the columns of $A$ being linearly independent, i.e. $\operatorname{rank}A=m$; hence the square matrix $A$ has full rank and is invertible, and $\phi$ is an isomorphism.

This conclusion does not hold for a general commutative unital ring.

Counterexample. Take $R=\mathbb Z$ (a commutative unital ring), $m=1$, and define $\phi:\mathbb Z\to\mathbb Z$ by $\phi\left(n\right)=2n$. This is an endomorphism of $\mathbb Z$. It is injective: if $2n=0$, then in the integral domain $\mathbb Z$, $n=0$. But it is not surjective: $1\notin 2\mathbb Z$, i.e. there is no $n$ with $2n=1$. Thus $\phi$ is injective but not bijective, and is not an isomorphism.

Therefore an injective endomorphism of a free module over a general commutative unital ring need not be an isomorphism. $\blacksquare$

## 3.4-4

Let $R=\mathbb Z\left[\alpha\right]$. Construct a finitely generated $R$-module $M$ that cannot be written as a direct sum of finitely many cyclic submodules. (The original problem lost the condition on $\alpha$; here we take the standard choice that $\alpha$ is an indeterminate, i.e. $R=\mathbb Z\left[x\right]$, which is not a principal ideal domain.)

### Solution to 3.4-4

Take $R=\mathbb Z\left[x\right]$, where $\alpha=x$ is an indeterminate. $R$ is not a principal ideal domain: the ideal $I=\left(2,x\right)$ is not generated by a single element.

Now view the ideal $I$ itself as an $R$-module. It is generated by $2$ and $x$, hence is a finitely generated $R$-module. We show that $I$ cannot be written as a direct sum of finitely many cyclic submodules.

Suppose, for contradiction, that $I=N_1\oplus\cdots\oplus N_k$, each $N_j$ cyclic, say $N_j=Ry_j$. Since $I$ is an ideal of the integral domain $R$, it is torsion-free as an $R$-module (if $r\in R$ is nonzero and $a\in I$ is nonzero, then $ra\ne0$). Hence in each cyclic module $Ry_j\cong R/\operatorname{ann}\left(y_j\right)$ we have $\operatorname{ann}\left(y_j\right)=0$, i.e. $N_j\cong R$. Thus $I\cong R^k$.

Now look at the rank. Tensor to the field of fractions $\mathbb Q\left(x\right)$: $I\otimes_R\mathbb Q\left(x\right)=\mathbb Q\left(x\right)$, of rank $1$. Hence $k=1$, i.e. $I\cong R$, so $I$ is principal, $I=\left(g\right)$.

But $I=\left(2,x\right)$ is not principal: the only units of $R=\mathbb Z\left[x\right]$ are $\pm1$. If $I=\left(g\right)$, then $2=gf$ and $x=gh$. From $2=gf$, $f,g$ must be constants $\pm1,\pm2$; combined with $x=gh$, this is impossible ($x$ does not divide $2$). More directly, every element $2f+xg$ of $I$ has even constant term, so $1\notin I$; hence $I\ne R=\left(1\right)$, and it cannot be generated by $\pm2$ or by $x$ alone.

Contradiction. Thus $I$ cannot be written as a direct sum of finitely many cyclic submodules. This agrees with the fact that **Theorem 3.4.5 (Structure Theorem for Finitely Generated Modules over a PID)** holds only over a principal ideal domain: without the PID hypothesis, a finitely generated module need not decompose into cyclic submodules. $\blacksquare$

## 3.4-5

Let $D=\mathbb Z\left[i\right]$ (the Gaussian integers, a principal ideal domain), and let $K$ be the submodule of $D^3$ generated by the vector $\left(2-3i,6+9i,-18i\right)$. Find the invariant factors and elementary divisors of $D^3/K$. (The beginning of the original problem is damaged; it is completed above in the mathematically valid form, with $i=\sqrt{-1}$.)

### Solution to 3.4-5

Set $v=\left(2-3i,6+9i,-18i\right)\in D^3$ and $K=Dv$. The quotient $D^3/K$ is determined by the Smith normal form of the $1\times3$ matrix $A=\begin{bmatrix}2-3i & 6+9i & -18i\end{bmatrix}$. The first invariant factor is the gcd (up to associates) of the three entries of $A$.

Compute in $D=\mathbb Z\left[i\right]$. Set $a=2-3i$; its norm $N\left(a\right)=2^2+3^2=13$, so $a$ is irreducible in $D$ ($13=\left(2-3i\right)\left(2+3i\right)$). Also $b=6+9i=3\left(2+3i\right)$, $c=-18i$, and $N\left(c\right)=18^2=324$.

Check whether $a=2-3i$ divides $b,c$:

$$
\frac{b}{a}=\frac{3\left(2+3i\right)\left(2+3i\right)}{13}=\frac{3\left(-5+12i\right)}{13}\notin\mathbb Z\left[i\right],
$$

$$
\frac{c}{a}=\frac{-18i\left(2+3i\right)}{13}=\frac{54-36i}{13}\notin\mathbb Z\left[i\right].
$$

Thus $a\nmid b$ and $a\nmid c$. Since the only nontrivial factors of $a$ are its associates ($a$ is irreducible), $a$ is not a common divisor of $b,c$. Similarly $2+3i$ does not divide $a$. Hence the gcd of $a,b,c$ is the unit $1$ in $D$.

Therefore the Smith normal form of $A$ is $\begin{bmatrix}1 & 0 & 0\end{bmatrix}$. By **Corollary 3.4.12 (Isomorphism Criterion for Finitely Generated Modules)**,

$$
D^3/K\cong D/\left(1\right)\oplus D/\left(0\right)\oplus D/\left(0\right)\cong D^2.
$$

Thus $D^3/K$ has rank $2$ and zero torsion. Its invariant factors (the torsion part $d_1,\cdots,d_k$) are empty, and its elementary divisors are empty; the module is isomorphic to the free module $D^2$. $\blacksquare$
