# week3

> **Definition 1.2.1 (Subgroup)**
> 
> Let $H$ be a nonempty subset of a group $G$. If $H$ forms a group under the operation of $G$, then $H$ is called a subgroup of $G$, denoted $H<{}G$.

> **Theorem 1.2.2 (Subgroup Criterion)**
> 
> Let $H$ be a nonempty subset of a group $G$. Then the following conditions are equivalent: (1) $H$ is a subgroup of $G$; (2) for all $a,b\in{H}$, $ab\in{H}$ and $a^{-1}\in{H}$; (3) for all $a,b\in{H}$, $ab^{-1}\in{H}$.

> **Lemma 1.2.12 (Coset Coincidence Criterion)**
> 
> Let $H$ be a subgroup of a group $G$ and $a,b\in{G}$. Then $aH$ and $bH$ are either disjoint or identical, and $aH=bH$ if and only if $a^{-1}b\in{H}$.

> **Theorem 1.2.22 (Lagrange's Theorem)**
> 
> Let $G$ be a finite group and $H<{}G$. Then $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, where $\left[G:H\right]$ is the index of $H$ in $G$. Hence the order of the subgroup $H$ is a divisor of the order of the group $G$; in particular, the order of any element is also a divisor of $\left|G\right|$.

> **Corollary 1.2.23 (Multiplicativity of the Index)**
> 
> Let $G$ be a finite group, $K<{}G$, $H<{}K$. Then $\left[G:H\right]=\left[G:K\right]\cdot\left[K:H\right]$.

> **Definition 1.3.1 (Normal Subgroup)**
> 
> Let $H$ be a subgroup of a group $G$. If $ghg^{-1}\in{H}$ for all $g\in{G}$ and $h\in{H}$, then $H$ is called a normal subgroup of $G$, denoted $H\triangleleft{G}$.

> **Theorem 1.3.5 (Equivalent Conditions for Normal Subgroups)**
> 
> Let $G$ be a group and $H<{}G$. Then the following conditions are equivalent: (1) $H\triangleleft{G}$; (2) $gH=Hg$ for all $g\in{G}$; (3) $aH\cdot{b}H=abH$ for all $a,b\in{G}$, where $aH\cdot{b}H=\left\{ah_1bh_2\mid{h}_1,h_2\in{H}\right\}$.

> **Definition 1.4.1 (Group Homomorphism and Isomorphism)**
> 
> Let $G$ and $G'$ be two groups. If a map $f:G\to{G}'$ satisfies $f\left(ab\right)=f\left(a\right)f\left(b\right)$ for all $a,b\in{G}$, then $f$ is called a group homomorphism from $G$ to $G'$. If the homomorphism $f$ is a bijection, then $f$ is called a group isomorphism from $G$ to $G'$; in this case the groups $G$ and $G'$ are said to be isomorphic, denoted $G\cong{G}'$.

> **Definition 1.4.9 (Left and Right Translations)**
> 
> For any $a\in{G}$, define the transformations $L_a,R_a$ on $G$ by $L_a\left(g\right)=ag$, $R_a\left(g\right)=ga$ for all $g\in{G}$; $L_a,R_a$ are called the left translation and right translation determined by $a$ respectively.

> **Definition 1.4.11 (Kernel and Image of a Homomorphism)**
> 
> Let $f:G\to{G}'$ be a group homomorphism. The set $\ker{f}=\left\{a\in{G}\mid{f}\left(a\right)=e'\right\}$ is called the kernel of the homomorphism $f$, and the set $\mathrm{Im}\left(f\right)=f\left(G\right)=\left\{f\left(a\right)\mid{a}\in{G}\right\}$ is called the image of the homomorphism $f$.

> **Theorem 1.4.19 (Fundamental Theorem of Group Homomorphisms)**
> 
> Let $f:G\to{G}'$ be a surjective group homomorphism. Then $G/\ker{f}\cong{G}'$.

## 1.2-20

Let $H_{1},H_{2}$ be two subgroups of a finite group $G$. Prove that

