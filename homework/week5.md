# week5

> **定理 1.10.10 (西罗第三定理)**
> 
> 设 $G$ 的西罗 $p$-子群的个数为 $n_{p}$, 则 (1) $G$ 的西罗 $p$-子群 $P\triangleleft{}G$ 当且仅当 $n_{p}=1$; (2) $n_{p}\mid{}m$ 且 $n_{p}\equiv1\pmod{p}$, 其中 $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$. $\left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}$. $\left(a-b\right)^{n}=\sum_{k=0}^{n}\binom{n}{k}a^{k}\left(-b\right)^{n-k}$, 且 $R$ 交换保证各项可以合并.

> **定义 2.1.1 (环)**
> 
> 设 $R$ 是非空集合, 在 $R$ 上定义两种二元运算 $+$ 与 $\cdot$, 满足: (1) $\left[R;+\right]$ 是交换群; (2) $\left[R;\cdot\right]$ 是半群; (3) 乘法对加法满足左右分配律: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$. 则称 $R$ 为一个环.

> **定义 2.1.8 (无零因子环)**
> 
> 如果环 $R$ 不是零环且没有零因子, 则称 $R$ 为无零因子环.

> **命题 2.2.11 (理想判别法)**
> 
> 设 $R$ 为环, $I$ 为 $R$ 的非空子集, 则 $I$ 为 $R$ 的理想的充分必要条件是 $a-b\in{}I$ 且 $ax,ya\in{}I$ 对一切 $a,b\in{}I$, $x,y\in{}R$ 成立.

> **定理 2.2.16 (商环)**
> 
> 设 $R$ 是一个环, $I$ 是 $R$ 的理想, 则商加法群 $R/I$ 在乘法 $\left(a+I\right)\left(b+I\right)=ab+I$ 下构成一个环, 称为 $R$ 对 $I$ 的商环.

> **定义 2.2.20 (整环,除环与域)**
> 
> 无零因子的交换幺环称为整环; 若幺环 $R$ 满足 $R^{*}$ 对乘法构成群 (其中 $R^{*}=R\setminus\left\{0\right\}$), 则称 $R$ 为除环; 交换的除环称为域.

## 1.10-12

(弗拉蒂尼) 设 $N\triangleleft{}G$, $P$ 为 $N$ 的西罗子群, 则 $G=N_{G}\left(P\right)N$.

### 解答 1.10-12

任取 $g\in{}G$. 因 $N\triangleleft{}G$, 共轭 $gPg^{-1}$ 仍为 $N$ 的子群; 又共轭保持阶, 由西罗子群与元素计数, $\left|gPg^{-1}\right|=\left|P\right|$, 故 $gPg^{-1}$ 也是 $N$ 的一个西罗 $p$-子群.

由**定理 1.10.8 (西罗第二定理)** (应用于子群 $N$), $N$ 的任意两个西罗 $p$-子群在 $N$ 中共轭, 故存在 $n\in{}N$ 使

$$
gPg^{-1}=nPn^{-1}.$
$
于是
$$

n^{-1}gPg^{-1}n=P, $

$

即 $n^{-1}g\in{}N_{G}\left(P\right)$ (它把 $P$ 共轭回 $P$). 记 $h=n^{-1}g\in{}N_{G}\left(P\right)$, 则 $g=nh$.

因此 $g\in{}N_{G}\left(P\right)N$. 由 $g\in{}G$ 的任意性, $G=N_{G}\left(P\right)N$.

$\blacksquare$

## 1.10-15

设 $p,q$ 都是素数, $p<{}q$, $p\nmid\left(q-1\right)$, 证明 $pq$ 阶群一定是循环群.

### 解答 1.10-15

设 $\left|G\right|=pq$. 由**定理 1.10.10 (西罗第三定理)**, 西罗 $q$-子群的个数 $n_{q}$ 满足 $n_{q}\mid{}p$ 且 $n_{q}\equiv1\pmod{q}$. 因 $p<{}q$, 如 1.10-10 题所示, $n_{q}=1$. 故 $G$ 的西罗 $q$-子群 $Q$ 唯一, 由**定理 1.10.10 (西罗第三定理)** (1), $Q\triangleleft{}G$, $\left|Q\right|=q$.

