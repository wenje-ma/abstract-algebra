# week3

> **Basic Knowledge: Conjugacy Relation and Conjugacy Classes**<br>Two elements $a,b$ of a group $G$ are called conjugate if there exists $g\in G$ such that $b=gag^{-1}$. The set $C_a=\left\{gag^{-1}\mid g\in G\right\}$ of all elements conjugate to $a$ is called the conjugacy class of $a$.

> **Basic Knowledge: Equivalence Classes Form a Partition**<br>Let $R$ be an equivalence relation on a set $A$. Then distinct equivalence classes in $A$ are pairwise disjoint, and their union is $A$; that is, the equivalence classes form a partition of $A$.

> **Basic Knowledge: Product of Subgroups**<br>Let $H,K$ be subgroups of a group $G$, and write $HK=\left\{hk\mid h\in H,k\in K\right\}$, $KH=\left\{kh\mid k\in K,h\in H\right\}$. Then $HK<G$ if and only if $HK=KH$: if $HK<G$, then for $hk\in HK$, $\left(hk\right)^{-1}=k^{-1}h^{-1}\in HK$, i.e. $KH\subseteq HK$; and $\left(k^{-1}h^{-1}\right)^{-1}=hk\in HK$ shows $HK\subseteq KH$, so $HK=KH$. Conversely, if $HK=KH$, then for any $hk,h'k'\in HK$, since $kh'\in KH=HK$, write $kh'=h''k''$; then $\left(hk\right)\left(h'k'\right)=h\left(kh'\right)k'=h\left(h''k''\right)k'=\left(hh''\right)\left(k''k'\right)\in HK$; and $\left(hk\right)^{-1}=k^{-1}h^{-1}\in KH=HK$, so by **Theorem 1.2.2 (Subgroup Criterion)** (condition (2)), $HK<G$.

> **Basic Knowledge: Conjugacy Maps Preserve Order**<br>For $g\in G$, the map $\varphi_g:H\to gHg^{-1}$, $h\mapsto ghg^{-1}$ is a bijection, so $\left|gHg^{-1}\right|=\left|H\right|$.

> **Theorem 1.2.2 (Subgroup Criterion)**<br>Let $H$ be a nonempty subset of a group $G$. Then the following conditions are equivalent: (1) $H$ is a subgroup of $G$; (2) for all $a,b\in H$, $ab\in H$ and $a^{-1}\in H$; (3) for all $a,b\in H$, $ab^{-1}\in H$.

> **Definition 1.3.1 (Normal Subgroup)**<br>Let $H$ be a subgroup of a group $G$. If $ghg^{-1}\in H$ for all $g\in G$ and $h\in H$, then $H$ is called a normal subgroup of $G$, denoted $H\triangleleft G$.

> **Theorem 1.3.5 (Equivalent Conditions for Normal Subgroups)**<br>Let $G$ be a group and $H<G$. Then the following conditions are equivalent: (1) $H\triangleleft G$; (2) $gH=Hg$ for all $g\in G$; (3) $aH\cdot bH=abH$ for all $a,b\in G$, where $aH\cdot bH=\left\{ah_1bh_2\mid h_1,h_2\in H\right\}$.

---

## 1.3-7

Prove that the conjugacy relation on a group $G$ is an equivalence relation, and hence the conjugacy classes form a partition of $G$.

### Solution 1.3-7

Define a relation $R$ on $G$ by: $aRb$ if and only if there exists $g\in G$ such that $b=gag^{-1}$, i.e. $a,b$ are conjugate. We verify the three conditions of an equivalence relation.

**Reflexivity**: For any $a\in G$, take $g=e$; then $a=eae^{-1}$, so $aRa$.

**Symmetry**: If $aRb$, i.e. there exists $g\in G$ with $b=gag^{-1}$, then $a=g^{-1}bg$. Since $\left(g^{-1}\right)^{-1}=g$, we have $a=g^{-1}b\left(g^{-1}\right)^{-1}$, hence $bRa$.

**Transitivity**: If $aRb$ and $bRc$, i.e. there exist $g,h\in G$ with $b=gag^{-1}$ and $c=hbh^{-1}$, then

