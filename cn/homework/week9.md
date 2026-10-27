# week9

> **基础知识: 线性映射保持子空间维数**<br>可逆线性变换把 $k$ 维子空间映为 $k$ 维子空间; 对任意两个非零向量 $v,w$, 存在可逆线性变换 $\rho$ 使 $\rho v=w$ (分别把 $v,w$ 扩充为 $\mathbb R^n$ 的基并定义线性映射).

> **基础知识: 正交与酉变换**<br>正交变换保持内积, 因而把标准正交组映为标准正交组, 把 $k$ 维子空间映为 $k$ 维子空间; 任意两组标准正交基可由某个正交 (酉) 变换互相映射.

> **基础知识: 分式线性变换**<br>分式线性变换 (默比乌斯变换) $z\mapsto\frac{az+b}{cz+d}$ 的复合对应矩阵乘法; 具有无穷多个不动点的分式线性变换必为恒等变换.

> **基础知识: 群作用的轨道分解**<br>设 $G$ 作用在 $X$ 上, 则 $X$ 是互不相交的轨道之并; 对 $x\in X$, 轨道 $O_x$ 的大小为 $\left|G\right|/\left|F_x\right|$, 其中 $F_x$ 为 $x$ 的迷向子群. 特别地, 在 $\mathbb Z_2$ 作用于 $X$ 时, 非不动点的轨道恰含 $2$ 个元素, 故 $\left|X\right|\equiv\left|\mathrm{Fix}\right|\pmod 2$, 其中 $\mathrm{Fix}$ 为不动点集.

> **定义 1.9.1 (群作用)**<br>设 $G$ 是群, $X$ 是非空集合. 若映射 $f:G\times X\to X$ 满足 $f\left(e,x\right)=x$ 且 $f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right)$, 则称 $f$ 决定了 $G$ 在 $X$ 上的一个作用, 记 $f\left(g,x\right)=gx$.

> **定义 1.9.7 (可递作用与有效作用)**<br>若对任意 $x,y\in X$ 存在 $g\in G$ 使 $gx=y$, 称 $G$ 在 $X$ 上的作用可递, 称 $X$ 为 $G$ 的齐性空间. 若由 $gx=x$ 对一切 $x\in X$ 成立可推出 $g=e$, 称作用有效. 若对任意 $g\in G$, $x\in X$ 都有 $gx=x$, 称作用平凡.

> **定义 1.9.9 (轨道与迷向子群)**<br>设 $G$ 作用在 $X$ 上, $x\in X$. 称 $O_x=\left\{gx\mid g\in G\right\}$ 为 $x$ 的轨道. 称 $F_x=\left\{g\in G\mid gx=x\right\}$ 为 $x$ 的迷向子群.

> **推论 1.9.15 (轨道-迷向子群定理)**<br>设群 $G$ 作用在 $X$ 上, $x\in X$, 则 $\left|O_x\right|=\left|G/F_x\right|=\left[G:F_x\right]$; 从而 $\left|O_x\right|\mid\left|G\right|$.

---

## 1.9-4

(1) 记 $\mathbb R^n$ 的所有 $1$ 维子空间的全体为 $P^{n-1}\left(\mathbb R\right)$, 称为实射影空间. 对任意 $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$, $W\in P^{n-1}\left(\mathbb R\right)$, $\rho\left(W\right)$ 也是一个 $1$ 维子空间. 试验证这是 $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上的可递作用, 并求迷向子群.

(2) 记 $\mathbb R^n$ 的所有 $k$ 维子空间的全体为 $\mathrm{Gr}\left(k,n\right)$, 称为格拉斯曼流形. 对任意 $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$, $W\in\mathrm{Gr}\left(k,n\right)$, $\rho\left(W\right)$ 也是一个 $k$ 维子空间. 试验证这是 $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上的可递作用, 并求迷向子群.

