# week12

> **基础知识: 交换环中的二项式定理**<br>设 $R$ 为交换环, $a,b\in R$, $n$ 为正整数, 则
$$
\left(a-b\right)^{n}=\sum_{k=0}^{n}\binom{n}{k}a^{k}\left(-b\right)^{n-k},
$$
且 $R$ 交换保证各项可以合并.

> **基础知识: 整数环 $\mathbb Z$ 是整环**<br>整数环 $\mathbb Z$ 是整环, 因而满足**定义 2.1.8 (无零因子环)**; 且对任意 $m\ge0$, $m\mathbb Z$ 是 $\mathbb Z$ 的理想, 商环 $\mathbb Z/m\mathbb Z$ 记作 $\mathbb Z_m$.

> **基础知识: 可逆元的消去**<br>在无零因子环 $R$ 中, 若 $ab=0$ 且 $a\ne0$, 则 $b=0$; 若 $ba=0$ 且 $a\ne0$, 则 $b=0$ (否则出现零因子).

> **定义 2.1.1 (环)**<br>设 $R$ 是非空集合, 在 $R$ 上定义两种二元运算 $+$ 与 $\cdot$, 满足: (1) $\left[R;+\right]$ 是交换群; (2) $\left[R;\cdot\right]$ 是半群; (3) 乘法对加法满足左右分配律: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$. 则称 $R$ 为一个环.

> **定义 2.1.8 (无零因子环)**<br>如果环 $R$ 不是零环且没有零因子, 则称 $R$ 为无零因子环.

> **命题 2.2.11 (理想判别法)**<br>设 $R$ 为环, $I$ 为 $R$ 的非空子集, 则 $I$ 为 $R$ 的理想的充分必要条件是 $a-b\in I$ 且 $ax,ya\in I$ 对一切 $a,b\in I$, $x,y\in R$ 成立.

> **定理 2.2.16 (商环)**<br>设 $R$ 是一个环, $I$ 是 $R$ 的理想, 则商加法群 $R/I$ 在乘法 $\left(a+I\right)\left(b+I\right)=ab+I$ 下构成一个环, 称为 $R$ 对 $I$ 的商环.

> **定义 2.2.20 (整环,除环与域)**<br>无零因子的交换幺环称为整环; 若幺环 $R$ 满足 $R^{*}$ 对乘法构成群 (其中 $R^{*}=R\setminus\left\{0\right\}$), 则称 $R$ 为除环; 交换的除环称为域.

---

## 2.2-3

设 $R$ 为无零因子环, $I$ 为 $R$ 的理想, 问商环 $R/I$ 是否一定是无零因子环?

### 解答 2.2-3

不一定. 下面举反例.

取整数环 $R=\mathbb Z$. 由**基础知识: 整数环 $\mathbb Z$ 是整环**, $\mathbb Z$ 是整环, 因而满足**定义 2.1.8 (无零因子环)**. 取理想 $I=6\mathbb Z$. 由**定理 2.2.16 (商环)**, 商环为

$$
R/I=\mathbb Z/6\mathbb Z=\mathbb Z_6.
$$

在 $\mathbb Z_6$ 中,

$$
\left(2+6\mathbb Z\right)\left(3+6\mathbb Z\right)=6+6\mathbb Z=0+6\mathbb Z,
$$

但 $2\notin6\mathbb Z$, $3\notin6\mathbb Z$, 故 $2+6\mathbb Z$ 与 $3+6\mathbb Z$ 都是非零的零因子. 由**定义 2.1.8 (无零因子环)**, $R/I$ 不是无零因子环.

因此 $R/I$ 未必是无零因子环. $\blacksquare$

---

## 2.2-6

设 $R$ 为无零因子环, 且只有有限个理想 (包括左理想,右理想和双边理想). 证明 $R$ 是除环.

### 解答 2.2-6

**先证 $R$ 有幺元.** 因 $R$ 是无零因子环, 由**定义 2.1.8 (无零因子环)**, $R$ 不是零环, 故存在 $0\ne a\in R$. 考虑左理想的降链

$$
R\supseteq Ra\supseteq Ra^{2}\supseteq\cdots.
$$

