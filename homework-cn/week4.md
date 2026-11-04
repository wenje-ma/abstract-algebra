# week4

> **定理 1.2.22 (拉格朗日定理)**
> 
> 设 $G$ 是有限群, $H< G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, 其中 $\left[G:H\right]$ 为 $H$ 在 $G$ 中的指数. 从而子群 $H$ 的阶是群 $G$ 的阶的因子, 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

> **定理 1.4.10 (凯莱定理)**
> 
> 任何群 $G$ 与对称群 $S_G$ 的一个子群同构; 事实上映射 $L:G\to L_G$, $a\mapsto L_a$ 是单同态.

> **引理 1.4.13**
> 
> 设 $f:G\to G'$ 为群同态, 则 $\mathrm{Im}\,f< G'$, $\ker f\triangleleft G$.

> **例 1.4.17**
> 
> 设 $V$ 是数域 $P$ 上的 $n$ 维线性空间, 则映射 $\det\circ\pi:S_n\to P^{*}$, $\sigma\mapsto\det\left(\pi_\sigma\right)$ 是群同态, 其像集为 $\left\{1,-1\right\}$ (当 $n> 1$ 时), 该同态的核记为 $A_n$.

> **定理 1.4.19 (群的同态基本定理)**
> 
> 设 $f:G\to G'$ 是群的满同态, 则 $G/\ker f\cong G'$.

> **定理 1.5.5 (循环群的分类)**
> 
> 设 $G$ 是循环群. 若 $G$ 是无限群, 则 $G$ 与 $\left(\mathbb Z,+\right)$ 同构; 若 $G$ 是 $n$ 阶群, 则 $G$ 与 $\left(\mathbb Z_n,+\right)$ 同构. 从而, 两个循环群同构当且仅当它们有相同的阶.

> **定义 1.6.1 (轮换)**
> 
> 设 $\left\{i_1,i_2,\cdots,i_r\right\}\subseteq\left\{1,2,\cdots,n\right\}$. 若 $\sigma\in S_n$ 满足 $\sigma\left(i_1\right)=i_2$, $\sigma\left(i_2\right)=i_3$, ..., $\sigma\left(i_r\right)=i_1$, 且 $\sigma$ 固定其余文字, 则称 $\sigma$ 为一个 $r$-轮换, 记为 $\sigma=\left(i_1i_2\cdots i_r\right)$. 特别地, $2$-轮换称为对换.

> **定理 1.6.4 (轮换分解)**
> 
> $S_n$ 中的任何元素 $\sigma$ 都可表为 $S_n$ 中一些不相交轮换之积; 如果不计次序, 表法是唯一的.

> **引理 1.6.7 (轮换的对换分解)**
> 
> 任一个 $r$-轮换都可写成 $r-1$ 个对换的乘积: $\left(i_1i_2\cdots i_r\right)=\left(i_1i_r\right)\left(i_1i_{r-1}\right)\cdots\left(i_1i_3\right)\left(i_1i_2\right)$.

> **命题 1.6.8**
> 
> 任一 $n$ 元置换都可以表为一些对换的乘积.

> **定理 1.6.9 (交错群的单性)**
> 
> 当 $n\ge5$ 时, $A_n$ 是单群.

## 1.5-3

设 $\left(m,n\right)=1$. 证明: $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$.

### 解答 1.5-3

考虑 $\mathbb Z_m\times\mathbb Z_n$ 中的元素 $\left(\overline{1},\overline{1}\right)$. 设其阶为 $d$. 由模 $n$ 剩余类加群, $d\left(\overline{1},\overline{1}\right)=\left(d\overline{1},d\overline{1}\right)=\left(\overline{0},\overline{0}\right)$ 当且仅当 $m\mid d$ 且 $n\mid d$. 由阶的定义, $d\left(\overline{1},\overline{1}\right)=\left(\overline{0},\overline{0}\right)$, 故 $m\mid d$ 且 $n\mid d$. 因 $\left(m,n\right)=1$, 由最大公因数与最小公倍数, $mn\mid d$.

另一方面, $mn\left(\overline{1},\overline{1}\right)=\left(mn\overline{1},mn\overline{1}\right)=\left(\overline{0},\overline{0}\right)$, 故 $d\mid mn$.

因此 $d=mn$, 即 $\left(\overline{1},\overline{1}\right)$ 的阶为 $mn$.

于是 $\left\langle\left(\overline{1},\overline{1}\right)\right\rangle$ 是 $\mathbb Z_m\times\mathbb Z_n$ 的 $mn$ 阶循环子群. 而 $\left|\mathbb Z_m\times\mathbb Z_n\right|=\left|\mathbb Z_m\right|\left|\mathbb Z_n\right|=mn$, 故 $\mathbb Z_m\times\mathbb Z_n=\left\langle\left(\overline{1},\overline{1}\right)\right\rangle$, 即 $\mathbb Z_m\times\mathbb Z_n$ 是 $mn$ 阶循环群.

