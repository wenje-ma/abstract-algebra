# week1

> **基础知识: 非负整数加法的基本性质**<br>$\mathbb N=\left\{0,1,2,\cdots\right\}$ 对通常加法封闭, 加法满足结合律与交换律; $0\in\mathbb N$ 是加法单位元, 即对任意 $a\in\mathbb N$ 有 $0+a=a+0=a$; 加法满足消去律, 即由 $a+c=b+c$ 可推出 $a=b$; 且对任意 $a\in\mathbb N$ 有 $1+a\ge1>0$, 故不存在 $b\in\mathbb N$ 使 $1+b=0$.

> **基础知识: 幂集,指示函数与对称差**<br>设 $X$ 为非空集合, $P\left(X\right)$ 为 $X$ 的所有子集的集合 (幂集). 对 $A\subseteq X$, 指示函数 $\chi_A:X\to\left\{0,1\right\}$ 定义为 $\chi_A\left(x\right)=1$ 当且仅当 $x\in A$; 映射 $A\mapsto\chi_A$ 是单射. 对称差定义为 $A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right)$, 且 $\chi_{A\triangle B}=\chi_A+\chi_B\pmod2$.

> **基础知识: 模 2 加法**<br>集合 $\left\{0,1\right\}$ 上的模 2 加法满足结合律与交换律, $0$ 是单位元, 且每个元素自逆, 即对任意 $x\in\left\{0,1\right\}$ 有 $x+x=0\pmod2$.

> **基础知识: 方阵可逆性与行列式**<br>对方阵 $A\in\mathbb R^{n\times n}$, $A$ 可逆当且仅当 $\left|A\right|\ne0$; 行列式满足乘性, 即 $\left|AC\right|=\left|A\right|\left|C\right|$; 若 $A$ 可逆, 则 $A^{-1}$ 也可逆且 $\left|A^{-1}\right|\ne0$.

> **基础知识: 矩阵乘法结合律**<br>矩阵乘法满足结合律, 即对任意 $A,B,C\in\mathbb R^{n\times n}$ 有 $\left(AB\right)C=A\left(BC\right)$.

> **基础知识: 数论函数与狄利克雷卷积**<br>数论函数是 $\mathbb N^*\to\mathbb C$ 的映射. 对 $f,g\in S$, 狄利克雷卷积定义为 $\left(f*g\right)\left(n\right)=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)=\sum_{ab=n}f\left(a\right)g\left(b\right)$; 定义 $e\in S$ 为 $e\left(1\right)=1$ 且 $n>1$ 时 $e\left(n\right)=0$. 有限和可重排, 即 $\sum_{d\mid n}\sum_{e\mid\frac{n}{d}}f\left(d\right)g\left(e\right)h\left(\frac{n}{de}\right)=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right)$.

> **基础知识: 互素因子的唯一分解**<br>若 $\left(m,n\right)=1$, 则 $d\mid mn$ 可唯一地分解为 $d=d_1d_2$, 其中 $d_1\mid m$, $d_2\mid n$, 且此时 $\left(d_1,d_2\right)=1$, $\left(\frac{m}{d_1},\frac{n}{d_2}\right)=1$.

> **基础知识: 积性函数与完全积性函数**<br>称数论函数 $f$ 为积性函数, 如果 $\left(m,n\right)=1$ 时 $f\left(mn\right)=f\left(m\right)f\left(n\right)$; 称 $f$ 为完全积性函数, 如果对任意 $m,n\in\mathbb N^*$ 有 $f\left(mn\right)=f\left(m\right)f\left(n\right)$.

> **基础知识: 正因子个数函数**<br>记 $\tau\left(n\right)=\sum_{d\mid n}1$ 为 $n$ 的正因子个数; 特别地, $\tau\left(2\right)=2$, $\tau\left(4\right)=3$.

> **定义 1.1.4 (半群与幺半群)**<br>若非空集合 $S$ 中定义了一个满足结合律的二元运算 $*$, 则称 $\left\{S;*\right\}$ 为一个半群, 将 $a*b$ 简记为 $ab$. 若半群 $S$ 中存在元素 $e$, 对任意 $a\in S$ 有 $ea=a$ (或 $ae=a$), 则称 $e$ 为 $S$ 的左(右)幺元; 若 $e$ 既是左幺元又是右幺元, 则称 $e$ 为 $S$ 的幺元, 含幺元的半群称为幺半群; 若 $S$ 中的运算还满足交换律, 则称 $S$ 为交换幺半群.

