# week10

> **Basic Knowledge: Solvability of Prime-Order and Cyclic Groups**<br>A group of prime order is cyclic, hence solvable; every cyclic (abelian) group is solvable.

> **Basic Knowledge: Order of Elements in a Direct Product**<br>If $a\in G$ and $b\in H$, then the order of $\left(a,b\right)$ in the direct product $G\times H$ is $\mathrm{lcm}\left(\mathrm{ord}\,a,\mathrm{ord}\,b\right)$. Hence when $\left(m,n\right)=1$, $\mathbb Z_m\times\mathbb Z_n$ is a cyclic group of order $mn$, i.e. $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$.

> **Basic Knowledge: Index-Two Subgroups and the Alternating Subgroup of $S_n$**<br>A subgroup of index $2$ is normal; the index-two subgroup of $S_n$ is unique, namely the alternating group $A_n$. In particular, the index-two subgroup of $S_5$ is $A_5$.

> **Basic Knowledge: Groups of Order Four Are Abelian**<br>A group of order $4$ is either a cyclic group of order $4$ or the Klein four-group, both of which are abelian.

> **Basic Knowledge: Sylow Subgroups and Element Counting**<br>Conjugation preserves order, so a conjugate subgroup has the same order as the original; two distinct subgroups of prime order intersect in $\left\{e\right\}$; a Sylow $p$-subgroup of order $p^{k}$ contains $p^{k}-1$ non-identity elements of $p$-power order. For a finite simple group, the number of Sylow $p$-subgroups cannot be $1$ (otherwise that Sylow subgroup would be normal).

> **Basic Knowledge: Actions on Coset Spaces**<br>If $H<G$, then $G$ acts on the left coset space $G/H$ by left translation, giving a group homomorphism $G\to S_{\left[G:H\right]}$; its kernel $\bigcap_{g\in G}gHg^{-1}$ is a normal subgroup of $G$.

> **Lemma 1.7.7**<br>Let $A,B$ be subgroups of $G$ with $G=AB$ and $A\cap B=\left\{e\right\}$. Then $A$ and $B$ are both normal subgroups of $G$ if and only if $ab=ba$ for all $a\in A$ and $b\in B$.

> **Lemma 1.8.8 (Heredity of Solvability)**<br>Subgroups and quotient groups of a solvable group are solvable; conversely, if $N\trianglelefteq G$ and both $N$ and $G/N$ are solvable, then $G$ is solvable.

