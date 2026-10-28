# week15

> **基础知识: 整环 $\mathbb Z\left[\sqrt{-5}\right]$ 的范数**<br>对 $x+y\sqrt{-5}\in\mathbb Z\left[\sqrt{-5}\right]$ 定义 $N\left(x+y\sqrt{-5}\right)=x^{2}+5y^{2}$. 则 $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$, 且 $\xi$ 为单位当且仅当 $N\left(\xi\right)=1$; $N$ 取非负整数值, 且不存在范数为 $3$ 的元素 (方程 $x^{2}+5y^{2}=3$ 无整数解).

> **基础知识: 代数整数环 $\mathbb Z\left[\omega\right]$ 的范数**<br>设 $\omega=\frac{1+\sqrt{-3}}{2}$, 则 $\omega^{2}=\omega-1$, $\overline\omega=\frac{1-\sqrt{-3}}{2}$, 且 $\mathbb Z\left[\omega\right]=\left\{m+n\omega\mid m,n\in\mathbb Z\right\}$. 定义 $N\left(m+n\omega\right)=\left(m+n\omega\right)\left(m+n\overline\omega\right)=m^{2}+mn+n^{2}$, 则 $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$, 且 $\xi$ 为单位当且仅当 $N\left(\xi\right)=1$.

> **基础知识: 数域上多项式环是唯一分解整环**<br>数域上的一元及多元多项式环是唯一分解整环; 在 $\mathbb Q\left[x,y\right]$ 中, $x,y$ 是互不相伴的不可约元素 (其单位恰为非零常数).

> **定义 2.5.2 (相伴)**<br>设 $R$ 为整环, $a,b\in R$. 如果存在 $R$ 中单位 $u$ 使得 $a=ub$, 则称 $a$ 与 $b$ 相伴, 记为 $a\sim b$.

> **定义 2.5.6 (不可约元素)**<br>设 $R$ 为整环, $\alpha\in R^{*}\setminus U$ (即非零且非单位). 如果 $\alpha$ 不存在非平凡因子, 则称 $\alpha$ 为不可约元素, 否则称 $\alpha$ 为可约元素.

> **定义 2.5.14 (公因子与最大公因子)**<br>设 $R$ 为整环, $a_1,a_2,\cdots,a_n\in R$. 若 $c\in R$ 同时整除所有 $a_i$, 则称 $c$ 为它们的公因子; 若公因子 $d$ 能被任一公因子整除, 则称 $d$ 为最大公因子. 若 $a,b$ 的最大公因子是单位, 则称 $a,b$ 互素.

---

## 2.5-8

设 $R=\mathbb Z\left[\sqrt{-5}\right]$.

(1) 试证明: 若 $a^{2}+5b^{2}=9$, 则 $a+b\sqrt{-5}$ 是不可约元素;

(2) 试证明: 元素 $\alpha=6+3\sqrt{-5}$, $\beta=9$ 在 $R$ 中不存在最大公因子.

### 解答 2.5-8

在 $R$ 上由**基础知识: 整环 $\mathbb Z\left[\sqrt{-5}\right]$ 的范数** 定义范数 $N\left(x+y\sqrt{-5}\right)=x^{2}+5y^{2}$, 则 $N$ 积性, $\xi$ 为单位当且仅当 $N\left(\xi\right)=1$.

**第 (1) 部分.** 设 $\gamma=a+b\sqrt{-5}$, 则 $N\left(\gamma\right)=a^{2}+5b^{2}=9\ne1$, 故 $\gamma$ 非单位, 即 $\gamma\in R^{*}\setminus U$. 反设 $\gamma=\xi\eta$ 为非平凡分解 (即 $\xi,\eta$ 均非单位), 则

$$
N\left(\xi\right)N\left(\eta\right)=N\left(\gamma\right)=9.
$$

