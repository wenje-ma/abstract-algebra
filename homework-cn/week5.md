# week5

> **定理 1.2.22 (拉格朗日定理)**
> 
> 设 $G$ 是有限群, $H< G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, 其中 $\left[G:H\right]$ 为 $H$ 在 $G$ 中的指数. 从而子群 $H$ 的阶是群 $G$ 的阶的因子, 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

> **定理 1.4.10 (凯莱定理)**
> 
> 任何群 $G$ 与对称群 $S_G$ 的一个子群同构; 事实上映射 $L:G\to L_G$, $a\mapsto L_a$ 是单同态.

> **引理 1.4.13**
> 
> 设 $f:G\to G'$ 为群同态, 则 $\mathrm{Im}\,f< G'$, $\ker f\triangleleft G$.

> **例 1.4.17**
> 
> 设 $V$ 是数域 $P$ 上的 $n$ 维线性空间, 则映射 $\det\circ\pi:S_n\to P^{*}$, $\sigma\mapsto\det\left(\pi_\sigma\right)$ 是群同态, 其像集为 $\left\{1,-1\right\}$ (当 $n> 1$ 时), 该同态的核记为 $A_n$.

> **定理 1.4.19 (群的同态基本定理)**
> 
> 设 $f:G\to G'$ 是群的满同态, 则 $G/\ker f\cong G'$.

> **定理 1.4.23 (3) (第二同构定理)**
> 
> 设 $G$ 是群, $N\triangleleft G$, $H< G$, 则 $HN/N\cong H/\left(H\cap N\right)$.

> **定义 1.6.1 (轮换)**
> 
> 设 $\left\{i_1,i_2,\cdots,i_r\right\}\subseteq\left\{1,2,\cdots,n\right\}$. 若 $\sigma\in S_n$ 满足 $\sigma\left(i_1\right)=i_2$, $\sigma\left(i_2\right)=i_3$, ..., $\sigma\left(i_r\right)=i_1$, 且 $\sigma$ 固定其余文字, 则称 $\sigma$ 为一个 $r$-轮换, 记为 $\sigma=\left(i_1i_2\cdots i_r\right)$. 特别地, $2$-轮换称为对换.

> **定理 1.6.4 (轮换分解)**
> 
> $S_n$ 中的任何元素 $\sigma$ 都可表为 $S_n$ 中一些不相交轮换之积; 如果不计次序, 表法是唯一的.

> **引理 1.6.7 (轮换的对换分解)**
> 
> 任一个 $r$-轮换都可写成 $r-1$ 个对换的乘积: $\left(i_1i_2\cdots i_r\right)=\left(i_1i_r\right)\left(i_1i_{r-1}\right)\cdots\left(i_1i_3\right)\left(i_1i_2\right)$.

> **命题 1.6.8**
> 
> 任一 $n$ 元置换都可以表为一些对换的乘积.

> **定理 1.6.9 (交错群的单性)**
> 
> 当 $n\ge5$ 时, $A_n$ 是单群.

> **定义 1.7.9 (次正规序列与合成序列)**
> 
> 群 $G$ 中的子群序列 $G=G_1\trianglerighteq G_2\trianglerighteq\cdots\trianglerighteq G_t\trianglerighteq G_{t+1}=\left\{e\right\}$, 若满足 $G_{i+1}\trianglelefteq G_i$ ($i=1,\cdots,t$), 则称为次正规序列, 称 $G_i/G_{i+1}$ 为此序列的因子群. 若诸因子 $G_i/G_{i+1}$ 都是单群, 则称该次正规序列为 $G$ 的合成序列, 称 $G_i/G_{i+1}$ 为 $G$ 的合成因子.

> **定义 1.7.12 (同构序列)**
> 
> 群 $G$ 的两个次正规序列 $G=G_1\supset G_2\supset\cdots\supset G_t=\left\{e\right\}$ 与 $G=H_1\supset H_2\supset\cdots\supset H_s=\left\{e\right\}$ 称为同构的, 如果这两个序列的因子集之间有一一对应, 且对应的因子同构.

