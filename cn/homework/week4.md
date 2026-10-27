# week4

> **基础知识: 反同态与反同构**<br>若映射 $f:G\to G'$ 满足 $f\left(ab\right)=f\left(b\right)f\left(a\right)$, $\forall a,b\in G$, 则称 $f$ 为反同态; 若反同态是双射, 则称 $f$ 为反同构.

> **基础知识: 对称群与双射变换**<br>非空集合 $X$ 上所有双射 (置换) 的全体 $S_X$ 在变换的复合下构成群, 称为 $X$ 的对称群; $G$ 上的左平移 $L_a$ 与右平移 $R_a$ 都是 $G$ 上的双射, 因 $L_{a^{-1}}$, $R_{a^{-1}}$ 分别是它们的逆.

> **基础知识: 三角函数的和角公式**<br>对任意 $x,y\in\mathbb R$, $\cos\left(x+y\right)=\cos x\cos y-\sin x\sin y$, $\sin\left(x+y\right)=\sin x\cos y+\cos x\sin y$.

> **基础知识: 复指数与单位圆**<br>对任意 $x\in\mathbb R$, $\cos x+\sqrt{-1}\sin x\in\mathbb C^{*}$, 且 $\cos x+\sqrt{-1}\sin x=1$ 当且仅当 $x=2k\pi$ ($k\in\mathbb Z$).

> **基础知识: 自同构群同态的性质**<br>设 $\varphi:G\to\mathrm{Aut}\left(H\right)$ 是群同态, 则对任意 $a,b\in G$ 有 $\varphi\left(ab\right)=\varphi\left(a\right)\varphi\left(b\right)$, $\varphi\left(a^{-1}\right)=\varphi\left(a\right)^{-1}$, $\varphi\left(e_G\right)=\mathrm{id}_H$; 特别地 $\varphi\left(a^{-1}\right)\varphi\left(a\right)=\mathrm{id}_H$.

> **定理 1.2.2 (子群判别法)**<br>设 $H$ 是群 $G$ 的非空子集, 则下列条件等价: (1) $H$ 是 $G$ 的子群; (2) 对任意 $a,b\in H$, 有 $ab\in H$, $a^{-1}\in H$; (3) 对任意 $a,b\in H$, 有 $ab^{-1}\in H$.

> **定义 1.3.1 (正规子群)**<br>设 $H$ 是群 $G$ 的子群. 如果对任意 $g\in G$, $h\in H$, 有 $ghg^{-1}\in H$, 则称 $H$ 为 $G$ 的一个正规子群, 记为 $H\triangleleft G$.

> **定义 1.4.1 (群同态与同构)**<br>设 $G$ 和 $G'$ 是两个群, 如果映射 $f:G\to G'$ 满足 $f\left(ab\right)=f\left(a\right)f\left(b\right)$, $\forall a,b\in G$, 则称 $f$ 是 $G$ 到 $G'$ 的群同态. 若同态 $f$ 是双射, 则称 $f$ 是 $G$ 到 $G'$ 的群同构, 此时称群 $G$ 与 $G'$ 是同构的, 记为 $G\cong G'$.

> **定义 1.4.9 (左平移与右平移)**<br>对任意 $a\in G$, 定义 $G$ 上的变换 $L_a,R_a$ 为 $L_a\left(g\right)=ag$, $R_a\left(g\right)=ga$, $\forall g\in G$; 分别称 $L_a,R_a$ 为由 $a$ 决定的左平移变换和右平移变换.

> **定义 1.4.11 (同态的核与像)**<br>设 $f:G\to G'$ 是群同态, 则集合 $\ker f=\left\{a\in G\mid f\left(a\right)=e'\right\}$ 称为同态 $f$ 的核, 集合 $\mathrm{Im}\left(f\right)=f\left(G\right)=\left\{f\left(a\right)\mid a\in G\right\}$ 称为同态 $f$ 的像.

> **定理 1.4.19 (群的同态基本定理)**<br>设 $f:G\to G'$ 是群的满同态, 则 $G/\ker f\cong G'$.

---

## 1.4-3

设 $G$ 是一个群, 定义 $R:G\to S_{G}$ 为 $R\left(a\right)=R_{a}$, 其中 $R_{a}$ 为右平移变换. 证明: $R$ 是 $G$ 的反同构, 即满足 $R\left(ab\right)=R\left(b\right)R\left(a\right)$.

### 解答 1.4-3

对任意 $g\in G$, 由**定义 1.4.9 (左平移与右平移)**, $R_a\left(g\right)=ga$.

