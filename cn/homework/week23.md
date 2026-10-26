# 作业 23

> **定理 3.6.3**（约当标准形）设 $F$ 为特征为零的代数闭域, $V$ 为 $F$ 上 $n$ 维线性空间, $A$ 为 $V$ 上的线性变换, 则存在 $V$ 的一组基使得 $A$ 在该基下的矩阵为准对角矩阵 $\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, 其中每个 $J_i$ 都是约当块. 两个 $F$ 上 $n\times n$ 矩阵相似当且仅当它们具有相同的约当标准形.

> **基础知识**（逆转置矩阵）设 $P$ 为 $n$ 阶反转矩阵, 即 $P_{i,n+1-i}=1$, 其余元素为 $0$, 则 $P$ 为对称矩阵, $P^2=I_n$, 且 $P^{-1}=P$. 若 $N$ 为 $n$ 阶幂零移位矩阵(即 $N_{i,i+1}=1$, 其余为 $0$), 则 $PNP=N^T$, 从而 $PN$ 为对称矩阵.

> **基础知识**（幂零核与约当块计数）设 $A$ 为 $n$ 阶方阵, $a$ 为 $A$ 的一个特征值. 记
> $$
> \nu_k=\dim\ker\left(aI_n-A\right)^k=n-\mathrm{rank}\left(aI_n-A\right)^k,
> $$
> 并约定 $\nu_0=0$. 则 $A$ 的以 $a$ 为特征值, 阶数不小于 $s$ 的约当块个数为 $\nu_s-\nu_{s-1}$. 因而序列 $\left\{\nu_k\right\}_{k\geqslant0}$ 完全决定了 $a$ 处约当块的大小与个数.

### 习题一

（习题 3.6-9）设 $F$ 为特征为零的代数闭域, 试证明 $F$ 上任何一个约当块都能写成两个对称矩阵的乘积.

### 解答 习题一

设 $J$ 为 $F$ 上 $n$ 阶约当块, 其特征值为 $\lambda\in F$, 则 $J=\lambda I_n+N$, 其中 $N$ 为 $n$ 阶幂零移位矩阵.

设 $P$ 为 $n$ 阶反转矩阵. 由**基础知识**（逆转置矩阵）, $P$ 对称, $P^2=I_n$, 且 $PN$ 对称. 令

$$
A=PJ=\lambda P+PN.
$$

因 $P$ 与 $PN$ 均对称, 故 $A$ 为对称矩阵. 又 $P^2=I_n$, 故 $P^{-1}=P$, 于是

$$
J=P^{-1}A=PA.
$$

其中 $P$ 与 $A$ 均为 $F$ 上对称矩阵. 故任一约当块均可写成两个对称矩阵的乘积. $\blacksquare$

### 习题二

（习题 3.6-10）试证明任何一个特征为零的代数闭域 $F$ 上的方阵都能写成 $F$ 上两个对称矩阵的乘积.

### 解答 习题二

设 $A$ 为 $F$ 上 $n$ 阶方阵. 由**定理 3.6.3**（约当标准形）, 存在可逆矩阵 $S$ 使

$$
S^{-1}AS=J=\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right),
$$

其中 $J_1,J_2,\cdots,J_s$ 均为约当块.

由**习题一**的结论, 每个约当块 $J_i$ 可写为 $J_i=P_iQ_i$, 其中 $P_i,Q_i$ 均为对称矩阵. 令

$$
P=\mathrm{diag}\left(P_1,P_2,\cdots,P_s\right),
$$

$$
Q=\mathrm{diag}\left(Q_1,Q_2,\cdots,Q_s\right),
$$

则 $P,Q$ 均为对称矩阵, 且 $J=PQ$.

于是

$$
A=SJS^{-1}=SPQS^{-1}=\left(SPS^T\right)\left(S^{-T}QS^{-1}\right).
$$

其中 $SPS^T$ 为对称矩阵, 因其转置为

$$
\left(SPS^T\right)^T=SP^TS^T=SPS^T;
$$
同理

$$
S^{-T}QS^{-1}=\left(S^{-1}\right)^TQS^{-1}
$$

亦为对称矩阵. 故 $A$ 为两个对称矩阵之积. $\blacksquare$

### 习题三

（习题 3.6-11）设 $A$ 为实线性空间 $V$ 上的线性变换, 试证明存在 $V$ 的一组基使得在这组基下 $A$ 的矩阵具有分块矩阵

$$
\begin{bmatrix}B_1&B_2\\0&B_3\end{bmatrix}
$$

的形式, 其中 $B_1$ 为 $1$ 阶或 $2$ 阶方阵.

### 解答 习题三

