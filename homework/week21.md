# 作业 21

> **定理 3.4.5**（结构定理）主理想整环 $D$ 上的任何有限生成模 $M$ 都有分解 $M=Dy_1\oplus\cdots\oplus Dy_s$, 其中 $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$, 且 $y_j\ne0$. 其中非零零化子对应的 $d_i$（$\operatorname{ann}\left(y_i\right)=\left(d_i\right)$）称为不变因子, 其分解为不可约元素幂次者称为初等因子.

> **推论 3.4.12**（同构判定）设 $M_1,M_2$ 为主理想整环 $D$ 上的有限生成模, 则 $M_1\cong M_2$ 当且仅当它们有相同的秩和不变因子, 当且仅当有相同的秩和初等因子.

> **定理 3.4.9**（$p$-分支分解）设 $M$ 为主理想整环 $D$ 上有限生成扭模, 则存在有限个互不相伴的不可约元素 $p_1,\cdots,p_m$ 使 $M=M_{p_1}\oplus\cdots\oplus M_{p_m}$, 其中 $M_p=\left\{x\in M\mid \exists e,\ p^ex=0\right\}$ 为 $p$-分支. 特别地, 若 $\operatorname{ann}\left(y\right)=\left(ab\right)$ 且 $a,b$ 互素, 则 $Dy=Dy_1\oplus Dy_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$.

> **定理 2.7.7**（贝祖等式）设 $R$ 为主理想整环, $a,b\in R$, $d$ 为 $a,b$ 的一个最大公因子, 则存在 $u,v\in R$ 使 $d=ua+vb$.

### 习题一

（习题 3.4-4）设 $R=\mathbb Z\left[\alpha\right]$, 试构造一个有限生成的 $R$-模 $M$, 使得 $M$ 不能写成有限个循环子模的直和.（题面原文丢失了对 $\alpha$ 的条件, 这里按标准取 $\alpha$ 为不定元, 即 $R=\mathbb Z\left[x\right]$, 它不是主理想整环.）

### 解答 习题一

取 $R=\mathbb Z\left[x\right]$, 其中 $\alpha=x$ 为不定元. $R$ 不是主理想整环: 理想 $I=\left(2,x\right)$ 不由单个元素生成.

现在把理想 $I$ 本身看作一个 $R$-模. 它由 $2$ 和 $x$ 生成, 因而是有限生成 $R$-模. 下证 $I$ 不能写成有限个循环子模的直和.

反证. 若 $I=N_1\oplus\cdots\oplus N_k$, 每个 $N_j$ 是循环子模, 记 $N_j=Ry_j$. 由于 $I$ 是整环 $R$ 的理想, $I$ 作为 $R$-模无挠（若 $r\in R$ 非零, $a\in I$ 非零, 则 $ra\ne0$）. 故每个循环模 $Ry_j\cong R/\operatorname{ann}\left(y_j\right)$ 中 $\operatorname{ann}\left(y_j\right)=0$, 即 $N_j\cong R$. 于是 $I\cong R^k$.

再看秩. 作张量积到分式域 $\mathbb Q\left(x\right)$ 上, $I\otimes_R\mathbb Q\left(x\right)=\mathbb Q\left(x\right)$, 秩为 $1$. 故 $k=1$, 即 $I\cong R$, 从而 $I$ 是主理想, $I=\left(g\right)$.

但 $I=\left(2,x\right)$ 不是主理想: $R=\mathbb Z\left[x\right]$ 的单位只有 $\pm1$, 若 $I=\left(g\right)$, 则 $2=gf$, $x=gh$. 由 $2=gf$ 知 $f,g$ 只能是常数 $\pm1,\pm2$; 结合 $x=gh$ 不可能（$x$ 不能整除 $2$）. 更直接地, $I$ 中每个元素 $2f+xg$ 的常数项都是偶数, 故 $1\notin I$, 因而 $I\ne R=\left(1\right)$, 也不可能由 $\pm2$ 或 $x$ 单独生成.

矛盾. 故 $I$ 不能写成有限个循环子模的直和. 这与**定理 3.4.5**（结构定理）仅在主理想整环上成立相吻合: 脱离主理想整环前提, 有限生成模一般不能分解为循环子模的直和. $\blacksquare$

### 习题二

（习题 3.4-5）设 $D=\mathbb Z\left[i\right]$（高斯整数环, 是主理想整环）, $K$ 为 $D^3$ 中由向量 $\left(2-3i,\ 6+9i,\ -18i\right)$ 生成的子模, 试求出 $D^3/K$ 的不变因子和初等因子.（题面原文开头残缺, 按数学上成立的理解补全为上述形式; 其中 $i=\sqrt{-1}$.）

### 解答 习题二

记 $v=\left(2-3i,\ 6+9i,\ -18i\right)\in D^3$, $K=Dv$. 商模 $D^3/K$ 由 $1\times3$ 矩阵