$$
\left[G:H_{1}\cap{H}_{2}\right]\le\left[G:H_{1}\right]\left[G:H_{2}\right].
$$

Moreover, if $\left[G:H_{1}\right]$ and $\left[G:H_{2}\right]$ are coprime, then

$$
\left[G:H_{1}\cap{H}_{2}\right]=\left[G:H_{1}\right]\left[G:H_{2}\right]
$$

and $G=H_{1}H_{2}$.

### Solution to 1.2-20

First prove the inequality. Consider the map

$$
\varphi:G/\left(H_{1}\cap{H}_{2}\right)\to{G}/H_{1}\times{G}/H_{2},\quad{g}\left(H_{1}\cap{H}_{2}\right)\mapsto\left(gH_{1},gH_{2}\right).
$$

Well-defined: if $g\left(H_{1}\cap{H}_{2}\right)=g'\left(H_{1}\cap{H}_{2}\right)$, then by **Lemma 1.2.12 (Coset Coincidence Criterion)**, $g^{-1}g'\in{H}_{1}\cap{H}_{2}$, so $g^{-1}g'\in{H}_{1}$ and $g^{-1}g'\in{H}_{2}$, and by **Lemma 1.2.12 (Coset Coincidence Criterion)** again, $gH_{1}=g'H_{1}$ and $gH_{2}=g'H_{2}$; hence $\varphi$ is well-defined.

Injectivity: if $\left(gH_{1},gH_{2}\right)=\left(g'H_{1},g'H_{2}\right)$, then by **Lemma 1.2.12 (Coset Coincidence Criterion)**, $g^{-1}g'\in{H}_{1}$ and $g^{-1}g'\in{H}_{2}$, so $g^{-1}g'\in{H}_{1}\cap{H}_{2}$, and by **Lemma 1.2.12 (Coset Coincidence Criterion)** again, $g\left(H_{1}\cap{H}_{2}\right)=g'\left(H_{1}\cap{H}_{2}\right)$. Hence $\varphi$ is injective.

Therefore $\left[G:H_{1}\cap{H}_{2}\right]=\left|G/\left(H_{1}\cap{H}_{2}\right)\right|\le\left|G/H_{1}\right|\cdot\left|G/H_{2}\right|=\left[G:H_{1}\right]\left[G:H_{2}\right]$.

Next prove equality in the coprime case. By **Corollary 1.2.23 (Multiplicativity of the Index)**, since $H_{1}\cap{H}_{2}<{}H_{1}<{}G$,

$$
\left[G:H_{1}\cap{H}_{2}\right]=\left[G:H_{1}\right]\left[H_{1}:H_{1}\cap{H}_{2}\right].
$$

Hence $\left[G:H_{1}\right]\mid\left[G:H_{1}\cap{H}_{2}\right]$. Similarly, from $H_{1}\cap{H}_{2}<{}H_{2}<{}G$, we get $\left[G:H_{2}\right]\mid\left[G:H_{1}\cap{H}_{2}\right]$. Since $\left[G:H_{1}\right]$ and $\left[G:H_{2}\right]$ are coprime, by Greatest Common Divisor and Least Common Multiple, $\left[G:H_{1}\right]\left[G:H_{2}\right]\mid\left[G:H_{1}\cap{H}_{2}\right]$. Combined with the inequality $\left[G:H_{1}\cap{H}_{2}\right]\le\left[G:H_{1}\right]\left[G:H_{2}\right]$ just proved, we get $\left[G:H_{1}\cap{H}_{2}\right]=\left[G:H_{1}\right]\left[G:H_{2}\right]$.

Finally prove $G=H_{1}H_{2}$. By Order of a Product of Finite Subsets,

$$
\left|H_{1}H_{2}\right|=\frac{\left|H_{1}\right|\left|H_{2}\right|}{\left|H_{1}\cap{H}_{2}\right|}.
$$

