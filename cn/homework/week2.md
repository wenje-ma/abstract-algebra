# week2

> **基础知识: 元素的阶与生成子群**<br>设 $a\in G$, 则 $\left\langle a\right\rangle=\left\{a^{n}\mid n\in\mathbb Z\right\}$ 是 $G$ 的子群, 称为由 $a$ 生成的子群; 该子群的阶称为元素 $a$ 的阶. 若 $a$ 的阶为 $m$, 则 $a^{m}=e$, 且对任意整数 $k$ 有 $a^{k}=e$ 当且仅当 $m\mid k$.

> **基础知识: 交换群中幂运算的分配**<br>若 $ab=ba$, 则对任意整数 $k$ 有 $\left(ab\right)^{k}=a^{k}b^{k}$.

> **基础知识: 元素幂的阶**<br>若 $a$ 的阶为 $m$, 则 $a^{k}$ 的阶为 $\frac{m}{\left(m,k\right)}$, 其中 $\left(m,k\right)$ 是 $m,k$ 的最大公因数.

> **基础知识: 最大公因数与最小公倍数**<br>对正整数 $m,n$, 记 $\left(m,n\right)$ 为最大公因数, $\left[m,n\right]$ 为最小公倍数, 则 $\left(m,n\right)\left[m,n\right]=mn$; $m\mid k$ 且 $n\mid k$ 当且仅当 $\left[m,n\right]\mid k$; 若 $\left(m,n\right)=1$, 则 $m\mid k$ 且 $n\mid k$ 当且仅当 $mn\mid k$.

> **基础知识: 素因数分解与最高次幂**<br>任一正整数 $m$ 可唯一分解为 $m=\prod_{p}p^{\alpha_p}$; 对 $m=\prod_{p}p^{\alpha_p}$, $n=\prod_{p}p^{\beta_p}$ 有 $\left[m,n\right]=\prod_{p}p^{\max\left(\alpha_p,\beta_p\right)}$.

> **基础知识: 互素阶交换元素之积的阶**<br>设 $x,y$ 交换且 $o\left(x\right),o\left(y\right)$ 互素, 则 $o\left(xy\right)=o\left(x\right)o\left(y\right)$.

> **基础知识: 整数矩阵的伴随矩阵与行列式**<br>若方阵 $B$ 的元素均为整数且 $\left|B\right|=1$, 则 $B^{-1}$ 的元素均为整数; 且 $\left|AB^{-1}\right|=\left|A\right|\left|B^{-1}\right|=\frac{\left|A\right|}{\left|B\right|}$.

> **基础知识: 初等行变换与辗转相除法**<br>左乘 $\begin{bmatrix}1&k\\0&1\end{bmatrix}$ 等价于把某行加上另一行的 $k$ 倍; 由辗转相除法, 反复作这两类初等行变换可将任一整数矩阵化为对角形; 若所得对角矩阵的行列式为 $1$, 则其对角元必为 $\pm1$, 且 $\begin{bmatrix}-1&0\\0&-1\end{bmatrix}$ 可由 $\begin{bmatrix}0&-1\\1&0\end{bmatrix}$ 表出 (因其平方等于 $-I$).

> **基础知识: 有限集乘积的阶**<br>设 $H,K$ 是群 $G$ 的有限子群, 则 $\left|HK\right|=\frac{\left|H\right|\left|K\right|}{\left|H\cap K\right|}$: 事实上映射 $H\times K\to HK$, $\left(h,k\right)\mapsto hk$ 是满射, 且 $\left(h_1,k_1\right),\left(h_2,k_2\right)$ 像相同当且仅当 $h_1^{-1}h_2=k_1k_2^{-1}\in H\cap K$, 故每个像有恰好 $\left|H\cap K\right|$ 个原像.

> **定义 1.2.1 (子群)**<br>设 $H$ 是群 $G$ 的一个非空子集, 如果 $H$ 对于 $G$ 的运算也构成群, 则称 $H$ 为 $G$ 的子群, 记作 $H<G$.

