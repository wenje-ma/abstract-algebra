# week3

> **定义 1.2.1 (子群)**
> 
> 设 $H$ 是群 $G$ 的一个非空子集, 如果 $H$ 对于 $G$ 的运算也构成群, 则称 $H$ 为 $G$ 的子群, 记作 $H< G$.

> **定理 1.2.2 (子群判别法)**
> 
> 设 $H$ 是群 $G$ 的非空子集, 则下列条件等价: (1) $H$ 是 $G$ 的子群; (2) 对任意 $a,b\in H$, 有 $ab\in H$, $a^{-1}\in H$; (3) 对任意 $a,b\in H$, 有 $ab^{-1}\in H$.

> **引理 1.2.12 (陪集重合条件)**
> 
> 设 $H$ 是群 $G$ 的子群, $a,b\in G$, 则 $aH$ 和 $bH$ 要么互不相交, 要么重合, 且 $aH=bH$ 当且仅当 $a^{-1}b\in H$.

> **定理 1.2.22 (拉格朗日定理)**
> 
> 设 $G$ 是有限群, $H< G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, 其中 $\left[G:H\right]$ 为 $H$ 在 $G$ 中的指数. 从而子群 $H$ 的阶是群 $G$ 的阶的因子, 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

> **推论 1.2.23 (指数的乘法)**
> 
> 设 $G$ 是有限群, $K< G$, $H< K$, 则 $\left[G:H\right]=\left[G:K\right]\cdot\left[K:H\right]$.

> **定义 1.3.1 (正规子群)**
> 
> 设 $H$ 是群 $G$ 的子群. 如果对任意 $g\in G$, $h\in H$, 有 $ghg^{-1}\in H$, 则称 $H$ 为 $G$ 的一个正规子群, 记为 $H\triangleleft G$.

> **定理 1.3.5 (正规子群的等价条件)**
> 
> 设 $G$ 是群, $H< G$, 则下列条件等价: (1) $H\triangleleft G$; (2) 对任意 $g\in G$, $gH=Hg$; (3) 对任意 $a,b\in G$, $aH\cdot bH=abH$, 这里 $aH\cdot bH=\left\{ah_1bh_2\mid h_1,h_2\in H\right\}$.

> **定义 1.4.1 (群同态与同构)**
> 
> 设 $G$ 和 $G'$ 是两个群, 如果映射 $f:G\to G'$ 满足 $f\left(ab\right)=f\left(a\right)f\left(b\right)$, $\forall a,b\in G$, 则称 $f$ 是 $G$ 到 $G'$ 的群同态. 若同态 $f$ 是双射, 则称 $f$ 是 $G$ 到 $G'$ 的群同构, 此时称群 $G$ 与 $G'$ 是同构的, 记为 $G\cong G'$.

> **定义 1.4.9 (左平移与右平移)**
> 
> 对任意 $a\in G$, 定义 $G$ 上的变换 $L_a,R_a$ 为 $L_a\left(g\right)=ag$, $R_a\left(g\right)=ga$, $\forall g\in G$; 分别称 $L_a,R_a$ 为由 $a$ 决定的左平移变换和右平移变换.

> **定义 1.4.11 (同态的核与像)**
> 
> 设 $f:G\to G'$ 是群同态, 则集合 $\ker f=\left\{a\in G\mid f\left(a\right)=e'\right\}$ 称为同态 $f$ 的核, 集合 $\mathrm{Im}\left(f\right)=f\left(G\right)=\left\{f\left(a\right)\mid a\in G\right\}$ 称为同态 $f$ 的像.

> **定理 1.4.19 (群的同态基本定理)**
> 
> 设 $f:G\to G'$ 是群的满同态, 则 $G/\ker f\cong G'$.

## 1.2-20

设 $H_{1},H_{2}$ 为有限群 $G$ 的两个子群, 证明

$$
\left[G:H_{1}\cap H_{2}\right]\le\left[G:H_{1}\right]\left[G:H_{2}\right].
$$

又若 $\left[G:H_{1}\right]$ 与 $\left[G:H_{2}\right]$ 互素, 则

$$
\left[G:H_{1}\cap H_{2}\right]=\left[G:H_{1}\right]\left[G:H_{2}\right]
$$

且 $G=H_{1}H_{2}$.

### 解答 1.2-20

**先证不等式.** 考虑映射

