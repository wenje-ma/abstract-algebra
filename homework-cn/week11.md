# week11

> **定理 2.7.7 (贝祖等式)**
> 
> 设 $R$ 为主理想整环, $a,b\in R$, $d$ 为 $a,b$ 的一个最大公因子, 则存在 $u,v\in R$ 使 $d=ua+vb$.

> **定理 3.4.5 (主理想整环上有限生成模的结构定理)**
> 
> 主理想整环 $D$ 上的任何有限生成模 $M$ 都有分解 $M=Dy_1\oplus\cdots\oplus Dy_s$, 其中 $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$, 且 $y_j\ne0$. 其中非零零化子对应的 $d_i$ ($\operatorname{ann}\left(y_i\right)=\left(d_i\right)$) 称为不变因子, 其分解为不可约元素幂次者称为初等因子.

> **定理 3.4.9 (扭模的 $p$-分支分解)**
> 
> 设 $M$ 为主理想整环 $D$ 上有限生成扭模, 则存在有限个互不相伴的不可约元素 $p_1,\cdots,p_m$ 使 $M=M_{p_1}\oplus\cdots\oplus M_{p_m}$, 其中 $M_p=\left\{x\in M\mid \exists e,p^ex=0\right\}$ 为 $p$-分支. 特别地, 若 $\operatorname{ann}\left(y\right)=\left(ab\right)$ 且 $a,b$ 互素, 则 $Dy=Dy_1\oplus Dy_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$.

> **推论 3.4.12 (有限生成模的同构判定)**
> 
> 设 $M_1,M_2$ 为主理想整环 $D$ 上的有限生成模, 则 $M_1\cong M_2$ 当且仅当它们有相同的秩和不变因子, 当且仅当有相同的秩和初等因子.

> **定理 3.5.2 (有限交换群的分类数)**
> 
> 设自然数 $n$ 有素因数分解 $n=p_1^{m_1}p_2^{m_2}\cdots p_s^{m_s}$, 其中 $p_1,p_2,\cdots,p_s$ 为互不相同的素数, $m_i> 0$, 则在同构意义下 $n$ 阶交换群的个数为 $\prod_{i=1}^s p\left(m_i\right)$, 其中 $p\left(m\right)$ 表示自然数 $m$ 的不同分划的个数.

> **定理 3.6.3 (约当标准形)**
> 
> 设 $F$ 为特征为零的代数闭域, $V$ 为 $F$ 上 $n$ 维线性空间, $A$ 为 $V$ 上的线性变换, 则存在 $V$ 的一组基使得 $A$ 在该基下的矩阵为准对角矩阵 $\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, 其中每个 $J_i$ 都是约当块. 两个 $F$ 上 $n\times n$ 矩阵相似当且仅当它们具有相同的约当标准形.

## 3.4-6

设 $D$ 是主理想整环, $M$ 是 $D$ 上有限生成的扭模, 对 $a\in D$, 令 $M\left(a\right)=\left\{x\in M\mid ax=0\right\}$. 试证明:

(1) $M\left(a\right)$ 是 $M$ 的子模, 且若 $a$ 可逆, 则 $M\left(a\right)=\left\{0\right\}$;

(2) 若 $a\mid b$, 则 $M\left(a\right)\subset M\left(b\right)$;

(3) 设 $a,b\in D$, 则 $M\left(a\right)\cap M\left(b\right)=M\left(\left(a,b\right)\right)$, 其中 $\left(a,b\right)$ 为 $a,b$ 的一个最大公因子;

(4) 若 $a,b$ 互素, 则 $M\left(ab\right)=M\left(a\right)\oplus M\left(b\right)$.

### 解答 3.4-6

(1) $M\left(a\right)$ 非空 (含 $0$). 若 $x,y\in M\left(a\right)$, 则 $a\left(x-y\right)=ax-ay=0$; 对 $r\in D$, $a\left(rx\right)=r\left(ax\right)=0$. 故 $M\left(a\right)$ 是子模. 若 $a$ 可逆, $ax=0$ 两边乘 $a^{-1}$ 得 $x=0$, 故 $M\left(a\right)=\left\{0\right\}$.

