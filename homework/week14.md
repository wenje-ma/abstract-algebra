# 作业 14

> **定义 2.4.1**（环同态与同构）设 $R_1,R_2$ 为两个环, $f$ 为 $R_1$ 到 $R_2$ 的映射, 若对任何 $a,b\in R_1$ 有 $f\left(a+b\right)=f\left(a\right)+f\left(b\right)$, $f\left(ab\right)=f\left(a\right)f\left(b\right)$, 则称 $f$ 为同态; 单射的同态称为单同态, 满射的同态称为满同态, 双射的同态称为同构.

> **定义 2.2.20**（整环、除环与域）无零因子的交换幺环称为整环; 若幺环 $R$ 满足 $R^*$ 对乘法构成群（$R^*=R\setminus\left\{0\right\}$）, 则称 $R$ 为除环; 交换的除环称为域.

### 习题一

（习题 2.4-6）试求出数域 $\mathbb Q\left[\sqrt{-1}\right]=\left\{a+b\sqrt{-1}\mid a,b\in\mathbb Q\right\}$ 的所有自同构.

### 解答 习题一

记 $i=\sqrt{-1}$. 设 $\varphi:\mathbb Q\left[i\right]\to\mathbb Q\left[i\right]$ 为自同构. 由**定义 2.4.1**（环同态与同构）, $\varphi\left(1\right)=1$, 故 $\varphi$ 在 $\mathbb Q$ 上为恒等映射. 令 $\varphi\left(i\right)=u=a+bi$, $a,b\in\mathbb Q$.

因 $i^2=-1$, 故

$$
\begin{aligned}u^2&=\varphi\left(i\right)^2\\&=\varphi\left(i^2\right)\\&=\varphi\left(-1\right)\\&=-1.\end{aligned}
$$

即 $\left(a+bi\right)^2=a^2-b^2+2abi=-1$. 比较实部、虚部得 $2ab=0$, $a^2-b^2=-1$. 若 $b=0$, 则 $a^2=-1$, 在 $\mathbb Q$ 中无解; 故 $a=0$, $b^2=1$, $b=\pm1$. 于是 $u=i$ 或 $u=-i$.

（1）$\varphi\left(i\right)=i$: 此时 $\varphi\left(a+bi\right)=a+bi$, 即恒等自同构.

（2）$\varphi\left(i\right)=-i$: 此时 $\varphi\left(a+bi\right)=a-bi$, 即复共轭映射.

两者均保持加法与乘法且双射. 故 $\mathbb Q\left[i\right]$ 恰有两个自同构: 恒等映射与共轭映射. $\blacksquare$

### 习题二

（习题 2.4-7）试证明实数域的自同构只有恒等同构.

### 解答 习题二

设 $\varphi:\mathbb R\to\mathbb R$ 为域自同构. 首先 $\varphi$ 保持有理数: $\varphi\left(1\right)=1$, 故 $\varphi\left(n\right)=n$, $\varphi\left(m/n\right)=m/n$.

**保序性** 若 $x>0$, 则存在 $y\ne0$ 使 $x=y^2$, 于是 $\varphi\left(x\right)=\varphi\left(y\right)^2>0$. 因而当 $x>y$ 时, $x-y>0$ 给出 $\varphi\left(x\right)-\varphi\left(y\right)>0$, 即 $\varphi$ 严格递增.

**恒等性** 反设存在 $x$ 使 $\varphi\left(x\right)\ne x$. 若 $\varphi\left(x\right)>x$, 由有理数在 $\mathbb R$ 中的稠密性, 取 $q\in\mathbb Q$ 使 $x<q<\varphi\left(x\right)$. 由 $x<q$ 及 $\varphi$ 递增得 $\varphi\left(x\right)<\varphi\left(q\right)=q$, 与 $q<\varphi\left(x\right)$ 矛盾. 若 $\varphi\left(x\right)<x$, 同理取 $q$ 使 $\varphi\left(x\right)<q<x$, 由 $\varphi$ 递增得 $q=\varphi\left(q\right)<\varphi\left(x\right)$, 矛盾.

