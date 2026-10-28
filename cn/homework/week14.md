# week14

> **基础知识: 环自同构固定素域**<br>设 $\varphi$ 是域 (或含 $1$ 的环) 的自同构, 则 $\varphi\left(1\right)=1$, 故 $\varphi$ 保持加法与乘法且把 $1$ 映到 $1$, 因而 $\varphi$ 在有理数域 $\mathbb Q$ 上为恒等映射.

> **基础知识: 实数域的保序性**<br>实数 $x>0$ 当且仅当存在 $y\ne0$ 使 $x=y^{2}$. 故域自同构 $\varphi:\mathbb R\to\mathbb R$ 把正数映为正数, 从而严格递增; 且有理数在 $\mathbb R$ 中稠密.

> **基础知识: 整环的无零因子**<br>整环无零因子, 故若 $b,d\ne0$ 则 $bd\ne0$; 且由 $d\ne0$ 与 $d\left(af-be\right)=0$ 可推出 $af=be$.

> **基础知识: 同余关系与商结构**<br>若等价关系 $\sim$ 对某运算为同余关系, 则该运算在商集合上有定义, 且相应的交换律,结合律,分配律随之保持.

> **基础知识: 域中逆元**<br>域中非零元可逆; 若 $a,b\ne0$, 则 $\left(ab^{-1}\right)^{-1}=ba^{-1}$.

> **定义 2.2.20 (整环,除环与域)**<br>无零因子的交换幺环称为整环; 若幺环 $R$ 满足 $R^{*}$ 对乘法构成群 (其中 $R^{*}=R\setminus\left\{0\right\}$), 则称 $R$ 为除环; 交换的除环称为域.

> **定义 2.4.1 (环同态与同构)**<br>设 $R_1,R_2$ 为两个环, $f$ 为 $R_1$ 到 $R_2$ 的映射. 若对任何 $a,b\in R_1$ 有 $f\left(a+b\right)=f\left(a\right)+f\left(b\right)$ 且 $f\left(ab\right)=f\left(a\right)f\left(b\right)$, 则称 $f$ 为同态; 单射的同态称为单同态, 满射的同态称为满同态, 双射的同态称为同构.

---

## 2.4-6

试求出数域

$$
\mathbb Q\left[\sqrt{-1}\right]=\left\{a+b\sqrt{-1}\mid a,b\in\mathbb Q\right\}
$$

的所有自同构.

### 解答 2.4-6

记 $i=\sqrt{-1}$. 设 $\varphi:\mathbb Q\left[i\right]\to\mathbb Q\left[i\right]$ 为环的自同构. 由**定义 2.4.1 (环同态与同构)**, $\varphi$ 保持乘法与加法; 又 $\varphi\left(1\right)=1$, 由**基础知识: 环自同构固定素域**, $\varphi$ 在 $\mathbb Q$ 上为恒等映射.

令 $\varphi\left(i\right)=u=a+bi$, $a,b\in\mathbb Q$. 因 $i^{2}=-1$, 且 $\varphi$ 保持乘法与加法,

$$
u^{2}=\varphi\left(i\right)^{2}=\varphi\left(i^{2}\right)=\varphi\left(-1\right)=-1.
$$

即

$$
\left(a+bi\right)^{2}=a^{2}-b^{2}+2abi=-1.
$$

比较实部与虚部得 $2ab=0$ 且 $a^{2}-b^{2}=-1$. 若 $b=0$, 则 $a^{2}=-1$, 在 $\mathbb Q$ 中无解; 故 $a=0$, $b^{2}=1$, $b=\pm1$. 于是 $u=i$ 或 $u=-i$.

情况一 $\varphi\left(i\right)=i$: 此时对 $a,b\in\mathbb Q$, $\varphi\left(a+bi\right)=a+bi$, 即恒等自同构.

情况二 $\varphi\left(i\right)=-i$: 此时 $\varphi\left(a+bi\right)=a-bi$, 即复共轭映射.

