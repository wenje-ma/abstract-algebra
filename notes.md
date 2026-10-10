# 抽象代数

## 群的基本概念

**定义 1.1.4**（半群与幺半群）

设 $S$ 是非空集合, 其上定义了一个满足结合律的二元运算 $*$, 则称 $\left[S;*\right]$ 为一个半群. 若半群中存在单位元 $e$, 即对任意 $a\in S$ 有 $ea=ae=a$, 则称该半群为幺半群; 若运算还满足交换律, 则称交换幺半群.

**例 1.1.7**（变换幺半群）

设 $X$ 为非空集合, $M\left(X\right)$ 为 $X$ 上所有变换的全体, 则 $M\left(X\right)$ 在变换的复合下构成幺半群, 其单位元为 $X$ 的恒等变换.

**定义 1.1.10**（逆元）

设 $S$ 是幺半群, $e$ 是单位元, $a\in S$. 若存在 $b\in S$ 使 $ba=e$（$ab=e$）, 则称 $b$ 为 $a$ 的左（右）逆元; 若 $ba=ab=e$, 则称 $b$ 为 $a$ 的逆元, 此时称 $a$ 为可逆元.

**定义 1.1.14**（群与阿贝尔群）

若幺半群 $G$ 中的每个元都是可逆元, 则称 $G$ 为一个群. 若群中运算还满足交换律, 则称 $G$ 为交换群或阿贝尔群.

**引理 1.1.17**（消去律）

群 $G$ 的运算满足左（右）消去律, 即对任意 $a,b,c\in G$, 由 $ab=ac$（$ba=ca$）可推出 $b=c$.

**定义 1.2.1**（子群）

设 $H$ 是群 $G$ 的一个非空子集, 如果 $H$ 对于 $G$ 的运算也构成群, 则称 $H$ 为 $G$ 的子群, 记作 $H< G$.

**定理 1.2.2**（子群判别法）

设 $H$ 是群 $G$ 的非空子集, 则 $H< G$ 当且仅当对任意 $a,b\in H$ 有 $ab^{-1}\in H$.

**定理 1.2.22**（拉格朗日定理）

设 $G$ 是有限群, $H< G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, 其中 $\left[G:H\right]$ 为 $H$ 在 $G$ 中的指数. 从而子群 $H$ 的阶是群 $G$ 的阶的因子, 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

**推论 1.2.23**（指数的乘法）

设 $G$ 是有限群, $K< H< G$, 则有 $\left[G:K\right]=\left[G:H\right]\cdot\left[H:K\right]$.

**基础知识**（对称差）

对任意 $A,B\in\mathcal P\left(X\right)$, 对称差定义为 $A\triangle B=\left(A\setminus B\right)\cup\left(B\setminus A\right)$.

**基础知识**（元素的阶）

设 $G$ 为群, $a\in G$, 则 $\left\langle a\right\rangle=\left\{a^{n}\mid n\in\mathbb Z\right\}$ 是 $G$ 的子群, 称为由 $a$ 生成的子群. 该子群的阶称为元素 $a$ 的阶.

**基础知识**（最小公倍数与最大公因数）

对正整数 $m,n$, 记 $\left(m,n\right)$ 为最大公因数, $\left[m,n\right]$ 为最小公倍数, 满足 $\left(m,n\right)\left[m,n\right]=mn$.

**基础知识**（狄利克雷卷积）

对 $f,g\in S$, 狄利克雷卷积定义为

$$
\begin{aligned}&\quad\;\left(f*g\right)\left(n\right)\\
&=\sum_{d\mid n}f\left(d\right)g\left(\frac{n}{d}\right)\\
&=\sum_{ab=n}f\left(a\right)g\left(b\right).
\end{aligned}
$$

## 群同态与群的结构

**定义 1.3.1**（正规子群）

设 $H$ 是群 $G$ 的子群. 如果对任意 $g\in G$, $h\in H$, 有 $ghg^{-1}\in H$, 则称 $H$ 为 $G$ 的一个正规子群, 记为 $H\triangleleft G$.