> **定理 1.2.2 (子群判别法)**<br>设 $H$ 是群 $G$ 的非空子集, 则下列条件等价: (1) $H$ 是 $G$ 的子群; (2) 对任意 $a,b\in H$, 有 $ab\in H$, $a^{-1}\in H$; (3) 对任意 $a,b\in H$, 有 $ab^{-1}\in H$.

> **引理 1.2.12 (陪集重合条件)**<br>设 $H$ 是群 $G$ 的子群, $a,b\in G$, 则 $aH$ 和 $bH$ 要么互不相交, 要么重合, 且 $aH=bH$ 当且仅当 $a^{-1}b\in H$.

> **定理 1.2.22 (拉格朗日定理)**<br>设 $G$ 是有限群, $H<G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, 其中 $\left[G:H\right]$ 为 $H$ 在 $G$ 中的指数. 从而子群 $H$ 的阶是群 $G$ 的阶的因子, 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

> **推论 1.2.23 (指数的乘法)**<br>设 $G$ 是有限群, $K<G$, $H<K$, 则 $\left[G:H\right]=\left[G:K\right]\cdot\left[K:H\right]$.

---

## 1.2-8

设 $a,b$ 分别是群 $G$ 中的 $m,n$ 阶元, $ab=ba$.

(1) 若 $\left(m,n\right)=1$, 证明 $ab$ 的阶为 $mn$;

(2) 若 $\left\langle a\right\rangle\cap\left\langle b\right\rangle=\left\{e\right\}$, 证明: $ab$ 的阶为 $\left[m,n\right]$;

(3) 如果 $\left\langle a\right\rangle\cap\left\langle b\right\rangle\ne\left\{e\right\}$, 试讨论 $ab$ 的阶. $G$ 中是否一定存在 $\left[m,n\right]$ 阶元素?

### 解答 1.2-8

**(1) 证明 $ab$ 的阶为 $mn$.** 由**基础知识: 交换群中幂运算的分配**, 因 $ab=ba$, 对任意整数 $k$ 有 $\left(ab\right)^{k}=a^{k}b^{k}$. 于是

$$
\left(ab\right)^{mn}=a^{mn}b^{mn}=\left(a^{m}\right)^{n}\left(b^{n}\right)^{m}=e,
$$

故由**基础知识: 元素的阶与生成子群**, $ab$ 的阶整除 $mn$.

反之, 设 $\left(ab\right)^{k}=e$. 则由 $\left(ab\right)^{k}=a^{k}b^{k}$ 得 $a^{k}b^{k}=e$, 即 $a^{k}=b^{-k}$. 左端 $a^{k}\in\left\langle a\right\rangle$, 右端 $b^{-k}\in\left\langle b\right\rangle$, 故 $a^{k}\in\left\langle a\right\rangle\cap\left\langle b\right\rangle$. 由**定理 1.2.22 (拉格朗日定理)**, $\left|\left\langle a\right\rangle\cap\left\langle b\right\rangle\right|$ 同时整除 $\left|\left\langle a\right\rangle\right|=m$ 与 $\left|\left\langle b\right\rangle\right|=n$, 故整除 $\left(m,n\right)=1$, 因而 $\left|\left\langle a\right\rangle\cap\left\langle b\right\rangle\right|=1$, 即 $\left\langle a\right\rangle\cap\left\langle b\right\rangle=\left\{e\right\}$. 于是 $a^{k}=b^{-k}\in\left\langle a\right\rangle\cap\left\langle b\right\rangle=\left\{e\right\}$, 即 $a^{k}=e$, $b^{k}=e$. 由**基础知识: 元素的阶与生成子群**, $m\mid k$ 且 $n\mid k$. 因 $\left(m,n\right)=1$, 由**基础知识: 最大公因数与最小公倍数**, $mn\mid k$.

综上, $ab$ 的阶整除 $mn$ 且 $mn$ 整除 $ab$ 的阶, 故 $ab$ 的阶为 $mn$.