$$
c=hbh^{-1}=h\left(gag^{-1}\right)h^{-1}=\left(hg\right)a\left(hg\right)^{-1},
$$

so $aRc$.

In summary, the conjugacy relation $R$ is an equivalence relation. By **Basic Knowledge: Equivalence Classes Form a Partition**, $G$ is partitioned into pairwise disjoint equivalence classes. The equivalence class of $a$ is exactly the conjugacy class $C_a$ of $a$ (**Basic Knowledge: Conjugacy Relation and Conjugacy Classes**), so the conjugacy classes form a partition of $G$. $\blacksquare$

---

## 1.3-9

Let $H,K$ be two subgroups of a group $G$. Prove that if one of $H,K$ is a normal subgroup of $G$, then $HK<G$; and if both $H,K$ are normal subgroups of $G$, then $HK\triangleleft G$.

### Solution 1.3-9

**First prove that if one of $H,K$ is normal, then $HK<G$.** Without loss of generality suppose $H\triangleleft G$. By **Theorem 1.3.5 (Equivalent Conditions for Normal Subgroups)** (condition (2)), $kH=Hk$ for every $k\in K$. Hence

$$
KH=\bigcup_{k\in K}kH=\bigcup_{k\in K}Hk=HK,
$$

i.e. $HK=KH$. By **Basic Knowledge: Product of Subgroups**, $HK<G$. Similarly, if $K\triangleleft G$, the symmetric argument gives $HK<G$.

**Next prove that if both $H,K$ are normal, then $HK\triangleleft G$.** By the previous paragraph, $HK<G$. We now prove normality. For any $g\in G$ and $hk\in HK$,

$$
g\left(hk\right)g^{-1}=\left(ghg^{-1}\right)\left(gkg^{-1}\right).
$$

Since $H\triangleleft G$, by **Definition 1.3.1 (Normal Subgroup)**, $ghg^{-1}\in H$; since $K\triangleleft G$, similarly $gkg^{-1}\in K$. Hence $g\left(hk\right)g^{-1}\in HK$. Since $g$ and $hk$ are arbitrary, $g\left(HK\right)g^{-1}\subseteq HK$ for all $g\in G$, and by **Definition 1.3.1 (Normal Subgroup)**, $HK\triangleleft G$. $\blacksquare$

---

## 1.3-10

If a group $G$ has exactly one subgroup $H$ of order $m$, prove that $H\triangleleft G$.

### Solution 1.3-10

For any $g\in G$, consider the set $gHg^{-1}=\left\{ghg^{-1}\mid h\in H\right\}$.

**Step 1: verify that $gHg^{-1}<G$.** For any $x,y\in gHg^{-1}$, there exist $h_1,h_2\in H$ with $x=gh_1g^{-1}$, $y=gh_2g^{-1}$, and then

$$
xy^{-1}=gh_1g^{-1}\left(gh_2g^{-1}\right)^{-1}=gh_1g^{-1}gh_2^{-1}g^{-1}=g\left(h_1h_2^{-1}\right)g^{-1}\in gHg^{-1}.
$$

By **Theorem 1.2.2 (Subgroup Criterion)** (condition (3)), $gHg^{-1}<G$.

**Step 2: compute $\left|gHg^{-1}\right|$.** By **Basic Knowledge: Conjugacy Maps Preserve Order**, the map $h\mapsto ghg^{-1}$ is a bijection from $H$ to $gHg^{-1}$, so $\left|gHg^{-1}\right|=\left|H\right|=m$.

**Step 3: uniqueness gives $gHg^{-1}=H$.** Since $G$ has exactly one subgroup $H$ of order $m$, and $gHg^{-1}$ is also a subgroup of $G$ of order $m$, we have $gHg^{-1}=H$.

**Step 4: prove that $H\triangleleft G$.** For any $g\in G$ and $h\in H$, since $gHg^{-1}=H$, we have $ghg^{-1}\in H$. By **Definition 1.3.1 (Normal Subgroup)**, $H\triangleleft G$. $\blacksquare$