$$
A=\begin{pmatrix}2-3i & 6+9i & -18i\end{pmatrix}
$$

的史密斯标准形决定. 不变因子的第一个为 $A$ 三个元素的最大公因子（在相伴意义下）.

在 $D=\mathbb Z\left[i\right]$ 中计算. 记 $a=2-3i$, 其范数 $N\left(a\right)=2^2+3^2=13$, 故 $a$ 是 $D$ 中的不可约元素（$13=\left(2-3i\right)\left(2+3i\right)$）. 又 $b=6+9i=3\left(2+3i\right)$, $c=-18i$, $N\left(c\right)=18^2=324$.

考察 $a=2-3i$ 是否整除 $b,c$:

$$
\begin{aligned}&\quad\;\frac{b}{a}\\&=\frac{3\left(2+3i\right)\left(2+3i\right)}{13}\\&=\frac{3\left(-5+12i\right)}{13}\\&\notin\mathbb Z\left[i\right],\end{aligned}
$$

$$
\begin{aligned}&\quad\;\frac{c}{a}\\&=\frac{-18i\left(2+3i\right)}{13}\\&=\frac{54-36i}{13}\\&\notin\mathbb Z\left[i\right].\end{aligned}
$$

故 $a\nmid b$, $a\nmid c$. 而 $a$ 的非平凡因子只有其相伴元（$a$ 不可约）, 所以 $a$ 不是 $b,c$ 的公因子. 同理 $2+3i$ 也不整除 $a$. 于是 $a,b,c$ 的最大公因子是 $D$ 中的单位 $1$.

因此 $A$ 的史密斯标准形为 $\begin{pmatrix}1 & 0 & 0\end{pmatrix}$. 由**推论 3.4.12**（同构判定）,

$$
D^3/K\cong D/\left(1\right)\oplus D/\left(0\right)\oplus D/\left(0\right)\cong D^2.
$$

即 $D^3/K$ 的秩为 $2$, 挠部分为零. 故其不变因子（挠部分 $d_1,\cdots,d_k$）为空, 初等因子也为空; 模同构于自由模 $D^2$. $\blacksquare$

### 习题三

（习题 3.4-6）设 $D$ 是主理想整环, $M$ 是 $D$ 上有限生成的扭模, 对 $a\in D$, 令 $M\left(a\right)=\left\{x\in M\mid ax=0\right\}$. 试证明:

（1）$M\left(a\right)$ 是 $M$ 的子模, 且若 $a$ 可逆, 则 $M\left(a\right)=\left\{0\right\}$;

（2）若 $a\mid b$, 则 $M\left(a\right)\subset M\left(b\right)$;

（3）设 $a,b\in D$, 则 $M\left(a\right)\cap M\left(b\right)=M\left(\left(a,b\right)\right)$, 其中 $\left(a,b\right)$ 为 $a,b$ 的一个最大公因子;

（4）若 $a,b$ 互素, 则 $M\left(ab\right)=M\left(a\right)\oplus M\left(b\right)$.

### 解答 习题三

（1）$M\left(a\right)$ 非空（含 $0$）. 若 $x,y\in M\left(a\right)$, 则 $a\left(x-y\right)=ax-ay=0$; 对 $r\in D$, $a\left(rx\right)=r\left(ax\right)=0$. 故 $M\left(a\right)$ 是子模. 若 $a$ 可逆, $ax=0$ 两边乘 $a^{-1}$ 得 $x=0$, 故 $M\left(a\right)=\left\{0\right\}$.

（2）设 $b=ac$. 若 $x\in M\left(a\right)$, $ax=0$, 则 $bx=cax=0$, 故 $x\in M\left(b\right)$. 因而 $M\left(a\right)\subset M\left(b\right)$.

（3）记 $d=\left(a,b\right)$ 为最大公因子. 由 $d\mid a$, $d\mid b$, 用 (2) 得 $M\left(d\right)\subset M\left(a\right)$ 且 $M\left(d\right)\subset M\left(b\right)$, 故 $M\left(d\right)\subset M\left(a\right)\cap M\left(b\right)$.

反之, 若 $x\in M\left(a\right)\cap M\left(b\right)$, 则 $ax=bx=0$. 由**定理 2.7.7**（贝祖等式）, 存在 $u,v\in D$ 使 $d=ua+vb$. 于是

$$
\begin{aligned}&\quad\;dx\\&=\left(ua+vb\right)x\\&=uax+vbx\\&=0,\end{aligned}
$$

故 $x\in M\left(d\right)$. 因此 $M\left(a\right)\cap M\left(b\right)=M\left(d\right)=M\left(\left(a,b\right)\right)$.

（4）设 $a,b$ 互素, 即 $\left(a,b\right)=1$. 由 (2), $a\mid ab$, $b\mid ab$, 故 $M\left(a\right)\subset M\left(ab\right)$, $M\left(b\right)\subset M\left(ab\right)$, 因而 $M\left(a\right)+M\left(b\right)\subset M\left(ab\right)$.

