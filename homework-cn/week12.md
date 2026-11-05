# week12

> **引理 4.1.9 (域同态必单射)**
> 
> 域同态 $\varphi:F\to{E}$ 一定是单射. 特别地, 域自同构保持域中运算及 $1$, 因而保持素域 ($\mathbb{Q}$ 或 $\mathbb{F}_p$) 上的所有元素不动.

> **定义 4.1.15 (扩张次数)**
> 
> 设 $E$ 为 $F$ 的扩张, $E$ 作为 $F$-线性空间的维数称为 $E$ 对 $F$ 的扩张次数, 记为 $\left[E:F\right]$. 若 $\left[E:F\right]<\infty$, 称 $E$ 为 $F$ 的有限扩张; 否则称 $E$ 为 $F$ 的无限扩张.

> **定理 4.1.16 (扩张次数的望远镜法则)**
> 
> 若 $K/F$ 与 $E/K$ 都是有限扩张, 则 $E/F$ 也是有限扩张, 且 $\left[E:F\right]=\left[E:K\right]\left[K:F\right]$.

> **引理 4.2.1 (有限扩张必为代数扩张)**
> 
> 设 $E/F$ 为有限扩张, 则 $E$ 中每个元素都是 $F$ 上的代数元. 换言之, 若 $E$ 中存在 $F$ 上的超越元, 则 $E/F$ 必为无限扩张.

> **定理 4.2.13 (单代数扩张的结构)**
> 
> 域 $F$ 的单代数扩张 $F\left(\alpha\right)$ 必同构于 $F\left[x\right]/\left(\mathrm{Irr}\left(\alpha,F\right)\right)$. 设 $\deg\left(\alpha,F\right)=n$, 则 $F\left(\alpha\right)$ 作为 $F$-线性空间的维数为 $n$, 且 $1,\alpha,\alpha^2,\cdots,\alpha^{n-1}$ 为其一组 $F$-基.

## 4.1-4

求下列域扩张的次数:

(1) $\left[\mathbb{Q}\left(\sqrt2+\sqrt3\right):\mathbb{Q}\right]$;

(2) $\left[\mathbb{Q}\left(\sqrt2+\sqrt3\right):\mathbb{Q}\left(\sqrt3\right)\right]$.

### 解答 4.1-4

记 $\alpha=\sqrt2+\sqrt3$. 先证明 $\mathbb{Q}\left(\alpha\right)=\mathbb{Q}\left(\sqrt2,\sqrt3\right)$.

一方面, $\alpha\in\mathbb{Q}\left(\sqrt2,\sqrt3\right)$, 故 $\mathbb{Q}\left(\alpha\right)\subseteq\mathbb{Q}\left(\sqrt2,\sqrt3\right)$.

另一方面, 因 $\left(\sqrt2+\sqrt3\right)\left(\sqrt3-\sqrt2\right)=3-2=1$, 故 $\alpha^{-1}=\sqrt3-\sqrt2$. 于是 $\sqrt2=\frac{\alpha-\alpha^{-1}}{2}\in\mathbb{Q}\left(\alpha\right)$, 同理 $\sqrt3=\frac{\alpha+\alpha^{-1}}{2}\in\mathbb{Q}\left(\alpha\right)$, 故 $\mathbb{Q}\left(\sqrt2,\sqrt3\right)\subseteq\mathbb{Q}\left(\alpha\right)$. 因而 $\mathbb{Q}\left(\alpha\right)=\mathbb{Q}\left(\sqrt2,\sqrt3\right)$.

再证 $\sqrt2\notin\mathbb{Q}\left(\sqrt3\right)$. 反设 $\sqrt2=a+b\sqrt3$, $a,b\in\mathbb{Q}$. 两边平方得 $2=a^2+3b^2+2ab\sqrt3$. 因 $1,\sqrt3$ 在 $\mathbb{Q}$ 上线性无关, 故 $ab=0$. 若 $b=0$, 则 $2=a^2$, 无有理解; 若 $a=0$, 则 $2=3b^2$, 即 $b^2=2/3$, 亦无有理解. 故 $\sqrt2\notin\mathbb{Q}\left(\sqrt3\right)$.

