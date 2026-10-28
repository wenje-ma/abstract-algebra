# week19

> **Theorem 3.1.10 (Criterion for a Direct Sum)**<br>Let $M_1,\cdots,M_s$ be submodules of an $R$-module $M$. Then $M=M_1\oplus\cdots\oplus M_s$ iff: (1) $M=M_1+\cdots+M_s$; (2) for every $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

> **Proposition 3.1.16 (Kernel and Image of a Homomorphism)**<br>The kernel $\ker\phi$ of a module homomorphism $\phi:M_1\to M_2$ is a submodule of $M_1$, and the image $\operatorname{Im}\phi$ is a submodule of $M_2$.

> **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**<br>If $\phi:M_1\to M_2$ is a surjective module homomorphism, then the quotient module $M_1/\ker\phi$ is isomorphic to $M_2$; moreover, if $N_1$ is a submodule of $M_1$ containing $\ker\phi$, then $M_1/N_1\cong M_2/\phi\left(N_1\right)$.

---

## 3.1-11

Let $M$ be a module and $M_1,M_2$ submodules of $M$. Prove:

(1) If $M_1\subset M_2$, then $M/M_2\cong\left(M/M_1\right)/\left(M_2/M_1\right)$;

(2) If $M=M_1\oplus M_2$, then $M_1\cong\left(M_1+M_2\right)/M_2$ and $M_2\cong\left(M_1+M_2\right)/M_1$.

### Solution 3.1-11

(1) Define $\pi:M/M_1\to M/M_2$ by $\pi\left(m+M_1\right)=m+M_2$. It is well-defined: if $m+M_1=m'+M_1$, then $m-m'\in M_1\subset M_2$, so $m+M_2=m'+M_2$. It is plainly a surjective module homomorphism. Its kernel is $\ker\pi=\left\{m+M_1\mid m\in M_2\right\}=M_2/M_1$. By **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**,

$$
\left(M/M_1\right)/\left(M_2/M_1\right)=M/\ker\pi\cong\operatorname{Im}\pi=M/M_2.
$$

(2) Consider the quotient map $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$ restricted to the submodule $M_1$, i.e. $\rho|_{M_1}$. It is surjective: every coset $m_1+m_2+M_2=m_1+M_2$ is the image of $m_1\in M_1$. Its kernel is $\ker\rho|_{M_1}=\left\{m_1\in M_1\mid m_1\in M_2\right\}=M_1\cap M_2$. Since $M=M_1\oplus M_2$ is an internal direct sum, by **Theorem 3.1.10 (Criterion for a Direct Sum)**, $M_1\cap M_2=\left\{0\right\}$. By **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**,

$$
M_1/\left(M_1\cap M_2\right)=M_1\cong\left(M_1+M_2\right)/M_2.
$$

Similarly, $M_2\cong\left(M_1+M_2\right)/M_1$. $\blacksquare$

---

## 3.1-12

Let $M$ be a module and $M_1,M_2$ submodules of $M$. Prove that $\left(M_1+M_2\right)/M_2\cong M_1/\left(M_1\cap M_2\right)$.

### Solution 3.1-12

Take the quotient map $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$, restricted to $M_1$ to give $\phi=\rho|_{M_1}:M_1\to\left(M_1+M_2\right)/M_2$. First show $\phi$ is surjective. Every coset of the form $m_1+m_2+M_2$ equals $m_1+M_2=\phi\left(m_1\right)$, so $\phi$ is onto.

Now find the kernel. By **Proposition 3.1.16 (Kernel and Image of a Homomorphism)**, $\ker\phi=\left\{m_1\in M_1\mid m_1\in M_2\right\}=M_1\cap M_2$. By **Theorem 3.1.17 (Fundamental Homomorphism Theorem for Modules)**,

$$
M_1/\ker\phi=M_1/\left(M_1\cap M_2\right)\cong\left(M_1+M_2\right)/M_2.
$$

This is the second isomorphism theorem. $\blacksquare$

---

## 3.1-13

Let $M$ be a module and $M_1,M_2,\cdots,M_s$ submodules of $M$. Prove that $M=M_1\oplus\cdots\oplus M_s$ iff:

(1) $M=M_1+M_2+\cdots+M_s$;

(2) for every $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

### Solution 3.1-13

**Necessity.** Suppose $M=M_1\oplus\cdots\oplus M_s$ is an internal direct sum. Then (1) is immediate. If $x\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)$, then $x$ is both an element of $M_j$ and a sum of elements of $M_1,\cdots,M_{j-1}$, which gives a nontrivial representation of $0$ (the components other than the $M_j$ component sum to $-x$), contradicting the uniqueness of the direct-sum decomposition. Hence $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

**Sufficiency.** Assume (1) and (2). It suffices to prove that the representation of $0$ in $M$ is unique. Suppose $m_1+m_2+\cdots+m_s=0$ with $m_i\in M_i$. Let $j$ be the largest index with $m_j\ne0$; then $j\ge2$ (otherwise $m_1=0$). Rearranging gives $m_j=-\left(m_1+\cdots+m_{j-1}\right)\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$, so $m_j=0$, a contradiction. Hence all $m_i=0$, and the representation of $0$ is unique. By **Theorem 3.1.10 (Criterion for a Direct Sum)**, $M=M_1\oplus\cdots\oplus M_s$. $\blacksquare$

---

## 3.1-14

If condition (2) above is replaced by $M_i\cap M_j=\left\{0\right\}$ for all $i\ne j$, does the conclusion still hold? Explain.

### Solution 3.1-14

The conclusion does not hold. Pairwise zero intersections do not guarantee an internal direct-sum decomposition.

Counterexample. Take the two-dimensional vector space $M=\mathbb R^2$ over $\mathbb R$ as an $\mathbb R$-module, with basis $e_1,e_2$. Set $M_1=\mathbb R e_1$, $M_2=\mathbb R e_2$, $M_3=\mathbb R\left(e_1+e_2\right)$. These are all one-dimensional subspaces of $M$. The intersection of any two distinct one-dimensional subspaces is zero, i.e. $M_i\cap M_j=\left\{0\right\}$ for $i\ne j$. Also $M_1+M_2+M_3=\mathbb R e_1+\mathbb R e_2=M$, so condition (1) holds. But there is a nontrivial relation $e_1+e_2-\left(e_1+e_2\right)=0$, where $e_1\in M_1$, $e_2\in M_2$, and $-\left(e_1+e_2\right)\in M_3$, all three terms nonzero; hence the representation of $0$ is not unique, and $M\ne M_1\oplus M_2\oplus M_3$.

Thus pairwise zero intersection is only a necessary, not sufficient, condition for a direct sum, and cannot replace the nested-intersection condition above. $\blacksquare$

---

## 3.1-15

Let $M$ be a module and $M_1,M_2,\cdots,M_s$ submodules of $M$ with $M=M_1\oplus M_2\oplus\cdots\oplus M_s$. Let $N$ be a submodule of $M$ with $N=N_1\oplus N_2\oplus\cdots\oplus N_s$, where $N_i\subset M_i$ for $i=1,2,\cdots,s$. Prove that $M/N\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s$.

### Solution 3.1-15

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
