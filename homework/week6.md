# week6

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

## 2.1-16

(华罗庚) 设 $R$ 为幺环, $e$ 为幺元, $a,b\in{}R$. 证明: 若 $ab$, $ab-e$ 都可逆, 则 $a-b^{-1}$ 可逆, 且 $\left(a-b^{-1}\right)^{-1}-a^{-1}$ 也可逆, 且

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
\left(bX^{-1}-a^{-1}\right)\cdot{}a\left(ba-e\right)=bX^{-1}a\left(ba-e\right)-a^{-1}a\left(ba-e\right)=\left[bX^{-1}a-e\right]\left(ba-e\right).
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

因此 $R/I$ 未必是无零因子环.

$\blacksquare$

## 2.2-6

设 $R$ 为无零因子环, 且只有有限个理想 (包括左理想,右理想和双边理想). 证明 $R$ 是除环.

### 解答 2.2-6

先证 $R$ 有幺元. 因 $R$ 是无零因子环, 由**定义 2.1.8 (无零因子环)**, $R$ 不是零环, 故存在 $0\ne{}a\in{}R$. 考虑左理想的降链

$$
R\supseteq{}Ra\supseteq{}Ra^{2}\supseteq\cdots.
$$

因 $R$ 只有有限个左理想, 该链必稳定, 即存在 $m$ 使 $Ra^{m}=Ra^{m+1}$. 于是 $a^{m}\in{}Ra^{m+1}$, 存在 $b\in{}R$ 使 $a^{m}=ba^{m+1}$. 令 $e=ba$, 则 $ea^{m}=a^{m}$.

对任意 $x\in{}R$,

$$
\left(xe-x\right)a^{m}=x\left(ea^{m}\right)-xa^{m}=xa^{m}-xa^{m}=0.
$$

因 $a^{m}\ne0$ (由 $a\ne0$ 及**定义 2.1.8 (无零因子环)**, $a^{m}\ne0$), 由可逆元的消去, 得 $xe-x=0$, 即 $xe=x$ 对一切 $x\in{}R$ 成立. 故 $e$ 是 $R$ 的右单位元, 且 $e\ne0$ (否则由 $xe=x$ 得 $x=0$ 对一切 $x$, 与 $R$ 非零环矛盾).

又对任意 $x\in{}R$,

$$
e\left(ex-x\right)=e^{2}x-ex=ex-ex=0,
$$

其中用到右单位元给出 $e^{2}=e\cdot{}e=e$. 因 $e\ne0$ 且 $e\left(ex-x\right)=0$, 由可逆元的消去, 得 $ex-x=0$, 即 $ex=x$. 故 $e$ 同时是左单位元, 即 $e$ 是 $R$ 的幺元.

再证每个非零元可逆. 任取 $0\ne{}x\in{}R$. 同理, 左理想降链 $Rx\supseteq{}Rx^{2}\supseteq\cdots$ 因只有有限个左理想而稳定, 存在 $n$ 使 $Rx^{n}=Rx^{n+1}$. 于是存在 $y\in{}R$ 使 $x^{n}=yx^{n+1}=\left(yx\right)x^{n}$, 即 $\left(e-yx\right)x^{n}=0$. 因 $x^{n}\ne0$, 由可逆元的消去, 得 $e-yx=0$, 即 $yx=e$. 故 $y$ 是 $x$ 的左逆元.

又

$$
\left(xy-e\right)x=xyx-ex=x\left(yx\right)-x=xe-x=0,
$$

由 $x\ne0$ 及可逆元的消去, 得 $xy=e$. 故 $x$ 也有右逆元 $y$, 即 $x$ 可逆.

于是 $R^{*}=R\setminus\left\{0\right\}$ 中每个元素可逆, 即 $R^{*}$ 关于乘法构成群. 由**定义 2.2.20 (整环,除环与域)**, $R$ 是除环.

$\blacksquare$

## 2.2-11

设 $R$ 是交换环, $I$ 是 $R$ 的理想, 定义