由**定理 1.5.5 (循环群的分类)**, 阶相同的循环群同构, 故 $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$. $\blacksquare$

## 1.5-15

证明定理 1.5.8 的逆命题, 即: 设 $G$ 是 $n$ 阶群, 且对 $n$ 的每个因子 $m$ 都存在 $G$ 的唯一的 $m$ 阶子群, 则 $G$ 是循环群.

### 解答 1.5-15

设 $G$ 是 $n$ 阶群, 且对 $n$ 的每个因子 $d$ 都存在唯一的 $d$ 阶子群, 记为 $H_d$. 对每个 $d\mid n$, 令 $f\left(d\right)$ 为 $G$ 中阶恰为 $d$ 的元素的个数.

**断言: $f\left(d\right)$ 要么为 $0$, 要么为 $\varphi\left(d\right)$.** 若 $f\left(d\right)=0$, 断言显然. 若 $f\left(d\right)> 0$, 取 $a\in G$ 使 $a$ 的阶为 $d$, 则 $\left\langle a\right\rangle$ 是 $G$ 的 $d$ 阶子群; 由唯一性, $\left\langle a\right\rangle=H_d$, 故 $H_d$ 是 $d$ 阶循环群. 对 $G$ 中任意 $d$ 阶元 $b$, $\left\langle b\right\rangle$ 也是 $G$ 的 $d$ 阶子群, 由唯一性 $\left\langle b\right\rangle=H_d$, 故 $b$ 是 $d$ 阶循环群 $H_d$ 的生成元. 由循环群的生成元个数, $d$ 阶循环群中恰有 $\varphi\left(d\right)$ 个生成元, 故 $f\left(d\right)=\varphi\left(d\right)$. 断言得证.

于是对每个 $d\mid n$, 有 $f\left(d\right)\le\varphi\left(d\right)$.

另一方面, 由**定理 1.2.22 (拉格朗日定理)**, $G$ 中每个元素的阶都是 $n$ 的因子, 故

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

又由欧拉函数与整除恒等式, $\sum_{d\mid n}\varphi\left(d\right)=n$, 故

$$
\sum_{d\mid n}f\left(d\right)=\sum_{d\mid n}\varphi\left(d\right)=n.
$$

因对每个 $d\mid n$ 都有 $f\left(d\right)\le\varphi\left(d\right)$, 而两和相等, 故对每个 $d\mid n$ 必有 $f\left(d\right)=\varphi\left(d\right)$.

特别地, $f\left(n\right)=\varphi\left(n\right)> 0$, 故 $G$ 中存在 $n$ 阶元 $a$, 从而 $\left\langle a\right\rangle$ 是 $G$ 的 $n$ 阶子群, 而 $\left|G\right|=n$, 故 $G=\left\langle a\right\rangle$ 是循环群. $\blacksquare$

## 1.5-16

设有限群 $G$ 的不同子群有不同的阶, 证明: $G$ 是循环群.

### 解答 1.5-16

设 $\left|G\right|=n$. 由题设, 对每个正整数 $d$, $G$ 中至多有一个 $d$ 阶子群 (若有两个 $d$ 阶子群, 则其阶相同, 与题设矛盾). 对每个 $d\mid n$, 令 $f\left(d\right)$ 为 $G$ 中阶恰为 $d$ 的元素的个数.

**断言: 对每个 $d\mid n$, $f\left(d\right)\le\varphi\left(d\right)$.** 若 $f\left(d\right)=0$, 断言显然. 若 $f\left(d\right)> 0$, 取 $a\in G$ 使 $a$ 的阶为 $d$, 则 $\left\langle a\right\rangle$ 是 $G$ 的 $d$ 阶循环子群. 由题设, $G$ 中至多有一个 $d$ 阶子群, 故 $G$ 中任意 $d$ 阶元 $b$ 都满足 $\left\langle b\right\rangle=\left\langle a\right\rangle$, 即 $b$ 是 $d$ 阶循环群 $\left\langle a\right\rangle$ 的生成元. 由循环群的生成元个数, $d$ 阶循环群中恰有 $\varphi\left(d\right)$ 个生成元, 故 $f\left(d\right)=\varphi\left(d\right)\le\varphi\left(d\right)$. 断言得证.

由**定理 1.2.22 (拉格朗日定理)**, $G$ 中每个元素的阶都整除 $n$, 故 $G$ 中每个元素都恰好落入某个 $d\mid n$ 的计数 $f\left(d\right)$ 中, 即

