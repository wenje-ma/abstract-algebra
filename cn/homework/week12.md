# 作业 12

> **定义 2.1.8**（无零因子环）如果环 $R$ 不是零环且没有零因子, 则称 $R$ 为无零因子环.

> **命题 2.2.11**（理想判别法）设 $R$ 为环, $I$ 为 $R$ 的非空子集, 则 $I$ 为 $R$ 的理想的充分必要条件是对任意 $a,b\in I$ 有 $a-b\in I$, 且对任意 $a\in I$, $\alpha,\gamma\in R$ 有 $\alpha a,a\gamma\in I$.

> **定理 2.2.16**（商环）设 $R$ 是一个环, $I$ 是 $R$ 的理想, 则商加法群 $R/I$ 在乘法 $\left(a+I\right)\left(b+I\right)=ab+I$ 下构成一个环, 称为 $R$ 对 $I$ 的商环.

> **定义 2.2.20**（整环、除环与域）无零因子的交换幺环称为整环; 若幺环 $R$ 满足 $R^*$ 对乘法构成群($R^*=R\setminus\left\{0\right\}$), 则称 $R$ 为除环; 交换的除环称为域.

### 习题一

（习题 2.2-3）设 $R$ 为无零因子环, $I$ 为 $R$ 的理想, 问商环 $R/I$ 是否一定是无零因子环?

### 解答 习题一

不一定. 下面举反例.

取整数环 $R=\mathbb Z$, 它是整环, 因而满足**定义 2.1.8**（无零因子环）. 取理想 $I=6\mathbb Z$. 由**定理 2.2.16**（商环）, 商环为

$$
R/I=\mathbb Z/6\mathbb Z.
$$

在 $\mathbb Z/6\mathbb Z$ 中,

$$
\begin{aligned}\left(2+6\mathbb Z\right)\left(3+6\mathbb Z\right)&=6+6\mathbb Z\\&=0+6\mathbb Z,\end{aligned}
$$

但 $2\notin 6\mathbb Z$, $3\notin 6\mathbb Z$. 故 $2+6\mathbb Z$ 与 $3+6\mathbb Z$ 都是非零的零因子.

因此 $R/I$ 未必是无零因子环. $\blacksquare$

### 习题二

（习题 2.2-6）设 $R$ 为无零因子环, 且只有有限个理想(包括左理想, 右理想和双边理想). 证明 $R$ 是除环.

### 解答 习题二

先证 $R$ 有幺元. 任取 $0\ne a\in R$, 考虑左理想的降链

$$
R\supseteq Ra\supseteq Ra^2\supseteq\cdots.
$$

因 $R$ 只有有限个左理想, 该链必稳定, 即存在 $m$ 使 $Ra^m=Ra^{m+1}$. 于是 $a^m\in Ra^{m+1}$, 存在 $b\in R$ 使 $a^m=ba^{m+1}$. 令 $e=ba$, 则 $ea^m=a^m$.

对任意 $x\in R$,

$$
\begin{aligned}\left(xe-x\right)a^m&=x\left(ea^m\right)-xa^m\\&=xa^m-xa^m\\&=0.\end{aligned}
$$

因 $a^m\ne0$ 且 $R$ 无右零因子, 得 $xe-x=0$, 即 $xe=x$ 对一切 $x\in R$ 成立, 故 $e$ 是 $R$ 的右单位元, 且 $e\ne0$.

又对任意 $x\in R$,

$$
\begin{aligned}e\left(ex-x\right)&=e^2x-ex\\&=ex-ex\\&=0,\end{aligned}
$$

其中用到右单位元给出 $e^2=e$. 因 $e\ne0$ 且 $R$ 无左零因子, 得 $ex-x=0$, 即 $ex=x$. 故 $e$ 是 $R$ 的幺元.

再证每个非零元可逆. 任取 $0\ne x\in R$, 同理左理想降链 $Rx\supseteq Rx^2\supseteq\cdots$ 稳定, 存在 $n$ 使 $Rx^n=Rx^{n+1}$. 于是存在 $y\in R$ 使 $x^n=yx^{n+1}=\left(yx\right)x^n$, 即 $\left(e-yx\right)x^n=0$. 由 $x^n\ne0$ 消去得 $yx=e$, 即 $y$ 是 $x$ 的左逆. 又

$$
\begin{aligned}\left(xy-e\right)x&=xyx-ex\\&=x\left(yx\right)-x\\&=xe-x\\&=0,\end{aligned}
$$

由 $x\ne0$ 得 $xy=e$. 故 $x$ 有双侧逆元.

于是 $R^*=R\setminus\left\{0\right\}$ 关于乘法构成群. 由**定义 2.2.20**（整环、除环与域）, $R$ 是除环. $\blacksquare$

### 习题三

（习题 2.2-11）设 $R$ 是交换环, $I$ 是 $R$ 的理想, 定义

$$
\sqrt{I}=\left\{a\in R\mid\exists\,n\in\mathbb N,\;a^n\in I\right\}.
$$

试证明 $\sqrt{I}$ 也是 $R$ 的理想, 称为理想 $I$ 的根基. 特别地, $R$ 中所有幂零元组成的集合(即理想 $\left\{0\right\}$ 的根基)构成 $R$ 的理想, 称为 $R$ 的幂零根基, 记为 $\operatorname{Rad}R$. 证明对任何 $R$ 的理想 $I$, 有 $\sqrt{\sqrt{I}}=\sqrt{I}$.

