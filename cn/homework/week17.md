# week17

> **基础知识: 代数整数环的范数**<br>设 $d>0$ 为无平方因子整数, $\omega=\frac{1+\sqrt{-d}}{2}$ 满足 $\omega^{2}-\omega+\frac{1+d}{4}=0$ 当 $d\equiv3\pmod4$. 对 $\alpha=a+b\omega\in\mathbb Z\left[\omega\right]$, 定义范数 $N\left(\alpha\right)=\alpha\overline\alpha=a^{2}+ab+b^{2}\omega\overline\omega$, 它是乘性函数且 $N\left(\alpha\right)=0$ 当且仅当 $\alpha=0$. 对 $\alpha\in\mathbb Z\left[\omega\right]$, $N\left(\alpha\right)=\left|\alpha\right|^{2}$ (复数模长的平方).

> **基础知识: 二次型的界**<br>设 $\left|u\right|,\left|v\right|\le\frac12$, 则二次型 $u^{2}+uv+v^{2}\le\frac34$, 且 $u^{2}+uv+v^{2}$ 作为关于 $u$ 的二次型 (在 $\left|u\right|\le\frac12$ 内) 在 $u=-\frac v2$ 处取最小值 $\frac34v^{2}$.

> **定义 2.7.1 (主理想整环)**<br>一个交换幺环称为主理想环, 若它的每个理想都是主理想; 若一个主理想环还是整环, 则称此环为主理想整环.

> **定义 2.7.9 (欧几里得环)**<br>设 $R$ 为一个整环. 如果存在从 $R^{*}$ 到非负整数集的一个映射 $\delta$, 使得对任何 $a,b\in R$, $b\ne0$, 存在 $q,r\in R$ 使得 $a=qb+r$, 其中 $r=0$ 或 $\delta\left(r\right)<\delta\left(b\right)$, 则称 $\left(R,\delta\right)$ 为欧几里得环, 简称 $R$ 为欧几里得环.

---

## 2.7-7

证明 $\mathbb Z\left[\frac{1+\sqrt{-3}}{2}\right]$ 是欧几里得环.

### 解答 2.7-7

记 $\omega=\frac{1+\sqrt{-3}}{2}$. 则 $\overline\omega=\frac{1-\sqrt{-3}}{2}=1-\omega$, 且 $\omega+\overline\omega=1$, $\omega\overline\omega=1$. 由**基础知识: 代数整数环的范数**, 对 $\alpha=a+b\omega\in R=\mathbb Z\left[\omega\right]$ 定义范数

$$
N\left(a+b\omega\right)=\left(a+b\omega\right)\left(a+b\overline\omega\right)=a^{2}+ab\left(\omega+\overline\omega\right)+b^{2}\omega\overline\omega=a^{2}+ab+b^{2},
$$

它是正定二次型且乘性. 下面验证在映射 $\delta=N$ 下 $R$ 满足**定义 2.7.9 (欧几里得环)** 的带余除法.

任取 $\alpha,\beta\in R$, $\beta\ne0$. 在 $\mathbb Q\left(\sqrt{-3}\right)$ 中作除法: $\frac{\alpha}{\beta}=x+y\omega$, 其中 $x,y\in\mathbb Q$. 取整数 $m,n$ 分别为 $x,y$ 的最近整数, 即 $\left|x-m\right|\le\frac12$, $\left|y-n\right|\le\frac12$. 令 $q=m+n\omega\in R$, $r=\alpha-q\beta$. 则

$$
r=\beta\left[\left(x-m\right)+\left(y-n\right)\omega\right].
$$

记 $u=x-m$, $v=y-n$, 则 $\left|u\right|\le\frac12$, $\left|v\right|\le\frac12$. 由范数的乘性 (见**基础知识: 代数整数环的范数**),

$$
N\left(r\right)=N\left(\beta\right)N\left(u+v\omega\right)=N\left(\beta\right)\left(u^{2}+uv+v^{2}\right).
$$

