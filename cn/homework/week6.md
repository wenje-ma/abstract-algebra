# 作业 6

> **定义 1.6.1**（轮换）设
> $$
> \left\{i_{1},i_{2},\dots,i_{r}\right\}\subseteq\left\{1,2,\dots,n\right\}.
> $$
> 若 $\sigma\in S_{n}$ 满足 $\sigma\left(i_{1}\right)=i_{2}$, $\sigma\left(i_{2}\right)=i_{3}$, ..., $\sigma\left(i_{r}\right)=i_{1}$, 且 $\sigma$ 固定其余文字, 则称 $\sigma$ 为一个 $r$-轮换, 记为 $\sigma=\left(i_{1}i_{2}\dots i_{r}\right)$. 特别地, $2$-轮换称为对换.

> **定理 1.6.4**（轮换分解）$S_{n}$ 中的任何元素都可表为 $S_{n}$ 中一些不相交轮换之积. 如果不计次序, 表法是唯一的.

> **引理 1.6.7**（轮换的对换分解）任一个 $r$-轮换都可写成 $r-1$ 个对换的乘积:
> $$
> \left(i_{1}i_{2}\dots i_{r}\right)=\left(i_{1}i_{r}\right)\left(i_{1}i_{r-1}\right)\dots\left(i_{1}i_{3}\right)\left(i_{1}i_{2}\right).
> $$

> **基础知识**（交错群）当一个置换能表为奇(偶)数个对换的乘积时, 称为奇置换(偶置换). $n$ 元偶置换的全体 $A_{n}$ 是 $S_{n}$ 的正规子群, 称为 $n$ 元交错群, 且 $\left|A_{n}\right|=\left|S_{n}\right|/2=n!/2$.

> **定理 1.6.9**（交错群的单性）当 $n\ge 5$ 时, $A_{n}$ 是单群.

> **定理 1.2.22**（拉格朗日定理）设 $G$ 是有限群, $H<G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$.

### 习题一

（习题 1.6-5）证明:

$$
\begin{aligned}
S_{n}&=\left\langle\left(12\right),\left(13\right),\dots,\left(1n\right)\right\rangle=\left\langle\left(12\right),\left(12\dots n\right)\right\rangle,\
A_{n}&=\left\langle\left(123\right),\left(124\right),\dots,\left(12n\right)\right\rangle.
\end{aligned}
$$

### 解答 习题一

**第一部分:

$$
S_{n}=\left\langle\left(12\right),\left(13\right),\dots,\left(1n\right)\right\rangle.
$$

**

$S_{n}$ 由所有对换生成. 任取对换 $\left(ij\right)$, $i\ne 1$, $j\ne 1$. 由共轭公式,

$$
\begin{aligned}\left(1i\right)\left(1j\right)\left(1i\right)&=\left(\left(1i\right)\left(1\right),\left(1i\right)\left(j\right)\right)\\&=\left(i,j\right)\\&=\left(ij\right).\end{aligned}
$$

故任意对换 $\left(ij\right)$ 均可由 $\left(12\right),\left(13\right),\dots,\left(1n\right)$ 表出, 因此

$$
S_{n}=\left\langle\left(12\right),\left(13\right),\dots,\left(1n\right)\right\rangle.
$$

**第二部分: $S_{n}=\left\langle\left(12\right),\left(12\dots n\right)\right\rangle$.**

记 $\sigma=\left(12\dots n\right)$. 由共轭公式, 对 $k=1,2,\dots,n-1$,

$$
\begin{aligned}\sigma^{k-1}\left(12\right)\sigma^{-\left(k-1\right)}&=\left(\sigma^{k-1}\left(1\right)\sigma^{k-1}\left(2\right)\right)\\&=\left(k,k+1\right).\end{aligned}
$$

故相邻对换 $\left(12\right),\left(23\right),\dots,\left(n-1,n\right)$ 均属于 $\left\langle\left(12\right),\sigma\right\rangle$. 而相邻对换生成 $S_{n}$, 故 $\left\langle\left(12\right),\sigma\right\rangle=S_{n}$.

**第三部分:

$$
A_{n}=\left\langle\left(123\right),\left(124\right),\dots,\left(12n\right)\right\rangle.
$$

**

由**引理 1.6.7**（轮换的对换分解）及**定理 1.6.4**（轮换分解）, $A_{n}$ 由所有 $3$-轮换生成(两个对换之积若不相交则为两个 $2$-轮换, 可表为 $3$-轮换乘积; 一般偶置换可分解为偶数个对换, 从而表为偶数个对换乘积之积, 即 $3$-轮换乘积).

下证任意 $3$-轮换均可由 $\left(123\right),\left(124\right),\dots,\left(12n\right)$ 表出.

(1)含 $1$ 和 $2$ 的 $3$-轮换即为 $\left(12k\right)$ 或其逆, 已在生成集中.

(2)含 $1$ 但不含 $2$ 的 $3$-轮换 $\left(1jk\right)$:

