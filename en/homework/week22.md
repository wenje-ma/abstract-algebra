# Assignment 22

> **Theorem 3.5.2** (Number of Isomorphism Classes of Finite Abelian Groups) Let the natural number $n$ have prime factorization $n=p_1^{m_1}p_2^{m_2}\cdots p_s^{m_s}$, where $p_1,p_2,\cdots,p_s$ are distinct primes and $m_i>0$. Then the number of abelian groups of order $n$, up to isomorphism, is $\prod_{i=1}^s p\left(m_i\right)$, where $p\left(m\right)$ denotes the number of distinct partitions of the natural number $m$.

> **Basic Knowledge** (Order of an Element in a Direct Product) Let $G=H_1\times H_2\times\cdots\times H_s$ be a direct product of finite abelian groups, and let $g=\left(h_1,h_2,\cdots,h_s\right)$. Then
> $$
> o\left(g\right)=\mathrm{lcm}\left(o\left(h_1\right),o\left(h_2\right),\cdots,o\left(h_s\right)\right).
> $$
> In particular, $o\left(g\right)\mid q$ if and only if $o\left(h_i\right)\mid q$ for every $i$.

> **Basic Knowledge** (Finite Subgroups of the Rational Multiplicative Group) In the multiplicative group $\mathbb Q^*$, every element has finite order if and only if it is $1$ or $-1$; that is, the only finite subgroup of $\mathbb Q^*$ is $\left\{\pm1\right\}$. Indeed, if $r=p/q\in\mathbb Q^*$ (in lowest terms) satisfies $r^n=1$, then $p^n=q^n$, so $p=\pm q$, i.e. $r=\pm1$.

### Problem 1

(Problem 3.5-4) Determine the number of isomorphism classes of abelian groups of order $936$.

### Solution to Problem 1

First factor $936$ into primes. We have

$$
\begin{aligned}936&=8\times117\\&=2^3\times3^2\times13.\end{aligned}
$$

That is, $936=2^3\cdot3^2\cdot13^1$.

Compute the partition numbers of the exponents. The partitions of exponent $3$ are $3$, $2+1$, $1+1+1$, giving $p\left(3\right)=3$; the partitions of exponent $2$ are $2$, $1+1$, giving $p\left(2\right)=2$; the partition of exponent $1$ is just $1$, so $p\left(1\right)=1$.

By **Theorem 3.5.2** (Number of Isomorphism Classes of Finite Abelian Groups), the number of abelian groups of order $936$, up to isomorphism, is

$$
\begin{aligned}p\left(3\right)p\left(2\right)p\left(1\right)&=3\times2\times1\\&=6.\end{aligned}
$$

Hence there are $936$ isomorphism classes of abelian groups of order $6$. $\blacksquare$

### Problem 2

(Problem 3.5-8) (1) Let $G=\mathbb Z_{p^e}$, where $p$ is prime and $e>0$. Write $G$ for the order of an element $g$. Prove that if $o\left(g\right)$, then $l\leqslant e$; and if $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l$, then $l>e$.$\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^e$ be finite abelian groups, and let 

 $H_1,H_2,\cdots,H_s$ be a natural number. Set$q$and 

$$
m_i=\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|,
$$
$G=H_1\times H_2\times\cdots\times H_s$(3) Determine how many elements in 

$$
\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|=m_1m_2\cdots m_s.
$$

 have order dividing $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$.$4$ as an additive cyclic group, whose elements are 

 

 $G=\mathbb Z_{p^e}$ modulo $0,1,2,\cdots,p^e-1$. For $p^e$,$g=k\in\mathbb Z_{p^e}$Thus 

$$
o\left(g\right)=\frac{p^e}{\gcd\left(k,p^e\right)}.
$$

 is equivalent to $o\left(g\right)\mid p^l$, i.e. $p^l g=0$.$p^l k\equiv0\pmod{p^e}$, this is equivalent to 

 $l\leqslant e$ being divisible by $k$. Among the residue classes modulo $p^{e-l}$, exactly $p^e$ are divisible by $p^{e-l}$, so$p^l$When 

$$
\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l.
$$

