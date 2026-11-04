# week10

> **定理 2.7.7 (贝祖等式)**
> 
> 设 $R$ 为主理想整环, $a,b\in R$, $d$ 为 $a,b$ 的一个最大公因子, 则存在 $u,v\in R$ 使 $d=ua+vb$.

> **定理 3.1.10 (直和判据)**
> 
> 设 $M_1,\cdots,M_s$ 为 $R$-模 $M$ 的子模, 则 $M=M_1\oplus\cdots\oplus M_s$ 当且仅当: (1) $M=M_1+\cdots+M_s$; (2) 对任何 $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

> **命题 3.1.16 (同态的核与像)**
> 
> 模同态 $\phi:M_1\to M_2$ 的核 $\ker\phi$ 是 $M_1$ 的子模, 同态像 $\operatorname{Im}\phi$ 是 $M_2$ 的子模.

> **定理 3.1.17 (模的同态基本定理)**
> 
> 设 $\phi$ 为模 $M_1$ 到 $M_2$ 的满同态, 则商模 $M_1/\ker\phi$ 与 $M_2$ 同构; 且若 $N_1$ 是 $M_1$ 的包含 $\ker\phi$ 的子模, 则 $M_1/N_1\cong M_2/\phi\left(N_1\right)$.

> **定理 3.3.6 (自由模基的刻画)**
> 
> 设 $M$ 为幺环 $R$ 上的模, $u_1,\cdots,u_m$ 为 $M$ 中元素, 则 $M$ 为自由模且 $u_1,\cdots,u_m$ 为一组基当且仅当: (1) $u_1,\cdots,u_m$ 是 $M$ 的一组生成元; (2) $u_1,\cdots,u_m$ 线性无关.

> **定理 3.4.5 (主理想整环上有限生成模的结构定理)**
> 
> 主理想整环 $D$ 上的任何有限生成模 $M$ 都有分解 $M=Dy_1\oplus\cdots\oplus Dy_s$, 其中 $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$, 且 $y_j\ne0$. 其中非零零化子对应的 $d_i$ ($\operatorname{ann}\left(y_i\right)=\left(d_i\right)$) 称为不变因子, 其分解为不可约元素幂次者称为初等因子.

> **定理 3.4.9 (扭模的 $p$-分支分解)**
> 
> 设 $M$ 为主理想整环 $D$ 上有限生成扭模, 则存在有限个互不相伴的不可约元素 $p_1,\cdots,p_m$ 使 $M=M_{p_1}\oplus\cdots\oplus M_{p_m}$, 其中 $M_p=\left\{x\in M\mid \exists e,p^ex=0\right\}$ 为 $p$-分支. 特别地, 若 $\operatorname{ann}\left(y\right)=\left(ab\right)$ 且 $a,b$ 互素, 则 $Dy=Dy_1\oplus Dy_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$.

> **推论 3.4.12 (有限生成模的同构判定)**
> 
> 设 $M_1,M_2$ 为主理想整环 $D$ 上的有限生成模, 则 $M_1\cong M_2$ 当且仅当它们有相同的秩和不变因子, 当且仅当有相同的秩和初等因子.

## 2.9-3

设 $R$ 是整环, $f\left(x\right)\in R\left[x\right]$, 则 $a\in R$ 为 $f\left(x\right)$ 的根当且仅当 $\left(x-a\right)$ 整除 $f\left(x\right)$.

### 解答 2.9-3

对 $f\left(x\right)$ 与首一多项式 $x-a$ 作带余除法, 由多项式带余除法, 存在 $q\left(x\right)\in R\left[x\right]$ 及常数 $c\in R$ 使 $f\left(x\right)=q\left(x\right)\left(x-a\right)+c$, 其中余式次数小于 $1$, 故为常数. 将 $x=a$ 代入, 注意 $a\in R$ 可与 $R\left[x\right]$ 中元素作求值同态, 得 $f\left(a\right)=q\left(a\right)\cdot0+c=c$.

于是 $a$ 为 $f\left(x\right)$ 的根, 即 $f\left(a\right)=0$, 当且仅当 $c=0$, 当且仅当 $f\left(x\right)=q\left(x\right)\left(x-a\right)$, 即 $\left(x-a\right)\mid f\left(x\right)$. $\blacksquare$