再考虑西罗 $p$-子群的个数 $n_{p}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{p}\mid{}q$ 且 $n_{p}\equiv1\pmod{p}$. 因 $q$ 为素数, $n_{p}=1$ 或 $q$. 若 $n_{p}=q$, 则 $q\equiv1\pmod{p}$, 即 $p\mid\left(q-1\right)$, 与题设 $p\nmid\left(q-1\right)$ 矛盾. 故 $n_{p}=1$.

于是 $G$ 的西罗 $p$-子群 $P$ 也唯一, 由**定理 1.10.10 (西罗第三定理)** (1), $P\triangleleft{}G$, $\left|P\right|=p$.

因 $p,q$ 互素, $P\cap{}Q=\left\{e\right\}$. 又

$$
\left|PQ\right|=\left|P\right|\left|Q\right|/\left|P\cap{}Q\right|=pq=\left|G\right|,
$$

故 $G=PQ$.

由**引理 1.7.7**, $P,Q$ 都是 $G$ 的正规子群且 $P\cap{}Q=\left\{e\right\}$, 故对任意 $a\in{}P$, $b\in{}Q$ 有 $ab=ba$. 于是映射

$$
P\times{}Q\to{}G,\quad\left(a,b\right)\mapsto{}ab
$$

保持乘法 (因 $ab=ba$) 且为双射 (单射由 $P\cap{}Q=\left\{e\right\}$, 满射由 $G=PQ$), 故它是群同构, 即 $G\cong{}P\times{}Q$.

又 $P\cong\mathbb{Z}_p$, $Q\cong\mathbb{Z}_q$, 而 $p,q$ 互素, 由直积中元素的阶, $\mathbb{Z}_p\times\mathbb{Z}_q\cong\mathbb{Z}_{pq}$, 故

$$
G\cong\mathbb{Z}_p\times\mathbb{Z}_q\cong\mathbb{Z}_{pq},
$$

即 $G$ 是 $pq$ 阶循环群.

$\blacksquare$

## 1.10-20

证明: $60$ 阶非阿贝尔有限单群必同构于 $A_5$.

### 解答 1.10-20

设 $G$ 是 $60$ 阶非阿贝尔单群. 先求西罗 $5$-子群的个数 $n_{5}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{5}\mid12$ 且 $n_{5}\equiv1\pmod5$, 故 $n_{5}=1$ 或 $6$. 由西罗子群与元素计数, $G$ 单故 $n_{5}\ne1$, 于是 $n_{5}=6$.

每个西罗 $5$-子群是 $5$ 阶循环群, 由西罗子群与元素计数, 含 $4$ 个 $5$ 阶元; 两个不同的西罗 $5$-子群交为 $\left\{e\right\}$ (交的阶同时整除 $5$, 故只能为 $1$). 因此 $G$ 中共有 $6\times4=24$ 个 $5$ 阶元.

再考虑西罗 $2$-子群的个数 $n_{2}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{2}\mid15$ 且 $n_{2}\equiv1\pmod2$, 故 $n_{2}\in\left\{1,3,5,15\right\}$. 由西罗子群与元素计数, $G$ 单故 $n_{2}\ne1$.

排除 $n_{2}=3$. 由群在陪集空间上的作用, $G$ 通过共轭作用在 $3$ 个西罗 $2$-子群上, 给出同态 $\pi:G\to{}S_3$. 其核 $\ker\pi$ 是 $G$ 的正规子群. 因 $G$ 单, $\ker\pi=\left\{e\right\}$ 或 $G$. 作用可递故非平凡, $\ker\pi\ne{}G$; 若 $\ker\pi=\left\{e\right\}$, 则 $G$ 同构于 $S_3$ 的子群, 而 $\left|S_3\right|=6<60$, 矛盾. 故 $n_{2}\ne3$.