这两种映射均保持加法与乘法 (复共轭保持 $\mathbb Q$ 上的运算) 且为双射, 由**定义 2.4.1 (环同态与同构)** 均为自同构. 故 $\mathbb Q\left[i\right]$ 恰有两个自同构: 恒等映射与共轭映射. $\blacksquare$

---

## 2.4-7

试证明实数域的自同构只有恒等同构.

### 解答 2.4-7

设 $\varphi:\mathbb R\to\mathbb R$ 为域自同构. 由**定义 2.4.1 (环同态与同构)** 与**基础知识: 环自同构固定素域**, $\varphi\left(1\right)=1$, 故 $\varphi$ 在 $\mathbb Q$ 上恒等: $\varphi\left(n\right)=n$ 对整数 $n$, 且 $\varphi\left(m/n\right)=m/n$ 对 $\frac{m}{n}\in\mathbb Q$.

**保序性**: 若 $x>0$, 由**基础知识: 实数域的保序性**, 存在 $y\ne0$ 使 $x=y^{2}$; 则

$$
\varphi\left(x\right)=\varphi\left(y^{2}\right)=\varphi\left(y\right)^{2}>0
$$

(因 $\varphi\left(y\right)\ne0$, 平方为正). 因而当 $x>y$ 时, $x-y>0$ 给出 $\varphi\left(x\right)-\varphi\left(y\right)=\varphi\left(x-y\right)>0$, 即 $\varphi$ 严格递增.

**恒等性**: 反设存在 $x\in\mathbb R$ 使 $\varphi\left(x\right)\ne x$. 若 $\varphi\left(x\right)>x$, 由**基础知识: 实数域的保序性** (有理数稠密), 取 $q\in\mathbb Q$ 使 $x<q<\varphi\left(x\right)$. 由 $x<q$ 及 $\varphi$ 严格递增, $\varphi\left(x\right)<\varphi\left(q\right)=q$, 与 $q<\varphi\left(x\right)$ 矛盾. 若 $\varphi\left(x\right)<x$, 同理取 $q\in\mathbb Q$ 使 $\varphi\left(x\right)<q<x$; 由 $\varphi$ 严格递增及 $q=\varphi\left(q\right)$, 得 $q<\varphi\left(x\right)$, 矛盾.

故 $\varphi\left(x\right)=x$ 对一切 $x\in\mathbb R$ 成立, 即 $\varphi$ 为恒等同构. $\blacksquare$

---

## 2.4-8

证明: 映射 $a+b\sqrt{-1}\mapsto a-b\sqrt{-1}$ 是环 $\mathbb C$ 的自同构.

### 解答 2.4-8

记 $\varphi:\mathbb C\to\mathbb C$, $\varphi\left(a+bi\right)=a-bi$, 其中 $a,b\in\mathbb R$.

**保加法**: 对 $a+bi$, $c+di\in\mathbb C$,

$$
\varphi\left(\left(a+bi\right)+\left(c+di\right)\right)=\varphi\left(\left(a+c\right)+\left(b+d\right)i\right)=\left(a+c\right)-\left(b+d\right)i=\left(a-bi\right)+\left(c-di\right)=\varphi\left(a+bi\right)+\varphi\left(c+di\right).
$$

**保乘法**: 

$$
\varphi\left(\left(a+bi\right)\left(c+di\right)\right)=\varphi\left(\left(ac-bd\right)+\left(ad+bc\right)i\right)=\left(ac-bd\right)-\left(ad+bc\right)i,
$$

而

$$
\varphi\left(a+bi\right)\varphi\left(c+di\right)=\left(a-bi\right)\left(c-di\right)=ac-bd-\left(ad+bc\right)i.
$$

两者相等, 故 $\varphi$ 保持乘法.

又连续两次作用后回到自身, 即 $\varphi\circ\varphi=\mathrm{id}$, 故 $\varphi$ 为双射. 由**定义 2.4.1 (环同态与同构)**, $\varphi$ 是 $\mathbb C$ 的自同构. $\blacksquare$

---

## 2.4-19