> **定理 1.7.13 (若尔当-赫尔德定理)**
> 
> 设群 $G$ 存在合成序列, 则 $G$ 的任意两个合成序列同构. 特别地, $G$ 的任意两个主序列也同构.

> **引理 1.8.3 (换位子性质)**
> 
> (1) $\left[g,h\right]^{-1}=\left[h,g\right]$, 且 $\left[g,h\right]=e$ 当且仅当 $gh=hg$. (2) 设 $\varphi:G\to H$ 为群同态, 则 $\varphi\left(\left[g,h\right]\right)=\left[\varphi\left(g\right),\varphi\left(h\right)\right]$; 特别地, 若 $\varphi\in\mathrm{Aut}\left(G\right)$, 则 $\varphi\left(\left[g,h\right]\right)=\left[\varphi\left(g\right),\varphi\left(h\right)\right]$.

> **引理 1.8.5**
> 
> 设 $N\triangleleft G$, 则 $G/N$ 是 阿贝尔群当且仅当 $\left[G,G\right]\subseteq N$. 特别地, $G/\left[G,G\right]$ 为 阿贝尔群.

> **定义 1.8.7 (可解群与幂零群)**
> 
> 在群 $G$ 中归纳定义导出列 $G^{\left(0\right)}=G$, $G^{\left(k+1\right)}=\left[G^{\left(k\right)},G^{\left(k\right)}\right]$. 若存在 $t$ 使得 $G^{\left(t\right)}=\left\{e\right\}$, 则称 $G$ 为可解群. 归纳定义降中心列 $G^{1}=G$, $G^{k+1}=\left[G,G^{k}\right]$, 若存在 $t$ 使得 $G^{t}=\left\{e\right\}$, 则称 $G$ 为幂零群.

> **引理 1.8.8 (可解群的遗传性)**
> 
> 可解群的子群,商群都是可解群; 反之, 设 $N\trianglelefteq G$, 且 $N$ 与 $G/N$ 都可解, 则 $G$ 可解.

> **定义 1.9.1 (群作用)**
> 
> 设 $G$ 是群, $X$ 是非空集合. 若映射 $f:G\times X\to X$ 满足 $f\left(e,x\right)=x$ 且 $f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right)$, 则称 $f$ 决定了 $G$ 在 $X$ 上的一个作用, 记 $f\left(g,x\right)=gx$.

> **定义 1.9.7 (可递作用与有效作用)**
> 
> 若对任意 $x,y\in X$ 存在 $g\in G$ 使 $gx=y$, 称 $G$ 在 $X$ 上的作用可递, 称 $X$ 为 $G$ 的齐性空间. 若由 $gx=x$ 对一切 $x\in X$ 成立可推出 $g=e$, 称作用有效. 若对任意 $g\in G$, $x\in X$ 都有 $gx=x$, 称作用平凡.

> **定义 1.9.9 (轨道与迷向子群)**
> 
> 设 $G$ 作用在 $X$ 上, $x\in X$. 称 $O_x=\left\{gx\mid g\in G\right\}$ 为 $x$ 的轨道. 称 $F_x=\left\{g\in G\mid gx=x\right\}$ 为 $x$ 的迷向子群.

> **推论 1.9.15 (轨道-迷向子群定理)**
> 
> 设群 $G$ 作用在 $X$ 上, $x\in X$, 则 $\left|O_x\right|=\left|G/F_x\right|=\left[G:F_x\right]$; 从而 $\left|O_x\right|\mid\left|G\right|$.

## 1.6-14

证明: 当 $n\ne2,6$ 时, $\mathrm{Aut}\left(S_n\right)\cong S_n$. 并求 $\mathrm{Aut}\left(S_2\right)$ 与 $\mathrm{Aut}\left(S_6\right)$.

### 解答 1.6-14

先证 $n\ne2,6$ 时 $\mathrm{Aut}\left(S_n\right)\cong S_n$. 由群的中心与内自同构, $\mathrm{Inn}\left(S_n\right)\cong S_n/C\left(S_n\right)$, 而当 $n\ge3$ 时 $C\left(S_n\right)=\left\{e\right\}$, 故 $\mathrm{Inn}\left(S_n\right)\cong S_n$. 于是只需证明 $\mathrm{Aut}\left(S_n\right)=\mathrm{Inn}\left(S_n\right)$, 即任一自同构都是内自同构.

