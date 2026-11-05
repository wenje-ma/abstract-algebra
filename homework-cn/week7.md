# week7

> **引理 1.7.7**
> 
> 设 $A,B$ 是 $G$ 的子群, $G=AB$, $A\cap{B}=\left\{e\right\}$, 则 $A,B$ 都是 $G$ 的正规子群当且仅当对任意 $a\in{A}$, $b\in{B}$ 有 $ab=ba$.

> **引理 1.8.8 (可解群的遗传性)**
> 
> 可解群的子群,商群都是可解群; 反之, 设 $N\trianglelefteq{G}$, 且 $N$ 与 $G/N$ 都可解, 则 $G$ 可解.

> **定理 1.10.8 (西罗第二定理)**
> 
> 设 $P$ 是 $G$ 的一个西罗 $p$-子群, $H$ 是 $G$ 的一个 $p^{k}$ 阶子群, $k\le{l}$ (其中 $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$), 则存在 $g\in{G}$ 使 $H\subseteq{g}Pg^{-1}$. 特别地, $G$ 的西罗 $p$-子群相互共轭.

> **定理 1.10.10 (西罗第三定理)**
> 
> 设 $G$ 的西罗 $p$-子群的个数为 $n_{p}$, 则 (1) $G$ 的西罗 $p$-子群 $P\triangleleft{G}$ 当且仅当 $n_{p}=1$; (2) $n_{p}\mid{m}$ 且 $n_{p}\equiv1\pmod{p}$, 其中 $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$.

$$
\left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}.
$$

$$
\left(a-b\right)^{n}=\sum_{k=0}^{n}\binom{n}{k}a^{k}\left(-b\right)^{n-k},
$$
且 $R$ 交换保证各项可以合并.

> **定义 2.1.1 (环)**
> 
> 设 $R$ 是非空集合, 在 $R$ 上定义两种二元运算 $+$ 与 $\cdot$, 满足: (1) $\left[R;+\right]$ 是交换群; (2) $\left[R;\cdot\right]$ 是半群; (3) 乘法对加法满足左右分配律: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$. 则称 $R$ 为一个环.

> **定义 2.1.8 (无零因子环)**
> 
> 如果环 $R$ 不是零环且没有零因子, 则称 $R$ 为无零因子环.

> **命题 2.2.11 (理想判别法)**
> 
> 设 $R$ 为环, $I$ 为 $R$ 的非空子集, 则 $I$ 为 $R$ 的理想的充分必要条件是 $a-b\in{I}$ 且 $ax,ya\in{I}$ 对一切 $a,b\in{I}$, $x,y\in{R}$ 成立.

> **定理 2.2.16 (商环)**
> 
> 设 $R$ 是一个环, $I$ 是 $R$ 的理想, 则商加法群 $R/I$ 在乘法 $\left(a+I\right)\left(b+I\right)=ab+I$ 下构成一个环, 称为 $R$ 对 $I$ 的商环.

> **定义 2.2.20 (整环,除环与域)**
> 
> 无零因子的交换幺环称为整环; 若幺环 $R$ 满足 $R^{*}$ 对乘法构成群 (其中 $R^{*}=R\setminus\left\{0\right\}$), 则称 $R$ 为除环; 交换的除环称为域.

## 1.10-20

证明: $60$ 阶非阿贝尔有限单群必同构于 $A_5$.

### 解答 1.10-20

设 $G$ 是 $60$ 阶非阿贝尔单群. 先求西罗 $5$-子群的个数 $n_{5}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{5}\mid12$ 且 $n_{5}\equiv1\pmod5$, 故 $n_{5}=1$ 或 $6$. 由西罗子群与元素计数, $G$ 单故 $n_{5}\ne1$, 于是 $n_{5}=6$.

每个西罗 $5$-子群是 $5$ 阶循环群, 由西罗子群与元素计数, 含 $4$ 个 $5$ 阶元; 两个不同的西罗 $5$-子群交为 $\left\{e\right\}$ (交的阶同时整除 $5$, 故只能为 $1$). 因此 $G$ 中共有 $6\times4=24$ 个 $5$ 阶元.

