# week5

> **基础知识: 模 $n$ 剩余类加群**<br>$\mathbb Z_n=\left\{\overline{0},\overline{1},\cdots,\overline{n-1}\right\}$ 对加法构成 $n$ 阶循环群, 生成元为 $\overline{1}$; 对整数 $k$, $k\overline{1}=\overline{0}$ 当且仅当 $n\mid k$. 对 $\left(\overline{x},\overline{y}\right)\in\mathbb Z_m\times\mathbb Z_n$, $k\left(\overline{x},\overline{y}\right)=\left(\overline{0},\overline{0}\right)$ 当且仅当 $m\mid kx$ 且 $n\mid ky$.

> **基础知识: 循环群的生成元个数**<br>设 $C$ 是 $d$ 阶循环群, 则 $C$ 中阶恰为 $d$ 的元素 (即生成元) 恰有 $\varphi\left(d\right)$ 个, 其中 $\varphi$ 为欧拉函数.

> **基础知识: 欧拉函数与整除恒等式**<br>$\varphi\left(n\right)$ 为与 $n$ 互素且不超过 $n$ 的正整数的个数; 对正整数 $n$, 有 $\sum_{d\mid n}\varphi\left(d\right)=n$.

> **基础知识: 最大公因数与最小公倍数**<br>对正整数 $m,n$, 若 $\left(m,n\right)=1$, 则 $m\mid k$ 且 $n\mid k$ 当且仅当 $mn\mid k$.

> **定理 1.2.22 (拉格朗日定理)**<br>设 $G$ 是有限群, $H<G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, 其中 $\left[G:H\right]$ 为 $H$ 在 $G$ 中的指数. 从而子群 $H$ 的阶是群 $G$ 的阶的因子, 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

> **定理 1.5.5 (循环群的分类)**<br>设 $G$ 是循环群. 若 $G$ 是无限群, 则 $G$ 与 $\left(\mathbb Z,+\right)$ 同构; 若 $G$ 是 $n$ 阶群, 则 $G$ 与 $\left(\mathbb Z_n,+\right)$ 同构. 从而, 两个循环群同构当且仅当它们有相同的阶.

---

## 1.5-3

设 $\left(m,n\right)=1$. 证明: $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$.

### 解答 1.5-3

考虑 $\mathbb Z_m\times\mathbb Z_n$ 中的元素 $\left(\overline{1},\overline{1}\right)$. 设其阶为 $d$. 由**基础知识: 模 $n$ 剩余类加群**, $d\left(\overline{1},\overline{1}\right)=\left(d\overline{1},d\overline{1}\right)=\left(\overline{0},\overline{0}\right)$ 当且仅当 $m\mid d$ 且 $n\mid d$. 由阶的定义, $d\left(\overline{1},\overline{1}\right)=\left(\overline{0},\overline{0}\right)$, 故 $m\mid d$ 且 $n\mid d$. 因 $\left(m,n\right)=1$, 由**基础知识: 最大公因数与最小公倍数**, $mn\mid d$.

另一方面, $mn\left(\overline{1},\overline{1}\right)=\left(mn\overline{1},mn\overline{1}\right)=\left(\overline{0},\overline{0}\right)$, 故 $d\mid mn$.

因此 $d=mn$, 即 $\left(\overline{1},\overline{1}\right)$ 的阶为 $mn$.

于是 $\left\langle\left(\overline{1},\overline{1}\right)\right\rangle$ 是 $\mathbb Z_m\times\mathbb Z_n$ 的 $mn$ 阶循环子群. 而 $\left|\mathbb Z_m\times\mathbb Z_n\right|=\left|\mathbb Z_m\right|\left|\mathbb Z_n\right|=mn$, 故 $\mathbb Z_m\times\mathbb Z_n=\left\langle\left(\overline{1},\overline{1}\right)\right\rangle$, 即 $\mathbb Z_m\times\mathbb Z_n$ 是 $mn$ 阶循环群.

由**定理 1.5.5 (循环群的分类)**, 阶相同的循环群同构, 故 $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$. $\blacksquare$

---

## 1.5-15

证明定理 1.5.8 的逆命题, 即: 设 $G$ 是 $n$ 阶群, 且对 $n$ 的每个因子 $m$ 都存在 $G$ 的唯一的 $m$ 阶子群, 则 $G$ 是循环群.

### 解答 1.5-15

设 $G$ 是 $n$ 阶群, 且对 $n$ 的每个因子 $d$ 都存在唯一的 $d$ 阶子群, 记为 $H_d$. 对每个 $d\mid n$, 令 $f\left(d\right)$ 为 $G$ 中阶恰为 $d$ 的元素的个数.