于是 $\left[\mathbb{Q}\left(\sqrt2,\sqrt3\right):\mathbb{Q}\left(\sqrt3\right)\right]=2$. 又 $\left[\mathbb{Q}\left(\sqrt3\right):\mathbb{Q}\right]=2$ (因 $x^2-3$ 不可约). 由**定理 4.1.16 (扩张次数的望远镜法则)**,

$$
\left[\mathbb{Q}\left(\sqrt2,\sqrt3\right):\mathbb{Q}\right]=\left[\mathbb{Q}\left(\sqrt2,\sqrt3\right):\mathbb{Q}\left(\sqrt3\right)\right]\left[\mathbb{Q}\left(\sqrt3\right):\mathbb{Q}\right]=2\times2=4.
$$

(1) 因 $\mathbb{Q}\left(\alpha\right)=\mathbb{Q}\left(\sqrt2,\sqrt3\right)$, 故 $\left[\mathbb{Q}\left(\sqrt2+\sqrt3\right):\mathbb{Q}\right]=4$.

(2) 同理 $\left[\mathbb{Q}\left(\sqrt2+\sqrt3\right):\mathbb{Q}\left(\sqrt3\right)\right]=2$. $\blacksquare$

## 4.1-10

证明: $\mathbb{R}/\mathbb{Q}$ 是无限扩张.

### 解答 4.1-10

数 $\pi\in\mathbb{R}$ 是 $\mathbb{Q}$ 上的超越元 (林德曼定理), 即 $\pi$ 不是任何非零有理系数多项式的根.

若 $\mathbb{R}/\mathbb{Q}$ 为有限扩张, 由**引理 4.2.1 (有限扩张必为代数扩张)**, $\mathbb{R}$ 中每个元素都是 $\mathbb{Q}$ 上的代数元, 特别地 $\pi$ 应为 $\mathbb{Q}$ 上的代数元, 矛盾.

故 $\mathbb{R}/\mathbb{Q}$ 不是有限扩张, 即 $\mathbb{R}/\mathbb{Q}$ 是无限扩张. $\blacksquare$

## 4.1-11

设 $E$ 是整环 $R$ 的分式域. 对任意 $R$ 的自同构 $\sigma$ 定义 $\overline\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\left(\sigma\left(b\right)\right)^{-1}$. 证明: $\overline\sigma$ 是 $E$ 的自同构.

### 解答 4.1-11

依分式域的泛性质, 分三步验证.

良定义. 设 $ab^{-1}=cd^{-1}$, $a,b,c,d\in{R}$, $b,d\ne0$. 则 $ad=bc$. 由 $\sigma$ 为环同态, $\sigma\left(a\right)\sigma\left(d\right)=\sigma\left(ad\right)=\sigma\left(bc\right)=\sigma\left(b\right)\sigma\left(c\right)$, 故 $\sigma\left(a\right)\sigma\left(b\right)^{-1}=\sigma\left(c\right)\sigma\left(d\right)^{-1}$, 即 $\overline\sigma\left(ab^{-1}\right)=\overline\sigma\left(cd^{-1}\right)$. 定义与代表元选取无关.

环同态. 对 $x=ab^{-1}$, $y=cd^{-1}\in{E}$, 有

$$
\overline\sigma\left(xy\right)=\overline\sigma\left(ac\left(bd\right)^{-1}\right)=\sigma\left(ac\right)\sigma\left(bd\right)^{-1}=\sigma\left(a\right)\sigma\left(c\right)\sigma\left(b\right)^{-1}\sigma\left(d\right)^{-1}=\overline\sigma\left(x\right)\overline\sigma\left(y\right),
$$

且

$$
\overline\sigma\left(x+y\right)=\overline\sigma\left(\left(ad+bc\right)\left(bd\right)^{-1}\right)=\sigma\left(ad+bc\right)\sigma\left(bd\right)^{-1}=\frac{\sigma\left(a\right)}{\sigma\left(b\right)}+\frac{\sigma\left(c\right)}{\sigma\left(d\right)}=\overline\sigma\left(x\right)+\overline\sigma\left(y\right).
$$