$$
\varphi:G/\left(H_{1}\cap H_{2}\right)\to G/H_{1}\times G/H_{2},\quad g\left(H_{1}\cap H_{2}\right)\mapsto\left(gH_{1},gH_{2}\right).
$$

**良定义**: 若 $g\left(H_{1}\cap H_{2}\right)=g'\left(H_{1}\cap H_{2}\right)$, 则由**引理 1.2.12 (陪集重合条件)**, $g^{-1}g'\in H_{1}\cap H_{2}$, 故 $g^{-1}g'\in H_{1}$ 且 $g^{-1}g'\in H_{2}$, 再由**引理 1.2.12 (陪集重合条件)**, $gH_{1}=g'H_{1}$, $gH_{2}=g'H_{2}$, 于是 $\varphi$ 良定义.

Wait, I used 定理1.2.19 which isn't in my citation env. Let me add it, or use 引理1.2.12 (aH=bH iff a^{-1}b∈H). Let me use 引理1.2.12. I need to add 引理1.2.12 to the citation env.

Let me revise: use 引理1.2.12 (aH=bH iff a^{-1}b∈H). I'll add it to the citation environment.

Let me rewrite that part with 引理1.2.12.

**单射**: 若 $\left(gH_{1},gH_{2}\right)=\left(g'H_{1},g'H_{2}\right)$, 则由**引理 1.2.12 (陪集重合条件)**, $g^{-1}g'\in H_{1}$ 且 $g^{-1}g'\in H_{2}$, 故 $g^{-1}g'\in H_{1}\cap H_{2}$, 再由**引理 1.2.12 (陪集重合条件)**, $g\left(H_{1}\cap H_{2}\right)=g'\left(H_{1}\cap H_{2}\right)$. 故 $\varphi$ 是单射.

于是 $\left[G:H_{1}\cap H_{2}\right]=\left|G/\left(H_{1}\cap H_{2}\right)\right|\le\left|G/H_{1}\right|\cdot\left|G/H_{2}\right|=\left[G:H_{1}\right]\left[G:H_{2}\right]$.

**再证互素情形下的等号.** 由**推论 1.2.23 (指数的乘法)**, 因 $H_{1}\cap H_{2}< H_{1}< G$,

$$
\left[G:H_{1}\cap H_{2}\right]=\left[G:H_{1}\right]\left[H_{1}:H_{1}\cap H_{2}\right].
$$

故 $\left[G:H_{1}\right]\mid\left[G:H_{1}\cap H_{2}\right]$. 同理, 由 $H_{1}\cap H_{2}< H_{2}< G$, $\left[G:H_{2}\right]\mid\left[G:H_{1}\cap H_{2}\right]$. 因 $\left[G:H_{1}\right]$ 与 $\left[G:H_{2}\right]$ 互素, 由最大公因数与最小公倍数, $\left[G:H_{1}\right]\left[G:H_{2}\right]\mid\left[G:H_{1}\cap H_{2}\right]$. 结合已证不等式 $\left[G:H_{1}\cap H_{2}\right]\le\left[G:H_{1}\right]\left[G:H_{2}\right]$, 得 $\left[G:H_{1}\cap H_{2}\right]=\left[G:H_{1}\right]\left[G:H_{2}\right]$.

**最后证 $G=H_{1}H_{2}$.** 由有限集乘积的阶,

$$
\left|H_{1}H_{2}\right|=\frac{\left|H_{1}\right|\left|H_{2}\right|}{\left|H_{1}\cap H_{2}\right|}.
$$

由**定理 1.2.22 (拉格朗日定理)**, $\left|H_{1}\right|=\frac{\left|G\right|}{\left[G:H_{1}\right]}$, $\left|H_{2}\right|=\frac{\left|G\right|}{\left[G:H_{2}\right]}$, 且

$$
\left|H_{1}\cap H_{2}\right|=\frac{\left|G\right|}{\left[G:H_{1}\cap H_{2}\right]}=\frac{\left|G\right|}{\left[G:H_{1}\right]\left[G:H_{2}\right]}.
$$

代入得

$$
\left|H_{1}H_{2}\right|=\frac{\frac{\left|G\right|}{\left[G:H_{1}\right]}\cdot\frac{\left|G\right|}{\left[G:H_{2}\right]}}{\frac{\left|G\right|}{\left[G:H_{1}\right]\left[G:H_{2}\right]}}=\left|G\right|.
$$