(2) 设 $b=ac$. 若 $x\in M\left(a\right)$, $ax=0$, 则 $bx=cax=0$, 故 $x\in M\left(b\right)$. 因而 $M\left(a\right)\subset M\left(b\right)$.

(3) 记 $d=\left(a,b\right)$ 为最大公因子. 由 $d\mid a$, $d\mid b$, 用 (2) 得 $M\left(d\right)\subset M\left(a\right)$ 且 $M\left(d\right)\subset M\left(b\right)$, 故 $M\left(d\right)\subset M\left(a\right)\cap M\left(b\right)$.

反之, 若 $x\in M\left(a\right)\cap M\left(b\right)$, 则 $ax=bx=0$. 由**定理 2.7.7 (贝祖等式)**, 存在 $u,v\in D$ 使 $d=ua+vb$. 于是 $dx=\left(ua+vb\right)x=uax+vbx=0$, 故 $x\in M\left(d\right)$. 因此 $M\left(a\right)\cap M\left(b\right)=M\left(d\right)=M\left(\left(a,b\right)\right)$.

(4) 设 $a,b$ 互素, 即 $\left(a,b\right)=1$. 由 (2), $a\mid ab$, $b\mid ab$, 故 $M\left(a\right)\subset M\left(ab\right)$, $M\left(b\right)\subset M\left(ab\right)$, 因而 $M\left(a\right)+M\left(b\right)\subset M\left(ab\right)$.

再求交. 由 (3), $M\left(a\right)\cap M\left(b\right)=M\left(\left(a,b\right)\right)=M\left(1\right)=\left\{0\right\}$ (用 (1)).

最后证 $M\left(ab\right)\subset M\left(a\right)+M\left(b\right)$. 由 $\left(a,b\right)=1$ 及**定理 2.7.7 (贝祖等式)**, 存在 $u,v$ 使 $ua+vb=1$. 对任意 $x\in M\left(ab\right)$, $abx=0$. 写 $x=\left(ua+vb\right)x=uax+vb x$. 记 $x_1=vb x$, $x_2=uax$. 则 $ax_1=avb x=vab x=0$, $bx_2=bua x=uab x=0$, 故 $x_1\in M\left(a\right)$, $x_2\in M\left(b\right)$, 从而 $x=x_1+x_2\in M\left(a\right)+M\left(b\right)$.

综上, $M\left(ab\right)=M\left(a\right)+M\left(b\right)$ 且 $M\left(a\right)\cap M\left(b\right)=\left\{0\right\}$, 故 $M\left(ab\right)=M\left(a\right)\oplus M\left(b\right)$. $\blacksquare$

## 3.4-10

设 $M$ 为主理想整环 $D$ 上的扭模, 试证明 $M$ 为单模当且仅当 $M=Dz$, 且 $\operatorname{ann}\left(z\right)=\left(p\right)$, 其中 $p$ 为素元素; 而 $M$ 为不可分解模当且仅当 $M=Dz$ 且 $\operatorname{ann}\left(z\right)=\left(p^e\right)$, 其中 $p$ 为素元素, $e\in\mathbb N$. (题面原文末式残缺, 按教材上下文补全为 $\left(p^e\right)$.)

### 解答 3.4-10

**单模情形.**

必要性. 设 $M$ 为单扭模. 由**定理 3.4.5 (主理想整环上有限生成模的结构定理)**, $M=Dy_1\oplus\cdots\oplus Dy_s$. 若 $s\ge2$, 则 $Dy_1$ 是 $M$ 的非平凡子模, 与单模矛盾. 故 $s=1$, $M=Dz$, $\operatorname{ann}\left(z\right)=\left(d\right)$.

若 $d$ 不是素元素, 则 $d$ 有非平凡分解 $d=ab$, $a,b$ 均非单位. 由**定理 3.4.9 (扭模的 $p$-分支分解)**, $Dz=Dy_1\oplus Dy_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$, 两个均为非零子模, 又与单模矛盾. 故 $d=p$ 为素元素.