(3) 考虑 $\mathrm{SL}\left(n,\mathbb R\right)$, $O\left(n\right)$, $\mathrm{SO}\left(n\right)$ 在上述集合上的作用并判断其可递性.

### 解答 1.9-4

**第 (1) 部分: $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上的作用.** 由**基础知识: 线性映射保持子空间维数**, 对 $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ 与 $1$ 维子空间 $W=\mathbb Rv$, $\rho\left(W\right)$ 仍是 $1$ 维子空间. 对 $\rho,\tau\in\mathrm{GL}\left(n,\mathbb R\right)$ 及 $W=\mathbb Rv$,

$$
\rho\left(\tau\left(W\right)\right)=\rho\left(\tau\left(\mathbb Rv\right)\right)=\rho\left(\mathbb R\tau\left(v\right)\right)=\mathbb R\rho\left(\tau\left(v\right)\right)=\left(\rho\tau\right)\left(W\right),
$$

且单位矩阵 $I$ 满足 $I\left(W\right)=W$. 由**定义 1.9.1 (群作用)**, 这是 $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上的一个作用.

**可递性**: 任取两条直线 $W_1=\mathbb Rv$, $W_2=\mathbb Rw$ ($v,w\ne0$). 由**基础知识: 线性映射保持子空间维数**, 存在可逆矩阵 $\rho$ 使 $\rho v=w$, 故 $\rho\left(W_1\right)=W_2$. 由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

**迷向子群**: 取 $W_0=\mathbb Re_1$, 其中 $e_1=\left(1,0,\cdots,0\right)^{\top}$. 条件 $\rho\left(W_0\right)=W_0$ 等价于 $\rho e_1\in\mathbb Re_1$, 即 $\rho$ 的第一列为 $\left(a,0,\cdots,0\right)^{\top}$, $a\ne0$. 故由**定义 1.9.9 (轨道与迷向子群)**, $W_0$ 的迷向子群为

$$
F_{W_0}=\left\{\begin{bmatrix}a & *\\0 & A\end{bmatrix}\;\middle|\;a\in\mathbb R^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb R\right)\right\}.
$$

**第 (2) 部分: $\mathrm{GL}\left(n,\mathbb R\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上的作用.** 同理 $\rho\left(\tau\left(W\right)\right)=\left(\rho\tau\right)\left(W\right)$ 且 $I\left(W\right)=W$, 由**定义 1.9.1 (群作用)** 这是作用.

**可递性**: 任取两个 $k$ 维子空间 $W_1,W_2$, 分别取基 $\left\{v_1,\cdots,v_k\right\}$ 与 $\left\{w_1,\cdots,w_k\right\}$, 扩充为 $\mathbb R^n$ 的基, 由**基础知识: 线性映射保持子空间维数** 定义可逆线性映射 $\rho$ 使 $\rho v_i=w_i$ ($i=1,\cdots,k$), 则 $\rho\left(W_1\right)=W_2$. 由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

**迷向子群**: 取 $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$. 条件 $\rho\left(W_0\right)=W_0$ 等价于 $\rho$ 把每个 $e_i$ ($i\le k$) 仍映回 $W_0$, 即 $\rho$ 的前 $k$ 列在第 $k+1,\cdots,n$ 行的分量为零, 亦即 $\rho$ 为分块上三角阵. 故由**定义 1.9.9 (轨道与迷向子群)**, 迷向子群为

$$
F_{W_0}=\left\{\begin{bmatrix}A & B\\0 & C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb R\right),\;C\in\mathrm{GL}\left(n-k,\mathbb R\right),\;B\in\mathbb R^{k\times\left(n-k\right)}\right\}.
$$