因 $R$ 只有有限个左理想, 该链必稳定, 即存在 $m$ 使 $Ra^{m}=Ra^{m+1}$. 于是 $a^{m}\in Ra^{m+1}$, 存在 $b\in R$ 使 $a^{m}=ba^{m+1}$. 令 $e=ba$, 则 $ea^{m}=a^{m}$.

对任意 $x\in R$,

$$
\left(xe-x\right)a^{m}=x\left(ea^{m}\right)-xa^{m}=xa^{m}-xa^{m}=0.
$$

因 $a^{m}\ne0$ (由 $a\ne0$ 及**定义 2.1.8 (无零因子环)**, $a^{m}\ne0$), 由**基础知识: 可逆元的消去**, 得 $xe-x=0$, 即 $xe=x$ 对一切 $x\in R$ 成立. 故 $e$ 是 $R$ 的右单位元, 且 $e\ne0$ (否则由 $xe=x$ 得 $x=0$ 对一切 $x$, 与 $R$ 非零环矛盾).

又对任意 $x\in R$,

$$
e\left(ex-x\right)=e^{2}x-ex=ex-ex=0,
$$

其中用到右单位元给出 $e^{2}=e\cdot e=e$. 因 $e\ne0$ 且 $e\left(ex-x\right)=0$, 由**基础知识: 可逆元的消去**, 得 $ex-x=0$, 即 $ex=x$. 故 $e$ 同时是左单位元, 即 $e$ 是 $R$ 的幺元.

**再证每个非零元可逆.** 任取 $0\ne x\in R$. 同理, 左理想降链 $Rx\supseteq Rx^{2}\supseteq\cdots$ 因只有有限个左理想而稳定, 存在 $n$ 使 $Rx^{n}=Rx^{n+1}$. 于是存在 $y\in R$ 使 $x^{n}=yx^{n+1}=\left(yx\right)x^{n}$, 即 $\left(e-yx\right)x^{n}=0$. 因 $x^{n}\ne0$, 由**基础知识: 可逆元的消去**, 得 $e-yx=0$, 即 $yx=e$. 故 $y$ 是 $x$ 的左逆元.

又

$$
\left(xy-e\right)x=xyx-ex=x\left(yx\right)-x=xe-x=0,
$$

由 $x\ne0$ 及**基础知识: 可逆元的消去**, 得 $xy=e$. 故 $x$ 也有右逆元 $y$, 即 $x$ 可逆.

于是 $R^{*}=R\setminus\left\{0\right\}$ 中每个元素可逆, 即 $R^{*}$ 关于乘法构成群. 由**定义 2.2.20 (整环,除环与域)**, $R$ 是除环. $\blacksquare$

---

## 2.2-11

设 $R$ 是交换环, $I$ 是 $R$ 的理想, 定义

$$
\sqrt{I}=\left\{a\in R\mid\exists\,n\in\mathbb N,\;a^{n}\in I\right\}.
$$

试证明 $\sqrt{I}$ 也是 $R$ 的理想, 称为理想 $I$ 的根基. 特别地, $R$ 中所有幂零元组成的集合 (即理想 $\left\{0\right\}$ 的根基) 构成 $R$ 的理想, 称为 $R$ 的幂零根基, 记为 $\mathrm{Rad}\,R$. 证明对任何 $R$ 的理想 $I$, 有 $\sqrt{\sqrt{I}}=\sqrt{I}$.

### 解答 2.2-11

**先证 $\sqrt{I}$ 是理想.** 用**命题 2.2.11 (理想判别法)** 验证.

首先 $0\in\sqrt{I}$ (取 $n=1$, $0\in I$), 故 $\sqrt{I}$ 非空.

设 $a,b\in\sqrt{I}$, 则存在 $m,n\in\mathbb N$ 使 $a^{m}\in I$, $b^{n}\in I$. 因 $R$ 交换, 由**基础知识: 交换环中的二项式定理**,

$$
\left(a-b\right)^{m+n-1}=\sum_{k=0}^{m+n-1}\binom{m+n-1}{k}a^{k}\left(-b\right)^{m+n-1-k}.
$$

对右端任一项: 若 $k\ge m$, 则 $a^{k}=a^{m}a^{k-m}\in I$; 若 $k<m$, 则 $m+n-1-k\ge n$, 故 $\left(-b\right)^{m+n-1-k}=b^{m+n-1-k}\in I$ (因 $b^{n}\in I$). 因而每一项均属于 $I$, 即 $\left(a-b\right)^{m+n-1}\in I$, 故 $a-b\in\sqrt{I}$.

