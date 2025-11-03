# week9

> **定理 3.1.10 (直和判据)**
> 
> 设 $M_1,\cdots,M_s$ 为 $R$-模 $M$ 的子模, 则 $M=M_1\oplus\cdots\oplus{M}_s$ 当且仅当: (1) $M=M_1+\cdots+M_s$; (2) 对任何 $2\le{j}\le{s}$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

> **命题 3.1.16 (同态的核与像)**
> 
> 模同态 $\phi:M_1\to{M}_2$ 的核 $\ker\phi$ 是 $M_1$ 的子模, 同态像 $\operatorname{Im}\phi$ 是 $M_2$ 的子模.

> **定理 3.1.17 (模的同态基本定理)**
> 
> 设 $\phi$ 为模 $M_1$ 到 $M_2$ 的满同态, 则商模 $M_1/\ker\phi$ 与 $M_2$ 同构; 且若 $N_1$ 是 $M_1$ 的包含 $\ker\phi$ 的子模, 则 $M_1/N_1\cong{M}_2/\phi\left(N_1\right)$.

> **定理 3.3.6 (自由模基的刻画)**
> 
> 设 $M$ 为幺环 $R$ 上的模, $u_1,\cdots,u_m$ 为 $M$ 中元素, 则 $M$ 为自由模且 $u_1,\cdots,u_m$ 为一组基当且仅当: (1) $u_1,\cdots,u_m$ 是 $M$ 的一组生成元; (2) $u_1,\cdots,u_m$ 线性无关.

> **定理 3.4.5 (主理想整环上有限生成模的结构定理)**
> 
> 主理想整环 $D$ 上的任何有限生成模 $M$ 都有分解 $M=Dy_1\oplus\cdots\oplus{D}y_s$, 其中 $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$, 且 $y_j\ne0$. 其中非零零化子对应的 $d_i$ ($\operatorname{ann}\left(y_i\right)=\left(d_i\right)$) 称为不变因子, 其分解为不可约元素幂次者称为初等因子.

> **推论 3.4.12 (有限生成模的同构判定)**
> 
> 设 $M_1,M_2$ 为主理想整环 $D$ 上的有限生成模, 则 $M_1\cong{M}_2$ 当且仅当它们有相同的秩和不变因子, 当且仅当有相同的秩和初等因子.

## 3.1-12

设 $M$ 为模, $M_1,M_2$ 是 $M$ 的子模, 试证明 $\left(M_1+M_2\right)/M_2\cong{M}_1/\left(M_1\cap{M}_2\right)$.

### 解答 3.1-12

取商映射 $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$, 限制到 $M_1$ 上得到 $\phi=\rho|_{M_1}:M_1\to\left(M_1+M_2\right)/M_2$. 先证 $\phi$ 是满同态. 任一形如 $m_1+m_2+M_2$ 的陪集等于 $m_1+M_2$, 即 $\phi\left(m_1\right)$, 故 $\phi$ 满.

再求核. 由**命题 3.1.16 (同态的核与像)**, $\ker\phi=\left\{m_1\in{M}_1\mid{m}_1\in{M}_2\right\}=M_1\cap{M}_2$. 由**定理 3.1.17 (模的同态基本定理)**,

$$
M_1/\ker\phi=M_1/\left(M_1\cap{M}_2\right)\cong\left(M_1+M_2\right)/M_2.
$$

此即第二同构定理.

$\blacksquare$

## 3.1-13

设 $M$ 为模, $M_1,M_2,\cdots,M_s$ 为 $M$ 的子模. 试证明 $M=M_1\oplus\cdots\oplus{M}_s$ 当且仅当:

(1) $M=M_1+M_2+\cdots+M_s$;

(2) 对任何 $2\le{j}\le{s}$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

### 解答 3.1-13

必要性. 设 $M=M_1\oplus\cdots\oplus{M}_s$ 为内直和, 则 (1) 显然. 若 $x\in{M}_j\cap\left(M_1+\cdots+M_{j-1}\right)$, 则 $x$ 既可写成 $M_j$ 中元素, 又可写成 $M_1,\cdots,M_{j-1}$ 中元素之和, 这给出 $0$ 的一个非平凡表示 (除 $M_j$ 分量外其余分量和为 $-x$), 与直和分解的唯一性矛盾. 故 $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

