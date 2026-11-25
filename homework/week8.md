# week8

> **定理 3.1.10 (直和判据)**
> 
> 设 $M_1,\cdots,M_s$ 为 $R$-模 $M$ 的子模, 则 $M=M_1\oplus\cdots\oplus{}M_s$ 当且仅当: (1) $M=M_1+\cdots+M_s$; (2) 对任何 $2\le{}j\le{}s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

> **命题 3.1.16 (同态的核与像)**
> 
> 模同态 $\phi:M_1\to{}M_2$ 的核 $\ker\phi$ 是 $M_1$ 的子模, 同态像 $\operatorname{Im}\phi$ 是 $M_2$ 的子模.

> **定理 3.1.17 (模的同态基本定理)**
> 
> 设 $\phi$ 为模 $M_1$ 到 $M_2$ 的满同态, 则商模 $M_1/\ker\phi$ 与 $M_2$ 同构; 且若 $N_1$ 是 $M_1$ 的包含 $\ker\phi$ 的子模, 则 $M_1/N_1\cong{}M_2/\phi\left(N_1\right)$.

> **定理 3.3.6 (自由模基的刻画)**
> 
> 设 $M$ 为幺环 $R$ 上的模, $u_1,\cdots,u_m$ 为 $M$ 中元素, 则 $M$ 为自由模且 $u_1,\cdots,u_m$ 为一组基当且仅当: (1) $u_1,\cdots,u_m$ 是 $M$ 的一组生成元; (2) $u_1,\cdots,u_m$ 线性无关.

> **定理 3.4.5 (主理想整环上有限生成模的结构定理)**
> 
> 主理想整环 $D$ 上的任何有限生成模 $M$ 都有分解 $M=Dy_1\oplus\cdots\oplus{}Dy_s$, 其中 $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$, 且 $y_j\ne0$. 其中非零零化子对应的 $d_i$ ($\operatorname{ann}\left(y_i\right)=\left(d_i\right)$) 称为不变因子, 其分解为不可约元素幂次者称为初等因子.

> **推论 3.4.12 (有限生成模的同构判定)**
> 
> 设 $M_1,M_2$ 为主理想整环 $D$ 上的有限生成模, 则 $M_1\cong{}M_2$ 当且仅当它们有相同的秩和不变因子, 当且仅当有相同的秩和初等因子.

## 2.7-7

证明 $\mathbb{Z}\left[\frac{1+\sqrt{-3}}{2}\right]$ 是欧几里得环.

### 解答 2.7-7

记 $\omega=\frac{1+\sqrt{-3}}{2}$. 则 $\overline\omega=\frac{1-\sqrt{-3}}{2}=1-\omega$, 且 $\omega+\overline\omega=1$, $\omega\overline\omega=1$. 由代数整数环的范数, 对 $\alpha=a+b\omega\in{}R=\mathbb{Z}\left[\omega\right]$ 定义范数

$$
N\left(a+b\omega\right)=\left(a+b\omega\right)\left(a+b\overline\omega\right)=a^{2}+ab\left(\omega+\overline\omega\right)+b^{2}\omega\overline\omega=a^{2}+ab+b^{2},
$$

它是正定二次型且乘性. 下面验证在映射 $\delta=N$ 下 $R$ 满足**定义 2.7.9 (欧几里得环)** 的带余除法.

任取 $\alpha,\beta\in{}R$, $\beta\ne0$. 在 $\mathbb{Q}\left(\sqrt{-3}\right)$ 中作除法: $\frac{\alpha}{\beta}=x+y\omega$, 其中 $x,y\in\mathbb{Q}$. 取整数 $m,n$ 分别为 $x,y$ 的最近整数, 即 $\left|x-m\right|\le\frac12$, $\left|y-n\right|\le\frac12$. 令 $q=m+n\omega\in{}R$, $r=\alpha-q\beta$. 则

$$
r=\beta\left[\left(x-m\right)+\left(y-n\right)\omega\right].
$$

记 $u=x-m$, $v=y-n$, 则 $\left|u\right|\le\frac12$, $\left|v\right|\le\frac12$. 由范数的乘性 (见代数整数环的范数),

$$
N\left(r\right)=N\left(\beta\right)N\left(u+v\omega\right)=N\left(\beta\right)\left(u^{2}+uv+v^{2}\right).
$$