处理 $n_{2}=5$. 由群在陪集空间上的作用, $G$ 共轭作用在 $5$ 个西罗 $2$-子群上, 给出同态 $\pi:G\to{}S_5$. 同理 $\ker\pi$ 为正规子群且非 $G$; 若 $\ker\pi=\left\{e\right\}$, 则 $G$ 同构于 $S_5$ 的一个 $60$ 阶子群. $S_5$ 的阶为 $120$, 该 $60$ 阶子群指数为 $2$, 由指数为 $2$ 的子群与 $S_n$ 的交错子群 必为正规子群且唯一, 即 $A_5$. 故 $G\cong{}A_5$, 结论成立.

排除 $n_{2}=15$. 若任意两个不同的西罗 $2$-子群交为 $\left\{e\right\}$, 则每个 $4$ 阶西罗 $2$-子群贡献 $3$ 个非单位元 (由$4$ 阶群是交换群 与西罗子群与元素计数), 共 $15\times3=45$ 个 $2$ 阶或 $4$ 阶元, 加上 $24$ 个 $5$ 阶元, 总数 $45+24=69>60$, 矛盾. 故存在两个不同的西罗 $2$-子群 $P,Q$ 使 $\left|P\cap{}Q\right|=2$.

设 $P\cap{}Q=\left\langle{}x\right\rangle$, 其中 $x$ 为 $2$ 阶元. 因 $P,Q$ 均为 $4$ 阶群, 由$4$ 阶群是交换群 皆交换, 且 $x\in{}P\cap{}Q$, 故 $P,Q\subseteq{}N_{G}\left(\left\langle{}x\right\rangle\right)$. 又 $P\ne{}Q$, 故 $\left|N_{G}\left(\left\langle{}x\right\rangle\right)\right|>4$. 同时 $\left|N_{G}\left(\left\langle{}x\right\rangle\right)\right|\mid60$ 且被 $4$ 整除 (因含 $4$ 阶子群 $P$), 故只能为 $12,20$ 或 $60$. 若为 $60$, 则 $\left\langle{}x\right\rangle\triangleleft{}G$, 与 $G$ 单矛盾. 故 $\left|N_{G}\left(\left\langle{}x\right\rangle\right)\right|=12$ 或 $20$, 对应指数 $5$ 或 $3$.

指数 $3$ 时, 由群在陪集空间上的作用, $G$ 左平移作用在 $3$ 个陪集上给出同态 $G\to{}S_3$, 与前述 $n_{2}=3$ 的矛盾相同, 故指数必为 $5$. 于是 $G$ 有指数 $5$ 的子群 $N_{G}\left(\left\langle{}x\right\rangle\right)$; 由群在陪集空间上的作用, $G$ 左平移作用在 $5$ 个陪集上给出同态 $G\to{}S_5$, 其核为正规子群且非 $G$, 因 $G$ 单故核为 $\left\{e\right\}$, 得单同态 $G\hookrightarrow{}S_5$. 如前所述, $S_5$ 的 $60$ 阶子群只能是 $A_5$, 故 $G\cong{}A_5$.

$\blacksquare$

## 2.1-3

设集合 $R=\left\{a,b,c\right\}$, 在 $R$ 上定义加法和乘法. 若加法 $+$ 和乘法 $\cdot$ 的运算表分别为

$$
\begin{array}{c\left|ccc}
+&a&b&c\\\hline
a&a&b&c\\
b&b&c&a\\
c&c&a&b
\end{array}
\quad
\begin{array}{c\right|ccc}
\cdot&a&b&c\\\hline
a&a&a&a\\
b&a&a&a\\
c&a&b&a
\end{array}
$$

问 $R$ 是否构成环?

### 解答 2.1-3

由加法表可见, $a$ 是加法零元, 且 $\left(R,+\right)\cong\mathbb{Z}_3$ (对应 $a\mapsto0$, $b\mapsto1$, $c\mapsto2$), 故 $\left(R,+\right)$ 是交换群, 满足**定义 2.1.1 (环)** 的条件 (1).

下面检验分配律. 取 $x=b$, $y=c$, $z=b$. 由加法表, $b+c=a$; 由乘法表, $a\cdot{}b=a$, $b\cdot{}b=a$, $c\cdot{}b=b$.