By **Theorem 1.2.22 (Lagrange's Theorem)**, $\left|H_{1}\right|=\frac{\left|G\right|}{\left[G:H_{1}\right]}$, $\left|H_{2}\right|=\frac{\left|G\right|}{\left[G:H_{2}\right]}$, and

$$
\left|H_{1}\cap{H}_{2}\right|=\frac{\left|G\right|}{\left[G:H_{1}\cap{H}_{2}\right]}=\frac{\left|G\right|}{\left[G:H_{1}\right]\left[G:H_{2}\right]}.
$$

Substituting,

$$
\left|H_{1}H_{2}\right|=\frac{\frac{\left|G\right|}{\left[G:H_{1}\right]}\cdot\frac{\left|G\right|}{\left[G:H_{2}\right]}}{\frac{\left|G\right|}{\left[G:H_{1}\right]\left[G:H_{2}\right]}}=\left|G\right|.
$$

Since $H_{1}H_{2}\subseteq{G}$ and the two have the same number of elements, $G=H_{1}H_{2}$. $\blacksquare$

## 1.3-7

Prove that the conjugacy relation on a group $G$ is an equivalence relation, and hence the conjugacy classes form a partition of $G$.

### Solution to 1.3-7

Define a relation $R$ on $G$ by: $aRb$ if and only if there exists $g\in{G}$ such that $b=gag^{-1}$, i.e. $a,b$ are conjugate. We verify the three conditions of an equivalence relation.

Reflexivity: For any $a\in{G}$, take $g=e$; then $a=eae^{-1}$, so $aRa$.

Symmetry: If $aRb$, i.e. there exists $g\in{G}$ with $b=gag^{-1}$, then $a=g^{-1}bg$. Since $\left(g^{-1}\right)^{-1}=g$, we have $a=g^{-1}b\left(g^{-1}\right)^{-1}$, hence $bRa$.

Transitivity: If $aRb$ and $bRc$, i.e. there exist $g,h\in{G}$ with $b=gag^{-1}$ and $c=hbh^{-1}$, then

$$
c=hbh^{-1}=h\left(gag^{-1}\right)h^{-1}=\left(hg\right)a\left(hg\right)^{-1},
$$

so $aRc$.

In summary, the conjugacy relation $R$ is an equivalence relation. By Equivalence Classes Form a Partition, $G$ is partitioned into pairwise disjoint equivalence classes. The equivalence class of $a$ is exactly the conjugacy class $C_a$ of $a$ (Conjugacy Relation and Conjugacy Classes), so the conjugacy classes form a partition of $G$. $\blacksquare$

## 1.3-9

Let $H,K$ be two subgroups of a group $G$. Prove that if one of $H,K$ is a normal subgroup of $G$, then $HK<{}G$; and if both $H,K$ are normal subgroups of $G$, then $HK\triangleleft{G}$.

### Solution to 1.3-9

First prove that if one of $H,K$ is normal, then $HK<{}G$. Without loss of generality suppose $H\triangleleft{G}$. By **Theorem 1.3.5 (Equivalent Conditions for Normal Subgroups)** (condition (2)), $kH=Hk$ for every $k\in{K}$. Hence

$$
KH=\bigcup_{k\in{K}}kH=\bigcup_{k\in{K}}Hk=HK,
$$

i.e. $HK=KH$. By Product of Subgroups, $HK<{}G$. Similarly, if $K\triangleleft{G}$, the symmetric argument gives $HK<{}G$.

Next prove that if both $H,K$ are normal, then $HK\triangleleft{G}$. By the previous paragraph, $HK<{}G$. We now prove normality. For any $g\in{G}$ and $hk\in{H}K$,

$$
g\left(hk\right)g^{-1}=\left(ghg^{-1}\right)\left(gkg^{-1}\right).
$$

Since $H\triangleleft{G}$, by **Definition 1.3.1 (Normal Subgroup)**, $ghg^{-1}\in{H}$; since $K\triangleleft{G}$, similarly $gkg^{-1}\in{K}$. Hence $g\left(hk\right)g^{-1}\in{H}K$. Since $g$ and $hk$ are arbitrary, $g\left(HK\right)g^{-1}\subseteq{H}K$ for all $g\in{G}$, and by **Definition 1.3.1 (Normal Subgroup)**, $HK\triangleleft{G}$. $\blacksquare$

## 1.3-10

If a group $G$ has exactly one subgroup $H$ of order $m$, prove that $H\triangleleft{G}$.

### Solution to 1.3-10

For any $g\in{G}$, consider the set $gHg^{-1}=\left\{ghg^{-1}\mid{h}\in{H}\right\}$.

Step 1: verify that $gHg^{-1}<{}G$. For any $x,y\in{g}Hg^{-1}$, there exist $h_1,h_2\in{H}$ with $x=gh_1g^{-1}$, $y=gh_2g^{-1}$, and then

$$
xy^{-1}=gh_1g^{-1}\left(gh_2g^{-1}\right)^{-1}=gh_1g^{-1}gh_2^{-1}g^{-1}=g\left(h_1h_2^{-1}\right)g^{-1}\in{g}Hg^{-1}.
$$

By **Theorem 1.2.2 (Subgroup Criterion)** (condition (3)), $gHg^{-1}<{}G$.

Step 2: compute $\left|gHg^{-1}\right|$. By Conjugacy Maps Preserve Order, the map $h\mapsto{g}hg^{-1}$ is a bijection from $H$ to $gHg^{-1}$, so $\left|gHg^{-1}\right|=\left|H\right|=m$.

Step 3: uniqueness gives $gHg^{-1}=H$. Since $G$ has exactly one subgroup $H$ of order $m$, and $gHg^{-1}$ is also a subgroup of $G$ of order $m$, we have $gHg^{-1}=H$.

Step 4: prove that $H\triangleleft{G}$. For any $g\in{G}$ and $h\in{H}$, since $gHg^{-1}=H$, we have $ghg^{-1}\in{H}$. By **Definition 1.3.1 (Normal Subgroup)**, $H\triangleleft{G}$. $\blacksquare$

## 1.4-3

Let $G$ be a group. Define $R:G\to{S}_{G}$ by $R\left(a\right)=R_{a}$, where $R_{a}$ is the right translation. Prove that $R$ is an anti-isomorphism of $G$, i.e. it satisfies $R\left(ab\right)=R\left(b\right)R\left(a\right)$.

### Solution to 1.4-3

For any $g\in{G}$, by **Definition 1.4.9 (Left and Right Translations)**, $R_a\left(g\right)=ga$.

Step 1: prove that $R$ is an anti-homomorphism. For any $g\in{G}$,

$$
R\left(ab\right)\left(g\right)=R_{ab}\left(g\right)=g\left(ab\right)=\left(ga\right)b=R_b\left(ga\right)=R_b\left(R_a\left(g\right)\right)=\left(R_b\circ{R}_a\right)\left(g\right)=R\left(b\right)R\left(a\right)\left(g\right).
$$

Since $g$ is arbitrary, $R\left(ab\right)=R\left(b\right)R\left(a\right)$, and by Anti-Homomorphism and Anti-Isomorphism, $R$ is an anti-homomorphism from $G$ to $S_G$.

Step 2: prove that $R$ is injective. If $R\left(a\right)=R\left(b\right)$, then $R_a=R_b$. In particular $R_a\left(e\right)=R_b\left(e\right)$, i.e. $ea=eb$, so $a=b$. Hence $R$ is injective.

Step 3: prove that the image of $R$ is a subgroup of $S_G$. Write $R_G=\left\{R_a\mid{a}\in{G}\right\}$. By definition, $R:G\to{R}_G$ is surjective. Also, by Symmetric Groups and Bijective Transformations, $R_a$ is a bijection of $G$ (with inverse $R_{a^{-1}}$), so $R_G\subseteq{S}_G$, and $R_G$ is a subgroup of $S_G$ (closed under composition and inverses in $R_G$, since $R_aR_b=R_{ba}$ and $R_a^{-1}=R_{a^{-1}}$).

In summary, $R:G\to{R}_G$ is a bijective anti-homomorphism, and by Anti-Homomorphism and Anti-Isomorphism, $R$ is an anti-isomorphism; that is, $G$ is anti-isomorphic to the subgroup $R_G$ of $S_G$. $\blacksquare$

## 1.4-7

Prove that $f\left(x\right)=\cos{x}+\sqrt{-1}\sin{x}$ is a group homomorphism from $\left(\mathbb{R},+\right)$ to $\left(\mathbb{C}^{*},\cdot\right)$, and find $\ker{f}$.

### Solution to 1.4-7

Step 1: prove that $f$ is a group homomorphism. For any $x,y\in\mathbb{R}$, by Addition Formulas for Trigonometric Functions,

$$
f\left(x+y\right)=\cos\left(x+y\right)+\sqrt{-1}\sin\left(x+y\right)=\left(\cos{x}\cos{y}-\sin{x}\sin{y}\right)+\sqrt{-1}\left(\sin{x}\cos{y}+\cos{x}\sin{y}\right)=\left(\cos{x}+\sqrt{-1}\sin{x}\right)\left(\cos{y}+\sqrt{-1}\sin{y}\right)=f\left(x\right)f\left(y\right).
$$

Moreover $f\left(x\right)\ne0$ for all $x\in\mathbb{R}$ (since $\cos^2x+\sin^2x=1$) (Complex Exponentials and the Unit Circle), so $f:\mathbb{R}\to\mathbb{C}^{*}$ is well-defined. By **Definition 1.4.1 (Group Homomorphism and Isomorphism)**, $f$ is a group homomorphism from $\left(\mathbb{R},+\right)$ to $\left(\mathbb{C}^{*},\cdot\right)$.

Step 2: find $\ker{f}$. By **Definition 1.4.11 (Kernel and Image of a Homomorphism)**, $\ker{f}=\left\{x\in\mathbb{R}\mid{f}\left(x\right)=1\right\}$. By Complex Exponentials and the Unit Circle, $f\left(x\right)=\cos{x}+\sqrt{-1}\sin{x}=1$ if and only if $x=2k\pi$, $k\in\mathbb{Z}$. Hence

$$
\ker{f}=2\pi\mathbb{Z}=\left\{2k\pi\mid{k}\in\mathbb{Z}\right\}.
$$

By **Theorem 1.4.19 (Fundamental Theorem of Group Homomorphisms)**, $\mathbb{R}/2\pi\mathbb{Z}\cong\mathrm{Im}\left(f\right)$, where $\mathrm{Im}\left(f\right)=\left\{f\left(x\right)\mid{x}\in\mathbb{R}\right\}$ is the multiplicative group of complex numbers on the unit circle $\left\{z\in\mathbb{C}\mid\left|z\right|=1\right\}$ (Complex Exponentials and the Unit Circle). $\blacksquare$

## 1.4-8

Let $G$ and $H$ be groups and $\varphi:G\to\mathrm{Aut}\left(H\right)$ a group homomorphism. On the set $\left\{\left(g,h\right)\mid{g}\in{G},h\in{H}\right\}$ define the multiplication by

$$
\left(g_{1},h_{1}\right)\left(g_{2},h_{2}\right)=\left(g_{1}g_{2},\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right),
$$

Prove that this set is a group, called the semidirect product of $G$ and $H$, denoted $G\ltimes{H}$. Furthermore, $G_{1}=\left\{\left(g,e_{H}\right)\mid{g}\in{G}\right\}$ is a subgroup of $G\ltimes{H}$, and $H_{1}=\left\{\left(e_{G},h\right)\mid{h}\in{H}\right\}$ is a normal subgroup of $G\ltimes{H}$.

### Solution to 1.4-8

Write $G\ltimes{H}=\left\{\left(g,h\right)\mid{g}\in{G},h\in{H}\right\}$, with the multiplication defined as in the problem. We verify the group axioms one by one.

Closure: For any $\left(g_1,h_1\right),\left(g_2,h_2\right)\in{G}\ltimes{H}$, since $g_1g_2\in{G}$, and $\varphi\left(g_2^{-1}\right)\left(h_1\right)\in{H}$ (as $\varphi\left(g_2^{-1}\right)\in\mathrm{Aut}\left(H\right)$) and $h_2\in{H}$, we have $\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\in{H}$ (Properties of Homomorphisms into Automorphism Groups). Hence $\left(g_1g_2,\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)\in{G}\ltimes{H}$, so closure holds.

Associativity: For any $\left(g_1,h_1\right),\left(g_2,h_2\right),\left(g_3,h_3\right)\in{G}\ltimes{H}$, on one hand

$$
\left(\left(g_1,h_1\right)\left(g_2,h_2\right)\right)\left(g_3,h_3\right)=\left(g_1g_2,\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)\left(g_3,h_3\right)=\left(\left(g_1g_2\right)g_3,\varphi\left(g_3^{-1}\right)\left(\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)h_3\right).
$$

Since $\varphi\left(g_3^{-1}\right)\in\mathrm{Aut}\left(H\right)$ preserves the multiplication of $H$, we have $\varphi\left(g_3^{-1}\right)\left(\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)=\varphi\left(g_3^{-1}\right)\varphi\left(g_2^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)$; and by Properties of Homomorphisms into Automorphism Groups, $\varphi\left(g_3^{-1}\right)\varphi\left(g_2^{-1}\right)=\varphi\left(g_3^{-1}g_2^{-1}\right)=\varphi\left(\left(g_2g_3\right)^{-1}\right)$. Hence

$$
\left(\left(g_1,h_1\right)\left(g_2,h_2\right)\right)\left(g_3,h_3\right)=\left(\left(g_1g_2\right)g_3,\varphi\left(\left(g_2g_3\right)^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)\cdot{h}_3\right).
$$

On the other hand,

$$
\left(g_1,h_1\right)\left(\left(g_2,h_2\right)\left(g_3,h_3\right)\right)=\left(g_1,h_1\right)\left(g_2g_3,\varphi\left(g_3^{-1}\right)\left(h_2\right)h_3\right)=\left(g_1\left(g_2g_3\right),\varphi\left(\left(g_2g_3\right)^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)\cdot{h}_3\right).
$$

Since $G$ satisfies associativity, $\left(g_1g_2\right)g_3=g_1\left(g_2g_3\right)$; the second components of the two right-hand sides coincide, so associativity holds.

Identity: Consider $\left(e_G,e_H\right)$. For any $\left(g,h\right)\in{G}\ltimes{H}$, since $\varphi\left(e_G\right)=\mathrm{id}_H$ (Properties of Homomorphisms into Automorphism Groups), we have $\varphi\left(e_G^{-1}\right)\left(h\right)=\mathrm{id}_H\left(h\right)=h$, and hence

$$
\left(g,h\right)\left(e_G,e_H\right)=\left(g,\varphi\left(e_G^{-1}\right)\left(h\right)e_H\right)=\left(g,h\right),
$$

and

$$
\left(e_G,e_H\right)\left(g,h\right)=\left(g,\varphi\left(g^{-1}\right)\left(e_H\right)h\right)=\left(g,\mathrm{id}_H\left(e_H\right)h\right)=\left(g,h\right).
$$

Hence $\left(e_G,e_H\right)$ is the identity.

Inverse: For $\left(g,h\right)\in{G}\ltimes{H}$, consider $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$. Since $\varphi\left(\left(g^{-1}\right)^{-1}\right)=\varphi\left(g\right)$, and $\varphi\left(g^{-1}\right)\varphi\left(g\right)=\mathrm{id}_H$, $\varphi\left(g\right)\varphi\left(g^{-1}\right)=\mathrm{id}_H$ (Properties of Homomorphisms into Automorphism Groups), we have

$$
\left(g,h\right)\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_G,\varphi\left(g\right)\left(h\right)\cdot\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_G,\varphi\left(g\right)\left(hh^{-1}\right)\right)=\left(e_G,e_H\right),
$$

