# Assignment 7

> **Definition 1.7.9** (Subnormal Series and Composition Series) A sequence of subgroups in a group $G$
> $$
> G=G_1\trianglerighteq G_2\trianglerighteq\cdots\trianglerighteq G_t\trianglerighteq G_{t+1}=\left\{e\right\}
> $$
> is called a subnormal series if $G_{i+1}\trianglelefteq G_i$, and the $G_i/G_{i+1}$ are called its factors. If all the factors $G_i/G_{i+1}$ are simple groups, the subnormal series is called a composition series of $G$, and the $G_i/G_{i+1}$ are called the composition factors of $G$.

> **Definition 1.7.12** (Isomorphic Series) Two subnormal series of a group $G$ are called isomorphic if there is a bijection between the factor sets of the two series such that corresponding factors are isomorphic.

> **Theorem 1.7.13** (Jordan–Hölder Theorem) If a group $G$ has a composition series, then any two composition series of $G$ are isomorphic.

> **Basic Knowledge** (Second Isomorphism Theorem) Let $A,B$ be subgroups of $G$ with $B\trianglelefteq G$ and $A\le G$. Then $A\cap B\trianglelefteq A$ and $A/\left(A\cap B\right)\cong AB/B$. In particular, if both $A,B$ are normal subgroups of $G$, then $AB/\!A\cong B/\left(A\cap B\right)$.

### Problem 1

(Problem 1.7-11) Let
$$
G=G_1\triangleright G_2\triangleright\cdots\triangleright G_t=\left\{e\right\},
$$
and
$$
G=H_1\triangleright H_2\triangleright\cdots\triangleright H_s=\left\{e\right\},
$$
be two composition series of $G$, with $G_2\ne H_2$. Set $K_3=G_2\cap H_2$. Take any composition series of $K_3$
$$
K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}.
$$
Prove that:
(1)

$$
G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\},\
G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

are also composition series of $G$;
(2) the four composition series of $G$ above are mutually equivalent.

### Solution to Problem 1

First prove $G_2H_2=G$. Since both $G_2,H_2$ are normal subgroups of $G$, $G_2H_2\trianglelefteq G$ and $G_2H_2\supseteq G_2$. Also $G/G_2$ is a composition factor and hence simple, so $G_2H_2/G_2$, as a normal subgroup of $G/G_2$, must be either trivial or $G/G_2$, i.e. $G_2H_2=G_2$ or $G$.

If $G_2H_2=G_2$, then $H_2\subseteq G_2$, and thus $G_2H_2=G_2\ne H_2$. On the other hand, $G_2H_2/H_2\trianglelefteq G/H_2$, and $G/H_2$ is also simple, so $G_2H_2=H_2$ or $G$. From $G_2H_2\ne H_2$ we get $G_2H_2=G$. But then $G_2=G$, contradicting $G_2\triangleleft G$. Hence $G_2H_2\ne G_2$.

Symmetrically, $G_2H_2\ne H_2$. Therefore the only possibility is
$$
G_2H_2=G.
$$

(1) From $G_2H_2=G$ and **Basic Knowledge** (Second Isomorphism Theorem),
$$
G_2/K_3=G_2/\left(G_2\cap H_2\right)\cong G_2H_2/H_2=G/H_2,
$$
and $G/H_2$ is a composition factor and hence simple, so $G_2/K_3$ is simple.

Symmetrically,
$$
H_2/K_3=H_2/\left(G_2\cap H_2\right)\cong G_2H_2/G_2=G/G_2,
$$
is also simple.

Also $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ is a composition series of $K_3$, so the factors $K_i/K_{i+1}$ ($i=3,\cdots,r-1$) are all simple. Therefore the series
$$
G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$
has all its factors $G/G_2$, $G_2/K_3$, $K_3/K_4,\cdots,K_{r-1}/K_r$ simple. By **Definition 1.7.9** (Subnormal Series and Composition Series), it is a composition series of $G$.

Symmetrically, the series
$$
G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$
has factors $G/H_2$, $H_2/K_3$, $K_3/K_4,\cdots,K_{r-1}/K_r$ all simple, so it is also a composition series of $G$.

(2) Denote the four composition series by
$$
S_1:\;G\triangleright G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\},;S_2:\;G\triangleright H_2\triangleright H_3\triangleright\cdots\triangleright H_s=\left\{e\right\},;S_3:\;G\triangleright G_2\triangleright K_3\triangleright\cdots\triangleright K_r=\left\{e\right\},;S_4:\;G\triangleright H_2\triangleright K_3\triangleright\cdots\triangleright K_r=\left\{e\right\}.
$$

We first show that $S_3$ and $S_4$ are isomorphic. The factors of $S_3$ are
$$
G/G_2, G_2/K_3\cong G/H_2, K_3/K_4,\cdots, K_{r-1}/K_r;
$$
$S_4$ are
$$
G/H_2, H_2/K_3\cong G/G_2, K_3/K_4,\cdots, K_{r-1}/K_r.
$$
As multisets, the two factor lists differ only in the order of the first two factors, with $G/G_2$ and $G/H_2$ interchanged; the remaining factors are identical. By **Definition 1.7.12** (Isomorphic Series), $S_3$ and $S_4$ are isomorphic.

Now show that $S_1$ and $S_3$ are isomorphic. Both $S_1$ and $S_3$ have first factor $G/G_2$. After removing the first term, their tails
$$
G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\}
$$
and
$$
G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$
are both composition series of $G_2$. Since $\left|G_2\right|< \left|G\right|$, induction on the order of the group and **Theorem 1.7.13** (Jordan–Hölder Theorem) give that these two composition series of $G_2$ are isomorphic. Adjoining the common first factor $G/G_2$, $S_1$ and $S_3$ are isomorphic.

Symmetrically, both $S_2$ and $S_4$ have first factor $G/H_2$, and their tails $H_2\triangleright\cdots\triangleright\left\{e\right\}$ and $H_2\triangleright K_3\triangleright\cdots\triangleright\left\{e\right\}$ are both composition series of $H_2$; by the induction hypothesis they are isomorphic, so $S_2$ and $S_4$ are isomorphic.

In summary, $S_1\cong S_3\cong S_4\cong S_2$, i.e. the four composition series are mutually equivalent. $\blacksquare$