因 $H_{1}H_{2}\subseteq G$ 且两者元素个数相等, 故 $G=H_{1}H_{2}$. $\blacksquare$

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

综上, 共轭关系 $R$ 是等价关系. 由等价关系的等价类构成划分, $G$ 划分为互不相交的等价类之并. 而 $a$ 所在的等价类恰为 $a$ 的共轭类 $C_a$ (共轭关系与共轭类), 故共轭类构成 $G$ 的一个划分. $\blacksquare$

## 1.3-9

设 $H,K$ 是群 $G$ 的两个子群. 证明: $H,K$ 中有一个是 $G$ 的正规子群, 则 $HK< G$; 若 $H,K$ 均是 $G$ 的正规子群, 则 $HK\triangleleft G$.

### 解答 1.3-9

**先证若 $H,K$ 中有一个是正规子群, 则 $HK< G$.** 不妨设 $H\triangleleft G$. 由**定理 1.3.5 (正规子群的等价条件)** (条件 (2)), 对任意 $k\in K$ 有 $kH=Hk$. 于是

$$
KH=\bigcup_{k\in K}kH=\bigcup_{k\in K}Hk=HK,
$$

即 $HK=KH$. 由子群乘积, $HK< G$. 同理, 若 $K\triangleleft G$, 由对称论证亦得 $HK< G$.

**再证若 $H,K$ 均是正规子群, 则 $HK\triangleleft G$.** 由上一段, $HK< G$. 下证正规性. 对任意 $g\in G$ 与 $hk\in HK$, 有

$$
g\left(hk\right)g^{-1}=\left(ghg^{-1}\right)\left(gkg^{-1}\right).
$$

因 $H\triangleleft G$, 由**定义 1.3.1 (正规子群)**, $ghg^{-1}\in H$; 因 $K\triangleleft G$, 同理 $gkg^{-1}\in K$. 故 $g\left(hk\right)g^{-1}\in HK$. 由 $g$ 与 $hk$ 的任意性, 对任意 $g\in G$ 有 $g\left(HK\right)g^{-1}\subseteq HK$, 依据**定义 1.3.1 (正规子群)**, $HK\triangleleft G$. $\blacksquare$

## 1.3-10

若群 $G$ 只有一个阶为 $m$ 的子群 $H$, 证明: $H\triangleleft G$.

### 解答 1.3-10

对任意 $g\in G$, 考虑集合 $gHg^{-1}=\left\{ghg^{-1}\mid h\in H\right\}$.

**第一步: 验证 $gHg^{-1}< G$.** 对任意 $x,y\in gHg^{-1}$, 存在 $h_1,h_2\in H$ 使 $x=gh_1g^{-1}$, $y=gh_2g^{-1}$, 则

$$
xy^{-1}=gh_1g^{-1}\left(gh_2g^{-1}\right)^{-1}=gh_1g^{-1}gh_2^{-1}g^{-1}=g\left(h_1h_2^{-1}\right)g^{-1}\in gHg^{-1}.
$$

由**定理 1.2.2 (子群判别法)** (条件 (3)), $gHg^{-1}< G$.

**第二步: 求 $\left|gHg^{-1}\right|$.** 由共轭映射保持阶, 映射 $h\mapsto ghg^{-1}$ 是 $H$ 到 $gHg^{-1}$ 的双射, 故 $\left|gHg^{-1}\right|=\left|H\right|=m$.

**第三步: 由唯一性得 $gHg^{-1}=H$.** 因 $G$ 只有一个阶为 $m$ 的子群 $H$, 而 $gHg^{-1}$ 也是 $G$ 的阶为 $m$ 的子群, 故 $gHg^{-1}=H$.

**第四步: 证明 $H\triangleleft G$.** 对任意 $g\in G$, $h\in H$, 因 $gHg^{-1}=H$, 故 $ghg^{-1}\in H$. 依据**定义 1.3.1 (正规子群)**, $H\triangleleft G$. $\blacksquare$

## 1.4-3

设 $G$ 是一个群, 定义 $R:G\to S_{G}$ 为 $R\left(a\right)=R_{a}$, 其中 $R_{a}$ 为右平移变换. 证明: $R$ 是 $G$ 的反同构, 即满足 $R\left(ab\right)=R\left(b\right)R\left(a\right)$.