对 $\dim V=n$ 作归纳. 当 $n=1$ 时结论显然成立. 假设维数小于 $n$ 时结论成立, 考虑 $n$ 维情形.

**情形一 $A$ 有实特征值 $\lambda$** 取对应的实特征向量 $v_1$, 扩充为 $V$ 的一组基 $v_1,v_2,\cdots,v_n$. 因 $v_1$ 生成的一维子空间是 $A$-不变子空间, $A$ 在该基下的矩阵形如

$$
\begin{bmatrix}\lambda&*\\0&A'\end{bmatrix},
$$

其中 $\lambda$ 为 $1$ 阶块, $A'$ 为 $n-1$ 阶实矩阵. 由归纳假设, $A'$ 可相似于所要求的分块上三角形式, 从而 $A$ 亦然.

**情形二 $A$ 无实特征值** 此时 $A$ 的特征多项式在 $\mathbb R\left[x\right]$ 上没有一次因式, 故可分解为若干个判别式小于零的二次不可约多项式之积. 取其中一个 $p\left(x\right)=x^2+bx+c$, $b^2-4c< 0$.

由主理想整环 $\mathbb R\left[x\right]$ 上有限生成扭模的结构理论(即 $V$ 作为 $\mathbb R\left[x\right]$-模的准素分解), $p\left(x\right)$ 对应的准素子空间非零. 取其中向量 $u$ 使得 $p\left(A\right)u=0$ 且 $u\ne0$. 因 $p\left(x\right)$ 无实根, $u$ 与 $Au$ 必线性无关(否则 $Au=au$, $a\in\mathbb R$, 则 $a$ 为 $p$ 的实根, 矛盾). 令 $W=\mathrm{span}\left\{u,Au\right\}$. 由 $p\left(A\right)u=0$ 即 $A^2u+bAu+cu=0$ 得

$$
A\left(Au\right)=A^2u=-cu-bAu\in W,
$$

故 $W$ 是 $2$ 维 $A$-不变子空间. 取 $W$ 的一组基, 扩充为 $V$ 的一组基, 则 $A$ 在该基下的矩阵形如

$$
\begin{bmatrix}B_1&B_2\\0&A'\end{bmatrix},
$$

其中 $B_1$ 为 $2$ 阶方阵($A$ 在 $W$ 上的限制), $A'$ 为 $n-2$ 阶实矩阵. 由归纳假设, $A'$ 可化为所要求的分块上三角形式, 从而 $A$ 亦然.

综上, 由归纳法, 存在 $V$ 的一组基使 $A$ 的矩阵为所要求的分块上三角形式. $\blacksquare$

### 习题四

（习题 3.6-12）(韦尔定理)试证明特征为零的代数闭域上两个 $n\times n$ 矩阵 $A,B$ 相似当且仅当对任何 $a\in F$ 及 $k\in\mathbb N$, $\left(aI_n-A\right)^k$ 与 $\left(aI_n-B\right)^k$ 具有相同的秩.

### 解答 习题四

**必要性** 若 $A$ 与 $B$ 相似, 则存在可逆矩阵 $P$ 使 $B=P^{-1}AP$. 于是

$$
\left(aI_n-B\right)^k=\left(aI_n-P^{-1}AP\right)^k=P^{-1}\left(aI_n-A\right)^kP.
$$

相似矩阵秩相同, 故

$$
\mathrm{rank}\left(aI_n-A\right)^k=\mathrm{rank}\left(aI_n-B\right)^k.
$$

**充分性** 设对任何 $a\in F$ 及 $k\in\mathbb N$, 两矩阵相应幂的秩相同. 由**定理 3.6.3**（约当标准形）, $A,B$ 均相似于其约当标准形, 只需证明二者约当标准形相同.

对任一 $a\in F$, 记

$$
\nu_k\left(A\right)=\dim\ker\left(aI_n-A\right)^k=n-\mathrm{rank}\left(aI_n-A\right)^k,
$$

并约定 $\nu_0\left(A\right)=0$. 由题设, $\nu_k\left(A\right)=\nu_k\left(B\right)$ 对所有 $k$ 成立. 由**基础知识**（幂零核与约当块计数）, $A$ 的以 $a$ 为特征值, 阶数不小于 $s$ 的约当块个数为 $\nu_s\left(A\right)-\nu_{s-1}\left(A\right)$, $B$ 同理. 故二者在 $a$ 处的约当块大小与个数完全一致.

由于 $F$ 是代数闭域, $A,B$ 的全部特征值均在 $F$ 中, 上述结论对每个特征值 $a$ 成立. 因而 $A$ 与 $B$ 的约当标准形完全相同, 从而 $A$ 与 $B$ 相似. $\blacksquare$
