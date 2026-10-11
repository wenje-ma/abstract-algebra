# 作业 5

> **定理 1.5.5**（循环群的分类）设 $G$ 是循环群, 若 $G$ 是无限群, 则 $G$ 与 $\left(\mathbb Z,+\right)$ 同构; 若 $G$ 是 $n$ 阶群, 则 $G$ 与 $\left(\mathbb Z_{n},+\right)$ 同构. 从而, 两个循环群同构当且仅当它们有相同的阶.

> **引理 1.5.7**（循环群的子群结构）循环群 $G=\left\langle a\right\rangle$ 的任一子群都形如 $\left\langle a^{l}\right\rangle$, $l\in\mathbb N$, 从而也是循环群.

> **定理 1.5.8**（循环群的子群存在唯一性）设 $G$ 是 $n$ 阶循环群, $k\mid n$, 则存在 $G$ 的唯一的 $k$ 阶子群.

> **定理 1.2.22**（拉格朗日定理）设 $G$ 是有限群, $H<G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$. 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

> **基础知识**（欧拉函数）$\varphi\left(n\right)$ 为与 $n$ 互素且不超过 $n$ 的正整数的个数. 对正整数 $n$, 有 $\sum_{d\mid n}\varphi\left(d\right)=n$. $n$ 阶循环群中恰有 $\varphi\left(n\right)$ 个生成元.

### 习题一

（习题 1.5-3）设 $\left(m,n\right)=1$. 证明: $\mathbb Z_{m}\times\mathbb Z_{n}\cong\mathbb Z_{mn}$.

### 解答 习题一

考虑 $\mathbb Z_{m}\times\mathbb Z_{n}$ 中的元素 $\left(1,1\right)$. 设其阶为 $d$, 则

$$
\begin{aligned}d\left(1,1\right)&=\left(d\bmod m,d\bmod n\right)\\&=\left(0,0\right),\end{aligned}
$$

即 $m\mid d$ 且 $n\mid d$. 因 $\left(m,n\right)=1$, 故 $mn\mid d$.

另一方面, $mn\left(1,1\right)=\left(0,0\right)$, 故 $d\mid mn$.

因此 $d=mn$, 即 $\left(1,1\right)$ 的阶为 $mn$.

于是 $\left\langle\left(1,1\right)\right\rangle$ 是 $\mathbb Z_{m}\times\mathbb Z_{n}$ 的 $mn$ 阶循环子群. 而 $\left|\mathbb Z_{m}\times\mathbb Z_{n}\right|=mn$, 故 $\mathbb Z_{m}\times\mathbb Z_{n}=\left\langle\left(1,1\right)\right\rangle$ 是 $mn$ 阶循环群.

由**定理 1.5.5**（循环群的分类）, 阶相同的循环群同构, 故 $\mathbb Z_{m}\times\mathbb Z_{n}\cong\mathbb Z_{mn}$. $\blacksquare$

### 习题二

（习题 1.5-15）证明定理 1.5.8 的逆命题, 即: 设 $G$ 是 $n$ 阶群, 且对 $n$ 的每个因子 $m$ 都存在 $G$ 的唯一的 $m$ 阶子群, 则 $G$ 是循环群.

### 解答 习题二

设 $G$ 是 $n$ 阶群, 且对 $n$ 的每个因子 $d$ 都存在唯一的 $d$ 阶子群, 记为 $H_{d}$.

对每个 $d\mid n$, 令 $f\left(d\right)$ 为 $G$ 中阶恰为 $d$ 的元素的个数.

**断言** $f\left(d\right)$ 要么为 $0$, 要么为 $\varphi\left(d\right)$.

事实上, 若 $f\left(d\right)=0$, 断言显然成立. 若 $f\left(d\right)>0$, 取 $a\in G$ 使 $\mathrm{ord}\left(a\right)=d$, 则 $\left\langle a\right\rangle$ 是 $G$ 的 $d$ 阶子群. 由唯一性, $\left\langle a\right\rangle=H_{d}$, 故 $H_{d}$ 是循环群. 又 $G$ 中任意 $d$ 阶元 $b$ 生成的子群 $\left\langle b\right\rangle$ 也是 $d$ 阶的, 故 $\left\langle b\right\rangle=H_{d}$. 因此 $G$ 中所有 $d$ 阶元都在 $H_{d}$ 中, 而 $d$ 阶循环群中恰有 $\varphi\left(d\right)$ 个生成元(即 $d$ 阶元), 故 $f\left(d\right)=\varphi\left(d\right)$.

于是对每个 $d\mid n$, 有 $f\left(d\right)\le\varphi\left(d\right)$.

另一方面, 由**定理 1.2.22**（拉格朗日定理）, $G$ 中每个元素的阶都是 $n$ 的因子, 故

$$
\begin{aligned}n&=\left|G\right|\\&=\sum_{d\mid n}f\left(d\right).\end{aligned}
$$

又由数论中的恒等式 $\sum_{d\mid n}\varphi\left(d\right)=n$, 得

$$
\begin{aligned}\sum_{d\mid n}f\left(d\right)&=\sum_{d\mid n}\varphi\left(d\right)\\&=n.\end{aligned}
$$

因对每个 $d\mid n$ 都有 $f\left(d\right)\le\varphi\left(d\right)$, 而两者之和相等, 故必有 $f\left(d\right)=\varphi\left(d\right)$ 对所有 $d\mid n$ 成立.

特别地, $f\left(n\right)=\varphi\left(n\right)>0$, 故 $G$ 中存在 $n$ 阶元, 从而 $G=\left\langle a\right\rangle$ 是循环群. $\blacksquare$

### 习题三

（习题 1.5-16）设有限群 $G$ 的不同子群有不同的阶, 证明: $G$ 是循环群.

### 解答 习题三

设 $\left|G\right|=n$. 由题设, 对每个正整数 $d$, $G$ 中至多有一个 $d$ 阶子群(若有两个子阶相同, 则与题设矛盾).

对每个 $d\mid n$, 令 $f\left(d\right)$ 为 $G$ 中阶恰为 $d$ 的元素的个数.

**断言** $f\left(d\right)\le\varphi\left(d\right)$.

事实上, 若 $f\left(d\right)=0$, 结论显然. 若 $f\left(d\right)>0$, 取 $a\in G$ 使 $\mathrm{ord}\left(a\right)=d$, 则 $\left\langle a\right\rangle$ 是 $G$ 的 $d$ 阶循环子群. 由题设, $G$ 中仅有这一个 $d$ 阶子群. 于是 $G$ 中任意 $d$ 阶元 $b$ 都满足 $\left\langle b\right\rangle=\left\langle a\right\rangle$, 即 $b$ 是这个 $d$ 阶循环群的生成元. 而 $d$ 阶循环群中恰有 $\varphi\left(d\right)$ 个生成元, 故 $f\left(d\right)=\varphi\left(d\right)\le\varphi\left(d\right)$.

由**定理 1.2.22**（拉格朗日定理）, $G$ 中每个元素的阶都整除 $n$, 故

$$
\begin{aligned}n&=\left|G\right|\\&=\sum_{d\mid n}f\left(d\right)\\&\le\sum_{d\mid n}\varphi\left(d\right)\\&=n.\end{aligned}
$$

上述不等式两边相等, 故对每个 $d\mid n$, 必有 $f\left(d\right)=\varphi\left(d\right)$.

特别地, $f\left(n\right)=\varphi\left(n\right)>0$, 故 $G$ 中存在 $n$ 阶元, 从而 $G$ 是循环群. $\blacksquare$