## 2.9-4

设 $R$ 是整环, $f\left(x\right)\in R\left[x\right]$, $a_1,a_2,\cdots,a_s$ 为 $f\left(x\right)$ 的不同的根, 则 $\left(x-a_1\right)\left(x-a_2\right)\cdots\left(x-a_s\right)$ 整除 $f\left(x\right)$. 由此证明整环上次数为 $m$ 的非零多项式的不同根的个数最多为 $m$.

### 解答 2.9-4

对 $s$ 作归纳. 当 $s=1$ 时, 即**2.9-3** 的结论.

设结论对 $s-1$ 成立, 即 $\prod_{i=1}^{s-1}\left(x-a_i\right)\mid f\left(x\right)$. 写 $f\left(x\right)=g\left(x\right)\prod_{i=1}^{s-1}\left(x-a_i\right)$. 将 $x=a_s$ 代入, 因 $a_s$ 是 $f$ 的根, $f\left(a_s\right)=0$, 故 $0=g\left(a_s\right)\prod_{i=1}^{s-1}\left(a_s-a_i\right)$.

由于 $a_1,\cdots,a_s$ 两两不同, $a_s-a_i\ne0$ ($1\le i\le s-1$). 又 $R$ 是整环, 无零因子, 故 $g\left(a_s\right)=0$. 由**2.9-3**, $\left(x-a_s\right)\mid g\left(x\right)$, 记 $g\left(x\right)=h\left(x\right)\left(x-a_s\right)$. 于是 $f\left(x\right)=h\left(x\right)\prod_{i=1}^{s}\left(x-a_i\right)$, 即 $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. 归纳完成.

现设 $f\left(x\right)\ne0$ 次数为 $m$, 有 $s$ 个不同根 $a_1,\cdots,a_s$. 由上, $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. 该乘积为 $s$ 次多项式, 它整除 $m$ 次多项式, 故次数 $s\le m$. 即整环上次数为 $m$ 的非零多项式的不同根的个数最多为 $m$. $\blacksquare$

## 2.9-11

试证明实数域 $\mathbb R$ 上的形式幂级数环 $\mathbb R\left[\!\left[t\right]\!\right]$ 是一个唯一分解整环.

### 解答 2.9-11

记 $R=\mathbb R\left[\!\left[t\right]\!\right]$. 任取非零幂级数 $f\left(t\right)=\sum_{n=0}^{\infty}a_nt^n\in R$. 设 $a_k$ 为其第一个非零系数, 即 $a_0=\cdots=a_{k-1}=0$, $a_k\ne0$, 称 $k$ 为 $f$ 的阶, 记 $\operatorname{ord}\left(f\right)=k$. 则 $f\left(t\right)=t^k\cdot\left(a_k+a_{k+1}t+\cdots\right)=t^k\,u\left(t\right)$, 其中 $u\left(t\right)=a_k+a_{k+1}t+\cdots$ 的常数项 $a_k\ne0$. 由形式幂级数环, $u\left(t\right)$ 是单位 (常数项非零即可逆).

先确定 $R$ 的不可约元素. 若 $f$ 非零非单位, 则 $k=\operatorname{ord}\left(f\right)\ge1$, $f=t^ku$. 若 $k=1$, $f=t\,u$, $u$ 为单位, 故 $f$ 与 $t$ 相伴. 而 $t$ 不可约: 若 $t=\alpha\beta$, 则 $1=\operatorname{ord}\left(t\right)=\operatorname{ord}\left(\alpha\right)+\operatorname{ord}\left(\beta\right)$, 故 $\operatorname{ord}\left(\alpha\right),\operatorname{ord}\left(\beta\right)$ 中一个为 $0$ 另一个为 $1$, 即其中一个为单位. 故 $t$ 不可约.

于是任何非零非单位元素 $f$ 都可写成 $f=t^k\,u$, $u$ 为单位, 其中 $k=\operatorname{ord}\left(f\right)$ 被 $f$ 唯一确定. 即 $f$ 在相伴意义下唯一分解为不可约元素 $t$ 的 $k$ 次幂乘以单位. 又 $t$ 是素元素: $t\mid fg\Rightarrow\operatorname{ord}\left(fg\right)\ge1\Rightarrow\operatorname{ord}\left(f\right)\ge1$ 或 $\operatorname{ord}\left(g\right)\ge1$, 即 $t\mid f$ 或 $t\mid g$.