又 $\overline\sigma\left(1\right)=\sigma\left(1\right)\sigma\left(1\right)^{-1}=1$, 故 $\overline\sigma$ 为环同态.

双射. 因 $\sigma$ 是 $R$ 的自同构, 其逆 $\tau=\sigma^{-1}$ 亦为 $R$ 的自同构. 直接验证可知 $\overline\tau$ 为 $\overline\sigma$ 的逆映射: 对 $x=ab^{-1}\in{E}$,

$$
\overline\tau\circ\overline\sigma\left(x\right)=\overline\tau\left(\sigma\left(a\right)\sigma\left(b\right)^{-1}\right)=\tau\left(\sigma\left(a\right)\right)\tau\left(\sigma\left(b\right)\right)^{-1}=ab^{-1}=x.
$$

同理 $\overline\sigma\circ\overline\tau=\mathrm{id}$. 故 $\overline\sigma$ 可逆, 为 $E$ 的自同构. $\blacksquare$

## 4.1-13

证明: $\mathrm{Aut}\left(\mathbb{R}\right)$ 是平凡群.

### 解答 4.1-13

设 $\sigma\in\mathrm{Aut}\left(\mathbb{R}\right)$. 由**引理 4.1.9 (域同态必单射)**, $\sigma$ 为域自同构, 保持乘法单位元, 故 $\sigma\left(1\right)=1$. 于是对任意 $n\in\mathbb{Z}$, $\sigma\left(n\right)=n$; 对任意 $m/n\in\mathbb{Q}$, $\sigma\left(m/n\right)=m/n$, 即 $\sigma$ 保持 $\mathbb{Q}$ 中每个元素不动.

下证 $\sigma$ 保持序. 设 $x>0$, 则存在 $y\in\mathbb{R}$, $y\ne0$, 使 $x=y^2$. 于是 $\sigma\left(x\right)=\sigma\left(y^2\right)=\sigma\left(y\right)^2>0$, 其中 $\sigma\left(y\right)\ne0$ (因 $\sigma$ 单射且 $y\ne0$). 故 $\sigma$ 把正数映为正数, 从而当 $a<{}b$ 即 $b-a>0$ 时 $\sigma\left(b\right)-\sigma\left(a\right)=\sigma\left(b-a\right)>0$, 即 $\sigma\left(a\right)<\sigma\left(b\right)$. 因而 $\sigma$ 是保序映射.

反设 $\sigma\ne\mathrm{id}$, 则存在 $x\in\mathbb{R}$ 使 $\sigma\left(x\right)\ne{x}$.

若 $\sigma\left(x\right)>{}x$, 由 $\mathbb{Q}$ 在 $\mathbb{R}$ 中稠密, 可取 $q\in\mathbb{Q}$ 使 $x<{}q<\sigma\left(x\right)$. 因 $\sigma$ 保序, 由 $x<{}q$ 得 $\sigma\left(x\right)<\sigma\left(q\right)=q$, 与 $q<\sigma\left(x\right)$ 矛盾.

若 $\sigma\left(x\right)<{}x$, 同理取 $q\in\mathbb{Q}$ 使 $\sigma\left(x\right)<{}q<{}x$. 由 $q<{}x$ 得 $q=\sigma\left(q\right)<\sigma\left(x\right)$, 与 $\sigma\left(x\right)<{}q$ 矛盾.

故 $\sigma\left(x\right)=x$ 对所有 $x\in\mathbb{R}$ 成立, 即 $\sigma=\mathrm{id}$. 因而 $\mathrm{Aut}\left(\mathbb{R}\right)$ 只含恒等元, 是平凡群. $\blacksquare$

## 4.2-5

设 $F\left(\alpha\right)$ 是 $F$ 的单代数扩张, $\deg\left(\alpha,F\right)=n$, 证明: $F\left(\alpha\right)$ 是 $n$ 维 $F$-线性空间, 且 $1,\alpha,\cdots,\alpha^{n-1}$ 是 $F\left(\alpha\right)$ 的一组基.