充分性. 设 (1)(2) 成立. 只需证 $M$ 中零元素的表示唯一. 设 $m_1+m_2+\cdots+m_s=0$, $m_i\in{M}_i$. 设 $j$ 为最大的使 $m_j\ne0$ 的下标, 则 $j\ge2$ (否则 $m_1=0$). 移项得 $m_j=-\left(m_1+\cdots+m_{j-1}\right)\in{M}_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$, 故 $m_j=0$, 矛盾. 因此所有 $m_i=0$, 零元素表示唯一. 由**定理 3.1.10 (直和判据)**, $M=M_1\oplus\cdots\oplus{M}_s$.

$\blacksquare$

## 3.1-14

试问将上题的条件 (2) 改为 $M_i\cap{M}_j=\left\{0\right\}$, $\forall{i}\ne{j}$, 结论还成立吗? 说明理由.

### 解答 3.1-14

结论不成立. 两两交为零不能保证内直和分解.

反例. 取数域 $\mathbb{R}$ 上二维线性空间 $M=\mathbb{R}^2$ 作为 $\mathbb{R}$-模, 基为 $e_1,e_2$. 令 $M_1=\mathbb{R}e_1$, $M_2=\mathbb{R}e_2$, $M_3=\mathbb{R}\left(e_1+e_2\right)$. 它们都是 $M$ 的一维子空间. 任意两个不同的一维子空间之交为零, 即 $M_i\cap{M}_j=\left\{0\right\}$, $i\ne{j}$. 且 $M_1+M_2+M_3=\mathbb{R}e_1+\mathbb{R}e_2=M$, 即条件 (1) 成立. 但存在非平凡关系 $e_1+e_2-\left(e_1+e_2\right)=0$, 其中 $e_1\in{M}_1$, $e_2\in{M}_2$, $-\left(e_1+e_2\right)\in{M}_3$, 三项均非零, 故零元素表示不唯一, $M\ne{M}_1\oplus{M}_2\oplus{M}_3$.

因此两两交为零只是直和的必要条件而非充分条件, 不能替代上题的嵌套交条件.

$\blacksquare$

## 3.1-15

设 $M$ 为模, $M_1,M_2,\cdots,M_s$ 为 $M$ 的子模, 且 $M=M_1\oplus{M}_2\oplus\cdots\oplus{M}_s$, 又 $N$ 是 $M$ 的子模, 且 $N=N_1\oplus{N}_2\oplus\cdots\oplus{N}_s$, 其中 $N_i\subset{M}_i$, $i=1,2,\cdots,s$. 试证明 $M/N\cong{M}_1/N_1\oplus{M}_2/N_2\oplus\cdots\oplus{M}_s/N_s$.

### 解答 3.1-15

任一 $m\in{M}$ 可唯一写成 $m=m_1+\cdots+m_s$, $m_i\in{M}_i$. 定义映射 $\phi:M\to{M}_1/N_1\oplus\cdots\oplus{M}_s/N_s$, $\phi\left(m_1+\cdots+m_s\right)=\left(m_1+N_1,\cdots,m_s+N_s\right)$. 由直和分解的唯一性, $\phi$ 是良定义的模同态.

它是满同态: 任取 $\left(m_1'+N_1,\cdots,m_s'+N_s\right)$, 取 $m=m_1'+\cdots+m_s'\in{M}$, 则 $\phi\left(m\right)$ 即为该元素.

求核. 由**命题 3.1.16 (同态的核与像)**,

$$
\ker\phi=\left\{m_1+\cdots+m_s\mid{m}_i+N_i=0,1\le{i}\le{s}\right\}=\left\{m_1+\cdots+m_s\mid{m}_i\in{N}_i\right\}=N_1\oplus\cdots\oplus{N}_s=N.
$$

由**定理 3.1.17 (模的同态基本定理)**,