**断言: $f\left(d\right)$ 要么为 $0$, 要么为 $\varphi\left(d\right)$.** 若 $f\left(d\right)=0$, 断言显然. 若 $f\left(d\right)>0$, 取 $a\in G$ 使 $a$ 的阶为 $d$, 则 $\left\langle a\right\rangle$ 是 $G$ 的 $d$ 阶子群; 由唯一性, $\left\langle a\right\rangle=H_d$, 故 $H_d$ 是 $d$ 阶循环群. 对 $G$ 中任意 $d$ 阶元 $b$, $\left\langle b\right\rangle$ 也是 $G$ 的 $d$ 阶子群, 由唯一性 $\left\langle b\right\rangle=H_d$, 故 $b$ 是 $d$ 阶循环群 $H_d$ 的生成元. 由**基础知识: 循环群的生成元个数**, $d$ 阶循环群中恰有 $\varphi\left(d\right)$ 个生成元, 故 $f\left(d\right)=\varphi\left(d\right)$. 断言得证.

于是对每个 $d\mid n$, 有 $f\left(d\right)\le\varphi\left(d\right)$.

另一方面, 由**定理 1.2.22 (拉格朗日定理)**, $G$ 中每个元素的阶都是 $n$ 的因子, 故

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

又由**基础知识: 欧拉函数与整除恒等式**, $\sum_{d\mid n}\varphi\left(d\right)=n$, 故

$$
\sum_{d\mid n}f\left(d\right)=\sum_{d\mid n}\varphi\left(d\right)=n.
$$

因对每个 $d\mid n$ 都有 $f\left(d\right)\le\varphi\left(d\right)$, 而两和相等, 故对每个 $d\mid n$ 必有 $f\left(d\right)=\varphi\left(d\right)$.

特别地, $f\left(n\right)=\varphi\left(n\right)>0$, 故 $G$ 中存在 $n$ 阶元 $a$, 从而 $\left\langle a\right\rangle$ 是 $G$ 的 $n$ 阶子群, 而 $\left|G\right|=n$, 故 $G=\left\langle a\right\rangle$ 是循环群. $\blacksquare$

---

## 1.5-16

设有限群 $G$ 的不同子群有不同的阶, 证明: $G$ 是循环群.

### 解答 1.5-16

设 $\left|G\right|=n$. 由题设, 对每个正整数 $d$, $G$ 中至多有一个 $d$ 阶子群 (若有两个 $d$ 阶子群, 则其阶相同, 与题设矛盾). 对每个 $d\mid n$, 令 $f\left(d\right)$ 为 $G$ 中阶恰为 $d$ 的元素的个数.

**断言: 对每个 $d\mid n$, $f\left(d\right)\le\varphi\left(d\right)$.** 若 $f\left(d\right)=0$, 断言显然. 若 $f\left(d\right)>0$, 取 $a\in G$ 使 $a$ 的阶为 $d$, 则 $\left\langle a\right\rangle$ 是 $G$ 的 $d$ 阶循环子群. 由题设, $G$ 中至多有一个 $d$ 阶子群, 故 $G$ 中任意 $d$ 阶元 $b$ 都满足 $\left\langle b\right\rangle=\left\langle a\right\rangle$, 即 $b$ 是 $d$ 阶循环群 $\left\langle a\right\rangle$ 的生成元. 由**基础知识: 循环群的生成元个数**, $d$ 阶循环群中恰有 $\varphi\left(d\right)$ 个生成元, 故 $f\left(d\right)=\varphi\left(d\right)\le\varphi\left(d\right)$. 断言得证.

由**定理 1.2.22 (拉格朗日定理)**, $G$ 中每个元素的阶都整除 $n$, 故 $G$ 中每个元素都恰好落入某个 $d\mid n$ 的计数 $f\left(d\right)$ 中, 即

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

又由**基础知识: 欧拉函数与整除恒等式**, $\sum_{d\mid n}\varphi\left(d\right)=n$. 结合上述断言,

$$
n=\sum_{d\mid n}f\left(d\right)\le\sum_{d\mid n}\varphi\left(d\right)=n.
$$

上式两端相等, 故对每个 $d\mid n$ 必有 $f\left(d\right)=\varphi\left(d\right)$.

特别地, $f\left(n\right)=\varphi\left(n\right)>0$, 故 $G$ 中存在 $n$ 阶元 $a$, 从而 $G=\left\langle a\right\rangle$ 是循环群. $\blacksquare$