由唯一分解整环 的定义, $R=\mathbb R\left[\!\left[t\right]\!\right]$ 是唯一分解整环. $\blacksquare$

## 3.1-11

设 $M$ 为模, $M_1,M_2$ 都是 $M$ 的子模. 试证明:

(1) 若 $M_1\subset M_2$, 则 $M/M_2\cong\left(M/M_1\right)/\left(M_2/M_1\right)$;

(2) 如果 $M=M_1\oplus M_2$, 则有 $M_1\cong\left(M_1+M_2\right)/M_2$, $M_2\cong\left(M_1+M_2\right)/M_1$.

### 解答 3.1-11

(1) 定义映射 $\pi:M/M_1\to M/M_2$ 为 $\pi\left(m+M_1\right)=m+M_2$. 它是良定义的: 若 $m+M_1=m'+M_1$, 则 $m-m'\in M_1\subset M_2$, 故 $m+M_2=m'+M_2$. 它显然是模满同态. 求其核: $\ker\pi=\left\{m+M_1\mid m\in M_2\right\}=M_2/M_1$. 由**定理 3.1.17 (模的同态基本定理)**,

$$
\left(M/M_1\right)/\left(M_2/M_1\right)=M/\ker\pi\cong\operatorname{Im}\pi=M/M_2.
$$

(2) 考虑商映射 $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$ 在子模 $M_1$ 上的限制 $\rho|_{M_1}$. 它是满同态: 任一元素 $m_1+m_2+M_2=m_1+M_2$ 都是 $m_1\in M_1$ 的像. 其核为 $\ker\rho|_{M_1}=\left\{m_1\in M_1\mid m_1\in M_2\right\}=M_1\cap M_2$. 因 $M=M_1\oplus M_2$ 为内直和, 由**定理 3.1.10 (直和判据)**, $M_1\cap M_2=\left\{0\right\}$. 再由**定理 3.1.17 (模的同态基本定理)**,

$$
M_1/\left(M_1\cap M_2\right)=M_1\cong\left(M_1+M_2\right)/M_2.
$$

同理, $M_2\cong\left(M_1+M_2\right)/M_1$. $\blacksquare$

## 3.1-12

设 $M$ 为模, $M_1,M_2$ 是 $M$ 的子模, 试证明 $\left(M_1+M_2\right)/M_2\cong M_1/\left(M_1\cap M_2\right)$.

### 解答 3.1-12

取商映射 $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$, 限制到 $M_1$ 上得到 $\phi=\rho|_{M_1}:M_1\to\left(M_1+M_2\right)/M_2$. 先证 $\phi$ 是满同态. 任一形如 $m_1+m_2+M_2$ 的陪集等于 $m_1+M_2$, 即 $\phi\left(m_1\right)$, 故 $\phi$ 满.

再求核. 由**命题 3.1.16 (同态的核与像)**, $\ker\phi=\left\{m_1\in M_1\mid m_1\in M_2\right\}=M_1\cap M_2$. 由**定理 3.1.17 (模的同态基本定理)**,

$$
M_1/\ker\phi=M_1/\left(M_1\cap M_2\right)\cong\left(M_1+M_2\right)/M_2.
$$

此即第二同构定理. $\blacksquare$

## 3.1-13

设 $M$ 为模, $M_1,M_2,\cdots,M_s$ 为 $M$ 的子模. 试证明 $M=M_1\oplus\cdots\oplus M_s$ 当且仅当:

(1) $M=M_1+M_2+\cdots+M_s$;

(2) 对任何 $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

### 解答 3.1-13

**必要性.** 设 $M=M_1\oplus\cdots\oplus M_s$ 为内直和, 则 (1) 显然. 若 $x\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)$, 则 $x$ 既可写成 $M_j$ 中元素, 又可写成 $M_1,\cdots,M_{j-1}$ 中元素之和, 这给出 $0$ 的一个非平凡表示 (除 $M_j$ 分量外其余分量和为 $-x$), 与直和分解的唯一性矛盾. 故 $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