$$
M/N=M/\ker\phi\cong{M}_1/N_1\oplus{M}_2/N_2\oplus\cdots\oplus{M}_s/N_s.
$$

$\blacksquare$

## 3.3-6

设 $R$ 为交换幺环, 而且任何有限生成的 $R$-模都是自由模, 证明 $R$ 为一个域.

### 解答 3.3-6

只需证明 $R$ 中每个非零元都是单位. 任取 $a\in{R}$, $a\ne0$. 考虑商模 $R/\left(a\right)$, 它由 $\overline1=1+\left(a\right)$ 生成, 因而是有限生成 $R$-模. 由题设, $R/\left(a\right)$ 是自由模.

断言 $R/\left(a\right)=0$. 否则它是非零自由模, 而 $\overline1$ 是它的生成元. 由**定理 3.3.6 (自由模基的刻画)**, 若 $\left\{\overline1\right\}$ 为一组基, 则其零化子为零, 即 $r\overline1=0\Rightarrow{r}=0$. 但 $a\overline1=a+\left(a\right)=0$, 且 $a\ne0$, 矛盾. 故 $R/\left(a\right)=0$.

$R/\left(a\right)=0$ 等价于 $\left(a\right)=R$, 即 $1\in\left(a\right)$, 亦即存在 $b\in{R}$ 使 $ab=1$. 故 $a$ 是单位.

由 $a\ne0$ 的任意性, $R$ 的每个非零元都是单位, 故 $R$ 是一个域.

$\blacksquare$

## 3.3-7

设 $R$ 为交换幺环, $\phi$ 为自由模 $R^m$ 的自同态, 试证明: 如果 $\phi$ 为满同态, 则 $\phi$ 为同构.

### 解答 3.3-7

取 $R^m$ 的一组标准基 $e_1,\cdots,e_m$, 设自同态 $\phi$ 在这组基下的矩阵为 $A\in{R}^{m\times{m}}$.

因 $\phi$ 是满同态, 对每个基向量 $e_j\in{R}^m$, 存在 $x_j\in{R}^m$ 使 $\phi\left(x_j\right)=e_j$. 将 $x_1,\cdots,x_m$ 作为列向量排成矩阵 $B$, 则 $AB=I_m$, 其中 $I_m$ 为 $m$ 阶单位矩阵. 两边取行列式, 由行列式乘性, $\det\left(A\right)\det\left(B\right)=\det\left(I_m\right)=1$.

故 $\det{A}$ 是 $R$ 中的单位. 由行列式与可逆性, $A$ 可逆, 即存在 $A^{-1}$ 使 $AA^{-1}=I_m$. 因而 $\phi$ 既是满同态又是单同态 ($\ker\phi=0$), 是双射, 故 $\phi$ 为模同构.

$\blacksquare$

## 3.3-8

条件同上题, 如果 $R$ 是域且 $\phi$ 是单同态, 证明 $\phi$ 是同构. 这个结论对于一般的交换幺环成立吗?

### 解答 3.3-8

当 $R$ 是域时, $R^m$ 是 $m$ 维线性空间. $\phi$ 是单同态意味着线性变换 $\phi$ 的核为零子空间. 由线性代数, 有限维线性空间上的单线性变换必为满射, 从而为同构. 也可由矩阵看: 单同态对应矩阵 $A$ 的列线性无关, 即 $\operatorname{rank}A=m$, 故方阵 $A$ 满秩, 可逆, $\phi$ 为同构.

这个结论对于一般的交换幺环不成立.

反例. 取 $R=\mathbb{Z}$ (交换幺环), $m=1$, 定义 $\phi:\mathbb{Z}\to\mathbb{Z}$ 为 $\phi\left(n\right)=2n$. $\phi$ 是 $\mathbb{Z}$ 上的自同态. 它是单同态: 若 $2n=0$, 在整环 $\mathbb{Z}$ 中 $n=0$. 但它不是满同态: $1\notin2\mathbb{Z}$, 即不存在 $n$ 使 $2n=1$. 故 $\phi$ 是单同态却不双射, 不是同构.

因此一般交换幺环上自由模的单自同态未必是同构.

$\blacksquare$
