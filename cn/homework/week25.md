# 作业 25

> **定理 4.2.13**（单代数扩张的结构）域 $F$ 的单代数扩张 $F\left(\alpha\right)$ 必同构于 $F\left[x\right]/\left(\mathrm{Irr}\left(\alpha,F\right)\right)$. 设 $\deg\left(\alpha,F\right)=n$, 则 $F\left(\alpha\right)$ 作为 $F$-线性空间的维数为 $n$, 且 $1,\alpha,\alpha^2,\cdots,\alpha^{n-1}$ 为其一组 $F$-基.

> **基础知识**（艾森斯坦判别法）设
> $$
> f\left(x\right)=a_nx^n+\cdots+a_0\in\mathbb Z\left[x\right],
> $$
> 若存在素数 $p$ 使得 $p\nmid a_n$, $p\mid a_i$ 对 $i=0,1,\cdots,n-1$, 但 $p^2\nmid a_0$, 则 $f\left(x\right)$ 在 $\mathbb Q\left[x\right]$ 上不可约.

> **基础知识**（特征 $p$ 下的弗罗贝尼乌斯映射）设域 $F$ 的特征为素数 $p$, 则对任意 $a,b\in F$ 有 $\left(a+b\right)^p=a^p+b^p$, 从而 $\left(x-a\right)^p=x^p-a^p$. 特别地, $x^p-c$ 在其分裂域中只有一个 $p$ 重根.

### 习题一

（习题 4.2-5）设 $F\left(\alpha\right)$ 是 $F$ 的单代数扩张, $\deg\left(\alpha,F\right)=n$, 证明: $F\left(\alpha\right)$ 是 $n$ 维 $F$-线性空间, 且 $1,\alpha,\cdots,\alpha^{n-1}$ 是 $F\left(\alpha\right)$ 的一组基.

### 解答 习题一

由**定理 4.2.13**（单代数扩张的结构）,

$$
F\left(\alpha\right)\cong F\left[x\right]/\left(\mathrm{Irr}\left(\alpha,F\right)\right).
$$

设 $f\left(x\right)=\mathrm{Irr}\left(\alpha,F\right)$ 为首一 $n$ 次不可约多项式.

商环 $F\left[x\right]/\left(f\left(x\right)\right)$ 中任一元素可唯一写为

$$
a_0+a_1x+\cdots+a_{n-1}x^{n-1}
$$
的形式(由带余除法, 余式次数小于 $n$). 在同构下, $x$ 对应于 $\alpha$, 故 $F\left(\alpha\right)$ 中任一元素可唯一表为

$$
a_0+a_1\alpha+\cdots+a_{n-1}\alpha^{n-1},
$$

$a_i\in F$.

因而 $1,\alpha,\cdots,\alpha^{n-1}$ 生成 $F\left(\alpha\right)$, 且在 $F$ 上线性无关(若 $\sum_{i=0}^{n-1}a_i\alpha^i=0$, 则 $\sum a_ix^i$ 是以 $\alpha$ 为根的次数小于 $n$ 的多项式, 与 $f$ 为最小多项式矛盾). 故它们构成 $F\left(\alpha\right)$ 的一组 $F$-基, 且 $\dim_F F\left(\alpha\right)=n$. $\blacksquare$

### 习题二

（习题 4.2-6）试证明对任何正整数 $n$, 存在 $\mathbb Q$ 的代数扩张 $K$ 使得 $\left[K:\mathbb Q\right]=n$.

### 解答 习题二

取 $K=\mathbb Q\left(2^{1/n}\right)$, 即由多项式 $x^n-2$ 的一个根 $\theta=2^{1/n}$ 生成的扩张.

对 $f\left(x\right)=x^n-2\in\mathbb Z\left[x\right]$, 取素数 $p=2$. 由**基础知识**（艾森斯坦判别法）, $2\nmid1$(首项系数), $2\mid0$(中间各项系数均为 $0$), 且 $2^2=4\nmid-2$(常数项), 故 $f\left(x\right)$ 在 $\mathbb Q\left[x\right]$ 上不可约.

因而 $\deg\left(\theta,\mathbb Q\right)=n$. 由**定理 4.2.13**（单代数扩张的结构）, $\left[K:\mathbb Q\right]=\left[\mathbb Q\left(\theta\right):\mathbb Q\right]=n$. 又 $K/\mathbb Q$ 为单代数扩张, 故为代数扩张. $\blacksquare$

### 习题三

（习题 4.2-9）若 $a,b\in\mathbb Q$ 满足 $\sqrt a+\sqrt b\ne0$, 证明:

$$
\mathbb Q\left(\sqrt a,\sqrt b\right)=\mathbb Q\left(\sqrt a+\sqrt b\right).
$$

### 解答 习题三

记 $\alpha=\sqrt a+\sqrt b$. 因 $\alpha\in\mathbb Q\left(\sqrt a,\sqrt b\right)$, 故 $\mathbb Q\left(\alpha\right)\subseteq\mathbb Q\left(\sqrt a,\sqrt b\right)$, 只需证反向包含.

由题设 $\alpha\ne0$, 计算得

$$
\alpha^2=a+b+2\sqrt{ab},
$$

故 $\sqrt{ab}=\frac{\alpha^2-a-b}{2}\in\mathbb Q\left(\alpha\right)$. 又

$$
\sqrt a-\sqrt b=\frac{\left(\sqrt a-\sqrt b\right)\left(\sqrt a+\sqrt b\right)}{\sqrt a+\sqrt b}=\frac{a-b}{\alpha}\in\mathbb Q\left(\alpha\right).
$$

于是

