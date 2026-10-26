# 作业 18

> **基础知识**（多项式带余除法）设 $R$ 为交换幺环, $f\left(x\right),g\left(x\right)\in R\left[x\right]$, 且 $g\left(x\right)$ 的首项系数为 $R$ 中的单位, 则存在唯一 $q\left(x\right),r\left(x\right)\in R\left[x\right]$ 使 $f\left(x\right)=q\left(x\right)g\left(x\right)+r\left(x\right)$, 其中 $r=0$ 或 $\deg r< \deg g$. 特别地, 除式为一次首一多项式 $x-a$ 时余式为常数.

> **基础知识**（唯一分解整环）一个整环 $R$ 称为唯一分解整环, 如果 $R$ 中每个非零非单位元素都可分解为有限个不可约元素的乘积, 且在相伴意义下分解唯一.

> **基础知识**（形式幂级数环）域 $k$ 上的形式幂级数环 $k\left[\!\left[t\right]\!\right]$ 由所有 $\sum_{n=0}^{\infty}a_nt^n$ 组成, 其单位恰为常数项非零的幂级数.

### 习题一

（习题 2.9-3）设 $R$ 是整环, $f\left(x\right)\in R\left[x\right]$, 则 $a\in R$ 为 $f\left(x\right)$ 的根当且仅当 $\left(x-a\right)$ 整除 $f\left(x\right)$.

### 解答 习题一

对 $f\left(x\right)$ 与首一多项式 $x-a$ 作带余除法, 由多项式带余除法, 存在 $q\left(x\right)\in R\left[x\right]$ 及常数 $c\in R$ 使

$$
f\left(x\right)=q\left(x\right)\left(x-a\right)+c,
$$

其中余式次数小于 $1$, 故为常数. 将 $x=a$ 代入, 注意 $a\in R$ 可与 $R\left[x\right]$ 中元素作求值同态, 得

$$
f\left(a\right)=q\left(a\right)\cdot0+c=c.
$$

于是 $a$ 为 $f\left(x\right)$ 的根, 即 $f\left(a\right)=0$, 当且仅当 $c=0$, 当且仅当 $f\left(x\right)=q\left(x\right)\left(x-a\right)$, 即 $\left(x-a\right)\mid f\left(x\right)$. $\blacksquare$

### 习题二

（习题 2.9-4）设 $R$ 是整环, $f\left(x\right)\in R\left[x\right]$, $a_1,a_2,\cdots,a_s$ 为 $f\left(x\right)$ 的不同的根, 则

$$
\left(x-a_1\right)\left(x-a_2\right)\cdots\left(x-a_s\right)
$$

整除 $f\left(x\right)$. 由此证明整环上次数为 $m$ 的非零多项式的不同根的个数最多为 $m$.

### 解答 习题二

对 $s$ 作归纳. 当 $s=1$ 时, 即习题一的结论.

设结论对 $s-1$ 成立, 即 $\prod_{i=1}^{s-1}\left(x-a_i\right)\mid f\left(x\right)$. 写

$$
f\left(x\right)=g\left(x\right)\prod_{i=1}^{s-1}\left(x-a_i\right).
$$

将 $x=a_s$ 代入, 因 $a_s$ 是 $f$ 的根, $f\left(a_s\right)=0$, 故

$$
0=g\left(a_s\right)\prod_{i=1}^{s-1}\left(a_s-a_i\right).
$$

由于 $a_1,\cdots,a_s$ 两两不同, $a_s-a_i\ne0$($1\le i\le s-1$). 又 $R$ 是整环, 无零因子, 故 $g\left(a_s\right)=0$. 由习题一, $\left(x-a_s\right)\mid g\left(x\right)$, 记 $g\left(x\right)=h\left(x\right)\left(x-a_s\right)$. 于是

$$
f\left(x\right)=h\left(x\right)\prod_{i=1}^{s}\left(x-a_i\right),
$$

即 $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. 归纳完成.

现设 $f\left(x\right)\ne0$ 次数为 $m$, 有 $s$ 个不同根 $a_1,\cdots,a_s$. 由上, $\prod_{i=1}^{s}\left(x-a_i\right)\mid f\left(x\right)$. 该乘积为 $s$ 次多项式, 它整除 $m$ 次多项式, 故次数 $s\le m$. 即整环上次数为 $m$ 的非零多项式的不同根的个数最多为 $m$. $\blacksquare$

### 习题三

（习题 2.9-11）试证明实数域 $\mathbb R$ 上的形式幂级数环 $\mathbb R\left[\!\left[t\right]\!\right]$ 是一个唯一分解整环.

### 解答 习题三

记 $R=\mathbb R\left[\!\left[t\right]\!\right]$. 任取非零幂级数 $f\left(t\right)=\sum_{n=0}^{\infty}a_nt^n\in R$. 设 $a_k$ 为其第一个非零系数, 即 $a_0=\cdots=a_{k-1}=0$, $a_k\ne0$, 称 $k$ 为 $f$ 的阶, 记 $\operatorname{ord}\left(f\right)=k$. 则

$$
f\left(t\right)=t^k\cdot\left(a_k+a_{k+1}t+\cdots\right)=t^k\,u\left(t\right),
$$

其中 $u\left(t\right)=a_k+a_{k+1}t+\cdots$ 的常数项 $a_k\ne0$. 由形式幂级数环的性质, $u\left(t\right)$ 是单位(常数项非零即可逆).

先确定 $R$ 的不可约元素. 若 $f$ 非零非单位, 则 $k=\operatorname{ord}\left(f\right)\ge1$, $f=t^ku$. 若 $k=1$, $f=t\,u$, $u$ 为单位, 故 $f$ 与 $t$ 相伴. 而 $t$ 不可约: 若 $t=\alpha\beta$, 则

$$
1=\operatorname{ord}\left(t\right)=\operatorname{ord}\left(\alpha\right)+\operatorname{ord}\left(\beta\right),
$$

故 $\operatorname{ord}\left(\alpha\right),\operatorname{ord}\left(\beta\right)$ 中一个为 $0$ 另一个为 $1$, 即其中一个为单位. 故 $t$ 不可约.

于是任何非零非单位元素 $f$ 都可写成

$$
f=t^k\,u, u\text{ 为单位},
$$

其中 $k=\operatorname{ord}\left(f\right)$ 被 $f$ 唯一确定. 即 $f$ 在相伴意义下唯一分解为不可约元素 $t$ 的 $k$ 次幂乘以单位. 又 $t$ 是素元素(

$$
t\mid fg\Rightarrow\operatorname{ord}\left(fg\right)\ge1\Rightarrow\operatorname{ord}\left(f\right)\ge1
$$

或 $\operatorname{ord}\left(g\right)\ge1$, 即 $t\mid f$ 或 $t\mid g$).

由唯一分解整环的定义, $R=\mathbb R\left[\!\left[t\right]\!\right]$ 是唯一分解整环. $\blacksquare$