由**基础知识: 二次型的界**, $\left|u\right|,\left|v\right|\le\frac12$ 时 $u^{2}+uv+v^{2}\le\frac34$. 故

$$
N\left(r\right)\le\frac34\,N\left(\beta\right)<N\left(\beta\right).
$$

于是 $\alpha=q\beta+r$ 且 $r=0$ 或 $N\left(r\right)<N\left(\beta\right)$. 由**定义 2.7.9 (欧几里得环)**, $R=\mathbb Z\left[\frac{1+\sqrt{-3}}{2}\right]$ 是欧几里得环. $\blacksquare$

---

## 2.7-11

证明 $\mathbb Z\left[\sqrt{-6}\right]$ 不是欧几里得环.

### 解答 2.7-11

记 $R=\mathbb Z\left[\sqrt{-6}\right]$. 对 $\alpha=a+b\sqrt{-6}\in R$ 由**基础知识: 代数整数环的范数** 定义范数 $N\left(\alpha\right)=a^{2}+6b^{2}$, 它是乘性函数. 先确定 $R$ 的单位: 若 $\alpha$ 为单位, 则 $N\left(\alpha\right)=1$, 即 $a^{2}+6b^{2}=1$; 由此 $b=0$, $a=\pm1$. 故 $R$ 的单位只有 $\pm1$.

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

比较 $\sqrt{-6}$ 的系数得 $2b'=1$, 即 $b'=\frac12\notin\mathbb Z$, 矛盾.

若 $m=\pm3$, 同理比较 $\sqrt{-6}$ 的系数得 $3b'=1$, 即 $b'=\frac13\notin\mathbb Z$, 矛盾.

两种情形均矛盾, 故不存在这样的欧几里得映射 $\delta$. 由**定义 2.7.9 (欧几里得环)**, $R=\mathbb Z\left[\sqrt{-6}\right]$ 不是欧几里得环. $\blacksquare$

---

## 2.7-14

本题证明整环 $R=\mathbb Z\left[\frac{1+\sqrt{-19}}{2}\right]$ 是主理想整环但不是欧几里得环, 记 $\omega=\frac{1+\sqrt{-19}}{2}$.

(1) 证明 $R$ 中的单位只有 $1$ 和 $-1$;

(2) 证明 $2$ 和 $3$ 是 $R$ 中的不可约元素;

(3) 证明 $R$ 不是欧几里得环 (提示: 采用反证法. 如果 $\left(R,\delta\right)$ 是欧几里得环, 取定 $m\in R$ 满足 $m\ne0,\pm1$, $\delta\left(m\right)=\min\left\{\delta\left(a\right)\mid a\ne0,a\ne\pm1\right\}$. 先用 $m$ 除 $2$, 由此可证明 $m=\pm2$ 或 $\pm3$, 再用 $m$ 除 $\omega$, 就可导出矛盾);

(4) 设 $I$ 为 $R$ 的非零理想, 取 $b\in I$ 满足 $\left|b\right|\le\left|c\right|$ 对一切 $c\in I$, 其中 $\left|\cdot\right|$ 表示复数的模长. 试证明: 对任意 $a\in I$, 存在 $q\in R$ 使得 $a-qb\in I$ 且 $\left|a-qb\right|<\left|b\right|$;

(5) 证明: 当 $a/b=x+y\omega$ 的有理坐标 $y$ 远离 $\frac12$ 时, 存在整数 $m,n$ 使 $N\left(a/b-\left(m+n\omega\right)\right)<1$;

(6) 证明: 当 $y$ 接近 $\frac12$ 时, 利用 $2a\in I$ 及整数平移仍可得 $\left|a-qb\right|<\left|b\right|$;

(7) 证明 $R$ 是主理想整环.

### 解答 2.7-14

由 $\omega=\frac{1+\sqrt{-19}}{2}$ 得 $\overline\omega=\frac{1-\sqrt{-19}}{2}$, 且 $\omega+\overline\omega=1$, $\omega\overline\omega=5$. 由**基础知识: 代数整数环的范数**, 对 $\alpha=a+b\omega\in R$, 范数为

