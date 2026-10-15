# 作业 4

> **定义 1.4.1**（群同态与同构）设 $G$ 和 $G'$ 是两个群, 如果映射 $f:G\to G'$ 满足 $f\left(ab\right)=f\left(a\right)f\left(b\right)$, $\forall a,b\in G$, 则称 $f$ 是 $G$ 到 $G'$ 的群同态. 若同态 $f$ 是双射, 则称 $f$ 是 $G$ 到 $G'$ 的群同构, 此时称群 $G$ 与 $G'$ 是同构的, 记为 $G\cong G'$.

> **定义 1.4.9**（左平移与右平移）对任意 $a\in G$, 定义 $G$ 上的变换 $L_{a},R_{a}$ 为 $L_{a}\left(g\right)=ag$, $R_{a}\left(g\right)=ga$, $\forall g\in G$. 分别称为由 $a$ 决定的左平移变换和右平移变换.

> **定义 1.4.11**（同态的核与像）设 $f:G\to G'$ 是群同态, 分别称集合
> $$
> \ker f=\left\{a\in G\mid f\left(a\right)=e'\right\}
> $$
> 与 $\mathrm{Im}\left(f\right)=f\left(G\right)$ 为同态 $f$ 的核和像.

> **定理 1.4.19**（群的同态基本定理）设 $f:G\to G'$ 是群的满同态, 则 $G/\ker f\cong G'$.

> **基础知识**（反同态）若映射 $f:G\to G'$ 满足 $f\left(ab\right)=f\left(b\right)f\left(a\right)$, 则称 $f$ 为反同态. 若反同态为双射, 则称反同构.

### 习题一

（习题 1.4-3）设 $G$ 是一个群, 定义 $R:G\to S_{G}$ 为 $R\left(a\right)=R_{a}$, 其中 $R_{a}$ 为右平移变换. 证明: $R$ 是 $G$ 的反同构, 即满足 $R\left(ab\right)=R\left(b\right)R\left(a\right)$.

### 解答 习题一

对任意 $g\in G$, 由**定义 1.4.9**（左平移与右平移）, $R_{a}\left(g\right)=ga$.

首先证反同态性. 对任意 $g\in G$,

$$
\begin{aligned}R\left(ab\right)\left(g\right)&=R_{ab}\left(g\right)\\&=g\left(ab\right)\\&=\left(ga\right)b\\&=R_{b}\left(ga\right)\\&=R_{b}\left(R_{a}\left(g\right)\right)\\&=\left(R_{b}\circ R_{a}\right)\left(g\right)\\&=R\left(b\right)R\left(a\right)\left(g\right).\end{aligned}
$$

由 $g$ 的任意性, $R\left(ab\right)=R\left(b\right)R\left(a\right)$, 故 $R$ 是反同态.

再证 $R$ 是双射.

**单射** 若 $R\left(a\right)=R\left(b\right)$, 则 $R_{a}=R_{b}$. 特别地, $R_{a}\left(e\right)=R_{b}\left(e\right)$, 即 $ea=eb$, 故 $a=b$.

**满射** 记 $R_{G}=\left\{R_{a}\mid a\in G\right\}$. 由定义, $R:G\to R_{G}$ 是满射. 又 $R_{a}$ 是 $G$ 上的双射(其逆为 $R_{a^{-1}}$), 故 $R_{G}\subseteq S_{G}$.

因此 $R:G\to R_{G}$ 是反同构, 即 $G$ 与 $S_{G}$ 的子群 $R_{G}$ 反同构. $\blacksquare$

### 习题二

（习题 1.4-7）证明 $f\left(x\right)=\cos x+\sqrt{-1}\sin x$ 是 $\left(\mathbb R,+\right)$ 到 $\left(\mathbb C^{*},\cdot\right)$ 的一个群同态, 并求 $\ker f$.

### 解答 习题二

对任意 $x,y\in\mathbb R$, 由三角恒等式,

$$
\begin{aligned}f\left(x+y\right)&=\cos\left(x+y\right)+\sqrt{-1}\sin\left(x+y\right)\\&=\left(\cos x\cos y-\sin x\sin y\right)+\sqrt{-1}\left(\sin x\cos y+\cos x\sin y\right)\\&=\left(\cos x+\sqrt{-1}\sin x\right)\left(\cos y+\sqrt{-1}\sin y\right)\\&=f\left(x\right)f\left(y\right).\end{aligned}
$$

故 $f$ 是 $\left(\mathbb R,+\right)$ 到 $\left(\mathbb C^{*},\cdot\right)$ 的群同态.

求核: $f\left(x\right)=1$ 当且仅当 $\cos x=1$ 且 $\sin x=0$, 即 $x=2k\pi$, $k\in\mathbb Z$. 故

$$
\begin{aligned}\ker f&=2\pi\mathbb Z\\&=\left\{2k\pi\mid k\in\mathbb Z\right\}.\end{aligned}
$$

由**定理 1.4.19**（群的同态基本定理）, $\mathbb R/2\pi\mathbb Z\cong\mathrm{Im}f$, 其中 $\mathrm{Im}f$ 为单位圆上的复数乘法群. $\blacksquare$

### 习题三

（习题 1.4-8）设 $G$ 和 $H$ 为群, $\varphi:G\to\mathrm{Aut}\left(H\right)$ 为群同态. 在集合 $\left\{\left(g,h\right)\mid g\in G,h\in H\right\}$ 中定义乘法为

$$
\left(g_{1},h_{1}\right)\left(g_{2},h_{2}\right)=\left(g_{1}g_{2},\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right),
$$

证明: 该集合是群, 称为 $G$ 与 $H$ 的半直积, 记为 $G\ltimes H$. 进一步, $G_{1}=\left\{\left(g,e_{H}\right)\mid g\in G\right\}$ 为 $G\ltimes H$ 的子群, $H_{1}=\left\{\left(e_{G},h\right)\mid h\in H\right\}$ 为 $G\ltimes H$ 的正规子群.

### 解答 习题三

记

$$
G\ltimes H=\left\{\left(g,h\right)\mid g\in G,h\in H\right\},
$$

乘法如题所定义. 下面逐条验证群公理.

**封闭性** 由定义直接可见, 乘积仍属于 $G\ltimes H$.

**结合律** 对任意

$$
\left(g_{1},h_{1}\right),\left(g_{2},h_{2}\right),\left(g_{3},h_{3}\right)\in G\ltimes H,
$$

$$
\begin{aligned}\left(\left(g_{1},h_{1}\right)\left(g_{2},h_{2}\right)\right)\left(g_{3},h_{3}\right)&=\left(g_{1}g_{2},\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right)\left(g_{3},h_{3}\right)\\&=\left(\left(g_{1}g_{2}\right)g_{3},\varphi\left(g_{3}^{-1}\right)\left(\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)h_{2}\right)h_{3}\right)\\&=\left(g_{1}\left(g_{2}g_{3}\right),\varphi\left(g_{3}^{-1}\right)\varphi\left(g_{2}^{-1}\right)\left(h_{1}\right)\cdot\varphi\left(g_{3}^{-1}\right)\left(h_{2}\right)\cdot h_{3}\right)\\&=\left(g_{1}\left(g_{2}g_{3}\right),\varphi\left(\left(g_{2}g_{3}\right)^{-1}\right)\left(h_{1}\right)\cdot\varphi\left(g_{3}^{-1}\right)\left(h_{2}\right)\cdot h_{3}\right).\end{aligned}
$$

