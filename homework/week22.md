# 作业 22

> **定理 3.5.2**（有限交换群的分类数）设自然数 $n$ 有素因数分解 $n=p_1^{m_1}p_2^{m_2}\cdots p_s^{m_s}$, 其中 $p_1,p_2,\cdots,p_s$ 为互不相同的素数, $m_i>0$, 则在同构意义下 $n$ 阶交换群的个数为 $\prod_{i=1}^s p\left(m_i\right)$, 其中 $p\left(m\right)$ 表示自然数 $m$ 的不同分划的个数.

> **基础知识**（直积中元素的阶）设 $G=H_1\times H_2\times\cdots\times H_s$ 为有限交换群的直积, $g=\left(h_1,h_2,\cdots,h_s\right)$, 则 $o\left(g\right)=\mathrm{lcm}\left(o\left(h_1\right),o\left(h_2\right),\cdots,o\left(h_s\right)\right)$. 特别地, $o\left(g\right)\mid q$ 当且仅当 $o\left(h_i\right)\mid q$ 对每个 $i$ 成立.

> **基础知识**（有理数乘法群的有限子群）乘法群 $\mathbb Q^*$ 中任一元素的阶有限当且仅当该元素为 $1$ 或 $-1$, 即 $\mathbb Q^*$ 的唯一有限子群为 $\left\{\pm1\right\}$. 事实上, 若 $r=p/q\in\mathbb Q^*$（既约）满足 $r^n=1$, 则 $p^n=q^n$, 故 $p=\pm q$, 即 $r=\pm1$.

### 习题一

（习题 3.5-4）试决定同构意义下 $936$ 阶交换群的类数.

### 解答 习题一

先对 $936$ 作素因数分解. 因

$$
\begin{aligned}936&=8\times117\\&=2^3\times3^2\times13.\end{aligned}
$$

即 $936=2^3\cdot3^2\cdot13^1$.

计算各指数的分划数. 指数 $3$ 的分划为 $3$, $2+1$, $1+1+1$, 共 $p\left(3\right)=3$ 种; 指数 $2$ 的分划为 $2$, $1+1$, 共 $p\left(2\right)=2$ 种; 指数 $1$ 的分划仅 $1$ 一种, 故 $p\left(1\right)=1$.

由**定理 3.5.2**（有限交换群的分类数）, 同构意义下 $936$ 阶交换群的个数为

$$
\begin{aligned}p\left(3\right)p\left(2\right)p\left(1\right)&=3\times2\times1\\&=6.\end{aligned}
$$

故同构意义下 $936$ 阶交换群共有 $6$ 类. $\blacksquare$

### 习题二

（习题 3.5-8）（1）设 $G=\mathbb Z_{p^e}$, $p$ 为素数, $e>0$. 记 $G$ 中元素 $g$ 的阶为 $o\left(g\right)$. 试证明: 若 $l\leqslant e$, 则 $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l$; 若 $l>e$, 则 $\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^e$.

（2）设 $H_1,H_2,\cdots,H_s$ 为有限交换群, $q$ 为自然数, 令 $m_i=\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|$, $G=H_1\times H_2\times\cdots\times H_s$, 则 $\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|=m_1m_2\cdots m_s$.

（3）试决定 $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ 中有多少个元素的阶能整除 $4$.

### 解答 习题二

（1）将 $G=\mathbb Z_{p^e}$ 视为加法循环群, 其元素为 $0,1,2,\cdots,p^e-1$ 模 $p^e$. 对 $g=k\in\mathbb Z_{p^e}$, 有

$$
o\left(g\right)=\frac{p^e}{\gcd\left(k,p^e\right)}.
$$

于是 $o\left(g\right)\mid p^l$ 等价于 $p^l g=0$, 即 $p^l k\equiv0\pmod{p^e}$.

当 $l\leqslant e$ 时, 上式等价于 $k$ 被 $p^{e-l}$ 整除. 在模 $p^e$ 的剩余类中, 被 $p^{e-l}$ 整除的剩余类恰有 $p^l$ 个, 故

$$
\left|\left\{g\in G\mid o\left(g\right)\mid p^l\right\}\right|=p^l.
$$

当 $l>e$ 时, $p^l$ 是 $p^e$ 的倍数, $p^l g=0$ 对一切 $g\in G$ 自动成立, 故该集合即 $G$ 本身, 其元素个数为 $p^e$.

