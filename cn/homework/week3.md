# week3

> **基础知识: 共轭关系与共轭类**<br>称群 $G$ 中的两个元素 $a,b$ 是共轭的, 如果存在 $g\in G$ 使得 $b=gag^{-1}$. 与 $a$ 共轭的所有元素的全体 $C_a=\left\{gag^{-1}\mid g\in G\right\}$ 称为 $a$ 的共轭类.

> **基础知识: 等价关系的等价类构成划分**<br>设 $R$ 是集合 $A$ 上的等价关系, 则 $A$ 中互不相同的等价类两两不交, 且它们的并等于 $A$, 即等价类全体构成 $A$ 的一个划分.

> **基础知识: 子群乘积**<br>设 $H,K$ 是群 $G$ 的子群, 记 $HK=\left\{hk\mid h\in H,k\in K\right\}$, $KH=\left\{kh\mid k\in K,h\in H\right\}$. 则 $HK<G$ 当且仅当 $HK=KH$: 若 $HK<G$, 则对 $hk\in HK$, $\left(hk\right)^{-1}=k^{-1}h^{-1}\in HK$, 即 $KH\subseteq HK$; 又 $\left(k^{-1}h^{-1}\right)^{-1}=hk\in HK$ 说明 $HK\subseteq KH$, 故 $HK=KH$. 反之若 $HK=KH$, 对任意 $hk,h'k'\in HK$, 因 $kh'\in KH=HK$, 设 $kh'=h''k''$, 则 $\left(hk\right)\left(h'k'\right)=h\left(kh'\right)k'=h\left(h''k''\right)k'=\left(hh''\right)\left(k''k'\right)\in HK$; 且 $\left(hk\right)^{-1}=k^{-1}h^{-1}\in KH=HK$, 故由**定理 1.2.2 (子群判别法)** (条件 (2)), $HK<G$.

> **基础知识: 共轭映射保持阶**<br>对 $g\in G$, 映射 $\varphi_g:H\to gHg^{-1}$, $h\mapsto ghg^{-1}$ 是双射, 故 $\left|gHg^{-1}\right|=\left|H\right|$.

> **定理 1.2.2 (子群判别法)**<br>设 $H$ 是群 $G$ 的非空子集, 则下列条件等价: (1) $H$ 是 $G$ 的子群; (2) 对任意 $a,b\in H$, 有 $ab\in H$, $a^{-1}\in H$; (3) 对任意 $a,b\in H$, 有 $ab^{-1}\in H$.

> **定义 1.3.1 (正规子群)**<br>设 $H$ 是群 $G$ 的子群. 如果对任意 $g\in G$, $h\in H$, 有 $ghg^{-1}\in H$, 则称 $H$ 为 $G$ 的一个正规子群, 记为 $H\triangleleft G$.

> **定理 1.3.5 (正规子群的等价条件)**<br>设 $G$ 是群, $H<G$, 则下列条件等价: (1) $H\triangleleft G$; (2) 对任意 $g\in G$, $gH=Hg$; (3) 对任意 $a,b\in G$, $aH\cdot bH=abH$, 这里 $aH\cdot bH=\left\{ah_1bh_2\mid h_1,h_2\in H\right\}$.

---

## 1.3-7

证明: 群 $G$ 中元素的共轭关系是一个等价关系, 从而共轭类构成了 $G$ 的一个划分.

### 解答 1.3-7

定义 $G$ 上的关系 $R$: $aRb$ 当且仅当存在 $g\in G$ 使得 $b=gag^{-1}$, 即 $a,b$ 共轭. 下面验证等价关系的三个条件.

**反身性**: 对任意 $a\in G$, 取 $g=e$, 则 $a=eae^{-1}$, 故 $aRa$.

**对称性**: 若 $aRb$, 即存在 $g\in G$ 使 $b=gag^{-1}$, 则 $a=g^{-1}bg$. 因 $\left(g^{-1}\right)^{-1}=g$, 故 $a=g^{-1}b\left(g^{-1}\right)^{-1}$, 从而 $bRa$.

**传递性**: 若 $aRb$ 且 $bRc$, 即存在 $g,h\in G$ 使 $b=gag^{-1}$, $c=hbh^{-1}$, 则