**充分性.** 设 (1)(2) 成立. 只需证 $M$ 中零元素的表示唯一. 设 $m_1+m_2+\cdots+m_s=0$, $m_i\in M_i$. 设 $j$ 为最大的使 $m_j\ne0$ 的下标, 则 $j\ge2$ (否则 $m_1=0$). 移项得 $m_j=-\left(m_1+\cdots+m_{j-1}\right)\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$, 故 $m_j=0$, 矛盾. 因此所有 $m_i=0$, 零元素表示唯一. 由**定理 3.1.10 (直和判据)**, $M=M_1\oplus\cdots\oplus M_s$. $\blacksquare$

## 3.1-14

试问将上题的条件 (2) 改为 $M_i\cap M_j=\left\{0\right\}$, $\forall i\ne j$, 结论还成立吗? 说明理由.

### 解答 3.1-14

结论不成立. 两两交为零不能保证内直和分解.

反例. 取数域 $\mathbb R$ 上二维线性空间 $M=\mathbb R^2$ 作为 $\mathbb R$-模, 基为 $e_1,e_2$. 令 $M_1=\mathbb R e_1$, $M_2=\mathbb R e_2$, $M_3=\mathbb R\left(e_1+e_2\right)$. 它们都是 $M$ 的一维子空间. 任意两个不同的一维子空间之交为零, 即 $M_i\cap M_j=\left\{0\right\}$, $i\ne j$. 且 $M_1+M_2+M_3=\mathbb R e_1+\mathbb R e_2=M$, 即条件 (1) 成立. 但存在非平凡关系 $e_1+e_2-\left(e_1+e_2\right)=0$, 其中 $e_1\in M_1$, $e_2\in M_2$, $-\left(e_1+e_2\right)\in M_3$, 三项均非零, 故零元素表示不唯一, $M\ne M_1\oplus M_2\oplus M_3$.

因此两两交为零只是直和的必要条件而非充分条件, 不能替代上题的嵌套交条件. $\blacksquare$

## 3.1-15

设 $M$ 为模, $M_1,M_2,\cdots,M_s$ 为 $M$ 的子模, 且 $M=M_1\oplus M_2\oplus\cdots\oplus M_s$, 又 $N$ 是 $M$ 的子模, 且 $N=N_1\oplus N_2\oplus\cdots\oplus N_s$, 其中 $N_i\subset M_i$, $i=1,2,\cdots,s$. 试证明 $M/N\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s$.

### 解答 3.1-15

任一 $m\in M$ 可唯一写成 $m=m_1+\cdots+m_s$, $m_i\in M_i$. 定义映射 $\phi:M\to M_1/N_1\oplus\cdots\oplus M_s/N_s$, $\phi\left(m_1+\cdots+m_s\right)=\left(m_1+N_1,\cdots,m_s+N_s\right)$. 由直和分解的唯一性, $\phi$ 是良定义的模同态.

它是满同态: 任取 $\left(m_1'+N_1,\cdots,m_s'+N_s\right)$, 取 $m=m_1'+\cdots+m_s'\in M$, 则 $\phi\left(m\right)$ 即为该元素.

求核. 由**命题 3.1.16 (同态的核与像)**,

$$
\ker\phi=\left\{m_1+\cdots+m_s\mid m_i+N_i=0,1\le i\le s\right\}=\left\{m_1+\cdots+m_s\mid m_i\in N_i\right\}=N_1\oplus\cdots\oplus N_s=N.
$$

由**定理 3.1.17 (模的同态基本定理)**,

$$
M/N=M/\ker\phi\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s.
$$

$\blacksquare$

## 3.3-6

设 $R$ 为交换幺环, 而且任何有限生成的 $R$-模都是自由模, 证明 $R$ 为一个域.

### 解答 3.3-6

只需证明 $R$ 中每个非零元都是单位. 任取 $a\in R$, $a\ne0$. 考虑商模 $R/\left(a\right)$, 它由 $\overline 1=1+\left(a\right)$ 生成, 因而是有限生成 $R$-模. 由题设, $R/\left(a\right)$ 是自由模.

