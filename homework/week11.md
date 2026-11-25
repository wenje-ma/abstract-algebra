# week11

> **定理 2.7.7 (贝祖等式)**
> 
> 设 $R$ 为主理想整环, $a,b\in{}R$, $d$ 为 $a,b$ 的一个最大公因子, 则存在 $u,v\in{}R$ 使 $d=ua+vb$.

> **定理 3.4.5 (主理想整环上有限生成模的结构定理)**
> 
> 主理想整环 $D$ 上的任何有限生成模 $M$ 都有分解 $M=Dy_1\oplus\cdots\oplus{}Dy_s$, 其中 $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$, 且 $y_j\ne0$. 其中非零零化子对应的 $d_i$ ($\operatorname{ann}\left(y_i\right)=\left(d_i\right)$) 称为不变因子, 其分解为不可约元素幂次者称为初等因子.

> **定理 3.4.9 (扭模的 $p$-分支分解)**
> 
> 设 $M$ 为主理想整环 $D$ 上有限生成扭模, 则存在有限个互不相伴的不可约元素 $p_1,\cdots,p_m$ 使 $M=M_{p_1}\oplus\cdots\oplus{}M_{p_m}$, 其中 $M_p=\left\{x\in{}M\mid\exists{}e,p^ex=0\right\}$ 为 $p$-分支. 特别地, 若 $\operatorname{ann}\left(y\right)=\left(ab\right)$ 且 $a,b$ 互素, 则 $Dy=Dy_1\oplus{}Dy_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$.

> **定理 3.5.2 (有限交换群的分类数)**
> 
> 设自然数 $n$ 有素因数分解 $n=p_1^{m_1}p_2^{m_2}\cdots{}p_s^{m_s}$, 其中 $p_1,p_2,\cdots,p_s$ 为互不相同的素数, $m_i>0$, 则在同构意义下 $n$ 阶交换群的个数为 $\prod_{i=1}^sp\left(m_i\right)$, 其中 $p\left(m\right)$ 表示自然数 $m$ 的不同分划的个数.

> **定理 3.6.3 (约当标准形)**
> 
> 设 $F$ 为特征为零的代数闭域, $V$ 为 $F$ 上 $n$ 维线性空间, $A$ 为 $V$ 上的线性变换, 则存在 $V$ 的一组基使得 $A$ 在该基下的矩阵为准对角矩阵 $\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, 其中每个 $J_i$ 都是约当块. 两个 $F$ 上 $n\times{}n$ 矩阵相似当且仅当它们具有相同的约当标准形.

## 3.6-9

设 $F$ 为特征为零的代数闭域, 试证明 $F$ 上任何一个约当块都能写成两个对称矩阵的乘积.

### 解答 3.6-9

设 $J$ 为 $F$ 上 $n$ 阶约当块, 其特征值为 $\lambda\in{}F$, 则 $J=\lambda{}I_n+N$, 其中 $N$ 为 $n$ 阶幂零移位矩阵.

设 $P$ 为 $n$ 阶反转矩阵. 由逆转置矩阵, $P$ 对称, $P^2=I_n$, 且 $PN$ 对称. 令 $A=PJ=\lambda{}P+PN$. 因 $P$ 与 $PN$ 均对称, 故 $A$ 为对称矩阵. 又 $P^2=I_n$, 故 $P^{-1}=P$, 于是 $J=P^{-1}A=PA$.

其中 $P$ 与 $A$ 均为 $F$ 上对称矩阵. 故任一约当块均可写成两个对称矩阵的乘积.

$\blacksquare$

## 3.6-10

试证明任何一个特征为零的代数闭域 $F$ 上的方阵都能写成 $F$ 上两个对称矩阵的乘积.

### 解答 3.6-10

设 $A$ 为 $F$ 上 $n$ 阶方阵. 由**定理 3.6.3 (约当标准形)**, 存在可逆矩阵 $S$ 使 $S^{-1}AS=J=\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, 其中 $J_1,J_2,\cdots,J_s$ 均为约当块.

由3.6-9 的结论, 每个约当块 $J_i$ 可写为 $J_i=P_iQ_i$, 其中 $P_i,Q_i$ 均为对称矩阵. 令 $P=\mathrm{diag}\left(P_1,P_2,\cdots,P_s\right)$, $Q=\mathrm{diag}\left(Q_1,Q_2,\cdots,Q_s\right)$, 则 $P,Q$ 均为对称矩阵, 且 $J=PQ$.