### 解答 4.2-5

由**定理 4.2.13 (单代数扩张的结构)**, $F\left(\alpha\right)\cong{F}\left[x\right]/\left(\mathrm{Irr}\left(\alpha,F\right)\right)$. 设 $f\left(x\right)=\mathrm{Irr}\left(\alpha,F\right)$ 为首一 $n$ 次不可约多项式.

商环 $F\left[x\right]/\left(f\left(x\right)\right)$ 中任一元素可唯一写为 $a_0+a_1x+\cdots+a_{n-1}x^{n-1}$ 的形式 (由带余除法, 余式次数小于 $n$). 在同构下, $x$ 对应于 $\alpha$, 故 $F\left(\alpha\right)$ 中任一元素可唯一表为 $a_0+a_1\alpha+\cdots+a_{n-1}\alpha^{n-1}$, $a_i\in{F}$.

因而 $1,\alpha,\cdots,\alpha^{n-1}$ 生成 $F\left(\alpha\right)$, 且在 $F$ 上线性无关 (若 $\sum_{i=0}^{n-1}a_i\alpha^i=0$, 则 $\sum{a}_ix^i$ 是以 $\alpha$ 为根的次数小于 $n$ 的多项式, 与 $f$ 为最小多项式矛盾). 故它们构成 $F\left(\alpha\right)$ 的一组 $F$-基, 且 $\dim_FF\left(\alpha\right)=n$. $\blacksquare$

## 4.2-6

试证明对任何正整数 $n$, 存在 $\mathbb{Q}$ 的代数扩张 $K$ 使得 $\left[K:\mathbb{Q}\right]=n$.

### 解答 4.2-6

取 $K=\mathbb{Q}\left(2^{1/n}\right)$, 即由多项式 $x^n-2$ 的一个根 $\theta=2^{1/n}$ 生成的扩张.

对 $f\left(x\right)=x^n-2\in\mathbb{Z}\left[x\right]$, 取素数 $p=2$. 由艾森斯坦判别法, $2\nmid1$ (首项系数), $2\mid0$ (中间各项系数均为 $0$), 且 $2^2=4\nmid-2$ (常数项), 故 $f\left(x\right)$ 在 $\mathbb{Q}\left[x\right]$ 上不可约.

因而 $\deg\left(\theta,\mathbb{Q}\right)=n$. 由**定理 4.2.13 (单代数扩张的结构)**, $\left[K:\mathbb{Q}\right]=\left[\mathbb{Q}\left(\theta\right):\mathbb{Q}\right]=n$. 又 $K/\mathbb{Q}$ 为单代数扩张, 故为代数扩张. $\blacksquare$

## 4.2-9

若 $a,b\in\mathbb{Q}$ 满足 $\sqrt{a}+\sqrt{b}\ne0$, 证明: $\mathbb{Q}\left(\sqrt{a},\sqrt{b}\right)=\mathbb{Q}\left(\sqrt{a}+\sqrt{b}\right)$.

### 解答 4.2-9

记 $\alpha=\sqrt{a}+\sqrt{b}$. 因 $\alpha\in\mathbb{Q}\left(\sqrt{a},\sqrt{b}\right)$, 故 $\mathbb{Q}\left(\alpha\right)\subseteq\mathbb{Q}\left(\sqrt{a},\sqrt{b}\right)$, 只需证反向包含.

由题设 $\alpha\ne0$, 计算得 $\alpha^2=a+b+2\sqrt{ab}$, 故 $\sqrt{ab}=\frac{\alpha^2-a-b}{2}\in\mathbb{Q}\left(\alpha\right)$. 又 $\sqrt{a}-\sqrt{b}=\frac{\left(\sqrt{a}-\sqrt{b}\right)\left(\sqrt{a}+\sqrt{b}\right)}{\sqrt{a}+\sqrt{b}}=\frac{a-b}{\alpha}\in\mathbb{Q}\left(\alpha\right)$.

