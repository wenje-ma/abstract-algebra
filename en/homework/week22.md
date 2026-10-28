# week22

> **Basic Knowledge: Order of an Element in a Direct Product**<br>Let $G=H_1\times H_2\times\cdots\times H_s$ be a direct product of finite abelian groups, and $g=\left(h_1,h_2,\cdots,h_s\right)$. Then $o\left(g\right)=\mathrm{lcm}\left(o\left(h_1\right),o\left(h_2\right),\cdots,o\left(h_s\right)\right)$. In particular, $o\left(g\right)\mid q$ iff $o\left(h_i\right)\mid q$ for every $i$.

> **Basic Knowledge: Finite Subgroups of the Rational Multiplicative Group**<br>An element of order finite in $\mathbb Q^*$ is either $1$ or $-1$; hence the only finite subgroup of $\mathbb Q^*$ is $\left\{\pm1\right\}$. Indeed, if $r=p/q\in\mathbb Q^*$ (in lowest terms) satisfies $r^n=1$, then $p^n=q^n$, so $p=\pm q$, i.e. $r=\pm1$.

> **Theorem 3.5.2 (Number of Isomorphism Classes of Finite Abelian Groups)**<br>Let $n=p_1^{m_1}p_2^{m_2}\cdots p_s^{m_s}$ be the prime factorization of $n$, with $p_1,p_2,\cdots,p_s$ distinct primes and $m_i> 0$. Then the number of isomorphism classes of abelian groups of order $n$ is $\prod_{i=1}^s p\left(m_i\right)$, where $p\left(m\right)$ is the number of distinct partitions of the natural number $m$.

---

## 3.5-4

Determine the number of isomorphism classes of abelian groups of order $936$.

### Solution 3.5-4

First factor $936$. Since $936=8\times117=2^3\times3^2\times13$, we have $936=2^3\cdot3^2\cdot13^1$.

Compute the partition numbers of the exponents. The partitions of $3$ are $3$, $2+1$, $1+1+1$, so $p\left(3\right)=3$; the partitions of $2$ are $2$, $1+1$, so $p\left(2\right)=2$; the only partition of $1$ is $1$, so $p\left(1\right)=1$.

By **Theorem 3.5.2 (Number of Isomorphism Classes of Finite Abelian Groups)**, the number of isomorphism classes of abelian groups of order $936$ is $p\left(3\right)p\left(2\right)p\left(1\right)=3\times2\times1=6$.

Hence there are $6$ isomorphism classes of abelian groups of order $936$. $\blacksquare$

---

## 3.5-8

(1) Let $G=\mathbb Z_{p^e}$, $p$ prime, $e> 0$, and write $o\left(g\right)$ for the order of $g\in G$. Prove: if $l\le e$, then $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l$; if $l> e$, then $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^e$.

(2) Let $H_1,H_2,\cdots,H_s$ be finite abelian groups, $q$ a natural number, and set $m_i=\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|$, $G=H_1\times H_2\times\cdots\times H_s$. Then $\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|=m_1m_2\cdots m_s$.

(3) Determine how many elements of $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ have order dividing $4$.

### Solution 3.5-8

(1) View $G=\mathbb Z_{p^e}$ as an additive cyclic group with elements $0,1,2,\cdots,p^e-1$ modulo $p^e$. For $g=k\in\mathbb Z_{p^e}$, $o\left(g\right)=\frac{p^e}{\gcd\left(k,p^e\right)}$. Thus $o\left(g\right)\mid p^l$ iff $p^l g=0$, i.e. $p^l k\equiv0\pmod{p^e}$.

When $l\le e$, this is equivalent to $k$ being divisible by $p^{e-l}$. Among the residue classes modulo $p^e$, exactly $p^l$ are divisible by $p^{e-l}$, so $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l$.

When $l> e$, $p^l$ is a multiple of $p^e$, and $p^l g=0$ holds automatically for every $g\in G$, so the set is all of $G$, with $p^e$ elements.