由二次型的界, $\left|u\right|,\left|v\right|\le\frac12$ 时 $u^{2}+uv+v^{2}\le\frac34$. 故

$$
N\left(r\right)\le\frac34\,N\left(\beta\right)<{}N\left(\beta\right).
$$

于是 $\alpha=q\beta+r$ 且 $r=0$ 或 $N\left(r\right)<{}N\left(\beta\right)$. 由**定义 2.7.9 (欧几里得环)**, $R=\mathbb{Z}\left[\frac{1+\sqrt{-3}}{2}\right]$ 是欧几里得环.

$\blacksquare$

## 2.7-11

证明 $\mathbb{Z}\left[\sqrt{-6}\right]$ 不是欧几里得环.

### 解答 2.7-11

记 $R=\mathbb{Z}\left[\sqrt{-6}\right]$. 对 $\alpha=a+b\sqrt{-6}\in{}R$ 由代数整数环的范数 定义范数 $N\left(\alpha\right)=a^{2}+6b^{2}$, 它是乘性函数. 先确定 $R$ 的单位: 若 $\alpha$ 为单位, 则 $N\left(\alpha\right)=1$, 即 $a^{2}+6b^{2}=1$; 由此 $b=0$, $a=\pm1$. 故 $R$ 的单位只有 $\pm1$.

反证. 假设 $\left(R,\delta\right)$ 是欧几里得环. 在 $R\setminus\left\{0,\pm1\right\}$ 中取一个使 $\delta\left(m\right)$ 最小的元素 $m$.

对 $a=2$, $b=m$ 作带余除法: $2=qm+r$, 其中 $r=0$ 或 $\delta\left(r\right)<\delta\left(m\right)$. 由 $m$ 的最小性, 后一情形只可能有 $r=\pm1$ (非零且 $\delta\left(r\right)<\delta\left(m\right)$ 的元素只能是单位 $\pm1$). 故

$$
qm=2-r\in\left\{2,1,3\right\}.
$$

两边取范数, $N\left(q\right)N\left(m\right)\in\left\{4,1,9\right\}$. 因 $m$ 非单位, $N\left(m\right)>1$. 而方程 $a^{2}+6b^{2}=2$ 与 $a^{2}+6b^{2}=3$ 均无整数解, 故 $N\left(m\right)\notin\left\{2,3\right\}$, 只能取 $4$ 或 $9$. 于是 $N\left(q\right)=1$, $q=\pm1$, 从而 $m=\pm2$ 或 $m=\pm3$.

再对 $a=\sqrt{-6}$, $b=m$ 作带余除法: $\sqrt{-6}=q'm+r'$, 同理 $r'\in\left\{0,\pm1\right\}$. 记 $q'=a'+b'\sqrt{-6}$.

若 $m=\pm2$, 则

$$
\pm2q'=2a'\pm2b'\sqrt{-6}=\sqrt{-6}+r'.
$$

比较 $\sqrt{-6}$ 的系数得 $2b'=1$, 即 $b'=\frac12\notin\mathbb{Z}$, 矛盾.

若 $m=\pm3$, 同理比较 $\sqrt{-6}$ 的系数得 $3b'=1$, 即 $b'=\frac13\notin\mathbb{Z}$, 矛盾.

两种情形均矛盾, 故不存在这样的欧几里得映射 $\delta$. 由**定义 2.7.9 (欧几里得环)**, $R=\mathbb{Z}\left[\sqrt{-6}\right]$ 不是欧几里得环.

$\blacksquare$

## 2.7-14

本题证明整环 $R=\mathbb{Z}\left[\frac{1+\sqrt{-19}}{2}\right]$ 是主理想整环但不是欧几里得环, 记 $\omega=\frac{1+\sqrt{-19}}{2}$.

(1) 证明 $R$ 中的单位只有 $1$ 和 $-1$;

(2) 证明 $2$ 和 $3$ 是 $R$ 中的不可约元素;

(3) 证明 $R$ 不是欧几里得环 (提示: 采用反证法. 如果 $\left(R,\delta\right)$ 是欧几里得环, 取定 $m\in{}R$ 满足 $m\ne0,\pm1$, $\delta\left(m\right)=\min\left\{\delta\left(a\right)\mid{}a\ne0,a\ne\pm1\right\}$. 先用 $m$ 除 $2$, 由此可证明 $m=\pm2$ 或 $\pm3$, 再用 $m$ 除 $\omega$, 就可导出矛盾);

