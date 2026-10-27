# week8

> **基础知识: 群到置换矩阵的忠实表示**<br>设 $G$ 是 $n$ 阶群. 由凯莱定理, 左平移给出单同态 $G\to S_G\cong S_n$; 再经置换矩阵嵌入, $G$ 同构于 $\mathrm{GL}\left(n,\mathbb C\right)$ 的一个子群, 故可把 $G$ 看作 $V=\mathbb C^{n}$ 上的线性变换群.

> **基础知识: 可解性在同构下保持**<br>若两个群同构, 则它们同为可解群或同不可解群; 幂零性同理.

> **基础知识: 特征标与公共特征子空间**<br>设 $N\triangleleft G$ 作用在 $V$ 上, $v\in V$ 是 $N$ 的公共特征向量, 特征为 $\lambda$, 即 $\sigma v=\lambda\left(\sigma\right)v$ ($\forall\sigma\in N$). 则对任意 $\tau\in G$, $\tau v\in V_{\lambda^{\tau}}$, 其中 $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$, $V_{\lambda}=\left\{v\mid\sigma v=\lambda\left(\sigma\right)v,\ \forall\sigma\in N\right\}$.

> **基础知识: 交换线性变换族的公共特征向量**<br>复数域 $\mathbb C$ 上的一组可交换的线性变换 (即一个 Abel 群的线性表示) 可同时对角化, 特别地存在公共特征向量.

> **基础知识: 幂零矩阵与有限阶元**<br>设 $M$ 是 $n$ 阶严格上三角矩阵, 则 $M$ 是幂零矩阵, 即存在 $r$ 使 $M^{r}=0$. 若 $A=I+M$ 有有限阶, 即存在正整数 $k$ 使 $A^{k}=I$, 则 $M=0$, 从而 $A=I$: 因 $\left(I+M\right)^{k}-I=kM+\binom{k}{2}M^{2}+\cdots+M^{k}=0$, 设 $s$ 为使 $M^{s}\ne0$ 的最小正整数, 则左端最低次项为 $kM^{s}$, 而 $k\ne0$ 在 $\mathbb C$ 中可逆, 故 $M^{s}=0$, 矛盾.

> **基础知识: 有限群元素皆有有限阶**<br>对有限群 $G$ 中任一元素 $g$, 存在正整数 $k$ 使 $g^{k}=e$, 即 $g$ 的阶有限.

> **定理 1.4.10 (凯莱定理)**<br>任何群 $G$ 与对称群 $S_G$ 的一个子群同构; 事实上映射 $L:G\to L_G$, $a\mapsto L_a$ 是单同态.

> **引理 1.8.3 (换位子性质)**<br>(1) $\left[g,h\right]^{-1}=\left[h,g\right]$, 且 $\left[g,h\right]=e$ 当且仅当 $gh=hg$. (2) 设 $\varphi:G\to H$ 为群同态, 则 $\varphi\left(\left[g,h\right]\right)=\left[\varphi\left(g\right),\varphi\left(h\right)\right]$; 特别地, 若 $\varphi\in\mathrm{Aut}\left(G\right)$, 则 $\varphi\left(\left[g,h\right]\right)=\left[\varphi\left(g\right),\varphi\left(h\right)\right]$.

> **引理 1.8.5**<br>设 $N\triangleleft G$, 则 $G/N$ 是 Abel 群当且仅当 $\left[G,G\right]\subseteq N$. 特别地, $G/\left[G,G\right]$ 为 Abel 群.

> **定义 1.8.7 (可解群与幂零群)**<br>在群 $G$ 中归纳定义导出列 $G^{\left(0\right)}=G$, $G^{\left(k+1\right)}=\left[G^{\left(k\right)},G^{\left(k\right)}\right]$. 若存在 $t$ 使得 $G^{\left(t\right)}=\left\{e\right\}$, 则称 $G$ 为可解群. 归纳定义降中心列 $G^{1}=G$, $G^{k+1}=\left[G,G^{k}\right]$, 若存在 $t$ 使得 $G^{t}=\left\{e\right\}$, 则称 $G$ 为幂零群.

> **引理 1.8.8 (可解群的遗传性)**<br>可解群的子群,商群都是可解群; 反之, 设 $N\trianglelefteq G$, 且 $N$ 与 $G/N$ 都可解, 则 $G$ 可解.

---

## 1.8-12

设 $G$ 为 $n$ 阶可解群, $B$ 为可逆的复上三角矩阵的全体. 证明: $G$ 同构于 $B$ 的某个子群. 如果 $G$ 为 $n$ 阶幂零群, $N$ 为对角线元全为 $1$ 的复上三角矩阵的全体, $G$ 是否同构于 $N$ 的某个子群?

### 解答 1.8-12