再考虑西罗 $2$-子群的个数 $n_{2}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{2}\mid15$ 且 $n_{2}\equiv1\pmod2$, 故 $n_{2}\in\left\{1,3,5,15\right\}$. 由西罗子群与元素计数, $G$ 单故 $n_{2}\ne1$.

排除 $n_{2}=3$. 由群在陪集空间上的作用, $G$ 通过共轭作用在 $3$ 个西罗 $2$-子群上, 给出同态 $\pi:G\to{S}_3$. 其核 $\ker\pi$ 是 $G$ 的正规子群. 因 $G$ 单, $\ker\pi=\left\{e\right\}$ 或 $G$. 作用可递故非平凡, $\ker\pi\ne{G}$; 若 $\ker\pi=\left\{e\right\}$, 则 $G$ 同构于 $S_3$ 的子群, 而 $\left|S_3\right|=6<60$, 矛盾. 故 $n_{2}\ne3$.

处理 $n_{2}=5$. 由群在陪集空间上的作用, $G$ 共轭作用在 $5$ 个西罗 $2$-子群上, 给出同态 $\pi:G\to{S}_5$. 同理 $\ker\pi$ 为正规子群且非 $G$; 若 $\ker\pi=\left\{e\right\}$, 则 $G$ 同构于 $S_5$ 的一个 $60$ 阶子群. $S_5$ 的阶为 $120$, 该 $60$ 阶子群指数为 $2$, 由指数为 $2$ 的子群与 $S_n$ 的交错子群 必为正规子群且唯一, 即 $A_5$. 故 $G\cong{A}_5$, 结论成立.

排除 $n_{2}=15$. 若任意两个不同的西罗 $2$-子群交为 $\left\{e\right\}$, 则每个 $4$ 阶西罗 $2$-子群贡献 $3$ 个非单位元 (由$4$ 阶群是交换群 与西罗子群与元素计数), 共 $15\times3=45$ 个 $2$ 阶或 $4$ 阶元, 加上 $24$ 个 $5$ 阶元, 总数 $45+24=69>60$, 矛盾. 故存在两个不同的西罗 $2$-子群 $P,Q$ 使 $\left|P\cap{Q}\right|=2$.

设 $P\cap{Q}=\left\langle{x}\right\rangle$, 其中 $x$ 为 $2$ 阶元. 因 $P,Q$ 均为 $4$ 阶群, 由$4$ 阶群是交换群 皆交换, 且 $x\in{P}\cap{Q}$, 故 $P,Q\subseteq{N}_{G}\left(\left\langle{x}\right\rangle\right)$. 又 $P\ne{Q}$, 故 $\left|N_{G}\left(\left\langle{x}\right\rangle\right)\right|>4$. 同时 $\left|N_{G}\left(\left\langle{x}\right\rangle\right)\right|\mid60$ 且被 $4$ 整除 (因含 $4$ 阶子群 $P$), 故只能为 $12,20$ 或 $60$. 若为 $60$, 则 $\left\langle{x}\right\rangle\triangleleft{G}$, 与 $G$ 单矛盾. 故 $\left|N_{G}\left(\left\langle{x}\right\rangle\right)\right|=12$ 或 $20$, 对应指数 $5$ 或 $3$.

指数 $3$ 时, 由群在陪集空间上的作用, $G$ 左平移作用在 $3$ 个陪集上给出同态 $G\to{S}_3$, 与前述 $n_{2}=3$ 的矛盾相同, 故指数必为 $5$. 于是 $G$ 有指数 $5$ 的子群 $N_{G}\left(\left\langle{x}\right\rangle\right)$; 由群在陪集空间上的作用, $G$ 左平移作用在 $5$ 个陪集上给出同态 $G\to{S}_5$, 其核为正规子群且非 $G$, 因 $G$ 单故核为 $\left\{e\right\}$, 得单同态 $G\hookrightarrow{S}_5$. 如前所述, $S_5$ 的 $60$ 阶子群只能是 $A_5$, 故 $G\cong{A}_5$. $\blacksquare$

## 2.1-3