**第 (3) 部分: 判断可递性.** $\mathrm{SL}\left(n,\mathbb R\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 与 $\mathrm{Gr}\left(k,n\right)$ 上的作用均可递: 在第 (1)(2) 部分构造的映射 $\rho$ 中, 若其行列式不为 $1$, 可在最后一行乘一个非零标量把行列式调整为 $1$, 而不改变对子空间的作用.

$O\left(n\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上可递: 由**基础知识: 正交与酉变换**, 任意两条单位直线可由正交变换互相映射. $O\left(n\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上亦可递: 两组 $k$ 维子空间的基可扩充为两组标准正交基, 由**基础知识: 正交与酉变换** 存在正交映射互相映射.

$\mathrm{SO}\left(n\right)$ 在 $P^{n-1}\left(\mathbb R\right)$ 上, 当 $n\ge3$ 时可递 (可用适当旋转把任一方向映到任一方向而保持行列式为 $1$); 在 $\mathrm{Gr}\left(k,n\right)$ 上, 当 $n\ge3$ 时亦可递. $\blacksquare$

---

## 1.9-5

记 $V_k\left(\mathbb R^n\right)$ 为 $\mathbb R^n$ 中所有 $k$ 元标准正交向量组的全体, 称为斯蒂弗尔流形. 对任意 $\rho\in O\left(n\right)$, $\left(\alpha_1,\cdots,\alpha_k\right)\in V_k\left(\mathbb R^n\right)$, 定义

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\left(\alpha_1\right),\cdots,\rho\left(\alpha_k\right)\right).
$$

试验证这是 $O\left(n\right)$ 在 $V_k\left(\mathbb R^n\right)$ 上的可递作用, 并求迷向子群.

### 解答 1.9-5

**验证作用**: 由**基础知识: 正交与酉变换**, 正交变换保持内积, 故若 $\left(\alpha_1,\cdots,\alpha_k\right)$ 是标准正交组, 则 $\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)$ 亦然, 即 $\rho\left(\alpha_1,\cdots,\alpha_k\right)\in V_k\left(\mathbb R^n\right)$. 又

$$
\rho\left(\tau\left(\alpha_1,\cdots,\alpha_k\right)\right)=\rho\left(\tau\alpha_1,\cdots,\tau\alpha_k\right)=\left(\rho\tau\alpha_1,\cdots,\rho\tau\alpha_k\right)=\left(\rho\tau\right)\left(\alpha_1,\cdots,\alpha_k\right),
$$

且单位矩阵作用不变. 由**定义 1.9.1 (群作用)**, 这是 $O\left(n\right)$ 在 $V_k\left(\mathbb R^n\right)$ 上的作用.

**可递性**: 任取两组标准正交向量组 $\left(\alpha_1,\cdots,\alpha_k\right)$ 与 $\left(\beta_1,\cdots,\beta_k\right)$, 由**基础知识: 正交与酉变换** 分别扩充为 $\mathbb R^n$ 的标准正交基 $\left(\alpha_1,\cdots,\alpha_k,\cdots,\alpha_n\right)$ 与 $\left(\beta_1,\cdots,\beta_k,\cdots,\beta_n\right)$. 定义线性映射 $\rho\alpha_i=\beta_i$ ($i=1,\cdots,n$), 则 $\rho\in O\left(n\right)$ 且

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\beta_1,\cdots,\beta_k\right).
$$

由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

**迷向子群**: 取基准向量组 $\left(e_1,\cdots,e_k\right)$. 条件 $\rho\left(e_i\right)=e_i$ ($i=1,\cdots,k$) 意味着 $\rho$ 在前 $k$ 个标准基向量上为恒等映射, 即 $\rho$ 为分块对角阵. 由**定义 1.9.9 (轨道与迷向子群)**, 迷向子群为

$$
F=\left\{\begin{bmatrix}I_k & 0\\0 & A\end{bmatrix}\;\middle|\;A\in O\left(n-k\right)\right\}.
$$

这就是 $\left(e_1,\cdots,e_k\right)$ 的迷向子群. $\blacksquare$

---

## 1.9-6

将 1.9-4, 1.9-5 两题中的作用推广到复空间情形.

### 解答 1.9-6