### 解答 1.4-3

对任意 $g\in G$, 由**定义 1.4.9 (左平移与右平移)**, $R_a\left(g\right)=ga$.

**第一步: 证明 $R$ 是反同态.** 对任意 $g\in G$,

$$
R\left(ab\right)\left(g\right)=R_{ab}\left(g\right)=g\left(ab\right)=\left(ga\right)b=R_b\left(ga\right)=R_b\left(R_a\left(g\right)\right)=\left(R_b\circ R_a\right)\left(g\right)=R\left(b\right)R\left(a\right)\left(g\right).
$$

由 $g$ 的任意性, $R\left(ab\right)=R\left(b\right)R\left(a\right)$, 依据反同态与反同构, $R$ 是 $G$ 到 $S_G$ 的反同态.

**第二步: 证明 $R$ 是单射.** 若 $R\left(a\right)=R\left(b\right)$, 则 $R_a=R_b$. 特别地, $R_a\left(e\right)=R_b\left(e\right)$, 即 $ea=eb$, 故 $a=b$. 因此 $R$ 是单射.

**第三步: 证明 $R$ 的像集是 $S_G$ 的子群.** 记 $R_G=\left\{R_a\mid a\in G\right\}$. 由定义, $R:G\to R_G$ 是满射. 又由对称群与双射变换, $R_a$ 是 $G$ 上的双射 (逆为 $R_{a^{-1}}$), 故 $R_G\subseteq S_G$, 且 $R_G$ 是 $S_G$ 的子群 (复合与逆均封闭于 $R_G$, 因 $R_aR_b=R_{ba}$, $R_a^{-1}=R_{a^{-1}}$).

综上, $R:G\to R_G$ 是双射反同态, 依据反同态与反同构, $R$ 是反同构, 即 $G$ 与 $S_G$ 的子群 $R_G$ 反同构. $\blacksquare$

## 1.4-7

证明 $f\left(x\right)=\cos x+\sqrt{-1}\sin x$ 是 $\left(\mathbb R,+\right)$ 到 $\left(\mathbb C^{*},\cdot\right)$ 的一个群同态, 并求 $\ker f$.

### 解答 1.4-7

**第一步: 证明 $f$ 是群同态.** 对任意 $x,y\in\mathbb R$, 由三角函数的和角公式,

$$
f\left(x+y\right)=\cos\left(x+y\right)+\sqrt{-1}\sin\left(x+y\right)=\left(\cos x\cos y-\sin x\sin y\right)+\sqrt{-1}\left(\sin x\cos y+\cos x\sin y\right)=\left(\cos x+\sqrt{-1}\sin x\right)\left(\cos y+\sqrt{-1}\sin y\right)=f\left(x\right)f\left(y\right).
$$

又 $f\left(x\right)\ne0$ 对任意 $x\in\mathbb R$ (因 $\cos^2x+\sin^2x=1$) (复指数与单位圆), 故 $f:\mathbb R\to\mathbb C^{*}$ 良定义. 由**定义 1.4.1 (群同态与同构)**, $f$ 是 $\left(\mathbb R,+\right)$ 到 $\left(\mathbb C^{*},\cdot\right)$ 的群同态.

**第二步: 求 $\ker f$.** 由**定义 1.4.11 (同态的核与像)**, $\ker f=\left\{x\in\mathbb R\mid f\left(x\right)=1\right\}$. 由复指数与单位圆, $f\left(x\right)=\cos x+\sqrt{-1}\sin x=1$ 当且仅当 $x=2k\pi$, $k\in\mathbb Z$. 故

$$
\ker f=2\pi\mathbb Z=\left\{2k\pi\mid k\in\mathbb Z\right\}.
$$

由**定理 1.4.19 (群的同态基本定理)**, $\mathbb R/2\pi\mathbb Z\cong\mathrm{Im}\left(f\right)$, 其中 $\mathrm{Im}\left(f\right)=\left\{f\left(x\right)\mid x\in\mathbb R\right\}$ 为单位圆 $\left\{z\in\mathbb C\mid\left|z\right|=1\right\}$ 上的复数乘法群 (复指数与单位圆). $\blacksquare$

## 1.4-8

设 $G$ 和 $H$ 为群, $\varphi:G\to\mathrm{Aut}\left(H\right)$ 为群同态. 在集合 $\left\{\left(g,h\right)\mid g\in G,h\in H\right\}$ 中定义乘法为