$$
\begin{aligned}\left(12k\right)\left(12j\right)^{-1}&=\left(12k\right)\left(1j2\right)\\&=\left(1jk\right).\end{aligned}
$$

(3)不含 $1$ 的 $3$-轮换 $\left(ijk\right)$: 由(2)可先得到 $\left(1ij\right)$ 与 $\left(1ik\right)$, 于是

$$
\begin{aligned}\left(1ij\right)^{-1}\left(1ik\right)&=\left(1ji\right)\left(1ik\right)\\&=\left(ikj\right)\\&=\left(ijk\right).\end{aligned}
$$

故所有 $3$-轮换均属于 $\left\langle\left(123\right),\left(124\right),\dots,\left(12n\right)\right\rangle$. 反之, 各生成元均为偶置换, 故包含于 $A_{n}$. 因此

$$
A_{n}=\left\langle\left(123\right),\left(124\right),\dots,\left(12n\right)\right\rangle.
$$

$\blacksquare$

### 习题二

（习题 1.6-6）证明: $S_{n}$ 的非平凡正规子群为 $A_{n}$ 或 $K_{4}$(当 $n=4$ 时).

### 解答 习题二

设 $N\triangleleft S_{n}$, $N\ne\left\{e\right\}$, $N\ne S_{n}$.

**情形 $n\ge 5$:** 由**定理 1.6.9**（交错群的单性）, $A_{n}$ 是单群.

考虑 $N\cap A_{n}$. 因 $N\triangleleft S_{n}$, $A_{n}\triangleleft S_{n}$, 故 $N\cap A_{n}\triangleleft A_{n}$. 由 $A_{n}$ 的单性, $N\cap A_{n}=\left\{e\right\}$ 或 $A_{n}$.

若 $N\cap A_{n}=A_{n}$, 则 $A_{n}\subseteq N$. 因 $N\ne S_{n}$, $N$ 不含奇置换. 又 $N\cap A_{n}=A_{n}\subsetneq N$, 而 $S_{n}/A_{n}$ 仅含两个元素, 故 $N=A_{n}$.

若 $N\cap A_{n}=\left\{e\right\}$, 则 $N$ 中无偶置换(除单位元), 即 $N$ 的非单位元均为奇置换. 此时 $N$ 中任意两个非单位元之积为偶置换, 故必为 $e$, 即 $N$ 中任意非单位元均为二阶元且两两可交换. 又 $N\triangleleft S_{n}$, 故 $N$ 由若干共轭的对换(或不相交对换乘积)组成. 但 $S_{n}$ 中所有对换互相共轭, 若 $N$ 含一个对换则必含所有对换, 从而 $N=S_{n}$, 矛盾. 故此情形不可能.

因此 $n\ge 5$ 时, $S_{n}$ 的非平凡正规子群只有 $A_{n}$.

**情形 $n=4$:** $S_{4}$ 阶为 $24$. $A_{4}$ 阶为 $12$, 是正规子群. 此外,

$$
K_{4}=\left\{e,\left(12\right)\left(34\right),\left(13\right)\left(24\right),\left(14\right)\left(23\right)\right\}
$$

是 $A_{4}$ 的正规子群, 且共轭作用下不变, 故 $K_{4}\triangleleft S_{4}$.

$S_{4}$ 的正规子群只有 $\left\{e\right\},K_{4},A_{4},S_{4}$. 故非平凡正规子群为 $A_{4}$ 与 $K_{4}$.

**情形 $n=3$:** $S_{3}$ 的正规子群只有 $\left\{e\right\},A_{3},S_{3}$, 非平凡者为 $A_{3}$.

**情形 $n\le 2$:** 无意义或无正规非平凡子群.

综上, $S_{n}$ 的非平凡正规子群为 $A_{n}$(对所有 $n\ge 3$), 以及 $n=4$ 时的 $K_{4}$. $\blacksquare$

### 习题三

（习题 1.6-11）设 $\left|G\right|=2n$, 其中 $n$ 为奇数. 证明: $G$ 有指数为 $2$ 的正规子群.

### 解答 习题三

考虑 $G$ 的左正则表示: 由凯莱定理, 映射

$$
\lambda:G\to S_{G}, g\mapsto L_{g},
$$

其中 $L_{g}\left(x\right)=gx$, 是单同态. 视 $\lambda$ 为 $G$ 到 $S_{2n}$ 的单同态.

作符号同态 $\mathrm{sgn}:S_{2n}\to\left\{1,-1\right\}$. 复合得

$$
\mathrm{sgn}\circ\lambda:G\to\left\{1,-1\right\}.
$$

这是群同态. 下证其为满射.

因 $\left|G\right|=2n$ 为偶数, $G$ 中存在二阶元 $a$(将 $G$ 中元素按互逆配对, $e$ 自成一对, 其余非二阶元两两配对, 因阶为偶数, 必有奇数个二阶元, 故存在非单位二阶元).

