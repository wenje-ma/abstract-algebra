# 作业 2

> **定义 1.2.1**（子群）设 $H$ 是群 $G$ 的一个非空子集, 如果 $H$ 对于 $G$ 的运算也构成群, 则称 $H$ 为 $G$ 的子群, 记作 $H<G$.

> **定理 1.2.2**（子群判别法）设 $H$ 是群 $G$ 的非空子集, 则 $H<G$ 当且仅当对任意 $a,b\in H$ 有 $ab^{-1}\in H$.

> **定理 1.2.22**（拉格朗日定理）设 $G$ 是有限群, $H<G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, 其中 $\left[G:H\right]$ 为 $H$ 在 $G$ 中的指数. 从而子群 $H$ 的阶是群 $G$ 的阶的因子, 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

> **推论 1.2.23**（指数的乘法）设 $G$ 是有限群, $K<H<G$, 则有 $\left[G:K\right]=\left[G:H\right]\cdot\left[H:K\right]$.

> **基础知识**（元素的阶）设 $G$ 为群, $a\in G$, 则 $\left\langle a\right\rangle=\left\{a^{n}\mid n\in\mathbb Z\right\}$ 是 $G$ 的子群, 称为由 $a$ 生成的子群. 该子群的阶称为元素 $a$ 的阶.

> **基础知识**（最小公倍数与最大公因数）对正整数 $m,n$, 记 $\left(m,n\right)$ 为最大公因数, $\left[m,n\right]$ 为最小公倍数, 满足 $\left(m,n\right)\left[m,n\right]=mn$.

### 习题一

（习题 1.2-8）设 $a,b$ 分别是群 $G$ 中的 $m,n$ 阶元, $ab=ba$.

（1）若 $\left(m,n\right)=1$, 证明 $ab$ 的阶为 $mn$;

（2）若 $\left\langle a\right\rangle\cap\left\langle b\right\rangle=\left\{e\right\}$, 证明: $ab$ 的阶为 $\left[m,n\right]$;

（3）如果 $\left\langle a\right\rangle\cap\left\langle b\right\rangle\ne\left\{e\right\}$, 试讨论 $ab$ 的阶. $G$ 中是否一定存在 $\left[m,n\right]$ 阶元素?

### 解答 习题一

（1）因 $ab=ba$, 故对任意整数 $k$ 有 $\left(ab\right)^{k}=a^{k}b^{k}$. 于是

$$
\begin{aligned}\left(ab\right)^{mn}&=a^{mn}b^{mn}\\&=\left(a^{m}\right)^{n}\left(b^{n}\right)^{m}\\&=e,\end{aligned}
$$

故 $ab$ 的阶整除 $mn$.

反之, 若 $\left(ab\right)^{k}=e$, 则 $a^{k}=b^{-k}$. 左端属于 $\left\langle a\right\rangle$, 右端属于 $\left\langle b\right\rangle$, 故 $a^{k}\in\left\langle a\right\rangle\cap\left\langle b\right\rangle$. 由**定理 1.2.22**（拉格朗日定理）, $\left|\left\langle a\right\rangle\cap\left\langle b\right\rangle\right|$ 同时整除 $\left|\left\langle a\right\rangle\right|=m$ 与 $\left|\left\langle b\right\rangle\right|=n$, 故整除 $\left(m,n\right)=1$, 即 $\left\langle a\right\rangle\cap\left\langle b\right\rangle=\left\{e\right\}$. 因此 $a^{k}=e$, $b^{k}=e$, 从而 $m\mid k$, $n\mid k$. 由 $\left(m,n\right)=1$ 得 $mn\mid k$.

综上, $ab$ 的阶为 $mn$.

（2）设 $d=\left[m,n\right]$. 因 $m\mid d$, $n\mid d$, 故

$$
\begin{aligned}\left(ab\right)^{d}&=a^{d}b^{d}\\&=e,\end{aligned}
$$

故 $ab$ 的阶整除 $d$.