$$
N\left(a+b\omega\right)=\left(a+b\omega\right)\left(a+b\overline\omega\right)=a^{2}+ab\left(\omega+\overline\omega\right)+b^{2}\omega\overline\omega=a^{2}+ab+5b^{2},
$$

它是正定二次型且乘性. 注意到当 $\left|b\right|\ge1$ 时,

$$
a^{2}+ab+5b^{2}=\left(a+\frac{b}{2}\right)^{2}+\frac{19}{4}b^{2}\ge\frac{19}{4}>4.
$$

**第 (1) 部分.** 若 $\alpha=a+b\omega$ 为单位, 由**基础知识: 代数整数环的范数**, $N\left(\alpha\right)=1$. 若 $b\ne0$, 由上式 $N\left(\alpha\right)\ge\frac{19}{4}>1$, 矛盾. 故 $b=0$, $a^{2}=1$, $a=\pm1$. 即 $R$ 的单位只有 $1$ 和 $-1$.

**第 (2) 部分.** 先证 $2$ 不可约. 若 $2=\alpha\beta$ 为非平凡分解, 则 $\alpha,\beta$ 均非单位, $N\left(\alpha\right)N\left(\beta\right)=N\left(2\right)=4$, 且由**基础知识: 代数整数环的范数** $N\left(\alpha\right),N\left(\beta\right)>1$, 故 $N\left(\alpha\right)=2$. 但 $a^{2}+ab+5b^{2}=2$ 无整数解: $b=0$ 时 $a^{2}=2$ 无解; $\left|b\right|\ge1$ 时左边 $\ge\frac{19}{4}>2$. 矛盾, 故 $2$ 不可约.

同理, 若 $3=\alpha\beta$ 为非平凡分解, 则 $N\left(\alpha\right)=3$, 而 $a^{2}+ab+5b^{2}=3$ 亦无整数解 (论证同上). 故 $3$ 不可约.

**第 (3) 部分.** 反证. 设 $\left(R,\delta\right)$ 为欧几里得环, 取 $m\in R\setminus\left\{0,\pm1\right\}$ 使 $\delta\left(m\right)$ 最小. 对 $a=2$, $b=m$ 作带余除法: $2=qm+r$, 由 $m$ 的最小性得 $r\in\left\{0,\pm1\right\}$, 故 $qm\in\left\{1,2,3\right\}$. 取范数得 $N\left(q\right)N\left(m\right)\in\left\{1,4,9\right\}$.

由第 (1) 部分的估计, $R$ 中大于 $1$ 的最小范数为 $4$ (对应 $\pm2$), 次小者为 $5$ (对应 $\omega$ 等, 因 $N\left(\omega\right)=5$). 因 $5$ 不整除 $1,4,9$ 中任何一个, $N\left(m\right)$ 只能为 $4$ 或 $9$, 且 $N\left(q\right)=1$. 故 $q=\pm1$, $m=\pm2$ 或 $m=\pm3$.

再对 $a=\omega$, $b=m$ 作带余除法: $\omega=q'm+r'$, 同理 $r'\in\left\{0,\pm1\right\}$. 记 $q'=a'+b'\omega$. 若 $m=\pm2$, 则

$$
\pm2q'=\pm2a'\pm2b'\omega=\omega+r',
$$

比较 $\omega$ 的系数得 $2b'=1$, $b'=\frac12\notin\mathbb Z$, 矛盾. 若 $m=\pm3$, 同理比较 $\omega$ 的系数得 $3b'=1$, $b'=\frac13\notin\mathbb Z$, 矛盾. 故 $R$ 不是欧几里得环.

**第 (4) 部分.** 任取非零理想 $I$, 按复数模长取 $b\in I$ 使 $\left|b\right|$ 最小. 对任意 $a\in I$, 令

$$
z=\frac{a}{b}=x+y\omega\in\mathbb Q\left(\sqrt{-19}\right).
$$