**第一步: 证明 $R$ 是反同态.** 对任意 $g\in G$,

$$
R\left(ab\right)\left(g\right)=R_{ab}\left(g\right)=g\left(ab\right)=\left(ga\right)b=R_b\left(ga\right)=R_b\left(R_a\left(g\right)\right)=\left(R_b\circ R_a\right)\left(g\right)=R\left(b\right)R\left(a\right)\left(g\right).
$$

由 $g$ 的任意性, $R\left(ab\right)=R\left(b\right)R\left(a\right)$, 依据**基础知识: 反同态与反同构**, $R$ 是 $G$ 到 $S_G$ 的反同态.

**第二步: 证明 $R$ 是单射.** 若 $R\left(a\right)=R\left(b\right)$, 则 $R_a=R_b$. 特别地, $R_a\left(e\right)=R_b\left(e\right)$, 即 $ea=eb$, 故 $a=b$. 因此 $R$ 是单射.

**第三步: 证明 $R$ 的像集是 $S_G$ 的子群.** 记 $R_G=\left\{R_a\mid a\in G\right\}$. 由定义, $R:G\to R_G$ 是满射. 又由**基础知识: 对称群与双射变换**, $R_a$ 是 $G$ 上的双射 (逆为 $R_{a^{-1}}$), 故 $R_G\subseteq S_G$, 且 $R_G$ 是 $S_G$ 的子群 (复合与逆均封闭于 $R_G$, 因 $R_aR_b=R_{ba}$, $R_a^{-1}=R_{a^{-1}}$).

综上, $R:G\to R_G$ 是双射反同态, 依据**基础知识: 反同态与反同构**, $R$ 是反同构, 即 $G$ 与 $S_G$ 的子群 $R_G$ 反同构. $\blacksquare$

---

## 1.4-7

证明 $f\left(x\right)=\cos x+\sqrt{-1}\sin x$ 是 $\left(\mathbb R,+\right)$ 到 $\left(\mathbb C^{*},\cdot\right)$ 的一个群同态, 并求 $\ker f$.

### 解答 1.4-7

**第一步: 证明 $f$ 是群同态.** 对任意 $x,y\in\mathbb R$, 由**基础知识: 三角函数的和角公式**,

$$
f\left(x+y\right)=\cos\left(x+y\right)+\sqrt{-1}\sin\left(x+y\right)=\left(\cos x\cos y-\sin x\sin y\right)+\sqrt{-1}\left(\sin x\cos y+\cos x\sin y\right)=\left(\cos x+\sqrt{-1}\sin x\right)\left(\cos y+\sqrt{-1}\sin y\right)=f\left(x\right)f\left(y\right).
$$

又 $f\left(x\right)\ne0$ 对任意 $x\in\mathbb R$ (因 $\cos^2x+\sin^2x=1$) (**基础知识: 复指数与单位圆**), 故 $f:\mathbb R\to\mathbb C^{*}$ 良定义. 由**定义 1.4.1 (群同态与同构)**, $f$ 是 $\left(\mathbb R,+\right)$ 到 $\left(\mathbb C^{*},\cdot\right)$ 的群同态.

**第二步: 求 $\ker f$.** 由**定义 1.4.11 (同态的核与像)**, $\ker f=\left\{x\in\mathbb R\mid f\left(x\right)=1\right\}$. 由**基础知识: 复指数与单位圆**, $f\left(x\right)=\cos x+\sqrt{-1}\sin x=1$ 当且仅当 $x=2k\pi$, $k\in\mathbb Z$. 故

$$
\ker f=2\pi\mathbb Z=\left\{2k\pi\mid k\in\mathbb Z\right\}.
$$

由**定理 1.4.19 (群的同态基本定理)**, $\mathbb R/2\pi\mathbb Z\cong\mathrm{Im}\left(f\right)$, 其中 $\mathrm{Im}\left(f\right)=\left\{f\left(x\right)\mid x\in\mathbb R\right\}$ 为单位圆 $\left\{z\in\mathbb C\mid\left|z\right|=1\right\}$ 上的复数乘法群 (**基础知识: 复指数与单位圆**). $\blacksquare$

---

## 1.4-8

设 $G$ 和 $H$ 为群, $\varphi:G\to\mathrm{Aut}\left(H\right)$ 为群同态. 在集合 $\left\{\left(g,h\right)\mid g\in G,h\in H\right\}$ 中定义乘法为

