# 作业 24

> **定义 4.1.15**（扩张次数）设 $E$ 为 $F$ 的扩张, $E$ 作为 $F$-线性空间的维数称为 $E$ 对 $F$ 的扩张次数, 记为 $\left[E:F\right]$. 若 $\left[E:F\right]<\infty$, 称 $E$ 为 $F$ 的有限扩张; 否则称 $E$ 为 $F$ 的无限扩张.

> **定理 4.1.16**（扩张次数的望远镜法则）若 $K/F$ 与 $E/K$ 都是有限扩张, 则 $E/F$ 也是有限扩张, 且 $\left[E:F\right]=\left[E:K\right]\left[K:F\right]$.

> **引理 4.2.1**（有限扩张必为代数扩张）设 $E/F$ 为有限扩张, 则 $E$ 中每个元素都是 $F$ 上的代数元. 换言之, 若 $E$ 中存在 $F$ 上的超越元, 则 $E/F$ 必为无限扩张.

> **引理 4.1.9**（域同态必单射）域同态 $\varphi:F\to E$ 一定是单射. 特别地, 域自同构保持域中运算及 $1$, 因而保持素域（$\mathbb Q$ 或 $\mathbb F_p$）上的所有元素不动.

> **基础知识**（分式域的泛性质）设 $R$ 为整环, $E$ 为其分式域. 任给 $R$ 的自同构 $\sigma$, 定义映射 $\bar\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\sigma\left(b\right)^{-1}$, 则 $\bar\sigma$ 良定义且为 $E$ 的自同构.

### 习题一

（习题 4.1-4）求下列域扩张的次数:
（1）$\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\right]$;
（2）$\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]$.

### 解答 习题一

记 $\alpha=\sqrt2+\sqrt3$. 先证明 $\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$.

一方面, $\alpha\in\mathbb Q\left(\sqrt2,\sqrt3\right)$, 故 $\mathbb Q\left(\alpha\right)\subseteq\mathbb Q\left(\sqrt2,\sqrt3\right)$.

另一方面, 因 $\left(\sqrt2+\sqrt3\right)\left(\sqrt3-\sqrt2\right)=3-2=1$, 故 $\alpha^{-1}=\sqrt3-\sqrt2$. 于是

$$
\begin{aligned}&\quad\;\sqrt2\\&=\frac{\alpha-\alpha^{-1}}{2}\in\mathbb Q\left(\alpha\right),\end{aligned}
$$

同理 $\sqrt3=\dfrac{\alpha+\alpha^{-1}}{2}\in\mathbb Q\left(\alpha\right)$, 故 $\mathbb Q\left(\sqrt2,\sqrt3\right)\subseteq\mathbb Q\left(\alpha\right)$. 因而 $\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$.

再证 $\sqrt2\notin\mathbb Q\left(\sqrt3\right)$. 反设 $\sqrt2=a+b\sqrt3$, $a,b\in\mathbb Q$. 两边平方得 $2=a^2+3b^2+2ab\sqrt3$. 因 $1,\sqrt3$ 在 $\mathbb Q$ 上线性无关, 故 $ab=0$. 若 $b=0$, 则 $2=a^2$, 无有理解; 若 $a=0$, 则 $2=3b^2$, 即 $b^2=2/3$, 亦无有理解. 故 $\sqrt2\notin\mathbb Q\left(\sqrt3\right)$.

于是 $\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]=2$. 又 $\left[\mathbb Q\left(\sqrt3\right):\mathbb Q\right]=2$（因 $x^2-3$ 不可约）. 由**定理 4.1.16**（扩张次数的望远镜法则）,

$$
\begin{aligned}&\quad\;\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\right]\\&=\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]\left[\mathbb Q\left(\sqrt3\right):\mathbb Q\right]\\&=2\times2\\&=4.\end{aligned}
$$

（1）因 $\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$, 故 $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\right]=4$.

（2）同理 $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]=2$. $\blacksquare$

### 习题二

（习题 4.1-10）证明: $\mathbb R/\mathbb Q$ 是无限扩张.

### 解答 习题二

数 $\pi\in\mathbb R$ 是 $\mathbb Q$ 上的超越元（林德曼定理）, 即 $\pi$ 不是任何非零有理系数多项式的根.

若 $\mathbb R/\mathbb Q$ 为有限扩张, 由**引理 4.2.1**（有限扩张必为代数扩张）, $\mathbb R$ 中每个元素都是 $\mathbb Q$ 上的代数元, 特别地 $\pi$ 应为 $\mathbb Q$ 上的代数元, 矛盾.

故 $\mathbb R/\mathbb Q$ 不是有限扩张, 即 $\mathbb R/\mathbb Q$ 是无限扩张. $\blacksquare$

### 习题三

（习题 4.1-11）设 $E$ 是整环 $R$ 的分式域. 对任意 $R$ 的自同构 $\sigma$ 定义 $\bar\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\left(\sigma\left(b\right)\right)^{-1}$. 证明: $\bar\sigma$ 是 $E$ 的自同构.

### 解答 习题三

依**基础知识**（分式域的泛性质）, 分三步验证.

**良定义** 设 $ab^{-1}=cd^{-1}$, $a,b,c,d\in R$, $b,d\ne0$. 则 $ad=bc$. 由 $\sigma$ 为环同态,