**定理 1.3.5**（正规子群的等价条件）

设 $G$ 是群, $H< G$, 则下列条件等价: （1）$H\triangleleft G$; （2）对任意 $g\in G$, $gH=Hg$; （3）对任意 $a,b\in G$, $aH\cdot bH=abH$.

**定理 1.3.6**（商群）

设 $G$ 是群, $H\triangleleft G$, 则 $G/H$ 对陪集乘法 $aH\cdot bH=abH$ 构成一个群, 称为 $G$ 对 $H$ 的商群.

**定义 1.4.1**（群同态与同构）

设 $G$ 和 $G'$ 是两个群, 如果映射 $f:G\to G'$ 满足 $f\left(ab\right)=f\left(a\right)f\left(b\right)$, $\forall a,b\in G$, 则称 $f$ 是 $G$ 到 $G'$ 的群同态. 若同态 $f$ 是双射, 则称 $f$ 是 $G$ 到 $G'$ 的群同构, 此时称群 $G$ 与 $G'$ 是同构的, 记为 $G\cong G'$.

**定义 1.4.9**（左平移与右平移）

对任意 $a\in G$, 定义 $G$ 上的变换 $L_{a},R_{a}$ 为 $L_{a}\left(g\right)=ag$, $R_{a}\left(g\right)=ga$, $\forall g\in G$. 分别称为由 $a$ 决定的左平移变换和右平移变换.

**定义 1.4.11**（同态的核与像）

设 $f:G\to G'$ 是群同态, 分别称集合 $\ker f=\left\{a\in G\mid f\left(a\right)=e'\right\}$ 与 $\mathrm{Im}\left(f\right)=f\left(G\right)$ 为同态 $f$ 的核和像.

**定理 1.4.19**（群的同态基本定理）

设 $f:G\to G'$ 是群的满同态, 则 $G/\ker f\cong G'$.

**定理 1.5.5**（循环群的分类）

设 $G$ 是循环群, 若 $G$ 是无限群, 则 $G$ 与 $\left(\mathbb Z,+\right)$ 同构; 若 $G$ 是 $n$ 阶群, 则 $G$ 与 $\left(\mathbb Z_{n},+\right)$ 同构. 从而, 两个循环群同构当且仅当它们有相同的阶.

**引理 1.5.7**（循环群的子群结构）

循环群 $G=\left\langle a\right\rangle$ 的任一子群都形如 $\left\langle a^{l}\right\rangle$, $l\in\mathbb N$, 从而也是循环群.

**定理 1.5.8**（循环群的子群存在唯一性）

设 $G$ 是 $n$ 阶循环群, $k\mid n$, 则存在 $G$ 的唯一的 $k$ 阶子群.

**基础知识**（共轭元素与共轭类）

称 $G$ 中的两个元素 $a,b$ 是共轭的, 如果存在 $g\in G$ 使得 $b=gag^{-1}$. 与 $a$ 共轭的所有元素的全体称为 $a$ 的共轭类.

**基础知识**（子群乘积）

设 $H,K$ 是群 $G$ 的子群, 则 $HK=\left\{hk\mid h\in H,k\in K\right\}$. $HK$ 是 $G$ 的子群当且仅当 $HK=KH$.

**基础知识**（第二同构定理）

设 $A,B$ 是 $G$ 的子群且 $B\trianglelefteq G$, $A\le G$, 则 $A\cap B\trianglelefteq A$ 且 $A/\left(A\cap B\right)\cong AB/B$. 特别地, 若 $A,B$ 均为 $G$ 的正规子群, 则 $AB/\!A\cong B/\left(A\cap B\right)$.

**基础知识**（反同态）

若映射 $f:G\to G'$ 满足 $f\left(ab\right)=f\left(b\right)f\left(a\right)$, 则称 $f$ 为反同态. 若反同态为双射, 则称反同构.

**基础知识**（欧拉函数）