> **例 1.1.7 (变换幺半群)**<br>记 $M\left(X\right)$ 为非空集合 $X$ 上的所有变换的集合, 则 $M\left(X\right)$ 在变换的乘法 (即复合) 下构成一个幺半群, 其幺元就是 $X$ 的恒等变换 $\mathrm{id}_X$.

> **定义 1.1.10 (逆元)**<br>设 $S$ 是幺半群, $e$ 是幺元, $a\in S$. 若存在 $b\in S$ 使得 $ba=e$ ($ab=e$), 则称 $b$ 为 $a$ 的左(右)逆元. 若 $b$ 既是 $a$ 的左逆元又是 $a$ 的右逆元, 即有 $ba=ab=e$, 则称 $b$ 为 $a$ 的逆元, 这时称 $a$ 为可逆元.

> **定义 1.1.14 (群与阿贝尔群)**<br>如果幺半群 $G$ 中的每个元都是可逆元, 则称 $G$ 为一个群. 若群中运算还满足交换律, 则称 $G$ 为交换群或阿贝尔群.

---

## 1.1-8

试举出一个无限交换半群的例子, 它有单位元且满足消去律, 但不是群.

### 解答 1.1-8

取 $S=\mathbb N$ (非负整数的全体), 运算为通常的加法 $+$.

**第一步: 验证 $\left(\mathbb N,+\right)$ 是交换半群.** 由**基础知识: 非负整数加法的基本性质**, $\mathbb N$ 对加法封闭, 且加法满足结合律与交换律. 故 $\mathbb N$ 上定义了一个满足结合律与交换律的二元运算 $+$, 依据**定义 1.1.4 (半群与幺半群)**, $\left(\mathbb N,+\right)$ 是交换半群.

**第二步: 验证 $\left(\mathbb N,+\right)$ 是交换幺半群.** 由**基础知识: 非负整数加法的基本性质**, $0\in\mathbb N$, 且对任意 $a\in\mathbb N$ 有 $0+a=a+0=a$. 故 $0$ 是 $\left(\mathbb N,+\right)$ 的幺元, 依据**定义 1.1.4 (半群与幺半群)**, 含幺元的半群是幺半群, 故 $\left(\mathbb N,+\right)$ 是交换幺半群.

**第三步: 验证消去律.** 对任意 $a,b,c\in\mathbb N$, 若 $a+c=b+c$, 由**基础知识: 非负整数加法的基本性质** (加法消去律), 得 $a=b$. 故 $\left(\mathbb N,+\right)$ 满足左(右)消去律.

**第四步: 验证 $\left(\mathbb N,+\right)$ 不是群.** 由**基础知识: 非负整数加法的基本性质**, 对任意 $b\in\mathbb N$ 有 $1+b\ge1>0$, 故不存在 $b\in\mathbb N$ 使 $1+b=0$. 因此 $1\in\mathbb N$ 不存在加法逆元, 即并非每个元素都可逆. 依据**定义 1.1.10 (逆元)** 与**定义 1.1.14 (群与阿贝尔群)**, 群要求每个元素都是可逆元, 故 $\left(\mathbb N,+\right)$ 不是群.

综上, $\left(\mathbb N,+\right)$ 是无限交换半群, 有单位元且满足消去律, 但不是群. $\blacksquare$

---

## 1.1-9

设 $P\left(X\right)$ 为非空集合 $X$ 的幂集. 对任意 $A,B\in P\left(X\right)$, 定义 $A$ 与 $B$ 的对称差为

$$
A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right).
$$

这里 $A\setminus B=\left\{x\in A\mid x\notin B\right\}$. 试证 $\left(P\left(X\right),\triangle\right)$ 为一个群. 当 $X$ 只含有两个元素时, 试给出该群的群表, 此时称该群为克莱因群.

### 解答 1.1-9

对任意 $A\in P\left(X\right)$, 用指示函数 $\chi_A:X\to\left\{0,1\right\}$ 刻画 $A$. 由**基础知识: 幂集,指示函数与对称差**, $A\mapsto\chi_A$ 是单射, 且 $\chi_{A\triangle B}=\chi_A+\chi_B\pmod2$.