于是 $A=SJS^{-1}=SPQS^{-1}=\left(SPS^{\top}\right)\left(S^{-T}QS^{-1}\right)$. 其中 $SPS^{\top}$ 为对称矩阵, 因其转置为 $\left(SPS^{\top}\right)^{\top}=SP^{\top}S^{\top}=SPS^{\top}$; 同理 $S^{-T}QS^{-1}=\left(S^{-1}\right)^{\top}QS^{-1}$ 亦为对称矩阵. 故 $A$ 为两个对称矩阵之积.

$\blacksquare$

## 3.6-11

设 $A$ 为实线性空间 $V$ 上的线性变换, 试证明存在 $V$ 的一组基使得在这组基下 $A$ 的矩阵具有分块矩阵 $\begin{bmatrix}B_1&B_2\\0&B_3\end{bmatrix}$ 的形式, 其中 $B_1$ 为 $1$ 阶或 $2$ 阶方阵.

### 解答 3.6-11

对 $\dim{}V=n$ 作归纳. 当 $n=1$ 时结论显然成立. 假设维数小于 $n$ 时结论成立, 考虑 $n$ 维情形.

情形一 $A$ 有实特征值 $\lambda$. 取对应的实特征向量 $v_1$, 扩充为 $V$ 的一组基 $v_1,v_2,\cdots,v_n$. 因 $v_1$ 生成的一维子空间是 $A$-不变子空间, $A$ 在该基下的矩阵形如 $\begin{bmatrix}\lambda&*\\0&A'\end{bmatrix}$, 其中 $\lambda$ 为 $1$ 阶块, $A'$ 为 $n-1$ 阶实矩阵. 由归纳假设, $A'$ 可相似于所要求的分块上三角形式, 从而 $A$ 亦然.

情形二 $A$ 无实特征值. 此时 $A$ 的特征多项式在 $\mathbb{R}\left[x\right]$ 上没有一次因式, 故可分解为若干个判别式小于零的二次不可约多项式之积. 取其中一个 $p\left(x\right)=x^2+bx+c$, $b^2-4c<0$.

由主理想整环 $\mathbb{R}\left[x\right]$ 上有限生成扭模的结构理论 (即 $V$ 作为 $\mathbb{R}\left[x\right]$-模的准素分解), $p\left(x\right)$ 对应的准素子空间非零. 取其中向量 $u$ 使得 $p\left(A\right)u=0$ 且 $u\ne0$. 因 $p\left(x\right)$ 无实根, $u$ 与 $Au$ 必线性无关 (否则 $Au=au$, $a\in\mathbb{R}$, 则 $a$ 为 $p$ 的实根, 矛盾). 令 $W=\mathrm{span}\left\{u,Au\right\}$. 由 $p\left(A\right)u=0$ 即 $A^2u+bAu+cu=0$ 得 $A\left(Au\right)=A^2u=-cu-bAu\in{}W$, 故 $W$ 是 $2$ 维 $A$-不变子空间. 取 $W$ 的一组基, 扩充为 $V$ 的一组基, 则 $A$ 在该基下的矩阵形如 $\begin{bmatrix}B_1&B_2\\0&A'\end{bmatrix}$, 其中 $B_1$ 为 $2$ 阶方阵 ($A$ 在 $W$ 上的限制), $A'$ 为 $n-2$ 阶实矩阵. 由归纳假设, $A'$ 可化为所要求的分块上三角形式, 从而 $A$ 亦然.

综上, 由归纳法, 存在 $V$ 的一组基使 $A$ 的矩阵为所要求的分块上三角形式.

$\blacksquare$

## 3.6-12

(韦尔定理) 试证明特征为零的代数闭域上两个 $n\times{}n$ 矩阵 $A,B$ 相似当且仅当对任何 $a\in{}F$ 及 $k\in\mathbb{N}$, $\left(aI_n-A\right)^k$ 与 $\left(aI_n-B\right)^k$ 具有相同的秩.

### 解答 3.6-12

必要性. 若 $A$ 与 $B$ 相似, 则存在可逆矩阵 $P$ 使 $B=P^{-1}AP$. 于是 $\left(aI_n-B\right)^k=\left(aI_n-P^{-1}AP\right)^k=P^{-1}\left(aI_n-A\right)^kP$. 相似矩阵秩相同, 故 $\mathrm{rank}\left(aI_n-A\right)^k=\mathrm{rank}\left(aI_n-B\right)^k$.

