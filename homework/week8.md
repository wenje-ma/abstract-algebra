# 作业 8

> **定义 1.8.1**（换位子与换位子群）设 $g,h\in G$, 称 $g^{-1}h^{-1}gh$ 为 $g,h$ 的换位子, 记为 $\left[g,h\right]$. 若 $H,K$ 都是 $G$ 的子群, 称 $\left[H,K\right]=\left\langle\left[h,k\right]\mid h\in H,k\in K\right\rangle$ 为 $H,K$ 的换位子群. 特别地, $\left[G,G\right]$ 称为 $G$ 的换位子群.

> **定义 1.8.7**（可解群与幂零群）在群 $G$ 中归纳定义导出列 $G^{\left(0\right)}=G$, $G^{\left(k+1\right)}=\left[G^{\left(k\right)},G^{\left(k\right)}\right]$. 若存在 $t$ 使得 $G^{\left(t\right)}=\left\{e\right\}$, 则称 $G$ 为可解群. 归纳定义降中心列 $G^{1}=G$, $G^{k+1}=\left[G,G^{k}\right]$, 若存在 $t$ 使得 $G^{t}=\left\{e\right\}$, 则称 $G$ 为幂零群.

> **引理 1.8.8**（可解群的遗传性）可解群的子群、商群都是可解群; 反之, 设 $N\trianglelefteq G$, 且 $N$ 与 $G/N$ 都可解, 则 $G$ 可解.

> **基础知识**（李定理的关键引理）设 $G$ 是 $\mathrm{GL}\left(V\right)$ 的可解子群, 其中 $V$ 是复数域上的有限维线性空间, 则 $G$ 在 $V$ 上有公共特征向量, 即存在 $V$ 的一维子空间在 $G$ 的作用下不变. 反复使用此结论可得 $G$ 可同时上三角化, 即 $G$ 共轭于可逆上三角矩阵群 $B$ 的子群.

### 习题一

（习题 1.8-12）设 $G$ 为 $n$ 阶可解群, $B$ 为可逆的复上三角矩阵的全体. 证明: $G$ 同构于 $B$ 的某个子群. 如果 $G$ 为 $n$ 阶幂零群, $N$ 为对角线元全为 $1$ 的复上三角矩阵的全体, $G$ 是否同构于 $N$ 的某个子群?

### 解答 习题一

先证第一部分. 设 $V$ 是复数域 $\mathbb C$ 上的 $n$ 维线性空间, $G$ 是 $\mathrm{GL}\left(V\right)$ 的可解子群. 对 $\dim V$ 作归纳证明 $G$ 可同时上三角化.

当 $\dim V=1$ 时, $\mathrm{GL}\left(V\right)$ 本身就是上三角矩阵群, 结论显然成立.

设 $\dim V=n>1$. 由**定义 1.8.7**（可解群与幂零群）, $G$ 的换位子群 $G^{\prime}=\left[G,G\right]$ 是 $G$ 的真正规子群, 且 $G/G^{\prime}$ 为交换群. 由归纳假设, $G^{\prime}$ 在 $V$ 上有公共特征向量. 设 $\lambda$ 是 $G^{\prime}$ 的一个特征标, 记其特征子空间为
$$
V_{\lambda}=\left\{v\in V\mid\sigma v=\lambda\left(\sigma\right)v,\;\forall\sigma\in G^{\prime}\right\}.
$$
因 $G^{\prime}\trianglelefteq G$, 对任意 $\tau\in G$, $\sigma\in G^{\prime}$ 及 $v\in V_{\lambda}$, 由**引理 1.8.3**（换位子性质）$\tau\sigma\tau^{-1}\in G^{\prime}$, 且
$$
\begin{aligned}\sigma\left(\tau v\right)&=\tau\left(\tau^{-1}\sigma\tau\right)v\\&=\tau\lambda\left(\tau^{-1}\sigma\tau\right)v\\&=\lambda\left(\tau^{-1}\sigma\tau\right)\tau v,\end{aligned}
$$
故 $\tau v\in V_{\lambda^{\tau}}$, 其中 $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$. 由于 $G/G^{\prime}$ 交换, $G$ 在 $G^{\prime}$ 的特征标上的作用轨道有限, 取其中一个轨道对应的特征子空间之和, 即得一个非零的 $G$-不变子空间 $W$.

在 $W$ 上, $G/G^{\prime}$ 为交换群, 而复数域上交换线性变换族可同时对角化, 故 $W$ 中存在 $G$ 的公共特征向量, 即存在一维 $G$-不变子空间 $L\subseteq V$.

于是 $G$ 在商空间 $V/L$ 上诱导一个可解子群, 由归纳假设, $G$ 在 $V/L$ 上可上三角化. 因而在 $V$ 中可取一组基, 使 $L$ 为第一个基向量张成的子空间, 而商空间的上三角化给出 $G$ 在 $V$ 上的上三角矩阵表示. 故 $G$ 共轭于 $B$ 的一个子群, 即 $G$ 同构于 $B$ 的某个子群.

再回答第二部分. 答案是否定的, 即非平凡的有限幂零群不能同构于 $N$ 的子群.

事实上, 设 $A\in N$, 即 $A$ 是对角线元全为 $1$ 的复上三角矩阵, 则 $A=I+M$, 其中 $M$ 是严格上三角矩阵, 从而 $M$ 是幂零矩阵, 即存在 $r$ 使 $M^{r}=0$. 若 $A$ 是有限阶元, 即存在正整数 $k$ 使 $A^{k}=I$, 则
$$
\begin{aligned}\left(I+M\right)^{k}-I&=kM+\binom{k}{2}M^{2}+\cdots+M^{k}\\&=0.\end{aligned}
$$
设 $s$ 是使 $M^{s}\ne0$ 的最小正整数, 则上式左端最低次项为 $kM^{s}$. 因 $k\ne0$ 在 $\mathbb C$ 中可逆, 故 $M^{s}=0$, 矛盾. 因此 $M=0$, 即 $A=I$.

这说明 $N$ 中的有限阶元只有单位矩阵 $I$ 自身. 因而 $N$ 的有限子群只能是平凡群 $\left\{I\right\}$. 任何非平凡的有限幂零群 $G$ 都含有非单位的有限阶元, 故不能同构于 $N$ 的子群. $\blacksquare$
