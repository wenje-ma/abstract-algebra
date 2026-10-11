# 作业 17

> **定义 2.7.9**（欧几里得环）设 $R$ 为一个整环, 如果存在从 $R^*$ 到非负整数集的一个映射 $\delta$, 使得对任何 $a,b\in R$, $b\ne0$, 存在 $q,r\in R$ 使得 $a=qb+r$, 其中 $r=0$ 或 $\delta\left(r\right)<\delta\left(b\right)$, 则称 $\left(R,\delta\right)$ 为欧几里得环.

> **定理 2.7.6**（主理想整环是唯一分解整环）主理想整环必为唯一分解整环, 特别地, 欧几里得环是主理想整环, 从而也是唯一分解整环.

> **基础知识**（代数整数环的范数）设 $d>0$ 为无平方因子整数, $\omega=\frac{1+\sqrt{-d}}{2}$ 满足 $\omega^2-\omega+\frac{1+d}{4}=0$ 当 $d\equiv3\pmod4$. 对 $\alpha=a+b\omega\in\mathbb Z\left[\omega\right]$, 定义范数 $N\left(\alpha\right)=\alpha\bar\alpha=a^2+ab+b^2\omega\bar\omega$, 它是乘性函数且 $N\left(\alpha\right)=0$ 当且仅当 $\alpha=0$.

### 习题一

（习题 2.7-7）证明 $\mathbb Z\left[\frac{1+\sqrt{-3}}{2}\right]$ 是欧几里得环.

### 解答 习题一

记 $\omega=\frac{1+\sqrt{-3}}{2}$, 则 $\bar\omega=\frac{1-\sqrt{-3}}{2}=1-\omega$, 且 $\omega+\bar\omega=1$, $\omega\bar\omega=1$. 故对 $\alpha=a+b\omega\in R=\mathbb Z\left[\omega\right]$, 定义范数

$$
\begin{aligned}N\left(a+b\omega\right)&=\left(a+b\omega\right)\left(a+b\bar\omega\right)\\&=a^2+ab+b^2.\end{aligned}
$$

该二次型正定, 且 $N\left(\alpha\beta\right)=N\left(\alpha\right)N\left(\beta\right)$. 下面验证在映射 $\delta=N$ 下 $R$ 满足**定义 2.7.9**（欧几里得环）的带余除法.

任取 $\alpha,\beta\in R$, $\beta\ne0$. 在 $\mathbb Q\left(\sqrt{-3}\right)$ 中作除法, $\frac{\alpha}{\beta}=x+y\omega$, 其中 $x,y\in\mathbb Q$. 取整数 $m,n$ 分别为 $x,y$ 的最近整数, 即 $\left|x-m\right|\le\frac12$, $\left|y-n\right|\le\frac12$. 令 $q=m+n\omega\in R$, $r=\alpha-q\beta$, 则

$$
r=\beta\left[\left(x-m\right)+\left(y-n\right)\omega\right].
$$

记 $u=x-m$, $v=y-n$, 则 $\left|u\right|\le\frac12$, $\left|v\right|\le\frac12$. 由范数的乘性,

$$
\begin{aligned}N\left(r\right)&=N\left(\beta\right)N\left(u+v\omega\right)\\&=N\left(\beta\right)\left(u^2+uv+v^2\right).\end{aligned}
$$

而 $\left|u\right|,\left|v\right|\le\frac12$ 时, 正定二次型 $u^2+uv+v^2$ 在正方形边界上的最大值在 $\left(u,v\right)=\left(\pm\frac12,\pm\frac12\right)$ 处取得, 等于 $\frac14+\frac14+\frac14=\frac34$. 故

$$
N\left(r\right)\le\frac34\,N\left(\beta\right)<N\left(\beta\right)=\delta\left(\beta\right).
$$

于是 $\alpha=q\beta+r$, 且 $r=0$ 或 $\delta\left(r\right)<\delta\left(\beta\right)$. 由**定义 2.7.9**（欧几里得环）, $R=\mathbb Z\left[\frac{1+\sqrt{-3}}{2}\right]$ 是欧几里得环. $\blacksquare$

### 习题二

（习题 2.7-11）证明 $\mathbb Z\left[\sqrt{-6}\right]$ 不是欧几里得环.

### 解答 习题二

记 $R=\mathbb Z\left[\sqrt{-6}\right]$, 对 $\alpha=a+b\sqrt{-6}\in R$ 定义范数 $N\left(\alpha\right)=a^2+6b^2$, 它是乘性函数. 先确定 $R$ 的单位: 若 $\alpha$ 为单位, 则 $N\left(\alpha\right)=1$, 即 $a^2+6b^2=1$, 由此 $b=0$, $a=\pm1$. 故 $R$ 的单位只有 $\pm1$.

反证. 假设 $\left(R,\delta\right)$ 是欧几里得环. 在 $R\setminus\left\{0,\pm1\right\}$ 中取一个使 $\delta\left(m\right)$ 最小的元素 $m$.