$\lambda\left(a\right)=L_{a}$ 是 $G$ 上的置换. 因 $a^{2}=e$, 对任意 $x\in G$, $L_{a}^{2}\left(x\right)=a^{2}x=x$, 故 $L_{a}$ 是对合. 又 $a\ne e$, $L_{a}$ 无不动点(若 $ax=x$ 则 $a=e$). 因此 $L_{a}$ 是 $n$ 个不相交对换之积, 其符号为

$$
\begin{aligned}\mathrm{sgn}\left(L_{a}\right)&=\left(-1\right)^{n}\\&=-1,\end{aligned}
$$

其中用到 $n$ 为奇数. 故 $\mathrm{sgn}\circ\lambda$ 是满同态.

令 $H=\ker\left(\mathrm{sgn}\circ\lambda\right)$. 由同态基本定理, $G/H\cong\left\{1,-1\right\}$, 故 $\left[G:H\right]=2$.

又 $H$ 是同态核, 故 $H\triangleleft G$. 即 $G$ 有指数为 $2$ 的正规子群. $\blacksquare$

### 习题四

（习题 1.6-14）证明: 当 $n\ne 2,6$ 时, $\mathrm{Aut}\left(S_{n}\right)=S_{n}$. 并求 $\mathrm{Aut}\left(S_{2}\right)$ 与 $\mathrm{Aut}\left(S_{6}\right)$.

### 解答 习题四

先证 $n\ne 2,6$ 时 $\mathrm{Aut}\left(S_{n}\right)=S_{n}$.

显然 $S_{n}$ 的内自同构群 $\mathrm{Inn}\left(S_{n}\right)\cong S_{n}/Z\left(S_{n}\right)$. 当 $n\ge 3$ 时 $S_{n}$ 的中心为平凡, 故 $\mathrm{Inn}\left(S_{n}\right)\cong S_{n}$. 只需证任一自同构均为内自同构.

设 $\varphi\in\mathrm{Aut}\left(S_{n}\right)$. 自同构保持元素的阶与共轭类. $S_{n}$ 中对换是唯一的一类二阶元: 它们的中心化子阶为 $2\cdot\left(n-2\right)!$, 与其余二阶元(如不相交对换之积)的中心化子阶不同. 因此 $\varphi$ 必将对换映为对换.

设 $\varphi\left(12\right)=\left(ab\right)$. 用适当的内自同构复合 $\varphi$, 可不妨设 $\varphi\left(12\right)=\left(12\right)$.

对 $k=3,\dots,n$, $\left(12\right)$ 与 $\left(1k\right)$ 的乘积 $\left(12\right)\left(1k\right)=\left(1k2\right)$ 是 $3$-轮换(阶为 $3$). 故 $\varphi\left(1k\right)$ 必为与 $\left(12\right)$ 恰好共享一个文字的对换(否则其与 $\left(12\right)$ 的乘积阶不为 $3$). 即 $\varphi\left(1k\right)=\left(1,j_{k}\right)$ 或 $\left(2,j_{k}\right)$.

若存在 $k$ 使 $\varphi\left(1k\right)=\left(2,j_{k}\right)$, 再用内自同构调整可统一为 $\varphi\left(1k\right)=\left(1,\sigma\left(k\right)\right)$ 形式, 其中 $\sigma\in S_{n-1}$ 是 $\left\{3,\dots,n\right\}$ 的一个排列.

于是 $\varphi$ 作用在生成元 $\left(12\right),\left(13\right),\dots,\left(1n\right)$ 上等于共轭作用于某 $\sigma\in S_{n}$. 由**习题一**的结果, 这些对换生成 $S_{n}$, 故 $\varphi$ 就是共轭自同构 $\mathrm{Ad}_{\sigma}$. 因此 $\varphi\in\mathrm{Inn}\left(S_{n}\right)$.

上述证明在 $n=6$ 时失效, 因为 $S_{6}$ 存在外自同构(将对换映为 $6$-轮换的平方等二阶元, 此类二阶元的中心化子阶与对换的相同), 这是 $S_{6}$ 独有的现象. 当 $n\ne 2,6$ 时,

$$
\mathrm{Aut}\left(S_{n}\right)=\mathrm{Inn}\left(S_{n}\right)\cong S_{n}.
$$

**$\mathrm{Aut}\left(S_{2}\right)$:** $S_{2}=\left\{e,\left(12\right)\right\}$ 是二阶循环群, 其自同构只能保持单位元, 故 $\mathrm{Aut}\left(S_{2}\right)=\left\{\mathrm{id}\right\}$ 是平凡群.

**$\mathrm{Aut}\left(S_{6}\right)$:** $S_{6}$ 存在外自同构, 且

$$
\left|\mathrm{Aut}\left(S_{6}\right)\right|=2\cdot\left|S_{6}\right|=1440,
$$
即

$$
\mathrm{Out}\left(S_{6}\right)=\mathrm{Aut}\left(S_{6}\right)/\mathrm{Inn}\left(S_{6}\right)\cong\mathbb Z_{2}.
$$

$\blacksquare$