设集合 $R=\left\{a,b,c\right\}$, 在 $R$ 上定义加法和乘法. 若加法 $+$ 和乘法 $\cdot$ 的运算表分别为

$$
\begin{array}{c\left|ccc}
+&a&b&c\\\hline
a&a&b&c\\
b&b&c&a\\
c&c&a&b
\end{array}
\qquad
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

下面检验分配律. 取 $x=b$, $y=c$, $z=b$. 由加法表, $b+c=a$; 由乘法表, $a\cdot{b}=a$, $b\cdot{b}=a$, $c\cdot{b}=b$.

先算左边:

$$
\left(x+y\right)z=\left(b+c\right)b=a\cdot{b}=a.
$$

再算右边:

$$
xz+yz=b\cdot{b}+c\cdot{b}=a+b=b.
$$

因 $a\ne{b}$, 故

$$
\left(b+c\right)b\ne{b}\cdot{b}+c\cdot{b}.
$$

左分配律不成立.

此外, 乘法的结合律亦不成立: 取 $x=c$, $y=c$, $z=b$, 由乘法表 $c\cdot{c}=a$, $c\cdot{b}=b$, $a\cdot{b}=a$, 则

$$
\left(c\cdot{c}\right)\cdot{b}=a\cdot{b}=a,
$$

而

$$
c\cdot\left(c\cdot{b}\right)=c\cdot{b}=b.
$$

二者不等.

因此 $R$ 不满足**定义 2.1.1 (环)** 中的乘法结合律与分配律, $R$ 不构成环. $\blacksquare$

## 2.1-5

设 $R$ 为幺环, $e$ 为幺元, $a\in{R}$. 若存在 $m\in\mathbb{N}$ 使得 $a^{m}=0$, 则称 $a$ 为幂零元. 证明: 若 $a$ 为幂零元, 则 $e+a$ 为可逆元.

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

故 $b$ 是 $e+a$ 的逆元, 即 $e+a$ 为可逆元. 这与幂零元与有限几何级数 的结论一致. $\blacksquare$

## 2.1-15

(华罗庚) 设 $R$ 为幺环, $e$ 为幺元, $a\in{R}$. 若元素 $c$ 满足 $ca=e$ ($ac=e$), 则称 $c$ 为 $a$ 的一个左逆元 (右逆元). 若 $c$ 既是 $a$ 的左逆元, 又是 $a$ 的右逆元, 则称 $c$ 为 $a$ 的逆元, 这时称 $a$ 可逆. 证明: 对任何 $a,b\in{R}$, $e-ab$ 可逆当且仅当 $e-ba$ 可逆.

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

因此 $e-ab$ 可逆当且仅当 $e-ba$ 可逆. $\blacksquare$

## 2.1-16

(华罗庚) 设 $R$ 为幺环, $e$ 为幺元, $a,b\in{R}$. 证明: 若 $ab$, $ab-e$ 都可逆, 则 $a-b^{-1}$ 可逆, 且 $\left(a-b^{-1}\right)^{-1}-a^{-1}$ 也可逆, 且

$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

### 解答 2.1-16

因 $b^{-1}$ 可逆 (结论中出现 $b^{-1}$, 题设蕴含 $b$ 可逆), 且 $ab$ 可逆, 由幺环中可逆元的性质, $a=\left(ab\right)b^{-1}$ 是可逆元之积, 故 $a$ 可逆, $a^{-1}$ 存在.

又因 $b^{-1}$ 可逆, 由**定义 2.1.1 (环)** 的分配律,

$$
a-b^{-1}=\left(ab-e\right)b^{-1}.
$$

由题设 $ab-e$ 可逆, 又 $b^{-1}$ 可逆, 由幺环中可逆元的性质, 可逆元之积仍可逆, 故 $a-b^{-1}$ 可逆, 且

$$
\left(a-b^{-1}\right)^{-1}=b\left(ab-e\right)^{-1}.
$$

记 $X=ab-e$, 则 $X^{-1}$ 存在. 要证

$$
\left(a-b^{-1}\right)^{-1}-a^{-1}=bX^{-1}-a^{-1}
$$

可逆, 且其逆为 $aba-a=a\left(ba-e\right)$.