(2) Take any $g=\left(h_1,h_2,\cdots,h_s\right)\in G$. By **Basic Knowledge: Order of an Element in a Direct Product**, $o\left(g\right)\mid q$ iff $o\left(h_i\right)\mid q$ for every $i$. Hence the $g$ satisfying the condition are exactly the direct product of the choices $\left\{h\in H_i\mid o\left(h\right)\mid q\right\}$, and by the multiplication principle,

$$
\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|=\prod_{i=1}^s\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|=m_1m_2\cdots m_s.
$$

(3) In $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$, requiring the order to divide $4$ means $4g=0$. Count the choices in each component.

For $\mathbb Z_4$, the group has order $4$, so $4g=0$ for all $4$ elements; $m_1=4$.

For $\mathbb Z_8$, $4k\equiv0\pmod 8$ iff $k$ is even, i.e. $k\in\left\{0,2,4,6\right\}$, $4$ choices; $m_2=4$.

For $\mathbb Z_{16}$, $4k\equiv0\pmod{16}$ iff $k\equiv0\pmod 4$, i.e. $k\in\left\{0,4,8,12\right\}$, $4$ choices; $m_3=4$.

By (2), the desired number is $m_1m_2m_3=4\times4\times4=64$.

Hence $64$ elements of $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ have order dividing $4$. $\blacksquare$

---

## 3.5-12

Classify the abelian groups of order $8$, and determine all homomorphisms from each of these groups to $\mathbb Q^*$.

### Solution 3.5-12

Since $8=2^3$, the partitions of $3$ are $3$, $2+1$, $1+1+1$, so $p\left(3\right)=3$. By **Theorem 3.5.2 (Number of Isomorphism Classes of Finite Abelian Groups)**, there are $3$ isomorphism classes of abelian groups of order $8$, namely $\mathbb Z_8$, $\mathbb Z_4\times\mathbb Z_2$, and $\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2$.

Now determine their homomorphisms to $\mathbb Q^*$. Let $\varphi:G\to\mathbb Q^*$ be a group homomorphism. Since $G$ is finite, $\varphi\left(G\right)$ is a finite subgroup of $\mathbb Q^*$. By **Basic Knowledge: Finite Subgroups of the Rational Multiplicative Group**, the only finite subgroup of $\mathbb Q^*$ is $\left\{\pm1\right\}$, so $\varphi\left(G\right)\subseteq\left\{\pm1\right\}$, i.e. each generator maps to either $1$ or $-1$.

**Case 1: $G=\mathbb Z_8$.** Let $g$ be a generator of $G$, $o\left(g\right)=8$. The homomorphism $\varphi$ is determined by $\varphi\left(g\right)\in\left\{\pm1\right\}$, and $\varphi\left(g\right)^8=1$ holds automatically for $\pm1$. Hence there are $2$ homomorphisms.

**Case 2: $G=\mathbb Z_4\times\mathbb Z_2$.** Let $g_1$ generate $\mathbb Z_4$ and $g_2$ generate $\mathbb Z_2$. The homomorphism is determined by $\varphi\left(g_1\right),\varphi\left(g_2\right)\in\left\{\pm1\right\}$, and the constraints $\varphi\left(g_1\right)^4=1$, $\varphi\left(g_2\right)^2=1$ hold automatically for $\pm1$. Hence there are $2\times2=4$ homomorphisms.

**Case 3: $G=\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2$.** Let $g_1,g_2,g_3$ be the three generators of order $2$. The homomorphism is determined by $\varphi\left(g_1\right),\varphi\left(g_2\right),\varphi\left(g_3\right)\in\left\{\pm1\right\}$, and all constraints hold automatically. Hence there are $2^3=8$ homomorphisms.

In summary, the abelian groups of order $8$ fall into $3$ classes, with $2$, $4$, and $8$ homomorphisms to $\mathbb Q^*$ respectively. $\blacksquare$