设 $\varphi\in\mathrm{Aut}\left(S_n\right)$. 自同构保持元素的阶, 故二阶元 (对合) 映为对合. 由对换的中心化子与对换的识别, 当 $n\ne6$ 时, $S_n$ 中对换是唯一的这样的二阶元共轭类 (其中心化子大小为 $2\left(n-2\right)!$), 而自同构保持共轭类与中心化子大小, 故 $\varphi$ 必将对换映为对换.

设 $\varphi\left(12\right)=\left(ab\right)$. 用内自同构 $\mathrm{Ad}_{\sigma}$ 复合 $\varphi$, 其中 $\sigma\in S_n$ 满足 $\sigma\left(a\right)=1$, $\sigma\left(b\right)=2$, 则 $\mathrm{Ad}_{\sigma}\varphi\left(12\right)=\left(\sigma\left(a\right)\sigma\left(b\right)\right)=\left(12\right)$. 故可不妨设 $\varphi\left(12\right)=\left(12\right)$.

对 $k=3,\cdots,n$, 因 $\left(12\right)\left(1k\right)=\left(1k2\right)$ 是 3-轮换, 阶为 $3$, 故 $\varphi\left(1k\right)$ 是与 $\varphi\left(12\right)=\left(12\right)$ 的乘积为 3-轮换的对换, 因而 $\varphi\left(1k\right)$ 必与 $\left(12\right)$ 恰好共享一个文字, 即 $\varphi\left(1k\right)=\left(1,j_k\right)$ 或 $\left(2,j_k\right)$ ($j_k\ne1,2$). 若存在 $k$ 使 $\varphi\left(1k\right)=\left(2,j_k\right)$, 用保持 $\left(12\right)$ 不变的内自同构 $\mathrm{Ad}_{\left(12\right)}$ (即交换文字 $1,2$) 复合, 可统一把每个 $\varphi\left(1k\right)$ 写成 $\left(1,\sigma\left(k\right)\right)$ 的形式, 其中 $\sigma\in S_{n-1}$ 是 $\left\{3,\cdots,n\right\}$ 的一个排列 (保持 $1,2$ 不动). 于是 $\varphi$ 在生成元 $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ 上的作用等于内自同构 $\mathrm{Ad}_{\sigma}$ 的作用.

由**习题 1.6-5 第一部分**, $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ 生成 $S_n$, 故 $\varphi$ 与 $\mathrm{Ad}_{\sigma}$ 在生成元上一致, 从而在 $S_n$ 上一致, 即 $\varphi=\mathrm{Ad}_{\sigma}\in\mathrm{Inn}\left(S_n\right)$.

上述证明在 $n=6$ 时失效, 因 $S_6$ 存在外自同构 (由对换的中心化子与对换的识别与$S_6$ 的外自同构). 故当 $n\ne2,6$ 时,

$$
\mathrm{Aut}\left(S_n\right)=\mathrm{Inn}\left(S_n\right)\cong S_n.
$$

求 $\mathrm{Aut}\left(S_2\right)$. $S_2=\left\{e,\left(12\right)\right\}$ 是二阶循环群, 自同构必须保持单位元 $e$, 故 $\mathrm{Aut}\left(S_2\right)=\left\{\mathrm{id}\right\}$ 是平凡群.

求 $\mathrm{Aut}\left(S_6\right)$. 由$S_6$ 的外自同构, $\mathrm{Out}\left(S_6\right)\cong\mathbb Z_2$ 且 $\left|\mathrm{Inn}\left(S_6\right)\right|=\left|S_6\right|=720$ (因 $C\left(S_6\right)=\left\{e\right\}$), 故 $\left|\mathrm{Aut}\left(S_6\right)\right|=\left|\mathrm{Out}\left(S_6\right)\right|\cdot\left|\mathrm{Inn}\left(S_6\right)\right|=2\cdot720=1440$. $\blacksquare$