$\varphi\left(n\right)$ 为与 $n$ 互素且不超过 $n$ 的正整数的个数. 对正整数 $n$, 有 $\sum_{d\mid n}\varphi\left(d\right)=n$. $n$ 阶循环群中恰有 $\varphi\left(n\right)$ 个生成元.

## 置换群与可解性

**定义 1.6.1**（轮换）

设 $\left\{i_{1},i_{2},\dots,i_{r}\right\}\subseteq\left\{1,2,\dots,n\right\}$. 若 $\sigma\in S_{n}$ 满足 $\sigma\left(i_{1}\right)=i_{2}$, $\sigma\left(i_{2}\right)=i_{3}$, ..., $\sigma\left(i_{r}\right)=i_{1}$, 且 $\sigma$ 固定其余文字, 则称 $\sigma$ 为一个 $r$-轮换, 记为 $\sigma=\left(i_{1}i_{2}\dots i_{r}\right)$. 特别地, $2$-轮换称为对换.

**定理 1.6.4**（轮换分解）

$S_{n}$ 中的任何元素都可表为 $S_{n}$ 中一些不相交轮换之积. 如果不计次序, 表法是唯一的.

**引理 1.6.7**（轮换的对换分解）

任一个 $r$-轮换都可写成 $r-1$ 个对换的乘积:

$$
\left(i_{1}i_{2}\dots i_{r}\right)=\left(i_{1}i_{r}\right)\left(i_{1}i_{r-1}\right)\dots\left(i_{1}i_{3}\right)\left(i_{1}i_{2}\right).
$$

**定理 1.6.9**（交错群的单性）

当 $n\ge 5$ 时, $A_{n}$ 是单群.

**定义 1.7.9**（次正规序列与合成序列）

群 $G$ 中的子群序列

$$
G=G_1\trianglerighteq G_2\trianglerighteq\cdots\trianglerighteq G_t\trianglerighteq G_{t+1}=\left\{e\right\}
$$

若满足 $G_{i+1}\trianglelefteq G_i$, 则称为次正规序列, 称 $G_i/G_{i+1}$ 为其因子. 若诸因子 $G_i/G_{i+1}$ 都是单群, 则称该次正规序列为 $G$ 的合成序列, 称 $G_i/G_{i+1}$ 为 $G$ 的合成因子.

**定义 1.7.12**（同构序列）

群 $G$ 的两个次正规序列称为同构的, 如果这两个序列的因子集之间有一一对应, 且对应的因子同构.

**定理 1.7.13**（若尔当-赫尔德定理）

设群 $G$ 存在合成序列, 则 $G$ 的任意两个合成序列同构.

**定义 1.8.1**（换位子与换位子群）

设 $g,h\in G$, 称 $g^{-1}h^{-1}gh$ 为 $g,h$ 的换位子, 记为 $\left[g,h\right]$. 若 $H,K$ 都是 $G$ 的子群, 称 $\left[H,K\right]=\left\langle\left[h,k\right]\mid h\in H,k\in K\right\rangle$ 为 $H,K$ 的换位子群. 特别地, $\left[G,G\right]$ 称为 $G$ 的换位子群.

**定义 1.8.7**（可解群与幂零群）

在群 $G$ 中归纳定义导出列 $G^{\left(0\right)}=G$, $G^{\left(k+1\right)}=\left[G^{\left(k\right)},G^{\left(k\right)}\right]$. 若存在 $t$ 使得 $G^{\left(t\right)}=\left\{e\right\}$, 则称 $G$ 为可解群. 归纳定义降中心列 $G^{1}=G$, $G^{k+1}=\left[G,G^{k}\right]$, 若存在 $t$ 使得 $G^{t}=\left\{e\right\}$, 则称 $G$ 为幂零群.

**引理 1.8.8**（可解群的遗传性）

可解群的子群、商群都是可解群; 反之, 设 $N\trianglelefteq G$, 且 $N$ 与 $G/N$ 都可解, 则 $G$ 可解.

**基础知识**（交错群）