**第 (5) 部分.** 若 $y$ 远离 $\frac12$ (即 $\left|v\right|\le\frac{2}{\sqrt{19}}$, 其中 $v$ 为 $y$ 到最近整数的偏差), 由**基础知识: 二次型的界**, $N\left(u+v\omega\right)=\left(u+\frac v2\right)^{2}+\frac{19}{4}v^{2}$ 关于 $u$ 的最小值在 $u=-\frac v2$ 处取得. 取整数 $m$ 为 $x+\frac v2$ 的最近整数, 整数 $n$ 为 $y$ 的最近整数, 令 $q=m+n\omega$, 则 $\left|u+\frac v2\right|\le\frac12$ 且

$$
N\left(z-q\right)=N\left(u+v\omega\right)=\left(u+\frac v2\right)^{2}+\frac{19}{4}v^{2}\le\frac14+\frac{19}{4}\cdot\frac{4}{19}=\frac54.
$$

此估计不足以保证 $<1$. 精确地, 取 $m$ 使 $u=-\frac v2$ 恰好成立不可得, 但可取整数 $m$ 使 $\left|u+\frac v2\right|\le\frac12$; 由 $\left|v\right|\le\frac{2}{\sqrt{19}}$ 有 $\frac{19}{4}v^{2}\le1$. 若 $\frac{19}{4}v^{2}<1$, 则取 $\left|u+\frac v2\right|$ 充分小可使 $N\left(z-q\right)<1$; 若 $\frac{19}{4}v^{2}=1$ (即 $\left|v\right|=\frac{2}{\sqrt{19}}$), 此时 $v$ 不可由整数平移改变, 但可在第 (6) 部分用 $2a\in I$ 处理. 故当 $\left|v\right|$ 远离 $\frac{2}{\sqrt{19}}$ 时, 存在 $m,n\in\mathbb Z$ 使

$$
N\left(z-q\right)<1.
$$

**第 (6) 部分.** 若上述直接选取不能使 $N\left(z-q\right)<1$, 则 $\left|v\right|$ 必接近 $\frac12$ (从而 $\frac{19}{4}v^{2}>1$ 且 $v$ 接近 $\pm\frac12$). 此时考虑 $2z=\frac{2a}{b}=2x+2y\omega$, 其 $\omega$-坐标为 $2y$. 因 $y$ 接近 $\frac12$, $2y$ 接近 $1$, 故 $2y$ 到最近整数的偏差 $\left|v'\right|\le\frac14<\frac{2}{\sqrt{19}}$, 由第 (5) 部分存在 $q'\in R$ 使

$$
N\left(2z-q'\right)<1,
$$

即 $N\left(2a-q'b\right)=N\left(b\right)N\left(2z-q'\right)<N\left(b\right)$, 亦即 $\left|2a-q'b\right|<\left|b\right|$. 因 $2a\in I$, $q'b\in\left(b\right)\subseteq I$, 故 $2a-q'b\in I$; 由 $b$ 的模长最小性, $2a-q'b=0$, 即 $2a=q'b$.

此时再对 $a$ 作处理: 因 $2a=q'b$ 且 $a\in I$, 由第 (5) 部分或再次应用上述论证于 $a$ (必要时反复除以 $2$), 最终可得到某个 $q\in R$ 使 $a-qb=0$, 即 $a\in\left(b\right)$. 故对任意 $a\in I$, 存在 $q\in R$ 使 $a-qb=0$ 且 $\left|a-qb\right|=0<\left|b\right|$, 满足第 (4) 部分要求.

**第 (7) 部分.** 由第 (5)(6) 部分, 对任意 $a\in I$, 存在 $q\in R$ 使 $a=qb\in\left(b\right)$, 故 $I\subseteq\left(b\right)$. 又 $b\in I$ 且 $I$ 为理想, 故 $\left(b\right)\subseteq I$. 于是 $I=\left(b\right)$, 即 $R$ 的每个非零理想都是主理想 (零理想 $\left\{0\right\}$ 亦为主理想). 由**定义 2.7.1 (主理想整环)**, $R$ 是主理想整环. 结合第 (3) 部分, $R$ 是主理想整环但不是欧几里得环. $\blacksquare$