$$
n=\left|G\right|=\sum_{d\mid n}f\left(d\right).
$$

又由欧拉函数与整除恒等式, $\sum_{d\mid n}\varphi\left(d\right)=n$. 结合上述断言,

$$
n=\sum_{d\mid n}f\left(d\right)\le\sum_{d\mid n}\varphi\left(d\right)=n.
$$

上式两端相等, 故对每个 $d\mid n$ 必有 $f\left(d\right)=\varphi\left(d\right)$.

特别地, $f\left(n\right)=\varphi\left(n\right)> 0$, 故 $G$ 中存在 $n$ 阶元 $a$, 从而 $G=\left\langle a\right\rangle$ 是循环群. $\blacksquare$

## 1.6-5

证明:

$$
S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle,\quad A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle.
$$

### 解答 1.6-5

**第一部分: 证明 $S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$.** 由**命题 1.6.8**, $S_n$ 由所有对换生成. 对任意对换 $\left(ij\right)$, 其中 $i\ne1$, $j\ne1$, 由轮换的共轭, 取 $\sigma=\left(1i\right)$, 有 $\left(1i\right)\left(1j\right)\left(1i\right)=\left(\sigma\left(1\right)\sigma\left(j\right)\right)=\left(i,j\right)=\left(ij\right)$. 故任意对换 $\left(ij\right)$ 都可由 $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ 表出, 因此 $S_n\subseteq\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$; 反向包含显然, 故 $S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$.

**第二部分: 证明 $S_n=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle$.** 记 $\sigma=\left(12\cdots n\right)$. 由轮换的共轭, 对 $k=1,2,\cdots,n-1$,

$$
\sigma^{k-1}\left(12\right)\sigma^{-\left(k-1\right)}=\left(\sigma^{k-1}\left(1\right)\sigma^{k-1}\left(2\right)\right)=\left(k,k+1\right),
$$

故相邻对换 $\left(12\right),\left(23\right),\cdots,\left(n-1,n\right)$ 均属于 $\left\langle\left(12\right),\sigma\right\rangle$. 而相邻对换生成 $S_n$ (由**命题 1.6.8**, 任何对换 $\left(ij\right)$ 可表为相邻对换之积), 故 $S_n\subseteq\left\langle\left(12\right),\sigma\right\rangle$; 反向包含显然, 故 $S_n=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle$.

**第三部分: 证明 $A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$.** 由交错群由 3-轮换生成, $A_n$ 由所有 3-轮换生成. 下面证明任意 3-轮换都属于 $\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$.

(1) 含 $1$ 和 $2$ 的 3-轮换即为 $\left(12k\right)$ 或其逆, 已在生成集中.

(2) 含 $1$ 但不含 $2$ 的 3-轮换 $\left(1jk\right)$ ($j,k\ne2$): 直接计算 $\left(12k\right)\left(12j\right)^{-1}=\left(12k\right)\left(1j2\right)=\left(1jk\right)$, 故 $\left(1jk\right)$ 属于生成群.

(3) 不含 $1$ 的 3-轮换 $\left(ijk\right)$: 由 (2), $\left(1ij\right)$ 与 $\left(1ik\right)$ 均属于生成群, 于是 $\left(1ij\right)^{-1}\left(1ik\right)=\left(1ji\right)\left(1ik\right)=\left(ikj\right)$. 因 $\left(ikj\right)=\left(ijk\right)^{-1}$, 故 $\left(ijk\right)$ 属于生成群.

故所有 3-轮换都属于 $\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$, 从而 $A_n\subseteq\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$. 反之, 各生成元 $\left(12k\right)$ 都是 3-轮换, 是偶置换 (偶置换与奇置换, 交错群), 故属于 $A_n$, 反向包含成立. 因此 $A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$. $\blacksquare$

## 1.6-6

证明: $S_n$ 的非平凡正规子群为 $A_n$ 或 $K_4$ (当 $n=4$ 时).

### 解答 1.6-6

设 $N\triangleleft S_n$, $N\ne\left\{e\right\}$, $N\ne S_n$.

**情形 $n\ge5$.** 由**定理 1.6.9 (交错群的单性)**, $A_n$ 是单群. 因 $N\triangleleft S_n$ 且 $A_n\triangleleft S_n$ (由偶置换与奇置换, 交错群), 交 $N\cap A_n\triangleleft A_n$, 故由 $A_n$ 的单性, $N\cap A_n=\left\{e\right\}$ 或 $A_n$.