$$
\sqrt{I}=\left\{a\in{}R\mid\exists\,n\in\mathbb{N},\;a^{n}\in{}I\right\}.
$$

试证明 $\sqrt{I}$ 也是 $R$ 的理想, 称为理想 $I$ 的根基. 特别地, $R$ 中所有幂零元组成的集合 (即理想 $\left\{0\right\}$ 的根基) 构成 $R$ 的理想, 称为 $R$ 的幂零根基, 记为 $\mathrm{Rad}\,R$. 证明对任何 $R$ 的理想 $I$, 有 $\sqrt{\sqrt{I}}=\sqrt{I}$.

### 解答 2.2-11

先证 $\sqrt{I}$ 是理想. 用**命题 2.2.11 (理想判别法)** 验证.

首先 $0\in\sqrt{I}$ (取 $n=1$, $0\in{}I$), 故 $\sqrt{I}$ 非空.

设 $a,b\in\sqrt{I}$, 则存在 $m,n\in\mathbb{N}$ 使 $a^{m}\in{}I$, $b^{n}\in{}I$. 因 $R$ 交换, 由交换环中的二项式定理,

$$
\left(a-b\right)^{m+n-1}=\sum_{k=0}^{m+n-1}\binom{m+n-1}{k}a^{k}\left(-b\right)^{m+n-1-k}.
$$

对右端任一项: 若 $k\ge{}m$, 则 $a^{k}=a^{m}a^{k-m}\in{}I$; 若 $k<{}m$, 则 $m+n-1-k\ge{}n$, 故 $\left(-b\right)^{m+n-1-k}=b^{m+n-1-k}\in{}I$ (因 $b^{n}\in{}I$). 因而每一项均属于 $I$, 即 $\left(a-b\right)^{m+n-1}\in{}I$, 故 $a-b\in\sqrt{I}$.

又设 $a\in\sqrt{I}$, $r\in{}R$ 且 $a^{n}\in{}I$, 则 $\left(ra\right)^{n}=r^{n}a^{n}\in{}I$ ($R$ 交换, $I$ 为理想, 由**命题 2.2.11 (理想判别法)**), 故 $ra\in\sqrt{I}$.

由**命题 2.2.11 (理想判别法)**, $\sqrt{I}$ 是 $R$ 的理想. 取 $I=\left\{0\right\}$, 则 $\sqrt{\left\{0\right\}}$ 恰为 $R$ 中所有幂零元 (即满足 $a^{n}=0$ 的元) 的集合, 它构成理想, 即幂零根基 $\mathrm{Rad}\,R$.

再证 $\sqrt{\sqrt{I}}=\sqrt{I}$.

先证 $\sqrt{I}\subseteq\sqrt{\sqrt{I}}$: 设 $a\in\sqrt{I}$, 则 $a^{n}\in{}I$ 对某 $n$ 成立. 因 $I\subseteq\sqrt{I}$ ($x\in{}I$ 时 $x^{1}\in{}I$, 故 $x\in\sqrt{I}$), 故 $a^{n}\in\sqrt{I}$, 即 $a\in\sqrt{\sqrt{I}}$.

再证 $\sqrt{\sqrt{I}}\subseteq\sqrt{I}$: 设 $a\in\sqrt{\sqrt{I}}$, 则存在 $n$ 使 $a^{n}\in\sqrt{I}$; 于是存在 $m$ 使 $\left(a^{n}\right)^{m}=a^{nm}\in{}I$, 故 $a\in\sqrt{I}$.

综上, $\sqrt{\sqrt{I}}=\sqrt{I}$.

$\blacksquare$

## 2.2-13

设 $R$ 为交换环, 定义 $R$ 上的运算为 $a\circ{}b=a+b-ab$.

(1) 证明 $\circ$ 满足结合律, 而且 $0\circ{}a=a$, 对一切 $a\in{}R$;

(2) 证明 $R$ 为域当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群, 其中 $e$ 为 $R$ 的幺元.

### 解答 2.2-13

第 (1) 部分. 对任意 $a,b,c\in{}R$, 由**定义 2.1.1 (环)** 的分配律展开:

$$
\left(a\circ{}b\right)\circ{}c=\left(a+b-ab\right)\circ{}c=\left(a+b-ab\right)+c-\left(a+b-ab\right)c=a+b+c-ab-ac-bc+abc,
$$

且

$$
a\circ\left(b\circ{}c\right)=a\circ\left(b+c-bc\right)=a+\left(b+c-bc\right)-a\left(b+c-bc\right)=a+b+c-ab-ac-bc+abc.
$$

两者相等, 故 $\circ$ 满足结合律. 又

$$
0\circ{}a=0+a-0\cdot{}a=a.
$$

此外因 $R$ 交换, $a\circ{}b=a+b-ab=b+a-ba=b\circ{}a$, 故 $\circ$ 也满足交换律.

第 (2) 部分. 作映射 $\psi:R\to{}R$, $\psi\left(x\right)=e-x$. 显然 $\psi$ 是双射 (其逆为自身), 且 $\psi\left(0\right)=e$, $\psi\left(e\right)=0$. 对任意 $a,b\in{}R$,

$$
\psi\left(a\right)\circ\psi\left(b\right)=\left(e-a\right)\circ\left(e-b\right)=\left(e-a\right)+\left(e-b\right)-\left(e-a\right)\left(e-b\right)=e-ab=\psi\left(ab\right).
$$

故 $\psi$ 把 $R$ 的乘法同态地搬移到 $\circ$ 运算上, 且 $\psi$ 限制为 $R\setminus\left\{0\right\}$ 到 $R\setminus\left\{e\right\}$ 的双射 ($\psi\left(x\right)=e$ 当且仅当 $x=0$). 因而 $\left(R\setminus\left\{0\right\},\cdot\right)$ 为交换群当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群.

而由**定义 2.2.20 (整环,除环与域)**, 交换幺环 $R$ 为域当且仅当 $R\setminus\left\{0\right\}$ 关于乘法构成交换群. 因此 $R$ 为域当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群.

$\blacksquare$

## 2.3-4

在四元数体 $H$ 中定义一个元素 $\alpha\in{}H$ 的范数为 $N\left(\alpha\right)=\alpha\overline\alpha$. 试证明:

(1) 对任何 $\alpha\in{}H$, $N\left(\alpha\right)\ge0$, 且 $N\left(\alpha\right)=0$ 当且仅当 $\alpha=0$;

(2) 对任何 $\alpha,\beta\in{}H$ 有

$$
\sqrt{N\left(\alpha+\beta\right)}\le\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)},
$$

且等号成立当且仅当 $\alpha,\beta$ 实线性相关;

(3) $N\left(\lambda\alpha\right)=\lambda^{2}N\left(\alpha\right)$, $\lambda\in\mathbb{R}$;

(4) $N\left(\overline\alpha\right)=N\left(\alpha\right)$;

(5) $N\left(\alpha\beta\right)=N\left(\alpha\right)N\left(\beta\right)$.

### 解答 2.3-4

设 $\alpha=a+bi+cj+dk$. 由四元数与共轭, 范数为

$$
N\left(\alpha\right)=\alpha\overline\alpha=a^{2}+b^{2}+c^{2}+d^{2}.
$$

第 (1) 部分. 因 $a,b,c,d\in\mathbb{R}$, 各项平方均非负, 故

$$
N\left(\alpha\right)=a^{2}+b^{2}+c^{2}+d^{2}\ge0.
$$

$N\left(\alpha\right)=0$ 当且仅当 $a^{2}+b^{2}+c^{2}+d^{2}=0$, 当且仅当 $a=b=c=d=0$, 即 $\alpha=0$. 故 (1) 得证.

第 (2) 部分. 把 $\alpha,\beta$ 看成 $\mathbb{R}^{4}$ 中的向量, 由欧氏范数的三角不等式, $N\left(\alpha\right)=\left\|\alpha\right\|^{2}$, 于是

$$
\sqrt{N\left(\alpha+\beta\right)}=\left\|\alpha+\beta\right\|\le\left\|\alpha\right\|+\left\|\beta\right\|=\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)}.
$$