**复射影空间与复格拉斯曼流形.** 复射影空间 $P^{n-1}\left(\mathbb C\right)$ 为 $\mathbb C^n$ 的所有 $1$ 维复子空间的全体, 复格拉斯曼流形 $\mathrm{Gr}_{\mathbb C}\left(k,n\right)$ 为 $\mathbb C^n$ 的所有 $k$ 维复子空间的全体. $\mathrm{GL}\left(n,\mathbb C\right)$ 分别以 $\rho\left(W\right)=\rho W$ 作用于二者, 由**基础知识: 线性映射保持子空间维数** 与复情形的等价论证 (与实情形完全相同), 由**定义 1.9.1 (群作用)** 与**定义 1.9.7 (可递作用与有效作用)**, 这是两个可递作用.

由**定义 1.9.9 (轨道与迷向子群)**, 分别取 $W_0=\mathbb Ce_1$ 与 $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$, 迷向子群分别为

$$
F_{W_0}=\left\{\begin{bmatrix}a & *\\0 & A\end{bmatrix}\;\middle|\;a\in\mathbb C^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb C\right)\right\}
$$

与

$$
F_{W_0}=\left\{\begin{bmatrix}A & B\\0 & C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb C\right),\;C\in\mathrm{GL}\left(n-k,\mathbb C\right),\;B\in\mathbb C^{k\times\left(n-k\right)}\right\}.
$$

**复斯蒂弗尔流形.** 记 $V_k\left(\mathbb C^n\right)$ 为 $\mathbb C^n$ 中所有 $k$ 元标准正交向量组 (关于标准埃尔米特内积) 的全体. $U\left(n\right)$ 以

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)
$$

作用于其上. 由**基础知识: 正交与酉变换**, 酉变换保持埃尔米特内积, 故定义合理, 由**定义 1.9.1 (群作用)** 这是作用. 作用可递: 由**基础知识: 正交与酉变换**, 两组标准正交向量组分别扩充为标准正交基, 对应的酉映射即为所求. 由**定义 1.9.9 (轨道与迷向子群)**, 取基准 $\left(e_1,\cdots,e_k\right)$, 迷向子群为

$$
F=\left\{\begin{bmatrix}I_k & 0\\0 & A\end{bmatrix}\;\middle|\;A\in U\left(n-k\right)\right\}.
$$

**可递性判断.** $\mathrm{SL}\left(n,\mathbb C\right)$ 在复射影空间与复格拉斯曼流形上可递 (仿实情形调整行列式); $U\left(n\right)$ 在复射影空间,复格拉斯曼流形与复斯蒂弗尔流形上均可递; $\mathrm{SU}\left(n\right)$ 在相应集合上, 当维数足够时亦可递. $\blacksquare$

---

## 1.9-8

设

$$
H=\left\{z=x+iy\in\mathbb C\mid y>0\right\},
$$

称为庞加莱上半平面. 对任意

$$
g=\begin{bmatrix}a & b\\c & d\end{bmatrix}\in\mathrm{SL}\left(2,\mathbb R\right),
$$

$z\in H$, 定义

$$
g\circ z=\frac{az+b}{cz+d}.
$$

试验证这定义了 $\mathrm{SL}\left(2,\mathbb R\right)$ 在 $H$ 上的一个作用 (称为默比乌斯变换或分式线性变换), 判断其可递性和有效性, 并求 $i$ 的迷向子群.

### 解答 1.9-8

**第一步: 验证 $g\circ z\in H$.** 对 $z=x+iy$ ($y>0$), 因 $\det g=ad-bc=1$, 直接计算虚部:

$$
\mathrm{Im}\left(\frac{az+b}{cz+d}\right)=\frac{\left(ad-bc\right)y}{\left|cz+d\right|^{2}}=\frac{y}{\left|cz+d\right|^{2}}>0,
$$

故 $g\circ z\in H$, 定义合理.