充分性. 设 $M=Dz$, $\operatorname{ann}\left(z\right)=\left(p\right)$, $p$ 素. 则 $M\cong D/\left(p\right)$. 因 $p$ 为素元素, $\left(p\right)$ 是极大理想, $D/\left(p\right)$ 是域, 作为 $D$-模它只有零和自身两个子模. 故 $M$ 是单模.

**不可分解模情形.**

必要性. 设 $M$ 不可分解. 由结构定理 $M=Dy_1\oplus\cdots\oplus Dy_s$. 若 $s\ge2$, 它已是两个非零子模的直和, 矛盾. 故 $s=1$, $M=Dz$, $\operatorname{ann}\left(z\right)=\left(d\right)$.

若 $d$ 含有两个互素的非单位因子, 即 $d=ab$, $\left(a,b\right)=1$, $a,b$ 均非单位, 则由**定理 3.4.9 (扭模的 $p$-分支分解)**, $Dz=Dz_1\oplus Dz_2$, 两个均非零, 矛盾. 故 $d$ 的所有不可约因子相伴, 即 $d=p^e$, $p$ 素, $e\in\mathbb N$.

充分性. 设 $M=Dz$, $\operatorname{ann}\left(z\right)=\left(p^e\right)$. $M\cong D/\left(p^e\right)$. $D/\left(p^e\right)$ 的子模与 $D$ 中包含 $\left(p^e\right)$ 的理想一一对应, 而这些理想为 $\left(p^e\right)\subset\left(p^{e-1}\right)\subset\cdots\subset\left(p\right)\subset D$, 构成一条全序链. 若 $M=N_1\oplus N_2$ 为两个非零子模直和, 则 $N_1,N_2$ 都是上述链中的非零真子模, 必两两有包含关系, 从而 $N_1\cap N_2\ne0$, 与直和矛盾. 故 $M$ 不可分解.

(注: 若允许秩为 $1$ 的自由循环模 $Dz$ 且 $\operatorname{ann}\left(z\right)=0$, 它同样不可分解, 因整环 $D$ 无非平凡理想直和分解.) $\blacksquare$

## 3.5-4

试决定同构意义下 $936$ 阶交换群的类数.

### 解答 3.5-4

先对 $936$ 作素因数分解. 因 $936=8\times117=2^3\times3^2\times13$, 即 $936=2^3\cdot3^2\cdot13^1$.

计算各指数的分划数. 指数 $3$ 的分划为 $3$, $2+1$, $1+1+1$, 共 $p\left(3\right)=3$ 种; 指数 $2$ 的分划为 $2$, $1+1$, 共 $p\left(2\right)=2$ 种; 指数 $1$ 的分划仅 $1$ 一种, 故 $p\left(1\right)=1$.

由**定理 3.5.2 (有限交换群的分类数)**, 同构意义下 $936$ 阶交换群的个数为 $p\left(3\right)p\left(2\right)p\left(1\right)=3\times2\times1=6$.

故同构意义下 $936$ 阶交换群共有 $6$ 类. $\blacksquare$

## 3.5-8

(1) 设 $G=\mathbb Z_{p^e}$, $p$ 为素数, $e> 0$. 记 $G$ 中元素 $g$ 的阶为 $o\left(g\right)$. 试证明: 若 $l\le e$, 则 $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l$; 若 $l> e$, 则 $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^e$.

(2) 设 $H_1,H_2,\cdots,H_s$ 为有限交换群, $q$ 为自然数, 令 $m_i=\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|$, $G=H_1\times H_2\times\cdots\times H_s$, 则 $\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|=m_1m_2\cdots m_s$.

(3) 试决定 $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ 中有多少个元素的阶能整除 $4$.

### 解答 3.5-8

(1) 将 $G=\mathbb Z_{p^e}$ 视为加法循环群, 其元素为 $0,1,2,\cdots,p^e-1$ 模 $p^e$. 对 $g=k\in\mathbb Z_{p^e}$, 有 $o\left(g\right)=\frac{p^e}{\gcd\left(k,p^e\right)}$. 于是 $o\left(g\right)\mid p^l$ 等价于 $p^l g=0$, 即 $p^l k\equiv0\pmod{p^e}$.