当一个置换能表为奇（偶）数个对换的乘积时, 称为奇置换（偶置换）. $n$ 元偶置换的全体 $A_{n}$ 是 $S_{n}$ 的正规子群, 称为 $n$ 元交错群, 且 $\left|A_{n}\right|=\left|S_{n}\right|/2=n!/2$.

**基础知识**（李定理的关键引理）

设 $G$ 是 $\mathrm{GL}\left(V\right)$ 的可解子群, 其中 $V$ 是复数域上的有限维线性空间, 则 $G$ 在 $V$ 上有公共特征向量, 即存在 $V$ 的一维子空间在 $G$ 的作用下不变. 反复使用此结论可得 $G$ 可同时上三角化, 即 $G$ 共轭于可逆上三角矩阵群 $B$ 的子群.

## 群作用与西罗定理

**定义 1.9.1**（群作用）

设 $G$ 是群, $X$ 是非空集合. 若映射 $f:G\times X\to X$ 满足 $f\left(e,x\right)=x$ 且 $f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right)$, 则称 $f$ 决定了 $G$ 在 $X$ 上的一个作用, 记 $f\left(g,x\right)=gx$.

**定义 1.9.7**（可递作用与有效作用）

若对任意 $x,y\in X$ 存在 $g\in G$ 使 $gx=y$, 称作用可递, 称 $X$ 为 $G$ 的齐性空间. 若由 $gx=x$ 对一切 $x\in X$ 成立可推出 $g=e$, 称作用有效.

**定义 1.9.9**（轨道与迷向子群）

设 $G$ 作用在 $X$ 上, $x\in X$. 称 $Ox=\left\{gx\mid g\in G\right\}$ 为 $x$ 的轨道. 称 $F_x=\left\{g\in G\mid gx=x\right\}$ 为 $x$ 的迷向子群.

**引理 1.9.11**（迷向子群的共轭）

设 $y=gx\in Ox$, 则 $F_y=gF_xg^{-1}$.

**推论 1.9.15**（轨道-迷向子群定理）

设群 $G$ 作用在 $X$ 上, $x\in X$, 则 $\left|Ox\right|=\left[G:F_x\right]$, 从而 $\left|Ox\right|$ 整除 $\left|G\right|$.

**定理 1.10.1**（柯西定理）

设素数 $p$ 是 $\left|G\right|$ 的因子, 则 $G$ 中存在 $p$ 阶元.

**定理 1.10.5**（西罗第一定理）

设 $\left|G\right|=p^{l}m$, $p$ 为素数, $l\ge1$, $\left(p,m\right)=1$, 则对任意 $k\le l$, $G$ 中存在 $p^{k}$ 阶子群. 特别地, $G$ 存在西罗 $p$-子群（$p^{l}$ 阶子群）.

**定理 1.10.8**（西罗第二定理）

设 $P$ 是 $G$ 的一个西罗 $p$-子群, $H$ 是 $G$ 的一个 $p^{k}$ 阶子群, $k\le l$, 则存在 $g\in G$ 使 $H\subseteq gPg^{-1}$. 特别地, $G$ 的西罗 $p$-子群相互共轭.

**定理 1.10.10**（西罗第三定理）

设 $G$ 的西罗 $p$-子群的个数为 $n_p$, 则 $n_p\mid m$, 且 $n_p\equiv1\pmod p$. 又西罗 $p$-子群正规当且仅当 $n_p=1$.

## 环与理想

**定义 2.1.1**（环）

设 $R$ 是非空集合, 在 $R$ 上定义两种二元运算 $+$ 与 $\cdot$, 满足:

（1）$\left[R;+\right]$ 是交换群;

（2）$\left[R;\cdot\right]$ 是半群（乘法满足结合律）;

（3）乘法对加法满足左右分配律: $a\left(b+c\right)=ab+ac$, $\left(a+b\right)c=ac+bc$.

则称 $R$ 为一个环.

**定义 2.1.8**（无零因子环）

如果环 $R$ 不是零环且没有零因子, 则称 $R$ 为无零因子环.

**命题 2.2.11**（理想判别法）