故 $\varphi\left(x\right)=x$ 对一切 $x\in\mathbb R$ 成立, 即 $\varphi$ 为恒等同构. $\blacksquare$

### 习题三

（习题 2.4-8）证明: 映射 $a+b\sqrt{-1}\mapsto a-b\sqrt{-1}$ 是环 $\mathbb C$ 的自同构.

### 解答 习题三

记 $\varphi\left(a+bi\right)=a-bi$.

**保加法**

$$
\begin{aligned}\varphi\left(\left(a+bi\right)+\left(c+di\right)\right)&=\varphi\left(\left(a+c\right)+\left(b+d\right)i\right)\\&=\left(a+c\right)-\left(b+d\right)i\\&=\left(a-bi\right)+\left(c-di\right)\\&=\varphi\left(a+bi\right)+\varphi\left(c+di\right).\end{aligned}
$$

**保乘法**

$$
\begin{aligned}\varphi\left(\left(a+bi\right)\left(c+di\right)\right)&=\varphi\left(\left(ac-bd\right)+\left(ad+bc\right)i\right)\\&=\left(ac-bd\right)-\left(ad+bc\right)i,\end{aligned}
$$

而

$$
\begin{aligned}\varphi\left(a+bi\right)\varphi\left(c+di\right)&=\left(a-bi\right)\left(c-di\right)\\&=ac-bd-\left(ad+bc\right)i.\end{aligned}
$$

两者相等. 又连续两次作用后回到自身, 即 $\varphi$ 为双射. 由**定义 2.4.1**（环同态与同构）, $\varphi$ 是 $\mathbb C$ 的自同构. $\blacksquare$

### 习题四

（习题 2.4-19）本题证明整环的分式域的存在性和唯一性. 设整环 $R$ 为域 $F$ 的子环, 若对任何 $a\in F$, 存在 $b,c\in R$ 使得 $a=bc^{-1}$, 则称 $F$ 为 $R$ 的分式域. 在集合 $R\times R^*$ 上定义加法与乘法如下:

$$
\left(a,b\right)+\left(c,d\right)=\left(ad+bc,bd\right).
$$

$$
\left(a,b\right)\left(c,d\right)=\left(ac,bd\right),
$$

其中 $\left(a,b\right),\left(c,d\right)\in R\times R^*$.
（1）证明 $R\times R^*$ 对于上述加法与乘法都成为交换幺半群, 其单位元分别是 $\left(0,1\right)$, $\left(1,1\right)$;
（2）在 $R\times R^*$ 中定义关系 $\left(a,b\right)\sim\left(c,d\right)$ 当且仅当 $ad=bc$. 证明 $\sim$ 是一个等价关系, 且对于上述乘法和加法都是同余关系;
（3）令 $F=\left(R\times R^*\right)/\sim$ 为等价类的集合, 将 $\left(a,b\right)$ 所在的类记为 $a/b$. 在 $F$ 上定义

$$
\frac{a}{b}+\frac{c}{d}=\frac{ad+bc}{bd}.
$$

$$
\frac{a}{b}\cdot\frac{c}{d}=\frac{ac}{bd}.
$$

证明 $F$ 对于上述加法与乘法成为一个域;
（4）试证明 $R$ 到 $F$ 的映射 $a\mapsto a/1$ 是单同态, 因此可以把 $R$ 看成 $F$ 的子环, 由此证明 $F$ 是 $R$ 的一个分式域;
（5）设 $K$ 是包含 $R$ 的域, 试证明 $K$ 包含一个子域 $F_2$, $F_2\supseteq R$, 且 $F_2$ 是 $R$ 的分式域, 从而分式域是包含 $R$ 的最小域.

### 解答 习题四