再求交. 由 (3), $M\left(a\right)\cap M\left(b\right)=M\left(\left(a,b\right)\right)=M\left(1\right)=\left\{0\right\}$（用 (1)）.

最后证 $M\left(ab\right)\subset M\left(a\right)+M\left(b\right)$. 由 $\left(a,b\right)=1$ 及**定理 2.7.7**, 存在 $u,v$ 使 $ua+vb=1$. 对任意 $x\in M\left(ab\right)$, $abx=0$. 写

$$
\begin{aligned}&\quad\;x\\&=\left(ua+vb\right)x\\&=uax+vb x.\end{aligned}
$$

记 $x_1=vb x$, $x_2=uax$. 则

$$
\begin{aligned}&\quad\;ax_1\\&=avb x\\&=vab x\\&=0,\quad &\quad\;bx_2\\&=bua x\\&=uab x\\&=0,\end{aligned}
$$

故 $x_1\in M\left(a\right)$, $x_2\in M\left(b\right)$, 从而 $x=x_1+x_2\in M\left(a\right)+M\left(b\right)$.

综上, $M\left(ab\right)=M\left(a\right)+M\left(b\right)$ 且 $M\left(a\right)\cap M\left(b\right)=\left\{0\right\}$, 故

$$
M\left(ab\right)=M\left(a\right)\oplus M\left(b\right).
$$

$\blacksquare$

### 习题四

（习题 3.4-10）设 $M$ 为主理想整环 $D$ 上的扭模, 试证明 $M$ 为单模当且仅当 $M=Dz$, 且 $\operatorname{ann}\left(z\right)=\left(p\right)$, 其中 $p$ 为素元素; 而 $M$ 为不可分解模当且仅当 $M=Dz$ 且 $\operatorname{ann}\left(z\right)=\left(p^e\right)$, 其中 $p$ 为素元素, $e\in\mathbb N$.（题面原文末式残缺, 按教材上下文补全为 $\left(p^e\right)$.）

### 解答 习题四

**单模情形**.

必要性. 设 $M$ 为单扭模. 由**定理 3.4.5**（结构定理）, $M=Dy_1\oplus\cdots\oplus Dy_s$. 若 $s\ge2$, 则 $Dy_1$ 是 $M$ 的非平凡子模, 与单模矛盾. 故 $s=1$, $M=Dz$, $\operatorname{ann}\left(z\right)=\left(d\right)$.

若 $d$ 不是素元素, 则 $d$ 有非平凡分解 $d=ab$, $a,b$ 均非单位. 由**定理 3.4.9**（$p$-分支分解）, $Dz=Dy_1\oplus Dy_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$, 两个均为非零子模, 又与单模矛盾. 故 $d=p$ 为素元素.

充分性. 设 $M=Dz$, $\operatorname{ann}\left(z\right)=\left(p\right)$, $p$ 素. 则 $M\cong D/\left(p\right)$. 因 $p$ 为素元素, $\left(p\right)$ 是极大理想, $D/\left(p\right)$ 是域, 作为 $D$-模它只有零和自身两个子模. 故 $M$ 是单模.

**不可分解模情形**.

必要性. 设 $M$ 不可分解. 由结构定理 $M=Dy_1\oplus\cdots\oplus Dy_s$. 若 $s\ge2$, 它已是两个非零子模的直和, 矛盾. 故 $s=1$, $M=Dz$, $\operatorname{ann}\left(z\right)=\left(d\right)$.

若 $d$ 含有两个互素的非单位因子, 即 $d=ab$, $\left(a,b\right)=1$, $a,b$ 均非单位, 则由**定理 3.4.9**, $Dz=Dz_1\oplus Dz_2$, 两个均非零, 矛盾. 故 $d$ 的所有不可约因子相伴, 即 $d=p^e$, $p$ 素, $e\in\mathbb N$.

充分性. 设 $M=Dz$, $\operatorname{ann}\left(z\right)=\left(p^e\right)$. $M\cong D/\left(p^e\right)$. $D/\left(p^e\right)$ 的子模与 $D$ 中包含 $\left(p^e\right)$ 的理想一一对应, 而这些理想为

$$
\left(p^e\right)\subset\left(p^{e-1}\right)\subset\cdots\subset\left(p\right)\subset D,
$$

构成一条全序链. 若 $M=N_1\oplus N_2$ 为两个非零子模直和, 则 $N_1,N_2$ 都是上述链中的非零真子模, 必两两有包含关系, 从而 $N_1\cap N_2\ne0$, 与直和矛盾. 故 $M$ 不可分解.

（注: 若允许秩为 $1$ 的自由循环模 $Dz$ 且 $\operatorname{ann}\left(z\right)=0$, 它同样不可分解, 因整环 $D$ 无非平凡理想直和分解.） $\blacksquare$