> **Theorem 1.10.8 (Sylow's Second Theorem)**<br>Let $P$ be a Sylow $p$-subgroup of $G$, and let $H$ be a subgroup of $G$ of order $p^{k}$, $k\le l$ (where $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$). Then there exists $g\in G$ with $H\subseteq gPg^{-1}$. In particular, the Sylow $p$-subgroups of $G$ are conjugate to one another.

> **Theorem 1.10.10 (Sylow's Third Theorem)**<br>Let $n_{p}$ be the number of Sylow $p$-subgroups of $G$. Then (1) a Sylow $p$-subgroup $P$ of $G$ satisfies $P\triangleleft G$ if and only if $n_{p}=1$; (2) $n_{p}\mid m$ and $n_{p}\equiv1\pmod p$, where $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$.

---

## 1.10-10

Let $\left|G\right|=pq$, where $p,q$ are distinct primes. Prove that $G$ is solvable.

### Solution 1.10-10

Without loss of generality suppose $p<q$. By **Theorem 1.10.10 (Sylow's Third Theorem)**, the number $n_{q}$ of Sylow $q$-subgroups satisfies $n_{q}\mid p$ and $n_{q}\equiv1\pmod q$. Since $p<q$, as a positive divisor of $p$ the number $n_{q}$ is either $1$ or $p$. If $n_{q}=p$, then $p\equiv1\pmod q$, i.e. $q\mid p-1$; but $p<q$ implies $p-1<q$, a contradiction. Hence $n_{q}=1$.

Thus the Sylow $q$-subgroup $Q$ of $G$ is unique, and by **Theorem 1.10.10 (Sylow's Third Theorem)** (1), $Q\triangleleft G$. Since $\left|Q\right|=q$ is prime, by **Basic Knowledge: Solvability of Prime-Order and Cyclic Groups**, $Q$ is cyclic and hence solvable. The quotient group $G/Q$ has order $p$, also a cyclic group of prime order, and by **Basic Knowledge: Solvability of Prime-Order and Cyclic Groups** is also solvable.

By **Lemma 1.8.8 (Heredity of Solvability)**, since both $Q$ and $G/Q$ are solvable, $G$ is solvable. $\blacksquare$

---

## 1.10-12

(Frattini) Let $N\triangleleft G$, and let $P$ be a Sylow subgroup of $N$. Then $G=N_{G}\left(P\right)N$.

### Solution 1.10-12

Take any $g\in G$. Since $N\triangleleft G$, the conjugate $gPg^{-1}$ is still a subgroup of $N$; and conjugation preserves order, so by **Basic Knowledge: Sylow Subgroups and Element Counting**, $\left|gPg^{-1}\right|=\left|P\right|$. Hence $gPg^{-1}$ is also a Sylow $p$-subgroup of $N$.

By **Theorem 1.10.8 (Sylow's Second Theorem)** (applied to the subgroup $N$), any two Sylow $p$-subgroups of $N$ are conjugate in $N$, so there exists $n\in N$ with

$$
gPg^{-1}=nPn^{-1}.
$$

Hence

$$
n^{-1}gPg^{-1}n=P,
$$

i.e. $n^{-1}g\in N_{G}\left(P\right)$ (it conjugates $P$ back to $P$). Write $h=n^{-1}g\in N_{G}\left(P\right)$; then $g=nh$.

Therefore $g\in N_{G}\left(P\right)N$. Since $g\in G$ was arbitrary, $G=N_{G}\left(P\right)N$. $\blacksquare$

---

## 1.10-15

Let $p,q$ be primes with $p<q$ and $p\nmid\left(q-1\right)$. Prove that a group of order $pq$ is cyclic.

### Solution 1.10-15

Let $\left|G\right|=pq$. By **Theorem 1.10.10 (Sylow's Third Theorem)**, the number $n_{q}$ of Sylow $q$-subgroups satisfies $n_{q}\mid p$ and $n_{q}\equiv1\pmod q$. Since $p<q$, as shown in Problem 1.10-10, we have $n_{q}=1$. Hence the Sylow $q$-subgroup $Q$ of $G$ is unique; by **Theorem 1.10.10 (Sylow's Third Theorem)** (1), $Q\triangleleft G$ and $\left|Q\right|=q$.

Now consider the number $n_{p}$ of Sylow $p$-subgroups. By **Theorem 1.10.10 (Sylow's Third Theorem)**, $n_{p}\mid q$ and $n_{p}\equiv1\pmod p$. Since $q$ is prime, $n_{p}=1$ or $q$. If $n_{p}=q$, then $q\equiv1\pmod p$, i.e. $p\mid\left(q-1\right)$, contradicting the hypothesis $p\nmid\left(q-1\right)$. Hence $n_{p}=1$.

Thus the Sylow $p$-subgroup $P$ of $G$ is also unique, and by **Theorem 1.10.10 (Sylow's Third Theorem)** (1), $P\triangleleft G$, $\left|P\right|=p$.

Since $p,q$ are coprime, $P\cap Q=\left\{e\right\}$. Also

$$
\left|PQ\right|=\left|P\right|\left|Q\right|/\left|P\cap Q\right|=pq=\left|G\right|,
$$

so $G=PQ$.

By **Lemma 1.7.7**, since $P,Q$ are both normal subgroups of $G$ and $P\cap Q=\left\{e\right\}$, we have $ab=ba$ for all $a\in P$, $b\in Q$. Hence the map

$$
P\times Q\to G,\quad\left(a,b\right)\mapsto ab
$$

preserves multiplication (because $ab=ba$) and is bijective (injective since $P\cap Q=\left\{e\right\}$, surjective since $G=PQ$); therefore it is a group isomorphism, i.e. $G\cong P\times Q$.

Moreover $P\cong\mathbb Z_p$ and $Q\cong\mathbb Z_q$, and $p,q$ are coprime, so by **Basic Knowledge: Order of Elements in a Direct Product**, $\mathbb Z_p\times\mathbb Z_q\cong\mathbb Z_{pq}$; hence

$$
G\cong\mathbb Z_p\times\mathbb Z_q\cong\mathbb Z_{pq},
$$

i.e. $G$ is a cyclic group of order $pq$. $\blacksquare$

---

## 1.10-20

Prove that a non-abelian finite simple group of order $60$ is isomorphic to $A_5$.

### Solution 1.10-20

Let $G$ be a non-abelian simple group of order $60$. First compute the number $n_{5}$ of Sylow $5$-subgroups. By **Theorem 1.10.10 (Sylow's Third Theorem)**, $n_{5}\mid12$ and $n_{5}\equiv1\pmod5$, so $n_{5}=1$ or $6$. By **Basic Knowledge: Sylow Subgroups and Element Counting**, since $G$ is simple, $n_{5}\ne1$; hence $n_{5}=6$.

Each Sylow $5$-subgroup is a cyclic group of order $5$ and, by **Basic Knowledge: Sylow Subgroups and Element Counting**, contains $4$ elements of order $5$; two distinct Sylow $5$-subgroups intersect in $\left\{e\right\}$ (the order of the intersection divides $5$, so it must be $1$). Hence $G$ contains $6\times4=24$ elements of order $5$.

Now consider the number $n_{2}$ of Sylow $2$-subgroups. By **Theorem 1.10.10 (Sylow's Third Theorem)**, $n_{2}\mid15$ and $n_{2}\equiv1\pmod2$, so $n_{2}\in\left\{1,3,5,15\right\}$. By **Basic Knowledge: Sylow Subgroups and Element Counting**, since $G$ is simple, $n_{2}\ne1$.

**Exclude $n_{2}=3$.** By **Basic Knowledge: Actions on Coset Spaces**, $G$ acts by conjugation on the $3$ Sylow $2$-subgroups, giving a homomorphism $\pi:G\to S_3$. Its kernel $\ker\pi$ is a normal subgroup of $G$. Since $G$ is simple, $\ker\pi=\left\{e\right\}$ or $G$. The action is transitive, hence nontrivial, so $\ker\pi\ne G$; if $\ker\pi=\left\{e\right\}$, then $G$ is isomorphic to a subgroup of $S_3$, but $\left|S_3\right|=6<60$, a contradiction. Hence $n_{2}\ne3$.

**Handle $n_{2}=5$.** By **Basic Knowledge: Actions on Coset Spaces**, $G$ acts by conjugation on the $5$ Sylow $2$-subgroups, giving a homomorphism $\pi:G\to S_5$. Similarly $\ker\pi$ is a normal subgroup and is not $G$; if $\ker\pi=\left\{e\right\}$, then $G$ is isomorphic to a subgroup of $S_5$ of order $60$. Since $\left|S_5\right|=120$, this subgroup of order $60$ has index $2$, so by **Basic Knowledge: Index-Two Subgroups and the Alternating Subgroup of $S_n$** it must be the unique index-two subgroup, namely $A_5$. Hence $G\cong A_5$, and the conclusion holds.

**Exclude $n_{2}=15$.** If any two distinct Sylow $2$-subgroups intersected in $\left\{e\right\}$, then each $4$-order Sylow $2$-subgroup contributes $3$ non-identity elements (by **Basic Knowledge: Groups of Order Four Are Abelian** and **Basic Knowledge: Sylow Subgroups and Element Counting**), giving $15\times3=45$ elements of order $2$ or $4$; together with the $24$ elements of order $5$, the total is $45+24=69>60$, a contradiction. Hence there exist two distinct Sylow $2$-subgroups $P,Q$ with $\left|P\cap Q\right|=2$.

Write $P\cap Q=\left\langle x\right\rangle$, where $x$ has order $2$. Since $P,Q$ are groups of order $4$, by **Basic Knowledge: Groups of Order Four Are Abelian** they are abelian, and $x\in P\cap Q$, so $P,Q\subseteq N_{G}\left(\left\langle x\right\rangle\right)$. Since $P\ne Q$, we have $\left|N_{G}\left(\left\langle x\right\rangle\right)\right|>4$. Moreover $\left|N_{G}\left(\left\langle x\right\rangle\right)\right|\mid60$ and is divisible by $4$ (it contains the order-$4$ subgroup $P$), so it can only be $12,20$ or $60$. If it were $60$, then $\left\langle x\right\rangle\triangleleft G$, contradicting the simplicity of $G$. Hence $\left|N_{G}\left(\left\langle x\right\rangle\right)\right|=12$ or $20$, corresponding to index $5$ or $3$.

If the index is $3$, then by **Basic Knowledge: Actions on Coset Spaces**, $G$ acting on $3$ cosets by left translation gives a homomorphism $G\to S_3$, leading to the same contradiction as in the $n_{2}=3$ case. Hence the index must be $5$. Thus $G$ has a subgroup $N_{G}\left(\left\langle x\right\rangle\right)$ of index $5$; by **Basic Knowledge: Actions on Coset Spaces**, $G$ acting by left translation on the $5$ cosets gives a homomorphism $G\to S_5$ whose kernel is a normal subgroup different from $G$; since $G$ is simple, the kernel is $\left\{e\right\}$, yielding a monomorphism $G\hookrightarrow S_5$. As before, the order-$60$ subgroup of $S_5$ must be $A_5$, so $G\cong A_5$. $\blacksquare$