由**基础知识: 整环 $\mathbb Z\left[\sqrt{-5}\right]$ 的范数**, $N$ 取非负整数值, 且不存在范数为 $3$ 的元素. 故 $N\left(\xi\right),N\left(\eta\right)$ 只能取 $1$ 或 $9$: 若 $N\left(\xi\right)=1$ 则 $\xi$ 为单位, 若 $N\left(\xi\right)=9$ 则 $N\left(\eta\right)=1$ 从而 $\eta$ 为单位. 无论何种情形, $\gamma$ 的分解中必有一个因子为单位, 与 $\gamma=\xi\eta$ 为非平凡分解矛盾. 故 $\gamma$ 不存在非平凡因子, 由**定义 2.5.6 (不可约元素)**, $\gamma$ 为不可约元素.

**第 (2) 部分.** 先作分解:

$$
\beta=9=\left(2+\sqrt{-5}\right)\left(2-\sqrt{-5}\right),
$$

$$
\alpha=6+3\sqrt{-5}=3\left(2+\sqrt{-5}\right).
$$

其中 $N\left(3\right)=9$, $N\left(2+\sqrt{-5}\right)=N\left(2-\sqrt{-5}\right)=9$, 由第 (1) 部分, $3$, $2+\sqrt{-5}$, $2-\sqrt{-5}$ 均不可约.

$3$ 同时整除 $\alpha$ 与 $\beta$ ($9=3\cdot3$), $2+\sqrt{-5}$ 也同时整除 $\alpha$ 与 $\beta$, 故二者都是公因子.

**$2-\sqrt{-5}$ 不整除 $\alpha$**: 若存在 $\gamma\in R$ 使 $\gamma\left(2-\sqrt{-5}\right)=\alpha=3\left(2+\sqrt{-5}\right)$, 两端同乘 $2+\sqrt{-5}$ 并由 $\left(2+\sqrt{-5}\right)\left(2-\sqrt{-5}\right)=9$ 得

$$
\gamma\cdot9=3\left(2+\sqrt{-5}\right)^{2}=3\left(-1+4\sqrt{-5}\right),
$$

故 $\gamma=\left(-1+4\sqrt{-5}\right)/3=-\frac{1}{3}+\frac{4}{3}\sqrt{-5}\notin R$, 矛盾.

**$3$ 与 $2+\sqrt{-5}$ 互不整除**: $3\nmid\left(2+\sqrt{-5}\right)$ (否则 $\left(2+\sqrt{-5}\right)/3\notin R$); 且 $\left(2+\sqrt{-5}\right)\nmid3$, 因为否则 $3/\left(2+\sqrt{-5}\right)=\left(2-\sqrt{-5}\right)/3\notin R$.

反设 $d$ 是 $\alpha,\beta$ 的最大公因子. 由**定义 2.5.14 (公因子与最大公因子)**, 每个公因子都整除 $d$, 特别地 $3\mid d$ 且 $\left(2+\sqrt{-5}\right)\mid d$. 又 $d\mid\beta=9$, 而 $9$ 在相伴意义下的因子只有 $1,3,2+\sqrt{-5},2-\sqrt{-5},9$ (由第 (1) 部分, 范数 $9$ 的因子只有 $3,2\pm\sqrt{-5}$, 且无范数 $3$ 的元素). 逐一检查: $d=1$ 不被 $3$ 整除; $d=3$ 不被 $2+\sqrt{-5}$ 整除; $d=2+\sqrt{-5}$ 不被 $3$ 整除; $d=2-\sqrt{-5}$ 不整除 $\alpha$ (如上); $d=9$ 不整除 $\alpha$ (否则 $\alpha/9=\left(2+\sqrt{-5}\right)/3\notin R$). 均与 $3\mid d$, $\left(2+\sqrt{-5}\right)\mid d$, $d\mid\alpha$ 同时成立矛盾.

故 $\alpha,\beta$ 在 $R$ 中不存在最大公因子. $\blacksquare$

---

## 2.5-10

