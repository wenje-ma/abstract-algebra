# Assignment 22

> **Theorem 3.5.2** (Number of Isomorphism Classes of Finite Abelian Groups) Let the natural number $n$ have prime factorization $n=p_1^{m_1}p_2^{m_2}\cdots p_s^{m_s}$, where $p_1,p_2,\cdots,p_s$ are distinct primes and $m_i> 0$. Then the number of abelian groups of order $n$, up to isomorphism, is $\prod_{i=1}^s p\left(m_i\right)$, where $p\left(m\right)$ denotes the number of distinct partitions of the natural number $m$.

> **Basic Knowledge** (Order of an Element in a Direct Product) Let $G=H_1\times H_2\times\cdots\times H_s$ be a direct product of finite abelian groups, and let $g=\left(h_1,h_2,\cdots,h_s\right)$. Then
> $$
> o\left(g\right)=\mathrm{lcm}\left(o\left(h_1\right),o\left(h_2\right),\cdots,o\left(h_s\right)\right).
> $$
> In particular, $o\left(g\right)\mid q$ if and only if $o\left(h_i\right)\mid q$ for every $i$.

> **Basic Knowledge** (Finite Subgroups of the Rational Multiplicative Group) In the multiplicative group $\mathbb Q^*$, an element has finite order if and only if it is $1$ or $-1$; that is, the only finite subgroup of $\mathbb Q^*$ is $\left\{\pm1\right\}$. Indeed, if $r=p/q\in\mathbb Q^*$ (in lowest terms) satisfies $r^n=1$, then $p^n=q^n$, so $p=\pm q$, i.e. $r=\pm1$.

### Problem 1

(Problem 3.5-4) Determine the number of isomorphism classes of abelian groups of order $936$.

### Solution to Problem 1

First factor $936$ into primes. We have

$$
936=8\times117=2^3\times3^2\times13.
$$

That is, $936=2^3\cdot3^2\cdot13^1$.

Compute the partition numbers of the exponents. The partitions of exponent $3$ are $3$, $2+1$, $1+1+1$, giving $p\left(3\right)=3$; the partitions of exponent $2$ are $2$, $1+1$, giving $p\left(2\right)=2$; the partition of exponent $1$ is just $1$, so $p\left(1\right)=1$.

By **Theorem 3.5.2** (Number of Isomorphism Classes of Finite Abelian Groups), the number of abelian groups of order $936$, up to isomorphism, is

$$
p\left(3\right)p\left(2\right)p\left(1\right)=3\times2\times1=6.
$$

Hence there are $6$ isomorphism classes of abelian groups of order $936$. $\blacksquare$

### Problem 2

(Problem 3.5-8) (1) Let $G=\mathbb Z_{p^e}$, where $p$ is prime and $e> 0$. Write $o\left(g\right)$ for the order of an element $g\in G$. Prove that if $l\leqslant e$, then $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l$; and if $l> e$, then $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^e$.

(2) Let $H_1,H_2,\cdots,H_s$ be finite abelian groups, let $q$ be a natural number, and set

$$
m_i=\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|.
$$

Let $G=H_1\times H_2\times\cdots\times H_s$. Then

$$
\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|=m_1m_2\cdots m_s.
$$

(3) Determine how many elements in $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ have order dividing $4$.

### Solution to Problem 2

(1) Regard $G=\mathbb Z_{p^e}$ as an additive cyclic group, whose elements are $0,1,2,\cdots,p^e-1$ modulo $p^e$. For $g=k\in\mathbb Z_{p^e}$, we have

$$
o\left(g\right)=\frac{p^e}{\gcd\left(k,p^e\right)}.
$$

Thus $o\left(g\right)\mid p^l$ is equivalent to $p^l g=0$, i.e. $p^l k\equiv0\pmod{p^e}$.

When $l\leqslant e$, this is equivalent to $k$ being divisible by $p^{e-l}$. Among the residue classes modulo $p^e$, exactly $p^l$ are divisible by $p^{e-l}$, so

$$
\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l.
$$

When $l> e$, $p^l$ is a multiple of $p^e$, so $p^l g=0$ holds automatically for every $g\in G$; hence this set is $G$ itself, which has $p^e$ elements.