当 $l\le e$ 时, 上式等价于 $k$ 被 $p^{e-l}$ 整除. 在模 $p^e$ 的剩余类中, 被 $p^{e-l}$ 整除的剩余类恰有 $p^l$ 个, 故 $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l$.

当 $l> e$ 时, $p^l$ 是 $p^e$ 的倍数, $p^l g=0$ 对一切 $g\in G$ 自动成立, 故该集合即 $G$ 本身, 其元素个数为 $p^e$.

(2) 任取 $g=\left(h_1,h_2,\cdots,h_s\right)\in G$. 由直积中元素的阶, $o\left(g\right)\mid q$ 当且仅当 $o\left(h_i\right)\mid q$ 对每个 $i$ 同时成立. 因而满足条件的 $g$ 恰为各分量分别取自对应集合 $\left\{h\in H_i\mid o\left(h\right)\mid q\right\}$ 的直积, 由乘法原理得

$$
\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|=\prod_{i=1}^s\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|=m_1m_2\cdots m_s.
$$

(3) 在 $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ 中, 要求元素的阶整除 $4$, 即 $4g=0$. 分别计算各分量的可选个数.

对 $\mathbb Z_4$, 群阶为 $4$, 故 $4g=0$ 对所有 $4$ 个元素都成立, $m_1=4$.

对 $\mathbb Z_8$, $4k\equiv0\pmod 8$ 等价于 $k$ 为偶数, 即 $k\in\left\{0,2,4,6\right\}$, 共 $4$ 个, $m_2=4$.

对 $\mathbb Z_{16}$, $4k\equiv0\pmod{16}$ 等价于 $k\equiv0\pmod 4$, 即 $k\in\left\{0,4,8,12\right\}$, 共 $4$ 个, $m_3=4$.

由 (2), 所求元素个数为 $m_1m_2m_3=4\times4\times4=64$.

故 $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ 中有 $64$ 个元素的阶能整除 $4$. $\blacksquare$

## 3.5-12

试给出 $8$ 阶交换群的分类, 并决定所有这些群到 $\mathbb Q^*$ 的同态.

### 解答 3.5-12

因 $8=2^3$, 指数 $3$ 的分划为 $3$, $2+1$, $1+1+1$, 共 $p\left(3\right)=3$ 种. 由**定理 3.5.2 (有限交换群的分类数)**, $8$ 阶交换群在同构意义下共有 $3$ 类, 分别为 $\mathbb Z_8$, $\mathbb Z_4\times\mathbb Z_2$, $\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2$.

下面分别决定它们到 $\mathbb Q^*$ 的同态. 设 $\varphi:G\to\mathbb Q^*$ 为群同态. 因 $G$ 有限, $\varphi\left(G\right)$ 是 $\mathbb Q^*$ 的有限子群. 由有理数乘法群的有限子群, $\mathbb Q^*$ 的唯一有限子群为 $\left\{\pm1\right\}$, 故 $\varphi\left(G\right)\subseteq\left\{\pm1\right\}$, 即每个生成元的像只能取 $1$ 或 $-1$.

**情形一 $G=\mathbb Z_8$.** 设 $g$ 为 $G$ 的生成元, $o\left(g\right)=8$. 同态 $\varphi$ 由 $\varphi\left(g\right)\in\left\{\pm1\right\}$ 唯一确定, 且 $\varphi\left(g\right)^8=1$ 对 $\pm1$ 自动成立. 故共有 $2$ 个同态.

**情形二 $G=\mathbb Z_4\times\mathbb Z_2$.** 设 $g_1$ 为 $\mathbb Z_4$ 的生成元, $g_2$ 为 $\mathbb Z_2$ 的生成元. 同态由 $\varphi\left(g_1\right),\varphi\left(g_2\right)\in\left\{\pm1\right\}$ 唯一确定, 且约束 $\varphi\left(g_1\right)^4=1$, $\varphi\left(g_2\right)^2=1$ 对 $\pm1$ 自动满足. 故共有 $2\times2=4$ 个同态.

