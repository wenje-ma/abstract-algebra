# week6

> **引理 1.7.7**
> 
> 设 $A,B$ 是 $G$ 的子群, $G=AB$, $A\cap{B}=\left\{e\right\}$, 则 $A,B$ 都是 $G$ 的正规子群当且仅当对任意 $a\in{A}$, $b\in{B}$ 有 $ab=ba$.

> **引理 1.8.8 (可解群的遗传性)**
> 
> 可解群的子群,商群都是可解群; 反之, 设 $N\trianglelefteq{G}$, 且 $N$ 与 $G/N$ 都可解, 则 $G$ 可解.

> **定义 1.9.1 (群作用)**
> 
> 设 $G$ 是群, $X$ 是非空集合. 若映射 $f:G\times{X}\to{X}$ 满足 $f\left(e,x\right)=x$ 且 $f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right)$, 则称 $f$ 决定了 $G$ 在 $X$ 上的一个作用, 记 $f\left(g,x\right)=gx$.

> **定义 1.9.7 (可递作用与有效作用)**
> 
> 若对任意 $x,y\in{X}$ 存在 $g\in{G}$ 使 $gx=y$, 称 $G$ 在 $X$ 上的作用可递, 称 $X$ 为 $G$ 的齐性空间. 若由 $gx=x$ 对一切 $x\in{X}$ 成立可推出 $g=e$, 称作用有效. 若对任意 $g\in{G}$, $x\in{X}$ 都有 $gx=x$, 称作用平凡.

> **定义 1.9.9 (轨道与迷向子群)**
> 
> 设 $G$ 作用在 $X$ 上, $x\in{X}$. 称 $O_x=\left\{gx\mid{g}\in{G}\right\}$ 为 $x$ 的轨道. 称 $F_x=\left\{g\in{G}\mid{g}x=x\right\}$ 为 $x$ 的迷向子群.

> **推论 1.9.15 (轨道-迷向子群定理)**
> 
> 设群 $G$ 作用在 $X$ 上, $x\in{X}$, 则 $\left|O_x\right|=\left|G/F_x\right|=\left[G:F_x\right]$; 从而 $\left|O_x\right|\mid\left|G\right|$.

> **定理 1.10.8 (西罗第二定理)**
> 
> 设 $P$ 是 $G$ 的一个西罗 $p$-子群, $H$ 是 $G$ 的一个 $p^{k}$ 阶子群, $k\le{l}$ (其中 $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$), 则存在 $g\in{G}$ 使 $H\subseteq{g}Pg^{-1}$. 特别地, $G$ 的西罗 $p$-子群相互共轭.

> **定理 1.10.10 (西罗第三定理)**
> 
> 设 $G$ 的西罗 $p$-子群的个数为 $n_{p}$, 则 (1) $G$ 的西罗 $p$-子群 $P\triangleleft{G}$ 当且仅当 $n_{p}=1$; (2) $n_{p}\mid{m}$ 且 $n_{p}\equiv1\pmod{p}$, 其中 $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$.

## 1.9-5

记 $V_k\left(\mathbb{R}^n\right)$ 为 $\mathbb{R}^n$ 中所有 $k$ 元标准正交向量组的全体, 称为斯蒂弗尔流形. 对任意 $\rho\in{O}\left(n\right)$, $\left(\alpha_1,\cdots,\alpha_k\right)\in{V}_k\left(\mathbb{R}^n\right)$, 定义

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\left(\alpha_1\right),\cdots,\rho\left(\alpha_k\right)\right).
$$

试验证这是 $O\left(n\right)$ 在 $V_k\left(\mathbb{R}^n\right)$ 上的可递作用, 并求迷向子群.

### 解答 1.9-5

验证作用: 由正交与酉变换, 正交变换保持内积, 故若 $\left(\alpha_1,\cdots,\alpha_k\right)$ 是标准正交组, 则 $\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)$ 亦然, 即 $\rho\left(\alpha_1,\cdots,\alpha_k\right)\in{V}_k\left(\mathbb{R}^n\right)$. 又