$$
c=hbh^{-1}=h\left(gag^{-1}\right)h^{-1}=\left(hg\right)a\left(hg\right)^{-1},
$$

故 $aRc$.

综上, 共轭关系 $R$ 是等价关系. 由**基础知识: 等价关系的等价类构成划分**, $G$ 划分为互不相交的等价类之并. 而 $a$ 所在的等价类恰为 $a$ 的共轭类 $C_a$ (**基础知识: 共轭关系与共轭类**), 故共轭类构成 $G$ 的一个划分. $\blacksquare$

---

## 1.3-9

设 $H,K$ 是群 $G$ 的两个子群. 证明: $H,K$ 中有一个是 $G$ 的正规子群, 则 $HK<G$; 若 $H,K$ 均是 $G$ 的正规子群, 则 $HK\triangleleft G$.

### 解答 1.3-9

**先证若 $H,K$ 中有一个是正规子群, 则 $HK<G$.** 不妨设 $H\triangleleft G$. 由**定理 1.3.5 (正规子群的等价条件)** (条件 (2)), 对任意 $k\in K$ 有 $kH=Hk$. 于是

$$
KH=\bigcup_{k\in K}kH=\bigcup_{k\in K}Hk=HK,
$$

即 $HK=KH$. 由**基础知识: 子群乘积**, $HK<G$. 同理, 若 $K\triangleleft G$, 由对称论证亦得 $HK<G$.

**再证若 $H,K$ 均是正规子群, 则 $HK\triangleleft G$.** 由上一段, $HK<G$. 下证正规性. 对任意 $g\in G$ 与 $hk\in HK$, 有

$$
g\left(hk\right)g^{-1}=\left(ghg^{-1}\right)\left(gkg^{-1}\right).
$$

因 $H\triangleleft G$, 由**定义 1.3.1 (正规子群)**, $ghg^{-1}\in H$; 因 $K\triangleleft G$, 同理 $gkg^{-1}\in K$. 故 $g\left(hk\right)g^{-1}\in HK$. 由 $g$ 与 $hk$ 的任意性, 对任意 $g\in G$ 有 $g\left(HK\right)g^{-1}\subseteq HK$, 依据**定义 1.3.1 (正规子群)**, $HK\triangleleft G$. $\blacksquare$

---

## 1.3-10

若群 $G$ 只有一个阶为 $m$ 的子群 $H$, 证明: $H\triangleleft G$.

### 解答 1.3-10

对任意 $g\in G$, 考虑集合 $gHg^{-1}=\left\{ghg^{-1}\mid h\in H\right\}$.

**第一步: 验证 $gHg^{-1}<G$.** 对任意 $x,y\in gHg^{-1}$, 存在 $h_1,h_2\in H$ 使 $x=gh_1g^{-1}$, $y=gh_2g^{-1}$, 则

$$
xy^{-1}=gh_1g^{-1}\left(gh_2g^{-1}\right)^{-1}=gh_1g^{-1}gh_2^{-1}g^{-1}=g\left(h_1h_2^{-1}\right)g^{-1}\in gHg^{-1}.
$$

由**定理 1.2.2 (子群判别法)** (条件 (3)), $gHg^{-1}<G$.

**第二步: 求 $\left|gHg^{-1}\right|$.** 由**基础知识: 共轭映射保持阶**, 映射 $h\mapsto ghg^{-1}$ 是 $H$ 到 $gHg^{-1}$ 的双射, 故 $\left|gHg^{-1}\right|=\left|H\right|=m$.

**第三步: 由唯一性得 $gHg^{-1}=H$.** 因 $G$ 只有一个阶为 $m$ 的子群 $H$, 而 $gHg^{-1}$ 也是 $G$ 的阶为 $m$ 的子群, 故 $gHg^{-1}=H$.

**第四步: 证明 $H\triangleleft G$.** 对任意 $g\in G$, $h\in H$, 因 $gHg^{-1}=H$, 故 $ghg^{-1}\in H$. 依据**定义 1.3.1 (正规子群)**, $H\triangleleft G$. $\blacksquare$