**(2) 证明 $ab$ 的阶为 $\left[m,n\right]$.** 记 $d=\left[m,n\right]$. 由**基础知识: 交换群中幂运算的分配**, $\left(ab\right)^{d}=a^{d}b^{d}$. 因 $m\mid d$, $n\mid d$, 故 $a^{d}=\left(a^{m}\right)^{\frac{d}{m}}=e$, $b^{d}=\left(b^{n}\right)^{\frac{d}{n}}=e$, 于是 $\left(ab\right)^{d}=e$, 由**基础知识: 元素的阶与生成子群**, $ab$ 的阶整除 $d$.

反之, 设 $\left(ab\right)^{k}=e$, 则由 $\left(ab\right)^{k}=a^{k}b^{k}$ 得 $a^{k}=b^{-k}$. 因 $b^{-k}\in\left\langle b\right\rangle$ 且 $a^{k}\in\left\langle a\right\rangle$, 故 $a^{k}\in\left\langle a\right\rangle\cap\left\langle b\right\rangle=\left\{e\right\}$, 即 $a^{k}=e$, 从而 $b^{k}=e$. 由**基础知识: 元素的阶与生成子群**, $m\mid k$, $n\mid k$, 再由**基础知识: 最大公因数与最小公倍数**, $\left[m,n\right]\mid k$.

综上, $ab$ 的阶整除 $d$ 且 $d$ 整除 $ab$ 的阶, 故 $ab$ 的阶为 $\left[m,n\right]$.

**(3) 讨论 $ab$ 的阶.** 当 $\left\langle a\right\rangle\cap\left\langle b\right\rangle\ne\left\{e\right\}$ 时, 由 (2) 的论证可知 $ab$ 的阶仍整除 $\left[m,n\right]$, 但可能严格小于 $\left[m,n\right]$.

举例: 取 $G=\mathbb Z_4\times\mathbb Z_4$, $a=\left(1,0\right)$, $b=\left(1,2\right)$. 则 $a,b$ 均为 $4$ 阶元, 且

$$
\left\langle a\right\rangle=\left\{\left(0,0\right),\left(1,0\right),\left(2,0\right),\left(3,0\right)\right\},\quad\left\langle b\right\rangle=\left\{\left(0,0\right),\left(1,2\right),\left(2,0\right),\left(3,2\right)\right\},
$$

其交 $\left\langle a\right\rangle\cap\left\langle b\right\rangle=\left\{\left(0,0\right),\left(2,0\right)\right\}\ne\left\{e\right\}$. 而 $ab=\left(2,2\right)$, 且 $2ab=\left(0,0\right)$, 故 $ab$ 的阶为 $2<4=\left[4,4\right]$.

关于 $G$ 中是否一定存在 $\left[m,n\right]$ 阶元素, 答案是肯定的. 因 $ab=ba$, 子群 $H=\left\langle a,b\right\rangle$ 是交换群. 设 $m=\prod_{p}p^{\alpha_p}$, $n=\prod_{p}p^{\beta_p}$ 为素因数分解 (**基础知识: 素因数分解与最高次幂**). 对每个素数 $p$: 若 $\alpha_p\ge\beta_p$, 由**基础知识: 元素幂的阶**, $a^{m/p^{\alpha_p}}$ 的阶为 $\frac{m}{\left(m,m/p^{\alpha_p}\right)}=\frac{m}{m/p^{\alpha_p}}=p^{\alpha_p}$; 若 $\beta_p>\alpha_p$, 则 $b^{n/p^{\beta_p}}$ 的阶为 $\frac{n}{\left(n,n/p^{\beta_p}\right)}=p^{\beta_p}$. 于是对每个 $p$ 我们得到一个阶为 $p^{\max\left(\alpha_p,\beta_p\right)}$ 的元素 $x_p\in H$, 且当 $p$ 取不同素数时这些阶两两互素. 因 $H$ 是交换群, 这些 $x_p$ 两两交换, 反复用**基础知识: 互素阶交换元素之积的阶**, 乘积 $\prod_p x_p$ 的阶为 $\prod_p p^{\max\left(\alpha_p,\beta_p\right)}=\left[m,n\right]$. 故 $G$ 中必存在 $\left[m,n\right]$ 阶元素. $\blacksquare$

---

## 1.2-13

设 $SL\left(n,\mathbb Z\right)$ 为元素均为整数且行列式为 $1$ 的 $n$ 阶方阵的全体.