$$
\left(g_{1},h_{1}\right)\left(g_{2},h_{2}\right)=\left(g_{1}g_{2},\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right),
$$

证明: 该集合是群, 称为 $G$ 与 $H$ 的半直积, 记为 $G\ltimes H$. 进一步, $G_{1}=\left\{\left(g,e_{H}\right)\mid g\in G\right\}$ 为 $G\ltimes H$ 的子群, $H_{1}=\left\{\left(e_{G},h\right)\mid h\in H\right\}$ 为 $G\ltimes H$ 的正规子群.

### 解答 1.4-8

记 $G\ltimes H=\left\{\left(g,h\right)\mid g\in G,h\in H\right\}$, 乘法如题所定义. 逐条验证群公理.

**封闭性**: 对任意 $\left(g_1,h_1\right),\left(g_2,h_2\right)\in G\ltimes H$, 因 $g_1g_2\in G$, 且 $\varphi\left(g_2^{-1}\right)\left(h_1\right)\in H$ (因 $\varphi\left(g_2^{-1}\right)\in\mathrm{Aut}\left(H\right)$), $h_2\in H$, 故 $\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\in H$ (自同构群同态的性质). 于是 $\left(g_1g_2,\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)\in G\ltimes H$, 封闭性成立.

**结合律**: 对任意 $\left(g_1,h_1\right),\left(g_2,h_2\right),\left(g_3,h_3\right)\in G\ltimes H$, 一方面

$$
\left(\left(g_1,h_1\right)\left(g_2,h_2\right)\right)\left(g_3,h_3\right)=\left(g_1g_2,\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)\left(g_3,h_3\right)=\left(\left(g_1g_2\right)g_3,\ \varphi\left(g_3^{-1}\right)\left(\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)h_3\right).
$$

因 $\varphi\left(g_3^{-1}\right)\in\mathrm{Aut}\left(H\right)$ 保持 $H$ 的乘法, 故 $\varphi\left(g_3^{-1}\right)\left(\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)=\varphi\left(g_3^{-1}\right)\varphi\left(g_2^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)$; 又由自同构群同态的性质, $\varphi\left(g_3^{-1}\right)\varphi\left(g_2^{-1}\right)=\varphi\left(g_3^{-1}g_2^{-1}\right)=\varphi\left(\left(g_2g_3\right)^{-1}\right)$. 故

$$
\left(\left(g_1,h_1\right)\left(g_2,h_2\right)\right)\left(g_3,h_3\right)=\left(\left(g_1g_2\right)g_3,\ \varphi\left(\left(g_2g_3\right)^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)\cdot h_3\right).
$$

另一方面,

$$
\left(g_1,h_1\right)\left(\left(g_2,h_2\right)\left(g_3,h_3\right)\right)=\left(g_1,h_1\right)\left(g_2g_3,\varphi\left(g_3^{-1}\right)\left(h_2\right)h_3\right)=\left(g_1\left(g_2g_3\right),\ \varphi\left(\left(g_2g_3\right)^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)\cdot h_3\right).
$$

因 $G$ 满足结合律, $\left(g_1g_2\right)g_3=g_1\left(g_2g_3\right)$; 两式右端第二分量相同, 故结合律成立.

**单位元**: 考虑 $\left(e_G,e_H\right)$. 对任意 $\left(g,h\right)\in G\ltimes H$, 因 $\varphi\left(e_G\right)=\mathrm{id}_H$ (自同构群同态的性质), 故 $\varphi\left(e_G^{-1}\right)\left(h\right)=\mathrm{id}_H\left(h\right)=h$, 于是

$$
\left(g,h\right)\left(e_G,e_H\right)=\left(g,\varphi\left(e_G^{-1}\right)\left(h\right)e_H\right)=\left(g,h\right),
$$

且

$$
\left(e_G,e_H\right)\left(g,h\right)=\left(g,\varphi\left(g^{-1}\right)\left(e_H\right)h\right)=\left(g,\mathrm{id}_H\left(e_H\right)h\right)=\left(g,h\right).
$$

故 $\left(e_G,e_H\right)$ 是单位元.