（1）因 $R$ 为整环, $b,d\ne0$ 时 $bd\ne0$, 故上述运算封闭. 加法与乘法的交换律、结合律可由 $R$ 中相应运算直接验证. 对加法, $\left(a,b\right)+\left(0,1\right)=\left(a,b\right)$; 对乘法, $\left(a,b\right)\left(1,1\right)=\left(a,b\right)$. 故二者分别是以 $\left(0,1\right)$, $\left(1,1\right)$ 为单位元的交换幺半群.

（2）**等价关系** 自反: $ab=ba$. 对称: $ad=bc$ 即 $bc=ad$. 传递: 设 $\left(a,b\right)\sim\left(c,d\right)$, $\left(c,d\right)\sim\left(e,f\right)$, 则 $ad=bc$, $cf=de$. 两式分别乘 $f$ 与 $b$ 得 $adf=bcf=bde$, 由 $d\ne0$ 消去得 $af=be$, 故 $\left(a,b\right)\sim\left(e,f\right)$.

**同余关系** 设 $\left(a,b\right)\sim\left(a',b'\right)$, $\left(c,d\right)\sim\left(c',d'\right)$, 即 $ab'=a'b$, $cd'=c'd$. 则

$$
\left(ab'\right)\left(cd'\right)=\left(a'b\right)\left(c'd\right),
$$

即 $ac\cdot b'd'=bd\cdot a'c'$, 故 $\left(a,b\right)\left(c,d\right)\sim\left(a',b'\right)\left(c',d'\right)$. 加法同理:

$$
\begin{aligned}\left(ad+bc\right)b'd'&=ab'dd'+cd'bb'\\&=a'bdd'+c'dbb'\\&=bd\left(a'd'+b'c'\right),\end{aligned}
$$

故和亦等价. 因而运算在等价类上定义合理.

（3）由（2）, $F$ 上运算合理, 且保持交换律、结合律、分配律. $0/1$ 为零元, $1/1$ 为幺元. $a/b$ 的负元为 $\left(-a\right)/b$. 若 $a/b\ne0/1$, 则 $a\ne0$（否则 $\left(a,b\right)\sim\left(0,1\right)$ 即 $a=0$）, 其逆元为 $b/a$. 故 $F$ 是交换幺环且每个非零元可逆. 由**定义 2.2.20**（整环、除环与域）, $F$ 为域.

（4）作 $\iota:R\to F$, $\iota\left(a\right)=a/1$. 则

$$
\begin{aligned}\iota\left(a+b\right)&=\frac{a+b}{1}\\&=\frac{a}{1}+\frac{b}{1}\\&=\iota\left(a\right)+\iota\left(b\right),\end{aligned}
$$

$$
\begin{aligned}\iota\left(ab\right)&=\frac{ab}{1}\\&=\frac{a}{1}\cdot\frac{b}{1}\\&=\iota\left(a\right)\iota\left(b\right).\end{aligned}
$$

且 $a/1=0/1$ 当且仅当 $a=0$, 故 $\iota$ 为单同态. 由此可把 $R$ 等同于 $\iota\left(R\right)\subseteq F$. 对任意 $a/b\in F$, 有 $a/b=\left(a/1\right)\left(b/1\right)^{-1}$, 即 $F$ 中每一元均可写为 $R$ 中两元之商, 故 $F$ 是 $R$ 的分式域.

（5）在 $K$ 中令

$$
F_2=\left\{ab^{-1}\mid a,b\in R,\;b\ne0\right\}.
$$

$F_2$ 对加、减、乘封闭, 且非零元 $ab^{-1}$ 的逆为 $ba^{-1}$, 故 $F_2$ 是 $K$ 的子域. 又 $a=a\cdot1^{-1}\in F_2$, 故 $R\subseteq F_2$. 任何包含 $R$ 的域都必须含有所有 $ab^{-1}$, 因而必包含 $F_2$. 故 $F_2$ 是包含 $R$ 的最小域, 即 $R$ 的分式域. $\blacksquare$