**第一步: 封闭性.** 对任意 $A,B\in P\left(X\right)$, 由**基础知识: 幂集,指示函数与对称差**, $A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right)\subseteq X$, 故 $A\triangle B\in P\left(X\right)$. 因此 $\triangle$ 是 $P\left(X\right)$ 上的二元运算.

**第二步: 结合律.** 对任意 $A,B,C\in P\left(X\right)$, 由**基础知识: 幂集,指示函数与对称差**, $\chi_{\left(A\triangle B\right)\triangle C}=\left(\chi_A+\chi_B\right)+\chi_C\pmod2$ 且 $\chi_{A\triangle\left(B\triangle C\right)}=\chi_A+\left(\chi_B+\chi_C\right)\pmod2$. 由**基础知识: 模 2 加法** (结合律), $\left(\chi_A+\chi_B\right)+\chi_C=\chi_A+\left(\chi_B+\chi_C\right)\pmod2$. 故 $\chi_{\left(A\triangle B\right)\triangle C}=\chi_{A\triangle\left(B\triangle C\right)}$. 因 $A\mapsto\chi_A$ 是单射 (**基础知识: 幂集,指示函数与对称差**), $\left(A\triangle B\right)\triangle C=A\triangle\left(B\triangle C\right)$. 依据**定义 1.1.4 (半群与幺半群)**, $\left(P\left(X\right),\triangle\right)$ 是半群.

**第三步: 幺元.** 对任意 $A\in P\left(X\right)$, 由对称差定义 (**基础知识: 幂集,指示函数与对称差**), $A\triangle\varnothing=\left(A\setminus\varnothing\right)\cup\left(\varnothing\setminus A\right)=A$. 故 $\varnothing$ 是幺元, 依据**定义 1.1.4 (半群与幺半群)**, $\left(P\left(X\right),\triangle\right)$ 是幺半群.

**第四步: 逆元.** 对任意 $A\in P\left(X\right)$, 由对称差定义, $A\triangle A=\left(A\setminus A\right)\cup\left(A\setminus A\right)=\varnothing$. 故 $A\triangle A=\varnothing$, 即 $A$ 以自身为逆元, 依据**定义 1.1.10 (逆元)**, 每个元素 $A\in P\left(X\right)$ 都可逆 (逆元为其自身).

**第五步: 成群.** 由第二至四步, $\left(P\left(X\right),\triangle\right)$ 是幺半群且每个元素都可逆, 依据**定义 1.1.14 (群与阿贝尔群)**, $\left(P\left(X\right),\triangle\right)$ 是一个群.

当 $X=\left\{1,2\right\}$ 时, $P\left(X\right)=\left\{\varnothing,\left\{1\right\},\left\{2\right\},\left\{1,2\right\}\right\}$. 记 $0=\varnothing$, $a=\left\{1\right\}$, $b=\left\{2\right\}$, $c=\left\{1,2\right\}$. 由第四步, 各元素均以自身为逆元. 由对称差定义 (**基础知识: 幂集,指示函数与对称差**) 逐项计算 $a\triangle b=\left\{1,2\right\}=c$, $a\triangle c=\left\{2\right\}=b$, $b\triangle c=\left\{1\right\}=a$, 得群表

$$
\begin{array}{c|cccc}
\triangle & 0 & a & b & c\\\hline
0 & 0 & a & b & c\\
a & a & 0 & c & b\\
b & b & c & 0 & a\\
c & c & b & a & 0
\end{array}
$$

此即克莱因四元群. $\blacksquare$

---

## 1.1-16

设 $A\in\mathbb R^{n\times n}$, $\beta\in\mathbb R^n$, 定义 $\mathbb R^n$ 上的变换 $T_{\left(A,\beta\right)}$ 为

$$
T_{\left(A,\beta\right)}\left(\alpha\right)=A\alpha+\beta,\quad\forall\alpha\in\mathbb R^n.
$$

(1) 证明: 当 $\left|A\right|\ne0$ 时, $T_{\left(A,\beta\right)}$ 是双射;

(2) 证明: $\mathrm{Aff}\left(n,\mathbb R\right)=\left\{T_{\left(A,\beta\right)}\mid\left|A\right|\ne0\right\}$ 关于映射的复合构成群, 称为 $\mathbb R^n$ 的仿射变换群.

### 解答 1.1-16