本题证明整环的分式域的存在性和唯一性. 设整环 $R$ 为域 $F$ 的子环, 若对任何 $a\in F$, 存在 $b,c\in R$ 使得 $a=bc^{-1}$, 则称 $F$ 为 $R$ 的分式域. 在集合 $R\times R^{*}$ 上定义加法与乘法如下:

$$
\left(a,b\right)+\left(c,d\right)=\left(ad+bc,bd\right),
$$

$$
\left(a,b\right)\left(c,d\right)=\left(ac,bd\right),
$$

其中 $\left(a,b\right),\left(c,d\right)\in R\times R^{*}$.

(1) 证明 $R\times R^{*}$ 对于上述加法与乘法都成为交换幺半群, 其单位元分别是 $\left(0,1\right)$, $\left(1,1\right)$;

(2) 在 $R\times R^{*}$ 中定义关系 $\left(a,b\right)\sim\left(c,d\right)$ 当且仅当 $ad=bc$. 证明 $\sim$ 是一个等价关系, 且对于上述乘法和加法都是同余关系;

(3) 令 $F=\left(R\times R^{*}\right)/\sim$ 为等价类的集合, 将 $\left(a,b\right)$ 所在的类记为 $a/b$. 在 $F$ 上定义

$$
\frac{a}{b}+\frac{c}{d}=\frac{ad+bc}{bd},
$$

$$
\frac{a}{b}\cdot\frac{c}{d}=\frac{ac}{bd}.
$$

证明 $F$ 对于上述加法与乘法成为一个域;

(4) 试证明 $R$ 到 $F$ 的映射 $a\mapsto a/1$ 是单同态, 因此可以把 $R$ 看成 $F$ 的子环, 由此证明 $F$ 是 $R$ 的一个分式域;

(5) 设 $K$ 是包含 $R$ 的域, 试证明 $K$ 包含一个子域 $F_2$, $F_2\supseteq R$, 且 $F_2$ 是 $R$ 的分式域, 从而分式域是包含 $R$ 的最小域.

### 解答 2.4-19

**第 (1) 部分.** 因 $R$ 为整环, 由**基础知识: 整环的无零因子**, 当 $b,d\ne0$ 时 $bd\ne0$, 故 $R\times R^{*}$ 对加法与乘法封闭. 交换律与结合律由 $R$ 中相应运算的交换律,结合律逐分量直接验证. 对加法, $\left(a,b\right)+\left(0,1\right)=\left(a\cdot1+b\cdot0,b\cdot1\right)=\left(a,b\right)$; 对乘法, $\left(a,b\right)\left(1,1\right)=\left(a\cdot1,b\cdot1\right)=\left(a,b\right)$. 故二者分别是以 $\left(0,1\right)$, $\left(1,1\right)$ 为单位元的交换幺半群.

**第 (2) 部分. 等价关系**: 自反: $\left(a,b\right)\sim\left(a,b\right)$ 即 $ab=ba$, 成立. 对称: $ad=bc$ 即 $bc=ad$, 故 $\left(a,b\right)\sim\left(c,d\right)$ 蕴含 $\left(c,d\right)\sim\left(a,b\right)$. 传递: 设 $\left(a,b\right)\sim\left(c,d\right)$, $\left(c,d\right)\sim\left(e,f\right)$, 即 $ad=bc$, $cf=de$. 两式分别乘 $f$ 与 $b$ 得 $adf=bcf=bde$, 即 $d\left(af\right)=d\left(be\right)$; 因 $d\ne0$, 由**基础知识: 整环的无零因子** 消去得 $af=be$, 故 $\left(a,b\right)\sim\left(e,f\right)$. 故 $\sim$ 为等价关系.

**同余关系 (乘法)**: 设 $\left(a,b\right)\sim\left(a',b'\right)$, $\left(c,d\right)\sim\left(c',d'\right)$, 即 $ab'=a'b$, $cd'=c'd$. 则

$$
\left(ab'\right)\left(cd'\right)=\left(a'b\right)\left(c'd\right),
$$

即 $ac\cdot b'd'=bd\cdot a'c'$, 故