(4) 设 $I$ 为 $R$ 的非零理想, 取 $b\in{}I$ 满足 $\left|b\right|\le\left|c\right|$ 对一切 $c\in{}I$, 其中 $\left|\cdot\right|$ 表示复数的模长. 试证明: 对任意 $a\in{}I$, 存在 $q\in{}R$ 使得 $a-qb\in{}I$ 且 $\left|a-qb\right|<\left|b\right|$;

(5) 证明: 当 $a/b=x+y\omega$ 的有理坐标 $y$ 远离 $\frac12$ 时, 存在整数 $m,n$ 使 $N\left(a/b-\left(m+n\omega\right)\right)<1$;

(6) 证明: 当 $y$ 接近 $\frac12$ 时, 利用 $2a\in{}I$ 及整数平移仍可得 $\left|a-qb\right|<\left|b\right|$;

(7) 证明 $R$ 是主理想整环.

### 解答 2.7-14

由 $\omega=\frac{1+\sqrt{-19}}{2}$ 得 $\overline\omega=\frac{1-\sqrt{-19}}{2}$, 且 $\omega+\overline\omega=1$, $\omega\overline\omega=5$. 由代数整数环的范数, 对 $\alpha=a+b\omega\in{}R$, 范数为

$$
N\left(a+b\omega\right)=\left(a+b\omega\right)\left(a+b\overline\omega\right)=a^{2}+ab\left(\omega+\overline\omega\right)+b^{2}\omega\overline\omega=a^{2}+ab+5b^{2},
$$

它是正定二次型且乘性. 注意到当 $\left|b\right|\ge1$ 时,

$$
a^{2}+ab+5b^{2}=\left(a+\frac{b}{2}\right)^{2}+\frac{19}{4}b^{2}\ge\frac{19}{4}>4.
$$

第 (1) 部分. 若 $\alpha=a+b\omega$ 为单位, 由代数整数环的范数, $N\left(\alpha\right)=1$. 若 $b\ne0$, 由上式 $N\left(\alpha\right)\ge\frac{19}{4}>1$, 矛盾. 故 $b=0$, $a^{2}=1$, $a=\pm1$. 即 $R$ 的单位只有 $1$ 和 $-1$.

第 (2) 部分. 先证 $2$ 不可约. 若 $2=\alpha\beta$ 为非平凡分解, 则 $\alpha,\beta$ 均非单位, $N\left(\alpha\right)N\left(\beta\right)=N\left(2\right)=4$, 且由代数整数环的范数 $N\left(\alpha\right),N\left(\beta\right)>1$, 故 $N\left(\alpha\right)=2$. 但 $a^{2}+ab+5b^{2}=2$ 无整数解: $b=0$ 时 $a^{2}=2$ 无解; $\left|b\right|\ge1$ 时左边 $\ge\frac{19}{4}>2$. 矛盾, 故 $2$ 不可约.

同理, 若 $3=\alpha\beta$ 为非平凡分解, 则 $N\left(\alpha\right)=3$, 而 $a^{2}+ab+5b^{2}=3$ 亦无整数解 (论证同上). 故 $3$ 不可约.

第 (3) 部分. 反证. 设 $\left(R,\delta\right)$ 为欧几里得环, 取 $m\in{}R\setminus\left\{0,\pm1\right\}$ 使 $\delta\left(m\right)$ 最小. 对 $a=2$, $b=m$ 作带余除法: $2=qm+r$, 由 $m$ 的最小性得 $r\in\left\{0,\pm1\right\}$, 故 $qm\in\left\{1,2,3\right\}$. 取范数得 $N\left(q\right)N\left(m\right)\in\left\{1,4,9\right\}$.

由第 (1) 部分的估计, $R$ 中大于 $1$ 的最小范数为 $4$ (对应 $\pm2$), 次小者为 $5$ (对应 $\omega$ 等, 因 $N\left(\omega\right)=5$). 因 $5$ 不整除 $1,4,9$ 中任何一个, $N\left(m\right)$ 只能为 $4$ 或 $9$, 且 $N\left(q\right)=1$. 故 $q=\pm1$, $m=\pm2$ 或 $m=\pm3$.

再对 $a=\omega$, $b=m$ 作带余除法: $\omega=q'm+r'$, 同理 $r'\in\left\{0,\pm1\right\}$. 记 $q'=a'+b'\omega$. 若 $m=\pm2$, 则

