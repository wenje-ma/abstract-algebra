# 作业 9

> **定义 1.9.1**（群作用）设 $G$ 是群, $X$ 是非空集合. 若映射 $f:G\times X\to X$ 满足 $f\left(e,x\right)=x$ 且
> $$
> f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right),
> $$
> 则称 $f$ 决定了 $G$ 在 $X$ 上的一个作用, 记 $f\left(g,x\right)=gx$.

> **定义 1.9.7**（可递作用与有效作用）若对任意 $x,y\in X$ 存在 $g\in G$ 使 $gx=y$, 称作用可递, 称 $X$ 为 $G$ 的齐性空间. 若由 $gx=x$ 对一切 $x\in X$ 成立可推出 $g=e$, 称作用有效.

> **定义 1.9.9**（轨道与迷向子群）设 $G$ 作用在 $X$ 上, $x\in X$. 称 $Ox=\left\{gx\mid g\in G\right\}$ 为 $x$ 的轨道. 称 $F_x=\left\{g\in G\mid gx=x\right\}$ 为 $x$ 的迷向子群.

> **推论 1.9.15**（轨道-迷向子群定理）设群 $G$ 作用在 $X$ 上, $x\in X$, 则 $\left|Ox\right|=\left[G:F_x\right]$, 从而 $\left|Ox\right|$ 整除 $\left|G\right|$.

> **引理 1.9.11**（迷向子群的共轭）设 $y=gx\in Ox$, 则 $F_y=gF_xg^{-1}$.

### 习题一

（习题 1.9-4）(1)记 $\mathbb R^n$ 的所有 $1$ 维子空间的全体为 $P^{n-1}\left(\mathbb R\right)$, 称为实射影空间. 对任意 $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$, $W\in P^{n-1}\left(\mathbb R\right)$, $\rho\left(W\right)$ 也是一个 $1$ 维子空间. 试验证这是 $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上的可递作用, 并求迷向子群.

(2)记 $\mathbb R^n$ 的所有 $k$ 维子空间的全体为 $\mathrm{Gr}\left(k,n\right)$, 称为格拉斯曼流形. 对任意 $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$, $W\in\mathrm{Gr}\left(k,n\right)$, $\rho\left(W\right)$ 也是一个 $k$ 维子空间. 试验证这是 $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上的可递作用, 并求迷向子群.

(3)考虑 $\mathrm{SL}\left(n,\mathbb R\right)$, $O\left(n\right)$, $\mathrm{SO}\left(n\right)$ 在上述集合上的作用并判断其可递性.

### 解答 习题一

(1)验证作用: 对 $\rho,\tau\in\mathrm{GL}\left(n,\mathbb R\right)$ 及 $1$ 维子空间 $W=\mathbb Rv$,
$$
\begin{aligned}\rho\left(\tau\left(W\right)\right)&=\rho\left(\tau\left(\mathbb Rv\right)\right)\\&=\mathbb R\rho\tau\left(v\right)\\&=\left(\rho\tau\right)\left(W\right),\end{aligned}
$$
且单位矩阵 $I$ 满足 $I\left(W\right)=W$. 由**定义 1.9.1**（群作用）, 这是一个作用.

可递性: 任取两条直线 $W_1=\mathbb Rv$, $W_2=\mathbb Rw$, 其中 $v,w\ne0$. 存在可逆矩阵 $\rho$ 使 $\rho v=w$ (将 $v,w$ 分别扩充为基并定义线性映射), 故 $\rho\left(W_1\right)=W_2$. 由**定义 1.9.7**（可递作用与有效作用）, 作用可递.

迷向子群: 取 $W_0=\mathbb Re_1$, 其中 $e_1=\left(1,0,\cdots,0\right)^{T}$. 条件 $\rho\left(W_0\right)=W_0$ 等价于 $\rho e_1\in\mathbb Re_1$, 即 $\rho$ 的第一列为 $\left(a,0,\cdots,0\right)^{T}$, $a\ne0$. 故迷向子群为
$$
F_{W_0}=\left\{\begin{pmatrix}a & *\0 & A\end{pmatrix}\;\middle|\;a\in\mathbb R^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb R\right)\right\}.
$$

