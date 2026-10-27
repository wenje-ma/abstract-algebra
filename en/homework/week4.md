# week4

> **Basic Knowledge: Anti-Homomorphism and Anti-Isomorphism**<br>If a map $f:G\to G'$ satisfies $f\left(ab\right)=f\left(b\right)f\left(a\right)$ for all $a,b\in G$, then $f$ is called an anti-homomorphism; if an anti-homomorphism is a bijection, it is called an anti-isomorphism.

> **Basic Knowledge: Symmetric Groups and Bijective Transformations**<br>The set $S_X$ of all bijections (permutations) of a nonempty set $X$ forms a group under composition of transformations, called the symmetric group on $X$; the left translation $L_a$ and right translation $R_a$ on $G$ are both bijections of $G$, since $L_{a^{-1}}$, $R_{a^{-1}}$ are their inverses respectively.

> **Basic Knowledge: Addition Formulas for Trigonometric Functions**<br>For all $x,y\in\mathbb R$, $\cos\left(x+y\right)=\cos x\cos y-\sin x\sin y$ and $\sin\left(x+y\right)=\sin x\cos y+\cos x\sin y$.

> **Basic Knowledge: Complex Exponentials and the Unit Circle**<br>For all $x\in\mathbb R$, $\cos x+\sqrt{-1}\sin x\in\mathbb C^{*}$, and $\cos x+\sqrt{-1}\sin x=1$ if and only if $x=2k\pi$ ($k\in\mathbb Z$).

> **Basic Knowledge: Properties of Homomorphisms into Automorphism Groups**<br>Let $\varphi:G\to\mathrm{Aut}\left(H\right)$ be a group homomorphism. Then for all $a,b\in G$, $\varphi\left(ab\right)=\varphi\left(a\right)\varphi\left(b\right)$, $\varphi\left(a^{-1}\right)=\varphi\left(a\right)^{-1}$, and $\varphi\left(e_G\right)=\mathrm{id}_H$; in particular $\varphi\left(a^{-1}\right)\varphi\left(a\right)=\mathrm{id}_H$.

> **Theorem 1.2.2 (Subgroup Criterion)**<br>Let $H$ be a nonempty subset of a group $G$. Then the following conditions are equivalent: (1) $H$ is a subgroup of $G$; (2) for all $a,b\in H$, $ab\in H$ and $a^{-1}\in H$; (3) for all $a,b\in H$, $ab^{-1}\in H$.

> **Definition 1.3.1 (Normal Subgroup)**<br>Let $H$ be a subgroup of a group $G$. If $ghg^{-1}\in H$ for all $g\in G$ and $h\in H$, then $H$ is called a normal subgroup of $G$, denoted $H\triangleleft G$.

> **Definition 1.4.1 (Group Homomorphism and Isomorphism)**<br>Let $G$ and $G'$ be two groups. If a map $f:G\to G'$ satisfies $f\left(ab\right)=f\left(a\right)f\left(b\right)$ for all $a,b\in G$, then $f$ is called a group homomorphism from $G$ to $G'$. If the homomorphism $f$ is a bijection, then $f$ is called a group isomorphism from $G$ to $G'$; in this case the groups $G$ and $G'$ are said to be isomorphic, denoted $G\cong G'$.

> **Definition 1.4.9 (Left and Right Translations)**<br>For any $a\in G$, define the transformations $L_a,R_a$ on $G$ by $L_a\left(g\right)=ag$, $R_a\left(g\right)=ga$ for all $g\in G$; $L_a,R_a$ are called the left translation and right translation determined by $a$ respectively.

> **Definition 1.4.11 (Kernel and Image of a Homomorphism)**<br>Let $f:G\to G'$ be a group homomorphism. The set $\ker f=\left\{a\in G\mid f\left(a\right)=e'\right\}$ is called the kernel of the homomorphism $f$, and the set $\mathrm{Im}\left(f\right)=f\left(G\right)=\left\{f\left(a\right)\mid a\in G\right\}$ is called the image of the homomorphism $f$.

> **Theorem 1.4.19 (Fundamental Theorem of Group Homomorphisms)**<br>Let $f:G\to G'$ be a surjective group homomorphism. Then $G/\ker f\cong G'$.

---

## 1.4-3

Let $G$ be a group. Define $R:G\to S_{G}$ by $R\left(a\right)=R_{a}$, where $R_{a}$ is the right translation. Prove that $R$ is an anti-isomorphism of $G$, i.e. it satisfies $R\left(ab\right)=R\left(b\right)R\left(a\right)$.

