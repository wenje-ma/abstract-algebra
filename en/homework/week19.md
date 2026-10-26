# Assignment 19

> **Theorem 3.1.17** (Fundamental Homomorphism Theorem for Modules) Let $\phi$ be an epimorphism from a module $M_1$ to a module $M_2$. Then the quotient module $M_1/\ker\phi$ is isomorphic to $M_2$; moreover, if $N_1$ is a submodule of $M_1$ containing $\ker\phi$, then $M_1/N_1\cong M_2/\phi\left(N_1\right)$.

> **Proposition 3.1.16** (Kernel and Image of a Homomorphism) For a module homomorphism $\phi:M_1\to M_2$, the kernel $\ker\phi$ is a submodule of $M_1$, and the image $\operatorname{Im}\phi$ is a submodule of $M_2$.

> **Theorem 3.1.10** (Direct Sum Criterion)
> 
> Let $M_1,\cdots,M_s$ be submodules of an $R$-module $M$. Then $M=M_1\oplus\cdots\oplus M_s$ if and only if
> 
> (1) $M=M_1+\cdots+M_s$;
> 
> (2) for every $2\le j\le s$,
> $$
> M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}.
> $$

### Problem 1

(Problem 3.1-11) Let $M$ be a module, and let $M_1,M_2$ be submodules of $M$. Prove:

(1) if $M_1\subset M_2$, then

$$
M/M_2\cong\left(M/M_1\right)/\left(M_2/M_1\right);
$$

(2) if $M=M_1\oplus M_2$, then $M_1\cong\left(M_1+M_2\right)/M_2$ and $M_2\cong\left(M_1+M_2\right)/M_1$.

### Solution to Problem 1

(1) Define the map $\pi:M/M_1\to M/M_2$ by

$$
\pi\left(m+M_1\right)=m+M_2.
$$

It is well defined: if $m+M_1=m'+M_1$, then $m-m'\in M_1\subset M_2$, and hence $m+M_2=m'+M_2$. It is clearly an epimorphism of modules. Its kernel is

$$
\ker\pi=\left\{m+M_1\mid m\in M_2\right\}=M_2/M_1.
$$

By **Theorem 3.1.17** (Fundamental Homomorphism Theorem for Modules),

$$
\left(M/M_1\right)/\left(M_2/M_1\right)=M/\ker\pi\cong\operatorname{Im}\pi=M/M_2.
$$

(2) Consider the restriction to the submodule $M_1$ of the quotient map

$$
\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2,
$$

namely $\rho|_{M_1}$. It is an epimorphism: every element

$$
m_1+m_2+M_2=m_1+M_2
$$

is the image of some $m_1\in M_1$. Its kernel is

$$
\ker\rho|_{M_1}=\left\{m_1\in M_1\mid m_1\in M_2\right\}=M_1\cap M_2.
$$

Since $M=M_1\oplus M_2$ is an internal direct sum, by **Theorem 3.1.10** (Direct Sum Criterion), $M_1\cap M_2=\left\{0\right\}$. Again by **Theorem 3.1.17**,

$$
M_1/\left(M_1\cap M_2\right)=M_1\cong\left(M_1+M_2\right)/M_2.
$$

Symmetrically, $M_2\cong\left(M_1+M_2\right)/M_1$. $\blacksquare$

### Problem 2

(Problem 3.1-12) Let $M$ be a module, and let $M_1,M_2$ be submodules of $M$. Prove that

$$
\left(M_1+M_2\right)/M_2\cong M_1/\left(M_1\cap M_2\right).
$$

### Solution to Problem 2

Take the quotient map

$$
\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2,
$$

and restrict it to $M_1$ to obtain

$$
\phi=\rho|_{M_1}:M_1\to\left(M_1+M_2\right)/M_2.
$$

First show that $\phi$ is an epimorphism. Every coset of the form $m_1+m_2+M_2$ equals $m_1+M_2$, i.e. $\phi\left(m_1\right)$, so $\phi$ is surjective.

Now determine its kernel. By **Proposition 3.1.16** (Kernel and Image of a Homomorphism),

$$
\ker\phi=\left\{m_1\in M_1\mid m_1\in M_2\right\}=M_1\cap M_2.
$$

By **Theorem 3.1.17** (Fundamental Homomorphism Theorem for Modules),

$$
M_1/\ker\phi=M_1/\left(M_1\cap M_2\right)\cong\left(M_1+M_2\right)/M_2.
$$

This is the Second Isomorphism Theorem. $\blacksquare$

### Problem 3

(Problem 3.1-13) Let $M$ be a module, and let $M_1,M_2,\cdots,M_s$ be submodules of $M$. Prove that $M=M_1\oplus\cdots\oplus M_s$ if and only if