设 $R$ 为环, $I$ 为 $R$ 的非空子集, 则 $I$ 为 $R$ 的理想的充分必要条件是对任意 $a,b\in I$ 有 $a-b\in I$, 且对任意 $a\in I$, $\alpha,\gamma\in R$ 有 $\alpha a,a\gamma\in I$.

**定理 2.2.16**（商环）

设 $R$ 是一个环, $I$ 是 $R$ 的理想, 则商加法群 $R/I$ 在乘法 $\left(a+I\right)\left(b+I\right)=ab+I$ 下构成一个环, 称为 $R$ 对 $I$ 的商环.

**定义 2.2.20**（整环、除环与域）

无零因子的交换幺环称为整环; 若幺环 $R$ 满足 $R^*$ 对乘法构成群（$R^*=R\setminus\left\{0\right\}$）, 则称 $R$ 为除环; 交换的除环称为域.

**定义 2.4.1**（环同态与同构）

设 $R_1,R_2$ 为两个环, $f$ 为 $R_1$ 到 $R_2$ 的映射, 若对任何 $a,b\in R_1$ 有 $f\left(a+b\right)=f\left(a\right)+f\left(b\right)$, $f\left(ab\right)=f\left(a\right)f\left(b\right)$, 则称 $f$ 为同态; 单射的同态称为单同态, 满射的同态称为满同态, 双射的同态称为同构.

**基础知识**（幺环中可逆元的性质）

设 $R$ 为幺环, $e$ 为幺元. 若 $u,v\in R$ 可逆, 则 $uv$ 可逆, 且 $\left(uv\right)^{-1}=v^{-1}u^{-1}$. 若 $x^{m}=0$, 则有限几何级数给出

$$
\left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}.
$$

**基础知识**（四元数与共轭）

四元数体中元素写成 $\alpha=a+bi+cj+dk$, $a,b,c,d\in\mathbb R$, 其共轭为 $\overline\alpha=a-bi-cj-dk$, 范数 $N\left(\alpha\right)=\alpha\overline\alpha=a^2+b^2+c^2+d^2\in\mathbb R$. 共轭满足 $\overline{\alpha+\beta}=\overline\alpha+\overline\beta$, $\overline{\alpha\beta}=\overline\beta\overline\alpha$, $\overline{\overline\alpha}=\alpha$, 且实数的共轭为其自身.

## 唯一分解整环与欧几里得环

**定义 2.5.2**（相伴）

设 $R$ 为整环, $a,b\in R$. 如果存在 $R$ 中单位 $u$ 使得 $a=ub$, 则称 $a$ 与 $b$ 相伴, 记为 $a\sim b$.

**定义 2.5.6**（不可约元素）

设 $R$ 为整环, $\alpha\in R^*\setminus U$. 如果 $\alpha$ 不存在非平凡因子, 则称 $\alpha$ 为不可约元素, 否则称 $\alpha$ 为可约元素.

**定义 2.5.14**（公因子与最大公因子）

设 $R$ 为整环, $a_1,a_2,\cdots,a_n\in R$. 若 $c\in R$ 同时整除所有 $a_i$, 则称 $c$ 为它们的公因子; 若公因子 $d$ 能被任一公因子整除, 则称 $d$ 为最大公因子.

**定理 2.5.15**（唯一分解整环的等价条件）

整环 $R$ 为唯一分解整环, 当且仅当 $R$ 满足因子链条件与素条件, 即在唯一分解整环中每个不可约元素都是素元素: $p\mid ab$ 可推出 $p\mid a$ 或 $p\mid b$.

**定义 2.6.1**（素理想）

设 $I$ 为环 $R$ 的理想, $I\ne R$, 如果由 $ab\in I$ 可以推出 $a\in I$ 或 $b\in I$, 则称 $I$ 为 $R$ 的一个素理想.

**定理 2.7.6**（主理想整环是唯一分解整环）

主理想整环必为唯一分解整环, 特别地, 欧几里得环是主理想整环, 从而也是唯一分解整环.

**定理 2.7.7**（贝祖等式）