先算左边:

$$
\left(x+y\right)z=\left(b+c\right)b=a\cdot{}b=a.
$$

再算右边:

$$
xz+yz=b\cdot{}b+c\cdot{}b=a+b=b.
$$

因 $a\ne{}b$, 故

$$
\left(b+c\right)b\ne{}b\cdot{}b+c\cdot{}b.
$$

左分配律不成立.

此外, 乘法的结合律亦不成立: 取 $x=c$, $y=c$, $z=b$, 由乘法表 $c\cdot{}c=a$, $c\cdot{}b=b$, $a\cdot{}b=a$, 则

$$
\left(c\cdot{}c\right)\cdot{}b=a\cdot{}b=a,
$$

而

$$
c\cdot\left(c\cdot{}b\right)=c\cdot{}b=b.
$$

二者不等.

因此 $R$ 不满足**定义 2.1.1 (环)** 中的乘法结合律与分配律, $R$ 不构成环.

$\blacksquare$

## 2.1-5

设 $R$ 为幺环, $e$ 为幺元, $a\in{}R$. 若存在 $m\in\mathbb{N}$ 使得 $a^{m}=0$, 则称 $a$ 为幂零元. 证明: 若 $a$ 为幂零元, 则 $e+a$ 为可逆元.

### 解答 2.1-5

设 $a^{m}=0$. 构造

$$
b=e-a+a^{2}-a^{3}+\cdots+\left(-1\right)^{m-1}a^{m-1}.
$$

计算乘积 (利用**定义 2.1.1 (环)** 的分配律展开):

$$
\left(e+a\right)b=\left(e+a\right)\left(e-a+a^{2}-\cdots+\left(-1\right)^{m-1}a^{m-1}\right)=e+\left(-1\right)^{m-1}a^{m}=e,
$$

中间项全部抵消, 而 $a^{m}=0$. 同理,

$$
b\left(e+a\right)=\left(e-a+a^{2}-\cdots+\left(-1\right)^{m-1}a^{m-1}\right)\left(e+a\right)=e+\left(-1\right)^{m-1}a^{m}=e.
$$

故 $b$ 是 $e+a$ 的逆元, 即 $e+a$ 为可逆元. 这与幂零元与有限几何级数 的结论一致.

$\blacksquare$

## 2.1-15

(华罗庚) 设 $R$ 为幺环, $e$ 为幺元, $a\in{}R$. 若元素 $c$ 满足 $ca=e$ ($ac=e$), 则称 $c$ 为 $a$ 的一个左逆元 (右逆元). 若 $c$ 既是 $a$ 的左逆元, 又是 $a$ 的右逆元, 则称 $c$ 为 $a$ 的逆元, 这时称 $a$ 可逆. 证明: 对任何 $a,b\in{}R$, $e-ab$ 可逆当且仅当 $e-ba$ 可逆.

### 解答 2.1-15

先设 $e-ab$ 可逆, 记其逆为 $c=\left(e-ab\right)^{-1}$. 构造

$$
d=e+bca.
$$

验证 $d$ 是 $e-ba$ 的逆元. 利用**定义 2.1.1 (环)** 的分配律展开:

$$
\left(e-ba\right)d=\left(e-ba\right)\left(e+bca\right)=e-ba+bca-babca=e-ba+b\left(e-ab\right)ca=e-ba+ba=e,
$$

其中用到 $\left(e-ab\right)c=e$. 同理,

$$
d\left(e-ba\right)=\left(e+bca\right)\left(e-ba\right)=e-ba+bca-bcaba=e-ba+bc\left(e-ab\right)a=e-ba+ba=e,
$$

其中用到 $c\left(e-ab\right)=e$. 故 $d=e+bca$ 是 $e-ba$ 的逆元, 于是 $e-ba$ 可逆.

反之, 若 $e-ba$ 可逆, 将上述论证中 $a,b$ 互换, 即得 $e-ab$ 可逆.

因此 $e-ab$ 可逆当且仅当 $e-ba$ 可逆.

$\blacksquare$
