# 作业 1

> **定义 1.1.4**（半群与幺半群）设 $S$ 是非空集合, 其上定义了一个满足结合律的二元运算 $*$, 则称 $\left[S;*\right]$ 为一个半群. 若半群中存在单位元 $e$, 即对任意 $a\in S$ 有 $ea=ae=a$, 则称该半群为幺半群; 若运算还满足交换律, 则称交换幺半群.

> **定义 1.1.10**（逆元）设 $S$ 是幺半群, $e$ 是单位元, $a\in S$. 若存在 $b\in S$ 使 $ba=e$($ab=e$), 则称 $b$ 为 $a$ 的左(右)逆元; 若 $ba=ab=e$, 则称 $b$ 为 $a$ 的逆元, 此时称 $a$ 为可逆元.

> **定义 1.1.14**（群与阿贝尔群）若幺半群 $G$ 中的每个元都是可逆元, 则称 $G$ 为一个群. 若群中运算还满足交换律, 则称 $G$ 为交换群或阿贝尔群.

> **引理 1.1.17**（消去律）群 $G$ 的运算满足左(右)消去律, 即对任意 $a,b,c\in G$, 由 $ab=ac$($ba=ca$)可推出 $b=c$.

> **例 1.1.7**（变换幺半群）设 $X$ 为非空集合, $M\left(X\right)$ 为 $X$ 上所有变换的全体, 则 $M\left(X\right)$ 在变换的复合下构成幺半群, 其单位元为 $X$ 的恒等变换.

> **基础知识**（对称差）对任意 $A,B\in\mathcal P\left(X\right)$, 对称差定义为
> $$
> A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right).
> $$

> **基础知识**（狄利克雷卷积）对 $f,g\in S$, 狄利克雷卷积定义为 
>
> $$
> \begin{aligned}\left(f*g\right)\left(n\right)&=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)\\&=\sum_{ab=n}f\left(a\right)g\left(b\right).\end{aligned}
> $$
>

### 习题一

（习题 1.1-8）试举出一个无限交换半群的例子, 它有单位元且满足消去律, 但不是群.

### 解答 习题一

取 $S=\mathbb N$(非负整数的全体), 运算为通常的加法 $+$.

首先, 加法满足结合律与交换律, 故由**定义 1.1.4**（半群与幺半群）, $\left(\mathbb N,+\right)$ 是交换半群.

其次, $0\in\mathbb N$, 且对任意 $a\in\mathbb N$ 有 $a+0=0+a=a$, 故 $0$ 是单位元, 因而 $\left(\mathbb N,+\right)$ 是交换幺半群.

再次, 对任意 $a,b,c\in\mathbb N$, 由 $a+c=b+c$ 可在 $\mathbb N$ 内移项得 $a=b$, 故 $\left(\mathbb N,+\right)$ 满足左(右)消去律.

最后, 元素 $1\in\mathbb N$ 不存在加法逆元, 即不存在 $b\in\mathbb N$ 使 $1+b=0$, 故并非每个元都可逆. 由**定义 1.1.14**（群与阿贝尔群）, $\left(\mathbb N,+\right)$ 不是群.

综上, $\left(\mathbb N,+\right)$ 是无限交换半群, 有单位元且满足消去律, 但不是群. $\blacksquare$

### 习题二

（习题 1.1-9）设 $\mathcal P\left(X\right)$ 为非空集合 $X$ 的幂集. 对任意 $A,B\in\mathcal P\left(X\right)$, 定义 $A$ 与 $B$ 的对称差为

$$
A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right).
$$

试证 $\left(\mathcal P\left(X\right),\triangle\right)$ 为一个群. 当 $X$ 只含有两个元素时, 试给出该群的群表, 此时称该群为克莱因群.

### 解答 习题二

对任意 $A\in\mathcal P\left(X\right)$, 用指示函数 $\chi_A:X\to\left\{0,1\right\}$ 刻画 $A$. 由于 $A\triangle B$ 恰由那些恰好属于 $A,B$ 中一个的元素组成, 故

$$
\chi_{A\triangle B}=\chi_A+\chi_B\pmod 2.
$$

下面逐条验证群的四条公理.

**封闭性** 对任意 $A,B\in\mathcal P\left(X\right)$, 显然 $A\triangle B\in\mathcal P\left(X\right)$, 故 $\triangle$ 是 $\mathcal P\left(X\right)$ 上的二元运算.