设 $R$ 为主理想整环, $a,b\in R$, $d$ 为 $a,b$ 的一个最大公因子, 则存在 $u,v\in R$ 使 $d=ua+vb$.

**定义 2.7.9**（欧几里得环）

设 $R$ 为一个整环, 如果存在从 $R^*$ 到非负整数集的一个映射 $\delta$, 使得对任何 $a,b\in R$, $b\ne0$, 存在 $q,r\in R$ 使得 $a=qb+r$, 其中 $r=0$ 或 $\delta\left(r\right)< \delta\left(b\right)$, 则称 $\left(R,\delta\right)$ 为欧几里得环.

**基础知识**（唯一分解整环）

一个整环 $R$ 称为唯一分解整环, 如果 $R$ 中每个非零非单位元素都可分解为有限个不可约元素的乘积, 且在相伴意义下分解唯一.

**基础知识**（代数整数环的范数）

设 $d> 0$ 为无平方因子整数, $\omega=\frac{1+\sqrt{-d}}{2}$ 满足 $\omega^2-\omega+\frac{1+d}{4}=0$ 当 $d\equiv3\pmod4$. 对 $\alpha=a+b\omega\in\mathbb Z\left[\omega\right]$, 定义范数 $N\left(\alpha\right)=\alpha\overline\alpha=a^2+ab+b^2\omega\overline\omega$, 它是乘性函数且 $N\left(\alpha\right)=0$ 当且仅当 $\alpha=0$.

## 多项式与幂级数

**基础知识**（多项式带余除法）

设 $R$ 为交换幺环, $f\left(x\right),g\left(x\right)\in R\left[x\right]$, 且 $g\left(x\right)$ 的首项系数为 $R$ 中的单位, 则存在唯一 $q\left(x\right),r\left(x\right)\in R\left[x\right]$ 使 $f\left(x\right)=q\left(x\right)g\left(x\right)+r\left(x\right)$, 其中 $r=0$ 或 $\deg r< \deg g$. 特别地, 除式为一次首一多项式 $x-a$ 时余式为常数.

**基础知识**（形式幂级数环）

域 $k$ 上的形式幂级数环 $k\left[\!\left[t\right]\!\right]$ 由所有 $\sum_{n=0}^{\infty}a_nt^n$ 组成, 其单位恰为常数项非零的幂级数.

**基础知识**（艾森斯坦判别法）

设 $f\left(x\right)=a_nx^n+\cdots+a_0\in\mathbb Z\left[x\right]$, 若存在素数 $p$ 使得 $p\nmid a_n$, $p\mid a_i$ 对 $i=0,1,\cdots,n-1$, 但 $p^2\nmid a_0$, 则 $f\left(x\right)$ 在 $\mathbb Q\left[x\right]$ 上不可约.

## 模与模同态

**定理 3.1.10**（直和判据）

设 $M_1,\cdots,M_s$ 为 $R$-模 $M$ 的子模, 则 $M=M_1\oplus\cdots\oplus M_s$ 当且仅当 （1）$M=M_1+\cdots+M_s$; （2）对任何 $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

**命题 3.1.16**（同态的核与像）

模同态 $\phi:M_1\to M_2$ 的核 $\ker\phi$ 是 $M_1$ 的子模, 同态像 $\operatorname{Im}\phi$ 是 $M_2$ 的子模.

**定理 3.1.17**（模的同态基本定理）

设 $\phi$ 为模 $M_1$ 到 $M_2$ 的满同态, 则商模 $M_1/\ker\phi$ 与 $M_2$ 同构; 且若 $N_1$ 是 $M_1$ 的包含 $\ker\phi$ 的子模, 则 $M_1/N_1\cong M_2/\phi\left(N_1\right)$.

**定理 3.3.6**（基的刻画）

设 $M$ 为幺环 $R$ 上的模, $u_1,\cdots,u_m$ 为 $M$ 中元素, 则 $M$ 为自由模且 $u_1,\cdots,u_m$ 为一组基当且仅当 （1）$u_1,\cdots,u_m$ 是 $M$ 的一组生成元; （2）$u_1,\cdots,u_m$ 线性无关.

