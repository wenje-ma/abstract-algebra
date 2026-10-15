# Assignment 10

> **Theorem 1.10.1** (Cauchy's Theorem) Let a prime $p$ be a divisor of $\left|G\right|$. Then $G$ contains an element of order $p$.

> **Theorem 1.10.5** (First Sylow Theorem) Let $\left|G\right|=p^{l}m$, where $p$ is prime, $l\ge1$, and $\left(p,m\right)=1$. Then for any $k\le l$, $G$ contains a subgroup of order $p^{k}$. In particular, $G$ contains a Sylow $p$-subgroup (a subgroup of order $p^{l}$).

> **Theorem 1.10.8** (Second Sylow Theorem) Let $P$ be a Sylow $G$-subgroup of $p$ and $H$ a subgroup of $G$ of order $p^{k}$ with $k\le l$. Then there exists $g\in G$ such that $H\subseteq gPg^{-1}$. In particular, all Sylow $G$-subgroups of $p$ are conjugate.

> **Theorem 1.10.10** (Third Sylow Theorem) Let the number of Sylow $G$-subgroups of $p$ be $n_p$. Then $n_p\mid m$ and $n_p\equiv1\pmod p$. Moreover, a Sylow $p$-subgroup is normal if and only if $n_p=1$.

> **Lemma 1.8.8** (Heredity of Solvable Groups) Subgroups and quotient groups of a solvable group are solvable; conversely, if $N\trianglelefteq G$ and both $N$ and $G/N$ are solvable, then $G$ is solvable.

### Problem 1

(Problem 1.10-10) Let $\left|G\right|=pq$, where $p,q$ are distinct primes. Prove that $G$ is solvable.

### Solution to Problem 1

Without loss of generality, assume $p<q$. By **Theorem 1.10.10** (Third Sylow Theorem), the number $q$ of Sylow $n_q$-subgroups satisfies $n_q\mid p$ and $n_q\equiv1\pmod q$. Since $p<q$, $n_q$ as a positive divisor of $p$ can only be $1$ or $p$. If $n_q=p$, then $p\equiv1\pmod q$, i.e. $q\mid p-1$, but $p<q$ implies $p-1<q$, a contradiction. Hence $n_q=1$.

Thus the Sylow $G$-subgroup $q$ of $Q$ is unique, and by **Theorem 1.10.10**, $Q\trianglelefteq G$. Also $\left|Q\right|=q$ is prime, so $Q$ is cyclic and hence solvable. The quotient $G/Q$ has order $p$, also a cyclic group of prime order, and is solvable.

By **Lemma 1.8.8** (Heredity of Solvable Groups), both $Q$ and $G/Q$ are solvable, so $G$ is solvable. $\blacksquare$

### Problem 2

(Problem 1.10-12) (Frattini argument) Let $N\trianglelefteq G$ and let $P$ be a Sylow subgroup of $N$. Then $G=N_G\left(P\right)N$.

### Solution to Problem 2

Take any $g\in G$. Since $N\trianglelefteq G$, the conjugate $gPg^{-1}$ is again a subgroup of $N$, and
$$
\left|gPg^{-1}\right|=\left|P\right|,
$$
so $gPg^{-1}$ is also a Sylow $N$-subgroup of $p$.

By **Theorem 1.10.8** (Second Sylow Theorem), any two Sylow $N$-subgroups of $p$ are conjugate in $N$. Hence there exists $n\in N$ such that
$$
gPg^{-1}=nPn^{-1}.
$$
Then
$$
n^{-1}gPg^{-1}n=P,
$$
i.e. $n^{-1}g\in N_G\left(P\right)$. Write $h=n^{-1}g\in N_G\left(P\right)$; then $g=nh$.

Therefore $g\in N_G\left(P\right)N$. By the arbitrariness of $g$,
$$
G=N_G\left(P\right)N.
$$
$\blacksquare$

### Problem 3

(Problem 1.10-15) Let $p,q$ be primes with $p<q$ and $p\nmid\left(q-1\right)$. Prove that any group of order $pq$ is cyclic.

### Solution to Problem 3

Let $\left|G\right|=pq$. By **Theorem 1.10.10** (Third Sylow Theorem), the number $q$ of Sylow $n_q$-subgroups satisfies $n_q\mid p$ and $n_q\equiv1\pmod q$. Since $p<q$, as in Problem 1, $n_q=1$. Hence the Sylow $G$-subgroup $q$ of $Q$ is unique, $Q\trianglelefteq G$, and $\left|Q\right|=q$.

Now consider the number $p$ of Sylow $n_p$-subgroups. By **Theorem 1.10.10**, $n_p\mid q$ and $n_p\equiv1\pmod p$. Since $q$ is prime, $n_p=1$ or $q$. If $n_p=q$, then $q\equiv1\pmod p$, i.e. $p\mid\left(q-1\right)$, contradicting the assumption $p\nmid\left(q-1\right)$. Hence $n_p=1$.

Thus the Sylow $G$-subgroup $p$ of $P$ is also unique, $P\trianglelefteq G$, and $\left|P\right|=p$.

Since $p,q$ are coprime, $P\cap Q=\left\{e\right\}$. Also,

$$
\left|PQ\right|=\left|P\right|\left|Q\right|/\left|P\cap Q\right|=pq=\left|G\right|,
$$

so $G=PQ$.

By **Lemma 1.7.7** (Commutativity of Normal Subgroups), both $P,Q$ are normal in $G$ and $P\cap Q=\left\{e\right\}$, so for any $a\in P$ and $b\in Q$, $ab=ba$. Hence the map
$$
P\times Q\to G,\left(a,b\right)\mapsto ab
$$
is a group isomorphism, i.e. $G\cong P\times Q$.

Also $P\cong\mathbb Z_p$ and $Q\cong\mathbb Z_q$, and since $p,q$ are coprime,
$$
G\cong\mathbb Z_p\times\mathbb Z_q\cong\mathbb Z_{pq},
$$
i.e. $G$ is a cyclic group of order $pq$. $\blacksquare$

### Problem 4

(Problem 1.10-20) Prove that any nonabelian finite simple group of order $60$ is isomorphic to $A_5$.

### Solution to Problem 4

Let $G$ be a nonabelian simple group of order $60$. First find the number $5$ of Sylow $n_5$-subgroups. By **Theorem 1.10.10** (Third Sylow Theorem), $n_5\mid12$ and $n_5\equiv1\pmod5$, so $n_5=1$ or $6$. Since $G$ is simple, $n_5\ne1$, so $n_5=6$.

Each Sylow $5$-subgroup is cyclic of order $5$ and contains $4$ elements of order $5$; two distinct Sylow $5$-subgroups intersect in $\left\{e\right\}$ (the order of the intersection divides $5$, so it can only be $1$). Hence $G$ contains $6\times4=24$ elements of order $5$ in total.

Now consider the number $2$ of Sylow $n_2$-subgroups. $n_2\mid15$ and $n_2\equiv1\pmod2$, so $n_2\in\left\{1,3,5,15\right\}$. Since $G$ is simple, $n_2\ne1$.

If $n_2=3$, $G$ acts by conjugation on these $3$ Sylow $2$-subgroups, giving a homomorphism $\pi:G\to S_3$. Its kernel is a normal subgroup of $G$. Since $G$ is simple, $\ker\pi=\left\{e\right\}$ or $G$. The action is nontrivial, so $\ker\pi\ne G$; but if $\ker\pi=\left\{e\right\}$, then $G$ is isomorphic to a subgroup of $S_3$, while $\left|S_3\right|=6<60$, a contradiction. Hence $n_2\ne3$.

If $n_2=5$, $G$ acts by conjugation on the $5$ Sylow $2$-subgroups, giving a homomorphism $\pi:G\to S_5$. Similarly $\ker\pi=\left\{e\right\}$, so $G$ is isomorphic to a subgroup of order $S_5$ in $60$. Since $S_5$, a subgroup of index $120$ is necessarily normal, and $2$ is precisely the unique subgroup of index $A_5$ in $S_5$. Hence $2$.$G\cong A_5$. If any two distinct Sylow 

 $n_2=15$-subgroups intersect in $2$, then each Sylow $\left\{e\right\}$-subgroup of order $4$ contributes $2$ nonidentity elements, giving $3$ elements of order $15\times3=45$ or $2$; together with the $4$ elements of order $24$, the total exceeds $5$, a contradiction.$60$-subgroups 

 $2$ with $P,Q$. Write $\left|P\cap Q\right|=2$ where $P\cap Q=\left\{e,x\right\}$ has order $x$. Since both $2$ have order $P,Q$ (and are abelian), each is normal in itself, so $4$. Also $P,Q\subseteq N_G\left(\left\langle x\right\rangle\right)$, so $P\ne Q$. Meanwhile $\left|N_G\left(\left\langle x\right\rangle\right)\right|>4$ and is divisible by $\left|N_G\left(\left\langle x\right\rangle\right)\right|\mid60$, so it can only be $4$ or $12,20$. If it is $60$, then $60$, contradicting the simplicity of $\left\langle x\right\rangle\trianglelefteq G$. Hence $G$ or $\left|N_G\left(\left\langle x\right\rangle\right)\right|=12$, corresponding to index $20$ or $5$.$3$ would give a homomorphism 

 $3$, contradicting the earlier argument, so the index must be $G\to S_3$. Thus $5$ has a subgroup of index $G$, and $5$ acts by left translation on the $G$ cosets of this subgroup, giving a monomorphism $5$. As above, the only subgroup of order $G\hookrightarrow S_5$ in $S_5$ is $60$, so $A_5$. $G\cong A_5$ $\blacksquare$