## 1.7-11

设

$$
G=G_1\triangleright G_2\triangleright\cdots\triangleright G_t=\left\{e\right\}
$$

和

$$
G=H_1\triangleright H_2\triangleright\cdots\triangleright H_s=\left\{e\right\}
$$

是 $G$ 的两个合成序列, 且 $G_2\ne H_2$. 令 $K_3=G_2\cap H_2$. 任取 $K_3$ 的合成序列 $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$. 证明:

(1) $G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ 与 $G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ 也是 $G$ 的合成序列;

(2) 上述 $G$ 的四个合成序列彼此等价.

### 解答 1.7-11

第一步: 证明 $G_2H_2=G$. 因 $H_2\triangleleft G$, 由满同态保持正规子群, 自然同态 $\pi:G\to G/G_2$ 的像 $\pi\left(H_2\right)$ 是 $G/G_2$ 的正规子群. 又 $\pi\left(H_2\right)=\left\{hG_2\mid h\in H_2\right\}=\left(G_2H_2\right)/G_2$ (因 $G_2\subseteq G_2H_2$), 故 $\left(G_2H_2\right)/G_2\triangleleft G/G_2$. 因 $G/G_2$ 是合成因子, 为单群, 故 $\left(G_2H_2\right)/G_2$ 只能是平凡群或 $G/G_2$, 即 $G_2H_2=G_2$ 或 $G$.

同理, 由 $G_2\triangleleft G$, 自然同态 $\pi':G\to G/H_2$ 的像 $\pi'\left(G_2\right)=\left(G_2H_2\right)/H_2\triangleleft G/H_2$; 因 $G/H_2$ 为单群, 故 $G_2H_2=H_2$ 或 $G$.

断言 $G_2H_2\ne G_2$. 若 $G_2H_2=G_2$, 则 $H_2\subseteq G_2$. 由上一段 $G_2H_2\in\left\{H_2,G\right\}$, 即 $G_2=H_2$ 或 $G_2=G$; 前者与 $G_2\ne H_2$ 矛盾, 后者与 $G_2$ 是 $G$ 的真子群 (因 $G/G_2$ 是非平凡单群) 矛盾. 故 $G_2H_2\ne G_2$.

断言 $G_2H_2\ne H_2$. 若 $G_2H_2=H_2$, 则 $G_2\subseteq H_2$. 由 $G_2H_2\in\left\{G_2,G\right\}$, 即 $H_2=G_2$ 或 $H_2=G$; 前者与 $G_2\ne H_2$ 矛盾, 后者与 $H_2$ 为真子群矛盾. 故 $G_2H_2\ne H_2$.

因此只能有 $G_2H_2=G$.

第 (1) 步: 证明两个细化序列是合成序列. 由**定理 1.4.23 (3) (第二同构定理)**, 取 $H=G_2$, $N=H_2$, 得

$$
G_2/K_3=G_2/\left(G_2\cap H_2\right)\cong G_2H_2/H_2=G/H_2,
$$

而 $G/H_2$ 是合成因子, 为单群, 故 $G_2/K_3$ 是单群.

同理, 由**定理 1.4.23 (3) (第二同构定理)**, 取 $H=H_2$, $N=G_2$, 得

$$
H_2/K_3=H_2/\left(G_2\cap H_2\right)\cong G_2H_2/G_2=G/G_2,
$$

亦为单群.

又 $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ 是 $K_3$ 的合成序列, 故 $K_i/K_{i+1}$ ($i=3,\cdots,r-1$) 均为单群. 因此序列

$$
G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

的所有因子 $G/G_2$, $G_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ 均为单群; 且 $G_2\triangleright K_3$ 是合法的次正规步 ($K_3=G_2\cap H_2$, $H_2\triangleleft G$, 故 $K_3\triangleleft G_2$). 由**定义 1.7.9 (次正规序列与合成序列)**, 它是 $G$ 的合成序列.

同理, 序列

$$
G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

的因子 $G/H_2$, $H_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ 均为单群, 故由**定义 1.7.9 (次正规序列与合成序列)** 也是 $G$ 的合成序列.