$$
\rho\left(\tau\left(\alpha_1,\cdots,\alpha_k\right)\right)=\rho\left(\tau\alpha_1,\cdots,\tau\alpha_k\right)=\left(\rho\tau\alpha_1,\cdots,\rho\tau\alpha_k\right)=\left(\rho\tau\right)\left(\alpha_1,\cdots,\alpha_k\right),
$$

且单位矩阵作用不变. 由**定义 1.9.1 (群作用)**, 这是 $O\left(n\right)$ 在 $V_k\left(\mathbb{R}^n\right)$ 上的作用.

可递性: 任取两组标准正交向量组 $\left(\alpha_1,\cdots,\alpha_k\right)$ 与 $\left(\beta_1,\cdots,\beta_k\right)$, 由正交与酉变换 分别扩充为 $\mathbb{R}^n$ 的标准正交基 $\left(\alpha_1,\cdots,\alpha_k,\cdots,\alpha_n\right)$ 与 $\left(\beta_1,\cdots,\beta_k,\cdots,\beta_n\right)$. 定义线性映射 $\rho\alpha_i=\beta_i$ ($i=1,\cdots,n$), 则 $\rho\in{O}\left(n\right)$ 且

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\beta_1,\cdots,\beta_k\right).
$$

由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

迷向子群: 取基准向量组 $\left(e_1,\cdots,e_k\right)$. 条件 $\rho\left(e_i\right)=e_i$ ($i=1,\cdots,k$) 意味着 $\rho$ 在前 $k$ 个标准基向量上为恒等映射, 即 $\rho$ 为分块对角阵. 由**定义 1.9.9 (轨道与迷向子群)**, 迷向子群为

$$
F=\left\{\begin{bmatrix}I_k&0\\0&A\end{bmatrix}\;\middle|\;A\in{O}\left(n-k\right)\right\}.
$$

这就是 $\left(e_1,\cdots,e_k\right)$ 的迷向子群. $\blacksquare$

## 1.9-6

将 1.9-4, 1.9-5 两题中的作用推广到复空间情形.

### 解答 1.9-6

复射影空间与复格拉斯曼流形. 复射影空间 $P^{n-1}\left(\mathbb{C}\right)$ 为 $\mathbb{C}^n$ 的所有 $1$ 维复子空间的全体, 复格拉斯曼流形 $\mathrm{Gr}_{\mathbb{C}}\left(k,n\right)$ 为 $\mathbb{C}^n$ 的所有 $k$ 维复子空间的全体. $\mathrm{GL}\left(n,\mathbb{C}\right)$ 分别以 $\rho\left(W\right)=\rho{W}$ 作用于二者, 由线性映射保持子空间维数 与复情形的等价论证 (与实情形完全相同), 由**定义 1.9.1 (群作用)** 与**定义 1.9.7 (可递作用与有效作用)**, 这是两个可递作用.

由**定义 1.9.9 (轨道与迷向子群)**, 分别取 $W_0=\mathbb{C}e_1$ 与 $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$, 迷向子群分别为

$$
F_{W_0}=\left\{\begin{bmatrix}a&*\\0&A\end{bmatrix}\;\middle|\;a\in\mathbb{C}^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb{C}\right)\right\}
$$

与

$$
F_{W_0}=\left\{\begin{bmatrix}A&B\\0&C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb{C}\right),\;C\in\mathrm{GL}\left(n-k,\mathbb{C}\right),\;B\in\mathbb{C}^{k\times\left(n-k\right)}\right\}.
$$

复斯蒂弗尔流形. 记 $V_k\left(\mathbb{C}^n\right)$ 为 $\mathbb{C}^n$ 中所有 $k$ 元标准正交向量组 (关于标准埃尔米特内积) 的全体. $U\left(n\right)$ 以

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)
$$

作用于其上. 由正交与酉变换, 酉变换保持埃尔米特内积, 故定义合理, 由**定义 1.9.1 (群作用)** 这是作用. 作用可递: 由正交与酉变换, 两组标准正交向量组分别扩充为标准正交基, 对应的酉映射即为所求. 由**定义 1.9.9 (轨道与迷向子群)**, 取基准 $\left(e_1,\cdots,e_k\right)$, 迷向子群为

$$
F=\left\{\begin{bmatrix}I_k&0\\0&A\end{bmatrix}\;\middle|\;A\in{U}\left(n-k\right)\right\}.
$$