(2)验证作用同理: $\rho\left(\tau\left(W\right)\right)=\left(\rho\tau\right)\left(W\right)$.

可递性: 任取两个 $k$ 维子空间 $W_1,W_2$, 分别取基 $\left\{v_1,\cdots,v_k\right\}$ 与 $\left\{w_1,\cdots,w_k\right\}$, 扩充为 $\mathbb R^n$ 的基, 定义可逆线性映射 $\rho$ 使 $\rho v_i=w_i$, 则 $\rho\left(W_1\right)=W_2$. 故作用可递.

迷向子群: 取 $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$. 条件 $\rho\left(W_0\right)=W_0$ 等价于 $\rho$ 的前 $k$ 列在第 $k+1,\cdots,n$ 行的分量均为零, 即 $\rho$ 为分块上三角阵
$$
F_{W_0}=\left\{\begin{pmatrix}A & B\0 & C\end{pmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb R\right),\;C\in\mathrm{GL}\left(n-k,\mathbb R\right),\;B\in\mathbb R^{k\times\left(n-k\right)}\right\}.
$$

(3)$\mathrm{SL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 与 $\mathrm{Gr}\left(k,n\right)$ 上的作用均可递: 上述证明中, 若得到的映射行列式不为 $1$, 可在最后一行乘一个标量调整行列式为 $1$, 不改变子空间的像.

$O\left(n\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上可递: $O\left(n\right)$ 在单位球面上可递, 故在直线上可递. $O\left(n\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上亦可递: 两组标准正交基可通过正交映射互相映射.

$\mathrm{SO}\left(n\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上, 当 $n\ge3$ 时可递 (可通过适当旋转将任一方向映到任一方向而保持行列式为 $1$); 在 $\mathrm{Gr}\left(k,n\right)$ 上, 当 $n\ge3$ 时亦可递. $\blacksquare$

### 习题二

（习题 1.9-5）记 $V_k\left(\mathbb R^n\right)$ 为 $\mathbb R^n$ 中所有 $k$ 元标准正交向量组的全体, 称为斯蒂弗尔流形. 对任意 $\rho\in O\left(n\right)$, $\left(\alpha_1,\cdots,\alpha_k\right)\in V_k\left(\mathbb R^n\right)$, 定义
$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\left(\alpha_1\right),\cdots,\rho\left(\alpha_k\right)\right).
$$
试验证这是 $O\left(n\right)$ 在 $V_k\left(\mathbb R^n\right)$ 上的可递作用, 并求迷向子群.

### 解答 习题二

验证作用: 正交变换保持内积, 故若 $\left(\alpha_1,\cdots,\alpha_k\right)$ 为标准正交组, 则 $\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)$ 亦然. 且

$$
\rho\left(\tau\left(\alpha_1,\cdots,\alpha_k\right)\right)=\left(\rho\tau\right)\left(\alpha_1,\cdots,\alpha_k\right),
$$

单位矩阵作用不变, 故为群作用.

可递性: 任取两组标准正交向量组 $\left(\alpha_1,\cdots,\alpha_k\right)$ 与 $\left(\beta_1,\cdots,\beta_k\right)$, 分别扩充为 $\mathbb R^n$ 的标准正交基 $\left(\alpha_1,\cdots,\alpha_k,\cdots,\alpha_n\right)$ 与 $\left(\beta_1,\cdots,\beta_k,\cdots,\beta_n\right)$. 定义线性映射 $\rho\alpha_i=\beta_i$ ($i=1,\cdots,n$), 则 $\rho\in O\left(n\right)$ 且

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\beta_1,\cdots,\beta_k\right).
$$

故作用可递.

迷向子群: 取基准向量组 $\left(e_1,\cdots,e_k\right)$. 条件 $\rho\left(e_i\right)=e_i$ ($i=1,\cdots,k$) 意味着 $\rho$ 在前 $k$ 个标准基向量上为恒等映射, 即 $\rho$ 为分块对角阵
$$
F=\left\{\begin{pmatrix}I_k & 0\0 & A\end{pmatrix}\;\middle|\;A\in O\left(n-k\right)\right\}.
$$
这就是 $\left(e_1,\cdots,e_k\right)$ 的迷向子群. $\blacksquare$

### 习题三

（习题 1.9-6）将 $4$, $5$ 两题中的作用推广到复空间情形.

### 解答 习题三

复射影空间 $P^{n-1}\left(\mathbb C\right)$ 为 $\mathbb C^n$ 的所有 $1$ 维复子空间的全体, 复格拉斯曼流形 $\mathrm{Gr}_{\mathbb C}\left(k,n\right)$ 为 $\mathbb C^n$ 的所有 $k$ 维复子空间的全体. $\mathrm{GL}\left(n,\mathbb C\right)$ 分别以 $\rho\left(W\right)=\rho W$ 作用于二者, 验证方式与实情形完全相同, 作用均可递.

迷向子群分别为:
$$
F_{W_0}=\left\{\begin{pmatrix}a & *\0 & A\end{pmatrix}\;\middle|\;a\in\mathbb C^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb C\right)\right\}
$$
与
$$
F_{W_0}=\left\{\begin{pmatrix}A & B\0 & C\end{pmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb C\right),\;C\in\mathrm{GL}\left(n-k,\mathbb C\right),\;B\in\mathbb C^{k\times\left(n-k\right)}\right\}.
$$