(2) Take any $g=\left(h_1,h_2,\cdots,h_s\right)\in G$. By **Basic Knowledge** (Order of an Element in a Direct Product), $o\left(g\right)\mid q$ if and only if $o\left(h_i\right)\mid q$ simultaneously for every $i$. Hence the elements $g$ satisfying the condition are exactly the direct product of the corresponding sets $\left\{h\in H_i\mid o\left(h\right)\mid q\right\}$; by the multiplication principle,

$$
\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|=\prod_{i=1}^s\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|=m_1m_2\cdots m_s.
$$

(3) In $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$, we want elements whose order divides $4$, i.e. $4g=0$. Compute the number of choices for each component.

For $\mathbb Z_4$, the group order is $4$, so $4g=0$ holds for all $4$ elements; hence $m_1=4$.

For $\mathbb Z_8$, $4k\equiv0\pmod 8$ is equivalent to $k$ being even, i.e. $k\in\left\{0,2,4,6\right\}$, which gives $4$ choices; hence $m_2=4$.

For $\mathbb Z_{16}$, $4k\equiv0\pmod{16}$ is equivalent to $k\equiv0\pmod 4$, i.e. $k\in\left\{0,4,8,12\right\}$, which gives $4$ choices; hence $m_3=4$.

By (2), the desired number of elements is

$$
m_1m_2m_3=4\times4\times4=64.
$$

Hence there are $64$ elements in $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ whose order divides $4$. $\blacksquare$

### Problem 3

(Problem 3.5-12) Give the classification of abelian groups of order $8$, and determine all homomorphisms from each of these groups to $\mathbb Q^*$.

### Solution to Problem 3

Since $8=2^3$, the partitions of exponent $3$ are $3$, $2+1$, $1+1+1$, giving $p\left(3\right)=3$. By **Theorem 3.5.2** (Number of Isomorphism Classes of Finite Abelian Groups), there are $3$ isomorphism classes of abelian groups of order $8$, namely

$$
\mathbb Z_8,\ \mathbb Z_4\times\mathbb Z_2,\ \mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2.
$$

We now determine their homomorphisms to $\mathbb Q^*$. Let $\varphi:G\to\mathbb Q^*$ be a group homomorphism. Since $G$ is finite, $\varphi\left(G\right)$ is a finite subgroup of $\mathbb Q^*$. By **Basic Knowledge** (Finite Subgroups of the Rational Multiplicative Group), the only finite subgroup of $\mathbb Q^*$ is $\left\{\pm1\right\}$, so $\varphi\left(G\right)\subseteq\left\{\pm1\right\}$; that is, the image of each generator can only be $1$ or $-1$.

**Case 1: $G=\mathbb Z_8$.** Let $g$ be a generator of $G$, with $o\left(g\right)=8$. The homomorphism $\varphi$ is uniquely determined by $\varphi\left(g\right)\in\left\{\pm1\right\}$, and the condition $\varphi\left(g\right)^8=1$ holds automatically for both $\pm1$. Hence there are $2$ homomorphisms.

**Case 2: $G=\mathbb Z_4\times\mathbb Z_2$.** Let $g_1$ be a generator of $\mathbb Z_4$ and $g_2$ a generator of $\mathbb Z_2$. The homomorphism is uniquely determined by $\varphi\left(g_1\right),\varphi\left(g_2\right)\in\left\{\pm1\right\}$, and the constraints $\varphi\left(g_1\right)^4=1$ and $\varphi\left(g_2\right)^2=1$ are automatically satisfied for $\pm1$. Hence there are $2\times2=4$ homomorphisms.

**Case 3: $G=\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2$.** Let $g_1,g_2,g_3$ be three generators of order $2$. The homomorphism is uniquely determined by

$$
\varphi\left(g_1\right),\varphi\left(g_2\right),\varphi\left(g_3\right)\in\left\{\pm1\right\},
$$

and all constraints are automatically satisfied. Hence there are $2^3=8$ homomorphisms.

In summary, the abelian groups of order $8$ fall into $3$ classes, and the numbers of homomorphisms from them to $\mathbb Q^*$ are respectively $2$, $4$, and $8$. $\blacksquare$