可递性判断. $\mathrm{SL}\left(n,\mathbb{C}\right)$ 在复射影空间与复格拉斯曼流形上可递 (仿实情形调整行列式); $U\left(n\right)$ 在复射影空间,复格拉斯曼流形与复斯蒂弗尔流形上均可递; $\mathrm{SU}\left(n\right)$ 在相应集合上, 当维数足够时亦可递. $\blacksquare$

## 1.9-8

设

$$
H=\left\{z=x+iy\in\mathbb{C}\mid{y}>0\right\},
$$

称为庞加莱上半平面. 对任意

$$
g=\begin{bmatrix}a&b\\c&d\end{bmatrix}\in\mathrm{SL}\left(2,\mathbb{R}\right),
$$

$z\in{H}$, 定义

$$
g\circ{z}=\frac{az+b}{cz+d}.
$$

试验证这定义了 $\mathrm{SL}\left(2,\mathbb{R}\right)$ 在 $H$ 上的一个作用 (称为默比乌斯变换或分式线性变换), 判断其可递性和有效性, 并求 $i$ 的迷向子群.

### 解答 1.9-8

第一步: 验证 $g\circ{z}\in{H}$. 对 $z=x+iy$ ($y>0$), 因 $\det{g}=ad-bc=1$, 直接计算虚部:

$$
\mathrm{Im}\left(\frac{az+b}{cz+d}\right)=\frac{\left(ad-bc\right)y}{\left|cz+d\right|^{2}}=\frac{y}{\left|cz+d\right|^{2}}>0,
$$

故 $g\circ{z}\in{H}$, 定义合理.

第二步: 验证作用公理. 单位矩阵 $I=\begin{bmatrix}1&0\\0&1\end{bmatrix}$ 给出 $I\circ{z}=z$. 又由分式线性变换, 分式线性变换的复合对应矩阵乘法, 即 $\left(g_1g_2\right)\circ{z}=g_1\circ\left(g_2\circ{z}\right)$. 由**定义 1.9.1 (群作用)**, 这是 $\mathrm{SL}\left(2,\mathbb{R}\right)$ 在 $H$ 上的作用.

第三步: 判断可递性. 任取 $z=x+iy\in{H}$ ($y>0$), 取

$$
g=\begin{bmatrix}\sqrt{y}&x/\sqrt{y}\\0&1/\sqrt{y}\end{bmatrix},
$$

其行列式为 $1$, 且

$$
g\circ{i}=\frac{\sqrt{y}\cdot{i}+x/\sqrt{y}}{0\cdot{i}+1/\sqrt{y}}=\left(\sqrt{y}\cdot{i}+\frac{x}{\sqrt{y}}\right)\sqrt{y}=yi+x=z.
$$

故 $i$ 可映到任意 $z\in{H}$, 由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

第四步: 判断有效性. 若 $g\circ{z}=z$ 对一切 $z\in{H}$ 成立, 则分式线性变换 $\frac{az+b}{cz+d}$ 有无穷多个不动点, 由分式线性变换, 它必为恒等变换, 故 $c=0$, $b=0$, $a=d$; 结合 $\det{g}=ad-bc=a^{2}=1$, 得 $g=\pm{I}$. 其中 $-I=\begin{bmatrix}-1&0\\0&-1\end{bmatrix}$ 对一切 $z$ 也有 $\left(-I\right)\circ{z}=\frac{-z}{-1}=z$. 故作用的核为 $\left\{\pm{I}\right\}$, 由**定义 1.9.7 (可递作用与有效作用)**, 作用不是有效的; 其有效商群为

$$
\mathrm{PSL}\left(2,\mathbb{R}\right)=\mathrm{SL}\left(2,\mathbb{R}\right)/\left\{\pm{I}\right\}.
$$

第五步: 求 $i$ 的迷向子群. 由 $g\circ{i}=i$, 即

$$
\frac{ai+b}{ci+d}=i,\quad\Longrightarrow\quad{a}i+b=i\left(ci+d\right)=ci^{2}+di=-c+di.
$$

比较实部与虚部得 $b=-c$, $a=d$. 又