设 $R=\mathbb Z\left[\omega\right]$, 其中 $\omega=\frac{1+\sqrt{-3}}{2}$ (即 $\mathbb Q\left(\sqrt{-3}\right)$ 的代数整数环).

(1) 证明 $R$ 在数的加法和乘法下构成一个整环;

(2) 证明 $R$ 的所有单位是 $\pm1$, $\frac{\pm1\pm\sqrt{-3}}{2}$;

(3) 证明在 $R$ 中 $2$ 与 $1+\sqrt{-3}$ 相伴.

### 解答 2.5-10

由**基础知识: 代数整数环 $\mathbb Z\left[\omega\right]$ 的范数**, $\omega^{2}=\omega-1$, 故

$$
R=\mathbb Z\left[\omega\right]=\left\{m+n\omega\mid m,n\in\mathbb Z\right\}
$$

对乘法封闭 ($\omega^{2}=\omega-1\in R$).

**第 (1) 部分.** $R\subseteq\mathbb C$. $R$ 对加法封闭 (逐分量相加), 对乘法封闭, 含幺元 $1$. 由于 $\mathbb C$ 无零因子, 故 $R$ 是无零因子的交换幺环, 从而是整环.

**第 (2) 部分.** 由**基础知识: 代数整数环 $\mathbb Z\left[\omega\right]$ 的范数**, 定义

$$
N\left(m+n\omega\right)=\left(m+n\omega\right)\left(m+n\overline\omega\right)=m^{2}+mn+n^{2},
$$

则 $N$ 积性, 且 $\xi$ 为单位当且仅当 $N\left(\xi\right)=1$. 解

$$
m^{2}+mn+n^{2}=1,\quad m,n\in\mathbb Z,
$$

得

$$
\left(m,n\right)=\left(\pm1,0\right),\;\left(0,\pm1\right),\;\left(1,-1\right),\;\left(-1,1\right).
$$

对应元素为 $\pm1$, $\pm\omega$, $\pm\left(1-\omega\right)$. 因 $\omega=\frac{1+\sqrt{-3}}{2}$, $1-\omega=\frac{1-\sqrt{-3}}{2}$, 故 $R$ 的全部单位为 $\pm1$ 及 $\frac{\pm1\pm\sqrt{-3}}{2}$.

**第 (3) 部分.** 因 $1+\sqrt{-3}=2\omega$, 而 $\omega$ 是单位 ($N\left(\omega\right)=1$), 即 $1+\sqrt{-3}=2\cdot\omega$ 且 $\omega$ 为单位, 由**定义 2.5.2 (相伴)**, $2$ 与 $1+\sqrt{-3}$ 相伴. $\blacksquare$

---

## 2.5-15

已知 $\mathbb Q\left[x,y\right]$ 在多项式加法和乘法下构成环, 证明: $x$ 与 $y$ 互素. 试问是否存在 $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ 使得 $r\left(x,y\right)x+s\left(x,y\right)y=1$?

### 解答 2.5-15

由**基础知识: 数域上多项式环是唯一分解整环**, $\mathbb Q\left[x,y\right]$ 是唯一分解整环, 且 $x,y$ 都是不可约元素. $x,y$ 不相伴: 其单位恰为 $\mathbb Q^{*}$ 中的非零常数, 而 $x\ne cy$ 对任何 $c\in\mathbb Q^{*}$. 故 $x,y$ 的公共因子只能是单位, 即最大公因子为单位, 由**定义 2.5.14 (公因子与最大公因子)**, $x$ 与 $y$ 互素.

但不存在这样的 $r,s$. 反设存在 $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ 使 $r\left(x,y\right)x+s\left(x,y\right)y=1$. 将等式两边在 $\left(0,0\right)$ 处取值:

$$
r\left(0,0\right)\cdot0+s\left(0,0\right)\cdot0=1,
$$

即 $0=1$, 矛盾.

故虽然 $x,y$ 互素, 却不存在 $r,s\in\mathbb Q\left[x,y\right]$ 使 $rx+sy=1$. $\blacksquare$
