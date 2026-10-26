# 作业 15

> **定义 2.5.2**（相伴）设 $R$ 为整环, $a,b\in R$. 如果存在 $R$ 中单位 $u$ 使得 $a=ub$, 则称 $a$ 与 $b$ 相伴, 记为 $a\sim b$.

> **定义 2.5.6**（不可约元素）设 $R$ 为整环, $\alpha\in R^*\setminus U$. 如果 $\alpha$ 不存在非平凡因子, 则称 $\alpha$ 为不可约元素, 否则称 $\alpha$ 为可约元素.

> **定义 2.5.14**（公因子与最大公因子）设 $R$ 为整环, $a_1,a_2,\cdots,a_n\in R$. 若 $c\in R$ 同时整除所有 $a_i$, 则称 $c$ 为它们的公因子; 若公因子 $d$ 能被任一公因子整除, 则称 $d$ 为最大公因子.

> **定理 2.5.15**（唯一分解整环的等价条件）整环 $R$ 为唯一分解整环, 当且仅当 $R$ 满足因子链条件与素条件, 即在唯一分解整环中每个不可约元素都是素元素: $p\mid ab$ 可推出 $p\mid a$ 或 $p\mid b$.

### 习题一

（习题 2.5-8）设 $R=\mathbb Z\left[\sqrt{-5}\right]$.
(1)试证明: 若 $a^2+5b^2=9$, 则 $a+b\sqrt{-5}$ 是不可约元素;
(2)试证明: 元素 $\alpha=6+3\sqrt{-5}$, $\beta=9$ 在 $R$ 中不存在最大公因子.

### 解答 习题一

在 $R$ 上定义范数

$$
N\left(x+y\sqrt{-5}\right)=x^2+5y^2,
$$

则 $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$, 且 $\xi$ 为单位当且仅当 $N\left(\xi\right)=1$.

(1)设 $\gamma=a+b\sqrt{-5}$, 则 $N\left(\gamma\right)=a^2+5b^2=9\ne1$, 故 $\gamma$ 非单位, 即 $\gamma\in R^*\setminus U$. 反设 $\gamma=\xi\eta$ 为非平凡分解, 则

$$
N\left(\xi\right)N\left(\eta\right)=N\left(\gamma\right)=9.
$$

范数的取值为非负整数 $x^2+5y^2$. 不存在范数为 $3$ 的元素: $x^2+5y^2=3$ 在 $y=0$ 时要求 $x^2=3$, 非平方数; 在 $\left|y\right|\ge1$ 时 $5> 3$. 故 $N\left(\xi\right),N\left(\eta\right)$ 只能取 $1$ 或 $9$. 若 $N\left(\xi\right)=1$, 则 $\xi$ 为单位; 若 $N\left(\xi\right)=9$, 则 $N\left(\eta\right)=1$, $\eta$ 为单位.

因而 $\gamma$ 的任一分解中必有一个因子为单位, 由**定义 2.5.6**（不可约元素）, $\gamma$ 为不可约元素.

(2)先作分解:

$$
\beta=9=\left(2+\sqrt{-5}\right)\left(2-\sqrt{-5}\right),
$$

$$
\alpha=6+3\sqrt{-5}=3\left(2+\sqrt{-5}\right).
$$

其中 $N\left(3\right)=9$,

$$
N\left(2+\sqrt{-5}\right)=N\left(2-\sqrt{-5}\right)=9,
$$

由(1)均不可约.

$3$ 同时整除 $\alpha$ 与 $\beta$, $2+\sqrt{-5}$ 也同时整除 $\alpha$ 与 $\beta$, 二者都是公因子. 但 $2-\sqrt{-5}$ 不整除 $\alpha$: 若存在 $\gamma\in R$ 使 $\gamma\left(2-\sqrt{-5}\right)=\alpha$, 则

$$
\gamma=\frac{3\left(2+\sqrt{-5}\right)}{2-\sqrt{-5}}=\frac{3\left(2+\sqrt{-5}\right)^2}{9}=3+\frac{4}{3}\sqrt{-5}\notin R.
$$

又 $3\nmid\left(2+\sqrt{-5}\right)$(否则 $\left(2+\sqrt{-5}\right)/3\notin R$), 且 $\left(2+\sqrt{-5}\right)\nmid 3$