$$
\det{g}=ad-bc=a^{2}-\left(-c\right)c=a^{2}+c^{2}=1.
$$

由**定义 1.9.9 (轨道与迷向子群)**, $i$ 的迷向子群为

$$
F_i=\left\{\begin{bmatrix}a&b\\-b&a\end{bmatrix}\;\middle|\;a^{2}+b^{2}=1\right\}\cong{S}O\left(2\right).
$$

$\blacksquare$

## 1.9-19

(费马两平方和定理) 设 $p=4k+1$ 为素数,

$$
X=\left\{\left(x,y,z\right)\in\mathbb{N}^{3}\mid{x}^{2}+4yz=p\right\}.
$$

设

$$
p_1:\left(x,y,z\right)\mapsto\left(x,z,y\right),
$$

$$
p_2:\left(x,y,z\right)\mapsto
\begin{cases}
\left(x+2z,z,y-x-z\right),&x<{}y-z,\\
\left(2y-x,y,x-y+z\right),&y-z\le{x}<2y,\\
\left(x-2y,x-y+z,y\right),&x\ge2y.
\end{cases}
$$

证明: 上述两个映射分别定义了 $\mathbb{Z}_2$ 在 $X$ 上的两个作用, 试求两个作用的不动点的个数, 从而证明当 $p=4k+1$ 时, $x^{2}+y^{2}=p$ 有正整数解.

### 解答 1.9-19

先验证 $p_1$ 定义了 $\mathbb{Z}_2$ 的作用. $p_1$ 交换 $y,z$, 显然 $p_1^{2}=\mathrm{id}$; 且

$$
x^{2}+4zy=x^{2}+4yz=p,
$$

故 $p_1\left(X\right)\subseteq{X}$. 由**定义 1.9.1 (群作用)**, $p_1$ 是 $X$ 上的二阶对合, 定义了 $\mathbb{Z}_2=\left\{1,p_1\right\}$ 在 $X$ 上的作用.

再验证 $p_2$. 直接代入可验证在三个分段中 $p_2$ 都保持方程 $x^{2}+4yz=p$ 不变, 且 $p_2^{2}=\mathrm{id}$ (三个分段互为逆映射, 边界处一致). 由**定义 1.9.1 (群作用)**, $p_2$ 也是 $X$ 上的对合, 定义了 $\mathbb{Z}_2$ 的另一个作用.

求 $p_2$ 的不动点. 对三种情况分别令 $p_2\left(x,y,z\right)=\left(x,y,z\right)$:

情况一 $x<{}y-z$: 由 $x+2z=x$ 得 $z=0$, 与 $z\in\mathbb{N}^{+}$ 矛盾, 故无不动点.

情况二 $y-z\le{x}<2y$: 由 $2y-x=x$ 得 $x=y$; 第三坐标 $x-y+z=z$ 自动成立. 代入方程:

$$
x^{2}+4yz=x^{2}+4xz=x\left(x+4z\right)=p.
$$

因 $p$ 为素数且 $x$, $x+4z$ 均为正整数, 故 $x=1$, $x+4z=p$, 即 $z=\left(p-1\right)/4=k$. 对应不动点为 $\left(1,1,k\right)$.

情况三 $x\ge2y$: 由 $x-2y=x$ 得 $y=0$, 矛盾.

故 $\left|\mathrm{Fix}\left(p_2\right)\right|=1$, 恰有一个不动点.

由群作用的轨道分解, $p_2$ 的非不动点轨道大小均为 $2$, 故

$$
\left|X\right|\equiv\left|\mathrm{Fix}\left(p_2\right)\right|\equiv1\pmod2,
$$

即 $\left|X\right|$ 为奇数.

同理, $p_1$ 的非不动点轨道大小也为 $2$, 故

$$
\left|\mathrm{Fix}\left(p_1\right)\right|\equiv\left|X\right|\equiv1\pmod2.
$$

因此 $\left|\mathrm{Fix}\left(p_1\right)\right|\ge1$, 即 $p_1$ 至少有一个不动点.

$p_1$ 的不动点满足 $y=z$. 代入方程得

$$
x^{2}+4y^{2}=p,
$$

即