$$
\left(g_{1},h_{1}\right)\left(g_{2},h_{2}\right)=\left(g_{1}g_{2},\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right),
$$

证明: 该集合是群, 称为 $G$ 与 $H$ 的半直积, 记为 $G\ltimes H$. 进一步, $G_{1}=\left\{\left(g,e_{H}\right)\mid g\in G\right\}$ 为 $G\ltimes H$ 的子群, $H_{1}=\left\{\left(e_{G},h\right)\mid h\in H\right\}$ 为 $G\ltimes H$ 的正规子群.

### 解答 1.4-8

记 $G\ltimes H=\left\{\left(g,h\right)\mid g\in G,h\in H\right\}$, 乘法如题所定义. 逐条验证群公理.

**封闭性**: 对任意 $\left(g_1,h_1\right),\left(g_2,h_2\right)\in G\ltimes H$, 因 $g_1g_2\in G$, 且 $\varphi\left(g_2^{-1}\right)\left(h_1\right)\in H$ (因 $\varphi\left(g_2^{-1}\right)\in\mathrm{Aut}\left(H\right)$), $h_2\in H$, 故 $\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\in H$ (**基础知识: 自同构群同态的性质**). 于是 $\left(g_1g_2,\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)\in G\ltimes H$, 封闭性成立.

**结合律**: 对任意 $\left(g_1,h_1\right),\left(g_2,h_2\right),\left(g_3,h_3\right)\in G\ltimes H$, 一方面

$$
\left(\left(g_1,h_1\right)\left(g_2,h_2\right)\right)\left(g_3,h_3\right)=\left(g_1g_2,\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)\left(g_3,h_3\right)=\left(\left(g_1g_2\right)g_3,\ \varphi\left(g_3^{-1}\right)\left(\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)h_3\right).
$$

因 $\varphi\left(g_3^{-1}\right)\in\mathrm{Aut}\left(H\right)$ 保持 $H$ 的乘法, 故 $\varphi\left(g_3^{-1}\right)\left(\varphi\left(g_2^{-1}\right)\left(h_1\right)h_2\right)=\varphi\left(g_3^{-1}\right)\varphi\left(g_2^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)$; 又由**基础知识: 自同构群同态的性质**, $\varphi\left(g_3^{-1}\right)\varphi\left(g_2^{-1}\right)=\varphi\left(g_3^{-1}g_2^{-1}\right)=\varphi\left(\left(g_2g_3\right)^{-1}\right)$. 故

$$
\left(\left(g_1,h_1\right)\left(g_2,h_2\right)\right)\left(g_3,h_3\right)=\left(\left(g_1g_2\right)g_3,\ \varphi\left(\left(g_2g_3\right)^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)\cdot h_3\right).
$$

另一方面,

$$
\left(g_1,h_1\right)\left(\left(g_2,h_2\right)\left(g_3,h_3\right)\right)=\left(g_1,h_1\right)\left(g_2g_3,\varphi\left(g_3^{-1}\right)\left(h_2\right)h_3\right)=\left(g_1\left(g_2g_3\right),\ \varphi\left(\left(g_2g_3\right)^{-1}\right)\left(h_1\right)\cdot\varphi\left(g_3^{-1}\right)\left(h_2\right)\cdot h_3\right).
$$

因 $G$ 满足结合律, $\left(g_1g_2\right)g_3=g_1\left(g_2g_3\right)$; 两式右端第二分量相同, 故结合律成立.

**单位元**: 考虑 $\left(e_G,e_H\right)$. 对任意 $\left(g,h\right)\in G\ltimes H$, 因 $\varphi\left(e_G\right)=\mathrm{id}_H$ (**基础知识: 自同构群同态的性质**), 故 $\varphi\left(e_G^{-1}\right)\left(h\right)=\mathrm{id}_H\left(h\right)=h$, 于是

$$
\left(g,h\right)\left(e_G,e_H\right)=\left(g,\varphi\left(e_G^{-1}\right)\left(h\right)e_H\right)=\left(g,h\right),
$$

且

$$
\left(e_G,e_H\right)\left(g,h\right)=\left(g,\varphi\left(g^{-1}\right)\left(e_H\right)h\right)=\left(g,\mathrm{id}_H\left(e_H\right)h\right)=\left(g,h\right).
$$

故 $\left(e_G,e_H\right)$ 是单位元.