又设 $a\in\sqrt{I}$, $r\in R$ 且 $a^{n}\in I$, 则 $\left(ra\right)^{n}=r^{n}a^{n}\in I$ ($R$ 交换, $I$ 为理想, 由**命题 2.2.11 (理想判别法)**), 故 $ra\in\sqrt{I}$.

由**命题 2.2.11 (理想判别法)**, $\sqrt{I}$ 是 $R$ 的理想. 取 $I=\left\{0\right\}$, 则 $\sqrt{\left\{0\right\}}$ 恰为 $R$ 中所有幂零元 (即满足 $a^{n}=0$ 的元) 的集合, 它构成理想, 即幂零根基 $\mathrm{Rad}\,R$.

**再证 $\sqrt{\sqrt{I}}=\sqrt{I}$.**

先证 $\sqrt{I}\subseteq\sqrt{\sqrt{I}}$: 设 $a\in\sqrt{I}$, 则 $a^{n}\in I$ 对某 $n$ 成立. 因 $I\subseteq\sqrt{I}$ ($x\in I$ 时 $x^{1}\in I$, 故 $x\in\sqrt{I}$), 故 $a^{n}\in\sqrt{I}$, 即 $a\in\sqrt{\sqrt{I}}$.

再证 $\sqrt{\sqrt{I}}\subseteq\sqrt{I}$: 设 $a\in\sqrt{\sqrt{I}}$, 则存在 $n$ 使 $a^{n}\in\sqrt{I}$; 于是存在 $m$ 使 $\left(a^{n}\right)^{m}=a^{nm}\in I$, 故 $a\in\sqrt{I}$.

综上, $\sqrt{\sqrt{I}}=\sqrt{I}$. $\blacksquare$

---

## 2.2-13

设 $R$ 为交换环, 定义 $R$ 上的运算为 $a\circ b=a+b-ab$.

(1) 证明 $\circ$ 满足结合律, 而且 $0\circ a=a$, 对一切 $a\in R$;

(2) 证明 $R$ 为域当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群, 其中 $e$ 为 $R$ 的幺元.

### 解答 2.2-13

**第 (1) 部分.** 对任意 $a,b,c\in R$, 由**定义 2.1.1 (环)** 的分配律展开:

$$
\left(a\circ b\right)\circ c=\left(a+b-ab\right)\circ c=\left(a+b-ab\right)+c-\left(a+b-ab\right)c=a+b+c-ab-ac-bc+abc,
$$

且

$$
a\circ\left(b\circ c\right)=a\circ\left(b+c-bc\right)=a+\left(b+c-bc\right)-a\left(b+c-bc\right)=a+b+c-ab-ac-bc+abc.
$$

两者相等, 故 $\circ$ 满足结合律. 又

$$
0\circ a=0+a-0\cdot a=a.
$$

此外因 $R$ 交换, $a\circ b=a+b-ab=b+a-ba=b\circ a$, 故 $\circ$ 也满足交换律.

**第 (2) 部分.** 作映射 $\psi:R\to R$, $\psi\left(x\right)=e-x$. 显然 $\psi$ 是双射 (其逆为自身), 且 $\psi\left(0\right)=e$, $\psi\left(e\right)=0$. 对任意 $a,b\in R$,

$$
\psi\left(a\right)\circ\psi\left(b\right)=\left(e-a\right)\circ\left(e-b\right)=\left(e-a\right)+\left(e-b\right)-\left(e-a\right)\left(e-b\right)=e-ab=\psi\left(ab\right).
$$

故 $\psi$ 把 $R$ 的乘法同态地搬移到 $\circ$ 运算上, 且 $\psi$ 限制为 $R\setminus\left\{0\right\}$ 到 $R\setminus\left\{e\right\}$ 的双射 ($\psi\left(x\right)=e$ 当且仅当 $x=0$). 因而 $\left(R\setminus\left\{0\right\},\cdot\right)$ 为交换群当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群.

而由**定义 2.2.20 (整环,除环与域)**, 交换幺环 $R$ 为域当且仅当 $R\setminus\left\{0\right\}$ 关于乘法构成交换群. 因此 $R$ 为域当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群. $\blacksquare$