且等号成立当且仅当 $\alpha,\beta$ 实线性相关 (由欧氏范数的三角不等式). 故 (2) 得证.

第 (3) 部分. 对 $\lambda\in\mathbb{R}$, $\lambda\alpha=\lambda{}a+\lambda{}b\,i+\lambda{}c\,j+\lambda{}d\,k$, 由四元数与共轭,

$$
N\left(\lambda\alpha\right)=\left(\lambda{}a\right)^{2}+\left(\lambda{}b\right)^{2}+\left(\lambda{}c\right)^{2}+\left(\lambda{}d\right)^{2}=\lambda^{2}\left(a^{2}+b^{2}+c^{2}+d^{2}\right)=\lambda^{2}N\left(\alpha\right).
$$

故 (3) 得证.

第 (4) 部分. 由四元数与共轭, $\overline\alpha=a-bi-cj-dk$, 故

$$
N\left(\overline\alpha\right)=a^{2}+\left(-b\right)^{2}+\left(-c\right)^{2}+\left(-d\right)^{2}=a^{2}+b^{2}+c^{2}+d^{2}=N\left(\alpha\right).
$$

故 (4) 得证.

第 (5) 部分. 由共轭的反序性质 $\overline{\alpha\beta}=\overline\beta\,\overline\alpha$ (见四元数与共轭), 以及 $N\left(\beta\right)=\beta\overline\beta$ 为实数而可与任意四元数交换, 得

$$
N\left(\alpha\beta\right)=\left(\alpha\beta\right)\overline{\left(\alpha\beta\right)}=\alpha\beta\overline\beta\,\overline\alpha=\alpha\left(\beta\overline\beta\right)\overline\alpha=N\left(\beta\right)\alpha\overline\alpha=N\left(\alpha\right)N\left(\beta\right).
$$

故 (5) 得证.

$\blacksquare$

## 2.4-6

试求出数域

$$
\mathbb{Q}\left[\sqrt{-1}\right]=\left\{a+b\sqrt{-1}\mid{}a,b\in\mathbb{Q}\right\}
$$

的所有自同构.

### 解答 2.4-6

记 $i=\sqrt{-1}$. 设 $\varphi:\mathbb{Q}\left[i\right]\to\mathbb{Q}\left[i\right]$ 为环的自同构. 由**定义 2.4.1 (环同态与同构)**, $\varphi$ 保持乘法与加法; 又 $\varphi\left(1\right)=1$, 由环自同构固定素域, $\varphi$ 在 $\mathbb{Q}$ 上为恒等映射.

令 $\varphi\left(i\right)=u=a+bi$, $a,b\in\mathbb{Q}$. 因 $i^{2}=-1$, 且 $\varphi$ 保持乘法与加法,

$$
u^{2}=\varphi\left(i\right)^{2}=\varphi\left(i^{2}\right)=\varphi\left(-1\right)=-1.
$$

即

$$
\left(a+bi\right)^{2}=a^{2}-b^{2}+2abi=-1.
$$

比较实部与虚部得 $2ab=0$ 且 $a^{2}-b^{2}=-1$. 若 $b=0$, 则 $a^{2}=-1$, 在 $\mathbb{Q}$ 中无解; 故 $a=0$, $b^{2}=1$, $b=\pm1$. 于是 $u=i$ 或 $u=-i$.

情况一 $\varphi\left(i\right)=i$: 此时对 $a,b\in\mathbb{Q}$, $\varphi\left(a+bi\right)=a+bi$, 即恒等自同构.

情况二 $\varphi\left(i\right)=-i$: 此时 $\varphi\left(a+bi\right)=a-bi$, 即复共轭映射.

这两种映射均保持加法与乘法 (复共轭保持 $\mathbb{Q}$ 上的运算) 且为双射, 由**定义 2.4.1 (环同态与同构)** 均为自同构. 故 $\mathbb{Q}\left[i\right]$ 恰有两个自同构: 恒等映射与共轭映射.

$\blacksquare$