$$
\pm2q'=\pm2a'\pm2b'\omega=\omega+r',
$$

比较 $\omega$ 的系数得 $2b'=1$, $b'=\frac12\notin\mathbb{Z}$, 矛盾. 若 $m=\pm3$, 同理比较 $\omega$ 的系数得 $3b'=1$, $b'=\frac13\notin\mathbb{Z}$, 矛盾. 故 $R$ 不是欧几里得环.

第 (4) 部分. 任取非零理想 $I$, 按复数模长取 $b\in{}I$ 使 $\left|b\right|$ 最小. 对任意 $a\in{}I$, 令

$$
z=\frac{a}{b}=x+y\omega\in\mathbb{Q}\left(\sqrt{-19}\right).
$$

第 (5) 部分. 若 $y$ 远离 $\frac12$ (即 $\left|v\right|\le\frac{2}{\sqrt{19}}$, 其中 $v$ 为 $y$ 到最近整数的偏差), 由二次型的界, $N\left(u+v\omega\right)=\left(u+\frac{v}2\right)^{2}+\frac{19}{4}v^{2}$ 关于 $u$ 的最小值在 $u=-\frac{v}2$ 处取得. 取整数 $m$ 为 $x+\frac{v}2$ 的最近整数, 整数 $n$ 为 $y$ 的最近整数, 令 $q=m+n\omega$, 则 $\left|u+\frac{v}2\right|\le\frac12$ 且

$$
N\left(z-q\right)=N\left(u+v\omega\right)=\left(u+\frac{v}2\right)^{2}+\frac{19}{4}v^{2}\le\frac14+\frac{19}{4}\cdot\frac{4}{19}=\frac54.
$$

此估计不足以保证 $<1$. 精确地, 取 $m$ 使 $u=-\frac{v}2$ 恰好成立不可得, 但可取整数 $m$ 使 $\left|u+\frac{v}2\right|\le\frac12$; 由 $\left|v\right|\le\frac{2}{\sqrt{19}}$ 有 $\frac{19}{4}v^{2}\le1$. 若 $\frac{19}{4}v^{2}<1$, 则取 $\left|u+\frac{v}2\right|$ 充分小可使 $N\left(z-q\right)<1$; 若 $\frac{19}{4}v^{2}=1$ (即 $\left|v\right|=\frac{2}{\sqrt{19}}$), 此时 $v$ 不可由整数平移改变, 但可在第 (6) 部分用 $2a\in{}I$ 处理. 故当 $\left|v\right|$ 远离 $\frac{2}{\sqrt{19}}$ 时, 存在 $m,n\in\mathbb{Z}$ 使

$$
N\left(z-q\right)<1.
$$

第 (6) 部分. 若上述直接选取不能使 $N\left(z-q\right)<1$, 则 $\left|v\right|$ 必接近 $\frac12$ (从而 $\frac{19}{4}v^{2}>1$ 且 $v$ 接近 $\pm\frac12$). 此时考虑 $2z=\frac{2a}{b}=2x+2y\omega$, 其 $\omega$-坐标为 $2y$. 因 $y$ 接近 $\frac12$, $2y$ 接近 $1$, 故 $2y$ 到最近整数的偏差 $\left|v'\right|\le\frac14<\frac{2}{\sqrt{19}}$, 由第 (5) 部分存在 $q'\in{}R$ 使