**推论 3.3.10**（自由模秩的唯一性）

设 $R$ 为交换幺环, 则 $R^m\cong R^n$ 当且仅当 $m=n$, 其中 $R^m$ 表示 $m$ 个 $R$ 的外直和.

**基础知识**（行列式）

交换幺环 $R$ 上方阵 $A$ 可逆当且仅当其行列式 $\det A$ 为 $R$ 中的单位.

## 主理想整环上的有限生成模

**定理 3.4.5**（结构定理）

主理想整环 $D$ 上的任何有限生成模 $M$ 都有分解 $M=Dy_1\oplus\cdots\oplus Dy_s$, 其中 $\operatorname{ann}\left(y_1\right)\supset\operatorname{ann}\left(y_2\right)\supset\cdots\supset\operatorname{ann}\left(y_s\right)$, 且 $y_j\ne0$. 其中非零零化子对应的 $d_i$（$\operatorname{ann}\left(y_i\right)=\left(d_i\right)$）称为不变因子, 其分解为不可约元素幂次者称为初等因子.

**定理 3.4.9**（$p$-分支分解）

设 $M$ 为主理想整环 $D$ 上有限生成扭模, 则存在有限个互不相伴的不可约元素 $p_1,\cdots,p_m$ 使 $M=M_{p_1}\oplus\cdots\oplus M_{p_m}$, 其中 $M_p=\left\{x\in M\mid \exists e,\ p^ex=0\right\}$ 为 $p$-分支. 特别地, 若 $\operatorname{ann}\left(y\right)=\left(ab\right)$ 且 $a,b$ 互素, 则 $Dy=Dy_1\oplus Dy_2$, $\operatorname{ann}\left(y_1\right)=\left(a\right)$, $\operatorname{ann}\left(y_2\right)=\left(b\right)$.

**推论 3.4.12**（同构判定）

设 $M_1,M_2$ 为主理想整环 $D$ 上的有限生成模, 则 $M_1\cong M_2$ 当且仅当它们有相同的秩和不变因子, 当且仅当有相同的秩和初等因子.

**定理 3.5.2**（有限交换群的分类数）

设自然数 $n$ 有素因数分解 $n=p_1^{m_1}p_2^{m_2}\cdots p_s^{m_s}$, 其中 $p_1,p_2,\cdots,p_s$ 为互不相同的素数, $m_i> 0$, 则在同构意义下 $n$ 阶交换群的个数为 $\prod_{i=1}^s p\left(m_i\right)$, 其中 $p\left(m\right)$ 表示自然数 $m$ 的不同分划的个数.

**定理 3.6.3**（约当标准形）

设 $F$ 为特征为零的代数闭域, $V$ 为 $F$ 上 $n$ 维线性空间, $A$ 为 $V$ 上的线性变换, 则存在 $V$ 的一组基使得 $A$ 在该基下的矩阵为准对角矩阵 $\mathrm{diag}\left(J_1,J_2,\cdots,J_s\right)$, 其中每个 $J_i$ 都是约当块. 两个 $F$ 上 $n\times n$ 矩阵相似当且仅当它们具有相同的约当标准形.

**基础知识**（直积中元素的阶）

设 $G=H_1\times H_2\times\cdots\times H_s$ 为有限交换群的直积, $g=\left(h_1,h_2,\cdots,h_s\right)$, 则 $o\left(g\right)=\mathrm{lcm}\left(o\left(h_1\right),o\left(h_2\right),\cdots,o\left(h_s\right)\right)$. 特别地, $o\left(g\right)\mid q$ 当且仅当 $o\left(h_i\right)\mid q$ 对每个 $i$ 成立.

**基础知识**（有理数乘法群的有限子群）

乘法群 $\mathbb Q^*$ 中任一元素的阶有限当且仅当该元素为 $1$ 或 $-1$, 即 $\mathbb Q^*$ 的唯一有限子群为 $\left\{\pm1\right\}$. 事实上, 若 $r=p/q\in\mathbb Q^*$（既约）满足 $r^n=1$, 则 $p^n=q^n$, 故 $p=\pm q$, 即 $r=\pm1$.