**第二步: 验证作用公理.** 单位矩阵 $I=\begin{bmatrix}1&0\\0&1\end{bmatrix}$ 给出 $I\circ z=z$. 又由**基础知识: 分式线性变换**, 分式线性变换的复合对应矩阵乘法, 即 $\left(g_1g_2\right)\circ z=g_1\circ\left(g_2\circ z\right)$. 由**定义 1.9.1 (群作用)**, 这是 $\mathrm{SL}\left(2,\mathbb R\right)$ 在 $H$ 上的作用.

**第三步: 判断可递性.** 任取 $z=x+iy\in H$ ($y>0$), 取

$$
g=\begin{bmatrix}\sqrt y & x/\sqrt y\\0 & 1/\sqrt y\end{bmatrix},
$$

其行列式为 $1$, 且

$$
g\circ i=\frac{\sqrt y\cdot i+x/\sqrt y}{0\cdot i+1/\sqrt y}=\left(\sqrt y\cdot i+\frac{x}{\sqrt y}\right)\sqrt y=yi+x=z.
$$

故 $i$ 可映到任意 $z\in H$, 由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

**第四步: 判断有效性.** 若 $g\circ z=z$ 对一切 $z\in H$ 成立, 则分式线性变换 $\frac{az+b}{cz+d}$ 有无穷多个不动点, 由**基础知识: 分式线性变换**, 它必为恒等变换, 故 $c=0$, $b=0$, $a=d$; 结合 $\det g=ad-bc=a^{2}=1$, 得 $g=\pm I$. 其中 $-I=\begin{bmatrix}-1&0\\0&-1\end{bmatrix}$ 对一切 $z$ 也有 $\left(-I\right)\circ z=\frac{-z}{-1}=z$. 故作用的核为 $\left\{\pm I\right\}$, 由**定义 1.9.7 (可递作用与有效作用)**, 作用不是有效的; 其有效商群为

$$
\mathrm{PSL}\left(2,\mathbb R\right)=\mathrm{SL}\left(2,\mathbb R\right)/\left\{\pm I\right\}.
$$

**第五步: 求 $i$ 的迷向子群.** 由 $g\circ i=i$, 即

$$
\frac{ai+b}{ci+d}=i,\quad\Longrightarrow\quad ai+b=i\left(ci+d\right)=ci^{2}+di=-c+di.
$$

比较实部与虚部得 $b=-c$, $a=d$. 又

$$
\det g=ad-bc=a^{2}-\left(-c\right)c=a^{2}+c^{2}=1.
$$

由**定义 1.9.9 (轨道与迷向子群)**, $i$ 的迷向子群为

$$
F_i=\left\{\begin{bmatrix}a & b\\-b & a\end{bmatrix}\;\middle|\;a^{2}+b^{2}=1\right\}\cong SO\left(2\right).
$$

$\blacksquare$

---

## 1.9-19

(费马两平方和定理) 设 $p=4k+1$ 为素数,

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
\left(x-2y,\,x-y+z,\,y\right), & x\ge2y.
\end{cases}
$$

证明: 上述两个映射分别定义了 $\mathbb Z_2$ 在 $X$ 上的两个作用, 试求两个作用的不动点的个数, 从而证明当 $p=4k+1$ 时, $x^{2}+y^{2}=p$ 有正整数解.

### 解答 1.9-19

**先验证 $p_1$ 定义了 $\mathbb Z_2$ 的作用.** $p_1$ 交换 $y,z$, 显然 $p_1^{2}=\mathrm{id}$; 且

$$
x^{2}+4zy=x^{2}+4yz=p,
$$

故 $p_1\left(X\right)\subseteq X$. 由**定义 1.9.1 (群作用)**, $p_1$ 是 $X$ 上的二阶对合, 定义了 $\mathbb Z_2=\left\{1,p_1\right\}$ 在 $X$ 上的作用.

**再验证 $p_2$.** 直接代入可验证在三个分段中 $p_2$ 都保持方程 $x^{2}+4yz=p$ 不变, 且 $p_2^{2}=\mathrm{id}$ (三个分段互为逆映射, 边界处一致). 由**定义 1.9.1 (群作用)**, $p_2$ 也是 $X$ 上的对合, 定义了 $\mathbb Z_2$ 的另一个作用.