第 (2) 步: 证明四个合成序列彼此等价. 记四个合成序列为

$$
\begin{aligned}
S_1&:G\triangleright G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\},\\
S_2&:G\triangleright H_2\triangleright H_3\triangleright\cdots\triangleright H_s=\left\{e\right\},\\
S_3&:G\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\},\\
S_4&:G\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}.
\end{aligned}
$$

先证 $S_3$ 与 $S_4$ 同构. $S_3$ 的因子集为 $G/G_2$, $G_2/K_3\cong G/H_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$; $S_4$ 的因子集为 $G/H_2$, $H_2/K_3\cong G/G_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$. 两组因子作为多重集合仅前两项交换: $G/G_2$ 与 $G/H_2$ 互换位置, 其余因子完全相同. 故由**定义 1.7.12 (同构序列)**, $S_3$ 与 $S_4$ 同构.

再证 $S_1$ 与 $S_3$ 同构. $S_1$ 与 $S_3$ 的首因子均为 $G/G_2$. 去掉首项后, 二者的尾段

$$
G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\}
\quad\text{与}\quad
G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

都是 $G_2$ 的合成序列. 由**定理 1.7.13 (若尔当-赫尔德定理)**, 群 $G_2$ 的这两个合成序列同构. 补上二者共同的首因子 $G/G_2$ 后, 由**定义 1.7.12 (同构序列)**, $S_1$ 与 $S_3$ 同构.

同理证 $S_2$ 与 $S_4$ 同构. $S_2$ 与 $S_4$ 的首因子均为 $G/H_2$; 尾段 $H_2\triangleright H_3\triangleright\cdots\triangleright\left\{e\right\}$ 与 $H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright\left\{e\right\}$ 都是 $H_2$ 的合成序列, 由**定理 1.7.13 (若尔当-赫尔德定理)** 它们同构, 补上共同首因子 $G/H_2$ 后, $S_2$ 与 $S_4$ 同构.

综上, $S_1\cong S_3\cong S_4\cong S_2$, 即四个合成序列彼此等价. $\blacksquare$

## 1.8-12

设 $G$ 为 $n$ 阶可解群, $B$ 为可逆的复上三角矩阵的全体. 证明: $G$ 同构于 $B$ 的某个子群. 如果 $G$ 为 $n$ 阶幂零群, $N$ 为对角线元全为 $1$ 的复上三角矩阵的全体, $G$ 是否同构于 $N$ 的某个子群?

### 解答 1.8-12

先证第一部分. 由群到置换矩阵的忠实表示及**定理 1.4.10 (凯莱定理)**, $n$ 阶可解群 $G$ 同构于 $\mathrm{GL}\left(V\right)$ 的一个子群, 其中 $V=\mathbb C^{n}$; 由可解性在同构下保持, 可设 $G$ 本身是 $\mathrm{GL}\left(V\right)$ 的可解子群. 下面对 $\dim V$ 作归纳, 证明 $G$ 可同时上三角化, 即 $G$ 共轭于上三角矩阵群 $B$ 的子群.

归纳基础: 当 $\dim V=1$ 时, $\mathrm{GL}\left(V\right)\cong\mathbb C^{*}$ 本身就是上三角矩阵群, 结论显然成立.

归纳步: 设 $\dim V=n> 1$. 由**定义 1.8.7 (可解群与幂零群)**, $G$ 的换位子群 $G^{\prime}=\left[G,G\right]$ 是 $G$ 的真正规子群; 由**引理 1.8.5**, $G/G^{\prime}$ 为 阿贝尔群. 由**引理 1.8.8 (可解群的遗传性)**, $G^{\prime}$ 是可解群. 由归纳假设 (对 $G^{\prime}$ 在 $V$ 上反复运用基础情形的结果), $G^{\prime}$ 在 $V$ 上有公共特征向量; 设 $\lambda$ 是 $G^{\prime}$ 的一个特征标, 记其特征子空间为

$$
V_{\lambda}=\left\{v\in V\mid\sigma v=\lambda\left(\sigma\right)v,\ \forall\sigma\in G^{\prime}\right\}.
$$