**情形三 $G=\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2$.** 设 $g_1,g_2,g_3$ 为三个 $2$ 阶生成元. 同态由 $\varphi\left(g_1\right),\varphi\left(g_2\right),\varphi\left(g_3\right)\in\left\{\pm1\right\}$ 唯一确定, 约束均自动满足. 故共有 $2^3=8$ 个同态.

综上, $8$ 阶交换群共 $3$ 类, 它们到 $\mathbb Q^*$ 的同态个数分别为 $2$, $4$, $8$. $\blacksquare$

## 3.6-9

设 $F$ 为特征为零的代数闭域, 试证明 $F$ 上任何一个约当块都能写成两个对称矩阵的乘积.

### 解答 3.6-9

设 $J$ 为 $F$ 上 $n$ 阶约当块, 其特征值为 $\lambda\in F$, 则 $J=\lambda I_n+N$, 其中 $N$ 为 $n$ 阶幂零移位矩阵.

设 $P$ 为 $n$ 阶反转矩阵. 由逆转置矩阵, $P$ 对称, $P^2=I_n$, 且 $PN$ 对称. 令 $A=PJ=\lambda P+PN$. 因 $P$ 与 $PN$ 均对称, 故 $A$ 为对称矩阵. 又 $P^2=I_n$, 故 $P^{-1}=P$, 于是 $J=P^{-1}A=PA$.

其中 $P$ 与 $A$ 均为 $F$ 上对称矩阵. 故任一约当块均可写成两个对称矩阵的乘积. $\blacksquare$

## 3.6-10

试证明任何一个特征为零的代数闭域 $F$ 上的方阵都能写成 $F$ 上两个对称矩阵的乘积.

### 解答 3.6-10

设 $A$ 为 $F$ 上 $n$ 阶方阵. 由**定理 3.6.3 (约当标准形)**, 存在可逆矩阵 $S$ 使 $S^{-1}AS=J=\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, 其中 $J_1,J_2,\cdots,J_s$ 均为约当块.

由**3.6-9** 的结论, 每个约当块 $J_i$ 可写为 $J_i=P_iQ_i$, 其中 $P_i,Q_i$ 均为对称矩阵. 令 $P=\mathrm{diag}\left(P_1,P_2,\cdots,P_s\right)$, $Q=\mathrm{diag}\left(Q_1,Q_2,\cdots,Q_s\right)$, 则 $P,Q$ 均为对称矩阵, 且 $J=PQ$.

于是 $A=SJS^{-1}=SPQS^{-1}=\left(SPS^\top\right)\left(S^{-T}QS^{-1}\right)$. 其中 $SPS^\top$ 为对称矩阵, 因其转置为 $\left(SPS^\top\right)^\top=SP^\topS^\top=SPS^\top$; 同理 $S^{-T}QS^{-1}=\left(S^{-1}\right)^\topQS^{-1}$ 亦为对称矩阵. 故 $A$ 为两个对称矩阵之积. $\blacksquare$

## 3.6-11

设 $A$ 为实线性空间 $V$ 上的线性变换, 试证明存在 $V$ 的一组基使得在这组基下 $A$ 的矩阵具有分块矩阵 $\begin{bmatrix}B_1&B_2\\0&B_3\end{bmatrix}$ 的形式, 其中 $B_1$ 为 $1$ 阶或 $2$ 阶方阵.

### 解答 3.6-11

对 $\dim V=n$ 作归纳. 当 $n=1$ 时结论显然成立. 假设维数小于 $n$ 时结论成立, 考虑 $n$ 维情形.

**情形一 $A$ 有实特征值 $\lambda$.** 取对应的实特征向量 $v_1$, 扩充为 $V$ 的一组基 $v_1,v_2,\cdots,v_n$. 因 $v_1$ 生成的一维子空间是 $A$-不变子空间, $A$ 在该基下的矩阵形如 $\begin{bmatrix}\lambda&*\\0&A'\end{bmatrix}$, 其中 $\lambda$ 为 $1$ 阶块, $A'$ 为 $n-1$ 阶实矩阵. 由归纳假设, $A'$ 可相似于所要求的分块上三角形式, 从而 $A$ 亦然.