**逆元**: 对 $\left(g,h\right)\in G\ltimes H$, 考虑 $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$. 因 $\varphi\left(\left(g^{-1}\right)^{-1}\right)=\varphi\left(g\right)$, 且 $\varphi\left(g^{-1}\right)\varphi\left(g\right)=\mathrm{id}_H$, $\varphi\left(g\right)\varphi\left(g^{-1}\right)=\mathrm{id}_H$ (**基础知识: 自同构群同态的性质**), 故

$$
\left(g,h\right)\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_G,\ \varphi\left(g\right)\left(h\right)\cdot\varphi\left(g\right)\left(h^{-1}\right)\right)=\left(e_G,\varphi\left(g\right)\left(hh^{-1}\right)\right)=\left(e_G,e_H\right),
$$

且

$$
\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)\left(g,h\right)=\left(e_G,\ \varphi\left(g^{-1}\right)\left(\varphi\left(g\right)\left(h^{-1}\right)\right)h\right)=\left(e_G,\left(\varphi\left(g^{-1}\right)\varphi\left(g\right)\right)\left(h^{-1}\right)\cdot h\right)=\left(e_G,h^{-1}h\right)=\left(e_G,e_H\right).
$$

故 $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$ 是 $\left(g,h\right)$ 的逆元.

由封闭性,结合律,单位元,逆元全部成立, 依据**定义 1.4.1 (群同态与同构)** (群的定义见其引用环境), $G\ltimes H$ 是群.

**验证 $G_1<G\ltimes H$.** $\left(e_G,e_H\right)\in G_1$, 故 $G_1$ 非空. 对 $\left(g_1,e_H\right),\left(g_2,e_H\right)\in G_1$, 由逆元公式, $\left(g_2,e_H\right)^{-1}=\left(g_2^{-1},\varphi\left(g_2\right)\left(e_H\right)\right)=\left(g_2^{-1},e_H\right)$, 于是

$$
\left(g_1,e_H\right)\left(g_2,e_H\right)^{-1}=\left(g_1,e_H\right)\left(g_2^{-1},e_H\right)=\left(g_1g_2^{-1},\varphi\left(\left(g_2^{-1}\right)^{-1}\right)\left(e_H\right)e_H\right)=\left(g_1g_2^{-1},\varphi\left(g_2\right)\left(e_H\right)\right)=\left(g_1g_2^{-1},e_H\right)\in G_1.
$$

由**定理 1.2.2 (子群判别法)**, $G_1<G\ltimes H$.

**验证 $H_1\triangleleft G\ltimes H$.** 先证 $H_1<G\ltimes H$: $\left(e_G,e_H\right)\in H_1$, 非空; 对 $\left(e_G,h_1\right),\left(e_G,h_2\right)\in H_1$, 由逆元公式, $\left(e_G,h_2\right)^{-1}=\left(e_G,\varphi\left(e_G\right)\left(h_2^{-1}\right)\right)=\left(e_G,h_2^{-1}\right)$, 于是

$$
\left(e_G,h_1\right)\left(e_G,h_2\right)^{-1}=\left(e_G,h_1\right)\left(e_G,h_2^{-1}\right)=\left(e_G,\varphi\left(e_G^{-1}\right)\left(h_1\right)h_2^{-1}\right)=\left(e_G,h_1h_2^{-1}\right)\in H_1.
$$

由**定理 1.2.2 (子群判别法)**, $H_1<G\ltimes H$. 再证正规性: 对任意 $\left(g,k\right)\in G\ltimes H$ 与 $\left(e_G,h\right)\in H_1$, 由逆元公式 $\left(g,k\right)^{-1}=\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)$, 且 $\varphi\left(e_G^{-1}\right)=\mathrm{id}_H$, $\varphi\left(g\right)\varphi\left(g^{-1}\right)=\mathrm{id}_H$, 计算

$$
\left(g,k\right)\left(e_G,h\right)\left(g,k\right)^{-1}=\left(g,\varphi\left(e_G^{-1}\right)\left(k\right)h\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(g,kh\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_G,\varphi\left(g^{-1}\right)\left(kh\right)\cdot\varphi\left(g\right)\left(k^{-1}\right)\right)=\left(e_G,\varphi\left(g^{-1}\right)\varphi\left(g\right)\left(h\right)\right)=\left(e_G,h\right)\in H_1.
$$

故对任意 $\left(g,k\right)\in G\ltimes H$ 有 $\left(g,k\right)H_1\left(g,k\right)^{-1}\subseteq H_1$, 依据**定义 1.3.1 (正规子群)**, $H_1\triangleleft G\ltimes H$. $\blacksquare$
