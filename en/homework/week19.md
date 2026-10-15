# Assignment 19

> **Theorem 3.1.17** (Fundamental Homomorphism Theorem for Modules) Let $\phi$ be an epimorphism from a module $M_1$ to $M_2$. Then the quotient module $M_1/\ker\phi$ is isomorphic to $M_2$; and if $N_1$ is a submodule of $M_1$ containing $\ker\phi$, then $M_1/N_1\cong M_2/\phi\left(N_1\right)$.

> **Proposition 3.1.16** (Kernel and Image of a Homomorphism) The kernel $\phi:M_1\to M_2$ of a module homomorphism $\ker\phi$ is a submodule of $M_1$, and the image $\operatorname{Im}\phi$ is a submodule of $M_2$.

> **Theorem 3.1.10** (Direct Sum Criterion)
>
> Let $M_1,\cdots,M_s$ be submodules of an $R$-module $M$. Then $M=M_1\oplus\cdots\oplus M_s$ if and only if
>
> (1) $M=M_1+\cdots+M_s$;
>
> (2) for any $2\le j\le s$,
> $$
> M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}.
> $$

### Problem 1

(Problem 3.1-11) Let $M$ be a module, and let $M_1,M_2$ both be submodules of $M$. Prove:

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

It is well defined: if $m+M_1=m'+M_1$, then $m-m'\in M_1\subset M_2$, so $m+M_2=m'+M_2$. It is clearly an epimorphism of modules. Its kernel is

$$
\begin{aligned}\ker\pi&=\left\{m+M_1\mid m\in M_2\right\}\\&=M_2/M_1.\end{aligned}
$$

By **Theorem 3.1.17** (Fundamental Homomorphism Theorem for Modules),

$$
\begin{aligned}\left(M/M_1\right)/\left(M_2/M_1\right)&=M/\ker\pi\\&\cong\operatorname{Im}\pi\\&=M/M_2.\end{aligned}
$$

(2) Consider the quotient map

$$
\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2
$$
restricted to the submodule $M_1$, namely $\rho|_{M_1}$. It is an epimorphism: every element

$$
m_1+m_2+M_2=m_1+M_2
$$

is the image of some $m_1\in M_1$. Its kernel is

$$
\begin{aligned}\ker\rho|_{M_1}&=\left\{m_1\in M_1\mid m_1\in M_2\right\}\\&=M_1\cap M_2.\end{aligned}
$$

Since $M=M_1\oplus M_2$ is an internal direct sum, by **Theorem 3.1.10** (Direct Sum Criterion), $M_1\cap M_2=\left\{0\right\}$. Again by **Theorem 3.1.17**,

$$
\begin{aligned}M_1/\left(M_1\cap M_2\right)&=M_1\\&\cong\left(M_1+M_2\right)/M_2.\end{aligned}
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
restrict to $M_1$, to obtain

$$
\phi=\rho|_{M_1}:M_1\to\left(M_1+M_2\right)/M_2.
$$

First prove that $\phi$ is an epimorphism. Every coset of the form $m_1+m_2+M_2$ equals $m_1+M_2$, i.e. $\phi\left(m_1\right)$, so $\phi$ is surjective.

Now find the kernel. By **Proposition 3.1.16** (Kernel and Image of a Homomorphism),

$$
\begin{aligned}\ker\phi&=\left\{m_1\in M_1\mid m_1\in M_2\right\}\\&=M_1\cap M_2.\end{aligned}
$$

By **Theorem 3.1.17** (Fundamental Homomorphism Theorem for Modules),

$$
\begin{aligned}M_1/\ker\phi&=M_1/\left(M_1\cap M_2\right)\\&\cong\left(M_1+M_2\right)/M_2.\end{aligned}
$$

This is the Second Isomorphism Theorem. $\blacksquare$

### Problem 3

(Problem 3.1-13) Let $M$ be a module, and let $M_1,M_2,\cdots,M_s$ be submodules of $M$. Prove that $M=M_1\oplus\cdots\oplus M_s$ if and only if

(1)

$$
M=M_1+M_2+\cdots+M_s;
$$

(2) for any $2\le j\le s$,

$$
M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}.
$$

### Solution to Problem 3