**结合律** 由模 $2$ 加法的结合律,

$$
\begin{aligned}\chi_{\left(A\triangle B\right)\triangle C}&=\left(\chi_A+\chi_B\right)+\chi_C\\&=\chi_A+\left(\chi_B+\chi_C\right)\\&=\chi_{A\triangle\left(B\triangle C\right)},\end{aligned}
$$

故

$$
\left(A\triangle B\right)\triangle C=A\triangle\left(B\triangle C\right).
$$

**单位元** 对任意 $A\in\mathcal P\left(X\right)$, 有 $A\triangle\varnothing=\varnothing\triangle A=A$, 故 $\varnothing$ 是单位元.

**逆元** 对任意 $A\in\mathcal P\left(X\right)$, 有 $A\triangle A=\varnothing$, 故每个元素的逆元为其自身.

由**定义 1.1.14**（群与阿贝尔群）, $\left(\mathcal P\left(X\right),\triangle\right)$ 是一个群.

当 $X=\left\{1,2\right\}$ 时,

$$
\mathcal P\left(X\right)=\left\{\varnothing,\left\{1\right\},\left\{2\right\},\left\{1,2\right\}\right\}.
$$

记 $0=\varnothing$, $a=\left\{1\right\}$, $b=\left\{2\right\}$, $c=\left\{1,2\right\}$, 则各元素均自逆, 该群的群表为

$$
\begin{array}{c|cccc}
\triangle & 0 & a & b & c\\hline
0 & 0 & a & b & c\\
a & a & 0 & c & b\\
b & b & c & 0 & a\\
c & c & b & a & 0
\end{array}
$$

此即克莱因四元群. $\blacksquare$

### 习题三

（习题 1.1-16）设 $A\in\mathbb R^{n\times n}$, $B\in\mathbb R^n$, 定义 $\mathbb R^n$ 上的变换 $T\left(A,B\right)$ 为

$$
T\left(A,B\right)\left(\alpha\right)=A\alpha+B,\forall\alpha\in\mathbb R^n.
$$

(1)证明: 当 $\left|A\right|\ne0$ 时, $T\left(A,B\right)$ 是双射;

(2)证明:

$$
\mathrm{Aff}\left(n,\mathbb R\right)=\left\{T\left(A,B\right)\mid\left|A\right|\ne0\right\}
$$

关于映射的复合构成群, 称为 $\mathbb R^n$ 的仿射变换群.

### 解答 习题三

(1)设 $\left|A\right|\ne0$, 则 $A$ 可逆.

**单射** 若

$$
T\left(A,B\right)\left(\alpha_1\right)=T\left(A,B\right)\left(\alpha_2\right),
$$

则

$$
A\alpha_1+B=A\alpha_2+B,
$$

即 $A\left(\alpha_1-\alpha_2\right)=0$. 因 $A$ 可逆, 左乘 $A^{-1}$ 得 $\alpha_1-\alpha_2=0$, 故 $\alpha_1=\alpha_2$.

**满射** 对任意 $\beta\in\mathbb R^n$, 取 $\alpha=A^{-1}\left(\beta-B\right)$, 则

$$
\begin{aligned}T\left(A,B\right)\left(\alpha\right)&=A\left(A^{-1}\left(\beta-B\right)\right)+B\\&=\beta.\end{aligned}
$$

故 $T\left(A,B\right)$ 是双射.

(2)逐条验证 $\mathrm{Aff}\left(n,\mathbb R\right)$ 关于映射复合构成群.

**封闭性** 对

$$
T\left(A,B\right),T\left(C,D\right)\in\mathrm{Aff}\left(n,\mathbb R\right),
$$

对任意 $\alpha\in\mathbb R^n$,

$$
\begin{aligned}T\left(A,B\right)\circ T\left(C,D\right)\left(\alpha\right)&=A\left(C\alpha+D\right)+B\\&=\left(AC\right)\alpha+\left(AD+B\right)\\&=T\left(AC,AD+B\right)\left(\alpha\right).\end{aligned}
$$

又 $\left|AC\right|=\left|A\right|\left|C\right|\ne0$, 故

$$
T\left(AC,AD+B\right)\in\mathrm{Aff}\left(n,\mathbb R\right),
$$

即运算封闭.

**结合律** 映射的复合满足结合律.