$$
\sqrt a=\frac{1}{2}\left(\alpha+\frac{a-b}{\alpha}\right)\in\mathbb Q\left(\alpha\right),
$$

$$
\sqrt b=\frac{1}{2}\left(\alpha-\frac{a-b}{\alpha}\right)\in\mathbb Q\left(\alpha\right).
$$

因而 $\mathbb Q\left(\sqrt a,\sqrt b\right)\subseteq\mathbb Q\left(\alpha\right)$. 结合反向包含, 得

$$
\mathbb Q\left(\sqrt a,\sqrt b\right)=\mathbb Q\left(\sqrt a+\sqrt b\right).
$$

$\blacksquare$

### 习题四

（习题 4.2-10）设 $E=\mathbb F_p\left(t\right)$ 为 $\mathbb F_p$ 的单超越扩张.

(1)证明: $x^p-t\in E\left[x\right]$ 不可约;

(2)设 $\theta$ 是 $x^p-t$ 的一个根, 试将 $x^p-t$ 在 $E\left(\theta\right)$ 上分解为不可约多项式之积.

### 解答 习题四

(1)反设 $x^p-t$ 在 $E\left[x\right]$ 中非平凡分解, $x^p-t=f\left(x\right)g\left(x\right)$, 其中 $f,g$ 首一, $1\leq\deg f=k< p$.

设 $\theta$ 为 $x^p-t$ 在某分裂域中的根, 则 $\theta^p=t$. 由**基础知识**（特征 $p$ 下的弗罗贝尼乌斯映射）,

$$
\left(x-\theta\right)^p=x^p-\theta^p=x^p-t.
$$

故在分裂域中 $x^p-t=\left(x-\theta\right)^p$, 从而 $f\left(x\right)=\left(x-\theta\right)^k$.

$f\left(x\right)$ 中 $x^{k-1}$ 的系数为 $-k\theta$. 因 $f\in E\left[x\right]$, 该系数属于 $E$, 故 $k\theta\in E$. 又 $1\leq k< p$, 在特征 $p$ 域中 $k\ne0$, 故 $k$ 可逆, 从而 $\theta\in E$.

但 $\theta\in E=\mathbb F_p\left(t\right)$ 意味着存在互素多项式 $f_0\left(t\right),g_0\left(t\right)\in\mathbb F_p\left[t\right]$ 使 $\theta=f_0\left(t\right)/g_0\left(t\right)$. 由 $\theta^p=t$ 得 $f_0\left(t\right)^p=t\,g_0\left(t\right)^p$. 比较两边次数: 左端次数为 $p\deg f_0$, 右端次数为 $1+p\deg g_0$. 左端被 $p$ 整除, 右端模 $p$ 余 $1$, 矛盾. 故 $\theta\notin E$, 从而 $x^p-t$ 在 $E\left[x\right]$ 中不可约.

(2)在 $E\left(\theta\right)$ 中, 由**基础知识**（特征 $p$ 下的弗罗贝尼乌斯映射）,

$$
x^p-t=x^p-\theta^p=\left(x-\theta\right)^p.
$$

其中 $x-\theta$ 已是一次多项式, 自然不可约. 故 $x^p-t$ 在 $E\left(\theta\right)$ 上的不可约分解为 $\left(x-\theta\right)^p$. $\blacksquare$

### 习题五

（习题 4.2-13）设 $F\left(\alpha\right)$ 为 $F$ 的单超越扩张, $u\in F\left(\alpha\right)$, $u\notin F$, 证明 $\alpha$ 是域 $F\left(u\right)$ 上的代数元.

### 解答 习题五

因 $u\in F\left(\alpha\right)$, 且 $F\left(\alpha\right)$ 是 $F\left[\alpha\right]$ 的分式域, 故存在互素多项式 $f\left(x\right),g\left(x\right)\in F\left[x\right]$, $g\left(x\right)\ne0$, 使得

$$
u=\frac{f\left(\alpha\right)}{g\left(\alpha\right)}.
$$

考虑多项式

$$
h\left(x\right)=u\,g\left(x\right)-f\left(x\right)\in F\left(u\right)\left[x\right].
$$

将 $x=\alpha$ 代入, 得

$$
h\left(\alpha\right)=u\,g\left(\alpha\right)-f\left(\alpha\right)=0.
$$

下证 $h\left(x\right)\ne0$. 反设 $h\left(x\right)=0$, 则在 $F\left(u\right)\left[x\right]$ 中有 $u\,g\left(x\right)=f\left(x\right)$.

若 $g\left(x\right)$ 为常数多项式, 则 $f\left(x\right)$ 必非常数(否则 $u=f/g\in F$, 矛盾), 此时 $\deg\left(u\,g\right)=0$ 而 $\deg f> 0$, 与 $ug=f$ 矛盾.

若 $g\left(x\right)$ 非常数, 则 $\deg\left(ug\right)=\deg g$($u$ 为 $F\left(u\right)$ 中非零元, 不改变多项式次数). 由 $ug=f$ 得 $\deg f=\deg g$, 比较首项系数得 $u\cdot\mathrm{lc}\left(g\right)=\mathrm{lc}\left(f\right)$, 即 $u=\mathrm{lc}\left(f\right)/\mathrm{lc}\left(g\right)\in F$, 与 $u\notin F$ 矛盾.

故 $h\left(x\right)\ne0$, 而 $h\left(\alpha\right)=0$, 即 $\alpha$ 是 $F\left(u\right)$ 上非零多项式 $h$ 的根, 因而 $\alpha$ 是 $F\left(u\right)$ 上的代数元. $\blacksquare$