**求 $p_2$ 的不动点.** 对三种情况分别令 $p_2\left(x,y,z\right)=\left(x,y,z\right)$:

情况一 $x<y-z$: 由 $x+2z=x$ 得 $z=0$, 与 $z\in\mathbb N^{+}$ 矛盾, 故无不动点.

情况二 $y-z\le x<2y$: 由 $2y-x=x$ 得 $x=y$; 第三坐标 $x-y+z=z$ 自动成立. 代入方程:

$$
x^{2}+4yz=x^{2}+4xz=x\left(x+4z\right)=p.
$$

因 $p$ 为素数且 $x$, $x+4z$ 均为正整数, 故 $x=1$, $x+4z=p$, 即 $z=\left(p-1\right)/4=k$. 对应不动点为 $\left(1,1,k\right)$.

情况三 $x\ge2y$: 由 $x-2y=x$ 得 $y=0$, 矛盾.

故 $\left|\mathrm{Fix}\left(p_2\right)\right|=1$, 恰有一个不动点.

由**基础知识: 群作用的轨道分解**, $p_2$ 的非不动点轨道大小均为 $2$, 故

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

令 $a=x$, $b=2y$, 则 $a^{2}+b^{2}=p$, 且 $a,b$ 均为正整数 (因 $p$ 为奇素数故 $x\ne0$; $y=z\ge1$ 故 $b=2y\ge2$).

因此当 $p=4k+1$ 时, $x^{2}+y^{2}=p$ 有正整数解. $\blacksquare$

---

## 1.9-20

(伯恩赛德引理) 设群 $G$ 作用在集合 $X$ 上, 令 $t$ 表示 $X$ 在 $G$ 作用下的轨道的个数. 对任意 $g\in G$, $F\left(g\right)$ 表示 $X$ 在 $g$ 作用下不动点的个数, 即

$$
F\left(g\right)=\left|\left\{x\in X\mid gx=x\right\}\right|.
$$

试证

$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$

### 解答 1.9-20

考虑集合

$$
S=\left\{\left(g,x\right)\in G\times X\mid gx=x\right\}.
$$

**按 $g$ 计数**: 对固定的 $g\in G$, 满足 $gx=x$ 的 $x$ 恰有 $F\left(g\right)$ 个, 故

$$
\left|S\right|=\sum_{g\in G}F\left(g\right).
$$

**按 $x$ 计数**: 对固定的 $x\in X$, 满足 $gx=x$ 的 $g$ 恰为 $x$ 的迷向子群 $F_x=\left\{g\in G\mid gx=x\right\}$ 中的元素, 故

$$
\left|S\right|=\sum_{x\in X}\left|F_x\right|.
$$

由**推论 1.9.15 (轨道-迷向子群定理)**, 对 $x$ 所在的轨道 $O_x$, 有

$$
\left|O_x\right|=\left[G:F_x\right]=\left|G\right|/\left|F_x\right|,
$$

即 $\left|F_x\right|=\left|G\right|/\left|O_x\right|$.

将 $X$ 分解为互不相交的轨道之并. 设 $X$ 共有 $t$ 个轨道 $O_1,\cdots,O_t$. 对轨道 $O_i$ 中的任意 $x$, $\left|O_x\right|=\left|O_i\right|$, 故 $\left|F_x\right|=\left|G\right|/\left|O_i\right|$. 于是

$$
\sum_{x\in X}\left|F_x\right|=\sum_{i=1}^{t}\sum_{x\in O_i}\left|F_x\right|=\sum_{i=1}^{t}\left|O_i\right|\cdot\frac{\left|G\right|}{\left|O_i\right|}=\sum_{i=1}^{t}\left|G\right|=t\left|G\right|.
$$

综合两种计数方式, 得

$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$

$\blacksquare$