**Necessity** Suppose $M=M_1\oplus\cdots\oplus M_s$ is an internal direct sum; then (1) is clear. If

$$
x\in M_j\cap\left(M_1+\cdots+M_{j-1}\right),
$$
then $x$ can be written both as an element of $M_j$ and as a sum of elements of $M_1,\cdots,M_{j-1}$; this gives a nontrivial representation of $0$ (the components other than the $M_j$ component sum to $-x$), contradicting the uniqueness of the direct-sum decomposition. Hence

$$
M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}.
$$

**Sufficiency** Suppose (1) and (2) hold. It suffices to prove that the representation of the zero element in $M$ is unique. Suppose

$$
m_1+m_2+\cdots+m_s=0, m_i\in M_i.
$$

Let $j$ be the largest index for which $m_j\ne0$; then $j\ge2$ (otherwise $m_1=0$). Rearranging gives

$$
\begin{aligned}m_j&=-\left(m_1+\cdots+m_{j-1}\right)\\&\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)\\&=\left\{0\right\},\end{aligned}
$$

so $m_j=0$, a contradiction. Hence all $m_i=0$, and the representation of zero is unique. By **Theorem 3.1.10** (Direct Sum Criterion), $M=M_1\oplus\cdots\oplus M_s$. $\blacksquare$

### Problem 4

(Problem 3.1-14) If condition (2) of the previous problem is replaced by $M_i\cap M_j=\left\{0\right\}$ for all $\forall i\ne j$, does the conclusion still hold? Explain.

### Solution to Problem 4

The conclusion does not hold. Pairwise zero intersections do not guarantee an internal direct sum.

Counterexample. Take the two-dimensional real vector space $\mathbb R$ as an $M=\mathbb R^2$-module, with basis $\mathbb R$. Let $e_1,e_2$, $M_1=\mathbb R e_1$, $M_2=\mathbb R e_2$.$M_3=\mathbb R\left(e_1+e_2\right)$. The intersection of any two distinct one-dimensional subspaces is zero, i.e.

 $M$Also

$$
M_i\cap M_j=\left\{0\right\}, i\ne j.
$$

so condition (1) holds. But there is a nontrivial relation

$$
M_1+M_2+M_3=\mathbb R e_1+\mathbb R e_2=M,
$$

where 

$$
e_1+e_2-\left(e_1+e_2\right)=0,
$$

, $e_1\in M_1$, and $e_2\in M_2$; all three terms are nonzero, so the representation of zero is not unique, and $-\left(e_1+e_2\right)\in M_3$.$M\ne M_1\oplus M_2\oplus M_3$### Problem 5

(Problem 3.1-15) Let $\blacksquare$

 be a module, and let 

 $M$ be submodules of $M_1,M_2,\cdots,M_s$ with$M$Let 

$$
M=M_1\oplus M_2\oplus\cdots\oplus M_s,
$$
 be a submodule of $N$ with $M$, where $N=N_1\oplus N_2\oplus\cdots\oplus N_s$ for $N_i\subset M_i$. Prove that$i=1,2,\cdots,s$### Solution to Problem 5

$$
M/N\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s.
$$

 can be uniquely written as 

 $m\in M$ with $m=m_1+\cdots+m_s$. Define the map$m_i\in M_i$By the uniqueness of the direct-sum decomposition, 

$$
\phi:M\to M_1/N_1\oplus\cdots\oplus M_s/N_s, \phi\left(m_1+\cdots+m_s\right)=\left(m_1+N_1,\cdots,m_s+N_s\right).
$$

 is a well-defined module homomorphism.$\phi$, take 

 $\left(m_1'+N_1,\cdots,m_s'+N_s\right)$; then $m=m_1'+\cdots+m_s'\in M$ is exactly that element.$\phi\left(m\right)$By **Theorem 3.1.17** (Fundamental Homomorphism Theorem for Modules),

 

$$
\begin{aligned}\ker\phi&=\left\{m_1+\cdots+m_s\mid m_i+N_i=0,1\le i\le s\right\}\\&=\left\{m_1+\cdots+m_s\mid m_i\in N_i\right\}\\&=N_1\oplus\cdots\oplus N_s\\&=N.\end{aligned}
$$

 
$$
M/N=M/\ker\phi\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s.
$$
$\blacksquare$