因 $G^{\prime}\trianglelefteq G$, 对任意 $\tau\in G$, $\sigma\in G^{\prime}$ 及 $v\in V_{\lambda}$, 由**引理 1.8.3 (换位子性质)** (2) (取 $\varphi=\mathrm{Ad}_{\tau}$), $\tau\sigma\tau^{-1}\in G^{\prime}$, 且

$$
\sigma\left(\tau v\right)=\tau\left(\tau^{-1}\sigma\tau\right)v=\tau\lambda\left(\tau^{-1}\sigma\tau\right)v=\lambda\left(\tau^{-1}\sigma\tau\right)\tau v,
$$

故由特征标与公共特征子空间, $\tau v\in V_{\lambda^{\tau}}$, 其中 $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$. 由于 $G/G^{\prime}$ 是 阿贝尔群, $G$ 在 $G^{\prime}$ 的特征标集上的共轭作用轨道有限, 取其中一个轨道对应的特征子空间之和, 即得一个非零的 $G$-不变子空间 $W$.

在 $W$ 上, 因 $G/G^{\prime}$ 为 阿贝尔群而 $G^{\prime}$ 在 $W$ 上以标量作用, 故 $G$ 在 $W$ 上的像的换位子群为标量群, $G$ 的像在 $\mathrm{GL}\left(W\right)$ 中是 阿贝尔化的; 由交换线性变换族的公共特征向量, $W$ 中存在 $G$ 的公共特征向量, 即存在一维 $G$-不变子空间 $L\subseteq V$.

于是 $G$ 在商空间 $V/L$ 上诱导一个可解子群 (由可解性在同构下保持与商群的可解性, 或**引理 1.8.8 (可解群的遗传性)**), 由归纳假设, $G$ 在 $V/L$ 上可上三角化. 因而在 $V$ 中可取一组基, 使 $L$ 为第一个基向量张成的子空间, 而商空间的上三角化给出 $G$ 在 $V$ 上的上三角矩阵表示. 故 $G$ 共轭于 $B$ 的一个子群, 即 $G$ 同构于 $B$ 的某个子群. $\blacksquare$

再回答第二部分. 答案是否定的: 非平凡的有限幂零群 $G$ 不能同构于 $N$ 的子群.

事实上, 设 $A\in N$, 即 $A$ 是对角线元全为 $1$ 的复上三角矩阵, 则 $A=I+M$, 其中 $M$ 是严格上三角矩阵. 由幂零矩阵与有限阶元, $M$ 是幂零矩阵, 且若 $A$ 是有限阶元, 则 $M=0$, 即 $A=I$. 这说明 $N$ 中的有限阶元只有单位矩阵 $I$ 自身.

因此 $N$ 的有限子群只能是平凡群 $\left\{I\right\}$. 而 $G$ 是有限的非平凡幂零群, 由有限群元素皆有有限阶, $G$ 含有非单位的有限阶元, 故 $G$ 不能同构于 $N$ 的某个子群. $\blacksquare$

## 1.9-4

(1) 记 $\mathbb R^n$ 的所有 $1$ 维子空间的全体为 $P^{n-1}\left(\mathbb R\right)$, 称为实射影空间. 对任意 $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$, $W\in P^{n-1}\left(\mathbb R\right)$, $\rho\left(W\right)$ 也是一个 $1$ 维子空间. 试验证这是 $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上的可递作用, 并求迷向子群.

(2) 记 $\mathbb R^n$ 的所有 $k$ 维子空间的全体为 $\mathrm{Gr}\left(k,n\right)$, 称为格拉斯曼流形. 对任意 $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$, $W\in\mathrm{Gr}\left(k,n\right)$, $\rho\left(W\right)$ 也是一个 $k$ 维子空间. 试验证这是 $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上的可递作用, 并求迷向子群.

(3) 考虑 $\mathrm{SL}\left(n,\mathbb R\right)$, $O\left(n\right)$, $\mathrm{SO}\left(n\right)$ 在上述集合上的作用并判断其可递性.

### 解答 1.9-4