$$
p=x^{2}+\left(2y\right)^{2}.
$$

令 $a=x$, $b=2y$, 则 $a^{2}+b^{2}=p$, 且 $a,b$ 均为正整数 (因 $p$ 为奇素数故 $x\ne0$; $y=z\ge1$ 故 $b=2y\ge2$).

因此当 $p=4k+1$ 时, $x^{2}+y^{2}=p$ 有正整数解. $\blacksquare$

## 1.9-20

(伯恩赛德引理) 设群 $G$ 作用在集合 $X$ 上, 令 $t$ 表示 $X$ 在 $G$ 作用下的轨道的个数. 对任意 $g\in{G}$, $F\left(g\right)$ 表示 $X$ 在 $g$ 作用下不动点的个数, 即

$$
F\left(g\right)=\left|\left\{x\in{X}\mid{g}x=x\right\}\right|.
$$

试证

$$
\sum_{g\in{G}}F\left(g\right)=t\left|G\right|.
$$

### 解答 1.9-20

考虑集合

$$
S=\left\{\left(g,x\right)\in{G}\times{X}\mid{g}x=x\right\}.
$$

按 $g$ 计数: 对固定的 $g\in{G}$, 满足 $gx=x$ 的 $x$ 恰有 $F\left(g\right)$ 个, 故

$$
\left|S\right|=\sum_{g\in{G}}F\left(g\right).
$$

按 $x$ 计数: 对固定的 $x\in{X}$, 满足 $gx=x$ 的 $g$ 恰为 $x$ 的迷向子群 $F_x=\left\{g\in{G}\mid{g}x=x\right\}$ 中的元素, 故

$$
\left|S\right|=\sum_{x\in{X}}\left|F_x\right|.
$$

由**推论 1.9.15 (轨道-迷向子群定理)**, 对 $x$ 所在的轨道 $O_x$, 有

$$
\left|O_x\right|=\left[G:F_x\right]=\left|G\right|/\left|F_x\right|,
$$

即 $\left|F_x\right|=\left|G\right|/\left|O_x\right|$.

将 $X$ 分解为互不相交的轨道之并. 设 $X$ 共有 $t$ 个轨道 $O_1,\cdots,O_t$. 对轨道 $O_i$ 中的任意 $x$, $\left|O_x\right|=\left|O_i\right|$, 故 $\left|F_x\right|=\left|G\right|/\left|O_i\right|$. 于是

$$
\sum_{x\in{X}}\left|F_x\right|=\sum_{i=1}^{t}\sum_{x\in{O}_i}\left|F_x\right|=\sum_{i=1}^{t}\left|O_i\right|\cdot\frac{\left|G\right|}{\left|O_i\right|}=\sum_{i=1}^{t}\left|G\right|=t\left|G\right|.
$$

综合两种计数方式, 得

$$
\sum_{g\in{G}}F\left(g\right)=t\left|G\right|.
$$

$\blacksquare$

## 1.10-10

设 $\left|G\right|=pq$, 其中 $p,q$ 为不同的素数, 证明: $G$ 为可解群.

### 解答 1.10-10

不妨设 $p<{}q$. 由**定理 1.10.10 (西罗第三定理)**, 西罗 $q$-子群的个数 $n_{q}$ 满足 $n_{q}\mid{p}$ 且 $n_{q}\equiv1\pmod{q}$. 因 $p<{}q$, $n_{q}$ 作为 $p$ 的正因子只能是 $1$ 或 $p$. 若 $n_{q}=p$, 则 $p\equiv1\pmod{q}$, 即 $q\mid{p}-1$; 但 $p<{}q$ 蕴含 $p-1<{}q$, 矛盾. 故 $n_{q}=1$.

于是 $G$ 的西罗 $q$-子群 $Q$ 唯一, 由**定理 1.10.10 (西罗第三定理)** (1), $Q\triangleleft{G}$. 又 $\left|Q\right|=q$ 为素数, 由素数阶群与循环群的可解性, $Q$ 是循环群, 从而是可解群. 商群 $G/Q$ 的阶为 $p$, 也是素数阶循环群, 由素数阶群与循环群的可解性 亦是可解群.