**单位元** $T\left(I,0\right)$ 是恒等变换, 且 $\left|I\right|=1\ne0$, 故 $T\left(I,0\right)\in\mathrm{Aff}\left(n,\mathbb R\right)$, 且对任意 $T\left(A,B\right)$ 有

$$
\begin{aligned}T\left(A,B\right)\circ T\left(I,0\right)&=T\left(AI,A\cdot0+B\right)\\&=T\left(A,B\right).\end{aligned}
$$

**逆元** 对 $T\left(A,B\right)\in\mathrm{Aff}\left(n,\mathbb R\right)$, 因 $\left|A^{-1}\right|\ne0$, 故

$$
T\left(A^{-1},-A^{-1}B\right)\in\mathrm{Aff}\left(n,\mathbb R\right),
$$

且

$$
\begin{aligned}T\left(A^{-1},-A^{-1}B\right)\circ T\left(A,B\right)&=T\left(A^{-1}A,A^{-1}B-A^{-1}B\right)\\&=T\left(I,0\right),\end{aligned}
$$

故 $T\left(A^{-1},-A^{-1}B\right)$ 是 $T\left(A,B\right)$ 的逆元.

综上, 由**定义 1.1.14**（群与阿贝尔群）, $\mathrm{Aff}\left(n,\mathbb R\right)$ 关于映射的复合构成群. $\blacksquare$

### 习题四

（习题 1.1-20）设 $S$ 是所有数论函数(即 $\mathbb N\to\mathbb C$ 的映射)的全体. 对 $f,g\in S$, 定义狄利克雷卷积为

$$
\begin{aligned}\left(f*g\right)\left(n\right)&=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)\\&=\sum_{ab=n}f\left(a\right)g\left(b\right).\end{aligned}
$$

(1)证明: $\left(S,*\right)$ 为一个交换幺半群;

(2)证明: $f$ 可逆当且仅当 $f\left(1\right)\ne0$;

(3)称 $f$ 为积性函数, 如果 $\left(m,n\right)=1$ 时有 $f\left(mn\right)=f\left(m\right)f\left(n\right)$. 证明: 所有非零积性函数的全体在运算 $*$ 下构成一个阿贝尔群;

(4)称 $f$ 为完全积性函数, 如果对任意 $m,n\in\mathbb N^+$ 有 $f\left(mn\right)=f\left(m\right)f\left(n\right)$. 所有非零完全积性函数的全体在运算 $*$ 下是否构成一个阿贝尔群?

### 解答 习题四

(1)逐条验证 $\left(S,*\right)$ 是交换幺半群.

**封闭性** 对任意 $f,g\in S$, 由定义知 $f*g$ 是 $\mathbb N\to\mathbb C$ 的映射, 故 $f*g\in S$.

**交换性** 由

$$
\left(f*g\right)\left(n\right)=\sum_{ab=n}f\left(a\right)g\left(b\right)
$$

交换 $a,b$ 的次序得

$$
\begin{aligned}\left(f*g\right)\left(n\right)&=\sum_{ba=n}g\left(b\right)f\left(a\right)\\&=\left(g*f\right)\left(n\right),\end{aligned}
$$

故 $f*g=g*f$.

**结合律** 对任意 $n$,

$$
\begin{aligned}\left(\left(f*g\right)*h\right)\left(n\right)&=\sum_{ab=n}\left(f*g\right)\left(a\right)h\left(b\right)\\&=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right),\end{aligned}
$$

且

$$
\begin{aligned}\left(f*\left(g*h\right)\right)\left(n\right)&=\sum_{ab=n}f\left(a\right)\left(g*h\right)\left(b\right)\\&=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right),\end{aligned}
$$

两者同为三重和 $\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right)$, 故 $\left(f*g\right)*h=f*\left(g*h\right)$.

**单位元** 定义 $e\in S$ 为 $e\left(1\right)=1$, 且当 $n>1$ 时 $e\left(n\right)=0$. 则

$$
\begin{aligned}\left(e*f\right)\left(n\right)&=\sum_{d\mid n}e\left(d\right)f\left(\frac{n}{d}\right)\\&=e\left(1\right)f\left(n\right)\\&=f\left(n\right),\end{aligned}
$$

同理 $f*e=f$. 故 $e$ 是单位元.

由**定义 1.1.4**（半群与幺半群）, $\left(S,*\right)$ 是交换幺半群.

(2)**必要性** 若 $f$ 可逆, 则存在 $g\in S$ 使 $f*g=e$. 于是