**(1) 证明 $T_{\left(A,\beta\right)}$ 是双射.** 设 $\left|A\right|\ne0$. 由**基础知识: 方阵可逆性与行列式**, $A$ 可逆.

**单射**: 若 $T_{\left(A,\beta\right)}\left(\alpha_1\right)=T_{\left(A,\beta\right)}\left(\alpha_2\right)$, 则 $A\alpha_1+\beta=A\alpha_2+\beta$, 故 $A\left(\alpha_1-\alpha_2\right)=0$. 因 $A$ 可逆, 左乘 $A^{-1}$ 得 $\alpha_1-\alpha_2=0$, 即 $\alpha_1=\alpha_2$. 故 $T_{\left(A,\beta\right)}$ 是单射.

**满射**: 对任意 $\gamma\in\mathbb R^n$, 取 $\alpha=A^{-1}\left(\gamma-\beta\right)$, 则由矩阵乘法结合律与逆矩阵定义 (**基础知识: 矩阵乘法结合律**, **基础知识: 方阵可逆性与行列式**), $T_{\left(A,\beta\right)}\left(\alpha\right)=A\left(A^{-1}\left(\gamma-\beta\right)\right)+\beta=\left(\gamma-\beta\right)+\beta=\gamma$. 故 $T_{\left(A,\beta\right)}$ 是满射.

综上, $T_{\left(A,\beta\right)}$ 是双射.

**(2) 证明 $\mathrm{Aff}\left(n,\mathbb R\right)$ 是群.** 由**例 1.1.7 (变换幺半群)**, $M\left(\mathbb R^n\right)$ (所有变换的集合) 在复合下是幺半群, 故复合满足结合律且恒等变换是幺元. 由于每个 $T_{\left(A,\beta\right)}$ 都是 $\mathbb R^n$ 上的变换, $\mathrm{Aff}\left(n,\mathbb R\right)\subseteq M\left(\mathbb R^n\right)$. 下面逐条验证 $\mathrm{Aff}\left(n,\mathbb R\right)$ 关于复合构成群.

