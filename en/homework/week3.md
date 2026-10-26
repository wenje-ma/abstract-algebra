# Assignment 3

> **Definition 1.3.1** (Normal Subgroup) Let $H$ be a subgroup of a group $G$. If for any $g\in G$ and $h\in H$ we have $ghg^{-1}\in H$, then $H$ is called a normal subgroup of $G$, denoted $H\triangleleft G$.

> **Theorem 1.3.5** (Equivalent Conditions for a Normal Subgroup)
> 
> Let $G$ be a group and $H< G$. Then the following conditions are equivalent:
> 
> (1) $H\triangleleft G$;
> 
> (2) for any $g\in G$, $gH=Hg$;
> 
> (3) for any $a,b\in G$, $aH\cdot bH=abH$.

> **Theorem 1.3.6** (Quotient Group) Let $G$ be a group and $H\triangleleft G$. Then $G/H$ forms a group under coset multiplication $aH\cdot bH=abH$, called the quotient group of $G$ by $H$.

> **Basic Knowledge** (Conjugate Elements and Conjugacy Classes) Two elements $G$ in $a,b$ are said to be conjugate if there exists $g\in G$ such that $b=gag^{-1}$. The set of all elements conjugate to $a$ is called the conjugacy class of $a$.

> **Basic Knowledge** (Product of Subgroups) Let $H,K$ be subgroups of a group $G$. Then
> $$
> HK=\left\{hk\mid h\in H,k\in K\right\}.
> $$
> $HK$ is a subgroup of $G$ if and only if $HK=KH$.

### Problem 1

(Problem 1.3-7) Prove that the conjugacy relation between elements of a group $G$ is an equivalence relation, so that the conjugacy classes form a partition of $G$.

### Solution to Problem 1

Define a relation $G$ on $R$ by: $aRb$ if and only if there exists $g\in G$ such that $b=gag^{-1}$, i.e. $a,b$ are conjugate. We verify the three conditions for an equivalence relation.

**Reflexivity** For any $a\in G$, take $g=e$; then $a=eae^{-1}$, so $aRa$.

**Symmetry** If $aRb$, i.e. there exists $g\in G$ with $b=gag^{-1}$, then $a=g^{-1}bg=g^{-1}b\left(g^{-1}\right)^{-1}$, so $bRa$.

**Transitivity** If $aRb$ and $bRc$, i.e. there exist $g,h\in G$ with $b=gag^{-1}$ and $c=hbh^{-1}$, then

$$
c=hbh^{-1}=h\left(gag^{-1}\right)h^{-1}=\left(hg\right)a\left(hg\right)^{-1},
$$

so $aRc$.

Hence the conjugacy relation is an equivalence relation. By the general theory of equivalence relations, $G$ is partitioned into a disjoint union of conjugacy classes. $\blacksquare$

### Problem 2

(Problem 1.3-9) Let $H,K$ be two subgroups of a group $G$. Prove that if one of $H,K$ is a normal subgroup of $G$, then $HK< G$; if both $H,K$ are normal subgroups of $G$, then $HK\triangleleft G$.

### Solution to Problem 2

First prove that if one of $H,K$ is normal then $HK< G$. Without loss of generality, assume $H\triangleleft G$.

By **Theorem 1.3.5** (Equivalent Conditions for a Normal Subgroup), for any $k\in K$ we have $kH=Hk$. Then

$$
KH=\bigcup_{k\in K}kH=\bigcup_{k\in K}Hk=HK,
$$

i.e. $HK=KH$. By **Basic Knowledge** (Product of Subgroups), $HK< G$.

Now prove that if both $H,K$ are normal then $HK\triangleleft G$.

From the above, $HK< G$. We now prove normality. For any $g\in G$ and $hk\in HK$,

$$
g\left(hk\right)g^{-1}=\left(ghg^{-1}\right)\left(gkg^{-1}\right).
$$

Since $H\triangleleft G$, $ghg^{-1}\in H$; since $K\triangleleft G$, $gkg^{-1}\in K$. Therefore $g\left(hk\right)g^{-1}\in HK$. By the arbitrariness of $g,hk$, $g\left(HK\right)g^{-1}\subseteq HK$. By **Definition 1.3.1** (Normal Subgroup), $HK\triangleleft G$. $\blacksquare$

### Problem 3

(Problem 1.3-10) If a group $G$ has only one subgroup $m$ of order $H$, prove that $H\triangleleft G$.

### Solution to Problem 3

For any $g\in G$, consider the conjugate subgroup $gHg^{-1}$.

First, $gHg^{-1}$ is a subgroup of $G$. Indeed, the map

$$
\varphi:H\to gHg^{-1}, h\mapsto ghg^{-1}
$$

is a bijection (its inverse is $x\mapsto g^{-1}xg$) and preserves the multiplication:

$$
\varphi\left(h_{1}h_{2}\right)=gh_{1}h_{2}g^{-1}=\left(gh_{1}g^{-1}\right)\left(gh_{2}g^{-1}\right)=\varphi\left(h_{1}\right)\varphi\left(h_{2}\right).
$$

Hence $gHg^{-1}< G$.

Second, since $\varphi$ is a bijection, $\left|gHg^{-1}\right|=\left|H\right|=m$.

Since $G$ has only one subgroup of order $m$, we have $gHg^{-1}=H$.

By **Theorem 1.3.5** (Equivalent Conditions for a Normal Subgroup), $H\triangleleft G$. $\blacksquare$