反之, 若 $\left(ab\right)^{k}=e$, 则 $a^{k}=b^{-k}\in\left\langle a\right\rangle\cap\left\langle b\right\rangle=\left\{e\right\}$, 故 $a^{k}=e$, $b^{k}=e$. 于是 $m\mid k$, $n\mid k$, 从而 $\left[m,n\right]\mid k$.

因此 $ab$ 的阶为 $\left[m,n\right]$.

（3）当 $\left\langle a\right\rangle\cap\left\langle b\right\rangle\ne\left\{e\right\}$ 时, $ab$ 的阶仍整除 $\left[m,n\right]$, 但可能严格小于 $\left[m,n\right]$.

举例: 取 $G=\mathbb Z_{4}\times\mathbb Z_{4}$, $a=\left(1,0\right)$, $b=\left(1,2\right)$. 则 $a,b$ 均为 $4$ 阶元, $\left\langle a\right\rangle=\left\{\left(0,0\right),\left(1,0\right),\left(2,0\right),\left(3,0\right)\right\}$, $\left\langle b\right\rangle=\left\{\left(0,0\right),\left(1,2\right),\left(2,0\right),\left(3,2\right)\right\}$, 其交为 $\left\{\left(0,0\right),\left(2,0\right)\right\}\ne\left\{e\right\}$. 而 $ab=\left(2,2\right)$, 满足 $2ab=\left(0,0\right)$, 故 $ab$ 的阶为 $2<\left[4,4\right]=4$.

关于 $G$ 中是否一定存在 $\left[m,n\right]$ 阶元素, 答案是肯定的. 事实上, 由 $ab=ba$ 知子群 $H=\left\langle a,b\right\rangle$ 是交换群. 在交换群 $H$ 中, 设 $m=\prod p^{\alpha_{p}}$, $n=\prod p^{\beta_{p}}$ 为素因数分解. 对每个素数 $p$, 若 $\alpha_{p}\ge\beta_{p}$, 则取 $a^{m/p^{\alpha_{p}}}$, 其阶为 $p^{\alpha_{p}}$; 若 $\beta_{p}>\alpha_{p}$, 则取 $b^{n/p^{\beta_{p}}}$, 其阶为 $p^{\beta_{p}}$. 将所有这些元素相乘（因 $H$ 交换, 乘积有意义）, 所得元素的阶即为 $\prod p^{\max\left(\alpha_{p},\beta_{p}\right)}=\left[m,n\right]$. 故 $G$ 中必存在 $\left[m,n\right]$ 阶元素. $\blacksquare$

### 习题二

（习题 1.2-13）设 $SL\left(n,\mathbb Z\right)$ 的元素为整数且行列式为 $1$ 的 $n$ 阶方阵的全体.

（1）证明: $SL\left(n,\mathbb Z\right)$ 是 $GL\left(n,\mathbb R\right)$ 的子群;

（2）设 $S=\begin{pmatrix}0&-1\\1&0\end{pmatrix}$, $T=\begin{pmatrix}1&1\\0&1\end{pmatrix}$, $R=\begin{pmatrix}0&-1\\1&1\end{pmatrix}$, $U=\begin{pmatrix}1&0\\1&1\end{pmatrix}$, 证明: 其中任两个元素都是 $SL\left(2,\mathbb Z\right)$ 的生成元.

### 解答 习题二

（1）$SL\left(n,\mathbb Z\right)$ 非空, 因单位矩阵 $I_{n}$ 的元素均为整数且 $\det I_{n}=1$.

对任意 $A,B\in SL\left(n,\mathbb Z\right)$, $A,B$ 的元素均为整数, 故 $AB^{-1}$ 的元素亦为整数, 且

$$
\begin{aligned}\det\left(AB^{-1}\right)&=\det A\cdot\det\left(B^{-1}\right)\\&=\det A/\det B\\&=1/1\\&=1.\end{aligned}
$$

故 $AB^{-1}\in SL\left(n,\mathbb Z\right)$. 由**定理 1.2.2**（子群判别法）, $SL\left(n,\mathbb Z\right)<GL\left(n,\mathbb R\right)$.

（2）首先验证 $S,T,R,U$ 均属于 $SL\left(2,\mathbb Z\right)$: 各矩阵元素均为整数, 且行列式均为 $1$.