复斯蒂弗尔流形 $V_k\left(\mathbb C^n\right)$ 为 $\mathbb C^n$ 中所有 $k$ 元标准正交向量组 (关于标准埃尔米特内积) 的全体. $U\left(n\right)$ 以

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)
$$

作用于其上, 酉变换保持埃尔米特内积, 故定义合理. 作用可递: 两组标准正交向量组分别扩充为标准正交基, 对应的酉映射即为所求. 迷向子群为
$$
F=\left\{\begin{pmatrix}I_k & 0\0 & A\end{pmatrix}\;\middle|\;A\in U\left(n-k\right)\right\}.
$$

此外, $\mathrm{SL}\left(n,\mathbb C\right)$, $U\left(n\right)$, $\mathrm{SU}\left(n\right)$ 在上述集合上的作用可递性与实情形平行: $\mathrm{SL}\left(n,\mathbb C\right)$ 在复射影空间与复格拉斯曼流形上可递; $U\left(n\right)$ 在复射影空间, 复格拉斯曼流形与复斯蒂弗尔流形上均可递; $\mathrm{SU}\left(n\right)$ 在相应集合上, 当维数足够时亦可递. $\blacksquare$

### 习题四

（习题 1.9-8）设
$$
H=\left\{z=x+iy\in\mathbb C\mid y>0\right\},
$$
称为庞加莱上半平面. 对任意

$$
g=\begin{pmatrix}a & b\c & d\end{pmatrix}\in\mathrm{SL}\left(2,\mathbb R\right),
$$

$z\in H$, 定义
$$
g\circ z=\frac{az+b}{cz+d}.
$$
试验证这定义了 $\mathrm{SL}\left(2,\mathbb R\right)$ 在 $H$ 上的一个作用 (称为默比乌斯变换或分式线性变换), 判断其可递性和有效性, 并求 $i$ 的迷向子群.

### 解答 习题四

先验证 $g\circ z\in H$. 对 $z=x+iy$, $y>0$, 直接计算虚部:
$$
\mathrm{Im}\left(\frac{az+b}{cz+d}\right)=\frac{y}{\left|cz+d\right|^{2}}>0,
$$
故 $g\circ z\in H$.

验证作用公理: 单位矩阵 $I=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ 给出 $I\circ z=z$. 又分式线性变换的复合对应矩阵乘法 (行列式为 $1$ 时), 即 $\left(g_1g_2\right)\circ z=g_1\circ\left(g_2\circ z\right)$. 故由**定义 1.9.1**（群作用）, 这是 $\mathrm{SL}\left(2,\mathbb R\right)$ 在 $H$ 上的作用.