(1)

$$
M=M_1+M_2+\cdots+M_s;
$$

(2) for every $2\le j\le s$,

$$
M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}.
$$

### Solution to Problem 3

**Necessity** Suppose $M=M_1\oplus\cdots\oplus M_s$ is an internal direct sum; then (1) is clear. If

$$
x\in M_j\cap\left(M_1+\cdots+M_{j-1}\right),
$$

then $x$ can be written both as an element of $M_j$ and as a sum of elements of $M_1,\cdots,M_{j-1}$; this gives a nontrivial representation of $0$ (all components except the $M_j$ component sum to $-x$), contradicting the uniqueness of the direct-sum decomposition. Hence

$$
M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}.
$$

**Sufficiency** Suppose (1) and (2) hold. It suffices to show that the representation of the zero element in $M$ is unique. Suppose

$$
m_1+m_2+\cdots+m_s=0,\quad m_i\in M_i.
$$

Let $j$ be the largest index for which $m_j\ne0$; then $j\ge2$ (otherwise $m_1=0$). Rearranging gives

$$
m_j=-\left(m_1+\cdots+m_{j-1}\right)\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\},
$$

so $m_j=0$, a contradiction. Hence all $m_i=0$, and the representation of zero is unique. By **Theorem 3.1.10** (Direct Sum Criterion), $M=M_1\oplus\cdots\oplus M_s$. $\blacksquare$

### Problem 4

(Problem 3.1-14) If condition (2) of the previous problem is replaced by $M_i\cap M_j=\left\{0\right\}$ for all $i\ne j$, does the conclusion still hold? Explain.

### Solution to Problem 4

The conclusion does not hold. Pairwise zero intersections do not guarantee an internal direct-sum decomposition.

Counterexample. Take the two-dimensional real vector space $M=\mathbb R^2$ as an $\mathbb R$-module, with basis $e_1,e_2$. Set $M_1=\mathbb R e_1$, $M_2=\mathbb R e_2$, $M_3=\mathbb R\left(e_1+e_2\right)$.

These are all one-dimensional subspaces of $M$. The intersection of any two distinct one-dimensional subspaces is zero, i.e.

$$
M_i\cap M_j=\left\{0\right\},\quad i\ne j.
$$

Moreover,

$$
M_1+M_2+M_3=\mathbb R e_1+\mathbb R e_2=M,
$$

so condition (1) holds. However, there is a nontrivial relation

$$
e_1+e_2-\left(e_1+e_2\right)=0,
$$

where $e_1\in M_1$, $e_2\in M_2$, and $-\left(e_1+e_2\right)\in M_3$; all three terms are nonzero, so the representation of zero is not unique, and $M\ne M_1\oplus M_2\oplus M_3$.

Thus pairwise zero intersection is only a necessary condition for a direct sum, not a sufficient one, and cannot replace the nested-intersection condition of the previous problem. $\blacksquare$

### Problem 5

(Problem 3.1-15) Let $M$ be a module, and let $M_1,M_2,\cdots,M_s$ be submodules of $M$ such that

$$
M=M_1\oplus M_2\oplus\cdots\oplus M_s.
$$

Let $N$ be a submodule of $M$ such that $N=N_1\oplus N_2\oplus\cdots\oplus N_s$, where $N_i\subset M_i$ for $i=1,2,\cdots,s$. Prove that

$$
M/N\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s.
$$

### Solution to Problem 5

Every $m\in M$ can be uniquely written as $m=m_1+\cdots+m_s$ with $m_i\in M_i$. Define the map

$$
\phi:M\to M_1/N_1\oplus\cdots\oplus M_s/N_s,\quad \phi\left(m_1+\cdots+m_s\right)=\left(m_1+N_1,\cdots,m_s+N_s\right).
$$

By the uniqueness of the direct-sum decomposition, $\phi$ is a well-defined module homomorphism.

It is an epimorphism: given any $\left(m_1'+N_1,\cdots,m_s'+N_s\right)$, take $m=m_1'+\cdots+m_s'\in M$, and then $\phi\left(m\right)$ is precisely that element.

Now determine its kernel. By **Proposition 3.1.16** (Kernel and Image of a Homomorphism),

$$
\ker\phi=\left\{m_1+\cdots+m_s\mid m_i+N_i=0,\ 1\le i\le s\right\}=\left\{m_1+\cdots+m_s\mid m_i\in N_i\right\}=N_1\oplus\cdots\oplus N_s=N.
$$

By **Theorem 3.1.17** (Fundamental Homomorphism Theorem for Modules),

$$
M/N=M/\ker\phi\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s.
$$

$\blacksquare$