### Solution 1.4-3

For any $g\in G$, by **Definition 1.4.9 (Left and Right Translations)**, $R_a\left(g\right)=ga$.

**Step 1: prove that $R$ is an anti-homomorphism.** For any $g\in G$,

$$
R\left(ab\right)\left(g\right)=R_{ab}\left(g\right)=g\left(ab\right)=\left(ga\right)b=R_b\left(ga\right)=R_b\left(R_a\left(g\right)\right)=\left(R_b\circ R_a\right)\left(g\right)=R\left(b\right)R\left(a\right)\left(g\right).
$$

Since $g$ is arbitrary, $R\left(ab\right)=R\left(b\right)R\left(a\right)$, and by **Basic Knowledge: Anti-Homomorphism and Anti-Isomorphism**, $R$ is an anti-homomorphism from $G$ to $S_G$.

**Step 2: prove that $R$ is injective.** If $R\left(a\right)=R\left(b\right)$, then $R_a=R_b$. In particular $R_a\left(e\right)=R_b\left(e\right)$, i.e. $ea=eb$, so $a=b$. Hence $R$ is injective.

**Step 3: prove that the image of $R$ is a subgroup of $S_G$.** Write $R_G=\left\{R_a\mid a\in G\right\}$. By definition, $R:G\to R_G$ is surjective. Also, by **Basic Knowledge: Symmetric Groups and Bijective Transformations**, $R_a$ is a bijection of $G$ (with inverse $R_{a^{-1}}$), so $R_G\subseteq S_G$, and $R_G$ is a subgroup of $S_G$ (closed under composition and inverses in $R_G$, since $R_aR_b=R_{ba}$ and $R_a^{-1}=R_{a^{-1}}$).

In summary, $R:G\to R_G$ is a bijective anti-homomorphism, and by **Basic Knowledge: Anti-Homomorphism and Anti-Isomorphism**, $R$ is an anti-isomorphism; that is, $G$ is anti-isomorphic to the subgroup $R_G$ of $S_G$. $\blacksquare$

---

## 1.4-7

Prove that $f\left(x\right)=\cos x+\sqrt{-1}\sin x$ is a group homomorphism from $\left(\mathbb R,+\right)$ to $\left(\mathbb C^{*},\cdot\right)$, and find $\ker f$.

### Solution 1.4-7

**Step 1: prove that $f$ is a group homomorphism.** For any $x,y\in\mathbb R$, by **Basic Knowledge: Addition Formulas for Trigonometric Functions**,

$$
f\left(x+y\right)=\cos\left(x+y\right)+\sqrt{-1}\sin\left(x+y\right)=\left(\cos x\cos y-\sin x\sin y\right)+\sqrt{-1}\left(\sin x\cos y+\cos x\sin y\right)=\left(\cos x+\sqrt{-1}\sin x\right)\left(\cos y+\sqrt{-1}\sin y\right)=f\left(x\right)f\left(y\right).
$$

Moreover $f\left(x\right)\ne0$ for all $x\in\mathbb R$ (since $\cos^2x+\sin^2x=1$) (**Basic Knowledge: Complex Exponentials and the Unit Circle**), so $f:\mathbb R\to\mathbb C^{*}$ is well-defined. By **Definition 1.4.1 (Group Homomorphism and Isomorphism)**, $f$ is a group homomorphism from $\left(\mathbb R,+\right)$ to $\left(\mathbb C^{*},\cdot\right)$.

**Step 2: find $\ker f$.** By **Definition 1.4.11 (Kernel and Image of a Homomorphism)**, $\ker f=\left\{x\in\mathbb R\mid f\left(x\right)=1\right\}$. By **Basic Knowledge: Complex Exponentials and the Unit Circle**, $f\left(x\right)=\cos x+\sqrt{-1}\sin x=1$ if and only if $x=2k\pi$, $k\in\mathbb Z$. Hence

$$
\ker f=2\pi\mathbb Z=\left\{2k\pi\mid k\in\mathbb Z\right\}.
$$

By **Theorem 1.4.19 (Fundamental Theorem of Group Homomorphisms)**, $\mathbb R/2\pi\mathbb Z\cong\mathrm{Im}\left(f\right)$, where $\mathrm{Im}\left(f\right)=\left\{f\left(x\right)\mid x\in\mathbb R\right\}$ is the multiplicative group of complex numbers on the unit circle $\left\{z\in\mathbb C\mid\left|z\right|=1\right\}$ (**Basic Knowledge: Complex Exponentials and the Unit Circle**). $\blacksquare$