断言 $R/\left(a\right)=0$. 否则它是非零自由模, 而 $\overline 1$ 是它的生成元. 由**定理 3.3.6 (自由模基的刻画)**, 若 $\left\{\overline 1\right\}$ 为一组基, 则其零化子为零, 即 $r\overline 1=0\Rightarrow r=0$. 但 $a\overline 1=a+\left(a\right)=0$, 且 $a\ne0$, 矛盾. 故 $R/\left(a\right)=0$.

$R/\left(a\right)=0$ 等价于 $\left(a\right)=R$, 即 $1\in\left(a\right)$, 亦即存在 $b\in R$ 使 $ab=1$. 故 $a$ 是单位.

由 $a\ne0$ 的任意性, $R$ 的每个非零元都是单位, 故 $R$ 是一个域. $\blacksquare$

## 3.3-7

设 $R$ 为交换幺环, $\phi$ 为自由模 $R^m$ 的自同态, 试证明: 如果 $\phi$ 为满同态, 则 $\phi$ 为同构.

### 解答 3.3-7

取 $R^m$ 的一组标准基 $e_1,\cdots,e_m$, 设自同态 $\phi$ 在这组基下的矩阵为 $A\in R^{m\times m}$.

因 $\phi$ 是满同态, 对每个基向量 $e_j\in R^m$, 存在 $x_j\in R^m$ 使 $\phi\left(x_j\right)=e_j$. 将 $x_1,\cdots,x_m$ 作为列向量排成矩阵 $B$, 则 $AB=I_m$, 其中 $I_m$ 为 $m$ 阶单位矩阵. 两边取行列式, 由行列式乘性, $\det\left(A\right)\det\left(B\right)=\det\left(I_m\right)=1$.

故 $\det A$ 是 $R$ 中的单位. 由行列式与可逆性, $A$ 可逆, 即存在 $A^{-1}$ 使 $AA^{-1}=I_m$. 因而 $\phi$ 既是满同态又是单同态 ($\ker\phi=0$), 是双射, 故 $\phi$ 为模同构. $\blacksquare$

## 3.3-8

条件同上题, 如果 $R$ 是域且 $\phi$ 是单同态, 证明 $\phi$ 是同构. 这个结论对于一般的交换幺环成立吗?

### 解答 3.3-8

当 $R$ 是域时, $R^m$ 是 $m$ 维线性空间. $\phi$ 是单同态意味着线性变换 $\phi$ 的核为零子空间. 由线性代数, 有限维线性空间上的单线性变换必为满射, 从而为同构. 也可由矩阵看: 单同态对应矩阵 $A$ 的列线性无关, 即 $\operatorname{rank}A=m$, 故方阵 $A$ 满秩, 可逆, $\phi$ 为同构.

这个结论对于一般的交换幺环不成立.

反例. 取 $R=\mathbb Z$ (交换幺环), $m=1$, 定义 $\phi:\mathbb Z\to\mathbb Z$ 为 $\phi\left(n\right)=2n$. $\phi$ 是 $\mathbb Z$ 上的自同态. 它是单同态: 若 $2n=0$, 在整环 $\mathbb Z$ 中 $n=0$. 但它不是满同态: $1\notin 2\mathbb Z$, 即不存在 $n$ 使 $2n=1$. 故 $\phi$ 是单同态却不双射, 不是同构.

因此一般交换幺环上自由模的单自同态未必是同构. $\blacksquare$

## 3.4-4

设 $R=\mathbb Z\left[\alpha\right]$, 试构造一个有限生成的 $R$-模 $M$, 使得 $M$ 不能写成有限个循环子模的直和. (题面原文丢失了对 $\alpha$ 的条件, 这里按标准取 $\alpha$ 为不定元, 即 $R=\mathbb Z\left[x\right]$, 它不是主理想整环.)

### 解答 3.4-4

取 $R=\mathbb Z\left[x\right]$, 其中 $\alpha=x$ 为不定元. $R$ 不是主理想整环: 理想 $I=\left(2,x\right)$ 不由单个元素生成.

现在把理想 $I$ 本身看作一个 $R$-模. 它由 $2$ 和 $x$ 生成, 因而是有限生成 $R$-模. 下证 $I$ 不能写成有限个循环子模的直和.