**情形二 $A$ 无实特征值.** 此时 $A$ 的特征多项式在 $\mathbb R\left[x\right]$ 上没有一次因式, 故可分解为若干个判别式小于零的二次不可约多项式之积. 取其中一个 $p\left(x\right)=x^2+bx+c$, $b^2-4c< 0$.

由主理想整环 $\mathbb R\left[x\right]$ 上有限生成扭模的结构理论 (即 $V$ 作为 $\mathbb R\left[x\right]$-模的准素分解), $p\left(x\right)$ 对应的准素子空间非零. 取其中向量 $u$ 使得 $p\left(A\right)u=0$ 且 $u\ne0$. 因 $p\left(x\right)$ 无实根, $u$ 与 $Au$ 必线性无关 (否则 $Au=au$, $a\in\mathbb R$, 则 $a$ 为 $p$ 的实根, 矛盾). 令 $W=\mathrm{span}\left\{u,Au\right\}$. 由 $p\left(A\right)u=0$ 即 $A^2u+bAu+cu=0$ 得 $A\left(Au\right)=A^2u=-cu-bAu\in W$, 故 $W$ 是 $2$ 维 $A$-不变子空间. 取 $W$ 的一组基, 扩充为 $V$ 的一组基, 则 $A$ 在该基下的矩阵形如 $\begin{bmatrix}B_1&B_2\\0&A'\end{bmatrix}$, 其中 $B_1$ 为 $2$ 阶方阵 ($A$ 在 $W$ 上的限制), $A'$ 为 $n-2$ 阶实矩阵. 由归纳假设, $A'$ 可化为所要求的分块上三角形式, 从而 $A$ 亦然.

综上, 由归纳法, 存在 $V$ 的一组基使 $A$ 的矩阵为所要求的分块上三角形式. $\blacksquare$

## 3.6-12

(韦尔定理) 试证明特征为零的代数闭域上两个 $n\times n$ 矩阵 $A,B$ 相似当且仅当对任何 $a\in F$ 及 $k\in\mathbb N$, $\left(aI_n-A\right)^k$ 与 $\left(aI_n-B\right)^k$ 具有相同的秩.

### 解答 3.6-12

**必要性.** 若 $A$ 与 $B$ 相似, 则存在可逆矩阵 $P$ 使 $B=P^{-1}AP$. 于是 $\left(aI_n-B\right)^k=\left(aI_n-P^{-1}AP\right)^k=P^{-1}\left(aI_n-A\right)^kP$. 相似矩阵秩相同, 故 $\mathrm{rank}\left(aI_n-A\right)^k=\mathrm{rank}\left(aI_n-B\right)^k$.

**充分性.** 设对任何 $a\in F$ 及 $k\in\mathbb N$, 两矩阵相应幂的秩相同. 由**定理 3.6.3 (约当标准形)**, $A,B$ 均相似于其约当标准形, 只需证明二者约当标准形相同.

对任一 $a\in F$, 记 $\nu_k\left(A\right)=\dim\ker\left(aI_n-A\right)^k=n-\mathrm{rank}\left(aI_n-A\right)^k$, 并约定 $\nu_0\left(A\right)=0$. 由题设, $\nu_k\left(A\right)=\nu_k\left(B\right)$ 对所有 $k$ 成立. 由幂零核与约当块计数, $A$ 的以 $a$ 为特征值, 阶数不小于 $s$ 的约当块个数为 $\nu_s\left(A\right)-\nu_{s-1}\left(A\right)$, $B$ 同理. 故二者在 $a$ 处的约当块大小与个数完全一致.

由于 $F$ 是代数闭域, $A,B$ 的全部特征值均在 $F$ 中, 上述结论对每个特征值 $a$ 成立. 因而 $A$ 与 $B$ 的约当标准形完全相同, 从而 $A$ 与 $B$ 相似. $\blacksquare$