**基础知识**（逆转置矩阵）

设 $P$ 为 $n$ 阶反转矩阵, 即 $P_{i,n+1-i}=1$, 其余元素为 $0$, 则 $P$ 为对称矩阵, $P^2=I_n$, 且 $P^{-1}=P$. 若 $N$ 为 $n$ 阶幂零移位矩阵（即 $N_{i,i+1}=1$, 其余为 $0$）, 则 $PNP=N^T$, 从而 $PN$ 为对称矩阵.

**基础知识**（幂零核与约当块计数）

设 $A$ 为 $n$ 阶方阵, $a$ 为 $A$ 的一个特征值. 记

$$
\begin{aligned}&\quad\;\nu_k\\
&=\dim\ker\left(aI_n-A\right)^k\\
&=n-\mathrm{rank}\left(aI_n-A\right)^k,
\end{aligned}
$$

并约定 $\nu_0=0$. 则 $A$ 的以 $a$ 为特征值、阶数不小于 $s$ 的约当块个数为 $\nu_s-\nu_{s-1}$. 因而序列 $\left\{\nu_k\right\}_{k\geqslant0}$ 完全决定了 $a$ 处约当块的大小与个数.

## 域论

**引理 4.1.9**（域同态必单射）

域同态 $\varphi:F\to E$ 一定是单射. 特别地, 域自同构保持域中运算及 $1$, 因而保持素域（$\mathbb Q$ 或 $\mathbb F_p$）上的所有元素不动.

**定义 4.1.15**（扩张次数）

设 $E$ 为 $F$ 的扩张, $E$ 作为 $F$-线性空间的维数称为 $E$ 对 $F$ 的扩张次数, 记为 $\left[E:F\right]$. 若 $\left[E:F\right]< \infty$, 称 $E$ 为 $F$ 的有限扩张; 否则称 $E$ 为 $F$ 的无限扩张.

**定理 4.1.16**（扩张次数的望远镜法则）

若 $K/F$ 与 $E/K$ 都是有限扩张, 则 $E/F$ 也是有限扩张, 且 $\left[E:F\right]=\left[E:K\right]\left[K:F\right]$.

**引理 4.2.1**（有限扩张必为代数扩张）

设 $E/F$ 为有限扩张, 则 $E$ 中每个元素都是 $F$ 上的代数元. 换言之, 若 $E$ 中存在 $F$ 上的超越元, 则 $E/F$ 必为无限扩张.

**定理 4.2.13**（单代数扩张的结构）

域 $F$ 的单代数扩张 $F\left(\alpha\right)$ 必同构于 $F\left[x\right]/\left(\mathrm{Irr}\left(\alpha,F\right)\right)$. 设 $\deg\left(\alpha,F\right)=n$, 则 $F\left(\alpha\right)$ 作为 $F$-线性空间的维数为 $n$, 且 $1,\alpha,\alpha^2,\cdots,\alpha^{n-1}$ 为其一组 $F$-基.

**基础知识**（分式域的泛性质）

设 $R$ 为整环, $E$ 为其分式域. 任给 $R$ 的自同构 $\sigma$, 定义映射 $\overline\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\sigma\left(b\right)^{-1}$, 则 $\overline\sigma$ 良定义且为 $E$ 的自同构.

**基础知识**（特征 $p$ 下的弗罗贝尼乌斯映射）

设域 $F$ 的特征为素数 $p$, 则对任意 $a,b\in F$ 有 $\left(a+b\right)^p=a^p+b^p$, 从而 $\left(x-a\right)^p=x^p-a^p$. 因而对任意 $c\in F$, 若 $\alpha$ 是 $x^p-c$ 在某分裂域中的根（即 $\alpha^p=c$）, 则 $x^p-c=\left(x-\alpha\right)^p$, 即 $x^p-c$ 在其分裂域中只有一个 $p$ 重根.