$$
\begin{aligned}\left(f*g\right)\left(1\right)&=f\left(1\right)g\left(1\right)\\&=e\left(1\right)\\&=1,\end{aligned}
$$

故 $f\left(1\right)g\left(1\right)=1$, 特别地 $f\left(1\right)\ne0$.

**充分性** 设 $f\left(1\right)\ne0$. 归纳构造 $g\in S$: 令 $g\left(1\right)=f\left(1\right)^{-1}$. 对 $n>1$, 要求 $\left(f*g\right)\left(n\right)=0$, 即

$$
f\left(1\right)g\left(n\right)+\sum_{\substack{d\mid n\\d>1}}f\left(d\right)g\left(\frac{n}{d}\right)=0,
$$

解得

$$
g\left(n\right)=-f\left(1\right)^{-1}\sum_{\substack{d\mid n\\d>1}}f\left(d\right)g\left(\frac{n}{d}\right).
$$

右端只涉及下标 $n/d<n$ 处已定义的 $g$, 故可递归定义出 $g\in S$ 使 $f*g=e$. 由**定义 1.1.10**（逆元）, $f$ 可逆.

(3)记 $F$ 为非零积性函数全体.

先证非零积性函数满足 $f\left(1\right)=1$. 因 $f\ne0$, 存在 $m\in\mathbb N^+$ 使 $f\left(m\right)\ne0$. 又 $\left(1,1\right)=1$, 由积性得 $f\left(1\right)=f\left(1\cdot1\right)=f\left(1\right)^2$, 故 $f\left(1\right)=0$ 或 $1$. 若 $f\left(1\right)=0$, 则

$$
\begin{aligned}f\left(m\right)&=f\left(1\cdot m\right)\\&=f\left(1\right)f\left(m\right)\\&=0,\end{aligned}
$$

矛盾. 故 $f\left(1\right)=1\ne0$.

**封闭性** 设 $f,g$ 积性. 对 $\left(m,n\right)=1$, 任意 $d\mid mn$ 可唯一分解为 $d=d_1d_2$ 且 $d_1\mid m$, $d_2\mid n$, 此时 $\left(d_1,d_2\right)=1$, $\left(m/d_1,n/d_2\right)=1$. 于是

$$
\begin{aligned}\left(f*g\right)\left(mn\right)&=\sum_{d_1\mid m}\sum_{d_2\mid n}f\left(d_1\right)f\left(d_2\right)g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right)\\&=\left(f*g\right)\left(m\right)\left(f*g\right)\left(n\right),\end{aligned}
$$

故 $f*g$ 积性. 又

$$
\left(f*g\right)\left(1\right)=f\left(1\right)g\left(1\right)=1\ne0,
$$

故 $f*g\in F$.

**单位元** $e$ 是积性函数, 且 $e\left(1\right)=1\ne0$, 故 $e\in F$.

**逆元** 由(2), $f\in F$ 可逆, 设 $f*g=e$. 由(3)中归纳递推及 $f$ 的积性可证 $g$ 亦为积性函数; 且 $g\left(1\right)=f\left(1\right)^{-1}=1\ne0$, 故 $g\in F$.

**交换性** 由(1), 卷积满足交换律.

综上, 由**定义 1.1.14**（群与阿贝尔群）, $F$ 在 $*$ 下构成阿贝尔群.

(4)不构成. 事实上, 非零完全积性函数全体在卷积下不封闭. 取 $f\left(n\right)=1$(常数函数), 对任意 $m,n\in\mathbb N^+$ 有 $f\left(mn\right)=1=f\left(m\right)f\left(n\right)$, 故 $f$ 是完全积性的. 但

$$
\begin{aligned}\left(f*f\right)\left(n\right)&=\sum_{d\mid n}1\\&=\tau\left(n\right),\end{aligned}
$$

其中 $\tau\left(n\right)$ 为 $n$ 的正因子个数. 取 $n=4$, 则 $\tau\left(4\right)=3$, 而 $\tau\left(2\right)\tau\left(2\right)=4$, 故 $\tau\left(4\right)\ne\tau\left(2\right)\tau\left(2\right)$.

故 $f*f$ 不是完全积性函数, 即 $f*f$ 不属于非零完全积性函数全体. 因而该集合对卷积不封闭, 不构成群, 更不构成阿贝尔群. $\blacksquare$