第 (1) 部分: $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上的作用. 由线性映射保持子空间维数, 对 $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ 与 $1$ 维子空间 $W=\mathbb Rv$, $\rho\left(W\right)$ 仍是 $1$ 维子空间. 对 $\rho,\tau\in\mathrm{GL}\left(n,\mathbb R\right)$ 及 $W=\mathbb Rv$,

$$
\rho\left(\tau\left(W\right)\right)=\rho\left(\tau\left(\mathbb Rv\right)\right)=\rho\left(\mathbb R\tau\left(v\right)\right)=\mathbb R\rho\left(\tau\left(v\right)\right)=\left(\rho\tau\right)\left(W\right),
$$

且单位矩阵 $I$ 满足 $I\left(W\right)=W$. 由**定义 1.9.1 (群作用)**, 这是 $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上的一个作用.

可递性: 任取两条直线 $W_1=\mathbb Rv$, $W_2=\mathbb Rw$ ($v,w\ne0$). 由线性映射保持子空间维数, 存在可逆矩阵 $\rho$ 使 $\rho v=w$, 故 $\rho\left(W_1\right)=W_2$. 由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

迷向子群: 取 $W_0=\mathbb Re_1$, 其中 $e_1=\left(1,0,\cdots,0\right)^{\top}$. 条件 $\rho\left(W_0\right)=W_0$ 等价于 $\rho e_1\in\mathbb Re_1$, 即 $\rho$ 的第一列为 $\left(a,0,\cdots,0\right)^{\top}$, $a\ne0$. 故由**定义 1.9.9 (轨道与迷向子群)**, $W_0$ 的迷向子群为

$$
F_{W_0}=\left\{\begin{bmatrix}a & *\\0 & A\end{bmatrix}\;\middle|\;a\in\mathbb R^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb R\right)\right\}.
$$

第 (2) 部分: $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上的作用. 同理 $\rho\left(\tau\left(W\right)\right)=\left(\rho\tau\right)\left(W\right)$ 且 $I\left(W\right)=W$, 由**定义 1.9.1 (群作用)** 这是作用.

可递性: 任取两个 $k$ 维子空间 $W_1,W_2$, 分别取基 $\left\{v_1,\cdots,v_k\right\}$ 与 $\left\{w_1,\cdots,w_k\right\}$, 扩充为 $\mathbb R^n$ 的基, 由线性映射保持子空间维数 定义可逆线性映射 $\rho$ 使 $\rho v_i=w_i$ ($i=1,\cdots,k$), 则 $\rho\left(W_1\right)=W_2$. 由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

迷向子群: 取 $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$. 条件 $\rho\left(W_0\right)=W_0$ 等价于 $\rho$ 把每个 $e_i$ ($i\le k$) 仍映回 $W_0$, 即 $\rho$ 的前 $k$ 列在第 $k+1,\cdots,n$ 行的分量为零, 亦即 $\rho$ 为分块上三角阵. 故由**定义 1.9.9 (轨道与迷向子群)**, 迷向子群为

$$
F_{W_0}=\left\{\begin{bmatrix}A & B\\0 & C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb R\right),\;C\in\mathrm{GL}\left(n-k,\mathbb R\right),\;B\in\mathbb R^{k\times\left(n-k\right)}\right\}.
$$

第 (3) 部分: 判断可递性. $\mathrm{SL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 与 $\mathrm{Gr}\left(k,n\right)$ 上的作用均可递: 在第 (1)(2) 部分构造的映射 $\rho$ 中, 若其行列式不为 $1$, 可在最后一行乘一个非零标量把行列式调整为 $1$, 而不改变对子空间的作用.

$O\left(n\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上可递: 由正交与酉变换, 任意两条单位直线可由正交变换互相映射. $O\left(n\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上亦可递: 两组 $k$ 维子空间的基可扩充为两组标准正交基, 由正交与酉变换 存在正交映射互相映射.

$\mathrm{SO}\left(n\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上, 当 $n\ge3$ 时可递 (可用适当旋转把任一方向映到任一方向而保持行列式为 $1$); 在 $\mathrm{Gr}\left(k,n\right)$ 上, 当 $n\ge3$ 时亦可递. $\blacksquare$