---

## 1.4-8

Let $G$ and $H$ be groups and $\varphi:G\to\mathrm{Aut}\left(H\right)$ a group homomorphism. On the set $\left\{\left(g,h\right)\mid g\in G,h\in H\right\}$ define the multiplication by

$$
\left(g_{1},h_{1}\right)\left(g_{2},h_{2}\right)=\left(g_{1}g_{2},\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right),
$$

Prove that this set is a group, called the semidirect product of $G$ and $H$, denoted $G\ltimes H$. Furthermore, $G_{1}=\left\{\left(g,e_{H}\right)\mid g\in G\right\}$ is a subgroup of $G\ltimes H$, and $H_{1}=\left\{\left(e_{G},h\right)\mid h\in H\right\}$ is a normal subgroup of $G\ltimes H$.

### Solution 1.4-8

Write $G\ltimes H=\left\{\left(g,h\right)\mid g\in G,h\in H\right\}$, with the multiplication defined as in the problem. We verify the group axioms one by one.

**Closure**: For any $\left(g_1,h_1\right),\left(g_2,h_2\right)\in G\ltimes H$, since $g_1g_2\in G$, and $\varphi\left(g_2^{-1}\right)\left(h_1\right)\in H$ (as $\varphi\left(g_2^{-1}\right)\in\mathrm{Aut}\left(H\right)$) and $h_2\in H$, we have $\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\in H$ (**Basic Knowledge: Properties of Homomorphisms into Automorphism Groups**). Hence $\left(g_1g_2,\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)\in G\ltimes H$, so closure holds.

**Associativity**: For any $\left(g_1,h_1\right),\left(g_2,h_2\right),\left(g_3,h_3\right)\in G\ltimes H$, on one hand

$$
\left(\left(g_1,h_1\right)\left(g_2,h_2\right)\right)\left(g_3,h_3\right)=\left(g_1g_2,\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)\left(g_3,h_3\right)=\left(\left(g_1g_2\right)g_3,\ \varphi\left(g_3^{-1}\right)\left(\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)h_3\right).
$$

Since $\varphi\left(g_3^{-1}\right)\in\mathrm{Aut}\left(H\right)$ preserves the multiplication of $H$, we have $\varphi\left(g_3^{-1}\right)\left(\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)=\varphi\left(g_3^{-1}\right)\varphi\left(g_2^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)$; and by **Basic Knowledge: Properties of Homomorphisms into Automorphism Groups**, $\varphi\left(g_3^{-1}\right)\varphi\left(g_2^{-1}\right)=\varphi\left(g_3^{-1}g_2^{-1}\right)=\varphi\left(\left(g_2g_3\right)^{-1}\right)$. Hence

$$
\left(\left(g_1,h_1\right)\left(g_2,h_2\right)\right)\left(g_3,h_3\right)=\left(\left(g_1g_2\right)g_3,\ \varphi\left(\left(g_2g_3\right)^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)\cdot h_3\right).
$$

On the other hand,

$$
\left(g_1,h_1\right)\left(\left(g_2,h_2\right)\left(g_3,h_3\right)\right)=\left(g_1,h_1\right)\left(g_2g_3,\varphi\left(g_3^{-1}\right)\left(h_2\right)h_3\right)=\left(g_1\left(g_2g_3\right),\ \varphi\left(\left(g_2g_3\right)^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)\cdot h_3\right).
$$

Since $G$ satisfies associativity, $\left(g_1g_2\right)g_3=g_1\left(g_2g_3\right)$; the second components of the two right-hand sides coincide, so associativity holds.

**Identity**: Consider $\left(e_G,e_H\right)$. For any $\left(g,h\right)\in G\ltimes H$, since $\varphi\left(e_G\right)=\mathrm{id}_H$ (**Basic Knowledge: Properties of Homomorphisms into Automorphism Groups**), we have $\varphi\left(e_G^{-1}\right)\left(h\right)=\mathrm{id}_H\left(h\right)=h$, and hence

$$
\left(g,h\right)\left(e_G,e_H\right)=\left(g,\varphi\left(e_G^{-1}\right)\left(h\right)e_H\right)=\left(g,h\right),
$$

and

$$
\left(e_G,e_H\right)\left(g,h\right)=\left(g,\varphi\left(g^{-1}\right)\left(e_H\right)h\right)=\left(g,\mathrm{id}_H\left(e_H\right)h\right)=\left(g,h\right).
$$