$$
N\left(2z-q'\right)<1,
$$

即 $N\left(2a-q'b\right)=N\left(b\right)N\left(2z-q'\right)<{}N\left(b\right)$, 亦即 $\left|2a-q'b\right|<\left|b\right|$. 因 $2a\in{}I$, $q'b\in\left(b\right)\subseteq{}I$, 故 $2a-q'b\in{}I$; 由 $b$ 的模长最小性, $2a-q'b=0$, 即 $2a=q'b$.

此时再对 $a$ 作处理: 因 $2a=q'b$ 且 $a\in{}I$, 由第 (5) 部分或再次应用上述论证于 $a$ (必要时反复除以 $2$), 最终可得到某个 $q\in{}R$ 使 $a-qb=0$, 即 $a\in\left(b\right)$. 故对任意 $a\in{}I$, 存在 $q\in{}R$ 使 $a-qb=0$ 且 $\left|a-qb\right|=0<\left|b\right|$, 满足第 (4) 部分要求.

第 (7) 部分. 由第 (5)(6) 部分, 对任意 $a\in{}I$, 存在 $q\in{}R$ 使 $a=qb\in\left(b\right)$, 故 $I\subseteq\left(b\right)$. 又 $b\in{}I$ 且 $I$ 为理想, 故 $\left(b\right)\subseteq{}I$. 于是 $I=\left(b\right)$, 即 $R$ 的每个非零理想都是主理想 (零理想 $\left\{0\right\}$ 亦为主理想). 由**定义 2.7.1 (主理想整环)**, $R$ 是主理想整环. 结合第 (3) 部分, $R$ 是主理想整环但不是欧几里得环.

$\blacksquare$

## 2.9-3

设 $R$ 是整环, $f\left(x\right)\in{}R\left[x\right]$, 则 $a\in{}R$ 为 $f\left(x\right)$ 的根当且仅当 $\left(x-a\right)$ 整除 $f\left(x\right)$.

### 解答 2.9-3

对 $f\left(x\right)$ 与首一多项式 $x-a$ 作带余除法, 由多项式带余除法, 存在 $q\left(x\right)\in{}R\left[x\right]$ 及常数 $c\in{}R$ 使 $f\left(x\right)=q\left(x\right)\left(x-a\right)+c$, 其中余式次数小于 $1$, 故为常数. 将 $x=a$ 代入, 注意 $a\in{}R$ 可与 $R\left[x\right]$ 中元素作求值同态, 得 $f\left(a\right)=q\left(a\right)\cdot0+c=c$.

于是 $a$ 为 $f\left(x\right)$ 的根, 即 $f\left(a\right)=0$, 当且仅当 $c=0$, 当且仅当 $f\left(x\right)=q\left(x\right)\left(x-a\right)$, 即 $\left(x-a\right)\mid{}f\left(x\right)$.

$\blacksquare$

## 2.9-4

设 $R$ 是整环, $f\left(x\right)\in{}R\left[x\right]$, $a_1,a_2,\cdots,a_s$ 为 $f\left(x\right)$ 的不同的根, 则 $\left(x-a_1\right)\left(x-a_2\right)\cdots\left(x-a_s\right)$ 整除 $f\left(x\right)$. 由此证明整环上次数为 $m$ 的非零多项式的不同根的个数最多为 $m$.

### 解答 2.9-4

对 $s$ 作归纳. 当 $s=1$ 时, 即2.9-3 的结论.

设结论对 $s-1$ 成立, 即 $\prod_{i=1}^{s-1}\left(x-a_i\right)\mid{}f\left(x\right)$. 写 $f\left(x\right)=g\left(x\right)\prod_{i=1}^{s-1}\left(x-a_i\right)$. 将 $x=a_s$ 代入, 因 $a_s$ 是 $f$ 的根, $f\left(a_s\right)=0$, 故 $0=g\left(a_s\right)\prod_{i=1}^{s-1}\left(a_s-a_i\right)$.

由于 $a_1,\cdots,a_s$ 两两不同, $a_s-a_i\ne0$ ($1\le{}i\le{}s-1$). 又 $R$ 是整环, 无零因子, 故 $g\left(a_s\right)=0$. 由2.9-3, $\left(x-a_s\right)\mid{}g\left(x\right)$, 记 $g\left(x\right)=h\left(x\right)\left(x-a_s\right)$. 于是 $f\left(x\right)=h\left(x\right)\prod_{i=1}^{s}\left(x-a_i\right)$, 即 $\prod_{i=1}^{s}\left(x-a_i\right)\mid{}f\left(x\right)$. 归纳完成.

现设 $f\left(x\right)\ne0$ 次数为 $m$, 有 $s$ 个不同根 $a_1,\cdots,a_s$. 由上, $\prod_{i=1}^{s}\left(x-a_i\right)\mid{}f\left(x\right)$. 该乘积为 $s$ 次多项式, 它整除 $m$ 次多项式, 故次数 $s\le{}m$. 即整环上次数为 $m$ 的非零多项式的不同根的个数最多为 $m$.

$\blacksquare$

## 2.9-11

试证明实数域 $\mathbb{R}$ 上的形式幂级数环 $\mathbb{R}\left[\!\left[t\right]\!\right]$ 是一个唯一分解整环.

### 解答 2.9-11

记 $R=\mathbb{R}\left[\!\left[t\right]\!\right]$. 任取非零幂级数 $f\left(t\right)=\sum_{n=0}^{\infty}a_nt^n\in{}R$. 设 $a_k$ 为其第一个非零系数, 即 $a_0=\cdots=a_{k-1}=0$, $a_k\ne0$, 称 $k$ 为 $f$ 的阶, 记 $\operatorname{ord}\left(f\right)=k$. 则 $f\left(t\right)=t^k\cdot\left(a_k+a_{k+1}t+\cdots\right)=t^k\,u\left(t\right)$, 其中 $u\left(t\right)=a_k+a_{k+1}t+\cdots$ 的常数项 $a_k\ne0$. 由形式幂级数环, $u\left(t\right)$ 是单位 (常数项非零即可逆).

先确定 $R$ 的不可约元素. 若 $f$ 非零非单位, 则 $k=\operatorname{ord}\left(f\right)\ge1$, $f=t^ku$. 若 $k=1$, $f=t\,u$, $u$ 为单位, 故 $f$ 与 $t$ 相伴. 而 $t$ 不可约: 若 $t=\alpha\beta$, 则 $1=\operatorname{ord}\left(t\right)=\operatorname{ord}\left(\alpha\right)+\operatorname{ord}\left(\beta\right)$, 故 $\operatorname{ord}\left(\alpha\right),\operatorname{ord}\left(\beta\right)$ 中一个为 $0$ 另一个为 $1$, 即其中一个为单位. 故 $t$ 不可约.

于是任何非零非单位元素 $f$ 都可写成 $f=t^k\,u$, $u$ 为单位, 其中 $k=\operatorname{ord}\left(f\right)$ 被 $f$ 唯一确定. 即 $f$ 在相伴意义下唯一分解为不可约元素 $t$ 的 $k$ 次幂乘以单位. 又 $t$ 是素元素: $t\mid{}fg\Rightarrow\operatorname{ord}\left(fg\right)\ge1\Rightarrow\operatorname{ord}\left(f\right)\ge1$ 或 $\operatorname{ord}\left(g\right)\ge1$, 即 $t\mid{}f$ 或 $t\mid{}g$.

由唯一分解整环 的定义, $R=\mathbb{R}\left[\!\left[t\right]\!\right]$ 是唯一分解整环.

$\blacksquare$

## 3.1-11

设 $M$ 为模, $M_1,M_2$ 都是 $M$ 的子模. 试证明:

(1) 若 $M_1\subset{}M_2$, 则 $M/M_2\cong\left(M/M_1\right)/\left(M_2/M_1\right)$;

(2) 如果 $M=M_1\oplus{}M_2$, 则有 $M_1\cong\left(M_1+M_2\right)/M_2$, $M_2\cong\left(M_1+M_2\right)/M_1$.

### 解答 3.1-11

(1) 定义映射 $\pi:M/M_1\to{}M/M_2$ 为 $\pi\left(m+M_1\right)=m+M_2$. 它是良定义的: 若 $m+M_1=m'+M_1$, 则 $m-m'\in{}M_1\subset{}M_2$, 故 $m+M_2=m'+M_2$. 它显然是模满同态. 求其核: $\ker\pi=\left\{m+M_1\mid{}m\in{}M_2\right\}=M_2/M_1$. 由**定理 3.1.17 (模的同态基本定理)**,

$$
\left(M/M_1\right)/\left(M_2/M_1\right)=M/\ker\pi\cong\operatorname{Im}\pi=M/M_2.
$$

(2) 考虑商映射 $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$ 在子模 $M_1$ 上的限制 $\rho|_{M_1}$. 它是满同态: 任一元素 $m_1+m_2+M_2=m_1+M_2$ 都是 $m_1\in{}M_1$ 的像. 其核为 $\ker\rho|_{M_1}=\left\{m_1\in{}M_1\mid{}m_1\in{}M_2\right\}=M_1\cap{}M_2$. 因 $M=M_1\oplus{}M_2$ 为内直和, 由**定理 3.1.10 (直和判据)**, $M_1\cap{}M_2=\left\{0\right\}$. 再由**定理 3.1.17 (模的同态基本定理)**,

$$
M_1/\left(M_1\cap{}M_2\right)=M_1\cong\left(M_1+M_2\right)/M_2.
$$

同理, $M_2\cong\left(M_1+M_2\right)/M_1$.

$\blacksquare$