计算乘积 (利用**定义 2.1.1 (环)** 的分配律):

$$
\left(bX^{-1}-a^{-1}\right)\cdot{a}\left(ba-e\right)=bX^{-1}a\left(ba-e\right)-a^{-1}a\left(ba-e\right)=\left[bX^{-1}a-e\right]\left(ba-e\right).
$$

由 2.1-15 题 的华罗庚恒等式,

$$
\left(e-ba\right)^{-1}=e+b\left(e-ab\right)^{-1}a.
$$

注意到 $X=ab-e=-\left(e-ab\right)$, 故 $X^{-1}=-\left(e-ab\right)^{-1}$, 于是

$$
bX^{-1}a=-b\left(e-ab\right)^{-1}a=-\left[\left(e-ba\right)^{-1}-e\right]=e-\left(e-ba\right)^{-1}.
$$

因此

$$
bX^{-1}a-e=-\left(e-ba\right)^{-1}.
$$

又 $ba-e=-\left(e-ba\right)$, 故

$$
\left[bX^{-1}a-e\right]\left(ba-e\right)=\left(-\left(e-ba\right)^{-1}\right)\cdot\left(-\left(e-ba\right)\right)=\left(e-ba\right)^{-1}\left(e-ba\right)=e.
$$

同理可验证另一个方向 $\left(ba-e\right)\cdot\left(bX^{-1}-a^{-1}\right)=e$: 因 $\left(ba-e\right)=-\left(e-ba\right)$ 且 $bX^{-1}a-e=-\left(e-ba\right)^{-1}$, 类似交换位置后乘积仍为 $e$. 故 $a\left(ba-e\right)=aba-a$ 是

$$
bX^{-1}-a^{-1}=\left(a-b^{-1}\right)^{-1}-a^{-1}
$$

的逆元, 即

$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

$\blacksquare$

## 2.2-3

设 $R$ 为无零因子环, $I$ 为 $R$ 的理想, 问商环 $R/I$ 是否一定是无零因子环?

### 解答 2.2-3

不一定. 下面举反例.

取整数环 $R=\mathbb{Z}$. 由整数环 $\mathbb{Z}$ 是整环, $\mathbb{Z}$ 是整环, 因而满足**定义 2.1.8 (无零因子环)**. 取理想 $I=6\mathbb{Z}$. 由**定理 2.2.16 (商环)**, 商环为

$$
R/I=\mathbb{Z}/6\mathbb{Z}=\mathbb{Z}_6.
$$

在 $\mathbb{Z}_6$ 中,

$$
\left(2+6\mathbb{Z}\right)\left(3+6\mathbb{Z}\right)=6+6\mathbb{Z}=0+6\mathbb{Z},
$$

但 $2\notin6\mathbb{Z}$, $3\notin6\mathbb{Z}$, 故 $2+6\mathbb{Z}$ 与 $3+6\mathbb{Z}$ 都是非零的零因子. 由**定义 2.1.8 (无零因子环)**, $R/I$ 不是无零因子环.

因此 $R/I$ 未必是无零因子环. $\blacksquare$

## 2.2-6

设 $R$ 为无零因子环, 且只有有限个理想 (包括左理想,右理想和双边理想). 证明 $R$ 是除环.

### 解答 2.2-6

先证 $R$ 有幺元. 因 $R$ 是无零因子环, 由**定义 2.1.8 (无零因子环)**, $R$ 不是零环, 故存在 $0\ne{a}\in{R}$. 考虑左理想的降链

$$
R\supseteq{R}a\supseteq{R}a^{2}\supseteq\cdots.
$$

因 $R$ 只有有限个左理想, 该链必稳定, 即存在 $m$ 使 $Ra^{m}=Ra^{m+1}$. 于是 $a^{m}\in{R}a^{m+1}$, 存在 $b\in{R}$ 使 $a^{m}=ba^{m+1}$. 令 $e=ba$, 则 $ea^{m}=a^{m}$.

对任意 $x\in{R}$,

$$
\left(xe-x\right)a^{m}=x\left(ea^{m}\right)-xa^{m}=xa^{m}-xa^{m}=0.
$$