$$
\left(a,b\right)\left(c,d\right)=\left(ac,bd\right)\sim\left(a'c',b'd'\right)=\left(a',b'\right)\left(c',d'\right).
$$

**同余关系 (加法)**: 同上有

$$
\left(ad+bc\right)b'd'=ab'dd'+cd'bb'=a'bdd'+c'dbb'=bd\left(a'd'+b'c'\right),
$$

故 $\left(ad+bc,bd\right)\sim\left(a'd'+b'c',b'd'\right)$, 即 $\left(a,b\right)+\left(c,d\right)\sim\left(a',b'\right)+\left(c',d'\right)$. 故 $\sim$ 对乘法与加法均为同余关系.

**第 (3) 部分.** 由第 (2) 部分与**基础知识: 同余关系与商结构**, $F$ 上加法与乘法定义合理, 且保持交换律,结合律,分配律. $0/1$ 为加法零元, $1/1$ 为乘法幺元. $a/b$ 的负元为 $\left(-a\right)/b$, 因为 $\frac{a}{b}+\frac{-a}{b}=\frac{ab-ab}{b\cdot b}=\frac{0}{b^{2}}=\frac{0}{1}$. 若 $a/b\ne0/1$, 则 $a\ne0$ (否则 $\left(a,b\right)\sim\left(0,1\right)$ 即 $a\cdot1=b\cdot0$, $a=0$); 此时由**基础知识: 域中逆元**, 其乘法逆元为 $b/a$, 因为 $\frac{a}{b}\cdot\frac{b}{a}=\frac{ab}{ab}=\frac{1}{1}$. 故 $F$ 是交换幺环且每个非零元可逆. 由**定义 2.2.20 (整环,除环与域)**, $F$ 为域.

**第 (4) 部分.** 作映射 $\iota:R\to F$, $\iota\left(a\right)=a/1$. 则

$$
\iota\left(a+b\right)=\frac{a+b}{1}=\frac{a}{1}+\frac{b}{1}=\iota\left(a\right)+\iota\left(b\right),
$$

$$
\iota\left(ab\right)=\frac{ab}{1}=\frac{a}{1}\cdot\frac{b}{1}=\iota\left(a\right)\iota\left(b\right),
$$

且 $a/1=0/1$ 当且仅当 $a\cdot1=1\cdot0$, 即 $a=0$, 故 $\iota$ 为单同态 (由**定义 2.4.1 (环同态与同构)**). 由此可把 $R$ 等同于 $\iota\left(R\right)\subseteq F$. 对任意 $a/b\in F$, 有 $a/b=\left(a/1\right)\left(b/1\right)^{-1}$, 即 $F$ 中每一元均可写为 $R$ (经 $\iota$ 嵌入) 中两元之商, 故 $F$ 是 $R$ 的分式域 (按题中定义).

**第 (5) 部分.** 在 $K$ 中令

$$
F_2=\left\{ab^{-1}\mid a,b\in R,\;b\ne0\right\}.
$$

$F_2$ 对加法封闭 ($ab^{-1}+cd^{-1}=\left(ad+bc\right)\left(bd\right)^{-1}$, 其中 $ad+bc,bd\in R$ 且 $bd\ne0$ 由**基础知识: 整环的无零因子**), 对乘法封闭 ($\left(ab^{-1}\right)\left(cd^{-1}\right)=\left(ac\right)\left(bd\right)^{-1}$), 且非零元 $ab^{-1}$ ($a\ne0$) 的逆为 $\left(ab^{-1}\right)^{-1}=ba^{-1}\in F_2$ (由**基础知识: 域中逆元**). 故 $F_2$ 是 $K$ 的子域. 又 $a=a\cdot1^{-1}\in F_2$, 故 $R\subseteq F_2$. 任何包含 $R$ 的域都必须含有所有 $ab^{-1}$ ($a,b\in R$, $b\ne0$), 因而必包含 $F_2$. 故 $F_2$ 是包含 $R$ 的最小域, 即 $R$ 的分式域. $\blacksquare$