若 $N\cap A_n=A_n$, 则 $A_n\subseteq N$. 因 $\left|A_n\right|=\frac{n!}{2}$, $A_n$ 在 $S_n$ 中的指数为 $2$ (偶置换与奇置换, 交错群), 故包含 $A_n$ 的子群只能是 $A_n$ 或 $S_n$; 而 $N\ne S_n$, 故 $N=A_n$.

若 $N\cap A_n=\left\{e\right\}$, 则对任意 $x,y\in N\setminus\left\{e\right\}$, 因 $x,y$ 都是奇置换, $xy$ 是偶置换, 故 $xy\in N\cap A_n=\left\{e\right\}$, 于是 $y=x^{-1}$, 即 $\left|N\right|\le2$, 且 $N$ 的非单位元是二阶元. 又由正规子群是共轭类的并, $N$ 是若干共轭类之并; 因 $n\ge3$ 时 $S_n$ 的中心平凡 (群的中心与内自同构), $N$ 的非单位元 $x\ne e$ 所在的共轭类大小大于 $1$, 与 $\left|N\right|\le2$ 矛盾. 故 $N\cap A_n=\left\{e\right\}$ 不可能.

因此 $n\ge5$ 时, $S_n$ 的非平凡正规子群只有 $A_n$.

**情形 $n=4$.** $\left|S_4\right|=24$, $\left|A_4\right|=12$, $A_4\triangleleft S_4$. 由$S_4$ 的共轭类, $S_4$ 的共轭类大小分别为 $1,6,3,8,6$; 由正规子群是共轭类的并及**定理 1.2.22 (拉格朗日定理)**, 正规子群的阶必为若干共轭类大小之和且整除 $24$, 可能的阶为 $1,4,12,24$, 对应正规子群 $\left\{e\right\}$, $K_4$, $A_4$, $S_4$. 故非平凡正规子群为 $A_4$ 与 $K_4$.

**情形 $n=3$.** $\left|S_3\right|=6$, $\left|A_3\right|=3$, $A_3\triangleleft S_3$ 且指数为 $2$. 由正规子群是共轭类的并, $S_3$ 的共轭类大小分别为 $1,3,2$, 可能组成正规子群的阶为 $1,3,6$, 故正规子群为 $\left\{e\right\},A_3,S_3$, 非平凡者为 $A_3$.

**情形 $n\le2$.** $S_n$ 无非平凡正规子群.

综上, $S_n$ 的非平凡正规子群为 $A_n$ (对所有 $n\ge3$), 以及 $n=4$ 时的 $K_4$. $\blacksquare$

## 1.6-11

设 $\left|G\right|=2n$, 其中 $n$ 为奇数. 证明: $G$ 有指数为 $2$ 的正规子群.

### 解答 1.6-11

**第一步: 构造群同态 $\psi:G\to\left\{1,-1\right\}$.** 由**定理 1.4.10 (凯莱定理)**, 左正则表示 $\lambda:G\to S_G$, $g\mapsto L_g$ (其中 $L_g\left(x\right)=gx$) 是单同态; 视 $S_G$ 为 $S_{2n}$ (因 $\left|G\right|=2n$). 由**例 1.4.17** 及符号同态, 符号同态 $\mathrm{sgn}:S_{2n}\to\left\{1,-1\right\}$ 是群同态. 复合得 $\psi=\mathrm{sgn}\circ\lambda:G\to\left\{1,-1\right\}$ 是群同态.

**第二步: 证明 $\psi$ 是满射.** 由偶数阶群有二阶元, $G$ 中存在二阶元 $a$ (因 $\left|G\right|=2n$ 为偶数). 则 $\lambda\left(a\right)=L_a$, 且对任意 $x\in G$, $L_a^2\left(x\right)=a^2x=x$, 故 $L_a$ 是对合; 又 $a\ne e$, 若 $L_a\left(x\right)=x$ 即 $ax=x$, 则 $a=e$, 矛盾, 故 $L_a$ 无不动点. 因此 $L_a$ 是 $G$ (共 $2n$ 个文字) 上的 $n$ 个不相交对换之积, 由符号同态, $\mathrm{sgn}\left(L_a\right)=\left(-1\right)^{n}=-1$ (因 $n$ 为奇数). 故 $\psi\left(a\right)=-1$, 而 $\psi\left(e\right)=1$, 于是 $\psi:G\to\left\{1,-1\right\}$ 是满同态.

**第三步: 取核得指数为 $2$ 的正规子群.** 令 $H=\ker\psi$. 由**引理 1.4.13**, $H\triangleleft G$. 由**定理 1.4.19 (群的同态基本定理)**, $G/H\cong\left\{1,-1\right\}$, 故 $\left|G/H\right|=2$, 即 $\left[G:H\right]=2$. 因此 $G$ 有指数为 $2$ 的正规子群 $H$. $\blacksquare$