### 解答 习题三

**先证 $\sqrt{I}$ 是理想**. 由**命题 2.2.11**（理想判别法）验证.

首先 $0\in\sqrt{I}$, 故 $\sqrt{I}$ 非空.

设 $a,b\in\sqrt{I}$, 则存在 $m,n\in\mathbb N$ 使 $a^m\in I$, $b^n\in I$. 因 $R$ 交换, 由二项式定理,

$$
\left(a-b\right)^{m+n-1}=\sum_{k=0}^{m+n-1}\binom{m+n-1}{k}a^k\left(-b\right)^{m+n-1-k}.
$$

对右端任一项, 若 $k\ge m$, 则 $a^k=a^m a^{k-m}\in I$; 若 $k<m$, 则 $m+n-1-k\ge n$, 故 $b^{m+n-1-k}=b^n b^{m-1-k}\in I$. 因而每一项均属于 $I$, 即 $\left(a-b\right)^{m+n-1}\in I$, 故 $a-b\in\sqrt{I}$.

又设 $a\in\sqrt{I}$, $r\in R$ 且 $a^n\in I$, 则 $\left(ra\right)^n=r^n a^n\in I$($R$ 交换, $I$ 为理想), 故 $ra\in\sqrt{I}$.

由**命题 2.2.11**（理想判别法）, $\sqrt{I}$ 是 $R$ 的理想. 取 $I=\left\{0\right\}$, 则 $\sqrt{\left\{0\right\}}$ 恰为 $R$ 中所有幂零元(即满足 $a^n=0$ 的元)的集合, 它构成理想, 即幂零根基 $\operatorname{Rad}R$.

**再证 $\sqrt{\sqrt{I}}=\sqrt{I}$**.

先证 $\sqrt{I}\subseteq\sqrt{\sqrt{I}}$. 设 $a\in\sqrt{I}$, 则 $a^n\in I$. 因 $I\subseteq\sqrt{I}$($x\in I$ 时 $x^1\in I$, 故 $x\in\sqrt{I}$), 故 $a^n\in\sqrt{I}$, 即 $a\in\sqrt{\sqrt{I}}$.

再证 $\sqrt{\sqrt{I}}\subseteq\sqrt{I}$. 设 $a\in\sqrt{\sqrt{I}}$, 则存在 $n$ 使 $a^n\in\sqrt{I}$. 于是存在 $m$ 使 $\left(a^n\right)^m=a^{nm}\in I$, 故 $a\in\sqrt{I}$.

综上, $\sqrt{\sqrt{I}}=\sqrt{I}$. $\blacksquare$

### 习题四

（习题 2.2-13）设 $R$ 为交换环, 定义 $R$ 上的运算为 $a\circ b=a+b-ab$.
(1)证明 $\circ$ 满足结合律, 而且 $0\circ a=a$, $\forall a\in R$;
(2)证明 $R$ 为域当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群, 其中 $e$ 为 $R$ 的幺元.

### 解答 习题四

(1)对任意 $a,b,c\in R$,

$$
\begin{aligned}\left(a\circ b\right)\circ c&=\left(a+b-ab\right)\circ c\\&=\left(a+b-ab\right)+c-\left(a+b-ab\right)c\\&=a+b+c-ab-ac-bc+abc,\end{aligned}
$$

且

$$
\begin{aligned}a\circ\left(b\circ c\right)&=a\circ\left(b+c-bc\right)\\&=a+\left(b+c-bc\right)-a\left(b+c-bc\right)\\&=a+b+c-ab-ac-bc+abc.\end{aligned}
$$

两者相等, 故 $\circ$ 满足结合律. 又 $0\circ a=0+a-0\cdot a=a$. 此外因 $R$ 交换, $a\circ b=b\circ a$, 故 $\circ$ 也交换.

(2)作映射 $\psi:R\to R$, $\psi\left(x\right)=e-x$. 显然 $\psi$ 是双射, 且 $\psi\left(0\right)=e$, $\psi\left(e\right)=0$. 对任意 $a,b\in R$,

$$
\begin{aligned}\psi\left(a\right)\circ\psi\left(b\right)&=\left(e-a\right)\circ\left(e-b\right)\\&=\left(e-a\right)+\left(e-b\right)-\left(e-a\right)\left(e-b\right)\\&=e-ab\\&=\psi\left(ab\right).\end{aligned}
$$

故 $\psi$ 把 $R$ 的乘法同态地搬移到 $\circ$ 运算上, 且 $\psi$ 限制为 $R\setminus\left\{0\right\}$ 到 $R\setminus\left\{e\right\}$ 的双射. 因而 $\left(R\setminus\left\{0\right\},\cdot\right)$ 为交换群当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群.

而由**定义 2.2.20**（整环、除环与域）, 交换幺环 $R$ 为域当且仅当 $R\setminus\left\{0\right\}$ 关于乘法构成交换群. 因此 $R$ 为域当且仅当 $\left(R\setminus\left\{e\right\},\circ\right)$ 为交换群. $\blacksquare$