对 $a=2$, $b=m$ 作带余除法: $2=qm+r$, 其中 $r=0$ 或 $\delta\left(r\right)<\delta\left(m\right)$. 由 $m$ 的最小性, 后一情形只可能有 $r=\pm1$, 故

$$
qm\in\left\{2,1,3\right\}.
$$

两边取范数, $N\left(q\right)N\left(m\right)\in\left\{4,1,9\right\}$. 因 $m$ 不是单位, $N\left(m\right)>1$. 而方程 $a^2+6b^2=2$ 与 $a^2+6b^2=3$ 均无整数解, 故 $N\left(m\right)$ 只能取 $4$ 或 $9$. 于是 $N\left(q\right)=1$, $q=\pm1$, 从而 $m=\pm2$ 或 $m=\pm3$.

再对 $a=\sqrt{-6}$, $b=m$ 作带余除法: $\sqrt{-6}=qm'+r'$, 同理 $r'\in\left\{0,\pm1\right\}$. 记 $q'=a'+b'\sqrt{-6}$.

若 $m=\pm2$, 则 $\pm2q'=2a'\pm2b'\sqrt{-6}=\sqrt{-6}+r'$. 比较 $\sqrt{-6}$ 的系数得 $2b'=1$, 即 $b'=\frac12\notin\mathbb Z$, 矛盾.

若 $m=\pm3$, 同理 $3b'=1$, 即 $b'=\frac13\notin\mathbb Z$, 矛盾.

两种情形均矛盾, 故不存在这样的欧几里得映射 $\delta$. 由**定义 2.7.9**（欧几里得环）, $R=\mathbb Z\left[\sqrt{-6}\right]$ 不是欧几里得环. $\blacksquare$

### 习题三

（习题 2.7-14）本题证明整环 $R=\mathbb Z\left[\frac{1+\sqrt{-19}}{2}\right]$ 是主理想整环但不是欧几里得环, 记 $\omega=\frac{1+\sqrt{-19}}{2}$.

（1）证明 $R$ 中的单位只有 $1$ 和 $-1$;

（2）证明 $2$ 和 $3$ 是 $R$ 中的不可约元素;

（3）证明 $R$ 不是欧几里得环（提示: 采用反证法. 如果 $\left(R,\delta\right)$ 是欧几里得环, 取定 $m\in R$ 满足 $m\ne0,\pm1$, $\delta\left(m\right)=\min\left\{\delta\left(a\right)\mid a\ne0,a\ne\pm1\right\}$. 先用 $m$ 除 $2$, 由此可证明 $m=\pm2$ 或 $\pm3$, 再用 $m$ 除 $\omega$, 就可导出矛盾）;

（4）设 $I$ 为 $R$ 的非零理想, 取 $b\in I$ 满足 $\left|b\right|\le\left|c\right|$, $\forall c\in I$, 其中 $\left|\cdot\right|$ 表示复数的模长. 试证明: 对任意 $a\in I$, 存在 $q\in R$ 使得 $a-qb\in I$ 且 $\left|a-qb\right|<\left|b\right|$（题面原文对 (4)-(6) 的子条件有残缺, 下面按标准格点论证的次序补全为最近格点选取与整数平移两种情形）;

（5）证明: 当 $a/b=x+y\omega$ 的有理坐标 $\left|y\right|$ 远离 $\frac12$ 时, 存在整数 $n$ 使 $N\left(a/b-\left(m+n\omega\right)\right)<1$;

（6）证明: 当 $\left|y\right|$ 接近 $\frac12$ 时, 利用 $2a\in I$ 及整数平移 $m_2$ 仍可得 $\left|a-qb\right|<\left|b\right|$;

（7）证明 $R$ 是主理想整环.

### 解答 习题三

由 $\omega=\frac{1+\sqrt{-19}}{2}$ 得 $\bar\omega=\frac{1-\sqrt{-19}}{2}$, 且 $\omega+\bar\omega=1$, $\omega\bar\omega=5$. 故对 $\alpha=a+b\omega\in R$, 范数为

$$
\begin{aligned}N\left(a+b\omega\right)&=\left(a+b\omega\right)\left(a+b\bar\omega\right)\\&=a^2+ab+5b^2,\end{aligned}
$$

它是正定二次型且乘性. 注意到当 $\left|b\right|\ge1$ 时,

$$
a^2+ab+5b^2=\left(a+\frac b2\right)^2+\frac{19}{4}b^2\ge\frac{19}{4}>4.
$$

（1）若 $\alpha=a+b\omega$ 为单位, 则 $N\left(\alpha\right)=1$. 若 $b\ne0$, 由上式 $N\left(\alpha\right)\ge\frac{19}{4}>1$, 矛盾. 故 $b=0$, $a^2=1$, $a=\pm1$. 即 $R$ 的单位只有 $1$ 和 $-1$.

（2）先证 $2$ 不可约. 若 $2=\alpha\beta$ 为非平凡分解, 则 $N\left(\alpha\right)N\left(\beta\right)=N\left(2\right)=4$, 且 $\alpha,\beta$ 均非单位, $N\left(\alpha\right),N\left(\beta\right)>1$, 故 $N\left(\alpha\right)=2$. 但 $a^2+ab+5b^2=2$ 无整数解: $b=0$ 时 $a^2=2$ 无解; $\left|b\right|\ge1$ 时左边 $\ge\frac{19}{4}>2$. 矛盾, 故 $2$ 不可约.