**逆元**: 对 $\left(g,h\right)\in G\ltimes H$, 考虑 $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$. 因 $\varphi\left(\left(g^{-1}\right)^{-1}\right)=\varphi\left(g\right)$, 且 $\varphi\left(g^{-1}\right)\varphi\left(g\right)=\mathrm{id}_H$, $\varphi\left(g\right)\varphi\left(g^{-1}\right)=\mathrm{id}_H$ (自同构群同态的性质), 故

$$
\left(g,h\right)\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_G,\ \varphi\left(g\right)\left(h\right)\cdot\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_G,\varphi\left(g\right)\left(hh^{-1}\right)\right)=\left(e_G,e_H\right),
$$

且

$$
\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)\left(g,h\right)=\left(e_G,\ \varphi\left(g^{-1}\right)\left(\varphi\left(g\right)\left(h^{-1}\right)\right)h\right)=\left(e_G,\left(\varphi\left(g^{-1}\right)\varphi\left(g\right)\right)\left(h^{-1}\right)\cdot h\right)=\left(e_G,h^{-1}h\right)=\left(e_G,e_H\right).
$$

故 $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$ 是 $\left(g,h\right)$ 的逆元.

由封闭性,结合律,单位元,逆元全部成立, 依据**定义 1.4.1 (群同态与同构)** (群的定义见其引用环境), $G\ltimes H$ 是群.

**验证 $G_1< G\ltimes H$.** $\left(e_G,e_H\right)\in G_1$, 故 $G_1$ 非空. 对 $\left(g_1,e_H\right),\left(g_2,e_H\right)\in G_1$, 由逆元公式, $\left(g_2,e_H\right)^{-1}=\left(g_2^{-1},\varphi\left(g_2\right)\left(e_H\right)\right)=\left(g_2^{-1},e_H\right)$, 于是

$$
\left(g_1,e_H\right)\left(g_2,e_H\right)^{-1}=\left(g_1,e_H\right)\left(g_2^{-1},e_H\right)=\left(g_1g_2^{-1},\varphi\left(\left(g_2^{-1}\right)^{-1}\right)\left(e_H\right)e_H\right)=\left(g_1g_2^{-1},\varphi\left(g_2\right)\left(e_H\right)\right)=\left(g_1g_2^{-1},e_H\right)\in G_1.
$$

由**定理 1.2.2 (子群判别法)**, $G_1< G\ltimes H$.

**验证 $H_1\triangleleft G\ltimes H$.** 先证 $H_1< G\ltimes H$: $\left(e_G,e_H\right)\in H_1$, 非空; 对 $\left(e_G,h_1\right),\left(e_G,h_2\right)\in H_1$, 由逆元公式, $\left(e_G,h_2\right)^{-1}=\left(e_G,\varphi\left(e_G\right)\left(h_2^{-1}\right)\right)=\left(e_G,h_2^{-1}\right)$, 于是

$$
\left(e_G,h_1\right)\left(e_G,h_2\right)^{-1}=\left(e_G,h_1\right)\left(e_G,h_2^{-1}\right)=\left(e_G,\varphi\left(e_G^{-1}\right)\left(h_1\right)h_2^{-1}\right)=\left(e_G,h_1h_2^{-1}\right)\in H_1.
$$

由**定理 1.2.2 (子群判别法)**, $H_1< G\ltimes H$. 再证正规性: 对任意 $\left(g,k\right)\in G\ltimes H$ 与 $\left(e_G,h\right)\in H_1$, 由逆元公式 $\left(g,k\right)^{-1}=\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)$, 且 $\varphi\left(e_G^{-1}\right)=\mathrm{id}_H$, $\varphi\left(g\right)\varphi\left(g^{-1}\right)=\mathrm{id}_H$, 计算

$$
\left(g,k\right)\left(e_G,h\right)\left(g,k\right)^{-1}=\left(g,\varphi\left(e_G^{-1}\right)\left(k\right)h\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(g,kh\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_G,\varphi\left(g^{-1}\right)\left(kh\right)\cdot\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_G,\varphi\left(g^{-1}\right)\varphi\left(g\right)\left(h\right)\right)=\left(e_G,h\right)\in H_1.
$$

故对任意 $\left(g,k\right)\in G\ltimes H$ 有 $\left(g,k\right)H_1\left(g,k\right)^{-1}\subseteq H_1$, 依据**定义 1.3.1 (正规子群)**, $H_1\triangleleft G\ltimes H$. $\blacksquare$