充分性. 设对任何 $a\in{}F$ 及 $k\in\mathbb{N}$, 两矩阵相应幂的秩相同. 由**定理 3.6.3 (约当标准形)**, $A,B$ 均相似于其约当标准形, 只需证明二者约当标准形相同.

对任一 $a\in{}F$, 记 $\nu_k\left(A\right)=\dim\ker\left(aI_n-A\right)^k=n-\mathrm{rank}\left(aI_n-A\right)^k$, 并约定 $\nu_0\left(A\right)=0$. 由题设, $\nu_k\left(A\right)=\nu_k\left(B\right)$ 对所有 $k$ 成立. 由幂零核与约当块计数, $A$ 的以 $a$ 为特征值, 阶数不小于 $s$ 的约当块个数为 $\nu_s\left(A\right)-\nu_{s-1}\left(A\right)$, $B$ 同理. 故二者在 $a$ 处的约当块大小与个数完全一致.

由于 $F$ 是代数闭域, $A,B$ 的全部特征值均在 $F$ 中, 上述结论对每个特征值 $a$ 成立. 因而 $A$ 与 $B$ 的约当标准形完全相同, 从而 $A$ 与 $B$ 相似.

$\blacksquare$

## 4.1-4

求下列域扩张的次数:

(1) $\left[\mathbb{Q}\left(\sqrt2+\sqrt3\right):\mathbb{Q}\right]$;

(2) $\left[\mathbb{Q}\left(\sqrt2+\sqrt3\right):\mathbb{Q}\left(\sqrt3\right)\right]$.

### 解答 4.1-4

按**定义 4.1.15 (扩张次数)**, 记 $\alpha=\sqrt2+\sqrt3$. 先证明 $\mathbb{Q}\left(\alpha\right)=\mathbb{Q}\left(\sqrt2,\sqrt3\right)$.

一方面, $\alpha\in\mathbb{Q}\left(\sqrt2,\sqrt3\right)$, 故 $\mathbb{Q}\left(\alpha\right)\subseteq\mathbb{Q}\left(\sqrt2,\sqrt3\right)$.

另一方面, 因 $\left(\sqrt2+\sqrt3\right)\left(\sqrt3-\sqrt2\right)=3-2=1$, 故 $\alpha^{-1}=\sqrt3-\sqrt2$. 于是 $\sqrt2=\frac{\alpha-\alpha^{-1}}{2}\in\mathbb{Q}\left(\alpha\right)$, 同理 $\sqrt3=\frac{\alpha+\alpha^{-1}}{2}\in\mathbb{Q}\left(\alpha\right)$, 故 $\mathbb{Q}\left(\sqrt2,\sqrt3\right)\subseteq\mathbb{Q}\left(\alpha\right)$. 因而 $\mathbb{Q}\left(\alpha\right)=\mathbb{Q}\left(\sqrt2,\sqrt3\right)$.

再证 $\sqrt2\notin\mathbb{Q}\left(\sqrt3\right)$. 反设 $\sqrt2=a+b\sqrt3$, $a,b\in\mathbb{Q}$. 两边平方得 $2=a^2+3b^2+2ab\sqrt3$. 因 $1,\sqrt3$ 在 $\mathbb{Q}$ 上线性无关, 故 $ab=0$. 若 $b=0$, 则 $2=a^2$, 无有理解; 若 $a=0$, 则 $2=3b^2$, 即 $b^2=2/3$, 亦无有理解. 故 $\sqrt2\notin\mathbb{Q}\left(\sqrt3\right)$.

于是 $\left[\mathbb{Q}\left(\sqrt2,\sqrt3\right):\mathbb{Q}\left(\sqrt3\right)\right]=2$. 又 $\left[\mathbb{Q}\left(\sqrt3\right):\mathbb{Q}\right]=2$ (因 $x^2-3$ 不可约). 由**定理 4.1.16 (扩张次数的望远镜法则)**,

$$
\left[\mathbb{Q}\left(\sqrt2,\sqrt3\right):\mathbb{Q}\right]=\left[\mathbb{Q}\left(\sqrt2,\sqrt3\right):\mathbb{Q}\left(\sqrt3\right)\right]\left[\mathbb{Q}\left(\sqrt3\right):\mathbb{Q}\right]=2\times2=4.
$$