, $l>e$ is a multiple of $p^l$, so $p^e$ automatically for all $p^l g=0$; hence this set is $g\in G$ itself, with $G$ elements.$p^e$. By **Basic Knowledge** (Order of an Element in a Direct Product), 

 $g=\left(h_1,h_2,\cdots,h_s\right)\in G$ if and only if $o\left(g\right)\mid q$ for every $o\left(h_i\right)\mid q$ simultaneously. Hence the set of $i$ satisfying the condition is exactly the direct product of the sets $g$; by the multiplication principle,$\left\{h\in H_i\mid o\left(h\right)\mid q\right\}$(3) In 

$$
\begin{aligned}\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|&=\prod_{i=1}^s\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|\\&=m_1m_2\cdots m_s.\end{aligned}
$$

, we want elements whose order divides $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$, i.e. $4$. Compute the number of choices for each component.$4g=0$, the group order is 

 $\mathbb Z_4$, so $4$ holds for all $4g=0$ elements; $4$.$m_1=4$, 

 $\mathbb Z_8$ is equivalent to $4k\equiv0\pmod 8$ being even, i.e. $k$, giving $k\in\left\{0,2,4,6\right\}$ choices; $4$.$m_2=4$, 

 $\mathbb Z_{16}$ is equivalent to $4k\equiv0\pmod{16}$, i.e. $k\equiv0\pmod 4$, giving $k\in\left\{0,4,8,12\right\}$ choices; $4$.$m_3=4$Hence there are 

 

$$
\begin{aligned}m_1m_2m_3&=4\times4\times4\\&=64.\end{aligned}
$$

 elements in $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ whose order divides $64$. $4$### Problem 3$\blacksquare$

, and determine all homomorphisms from each of these groups to 

 $8$.$\mathbb Q^*$, the partitions of exponent 

 

 $8=2^3$ are $3$, $3$, $2+1$, giving $1+1+1$. By **Theorem 3.5.2** (Number of Isomorphism Classes of Finite Abelian Groups), there are $p\left(3\right)=3$ isomorphism classes of abelian groups of order $8$, namely$3$We now determine their homomorphisms to 

$$
\mathbb Z_8,\mathbb Z_4\times\mathbb Z_2,\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2.
$$

. Let $\mathbb Q^*$ be a group homomorphism. Since $\varphi:G\to\mathbb Q^*$ is finite, $G$ is a finite subgroup of $\varphi\left(G\right)$. By **Basic Knowledge** (Finite Subgroups of the Rational Multiplicative Group), the only finite subgroup of $\mathbb Q^*$ is $\mathbb Q^*$, so $\left\{\pm1\right\}$; i.e. the image of each generator can only be $\varphi\left(G\right)\subseteq\left\{\pm1\right\}$ or $1$.$-1$** Let 

 $G=\mathbb Z_8$ be a generator of $g$, with $G$. The homomorphism $o\left(g\right)=8$ is uniquely determined by $\varphi$, and $\varphi\left(g\right)\in\left\{\pm1\right\}$ holds automatically for both $\varphi\left(g\right)^8=1$. Hence there are $\pm1$ homomorphisms.$2$** Let 

 $G=\mathbb Z_4\times\mathbb Z_2$ generate $g_1$ and $\mathbb Z_4$ generate $g_2$. The homomorphism is uniquely determined by $\mathbb Z_2$, and the constraints $\varphi\left(g_1\right),\varphi\left(g_2\right)\in\left\{\pm1\right\}$, $\varphi\left(g_1\right)^4=1$ are automatically satisfied for $\varphi\left(g_2\right)^2=1$. Hence there are $\pm1$ homomorphisms.$2\times2=4$** Let 

 $G=\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2$ be three generators of order $g_1,g_2,g_3$. The homomorphism is uniquely determined by$2$and all constraints are automatically satisfied. Hence there are 
$$
\varphi\left(g_1\right),\varphi\left(g_2\right),\varphi\left(g_3\right)\in\left\{\pm1\right\}
$$
 homomorphisms.$2^3=8$ classes of abelian groups of order 
 $8$, and the numbers of homomorphisms from them to $3$ are respectively $\mathbb Q^*$, $2$, and $4$. $8$ $\blacksquare$
