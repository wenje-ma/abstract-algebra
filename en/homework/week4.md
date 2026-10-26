# Assignment 4

> **Definition 1.4.1** (Group Homomorphism and Isomorphism) Let $G$ and $G'$ be two groups. If a map $f:G\to G'$ satisfies $f\left(ab\right)=f\left(a\right)f\left(b\right)$, $\forall a,b\in G$, then $f$ is called a group homomorphism from $G$ to $G'$. If the homomorphism $f$ is a bijection, then $f$ is called a group isomorphism from $G$ to $G'$; in this case the groups $G$ and $G'$ are said to be isomorphic, denoted $G\cong G'$.

> **Definition 1.4.9** (Left Translation and Right Translation) For any $a\in G$, the transformations $G$ on $L_{a},R_{a}$ are defined by $L_{a}\left(g\right)=ag$, $R_{a}\left(g\right)=ga$, $\forall g\in G$. They are called the left translation and right translation determined by $a$, respectively.

> **Definition 1.4.11** (Kernel and Image of a Homomorphism) Let $f:G\to G'$ be a group homomorphism. The sets
> $$
> \ker f=\left\{a\in G\mid f\left(a\right)=e'\right\}
> $$
> and $\mathrm{Im}\left(f\right)=f\left(G\right)$ are called the kernel and image of the homomorphism $f$, respectively.

> **Theorem 1.4.19** (Fundamental Homomorphism Theorem for Groups) Let $f:G\to G'$ be a surjective group homomorphism. Then $G/\ker f\cong G'$.

> **Basic Knowledge** (Anti-Homomorphism) If a map $f:G\to G'$ satisfies $f\left(ab\right)=f\left(b\right)f\left(a\right)$, then $f$ is called an anti-homomorphism. If the anti-homomorphism is a bijection, it is called an anti-isomorphism.

### Problem 1

(Problem 1.4-3) Let $G$ be a group. Define $R:G\to S_{G}$ by $R\left(a\right)=R_{a}$, where $R_{a}$ is the right translation. Prove that $R$ is an anti-isomorphism of $G$, i.e. it satisfies $R\left(ab\right)=R\left(b\right)R\left(a\right)$.

### Solution to Problem 1

For any $g\in G$, by **Definition 1.4.9** (Left Translation and Right Translation), $R_{a}\left(g\right)=ga$.

First prove anti-homomorphicity. For any $g\in G$,

$$
R\left(ab\right)\left(g\right)=R_{ab}\left(g\right)=g\left(ab\right)=\left(ga\right)b=R_{b}\left(ga\right)=R_{b}\left(R_{a}\left(g\right)\right)=\left(R_{b}\circ R_{a}\right)\left(g\right)=R\left(b\right)R\left(a\right)\left(g\right).
$$

By the arbitrariness of $g$, $R\left(ab\right)=R\left(b\right)R\left(a\right)$, so $R$ is an anti-homomorphism.

Now prove that $R$ is a bijection.

**Injectivity** If $R\left(a\right)=R\left(b\right)$, then $R_{a}=R_{b}$. In particular, $R_{a}\left(e\right)=R_{b}\left(e\right)$, i.e. $ea=eb$, so $a=b$.

**Surjectivity** Write $R_{G}=\left\{R_{a}\mid a\in G\right\}$. By definition, $R:G\to R_{G}$ is surjective. Also each $R_{a}$ is a bijection on $G$ (its inverse is $R_{a^{-1}}$), so $R_{G}\subseteq S_{G}$.

Therefore $R:G\to R_{G}$ is an anti-isomorphism, i.e. $G$ is anti-isomorphic to the subgroup $S_{G}$ of $R_{G}$. $\blacksquare$

### Problem 2

(Problem 1.4-7) Prove that $f\left(x\right)=\cos x+\sqrt{-1}\sin x$ is a group homomorphism from $\left(\mathbb R,+\right)$ to $\left(\mathbb C^{*},\cdot\right)$, and find $\ker f$.

### Solution to Problem 2

For any $x,y\in\mathbb R$, by trigonometric identities,

$$
f\left(x+y\right)=\cos\left(x+y\right)+\sqrt{-1}\sin\left(x+y\right)=\left(\cos x\cos y-\sin x\sin y\right)+\sqrt{-1}\left(\sin x\cos y+\cos x\sin y\right)=\left(\cos x+\sqrt{-1}\sin x\right)\left(\cos y+\sqrt{-1}\sin y\right)=f\left(x\right)f\left(y\right).
$$

Hence $f$ is a group homomorphism from $\left(\mathbb R,+\right)$ to $\left(\mathbb C^{*},\cdot\right)$.

Find the kernel: $f\left(x\right)=1$ if and only if $\cos x=1$ and $\sin x=0$, i.e. $x=2k\pi$, $k\in\mathbb Z$. Thus

$$
\ker f=2\pi\mathbb Z=\left\{2k\pi\mid k\in\mathbb Z\right\}.
$$

By **Theorem 1.4.19** (Fundamental Homomorphism Theorem for Groups), $\mathbb R/2\pi\mathbb Z\cong\mathrm{Im}f$, where $\mathrm{Im}f$ is the multiplicative group of complex numbers on the unit circle. $\blacksquare$

### Problem 3

(Problem 1.4-8) Let $G$ and $H$ be groups and $\varphi:G\to\mathrm{Aut}\left(H\right)$ a group homomorphism. Define a multiplication on the set $\left\{\left(g,h\right)\mid g\in G,h\in H\right\}$ by

$$
\left(g_{1},h_{1}\right)\left(g_{2},h_{2}\right)=\left(g_{1}g_{2},\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right),
$$

and prove that this set is a group, called the semidirect product of $G$ and $H$, denoted $G\ltimes H$. Furthermore, $G_{1}=\left\{\left(g,e_{H}\right)\mid g\in G\right\}$ is a subgroup of $G\ltimes H$, and $H_{1}=\left\{\left(e_{G},h\right)\mid h\in H\right\}$ is a normal subgroup of $G\ltimes H$.

### Solution to Problem 3

Write

$$
G\ltimes H=\left\{\left(g,h\right)\mid g\in G,h\in H\right\},
$$

with multiplication as defined in the problem. We verify the group axioms one by one.

**Closure** By definition, the product again lies in $G\ltimes H$.

**Associativity** For any

$$
\left(g_{1},h_{1}\right),\left(g_{2},h_{2}\right),\left(g_{3},h_{3}\right)\in G\ltimes H,
$$

$$
\left(\left(g_{1},h_{1}\right)\left(g_{2},h_{2}\right)\right)\left(g_{3},h_{3}\right)=\left(g_{1}g_{2},\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right)\left(g_{3},h_{3}\right)=\left(\left(g_{1}g_{2}\right)g_{3},\varphi\left(g_{3}^{-1}\right)\left(\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right)h_{3}\right)=\left(g_{1}\left(g_{2}g_{3}\right),\varphi\left(g_{3}^{-1}\right)\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)\cdot\varphi\left(g_{3}^{-1}\right)\left(h_{2}\right)\cdot h_{3}\right)=\left(g_{1}\left(g_{2}g_{3}\right),\varphi\left(\left(g_{2}g_{3}\right)^{-1}\right)\left(h_{1}\right)\cdot\varphi\left(g_{3}^{-1}\right)\left(h_{2}\right)\cdot h_{3}\right).
$$