于是 $\sqrt{a}=\frac{1}{2}\left(\alpha+\frac{a-b}{\alpha}\right)\in\mathbb{Q}\left(\alpha\right)$, $\sqrt{b}=\frac{1}{2}\left(\alpha-\frac{a-b}{\alpha}\right)\in\mathbb{Q}\left(\alpha\right)$.

因而 $\mathbb{Q}\left(\sqrt{a},\sqrt{b}\right)\subseteq\mathbb{Q}\left(\alpha\right)$. 结合反向包含, 得 $\mathbb{Q}\left(\sqrt{a},\sqrt{b}\right)=\mathbb{Q}\left(\sqrt{a}+\sqrt{b}\right)$. $\blacksquare$

## 4.2-10

设 $E=\mathbb{F}_p\left(t\right)$ 为 $\mathbb{F}_p$ 的单超越扩张.

(1) 证明: $x^p-t\in{E}\left[x\right]$ 不可约;

(2) 设 $\theta$ 是 $x^p-t$ 的一个根, 试将 $x^p-t$ 在 $E\left(\theta\right)$ 上分解为不可约多项式之积.

### 解答 4.2-10

(1) 反设 $x^p-t$ 在 $E\left[x\right]$ 中非平凡分解, $x^p-t=f\left(x\right)g\left(x\right)$, 其中 $f,g$ 首一, $1\le\deg{f}=k<{}p$.

设 $\theta$ 为 $x^p-t$ 在某分裂域中的根, 则 $\theta^p=t$. 由特征 $p$ 下的弗罗贝尼乌斯映射, $\left(x-\theta\right)^p=x^p-\theta^p=x^p-t$. 故在分裂域中 $x^p-t=\left(x-\theta\right)^p$, 从而 $f\left(x\right)=\left(x-\theta\right)^k$.

$f\left(x\right)$ 中 $x^{k-1}$ 的系数为 $-k\theta$. 因 $f\in{E}\left[x\right]$, 该系数属于 $E$, 故 $k\theta\in{E}$. 又 $1\le{k}<{}p$, 在特征 $p$ 域中 $k\ne0$, 故 $k$ 可逆, 从而 $\theta\in{E}$.

但 $\theta\in{E}=\mathbb{F}_p\left(t\right)$ 意味着存在互素多项式 $f_0\left(t\right),g_0\left(t\right)\in\mathbb{F}_p\left[t\right]$ 使 $\theta=f_0\left(t\right)/g_0\left(t\right)$. 由 $\theta^p=t$ 得 $f_0\left(t\right)^p=t\,g_0\left(t\right)^p$. 比较两边次数: 左端次数为 $p\deg{f}_0$, 右端次数为 $1+p\deg{g}_0$. 左端被 $p$ 整除, 右端模 $p$ 余 $1$, 矛盾. 故 $\theta\notin{E}$, 从而 $x^p-t$ 在 $E\left[x\right]$ 中不可约.

(2) 在 $E\left(\theta\right)$ 中, 由特征 $p$ 下的弗罗贝尼乌斯映射, $x^p-t=x^p-\theta^p=\left(x-\theta\right)^p$. 其中 $x-\theta$ 已是一次多项式, 自然不可约. 故 $x^p-t$ 在 $E\left(\theta\right)$ 上的不可约分解为 $\left(x-\theta\right)^p$. $\blacksquare$

## 4.2-13

设 $F\left(\alpha\right)$ 为 $F$ 的单超越扩张, $u\in{F}\left(\alpha\right)$, $u\notin{F}$, 证明 $\alpha$ 是域 $F\left(u\right)$ 上的代数元.

### 解答 4.2-13

因 $u\in{F}\left(\alpha\right)$, 且 $F\left(\alpha\right)$ 是 $F\left[\alpha\right]$ 的分式域, 故存在互素多项式 $f\left(x\right),g\left(x\right)\in{F}\left[x\right]$, $g\left(x\right)\ne0$, 使得 $u=\frac{f\left(\alpha\right)}{g\left(\alpha\right)}$.