(1) 证明: $SL\left(n,\mathbb Z\right)$ 是 $GL\left(n,\mathbb R\right)$ 的子群;

(2) 设 $S=\begin{bmatrix}0&-1\\1&0\end{bmatrix}$, $T=\begin{bmatrix}1&1\\0&1\end{bmatrix}$, $R=\begin{bmatrix}0&-1\\1&1\end{bmatrix}$, $U=\begin{bmatrix}1&0\\1&1\end{bmatrix}$, 证明: 其中任两个元素都是 $SL\left(2,\mathbb Z\right)$ 的生成元.

### 解答 1.2-13

**(1) 证明 $SL\left(n,\mathbb Z\right)<GL\left(n,\mathbb R\right)$.** 单位矩阵 $I_n$ 的元素均为整数且 $\left|I_n\right|=1$, 故 $SL\left(n,\mathbb Z\right)$ 非空. 对任意 $A,B\in SL\left(n,\mathbb Z\right)$, $B$ 的元素均为整数且 $\left|B\right|=1$, 由**基础知识: 整数矩阵的伴随矩阵与行列式**, $B^{-1}$ 的元素均为整数, 故 $AB^{-1}$ 的元素均为整数. 又由**基础知识: 整数矩阵的伴随矩阵与行列式**, $\left|AB^{-1}\right|=\frac{\left|A\right|}{\left|B\right|}=\frac{1}{1}=1$. 故 $AB^{-1}\in SL\left(n,\mathbb Z\right)$. 依据**定理 1.2.2 (子群判别法)** (条件 (3)), $SL\left(n,\mathbb Z\right)<GL\left(n,\mathbb R\right)$.

**(2) 证明 $S,T,R,U$ 中任两个都生成 $SL\left(2,\mathbb Z\right)$.** 首先验证 $S,T,R,U\in SL\left(2,\mathbb Z\right)$: 各矩阵的元素均为整数, 且直接计算得 $\left|S\right|=\left|T\right|=\left|R\right|=\left|U\right|=1$.

**先证 $\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$.** 对任意 $A=\begin{bmatrix}a&b\\c&d\end{bmatrix}\in SL\left(2,\mathbb Z\right)$, 由**基础知识: 初等行变换与辗转相除法**, 反复用左乘 $T^{k}$ 与 $U^{k}$ (即两类初等行变换) 配合辗转相除法可将 $A$ 化为对角矩阵; 又因 $\left|A\right|=1$ 且初等变换不改变行列式的绝对值, 所得对角矩阵的对角元必为 $\pm1$ 且乘积为 $\pm1$. 再由 $S^{2}=-I$ 可将 $-I$ 表出, 从而 $A$ 可由 $S,T$ 化为单位矩阵 $I$. 反之 $S,T\in SL\left(2,\mathbb Z\right)$, 故 $\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$.

下面证明其余各对生成的子群都等于 $\left\langle S,T\right\rangle$.

**$\left\langle S,R\right\rangle$ 与 $\left\langle T,R\right\rangle$.** 直接计算

$$
ST=\begin{bmatrix}0&-1\\1&0\end{bmatrix}\begin{bmatrix}1&1\\0&1\end{bmatrix}=\begin{bmatrix}0&-1\\1&1\end{bmatrix}=R.
$$

故 $R=ST$, 即 $R\in\left\langle S,T\right\rangle$, 且 $T=S^{-1}R\in\left\langle S,R\right\rangle$, $S=RT^{-1}\in\left\langle T,R\right\rangle$. 于是 $\left\langle S,R\right\rangle\supseteq\left\langle S,T\right\rangle$ 且 $\left\langle T,R\right\rangle\supseteq\left\langle S,T\right\rangle$; 又 $S,T$ 是 $S,R$ (或 $T,R$) 的表达式中出现的矩阵, 反包含显然, 故 $\left\langle S,R\right\rangle=\left\langle T,R\right\rangle=\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$.

**$\left\langle S,U\right\rangle$.** 计算 $S^{-1}TS$:

$$
S^{-1}TS=\begin{bmatrix}0&1\\-1&0\end{bmatrix}\begin{bmatrix}1&1\\0&1\end{bmatrix}\begin{bmatrix}0&-1\\1&0\end{bmatrix}=\begin{bmatrix}1&0\\-1&1\end{bmatrix}=U^{-1}.
$$

故 $T=SU^{-1}S^{-1}\in\left\langle S,U\right\rangle$, 于是 $\left\langle S,U\right\rangle\supseteq\left\langle S,T\right\rangle$. 又 $U=S^{-1}T^{-1}S\in\left\langle S,T\right\rangle$, 故 $\left\langle S,U\right\rangle\subseteq\left\langle S,T\right\rangle$. 因此 $\left\langle S,U\right\rangle=\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$.

**$\left\langle T,U\right\rangle$.** $T=\begin{bmatrix}1&1\\0&1\end{bmatrix}$, $U=\begin{bmatrix}1&0\\1&1\end{bmatrix}$ 正是**基础知识: 初等行变换与辗转相除法**中的两类初等变换矩阵, 由辗转相除法仅用这两类初等行变换即可将任一 $SL\left(2,\mathbb Z\right)$ 中元化为 $\pm I$, 故 $\left\langle T,U\right\rangle=SL\left(2,\mathbb Z\right)$.

**$\left\langle R,U\right\rangle$.** 由 $R=ST$ 得 $T=S^{-1}R$, 又 $U^{-1}=S^{-1}TS$, 代入得

$$
U^{-1}=S^{-1}\left(S^{-1}R\right)S=S^{-2}RS.
$$

因 $S^{2}=-I$, 故 $S^{-2}=\left(-I\right)^{-1}=-I$, 于是 $U^{-1}=-IRS=-RS$, 即 $S=-R^{-1}U^{-1}$. 直接计算 $R^{3}=\begin{bmatrix}-1&0\\0&-1\end{bmatrix}=-I$, 故 $-I=R^{3}\in\left\langle R,U\right\rangle$, 从而

$$
S=\left(-I\right)\left(-S\right)=\left(-I\right)\left(R^{-1}U^{-1}\right)=R^{3}R^{-1}U^{-1}=R^{2}U^{-1}\in\left\langle R,U\right\rangle.
$$

于是 $T=S^{-1}R\in\left\langle R,U\right\rangle$, 故 $\left\langle R,U\right\rangle\supseteq\left\langle S,T\right\rangle$. 又 $R,U\in SL\left(2,\mathbb Z\right)$, 反包含 $\left\langle R,U\right\rangle\subseteq\left\langle S,T\right\rangle$ 显然. 因此 $\left\langle R,U\right\rangle=\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$.

综上, $S,T,R,U$ 中任两个元素都生成 $SL\left(2,\mathbb Z\right)$. $\blacksquare$

---

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

**再证互素情形下的等号.** 由**推论 1.2.23 (指数的乘法)**, 因 $H_{1}\cap H_{2}<H_{1}<G$,

$$
\left[G:H_{1}\cap H_{2}\right]=\left[G:H_{1}\right]\left[H_{1}:H_{1}\cap H_{2}\right].
$$

故 $\left[G:H_{1}\right]\mid\left[G:H_{1}\cap H_{2}\right]$. 同理, 由 $H_{1}\cap H_{2}<H_{2}<G$, $\left[G:H_{2}\right]\mid\left[G:H_{1}\cap H_{2}\right]$. 因 $\left[G:H_{1}\right]$ 与 $\left[G:H_{2}\right]$ 互素, 由**基础知识: 最大公因数与最小公倍数**, $\left[G:H_{1}\right]\left[G:H_{2}\right]\mid\left[G:H_{1}\cap H_{2}\right]$. 结合已证不等式 $\left[G:H_{1}\cap H_{2}\right]\le\left[G:H_{1}\right]\left[G:H_{2}\right]$, 得 $\left[G:H_{1}\cap H_{2}\right]=\left[G:H_{1}\right]\left[G:H_{2}\right]$.

**最后证 $G=H_{1}H_{2}$.** 由**基础知识: 有限集乘积的阶**,

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