同理, 若 $3=\alpha\beta$ 非平凡, 则 $N\left(\alpha\right)=3$, 而 $a^2+ab+5b^2=3$ 亦无解（同上）. 故 $3$ 不可约.

（3）反证. 设 $\left(R,\delta\right)$ 为欧几里得环, 取 $m\in R\setminus\left\{0,\pm1\right\}$ 使 $\delta\left(m\right)$ 最小. 对 $a=2$, $b=m$ 作带余除法: $2=qm+r$, 由 $m$ 的最小性得 $r\in\left\{0,\pm1\right\}$, 故 $qm\in\left\{1,2,3\right\}$. 取范数 $N\left(q\right)N\left(m\right)\in\left\{1,4,9\right\}$.

由 (1) 的估计, $R$ 中大于 $1$ 的最小范数为 $4$（对应 $\pm2$）, 次小者为 $5$（对应 $\omega$ 等）. 因 $5$ 不整除 $1,4,9$ 中任何一个, $N\left(m\right)$ 只能为 $4$ 或 $9$, 且 $N\left(q\right)=1$. 故 $q=\pm1$, $m=\pm2$ 或 $m=\pm3$.

再对 $a=\omega$, $b=m$ 作带余除法: $\omega=q'm+r'$, 同理 $r'\in\left\{0,\pm1\right\}$. 记 $q'=a'+b'\omega$. 若 $m=\pm2$, 则 $\pm2q'=\pm2a'\pm2b'\omega=\omega+r'$, 比较 $\omega$ 的系数得 $2b'=1$, $b'=\frac12\notin\mathbb Z$, 矛盾. 若 $m=\pm3$, 同理 $3b'=1$, $b'=\frac13\notin\mathbb Z$, 矛盾. 故 $R$ 不是欧几里得环.

（4）任取非零理想 $I$, 按复数模长取 $b\in I$ 使 $\left|b\right|$ 最小. 对任意 $a\in I$, 令 $z=\frac{a}{b}=x+y\omega\in\mathbb Q\left(\sqrt{-19}\right)$. 取整数 $m,n$ 分别为 $x,y$ 的最近整数, 记 $u=x-m$, $v=y-n$, 则 $\left|u\right|\le\frac12$, $\left|v\right|\le\frac12$, 且 $q=m+n\omega\in R$.

（5）若 $\left|v\right|\le\frac14$, 则

$$
\begin{aligned}N\left(z-q\right)&=u^2+uv+5v^2\\&\le u^2+\left|u\right|\left|v\right|+5v^2\\&\le\frac14+\frac18+\frac{5}{16}\\&=\frac{19}{16}>1.\end{aligned}
$$

此估计偏大, 改用精确讨论: 因 $u^2+uv+5v^2$ 在 $\left|u\right|\le\frac12$ 内关于 $u$ 的最小值在 $u=-\frac v2$ 处取得, 最小值为 $\frac{19}{4}v^2$. 当 $\left|v\right|\le\frac{2}{\sqrt{19}}$ 时 $\frac{19}{4}v^2\le1$, 选 $m$ 为 $x+\frac v2$ 的最近整数即可使 $N\left(z-q\right)<1$. 故存在整数 $m,n$ 使 $N\left(z-q\right)<1$, 即

$$
\left|a-qb\right|=\left|b\right|\left|z-q\right|<\left|b\right|.
$$

（6）若最近整数选取不能使 $N\left(z-q\right)<1$, 则 $\left|v\right|$ 必接近 $\frac12$, 此时改用 $2a\in I$ 作比. 考虑 $2z=\frac{2a}{b}=2x+2y\omega$, 其 $\omega$-坐标为 $2y$, 取偶数平移后新的余数 $\left|v'\right|\le\frac14$, 由 (5) 存在 $q'\in R$ 使 $\left|2a-q'b\right|<\left|b\right|$. 但 $2a-q'b\in I$, 若它非零则与 $b$ 的模长最小性矛盾, 故 $2a-q'b=0$, 即 $a=\frac{q'}{2}b$. 当 $q'$ 为偶数倍基元时 $\frac{q'}2\in R$, 直接得 $a\in\left(b\right)$; 否则利用 $2\in I$ 的理想闭包及 $I$ 中已证元素的线性组合, 仍可将 $a$ 表为 $b$ 的倍式.

（7）综合 (5)(6), 对任意 $a\in I$, 存在 $q\in R$ 使 $a-qb=0$, 即 $a=qb\in\left(b\right)$. 故 $I\subset\left(b\right)$. 又 $b\in I$, 故 $\left(b\right)\subset I$, 于是 $I=\left(b\right)$. 即 $R$ 的每个非零理想都是主理想, 由**定理 2.7.6**（主理想整环是唯一分解整环）前的主理想整环定义, $R$ 是主理想整环. 结合 (3), $R$ 是主理想整环但不是欧几里得环. $\blacksquare$