(1) 因 $\mathbb{Q}\left(\alpha\right)=\mathbb{Q}\left(\sqrt2,\sqrt3\right)$, 故 $\left[\mathbb{Q}\left(\sqrt2+\sqrt3\right):\mathbb{Q}\right]=4$.

(2) 同理 $\left[\mathbb{Q}\left(\sqrt2+\sqrt3\right):\mathbb{Q}\left(\sqrt3\right)\right]=2$.

$\blacksquare$

## 4.1-10

证明: $\mathbb{R}/\mathbb{Q}$ 是无限扩张.

### 解答 4.1-10

数 $\pi\in\mathbb{R}$ 是 $\mathbb{Q}$ 上的超越元 (林德曼定理), 即 $\pi$ 不是任何非零有理系数多项式的根.

若 $\mathbb{R}/\mathbb{Q}$ 为有限扩张, 由**引理 4.2.1 (有限扩张必为代数扩张)**, $\mathbb{R}$ 中每个元素都是 $\mathbb{Q}$ 上的代数元, 特别地 $\pi$ 应为 $\mathbb{Q}$ 上的代数元, 矛盾.

故 $\mathbb{R}/\mathbb{Q}$ 不是有限扩张, 即 $\mathbb{R}/\mathbb{Q}$ 是无限扩张.

$\blacksquare$

## 4.1-11

设 $E$ 是整环 $R$ 的分式域. 对任意 $R$ 的自同构 $\sigma$ 定义 $\overline\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\left(\sigma\left(b\right)\right)^{-1}$. 证明: $\overline\sigma$ 是 $E$ 的自同构.

### 解答 4.1-11

依分式域的泛性质, 分三步验证.

良定义. 设 $ab^{-1}=cd^{-1}$, $a,b,c,d\in{}R$, $b,d\ne0$. 则 $ad=bc$. 由 $\sigma$ 为环同态, $\sigma\left(a\right)\sigma\left(d\right)=\sigma\left(ad\right)=\sigma\left(bc\right)=\sigma\left(b\right)\sigma\left(c\right)$, 故 $\sigma\left(a\right)\sigma\left(b\right)^{-1}=\sigma\left(c\right)\sigma\left(d\right)^{-1}$, 即 $\overline\sigma\left(ab^{-1}\right)=\overline\sigma\left(cd^{-1}\right)$. 定义与代表元选取无关.

环同态. 对 $x=ab^{-1}$, $y=cd^{-1}\in{}E$, 有

$$
\overline\sigma\left(xy\right)=\overline\sigma\left(ac\left(bd\right)^{-1}\right)=\sigma\left(ac\right)\sigma\left(bd\right)^{-1}=\sigma\left(a\right)\sigma\left(c\right)\sigma\left(b\right)^{-1}\sigma\left(d\right)^{-1}=\overline\sigma\left(x\right)\overline\sigma\left(y\right),
$$

且

$$
\overline\sigma\left(x+y\right)=\overline\sigma\left(\left(ad+bc\right)\left(bd\right)^{-1}\right)=\sigma\left(ad+bc\right)\sigma\left(bd\right)^{-1}=\frac{\sigma\left(a\right)}{\sigma\left(b\right)}+\frac{\sigma\left(c\right)}{\sigma\left(d\right)}=\overline\sigma\left(x\right)+\overline\sigma\left(y\right).
$$

又 $\overline\sigma\left(1\right)=\sigma\left(1\right)\sigma\left(1\right)^{-1}=1$, 故 $\overline\sigma$ 为环同态.

双射. 因 $\sigma$ 是 $R$ 的自同构, 其逆 $\tau=\sigma^{-1}$ 亦为 $R$ 的自同构. 直接验证可知 $\overline\tau$ 为 $\overline\sigma$ 的逆映射: 对 $x=ab^{-1}\in{}E$,

$$
\overline\tau\circ\overline\sigma\left(x\right)=\overline\tau\left(\sigma\left(a\right)\sigma\left(b\right)^{-1}\right)=\tau\left(\sigma\left(a\right)\right)\tau\left(\sigma\left(b\right)\right)^{-1}=ab^{-1}=x.
$$

同理 $\overline\sigma\circ\overline\tau=\mathrm{id}$. 故 $\overline\sigma$ 可逆, 为 $E$ 的自同构.

$\blacksquare$
