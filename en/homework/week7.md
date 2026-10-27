# week7

> **Basic Knowledge: Surjective Homomorphisms Preserve Normal Subgroups**<br>Let $f:G\to G'$ be a surjective homomorphism. If $H\triangleleft G$, then $f\left(H\right)\triangleleft G'$.

> **Theorem 1.4.23 (3) (Second Isomorphism Theorem)**<br>Let $G$ be a group, $N\triangleleft G$, and $H<G$. Then $HN/N\cong H/\left(H\cap N\right)$.

> **Definition 1.7.9 (Subnormal Series and Composition Series)**<br>A sequence of subgroups $G=G_1\trianglerighteq G_2\trianglerighteq\cdots\trianglerighteq G_t\trianglerighteq G_{t+1}=\left\{e\right\}$ of a group $G$ is called a subnormal series if $G_{i+1}\trianglelefteq G_i$ for $i=1,\cdots,t$; the quotient $G_i/G_{i+1}$ is called a factor of this series. If all factors $G_i/G_{i+1}$ are simple groups, then this subnormal series is called a composition series of $G$, and the $G_i/G_{i+1}$ are called composition factors of $G$.

> **Definition 1.7.12 (Isomorphic Series)**<br>Two subnormal series $G=G_1\supset G_2\supset\cdots\supset G_t=\left\{e\right\}$ and $G=H_1\supset H_2\supset\cdots\supset H_s=\left\{e\right\}$ of a group $G$ are called isomorphic if there is a bijection between the two sets of factors such that the corresponding factors are isomorphic.

> **Theorem 1.7.13 (Jordan-Holder Theorem)**<br>If a group $G$ has a composition series, then any two composition series of $G$ are isomorphic. In particular, any two principal series of $G$ are isomorphic.

---

## 1.7-11

Let

$$
G=G_1\triangleright G_2\triangleright\cdots\triangleright G_t=\left\{e\right\}
$$

and

$$
G=H_1\triangleright H_2\triangleright\cdots\triangleright H_s=\left\{e\right\}
$$

be two composition series of $G$, with $G_2\ne H_2$. Let $K_3=G_2\cap H_2$. Take any composition series $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ of $K_3$. Prove that:

(1) both $G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ and $G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ are also composition series of $G$;

(2) the above four composition series of $G$ are equivalent to one another.

### Solution 1.7-11

**Step 1: prove that $G_2H_2=G$.** Since $H_2\triangleleft G$, by **Basic Knowledge: Surjective Homomorphisms Preserve Normal Subgroups**, the image $\pi\left(H_2\right)$ under the natural homomorphism $\pi:G\to G/G_2$ is a normal subgroup of $G/G_2$. Moreover $\pi\left(H_2\right)=\left\{hG_2\mid h\in H_2\right\}=\left(G_2H_2\right)/G_2$ (since $G_2\subseteq G_2H_2$), so $\left(G_2H_2\right)/G_2\triangleleft G/G_2$. Since $G/G_2$ is a composition factor and hence simple, $\left(G_2H_2\right)/G_2$ must be trivial or all of $G/G_2$, i.e. $G_2H_2=G_2$ or $G$.

Similarly, since $G_2\triangleleft G$, the image $\pi'\left(G_2\right)=\left(G_2H_2\right)/H_2$ under the natural homomorphism $\pi':G\to G/H_2$ is a normal subgroup of $G/H_2$; since $G/H_2$ is simple, $G_2H_2=H_2$ or $G$.

**Claim: $G_2H_2\ne G_2$.** If $G_2H_2=G_2$, then $H_2\subseteq G_2$. From the previous paragraph $G_2H_2\in\left\{H_2,G\right\}$, i.e. $G_2=H_2$ or $G_2=G$; the former contradicts $G_2\ne H_2$, and the latter contradicts the fact that $G_2$ is a proper subgroup of $G$ (since $G/G_2$ is a nontrivial simple group). Hence $G_2H_2\ne G_2$.