$$
\begin{aligned}&\quad\;\sigma\left(a\right)\sigma\left(d\right)\\&=\sigma\left(ad\right)\\&=\sigma\left(bc\right)\\&=\sigma\left(b\right)\sigma\left(c\right),\end{aligned}
$$

故 $\sigma\left(a\right)\sigma\left(b\right)^{-1}=\sigma\left(c\right)\sigma\left(d\right)^{-1}$, 即 $\bar\sigma\left(ab^{-1}\right)=\bar\sigma\left(cd^{-1}\right)$. 定义与代表元选取无关.

**环同态** 对 $x=ab^{-1}$, $y=cd^{-1}\in E$, 有

$$
\begin{aligned}&\quad\;\bar\sigma\left(xy\right)\\&=\bar\sigma\left(ac\left(bd\right)^{-1}\right)\\&=\sigma\left(ac\right)\sigma\left(bd\right)^{-1}\\&=\sigma\left(a\right)\sigma\left(c\right)\sigma\left(b\right)^{-1}\sigma\left(d\right)^{-1}\\&=\bar\sigma\left(x\right)\bar\sigma\left(y\right),\end{aligned}
$$

且

$$
\begin{aligned}&\quad\;\bar\sigma\left(x+y\right)\\&=\bar\sigma\left(\left(ad+bc\right)\left(bd\right)^{-1}\right)\\&=\sigma\left(ad+bc\right)\sigma\left(bd\right)^{-1}\\&=\frac{\sigma\left(a\right)}{\sigma\left(b\right)}+\frac{\sigma\left(c\right)}{\sigma\left(d\right)}\\&=\bar\sigma\left(x\right)+\bar\sigma\left(y\right).\end{aligned}
$$

又 $\bar\sigma\left(1\right)=\sigma\left(1\right)\sigma\left(1\right)^{-1}=1$, 故 $\bar\sigma$ 为环同态.

**双射** 因 $\sigma$ 是 $R$ 的自同构, 其逆 $\tau=\sigma^{-1}$ 亦为 $R$ 的自同构. 直接验证可知 $\bar\tau$ 为 $\bar\sigma$ 的逆映射: 对 $x=ab^{-1}\in E$,

$$
\begin{aligned}&\quad\;\bar\tau\circ\bar\sigma\left(x\right)\\&=\bar\tau\left(\sigma\left(a\right)\sigma\left(b\right)^{-1}\right)\\&=\tau\left(\sigma\left(a\right)\right)\tau\left(\sigma\left(b\right)\right)^{-1}\\&=ab^{-1}\\&=x.\end{aligned}
$$

同理 $\bar\sigma\circ\bar\tau=\mathrm{id}$. 故 $\bar\sigma$ 可逆, 为 $E$ 的自同构. $\blacksquare$

### 习题四

（习题 4.1-13）证明: $\mathrm{Aut}\left(\mathbb R\right)$ 是平凡群.

### 解答 习题四

设 $\sigma\in\mathrm{Aut}\left(\mathbb R\right)$. 由**引理 4.1.9**（域同态必单射）, $\sigma$ 为域自同构, 保持乘法单位元, 故 $\sigma\left(1\right)=1$. 于是对任意 $n\in\mathbb Z$, $\sigma\left(n\right)=n$; 对任意 $m/n\in\mathbb Q$, $\sigma\left(m/n\right)=m/n$, 即 $\sigma$ 保持 $\mathbb Q$ 中每个元素不动.

下证 $\sigma$ 保持序. 设 $x>0$, 则存在 $y\in\mathbb R$, $y\ne0$, 使 $x=y^2$. 于是

$$
\begin{aligned}&\quad\;\sigma\left(x\right)\\&=\sigma\left(y^2\right)\\&=\sigma\left(y\right)^2>0,\end{aligned}
$$

其中 $\sigma\left(y\right)\ne0$（因 $\sigma$ 单射且 $y\ne0$）. 故 $\sigma$ 把正数映为正数, 从而当 $a<b$ 即 $b-a>0$ 时 $\sigma\left(b\right)-\sigma\left(a\right)=\sigma\left(b-a\right)>0$, 即 $\sigma\left(a\right)<\sigma\left(b\right)$. 因而 $\sigma$ 是保序映射.

反设 $\sigma\ne\mathrm{id}$, 则存在 $x\in\mathbb R$ 使 $\sigma\left(x\right)\ne x$.

若 $\sigma\left(x\right)>x$, 由 $\mathbb Q$ 在 $\mathbb R$ 中稠密, 可取 $q\in\mathbb Q$ 使 $x<q<\sigma\left(x\right)$. 因 $\sigma$ 保序, 由 $x<q$ 得 $\sigma\left(x\right)<\sigma\left(q\right)=q$, 与 $q<\sigma\left(x\right)$ 矛盾.

若 $\sigma\left(x\right)<x$, 同理取 $q\in\mathbb Q$ 使 $\sigma\left(x\right)<q<x$. 由 $q<x$ 得 $q=\sigma\left(q\right)<\sigma\left(x\right)$, 与 $\sigma\left(x\right)<q$ 矛盾.

故 $\sigma\left(x\right)=x$ 对所有 $x\in\mathbb R$ 成立, 即 $\sigma=\mathrm{id}$. 因而 $\mathrm{Aut}\left(\mathbb R\right)$ 只含恒等元, 是平凡群. $\blacksquare$