另一方面,

$$
\begin{aligned}\left(g_{1},h_{1}\right)\left(\left(g_{2},h_{2}\right)\left(g_{3},h_{3}\right)\right)&=\left(g_{1},h_{1}\right)\left(g_{2}g_{3},\varphi\left(g_{3}^{-1}\right)\left(h_{2}\right)h_{3}\right)\\&=\left(g_{1}\left(g_{2}g_{3}\right),\varphi\left(\left(g_{2}g_{3}\right)^{-1}\right)\left(h_{1}\right)\cdot\varphi\left(g_{3}^{-1}\right)\left(h_{2}\right)h_{3}\right).\end{aligned}
$$

二者相等, 故结合律成立.

**单位元** $\left(e_{G},e_{H}\right)$ 是单位元. 事实上,

$$
\begin{aligned}
\left(g,h\right)\left(e_{G},e_{H}\right)&=\left(g,\varphi\left(e^{-1}\right)\left(h\right)e_{H}\right)=\left(g,h\right),\
\left(e_{G},e_{H}\right)\left(g,h\right)&=\left(g,\varphi\left(g^{-1}\right)\left(e_{H}\right)h\right)=\left(g,h\right).
\end{aligned}
$$

**逆元** 对 $\left(g,h\right)$, 其逆元为 $\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)$. 验证:

$$
\begin{aligned}\left(g,h\right)\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)&=\left(gg^{-1},\varphi\left(\left(g^{-1}\right)^{-1}\right)\left(h\right)\cdot\varphi\left(g\right)\left(h^{-1}\right)\right)\\&=\left(e_{G},\varphi\left(g\right)\left(h\right)\varphi\left(g\right)\left(h^{-1}\right)\right)\\&=\left(e_{G},\varphi\left(g\right)\left(hh^{-1}\right)\right)\\&=\left(e_{G},e_{H}\right).\end{aligned}
$$

同理可验证

$$
\left(g^{-1},\varphi\left(g\right)\left(h^{-1}\right)\right)\left(g,h\right)=\left(e_{G},e_{H}\right).
$$

故 $G\ltimes H$ 是群.

下证 $G_{1}<G\ltimes H$. $\left(e_{G},e_{H}\right)\in G_{1}$. 对 $\left(g_{1},e_{H}\right),\left(g_{2},e_{H}\right)\in G_{1}$,

$$
\left(g_{1},e_{H}\right)\left(g_{2},e_{H}\right)^{-1}=\left(g_{1},e_{H}\right)\left(g_{2}^{-1},\varphi\left(g_{2}\right)\left(e_{H}\right)\right)=\left(g_{1}g_{2}^{-1},e_{H}\right)\in G_{1}.
$$

故 $G_{1}<G\ltimes H$.

最后证 $H_{1}\triangleleft G\ltimes H$. 先证 $H_{1}<G\ltimes H$: 对 $\left(e_{G},h_{1}\right),\left(e_{G},h_{2}\right)\in H_{1}$,

$$
\left(e_{G},h_{1}\right)\left(e_{G},h_{2}\right)^{-1}=\left(e_{G},h_{1}\right)\left(e_{G},h_{2}^{-1}\right)=\left(e_{G},h_{1}h_{2}^{-1}\right)\in H_{1}.
$$

再证正规性. 对任意 $\left(g,k\right)\in G\ltimes H$, $\left(e_{G},h\right)\in H_{1}$,

$$
\begin{aligned}\left(g,k\right)\left(e_{G},h\right)\left(g,k\right)^{-1}&=\left(g,k\right)\left(e_{G},h\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)\\&=\left(g,\varphi\left(e^{-1}\right)\left(k\right)h\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)\\&=\left(g,kh\right)\left(g^{-1},\varphi\left(g\right)\left(k^{-1}\right)\right)\\&=\left(e_{G},\varphi\left(g\right)\left(kh\right)\cdot\varphi\left(g\right)\left(k^{-1}\right)\right)\\&=\left(e_{G},\varphi\left(g\right)\left(h\right)\right)\in H_{1}.\end{aligned}
$$

故 $H_{1}\triangleleft G\ltimes H$. $\blacksquare$
