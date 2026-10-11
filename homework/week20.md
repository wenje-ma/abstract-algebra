# 作业 20

> **推论 3.3.10**（自由模秩的唯一性）设 $R$ 为交换幺环, 则 $R^m\cong R^n$ 当且仅当 $m=n$, 其中 $R^m$ 表示 $m$ 个 $R$ 的外直和.

> **定理 3.3.6**（基的刻画）
>
> 设 $M$ 为幺环 $R$ 上的模, $u_1,\cdots,u_m$ 为 $M$ 中元素, 则 $M$ 为自由模且 $u_1,\cdots,u_m$ 为一组基当且仅当
>
> (1) $u_1,\cdots,u_m$ 是 $M$ 的一组生成元;
>
> (2) $u_1,\cdots,u_m$ 线性无关.

> **基础知识**（行列式）交换幺环 $R$ 上方阵 $A$ 可逆当且仅当其行列式 $\det A$ 为 $R$ 中的单位.

### 习题一

（习题 3.3-6）设 $R$ 为交换幺环, 而且任何有限生成的 $R$-模都是自由模, 证明 $R$ 为一个域.

### 解答 习题一

只需证明 $R$ 中每个非零元都是单位. 任取 $a\in R$, $a\ne0$. 考虑商模 $R/\left(a\right)$, 它由 $\overline 1=1+\left(a\right)$ 生成, 因而是有限生成 $R$-模. 由题设, $R/\left(a\right)$ 是自由模.

断言 $R/\left(a\right)=0$. 否则它是非零自由模, 而 $\overline 1$ 是它的生成元. 由**定理 3.3.6**（基的刻画）, 若 $\left\{\overline 1\right\}$ 为一组基, 则其零化子为零, 即 $r\overline 1=0\Rightarrow r=0$. 但 $a\overline 1=a+\left(a\right)=0$, 且 $a\ne0$, 矛盾. 故 $R/\left(a\right)=0$.

$R/\left(a\right)=0$ 等价于 $\left(a\right)=R$, 即 $1\in\left(a\right)$, 亦即存在 $b\in R$ 使 $ab=1$. 故 $a$ 是单位.

由 $a\ne0$ 的任意性, $R$ 的每个非零元都是单位, 故 $R$ 是一个域. $\blacksquare$

### 习题二

（习题 3.3-7）设 $R$ 为交换幺环, $\phi$ 为自由模 $R^m$ 的自同态, 试证明: 如果 $\phi$ 为满同态, 则 $\phi$ 为同构.

### 解答 习题二

取 $R^m$ 的一组标准基 $e_1,\cdots,e_m$, 设自同态 $\phi$ 在这组基下的矩阵为 $A\in R^{m\times m}$.

因 $\phi$ 是满同态, 对每个基向量 $e_j\in R^m$, 存在 $x_j\in R^m$ 使 $\phi\left(x_j\right)=e_j$. 将 $x_1,\cdots,x_m$ 作为列向量排成矩阵 $B$, 则

$$
AB=I_m,
$$

其中 $I_m$ 为 $m$ 阶单位矩阵. 两边取行列式, 由行列式乘性,

$$
\begin{aligned}\det\left(A\right)\det\left(B\right)&=\det\left(I_m\right)\\&=1.\end{aligned}
$$

故 $\det A$ 是 $R$ 中的单位. 由行列式的基础知识, $A$ 可逆, 即存在 $A^{-1}$ 使 $AA^{-1}=I_m$. 因而 $\phi$ 既是满同态又是单同态（$\ker\phi=0$）, 是双射, 故 $\phi$ 为模同构. $\blacksquare$

### 习题三

（习题 3.3-8）条件同上题, 如果 $R$ 是域且 $\phi$ 是单同态, 证明 $\phi$ 是同构. 这个结论对于一般的交换幺环成立吗？

### 解答 习题三

当 $R$ 是域时, $R^m$ 是 $m$ 维线性空间. $\phi$ 是单同态意味着线性变换 $\phi$ 的核为零子空间. 由线性代数, 有限维线性空间上的单线性变换必为满射, 从而为同构. 也可由矩阵看: 单同态对应矩阵 $A$ 的列线性无关, 即 $\operatorname{rank}A=m$, 故方阵 $A$ 满秩, 可逆, $\phi$ 为同构.

这个结论对于一般的交换幺环不成立.

反例. 取 $R=\mathbb Z$（交换幺环）, $m=1$, 定义 $\phi:\mathbb Z\to\mathbb Z$ 为

$$
\phi\left(n\right)=2n.
$$

$\phi$ 是 $\mathbb Z$ 上的自同态. 它是单同态: 若 $2n=0$, 在整环 $\mathbb Z$ 中 $n=0$. 但它不是满同态: $1\notin 2\mathbb Z$, 即不存在 $n$ 使 $2n=1$. 故 $\phi$ 不单射却不双射, 不是同构.

因此一般交换幺环上自由模的单自同态未必是同构. $\blacksquare$