反证. 若 $I=N_1\oplus\cdots\oplus N_k$, 每个 $N_j$ 是循环子模, 记 $N_j=Ry_j$. 由于 $I$ 是整环 $R$ 的理想, $I$ 作为 $R$-模无挠 (若 $r\in R$ 非零, $a\in I$ 非零, 则 $ra\ne0$). 故每个循环模 $Ry_j\cong R/\operatorname{ann}\left(y_j\right)$ 中 $\operatorname{ann}\left(y_j\right)=0$, 即 $N_j\cong R$. 于是 $I\cong R^k$.

再看秩. 作张量积到分式域 $\mathbb Q\left(x\right)$ 上, $I\otimes_R\mathbb Q\left(x\right)=\mathbb Q\left(x\right)$, 秩为 $1$. 故 $k=1$, 即 $I\cong R$, 从而 $I$ 是主理想, $I=\left(g\right)$.

但 $I=\left(2,x\right)$ 不是主理想: $R=\mathbb Z\left[x\right]$ 的单位只有 $\pm1$, 若 $I=\left(g\right)$, 则 $2=gf$, $x=gh$. 由 $2=gf$ 知 $f,g$ 只能是常数 $\pm1,\pm2$; 结合 $x=gh$ 不可能 ($x$ 不能整除 $2$). 更直接地, $I$ 中每个元素 $2f+xg$ 的常数项都是偶数, 故 $1\notin I$, 因而 $I\ne R=\left(1\right)$, 也不可能由 $\pm2$ 或 $x$ 单独生成.

矛盾. 故 $I$ 不能写成有限个循环子模的直和. 这与**定理 3.4.5 (主理想整环上有限生成模的结构定理)** 仅在主理想整环上成立相吻合: 脱离主理想整环前提, 有限生成模一般不能分解为循环子模的直和. $\blacksquare$

## 3.4-5

设 $D=\mathbb Z\left[i\right]$ (高斯整数环, 是主理想整环), $K$ 为 $D^3$ 中由向量 $\left(2-3i,6+9i,-18i\right)$ 生成的子模, 试求出 $D^3/K$ 的不变因子和初等因子. (题面原文开头残缺, 按数学上成立的理解补全为上述形式; 其中 $i=\sqrt{-1}$.)

### 解答 3.4-5

记 $v=\left(2-3i,6+9i,-18i\right)\in D^3$, $K=Dv$. 商模 $D^3/K$ 由 $1\times3$ 矩阵 $A=\begin{bmatrix}2-3i & 6+9i & -18i\end{bmatrix}$ 的史密斯标准形决定. 不变因子的第一个为 $A$ 三个元素的最大公因子 (在相伴意义下).

在 $D=\mathbb Z\left[i\right]$ 中计算. 记 $a=2-3i$, 其范数 $N\left(a\right)=2^2+3^2=13$, 故 $a$ 是 $D$ 中的不可约元素 ($13=\left(2-3i\right)\left(2+3i\right)$). 又 $b=6+9i=3\left(2+3i\right)$, $c=-18i$, $N\left(c\right)=18^2=324$.

考察 $a=2-3i$ 是否整除 $b,c$:

$$
\frac{b}{a}=\frac{3\left(2+3i\right)\left(2+3i\right)}{13}=\frac{3\left(-5+12i\right)}{13}\notin\mathbb Z\left[i\right],
$$

$$
\frac{c}{a}=\frac{-18i\left(2+3i\right)}{13}=\frac{54-36i}{13}\notin\mathbb Z\left[i\right].
$$

故 $a\nmid b$, $a\nmid c$. 而 $a$ 的非平凡因子只有其相伴元 ($a$ 不可约), 所以 $a$ 不是 $b,c$ 的公因子. 同理 $2+3i$ 也不整除 $a$. 于是 $a,b,c$ 的最大公因子是 $D$ 中的单位 $1$.

因此 $A$ 的史密斯标准形为 $\begin{bmatrix}1 & 0 & 0\end{bmatrix}$. 由**推论 3.4.12 (有限生成模的同构判定)**,

$$
D^3/K\cong D/\left(1\right)\oplus D/\left(0\right)\oplus D/\left(0\right)\cong D^2.
$$

即 $D^3/K$ 的秩为 $2$, 挠部分为零. 故其不变因子 (挠部分 $d_1,\cdots,d_k$) 为空, 初等因子也为空; 模同构于自由模 $D^2$. $\blacksquare$
