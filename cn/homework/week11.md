# week11

> **基础知识: 幺环中可逆元的性质**<br>设 $R$ 为幺环, $e$ 为幺元. 若 $u,v\in R$ 均可逆, 则 $uv$ 可逆, 且 $\left(uv\right)^{-1}=v^{-1}u^{-1}$.

> **基础知识: 幂零元与有限几何级数**<br>设 $R$ 为幺环, $e$ 为幺元. 若 $x^{m}=0$ ($m\in\mathbb N$), 则有限几何级数给出
$$
\left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}.
$$

> **定义 2.1.1 (环)**<br>设 $R$ 是非空集合, 在 $R$ 上定义两种二元运算 $+$ 与 $\cdot$, 满足: (1) $\left[R;+\right]$ 是交换群; (2) $\left[R;\cdot\right]$ 是半群 (乘法满足结合律); (3) 乘法对加法满足左右分配律: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$ (对任意 $a,b,c\in R$). 则称 $R$ 为一个环.

---

## 2.1-3

设集合 $R=\left\{a,b,c\right\}$, 在 $R$ 上定义加法和乘法. 若加法 $+$ 和乘法 $\cdot$ 的运算表分别为

$$
\begin{array}{c|ccc}
+ & a & b & c\\\hline
a & a & b & c\\
b & b & c & a\\
c & c & a & b
\end{array}
\qquad
\begin{array}{c|ccc}
\cdot & a & b & c\\\hline
a & a & a & a\\
b & a & a & a\\
c & a & b & a
\end{array}
$$

问 $R$ 是否构成环?

### 解答 2.1-3

由加法表可见, $a$ 是加法零元, 且 $\left(R,+\right)\cong\mathbb Z_3$ (对应 $a\mapsto0$, $b\mapsto1$, $c\mapsto2$), 故 $\left(R,+\right)$ 是交换群, 满足**定义 2.1.1 (环)** 的条件 (1).

下面检验分配律. 取 $x=b$, $y=c$, $z=b$. 由加法表, $b+c=a$; 由乘法表, $a\cdot b=a$, $b\cdot b=a$, $c\cdot b=b$.

先算左边:

$$
\left(x+y\right)z=\left(b+c\right)b=a\cdot b=a.
$$

再算右边:

$$
xz+yz=b\cdot b+c\cdot b=a+b=b.
$$

因 $a\ne b$, 故

$$
\left(b+c\right)b\ne b\cdot b+c\cdot b.
$$

左分配律不成立.

此外, 乘法的结合律亦不成立: 取 $x=c$, $y=c$, $z=b$, 由乘法表 $c\cdot c=a$, $c\cdot b=b$, $a\cdot b=a$, 则

$$
\left(c\cdot c\right)\cdot b=a\cdot b=a,
$$

而

$$
c\cdot\left(c\cdot b\right)=c\cdot b=b.
$$

二者不等.

因此 $R$ 不满足**定义 2.1.1 (环)** 中的乘法结合律与分配律, $R$ 不构成环. $\blacksquare$

---

## 2.1-5

设 $R$ 为幺环, $e$ 为幺元, $a\in R$. 若存在 $m\in\mathbb N$ 使得 $a^{m}=0$, 则称 $a$ 为幂零元. 证明: 若 $a$ 为幂零元, 则 $e+a$ 为可逆元.

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

故 $b$ 是 $e+a$ 的逆元, 即 $e+a$ 为可逆元. 这与**基础知识: 幂零元与有限几何级数** 的结论一致. $\blacksquare$

---

## 2.1-15

(华罗庚) 设 $R$ 为幺环, $e$ 为幺元, $a\in R$. 若元素 $c$ 满足 $ca=e$ ($ac=e$), 则称 $c$ 为 $a$ 的一个左逆元 (右逆元). 若 $c$ 既是 $a$ 的左逆元, 又是 $a$ 的右逆元, 则称 $c$ 为 $a$ 的逆元, 这时称 $a$ 可逆. 证明: 对任何 $a,b\in R$, $e-ab$ 可逆当且仅当 $e-ba$ 可逆.

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

---

## 2.1-16

(华罗庚) 设 $R$ 为幺环, $e$ 为幺元, $a,b\in R$. 证明: 若 $ab$, $ab-e$ 都可逆, 则 $a-b^{-1}$ 可逆, 且 $\left(a-b^{-1}\right)^{-1}-a^{-1}$ 也可逆, 且

$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

### 解答 2.1-16

因 $b^{-1}$ 可逆 (结论中出现 $b^{-1}$, 题设蕴含 $b$ 可逆), 且 $ab$ 可逆, 由**基础知识: 幺环中可逆元的性质**, $a=\left(ab\right)b^{-1}$ 是可逆元之积, 故 $a$ 可逆, $a^{-1}$ 存在.

又因 $b^{-1}$ 可逆, 由**定义 2.1.1 (环)** 的分配律,

$$
a-b^{-1}=\left(ab-e\right)b^{-1}.
$$

由题设 $ab-e$ 可逆, 又 $b^{-1}$ 可逆, 由**基础知识: 幺环中可逆元的性质**, 可逆元之积仍可逆, 故 $a-b^{-1}$ 可逆, 且

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
\left(bX^{-1}-a^{-1}\right)\cdot a\left(ba-e\right)=bX^{-1}a\left(ba-e\right)-a^{-1}a\left(ba-e\right)=\left[bX^{-1}a-e\right]\left(ba-e\right).
$$

由 **2.1-15 题** 的华罗庚恒等式,

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