and

$$
\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)\left(g,h\right)=\left(e_G,\varphi\left(g^{-1}\right)\left(\varphi\left(g\right)\left(h^{-1}\right)\right)h\right)=\left(e_G,\left(\varphi\left(g^{-1}\right)\varphi\left(g\right)\right)\left(h^{-1}\right)\cdot{h}\right)=\left(e_G,h^{-1}h\right)=\left(e_G,e_H\right).
$$

Hence $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$ is the inverse of $\left(g,h\right)$.

Since closure, associativity, identity and inverse all hold, $G\ltimes{H}$ is a group.

Verify $G_1<{}G\ltimes{H}$. $\left(e_G,e_H\right)\in{G}_1$, so $G_1$ is nonempty. For $\left(g_1,e_H\right),\left(g_2,e_H\right)\in{G}_1$, by the inverse formula, $\left(g_2,e_H\right)^{-1}=\left(g_2^{-1},\varphi\left(g_2\right)\left(e_H\right)\right)=\left(g_2^{-1},e_H\right)$, and hence

$$
\left(g_1,e_H\right)\left(g_2,e_H\right)^{-1}=\left(g_1,e_H\right)\left(g_2^{-1},e_H\right)=\left(g_1g_2^{-1},\varphi\left(\left(g_2^{-1}\right)^{-1}\right)\left(e_H\right)e_H\right)=\left(g_1g_2^{-1},\varphi\left(g_2\right)\left(e_H\right)\right)=\left(g_1g_2^{-1},e_H\right)\in{G}_1.
$$