因 $a^{m}\ne0$ (由 $a\ne0$ 及**定义 2.1.8 (无零因子环)**, $a^{m}\ne0$), 由可逆元的消去, 得 $xe-x=0$, 即 $xe=x$ 对一切 $x\in{R}$ 成立. 故 $e$ 是 $R$ 的右单位元, 且 $e\ne0$ (否则由 $xe=x$ 得 $x=0$ 对一切 $x$, 与 $R$ 非零环矛盾).

又对任意 $x\in{R}$,

$$
e\left(ex-x\right)=e^{2}x-ex=ex-ex=0,
$$

其中用到右单位元给出 $e^{2}=e\cdot{e}=e$. 因 $e\ne0$ 且 $e\left(ex-x\right)=0$, 由可逆元的消去, 得 $ex-x=0$, 即 $ex=x$. 故 $e$ 同时是左单位元, 即 $e$ 是 $R$ 的幺元.

再证每个非零元可逆. 任取 $0\ne{x}\in{R}$. 同理, 左理想降链 $Rx\supseteq{R}x^{2}\supseteq\cdots$ 因只有有限个左理想而稳定, 存在 $n$ 使 $Rx^{n}=Rx^{n+1}$. 于是存在 $y\in{R}$ 使 $x^{n}=yx^{n+1}=\left(yx\right)x^{n}$, 即 $\left(e-yx\right)x^{n}=0$. 因 $x^{n}\ne0$, 由可逆元的消去, 得 $e-yx=0$, 即 $yx=e$. 故 $y$ 是 $x$ 的左逆元.

又

$$
\left(xy-e\right)x=xyx-ex=x\left(yx\right)-x=xe-x=0,
$$

由 $x\ne0$ 及可逆元的消去, 得 $xy=e$. 故 $x$ 也有右逆元 $y$, 即 $x$ 可逆.

于是 $R^{*}=R\setminus\left\{0\right\}$ 中每个元素可逆, 即 $R^{*}$ 关于乘法构成群. 由**定义 2.2.20 (整环,除环与域)**, $R$ 是除环. $\blacksquare$

## 2.2-11

设 $R$ 是交换环, $I$ 是 $R$ 的理想, 定义

$$
\sqrt{I}=\left\{a\in{R}\mid\exists\,n\in\mathbb{N},\;a^{n}\in{I}\right\}.
$$

试证明 $\sqrt{I}$ 也是 $R$ 的理想, 称为理想 $I$ 的根基. 特别地, $R$ 中所有幂零元组成的集合 (即理想 $\left\{0\right\}$ 的根基) 构成 $R$ 的理想, 称为 $R$ 的幂零根基, 记为 $\mathrm{Rad}\,R$. 证明对任何 $R$ 的理想 $I$, 有 $\sqrt{\sqrt{I}}=\sqrt{I}$.

### 解答 2.2-11

先证 $\sqrt{I}$ 是理想. 用**命题 2.2.11 (理想判别法)** 验证.

首先 $0\in\sqrt{I}$ (取 $n=1$, $0\in{I}$), 故 $\sqrt{I}$ 非空.

设 $a,b\in\sqrt{I}$, 则存在 $m,n\in\mathbb{N}$ 使 $a^{m}\in{I}$, $b^{n}\in{I}$. 因 $R$ 交换, 由交换环中的二项式定理,

$$
\left(a-b\right)^{m+n-1}=\sum_{k=0}^{m+n-1}\binom{m+n-1}{k}a^{k}\left(-b\right)^{m+n-1-k}.
$$

对右端任一项: 若 $k\ge{m}$, 则 $a^{k}=a^{m}a^{k-m}\in{I}$; 若 $k<{}m$, 则 $m+n-1-k\ge{n}$, 故 $\left(-b\right)^{m+n-1-k}=b^{m+n-1-k}\in{I}$ (因 $b^{n}\in{I}$). 因而每一项均属于 $I$, 即 $\left(a-b\right)^{m+n-1}\in{I}$, 故 $a-b\in\sqrt{I}$.