**封闭性**: 对任意 $T_{\left(A,\beta\right)},T_{\left(C,\delta\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$ 与任意 $\alpha\in\mathbb R^n$, 由矩阵乘法结合律与分配律 (**基础知识: 矩阵乘法结合律**),

$$
T_{\left(A,\beta\right)}\circ T_{\left(C,\delta\right)}\left(\alpha\right)=A\left(C\alpha+\delta\right)+\beta=\left(AC\right)\alpha+\left(A\delta+\beta\right)=T_{\left(AC,A\delta+\beta\right)}\left(\alpha\right).
$$

由**基础知识: 方阵可逆性与行列式**, $\left|AC\right|=\left|A\right|\left|C\right|\ne0$, 故 $T_{\left(AC,A\delta+\beta\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$. 因此复合在 $\mathrm{Aff}\left(n,\mathbb R\right)$ 上封闭.

**结合律**: 由**例 1.1.7 (变换幺半群)**, 复合满足结合律.

**幺元**: 恒等变换 $T_{\left(I,0\right)}$ 满足 $\left|I\right|=1\ne0$ (**基础知识: 方阵可逆性与行列式**), 故 $T_{\left(I,0\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$. 由**例 1.1.7 (变换幺半群)**, 恒等变换是复合的幺元, 故对任意 $T_{\left(A,\beta\right)}$ 有 $T_{\left(A,\beta\right)}\circ T_{\left(I,0\right)}=T_{\left(A,\beta\right)}=T_{\left(I,0\right)}\circ T_{\left(A,\beta\right)}$.

**逆元**: 对 $T_{\left(A,\beta\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$, 因 $\left|A\right|\ne0$, 由**基础知识: 方阵可逆性与行列式**, $A^{-1}$ 可逆且 $\left|A^{-1}\right|\ne0$, 故 $T_{\left(A^{-1},-A^{-1}\beta\right)}\in\mathrm{Aff}\left(n,\mathbb R\right)$. 对任意 $\alpha\in\mathbb R^n$, 由矩阵乘法结合律与分配律,

$$
T_{\left(A^{-1},-A^{-1}\beta\right)}\circ T_{\left(A,\beta\right)}\left(\alpha\right)=A^{-1}\left(A\alpha+\beta\right)-A^{-1}\beta=\alpha,
$$

且

$$
T_{\left(A,\beta\right)}\circ T_{\left(A^{-1},-A^{-1}\beta\right)}\left(\alpha\right)=A\left(A^{-1}\alpha-A^{-1}\beta\right)+\beta=\alpha,
$$

故 $T_{\left(A^{-1},-A^{-1}\beta\right)}\circ T_{\left(A,\beta\right)}=T_{\left(I,0\right)}=T_{\left(A,\beta\right)}\circ T_{\left(A^{-1},-A^{-1}\beta\right)}$. 依据**定义 1.1.10 (逆元)**, $T_{\left(A^{-1},-A^{-1}\beta\right)}$ 是 $T_{\left(A,\beta\right)}$ 的逆元.

由封闭性,结合律,幺元,逆元全部成立, 依据**定义 1.1.14 (群与阿贝尔群)**, $\mathrm{Aff}\left(n,\mathbb R\right)$ 关于映射的复合构成群. $\blacksquare$

---

## 1.1-20

设 $S$ 是所有数论函数 (即 $\mathbb N^*\to\mathbb C$ 的映射) 的全体. 对 $f,g\in S$, 定义狄利克雷卷积为

$$
f*g\left(n\right)=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)=\sum_{ab=n}f\left(a\right)g\left(b\right).
$$

(1) 证明: $\left(S,*\right)$ 为一个交换幺半群;

(2) 证明: $f$ 可逆当且仅当 $f\left(1\right)\ne0$;

(3) 称 $f$ 为积性函数, 如果 $\left(m,n\right)=1$ 时有 $f\left(mn\right)=f\left(m\right)f\left(n\right)$, 证明: 所有非零积性函数的全体在运算 $*$ 下构成一个阿贝尔群;

(4) 称 $f$ 为完全积性函数, 如果对任意 $m,n\in\mathbb N^*$ 有 $f\left(mn\right)=f\left(m\right)f\left(n\right)$, 所有非零完全积性函数的全体在运算 $*$ 下是否构成一个阿贝尔群?

### 解答 1.1-20

**(1) 证明 $\left(S,*\right)$ 是交换幺半群.** 依据**定义 1.1.4 (半群与幺半群)**, 逐条验证.

**封闭性**: 对任意 $f,g\in S$, 由**基础知识: 数论函数与狄利克雷卷积**, 对每个 $n\in\mathbb N^*$, $\left(f*g\right)\left(n\right)=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)$ 是有限个复数的和, 故为 $\mathbb C$ 中的元素, 即 $f*g$ 是 $\mathbb N^*\to\mathbb C$ 的映射, 故 $f*g\in S$.

**交换性**: 对任意 $f,g\in S$ 与 $n\in\mathbb N^*$, 由**基础知识: 数论函数与狄利克雷卷积**, $\left(f*g\right)\left(n\right)=\sum_{ab=n}f\left(a\right)g\left(b\right)$. 交换求和指标 $a,b$ 得 $\sum_{ab=n}f\left(a\right)g\left(b\right)=\sum_{ba=n}g\left(b\right)f\left(a\right)=\left(g*f\right)\left(n\right)$. 故 $f*g=g*f$, 即 $*$ 满足交换律.

**结合律**: 对任意 $f,g,h\in S$ 与 $n\in\mathbb N^*$, 由**基础知识: 数论函数与狄利克雷卷积**及有限和可重排,

$$
\left(\left(f*g\right)*h\right)\left(n\right)=\sum_{d\mid n}\left(f*g\right)\left(d\right)h\left(\frac{n}{d}\right)=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right),
$$

且

$$
\left(f*\left(g*h\right)\right)\left(n\right)=\sum_{d\mid n}f\left(d\right)\left(g*h\right)\left(\frac{n}{d}\right)=\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right).
$$

两者同为三重和 $\sum_{aby=n}f\left(a\right)g\left(b\right)h\left(y\right)$, 故 $\left(f*g\right)*h=f*\left(g*h\right)$, 即 $*$ 满足结合律.

**幺元**: 由**基础知识: 数论函数与狄利克雷卷积**, $e\left(1\right)=1$ 且 $n>1$ 时 $e\left(n\right)=0$, 故 $e\in S$. 对任意 $f\in S$ 与 $n\in\mathbb N^*$, $\left(e*f\right)\left(n\right)=\sum_{d\mid n}e\left(d\right)f\left(\frac{n}{d}\right)$. 因 $e\left(d\right)=0$ 除非 $d=1$, 故 $\left(e*f\right)\left(n\right)=e\left(1\right)f\left(n\right)=f\left(n\right)$, 即 $e*f=f$; 同理 $f*e=f$. 故 $e$ 是幺元.

由封闭性,交换性,结合律,幺元全部成立, 依据**定义 1.1.4 (半群与幺半群)**, $\left(S,*\right)$ 是交换幺半群.

**(2) 证明 $f$ 可逆当且仅当 $f\left(1\right)\ne0$.**

**必要性**: 若 $f$ 可逆, 由**定义 1.1.10 (逆元)**, 存在 $g\in S$ 使 $f*g=e$. 则 $\left(f*g\right)\left(1\right)=\sum_{d\mid 1}f\left(d\right)g\left(\frac{1}{d}\right)=f\left(1\right)g\left(1\right)$, 而 $e\left(1\right)=1$, 故 $f\left(1\right)g\left(1\right)=1$, 于是 $f\left(1\right)\ne0$.

**充分性**: 设 $f\left(1\right)\ne0$. 由**基础知识: 数论函数与狄利克雷卷积**归纳构造 $g\in S$: 令 $g\left(1\right)=f\left(1\right)^{-1}$; 对 $n>1$, 要求 $\left(f*g\right)\left(n\right)=0$, 即

$$
f\left(1\right)g\left(n\right)+\sum_{\substack{d\mid n\\d>1}}f\left(d\right)g\left(\frac{n}{d}\right)=0,
$$

解得

$$
g\left(n\right)=-f\left(1\right)^{-1}\sum_{\substack{d\mid n\\d>1}}f\left(d\right)g\left(\frac{n}{d}\right).
$$

右端只涉及下标 $\frac{n}{d}<n$ (因 $d>1$) 处已定义的 $g$, 故可递归定义出 $g\in S$, 且使 $\left(f*g\right)\left(1\right)=f\left(1\right)g\left(1\right)=1=e\left(1\right)$, 对 $n>1$ 有 $\left(f*g\right)\left(n\right)=0=e\left(n\right)$, 即 $f*g=e$. 依据**定义 1.1.10 (逆元)**, $f$ 可逆.

**(3) 证明非零积性函数全体 $F$ 在 $*$ 下构成阿贝尔群.**

先证 $F$ 中元素满足 $f\left(1\right)=1$. 对 $f\in F$, 因 $f\ne0$, 存在 $m\in\mathbb N^*$ 使 $f\left(m\right)\ne0$. 因 $\left(1,1\right)=1$, 由积性 (**基础知识: 积性函数与完全积性函数**), $f\left(1\right)=f\left(1\cdot1\right)=f\left(1\right)f\left(1\right)$, 故 $f\left(1\right)=0$ 或 $1$. 若 $f\left(1\right)=0$, 则 $f\left(m\right)=f\left(1\cdot m\right)=f\left(1\right)f\left(m\right)=0$, 与 $f\left(m\right)\ne0$ 矛盾. 故 $f\left(1\right)=1\ne0$.

**封闭性**: 对 $f,g\in F$ 与 $\left(m,n\right)=1$, 由**基础知识: 互素因子的唯一分解**, $d\mid mn$ 唯一地分解为 $d=d_1d_2$, 其中 $d_1\mid m$, $d_2\mid n$, 且 $\left(d_1,d_2\right)=1$, $\left(\frac{m}{d_1},\frac{n}{d_2}\right)=1$. 由 $f,g$ 的积性, $f\left(d_1d_2\right)=f\left(d_1\right)f\left(d_2\right)$, $g\left(\frac{mn}{d_1d_2}\right)=g\left(\frac{m}{d_1}\frac{n}{d_2}\right)=g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right)$. 故

$$
\left(f*g\right)\left(mn\right)=\sum_{d_1\mid m}\sum_{d_2\mid n}f\left(d_1\right)f\left(d_2\right)g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right)=\left(f*g\right)\left(m\right)\left(f*g\right)\left(n\right),
$$

即 $f*g$ 是积性函数. 又 $\left(f*g\right)\left(1\right)=f\left(1\right)g\left(1\right)=1\ne0$, 故 $f*g\ne0$, 于是 $f*g\in F$.

**幺元**: 由**基础知识: 数论函数与狄利克雷卷积**, $e\left(1\right)=1$ 且 $n>1$ 时 $e\left(n\right)=0$. 对 $\left(m,n\right)=1$, 若 $mn=1$ 则 $m=n=1$; 否则 $mn>1$, $e\left(mn\right)=0$, 而 $e\left(m\right)e\left(n\right)=0$ (因 $m,n$ 至少其一 $>1$), 故 $e$ 是积性函数. 又 $e\left(1\right)=1\ne0$, 故 $e\in F$.

**逆元**: 对 $f\in F$, 由 (2) 及 $f\left(1\right)=1\ne0$, $f$ 在 $S$ 中可逆, 设 $f*g=e$. 下面用强归纳证明 $g$ 是积性函数: 对 $\left(m,n\right)=1$, 设对所有 $\left(k,l\right)=1$ 且 $kl<mn$ 已证 $g\left(kl\right)=g\left(k\right)g\left(l\right)$, 证明 $g\left(mn\right)=g\left(m\right)g\left(n\right)$. 因 $mn>1$, $\left(f*g\right)\left(mn\right)=0$, 由**基础知识: 互素因子的唯一分解**与 $f$ 的积性,

$$
0=\left(f*g\right)\left(mn\right)=\sum_{d_1\mid m}\sum_{d_2\mid n}f\left(d_1\right)f\left(d_2\right)g\left(\frac{m}{d_1}\frac{n}{d_2}\right).
$$

在右端和中, 当 $\left(d_1,d_2\right)=\left(1,1\right)$ 时 $\frac{m}{d_1}\frac{n}{d_2}=mn$, 其余项 $\frac{m}{d_1}\frac{n}{d_2}<mn$ 且 $\left(\frac{m}{d_1},\frac{n}{d_2}\right)=1$, 由归纳假设 $g\left(\frac{m}{d_1}\frac{n}{d_2}\right)=g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right)$. 另一方面, 由 $\left(f*g\right)\left(m\right)=0$ 与 $\left(f*g\right)\left(n\right)=0$ 相乘, 得

$$
0=\sum_{d_1\mid m}\sum_{d_2\mid n}f\left(d_1\right)f\left(d_2\right)g\left(\frac{m}{d_1}\right)g\left(\frac{n}{d_2}\right).
$$

两式右端的和除首项外逐项相等, 而 $f\left(1\right)=1$, 故 $g\left(mn\right)=g\left(m\right)g\left(n\right)$. 因此 $g$ 是积性函数. 又由 $f*g=e$, $\left(f*g\right)\left(1\right)=f\left(1\right)g\left(1\right)=1$, 且 $f\left(1\right)=1$, 故 $g\left(1\right)=1\ne0$, 于是 $g\in F$, 即 $f$ 在 $F$ 中有逆元 $g$.

**交换性**: 由 (1), $*$ 满足交换律.

由封闭性,幺元,逆元,交换性全部成立, 依据**定义 1.1.14 (群与阿贝尔群)**, $F$ 在 $*$ 下构成阿贝尔群.

**(4) 结论: 不构成.** 事实上, 非零完全积性函数的全体在 $*$ 下不封闭. 取 $f\left(n\right)=1$ (常数函数), 对任意 $m,n\in\mathbb N^*$ 有 $f\left(mn\right)=1=f\left(m\right)f\left(n\right)$, 故 $f$ 是完全积性的, 且 $f\ne0$. 由**基础知识: 数论函数与狄利克雷卷积**,

$$
\left(f*f\right)\left(n\right)=\sum_{d\mid n}1=\tau\left(n\right),
$$

其中 $\tau\left(n\right)$ 为 $n$ 的正因子个数. 取 $n=2$, 则由**基础知识: 正因子个数函数**, $\tau\left(2\right)=2$, $\tau\left(4\right)=3$. 于是 $\tau\left(2\cdot2\right)=\tau\left(4\right)=3\ne4=\tau\left(2\right)\tau\left(2\right)$, 即 $\tau$ 不是完全积性函数. 故 $f*f=\tau$ 不是完全积性函数, 即 $f*f$ 不属于非零完全积性函数全体. 因此该集合对 $*$ 不封闭, 不构成阿贝尔群. $\blacksquare$