By **Theorem 1.2.2 (Subgroup Criterion)**, $G_1<{}G\ltimes{H}$.

Verify $H_1\triangleleft{G}\ltimes{H}$. First prove $H_1<{}G\ltimes{H}$: $\left(e_G,e_H\right)\in{H}_1$, nonempty; for $\left(e_G,h_1\right),\left(e_G,h_2\right)\in{H}_1$, by the inverse formula, $\left(e_G,h_2\right)^{-1}=\left(e_G,\varphi\left(e_G\right)\left(h_2^{-1}\right)\right)=\left(e_G,h_2^{-1}\right)$, and hence

$$
\left(e_G,h_1\right)\left(e_G,h_2\right)^{-1}=\left(e_G,h_1\right)\left(e_G,h_2^{-1}\right)=\left(e_G,\varphi\left(e_G^{-1}\right)\left(h_1\right)h_2^{-1}\right)=\left(e_G,h_1h_2^{-1}\right)\in{H}_1.
$$

By **Theorem 1.2.2 (Subgroup Criterion)**, $H_1<{}G\ltimes{H}$. Now prove normality: for any $\left(g,k\right)\in{G}\ltimes{H}$ and $\left(e_G,h\right)\in{H}_1$, by the inverse formula $\left(g,k\right)^{-1}=\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)$, and $\varphi\left(e_G^{-1}\right)=\mathrm{id}_H$, $\varphi\left(g\right)\varphi\left(g^{-1}\right)=\mathrm{id}_H$, we compute

$$
\left(g,k\right)\left(e_G,h\right)\left(g,k\right)^{-1}=\left(g,\varphi\left(e_G^{-1}\right)\left(k\right)h\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(g,kh\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_G,\varphi\left(g^{-1}\right)\left(kh\right)\cdot\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_G,\varphi\left(g^{-1}\right)\varphi\left(g\right)\left(h\right)\right)=\left(e_G,h\right)\in{H}_1.
$$

Hence $\left(g,k\right)H_1\left(g,k\right)^{-1}\subseteq{H}_1$ for all $\left(g,k\right)\in{G}\ltimes{H}$, and by **Definition 1.3.1 (Normal Subgroup)**, $H_1\triangleleft{G}\ltimes{H}$. $\blacksquare$