先证 $\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$. 这是 $SL\left(2,\mathbb Z\right)$ 的标准生成元结果: 任一 $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}\in SL\left(2,\mathbb Z\right)$, 可通过左乘 $T^{k}=\begin{pmatrix}1&k\\0&1\end{pmatrix}$（对应行初等变换: 第一行加 $k$ 倍第二行）和 $U^{k}=\begin{pmatrix}1&0\\k&1\end{pmatrix}$（对应第二行加 $k$ 倍第一行）配合辗转相除法将 $A$ 化为对角形, 又由行列式为 $1$ 可知对角元必为 $\pm1$, 再由 $S$ 可将 $-I$ 表出. 故 $\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$.

下面证明其余各对均与 $\left\langle S,T\right\rangle$ 相等.

**$R=ST$** 直接计算:

$$
\begin{aligned}ST&=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}\\&=\begin{pmatrix}0&-1\\1&1\end{pmatrix}\\&=R.\end{aligned}
$$

故 $T=S^{-1}R$, 从而 $\left\langle S,R\right\rangle=\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$. 同理, $S=RT^{-1}$, 故 $\left\langle T,R\right\rangle=\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$.

**$U$ 与 $S$ 的关系** 计算 $S^{-1}TS$:

$$
\begin{aligned}S^{-1}TS&=\begin{pmatrix}0&1\\-1&0\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}0&-1\\1&0\end{pmatrix}\\&=\begin{pmatrix}1&0\\-1&1\end{pmatrix}\\&=U^{-1}.\end{aligned}
$$

故 $T=SU^{-1}S^{-1}$, 从而 $\left\langle S,U\right\rangle\supseteq\left\langle S,T\right\rangle$. 又 $U=S^{-1}T^{-1}S\in\left\langle S,T\right\rangle$, 故 $\left\langle S,U\right\rangle=\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$.

**$\left\langle T,U\right\rangle=SL\left(2,\mathbb Z\right)$** $T$ 与 $U$ 即为初等矩阵 $\begin{pmatrix}1&1\\0&1\end{pmatrix}$ 与 $\begin{pmatrix}1&0\\1&1\end{pmatrix}$. 由上述辗转相除法, 仅用这两个初等变换即可将任意 $SL\left(2,\mathbb Z\right)$ 中元化为 $\pm I$, 故 $\left\langle T,U\right\rangle=SL\left(2,\mathbb Z\right)$.

**$\left\langle R,U\right\rangle=SL\left(2,\mathbb Z\right)$** 由 $R=ST$ 及 $U^{-1}=S^{-1}TS$, 代入得

$$
\begin{aligned}U^{-1}&=S^{-1}\left(S^{-1}R\right)S\\&=S^{-2}RS\\&=-IRS\\&=-RS,\end{aligned}
$$

其中 $S^{2}=-I$. 故 $S=-R^{-1}U^{-1}$. 又 $R^{3}=-I$（直接验证 $R^{3}=\begin{pmatrix}-1&0\\0&-1\end{pmatrix}$）, 所以 $-I=R^{3}\in\left\langle R,U\right\rangle$, 从而 $S=R^{3}R^{-1}U^{-1}=R^{2}U^{-1}\in\left\langle R,U\right\rangle$. 于是 $T=S^{-1}R\in\left\langle R,U\right\rangle$, 故 $\left\langle R,U\right\rangle\supseteq\left\langle S,T\right\rangle=SL\left(2,\mathbb Z\right)$. 反方向显然成立, 故 $\left\langle R,U\right\rangle=SL\left(2,\mathbb Z\right)$.

综上, $S,T,R,U$ 中任两个生成元均生成 $SL\left(2,\mathbb Z\right)$. $\blacksquare$

### 习题三

（习题 1.2-20）设 $H_{1},H_{2}$ 为有限群 $G$ 的两个子群, 证明 $\left[G:H_{1}\cap H_{2}\right]\le\left[G:H_{1}\right]\left[G:H_{2}\right]$. 又若 $\left[G:H_{1}\right]$ 与 $\left[G:H_{2}\right]$ 互素, 则 $\left[G:H_{1}\cap H_{2}\right]=\left[G:H_{1}\right]\left[G:H_{2}\right]$ 且 $G=H_{1}H_{2}$.