On the other hand,

$$
\left(g_{1},h_{1}\right)\left(\left(g_{2},h_{2}\right)\left(g_{3},h_{3}\right)\right)=\left(g_{1},h_{1}\right)\left(g_{2}g_{3},\varphi\left(g_{3}^{-1}\right)\left(h_{2}\right)h_{3}\right)=\left(g_{1}\left(g_{2}g_{3}\right),\varphi\left(\left(g_{2}g_{3}\right)^{-1}\right)\left(h_{1}\right)\cdot\varphi\left(g_{3}^{-1}\right)\left(h_{2}\right)h_{3}\right).
$$

The two are equal, so associativity holds.

**Identity** $\left(e_{G},e_{H}\right)$ is the identity. Indeed,

$$
\left(g,h\right)\left(e_{G},e_{H}\right)=\left(g,\varphi\left(e^{-1}\right)\left(h\right)e_{H}\right)=\left(g,h\right),\
\left(e_{G},e_{H}\right)\left(g,h\right)=\left(g,\varphi\left(g^{-1}\right)\left(e_{H}\right)h\right)=\left(g,h\right).
$$

**Inverse** The inverse of $\left(g,h\right)$ is $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$. Verification:

$$
\left(g,h\right)\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(gg^{-1},\varphi\left(\left(g^{-1}\right)^{-1}\right)\left(h\right)\cdot\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_{G},\varphi\left(g\right)\left(h\right)\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_{G},\varphi\left(g\right)\left(hh^{-1}\right)\right)=\left(e_{G},e_{H}\right).
$$

Symmetrically,

$$
\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)\left(g,h\right)=\left(e_{G},e_{H}\right).
$$

Hence $G\ltimes H$ is a group.

We now prove $G_{1}< G\ltimes H$. $\left(e_{G},e_{H}\right)\in G_{1}$. For $\left(g_{1},e_{H}\right),\left(g_{2},e_{H}\right)\in G_{1}$,

$$
\left(g_{1},e_{H}\right)\left(g_{2},e_{H}\right)^{-1}=\left(g_{1},e_{H}\right)\left(g_{2}^{-1},\varphi\left(g_{2}\right)\left(e_{H}\right)\right)=\left(g_{1}g_{2}^{-1},e_{H}\right)\in G_{1}.
$$

Hence $G_{1}< G\ltimes H$.

Finally prove $H_{1}\triangleleft G\ltimes H$. First show $H_{1}< G\ltimes H$: for $\left(e_{G},h_{1}\right),\left(e_{G},h_{2}\right)\in H_{1}$,

$$
\left(e_{G},h_{1}\right)\left(e_{G},h_{2}\right)^{-1}=\left(e_{G},h_{1}\right)\left(e_{G},h_{2}^{-1}\right)=\left(e_{G},h_{1}h_{2}^{-1}\right)\in H_{1}.
$$

Now prove normality. For any $\left(g,k\right)\in G\ltimes H$ and $\left(e_{G},h\right)\in H_{1}$,

$$
\left(g,k\right)\left(e_{G},h\right)\left(g,k\right)^{-1}=\left(g,k\right)\left(e_{G},h\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(g,\varphi\left(e^{-1}\right)\left(k\right)h\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(g,kh\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_{G},\varphi\left(g\right)\left(kh\right)\cdot\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_{G},\varphi\left(g\right)\left(h\right)\right)\in H_{1}.
$$

Hence $H_{1}\triangleleft G\ltimes H$. $\blacksquare$