$$
\left(\text{否则 }3/\left(2+\sqrt{-5}\right)=\left(2-\sqrt{-5}\right)/3\notin R\right),
$$

二者互不整除.

反设 $d$ 是 $\alpha,\beta$ 的最大公因子. 由**定义 2.5.14**（公因子与最大公因子）, 每个公因子都应整除 $d$, 特别地 $3\mid d$ 且 $\left(2+\sqrt{-5}\right)\mid d$. 但 $d\mid\beta=9$, 而 $9$ 在相伴意义下的因子只有 $1,3,2+\sqrt{-5},2-\sqrt{-5},9$(无范数为 $3$ 的元素). 这些因子中没有一个同时被 $3$ 与 $2+\sqrt{-5}$ 整除, 矛盾.

故 $\alpha,\beta$ 在 $R$ 中不存在最大公因子. $\blacksquare$

### 习题二

（习题 2.5-10）设 $R=\mathbb Z\left[\omega\right]$, 其中 $\omega=\frac{1+\sqrt{-3}}{2}$(即 $\mathbb Q\left(\sqrt{-3}\right)$ 的代数整数环).
(1)证明 $R$ 在数的加法和乘法下构成一个整环;
(2)证明 $R$ 的所有单位是 $\pm1$, $\frac{\pm1\pm\sqrt{-3}}{2}$;
(3)证明在 $R$ 中 $2$ 与 $1+\sqrt{-3}$ 相伴.

### 解答 习题二

注意 $\omega^2=\omega-1$, 故

$$
R=\left\{m+n\omega\mid m,n\in\mathbb Z\right\}
$$

对乘法封闭($\omega^2=\omega-1\in R$).

(1)$R\subseteq\mathbb C$, 对加法, 乘法封闭, 含幺元 $1$, 而 $\mathbb C$ 无零因子, 故 $R$ 是无零因子的交换幺环, 即整环.

(2)定义范数

$$
N\left(m+n\omega\right)=\left(m+n\omega\right)\left(m+n\bar\omega\right)=m^2+mn+n^2,
$$

其中 $\bar\omega=\frac{1-\sqrt{-3}}{2}$. 则 $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$, 且 $\xi$ 为单位当且仅当 $N\left(\xi\right)=1$. 解 $m^2+mn+n^2=1$ 得

$$
\left(m,n\right)=\left(\pm1,0\right),\;\left(0,\pm1\right),\;\left(1,-1\right),\;\left(-1,1\right).
$$

对应元素为 $\pm1$, $\pm\omega=\frac{\pm1\pm\sqrt{-3}}{2}$, $\pm\left(1-\omega\right)=\frac{\pm1\mp\sqrt{-3}}{2}$. 故 $R$ 的全部单位为 $\pm1$ 及 $\frac{\pm1\pm\sqrt{-3}}{2}$.

(3)因 $1+\sqrt{-3}=2\omega$, 而 $\omega$ 是单位, 由**定义 2.5.2**（相伴）, $2$ 与 $1+\sqrt{-3}$ 相伴. $\blacksquare$

### 习题三

（习题 2.5-15）已知 $\mathbb Q\left[x,y\right]$ 在多项式加法和乘法下构成环, 证明: $x$ 与 $y$ 互素. 试问是否存在 $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ 使得 $r\left(x,y\right)x+s\left(x,y\right)y=1$?

### 解答 习题三

$\mathbb Q\left[x,y\right]$ 是唯一分解整环. $x,y$ 都是不可约元素, 且不相伴(二者相差的单位只能是 $\mathbb Q^*$ 中非零常数, 而 $x\ne cy$). 由**定义 2.5.14**（公因子与最大公因子）, $x,y$ 的公因子只能是单位, 故其最大公因子为单位, 即 $x,y$ 互素.

但不存在这样的 $r,s$. 反设存在, 将等式两边在 $\left(0,0\right)$ 处取值, 得

$$
r\left(0,0\right)\cdot0+s\left(0,0\right)\cdot0=1,
$$

即 $0=1$, 矛盾.

故虽然 $x,y$ 互素, 却不存在 $r x+s y=1$. $\blacksquare$