由**引理 1.8.8 (可解群的遗传性)**, $Q$ 与 $G/Q$ 均可解, 故 $G$ 可解. $\blacksquare$

## 1.10-12

(弗拉蒂尼) 设 $N\triangleleft{G}$, $P$ 为 $N$ 的西罗子群, 则 $G=N_{G}\left(P\right)N$.

### 解答 1.10-12

任取 $g\in{G}$. 因 $N\triangleleft{G}$, 共轭 $gPg^{-1}$ 仍为 $N$ 的子群; 又共轭保持阶, 由西罗子群与元素计数, $\left|gPg^{-1}\right|=\left|P\right|$, 故 $gPg^{-1}$ 也是 $N$ 的一个西罗 $p$-子群.

由**定理 1.10.8 (西罗第二定理)** (应用于子群 $N$), $N$ 的任意两个西罗 $p$-子群在 $N$ 中共轭, 故存在 $n\in{N}$ 使

$$
gPg^{-1}=nPn^{-1}.
$$

于是

$$
n^{-1}gPg^{-1}n=P,
$$

即 $n^{-1}g\in{N}_{G}\left(P\right)$ (它把 $P$ 共轭回 $P$). 记 $h=n^{-1}g\in{N}_{G}\left(P\right)$, 则 $g=nh$.

因此 $g\in{N}_{G}\left(P\right)N$. 由 $g\in{G}$ 的任意性, $G=N_{G}\left(P\right)N$. $\blacksquare$

## 1.10-15

设 $p,q$ 都是素数, $p<{}q$, $p\nmid\left(q-1\right)$, 证明 $pq$ 阶群一定是循环群.

### 解答 1.10-15

设 $\left|G\right|=pq$. 由**定理 1.10.10 (西罗第三定理)**, 西罗 $q$-子群的个数 $n_{q}$ 满足 $n_{q}\mid{p}$ 且 $n_{q}\equiv1\pmod{q}$. 因 $p<{}q$, 如 1.10-10 题所示, $n_{q}=1$. 故 $G$ 的西罗 $q$-子群 $Q$ 唯一, 由**定理 1.10.10 (西罗第三定理)** (1), $Q\triangleleft{G}$, $\left|Q\right|=q$.

再考虑西罗 $p$-子群的个数 $n_{p}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{p}\mid{q}$ 且 $n_{p}\equiv1\pmod{p}$. 因 $q$ 为素数, $n_{p}=1$ 或 $q$. 若 $n_{p}=q$, 则 $q\equiv1\pmod{p}$, 即 $p\mid\left(q-1\right)$, 与题设 $p\nmid\left(q-1\right)$ 矛盾. 故 $n_{p}=1$.

于是 $G$ 的西罗 $p$-子群 $P$ 也唯一, 由**定理 1.10.10 (西罗第三定理)** (1), $P\triangleleft{G}$, $\left|P\right|=p$.

因 $p,q$ 互素, $P\cap{Q}=\left\{e\right\}$. 又

$$
\left|PQ\right|=\left|P\right|\left|Q\right|/\left|P\cap{Q}\right|=pq=\left|G\right|,
$$

故 $G=PQ$.

由**引理 1.7.7**, $P,Q$ 都是 $G$ 的正规子群且 $P\cap{Q}=\left\{e\right\}$, 故对任意 $a\in{P}$, $b\in{Q}$ 有 $ab=ba$. 于是映射

$$
P\times{Q}\to{G},\quad\left(a,b\right)\mapsto{a}b
$$

保持乘法 (因 $ab=ba$) 且为双射 (单射由 $P\cap{Q}=\left\{e\right\}$, 满射由 $G=PQ$), 故它是群同构, 即 $G\cong{P}\times{Q}$.

又 $P\cong\mathbb{Z}_p$, $Q\cong\mathbb{Z}_q$, 而 $p,q$ 互素, 由直积中元素的阶, $\mathbb{Z}_p\times\mathbb{Z}_q\cong\mathbb{Z}_{pq}$, 故

$$
G\cong\mathbb{Z}_p\times\mathbb{Z}_q\cong\mathbb{Z}_{pq},
$$

即 $G$ 是 $pq$ 阶循环群. $\blacksquare$