**Claim: $G_2H_2\ne H_2$.** If $G_2H_2=H_2$, then $G_2\subseteq H_2$. From $G_2H_2\in\left\{G_2,G\right\}$, we get $H_2=G_2$ or $H_2=G$; the former contradicts $G_2\ne H_2$, and the latter contradicts the fact that $H_2$ is a proper subgroup. Hence $G_2H_2\ne H_2$.

Therefore the only possibility is $G_2H_2=G$.

**Step for (1): prove that both refined series are composition series.** By **Theorem 1.4.23 (3) (Second Isomorphism Theorem)**, taking $H=G_2$ and $N=H_2$, we get

$$
G_2/K_3=G_2/\left(G_2\cap H_2\right)\cong G_2H_2/H_2=G/H_2,
$$

and $G/H_2$ is a composition factor, hence simple; so $G_2/K_3$ is simple.

Similarly, by **Theorem 1.4.23 (3) (Second Isomorphism Theorem)**, taking $H=H_2$ and $N=G_2$, we get

$$
H_2/K_3=H_2/\left(G_2\cap H_2\right)\cong G_2H_2/G_2=G/G_2,
$$

which is also simple.

Moreover $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ is a composition series of $K_3$, so each $K_i/K_{i+1}$ ($i=3,\cdots,r-1$) is simple. Hence all factors $G/G_2$, $G_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ of the series

$$
G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

are simple; and $G_2\triangleright K_3$ is a valid subnormal step ($K_3=G_2\cap H_2$, $H_2\triangleleft G$, so $K_3\triangleleft G_2$). By **Definition 1.7.9 (Subnormal Series and Composition Series)**, it is a composition series of $G$.

Similarly, all factors $G/H_2$, $H_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ of the series

$$
G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

are simple, so by **Definition 1.7.9 (Subnormal Series and Composition Series)** it is also a composition series of $G$.

**Step for (2): prove that the four composition series are equivalent.** Write the four composition series as

$$
\begin{aligned}
S_1&:G\triangleright G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\},\\
S_2&:G\triangleright H_2\triangleright H_3\triangleright\cdots\triangleright H_s=\left\{e\right\},\\
S_3&:G\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\},\\
S_4&:G\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}.
\end{aligned}
$$

**First prove that $S_3$ and $S_4$ are isomorphic.** The factors of $S_3$ are $G/G_2$, $G_2/K_3\cong G/H_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$; the factors of $S_4$ are $G/H_2$, $H_2/K_3\cong G/G_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$. As multisets the two families differ only in the first two entries: $G/G_2$ and $G/H_2$ are interchanged, and all remaining factors are identical. Hence by **Definition 1.7.12 (Isomorphic Series)**, $S_3$ and $S_4$ are isomorphic.

**Next prove that $S_1$ and $S_3$ are isomorphic.** The first factors of $S_1$ and $S_3$ are both $G/G_2$. After removing the first term, the two tails

$$
G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\}
\quad\text{and}\quad
G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

are both composition series of $G_2$. By **Theorem 1.7.13 (Jordan-Holder Theorem)**, these two composition series of the group $G_2$ are isomorphic. After adding back their common first factor $G/G_2$, by **Definition 1.7.12 (Isomorphic Series)**, $S_1$ and $S_3$ are isomorphic.

**Similarly prove that $S_2$ and $S_4$ are isomorphic.** The first factors of $S_2$ and $S_4$ are both $G/H_2$; the tails $H_2\triangleright H_3\triangleright\cdots\triangleright\left\{e\right\}$ and $H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright\left\{e\right\}$ are both composition series of $H_2$, hence isomorphic by **Theorem 1.7.13 (Jordan-Holder Theorem)**; after adding back the common first factor $G/H_2$, $S_2$ and $S_4$ are isomorphic.

In summary, $S_1\cong S_3\cong S_4\cong S_2$, so the four composition series are equivalent. $\blacksquare$