Hence $\left(e_G,e_H\right)$ is the identity.

**Inverse**: For $\left(g,h\right)\in G\ltimes H$, consider $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$. Since $\varphi\left(\left(g^{-1}\right)^{-1}\right)=\varphi\left(g\right)$, and $\varphi\left(g^{-1}\right)\varphi\left(g\right)=\mathrm{id}_H$, $\varphi\left(g\right)\varphi\left(g^{-1}\right)=\mathrm{id}_H$ (**Basic Knowledge: Properties of Homomorphisms into Automorphism Groups**), we have

$$
\left(g,h\right)\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_G,\ \varphi\left(g\right)\left(h\right)\cdot\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_G,\varphi\left(g\right)\left(hh^{-1}\right)\right)=\left(e_G,e_H\right),
$$

and

$$
\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)\left(g,h\right)=\left(e_G,\ \varphi\left(g^{-1}\right)\left(\varphi\left(g\right)\left(h^{-1}\right)\right)h\right)=\left(e_G,\left(\varphi\left(g^{-1}\right)\varphi\left(g\right)\right)\left(h^{-1}\right)\cdot h\right)=\left(e_G,h^{-1}h\right)=\left(e_G,e_H\right).
$$

Hence $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$ is the inverse of $\left(g,h\right)$.

Since closure, associativity, identity and inverse all hold, $G\ltimes H$ is a group.

**Verify $G_1<G\ltimes H$.** $\left(e_G,e_H\right)\in G_1$, so $G_1$ is nonempty. For $\left(g_1,e_H\right),\left(g_2,e_H\right)\in G_1$, by the inverse formula, $\left(g_2,e_H\right)^{-1}=\left(g_2^{-1},\varphi\left(g_2\right)\left(e_H\right)\right)=\left(g_2^{-1},e_H\right)$, and hence

$$
\left(g_1,e_H\right)\left(g_2,e_H\right)^{-1}=\left(g_1,e_H\right)\left(g_2^{-1},e_H\right)=\left(g_1g_2^{-1},\varphi\left(\left(g_2^{-1}\right)^{-1}\right)\left(e_H\right)e_H\right)=\left(g_1g_2^{-1},\varphi\left(g_2\right)\left(e_H\right)\right)=\left(g_1g_2^{-1},e_H\right)\in G_1.
$$

By **Theorem 1.2.2 (Subgroup Criterion)**, $G_1<G\ltimes H$.

**Verify $H_1\triangleleft G\ltimes H$.** First prove $H_1<G\ltimes H$: $\left(e_G,e_H\right)\in H_1$, nonempty; for $\left(e_G,h_1\right),\left(e_G,h_2\right)\in H_1$, by the inverse formula, $\left(e_G,h_2\right)^{-1}=\left(e_G,\varphi\left(e_G\right)\left(h_2^{-1}\right)\right)=\left(e_G,h_2^{-1}\right)$, and hence

$$
\left(e_G,h_1\right)\left(e_G,h_2\right)^{-1}=\left(e_G,h_1\right)\left(e_G,h_2^{-1}\right)=\left(e_G,\varphi\left(e_G^{-1}\right)\left(h_1\right)h_2^{-1}\right)=\left(e_G,h_1h_2^{-1}\right)\in H_1.
$$

By **Theorem 1.2.2 (Subgroup Criterion)**, $H_1<G\ltimes H$. Now prove normality: for any $\left(g,k\right)\in G\ltimes H$ and $\left(e_G,h\right)\in H_1$, by the inverse formula $\left(g,k\right)^{-1}=\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)$, and $\varphi\left(e_G^{-1}\right)=\mathrm{id}_H$, $\varphi\left(g\right)\varphi\left(g^{-1}\right)=\mathrm{id}_H$, we compute

$$
\left(g,k\right)\left(e_G,h\right)\left(g,k\right)^{-1}=\left(g,\varphi\left(e_G^{-1}\right)\left(k\right)h\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(g,kh\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_G,\varphi\left(g^{-1}\right)\left(kh\right)\cdot\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_G,\varphi\left(g^{-1}\right)\varphi\left(g\right)\left(h\right)\right)=\left(e_G,h\right)\in H_1.
$$

Hence $\left(g,k\right)H_1\left(g,k\right)^{-1}\subseteq H_1$ for all $\left(g,k\right)\in G\ltimes H$, and by **Definition 1.3.1 (Normal Subgroup)**, $H_1\triangleleft G\ltimes H$. $\blacksquare$