考虑多项式 $h\left(x\right)=u\,g\left(x\right)-f\left(x\right)\in{F}\left(u\right)\left[x\right]$. 将 $x=\alpha$ 代入, 得 $h\left(\alpha\right)=u\,g\left(\alpha\right)-f\left(\alpha\right)=0$.

下证 $h\left(x\right)\ne0$. 反设 $h\left(x\right)=0$, 则在 $F\left(u\right)\left[x\right]$ 中有 $u\,g\left(x\right)=f\left(x\right)$.

若 $g\left(x\right)$ 为常数多项式, 则 $f\left(x\right)$ 必非常数 (否则 $u=f/g\in{F}$, 矛盾), 此时 $\deg\left(u\,g\right)=0$ 而 $\deg{f}>0$, 与 $ug=f$ 矛盾.

若 $g\left(x\right)$ 非常数, 则 $\deg\left(ug\right)=\deg{g}$ ($u$ 为 $F\left(u\right)$ 中非零元, 不改变多项式次数). 由 $ug=f$ 得 $\deg{f}=\deg{g}$, 比较首项系数得 $u\cdot\mathrm{lc}\left(g\right)=\mathrm{lc}\left(f\right)$, 即 $u=\mathrm{lc}\left(f\right)/\mathrm{lc}\left(g\right)\in{F}$, 与 $u\notin{F}$ 矛盾.

故 $h\left(x\right)\ne0$, 而 $h\left(\alpha\right)=0$, 即 $\alpha$ 是 $F\left(u\right)$ 上非零多项式 $h$ 的根, 因而 $\alpha$ 是 $F\left(u\right)$ 上的代数元. $\blacksquare$

## 4.4-5

设 $F$ 为域, $c\in{F}$, $\mathrm{char}\,F=p\ne0$. 求证: $x^p-c$ 在 $F\left[x\right]$ 中不可约当且仅当 $x^p-c$ 在 $F$ 中无根.

### 解答 4.4-5

必要性. 设 $x^p-c$ 在 $F$ 中有根 $\alpha$, 即 $\alpha^p=c$, $\alpha\in{F}$. 由特征 $p$ 下的弗罗贝尼乌斯映射, $x^p-c=x^p-\alpha^p=\left(x-\alpha\right)^p$. 因 $p\ge2$, 上式给出 $x^p-c$ 在 $F\left[x\right]$ 中的非平凡分解, 故 $x^p-c$ 可约. 因而不可约必有根的反面成立, 即不可约推出 $x^p-c$ 在 $F$ 中无根.

充分性. 反设 $x^p-c$ 在 $F$ 中无根, 但 $x^p-c$ 在 $F\left[x\right]$ 中可约, 即存在非常数首一多项式 $f\left(x\right),g\left(x\right)\in{F}\left[x\right]$ 使 $x^p-c=f\left(x\right)g\left(x\right)$, 其中 $1\le\deg{f}=k<{}p$.

设 $E$ 为 $x^p-c$ 的分裂域, $\alpha\in{E}$ 为其根. 由特征 $p$ 下的弗罗贝尼乌斯映射, 在 $E\left[x\right]$ 中有 $x^p-c=\left(x-\alpha\right)^p$. 因 $f$ 首一, 比较分解得 $f\left(x\right)=\left(x-\alpha\right)^k$.

$f\left(x\right)=\left(x-\alpha\right)^k$ 中 $x^{k-1}$ 的系数为 $-k\alpha$. 因 $f\in{F}\left[x\right]$, 该系数属于 $F$, 故 $k\alpha\in{F}$. 又 $1\le{k}<{}p$, 在特征 $p$ 域中 $k\ne0$, 因而 $k$ 在 $F$ 中可逆, 故 $\alpha=\left(k\alpha\right)\cdot{k}^{-1}\in{F}$.

于是 $\alpha^p=c$, 即 $\alpha$ 是 $x^p-c$ 在 $F$ 中的根, 与反设矛盾. 故 $x^p-c$ 在 $F$ 中无根时必不可约.

综上, $x^p-c$ 在 $F\left[x\right]$ 中不可约当且仅当它在 $F$ 中无根. $\blacksquare$