**先证第一部分.** 由**基础知识: 群到置换矩阵的忠实表示**及**定理 1.4.10 (凯莱定理)**, $n$ 阶可解群 $G$ 同构于 $\mathrm{GL}\left(V\right)$ 的一个子群, 其中 $V=\mathbb C^{n}$; 由**基础知识: 可解性在同构下保持**, 可设 $G$ 本身是 $\mathrm{GL}\left(V\right)$ 的可解子群. 下面对 $\dim V$ 作归纳, 证明 $G$ 可同时上三角化, 即 $G$ 共轭于上三角矩阵群 $B$ 的子群.

**归纳基础**: 当 $\dim V=1$ 时, $\mathrm{GL}\left(V\right)\cong\mathbb C^{*}$ 本身就是上三角矩阵群, 结论显然成立.

**归纳步**: 设 $\dim V=n>1$. 由**定义 1.8.7 (可解群与幂零群)**, $G$ 的换位子群 $G^{\prime}=\left[G,G\right]$ 是 $G$ 的真正规子群; 由**引理 1.8.5**, $G/G^{\prime}$ 为 Abel 群. 由**引理 1.8.8 (可解群的遗传性)**, $G^{\prime}$ 是可解群. 由归纳假设 (对 $G^{\prime}$ 在 $V$ 上反复运用基础情形的结果), $G^{\prime}$ 在 $V$ 上有公共特征向量; 设 $\lambda$ 是 $G^{\prime}$ 的一个特征标, 记其特征子空间为

$$
V_{\lambda}=\left\{v\in V\mid\sigma v=\lambda\left(\sigma\right)v,\ \forall\sigma\in G^{\prime}\right\}.
$$

因 $G^{\prime}\trianglelefteq G$, 对任意 $\tau\in G$, $\sigma\in G^{\prime}$ 及 $v\in V_{\lambda}$, 由**引理 1.8.3 (换位子性质)** (2) (取 $\varphi=\mathrm{Ad}_{\tau}$), $\tau\sigma\tau^{-1}\in G^{\prime}$, 且

$$
\sigma\left(\tau v\right)=\tau\left(\tau^{-1}\sigma\tau\right)v=\tau\lambda\left(\tau^{-1}\sigma\tau\right)v=\lambda\left(\tau^{-1}\sigma\tau\right)\tau v,
$$

故由**基础知识: 特征标与公共特征子空间**, $\tau v\in V_{\lambda^{\tau}}$, 其中 $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$. 由于 $G/G^{\prime}$ 是 Abel 群, $G$ 在 $G^{\prime}$ 的特征标集上的共轭作用轨道有限, 取其中一个轨道对应的特征子空间之和, 即得一个非零的 $G$-不变子空间 $W$.

在 $W$ 上, 因 $G/G^{\prime}$ 为 Abel 群而 $G^{\prime}$ 在 $W$ 上以标量作用, 故 $G$ 在 $W$ 上的像的换位子群为标量群, $G$ 的像在 $\mathrm{GL}\left(W\right)$ 中是 Abel 化的; 由**基础知识: 交换线性变换族的公共特征向量**, $W$ 中存在 $G$ 的公共特征向量, 即存在一维 $G$-不变子空间 $L\subseteq V$.

于是 $G$ 在商空间 $V/L$ 上诱导一个可解子群 (由**基础知识: 可解性在同构下保持**与商群的可解性, 或**引理 1.8.8 (可解群的遗传性)**), 由归纳假设, $G$ 在 $V/L$ 上可上三角化. 因而在 $V$ 中可取一组基, 使 $L$ 为第一个基向量张成的子空间, 而商空间的上三角化给出 $G$ 在 $V$ 上的上三角矩阵表示. 故 $G$ 共轭于 $B$ 的一个子群, 即 $G$ 同构于 $B$ 的某个子群. $\blacksquare$

**再回答第二部分.** 答案是否定的: 非平凡的有限幂零群 $G$ 不能同构于 $N$ 的子群.

事实上, 设 $A\in N$, 即 $A$ 是对角线元全为 $1$ 的复上三角矩阵, 则 $A=I+M$, 其中 $M$ 是严格上三角矩阵. 由**基础知识: 幂零矩阵与有限阶元**, $M$ 是幂零矩阵, 且若 $A$ 是有限阶元, 则 $M=0$, 即 $A=I$. 这说明 $N$ 中的有限阶元只有单位矩阵 $I$ 自身.

因此 $N$ 的有限子群只能是平凡群 $\left\{I\right\}$. 而 $G$ 是有限的非平凡幂零群, 由**基础知识: 有限群元素皆有有限阶**, $G$ 含有非单位的有限阶元, 故 $G$ 不能同构于 $N$ 的某个子群. $\blacksquare$