### 解答 习题三

先证不等式. 考虑映射

$$
\varphi:G/\left(H_{1}\cap H_{2}\right)\to G/H_{1}\times G/H_{2},\quad g\left(H_{1}\cap H_{2}\right)\mapsto\left(gH_{1},gH_{2}\right).
$$

**良定义** 若 $g\left(H_{1}\cap H_{2}\right)=g'\left(H_{1}\cap H_{2}\right)$, 则 $g^{-1}g'\in H_{1}\cap H_{2}\subseteq H_{1}$ 且 $\subseteq H_{2}$, 故 $gH_{1}=g'H_{1}$, $gH_{2}=g'H_{2}$.

**单射** 若 $\left(gH_{1},gH_{2}\right)=\left(g'H_{1},g'H_{2}\right)$, 则 $g^{-1}g'\in H_{1}$ 且 $g^{-1}g'\in H_{2}$, 故 $g^{-1}g'\in H_{1}\cap H_{2}$, 从而 $g\left(H_{1}\cap H_{2}\right)=g'\left(H_{1}\cap H_{2}\right)$.

因此 $\varphi$ 是单射, 故

$$
\begin{aligned}\left[G:H_{1}\cap H_{2}\right]&=\left|G/\left(H_{1}\cap H_{2}\right)\right|\\&\le\left|G/H_{1}\right|\cdot\left|G/H_{2}\right|\\&=\left[G:H_{1}\right]\left[G:H_{2}\right].\end{aligned}
$$

再证互素情形下的等号成立. 由**推论 1.2.23**（指数的乘法）,

$$
\left[G:H_{1}\cap H_{2}\right]=\left[G:H_{1}\right]\left[H_{1}:H_{1}\cap H_{2}\right].
$$

因 $H_{1}\cap H_{2}<H_{1}<G$ 及 $H_{1}\cap H_{2}<H_{2}<G$, 故 $\left[G:H_{1}\right]\mid\left[G:H_{1}\cap H_{2}\right]$ 且 $\left[G:H_{2}\right]\mid\left[G:H_{1}\cap H_{2}\right]$. 又 $\left[G:H_{1}\right]$ 与 $\left[G:H_{2}\right]$ 互素, 故其乘积 $\left[G:H_{1}\right]\left[G:H_{2}\right]\mid\left[G:H_{1}\cap H_{2}\right]$.

结合已证的不等式 $\left[G:H_{1}\cap H_{2}\right]\le\left[G:H_{1}\right]\left[G:H_{2}\right]$, 得

$$
\left[G:H_{1}\cap H_{2}\right]=\left[G:H_{1}\right]\left[G:H_{2}\right].
$$

最后证 $G=H_{1}H_{2}$. 由子群乘积的阶公式,

$$
\left|H_{1}H_{2}\right|=\frac{\left|H_{1}\right|\left|H_{2}\right|}{\left|H_{1}\cap H_{2}\right|}.
$$

由**定理 1.2.22**（拉格朗日定理）, $\left|H_{1}\right|=\left|G\right|/\left[G:H_{1}\right]$, $\left|H_{2}\right|=\left|G\right|/\left[G:H_{2}\right]$, $\left|H_{1}\cap H_{2}\right|=\left|G\right|/\left[G:H_{1}\cap H_{2}\right]=\left|G\right|/\left(\left[G:H_{1}\right]\left[G:H_{2}\right]\right)$. 代入得

$$
\begin{aligned}\left|H_{1}H_{2}\right|&=\frac{\left(\left|G\right|/\left[G:H_{1}\right]\right)\cdot\left(\left|G\right|/\left[G:H_{2}\right]\right)}{\left|G\right|/\left(\left[G:H_{1}\right]\left[G:H_{2}\right]\right)}\\&=\left|G\right|.\end{aligned}
$$

因 $H_{1}H_{2}\subseteq G$ 且二者元素个数相同, 故 $G=H_{1}H_{2}$. $\blacksquare$
