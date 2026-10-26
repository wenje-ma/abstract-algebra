# 作业 11

> **定义 2.1.1**（环）设 $R$ 是非空集合, 在 $R$ 上定义两种二元运算 $+$ 与 $\cdot$, 满足:
> (1)$\left[R;+\right]$ 是交换群;
> (2)$\left[R;\cdot\right]$ 是半群 (乘法满足结合律);
> (3)乘法对加法满足左右分配律: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$.
> 则称 $R$ 为一个环.

> **基础知识**（幺环中可逆元的性质）设 $R$ 为幺环, $e$ 为幺元. 若 $u,v\in R$ 可逆, 则 $uv$ 可逆, 且 $\left(uv\right)^{-1}=v^{-1}u^{-1}$. 若 $x^{m}=0$, 则有限几何级数给出
> $$
> \left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}.
> $$

### 习题一

（习题 2.1-3）设集合 $R=\left\{a,b,c\right\}$, 在 $R$ 上定义加法和乘法. 若加法 $+$ 和乘法 $\cdot$ 的运算表分别为
$$
\begin{array}{c\left|ccc}
+ & a & b & c\\hline
a & a & b & c\\
b & b & c & a\\
c & c & a & b
\end{array}
\begin{array}{c\right|ccc}
\cdot & a & b & c\\hline
a & a & a & a\\
b & a & a & a\\
c & a & b & a
\end{array}
$$
问 $R$ 是否构成环?

### 解答 习题一

由加法表可见, $a$ 是加法零元, 且 $\left(R,+\right)\cong\mathbb Z_3$ (对应 $a\mapsto0$, $b\mapsto1$, $c\mapsto2$), 故 $\left(R,+\right)$ 是交换群, 满足**定义 2.1.1**（环）的条件 (1).

下面检验分配律. 取 $x=b$, $y=c$, $z=b$. 由加法表, $b+c=a$. 由乘法表, $a\cdot b=a$, $b\cdot b=a$, $c\cdot b=b$.

先算左边:
$$
\left(x+y\right)z=\left(b+c\right)b=a\cdot b=a.
$$

再算右边:
$$
xz+yz=bb+cb=a+b=b.
$$

因 $a\ne b$, 故
$$
\left(b+c\right)b\ne bb+cb.
$$

左分配律不成立. 此外, 乘法的结合律亦不成立: 取 $x=c$, $y=c$, $z=b$, 由乘法表 $c\cdot c=a$, $c\cdot b=b$, $a\cdot b=a$, 则
$$
\left(c\cdot c\right)\cdot b=a\cdot b=a,
$$
而
$$
c\cdot\left(c\cdot b\right)=c\cdot b=b.
$$
二者不等.

因此 $R$ 不满足环定义中的分配律与乘法结合律, $R$ 不构成环. $\blacksquare$

### 习题二

（习题 2.1-5）设 $R$ 为幺环, $e$ 为幺元, $a\in R$. 若 $\exists m\in\mathbb N$ 使得 $a^{m}=0$, 则称 $a$ 为幂零元. 证明: 若 $a$ 为幂零元, 则 $e+a$ 为可逆元.

### 解答 习题二

设 $a^{m}=0$. 构造
$$
b=e-a+a^{2}-a^{3}+\cdots+\left(-1\right)^{m-1}a^{m-1}.
$$

计算乘积:
$$
\left(e+a\right)b=\left(e+a\right)\left(e-a+a^{2}-\cdots+\left(-1\right)^{m-1}a^{m-1}\right)=e+\left(-1\right)^{m-1}a^{m}=e,
$$

中间项全部抵消, 而 $a^{m}=0$. 同理,
$$
b\left(e+a\right)=e+\left(-1\right)^{m-1}a^{m}=e.
$$

故 $b$ 是 $e+a$ 的逆元, 即 $e+a$ 为可逆元. $\blacksquare$

### 习题三

（习题 2.1-15）(华罗庚)设 $R$ 为幺环, $e$ 为幺元, $a\in R$. 若元素 $c$ 满足 $ca=e$ ($ac=e$), 则称 $c$ 为 $a$ 的一个右逆元 (左逆元). 若 $c$ 既是 $a$ 的左逆元, 又是 $a$ 的右逆元, 则称 $c$ 为 $a$ 的逆元, 这时称 $a$ 可逆. 证明: 对任何 $a,b\in R$, $e-ab$ 可逆当且仅当 $e-ba$ 可逆.

### 解答 习题三

先设 $e-ab$ 可逆, 记其逆为 $c=\left(e-ab\right)^{-1}$. 构造
$$
d=e+bca.
$$

验证 $d$ 是 $e-ba$ 的逆元:
$$
\left(e-ba\right)d=\left(e-ba\right)\left(e+bca\right)=e-ba+bca-babca=e-ba+b\left(e-ab\right)ca=e-ba+ba=e,
$$

其中用到 $\left(e-ab\right)c=e$. 同理,
$$
d\left(e-ba\right)=\left(e+bca\right)\left(e-ba\right)=e-ba+bca-bcaba=e-ba+bc\left(e-ab\right)a=e-ba+ba=e,
$$

其中用到 $c\left(e-ab\right)=e$. 故 $d=e+bca$ 是 $e-ba$ 的逆元, $e-ba$ 可逆.

反之, 若 $e-ba$ 可逆, 将上述论证中 $a,b$ 互换, 即得 $e-ab$ 可逆.

因此 $e-ab$ 可逆当且仅当 $e-ba$ 可逆. $\blacksquare$

### 习题四

（习题 2.1-16）(华罗庚)设 $R$ 为幺环, $e$ 为幺元, $a,b\in R$. 证明: 若 $ab$, $ab-e$ 都可逆, 则 $a-b^{-1}$ 可逆, 且 $\left(a-b^{-1}\right)^{-1}-a^{-1}$ 也可逆, 且
$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

### 解答 习题四

因 $b$ 可逆, 有
$$
a-b^{-1}=\left(ab-e\right)b^{-1}.
$$

由题设 $ab-e$ 可逆, 又 $b^{-1}$ 可逆, 由**基础知识**（幺环中可逆元的性质）, 可逆元之积仍可逆, 故 $a-b^{-1}$ 可逆, 且
$$
\left(a-b^{-1}\right)^{-1}=b\left(ab-e\right)^{-1}.
$$

记 $X=ab-e$, 则 $X^{-1}$ 存在. 要证
$$
\left(a-b^{-1}\right)^{-1}-a^{-1}=bX^{-1}-a^{-1}
$$
可逆, 且其逆为 $aba-a=a\left(ba-e\right)$.

计算乘积:
$$
\left(bX^{-1}-a^{-1}\right)\cdot a\left(ba-e\right)=bX^{-1}a\left(ba-e\right)-a^{-1}a\left(ba-e\right)=\left[bX^{-1}a-e\right]\left(ba-e\right).
$$

由习题三的华罗庚恒等式,

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

同理可验另一方向乘积为 $e$. 故 $a\left(ba-e\right)=aba-a$ 是

$$
bX^{-1}-a^{-1}=\left(a-b^{-1}\right)^{-1}-a^{-1}
$$

的逆元, 即
$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$
$\blacksquare$