又设 $a\in\sqrt{I}$, $r\in{R}$ 且 $a^{n}\in{I}$, 则 $\left(ra\right)^{n}=r^{n}a^{n}\in{I}$ ($R$ 交换, $I$ 为理想, 由**命题 2.2.11 (理想判别法)**), 故 $ra\in\sqrt{I}$.

由**命题 2.2.11 (理想判别法)**, $\sqrt{I}$ 是 $R$ 的理想. 取 $I=\left\{0\right\}$, 则 $\sqrt{\left\{0\right\}}$ 恰为 $R$ 中所有幂零元 (即满足 $a^{n}=0$ 的元) 的集合, 它构成理想, 即幂零根基 $\mathrm{Rad}\,R$.

再证 $\sqrt{\sqrt{I}}=\sqrt{I}$.

先证 $\sqrt{I}\subseteq\sqrt{\sqrt{I}}$: 设 $a\in\sqrt{I}$, 则 $a^{n}\in{I}$ 对某 $n$ 成立. 因 $I\subseteq\sqrt{I}$ ($x\in{I}$ 时 $x^{1}\in{I}$, 故 $x\in\sqrt{I}$), 故 $a^{n}\in\sqrt{I}$, 即 $a\in\sqrt{\sqrt{I}}$.

再证 $\sqrt{\sqrt{I}}\subseteq\sqrt{I}$: 设 $a\in\sqrt{\sqrt{I}}$, 则存在 $n$ 使 $a^{n}\in\sqrt{I}$; 于是存在 $m$ 使 $\left(a^{n}\right)^{m}=a^{nm}\in{I}$, 故 $a\in\sqrt{I}$.

综上, $\sqrt{\sqrt{I}}=\sqrt{I}$. $\blacksquare$

## 2.2-13

设 $R$ 为交换环, 定义 $R$ 上的运算为 $a\circ{b}=a+b-ab$.

(1) 证明 $\circ$ 满足结合律, 而且 $0\circ{a}=a$, 对一切 $a\in{R}$;

(2) 证明 $R$ 为域当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群, 其中 $e$ 为 $R$ 的幺元.

### 解答 2.2-13

第 (1) 部分. 对任意 $a,b,c\in{R}$, 由**定义 2.1.1 (环)** 的分配律展开:

$$
\left(a\circ{b}\right)\circ{c}=\left(a+b-ab\right)\circ{c}=\left(a+b-ab\right)+c-\left(a+b-ab\right)c=a+b+c-ab-ac-bc+abc,
$$

且

$$
a\circ\left(b\circ{c}\right)=a\circ\left(b+c-bc\right)=a+\left(b+c-bc\right)-a\left(b+c-bc\right)=a+b+c-ab-ac-bc+abc.
$$

两者相等, 故 $\circ$ 满足结合律. 又

$$
0\circ{a}=0+a-0\cdot{a}=a.
$$

此外因 $R$ 交换, $a\circ{b}=a+b-ab=b+a-ba=b\circ{a}$, 故 $\circ$ 也满足交换律.

第 (2) 部分. 作映射 $\psi:R\to{R}$, $\psi\left(x\right)=e-x$. 显然 $\psi$ 是双射 (其逆为自身), 且 $\psi\left(0\right)=e$, $\psi\left(e\right)=0$. 对任意 $a,b\in{R}$,

$$
\psi\left(a\right)\circ\psi\left(b\right)=\left(e-a\right)\circ\left(e-b\right)=\left(e-a\right)+\left(e-b\right)-\left(e-a\right)\left(e-b\right)=e-ab=\psi\left(ab\right).
$$

故 $\psi$ 把 $R$ 的乘法同态地搬移到 $\circ$ 运算上, 且 $\psi$ 限制为 $R\setminus\left\{0\right\}$ 到 $R\setminus\left\{e\right\}$ 的双射 ($\psi\left(x\right)=e$ 当且仅当 $x=0$). 因而 $\left(R\setminus\left\{0\right\},\cdot\right)$ 为交换群当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群.

而由**定义 2.2.20 (整环,除环与域)**, 交换幺环 $R$ 为域当且仅当 $R\setminus\left\{0\right\}$ 关于乘法构成交换群. 因此 $R$ 为域当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群. $\blacksquare$