可递性: 任取 $z=x+iy\in H$, $y>0$, 取
$$
g=\begin{pmatrix}\sqrt y & x/\sqrt y\0 & 1/\sqrt y\end{pmatrix},
$$
其行列式为 $1$, 且
$$
\begin{aligned}g\circ i&=\frac{\sqrt y\cdot i+x/\sqrt y}{1/\sqrt y}\\&=yi+x\\&=z.\end{aligned}
$$
故 $i$ 可映到任意 $z\in H$, 作用可递.

有效性: 若 $g\circ z=z$ 对一切 $z\in H$ 成立, 则分式线性变换 $\left(az+b\right)/\left(cz+d\right)$ 有无穷多个不动点, 故必为恒等变换, 即 $g=\pm I$. 其中 $-I=\begin{pmatrix}-1&0\\0&-1\end{pmatrix}$ 对一切 $z$ 也有 $\left(-I\right)\circ z=z$. 因此作用的核为 $\left\{\pm I\right\}$, 作用不是有效的; 其有效商群为

$$
\mathrm{PSL}\left(2,\mathbb R\right)=\mathrm{SL}\left(2,\mathbb R\right)/\left\{\pm I\right\}.
$$

$i$ 的迷向子群: 由 $g\circ i=i$, 即
$$
\begin{aligned}\frac{ai+b}{ci+d}=i,\\&\Longrightarrow\;ai+b&=i\left(ci+d\right)\\&=-c+di.\end{aligned}
$$
比较实虚部得 $b=-c$, $a=d$. 又

$$
\det g=ad-bc=a^{2}+c^{2}=1.
$$

故
$$
F_i=\left\{\begin{pmatrix}a & b\-b & a\end{pmatrix}\;\middle|\;a^{2}+b^{2}=1\right\}\cong SO\left(2\right).
$$
$\blacksquare$

### 习题五

（习题 1.9-19）(费马两平方和定理)设 $p=4k+1$ 为素数,
$$
X=\left\{\left(x,y,z\right)\in\mathbb N^{3}\mid x^{2}+4yz=p\right\}.
$$
设
$$
p_1:\left(x,y,z\right)\mapsto\left(x,z,y\right),
$$
$$
p_2:\left(x,y,z\right)\mapsto
\begin{cases}
\left(x+2z,\,z,\,y-x-z\right), & x<y-z,\\
\left(2y-x,\,y,\,x-y+z\right), & y-z\le x<2y,\\
\left(x-2y,\,x-y+z,\,y\right), & x\ge 2y.
\end{cases}
$$
证明: 上述两个映射分别定义了 $\mathbb Z_2$ 在 $X$ 上的两个作用, 试求两个作用的不动点的个数, 从而证明当 $p=4k+1$ 时, $x^{2}+y^{2}=p$ 有正整数解.

### 解答 习题五

先验证 $p_1$ 定义了 $\mathbb Z_2$ 的作用. $p_1$ 交换 $y,z$, 显然 $p_1^{2}=\mathrm{id}$, 且
$$
\begin{aligned}x^{2}+4zy&=x^{2}+4yz\\&=p,\end{aligned}
$$
故 $p_1\left(X\right)\subseteq X$. 因此 $p_1$ 是 $X$ 上的二阶对合, 定义了 $\mathbb Z_2=\left\{1,p_1\right\}$ 在 $X$ 上的作用.

再验证 $p_2$. 直接代入可验证在三个分段中 $p_2$ 保持方程 $x^{2}+4yz=p$ 不变, 且 $p_2^{2}=\mathrm{id}$ (三个分段互为逆映射, 边界处一致). 故 $p_2$ 也是 $X$ 上的对合, 定义了 $\mathbb Z_2$ 的另一个作用.

求 $p_2$ 的不动点. 对三种情况分别令 $p_2\left(x,y,z\right)=\left(x,y,z\right)$:

情况一 $x<y-z$: $x+2z=x$ 给出 $z=0$, 与 $z\in\mathbb N^{+}$ 矛盾, 无不动点.

情况二 $y-z\le x<2y$: $2y-x=x$ 给出 $x=y$; 第三坐标 $x-y+z=z$ 自动成立. 代入方程:
$$
\begin{aligned}x^{2}+4xz&=x\left(x+4z\right)\\&=p.\end{aligned}
$$
因 $p$ 为素数且 $x,x+4z$ 均为正整数, 故 $x=1$, $x+4z=p$, 即 $z=\left(p-1\right)/4=k$. 对应不动点为 $\left(1,1,k\right)$.

情况三 $x\ge2y$: $x-2y=x$ 给出 $y=0$, 矛盾.

故 $\left|\mathrm{Fix}\left(p_2\right)\right|=1$, 恰有一个不动点.

由于 $p_2$ 的非不动点轨道大小均为 $2$, 故
$$
\left|X\right|\equiv\left|\mathrm{Fix}\left(p_2\right)\right|\equiv1\pmod 2,
$$
即 $\left|X\right|$ 为奇数.

同理, $p_1$ 的非不动点轨道大小也为 $2$, 故
$$
\left|\mathrm{Fix}\left(p_1\right)\right|\equiv\left|X\right|\equiv1\pmod 2.
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
令 $a=x$, $b=2y$, 则 $a^{2}+b^{2}=p$, 且 $a,b$ 均为正整数 (因 $p$ 为奇素数, $x\ne0$; $y=z\ge1$ 故 $b=2y\ge2$).

因此当 $p=4k+1$ 时, $x^{2}+y^{2}=p$ 有正整数解. $\blacksquare$

### 习题六

（习题 1.9-20）(伯恩赛德引理)设群 $G$ 作用在集合 $X$ 上, 令 $t$ 表示 $X$ 在 $G$ 作用下的轨道的个数. 对任意 $g\in G$, $F\left(g\right)$ 表示 $X$ 在 $g$ 作用下不动点的个数, 即

$$
F\left(g\right)=\left|\left\{x\in X\mid gx=x\right\}\right|.
$$

试证
$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$

### 解答 习题六

考虑集合
$$
S=\left\{\left(g,x\right)\in G\times X\mid gx=x\right\}.
$$

按 $g$ 计数: 对固定的 $g\in G$, 满足 $gx=x$ 的 $x$ 恰有 $F\left(g\right)$ 个, 故
$$
\left|S\right|=\sum_{g\in G}F\left(g\right).
$$

按 $x$ 计数: 对固定的 $x\in X$, 满足 $gx=x$ 的 $g$ 恰为 $x$ 的迷向子群 $F_x=\left\{g\in G\mid gx=x\right\}$ 中的元素, 故
$$
\left|S\right|=\sum_{x\in X}\left|F_x\right|.
$$

由**推论 1.9.15**（轨道-迷向子群定理）, 对 $x$ 所在的轨道 $Ox$, 有

$$
\left|Ox\right|=\left[G:F_x\right]=\left|G\right|/\left|F_x\right|,
$$

即 $\left|F_x\right|=\left|G\right|/\left|Ox\right|$.

将 $X$ 分解为互不相交的轨道之并. 设 $X$ 共有 $t$ 个轨道 $O_1,\cdots,O_t$. 对轨道 $O_i$ 中的任意 $x$, $\left|Ox\right|=\left|O_i\right|$, 故 $\left|F_x\right|=\left|G\right|/\left|O_i\right|$. 于是
$$
\begin{aligned}\sum_{x\in X}\left|F_x\right|&=\sum_{i=1}^{t}\sum_{x\in O_i}\left|F_x\right|\\&=\sum_{i=1}^{t}\left|O_i\right|\cdot\frac{\left|G\right|}{\left|O_i\right|}\\&=\sum_{i=1}^{t}\left|G\right|\\&=t\left|G\right|.\end{aligned}
$$

综合两种计数方式, 得
$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$
$\blacksquare$