（2）任取 $g=\left(h_1,h_2,\cdots,h_s\right)\in G$. 由**基础知识**（直积中元素的阶）, $o\left(g\right)\mid q$ 当且仅当 $o\left(h_i\right)\mid q$ 对每个 $i$ 同时成立. 因而满足条件的 $g$ 恰为各分量分别取自对应集合 $\left\{h\in H_i\mid o\left(h\right)\mid q\right\}$ 的直积, 由乘法原理得

$$
\begin{aligned}\left|\left\{g\in G\mid o\left(g\right)\mid q\right\}\right|&=\prod_{i=1}^s\left|\left\{h\in H_i\mid o\left(h\right)\mid q\right\}\right|\\&=m_1m_2\cdots m_s.\end{aligned}
$$

（3）在 $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ 中, 要求元素的阶整除 $4$, 即 $4g=0$. 分别计算各分量的可选个数.

对 $\mathbb Z_4$, 群阶为 $4$, 故 $4g=0$ 对所有 $4$ 个元素都成立, $m_1=4$.

对 $\mathbb Z_8$, $4k\equiv0\pmod 8$ 等价于 $k$ 为偶数, 即 $k\in\left\{0,2,4,6\right\}$, 共 $4$ 个, $m_2=4$.

对 $\mathbb Z_{16}$, $4k\equiv0\pmod{16}$ 等价于 $k\equiv0\pmod 4$, 即 $k\in\left\{0,4,8,12\right\}$, 共 $4$ 个, $m_3=4$.

由（2）, 所求元素个数为

$$
\begin{aligned}m_1m_2m_3&=4\times4\times4\\&=64.\end{aligned}
$$

故 $\mathbb Z_4\times\mathbb Z_8\times\mathbb Z_{16}$ 中有 $64$ 个元素的阶能整除 $4$. $\blacksquare$

### 习题三

（习题 3.5-12）试给出 $8$ 阶交换群的分类, 并决定所有这些群到 $\mathbb Q^*$ 的同态.

### 解答 习题三

因 $8=2^3$, 指数 $3$ 的分划为 $3$, $2+1$, $1+1+1$, 共 $p\left(3\right)=3$ 种. 由**定理 3.5.2**（有限交换群的分类数）, $8$ 阶交换群在同构意义下共有 $3$ 类, 分别为

$$
\mathbb Z_8,\quad\mathbb Z_4\times\mathbb Z_2,\quad\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2.
$$

下面分别决定它们到 $\mathbb Q^*$ 的同态. 设 $\varphi:G\to\mathbb Q^*$ 为群同态. 因 $G$ 有限, $\varphi\left(G\right)$ 是 $\mathbb Q^*$ 的有限子群. 由**基础知识**（有理数乘法群的有限子群）, $\mathbb Q^*$ 的唯一有限子群为 $\left\{\pm1\right\}$, 故 $\varphi\left(G\right)\subseteq\left\{\pm1\right\}$, 即每个生成元的像只能取 $1$ 或 $-1$.

**情形一 $G=\mathbb Z_8$** 设 $g$ 为 $G$ 的生成元, $o\left(g\right)=8$. 同态 $\varphi$ 由 $\varphi\left(g\right)\in\left\{\pm1\right\}$ 唯一确定, 且 $\varphi\left(g\right)^8=1$ 对 $\pm1$ 自动成立. 故共有 $2$ 个同态.

**情形二 $G=\mathbb Z_4\times\mathbb Z_2$** 设 $g_1$ 为 $\mathbb Z_4$ 的生成元, $g_2$ 为 $\mathbb Z_2$ 的生成元. 同态由 $\varphi\left(g_1\right),\varphi\left(g_2\right)\in\left\{\pm1\right\}$ 唯一确定, 且约束 $\varphi\left(g_1\right)^4=1$, $\varphi\left(g_2\right)^2=1$ 对 $\pm1$ 自动满足. 故共有 $2\times2=4$ 个同态.

**情形三 $G=\mathbb Z_2\times\mathbb Z_2\times\mathbb Z_2$** 设 $g_1,g_2,g_3$ 为三个 $2$ 阶生成元. 同态由 $\varphi\left(g_1\right),\varphi\left(g_2\right),\varphi\left(g_3\right)\in\left\{\pm1\right\}$ 唯一确定, 约束均自动满足. 故共有 $2^3=8$ 个同态.

综上, $8$ 阶交换群共 $3$ 类, 它们到 $\mathbb Q^*$ 的同态个数分别为 $2$, $4$, $8$. $\blacksquare$
