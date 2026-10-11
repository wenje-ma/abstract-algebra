# 作业 3

> **定义 1.3.1**（正规子群）设 $H$ 是群 $G$ 的子群. 如果对任意 $g\in G$, $h\in H$, 有 $ghg^{-1}\in H$, 则称 $H$ 为 $G$ 的一个正规子群, 记为 $H\triangleleft G$.

> **定理 1.3.5**（正规子群的等价条件）
>
> 设 $G$ 是群, $H<G$, 则下列条件等价:
>
> （1）$H\triangleleft G$;
>
> （2）对任意 $g\in G$, $gH=Hg$;
>
> （3）对任意 $a,b\in G$, $aH\cdot bH=abH$.

> **定理 1.3.6**（商群）设 $G$ 是群, $H\triangleleft G$, 则 $G/H$ 对陪集乘法 $aH\cdot bH=abH$ 构成一个群, 称为 $G$ 对 $H$ 的商群.

> **基础知识**（共轭元素与共轭类）称 $G$ 中的两个元素 $a,b$ 是共轭的, 如果存在 $g\in G$ 使得 $b=gag^{-1}$. 与 $a$ 共轭的所有元素的全体称为 $a$ 的共轭类.

> **基础知识**（子群乘积）设 $H,K$ 是群 $G$ 的子群, 则 $HK=\left\{hk\mid h\in H,k\in K\right\}$. $HK$ 是 $G$ 的子群当且仅当 $HK=KH$.

### 习题一

（习题 1.3-7）证明: 群 $G$ 中元素的共轭关系是一个等价关系, 从而共轭类构成了 $G$ 的一个划分.

### 解答 习题一

定义 $G$ 上的关系 $R$: $aRb$ 当且仅当存在 $g\in G$ 使得 $b=gag^{-1}$, 即 $a,b$ 共轭. 下面验证等价关系的三个条件.

**反身性** 对任意 $a\in G$, 取 $g=e$, 则 $a=eae^{-1}$, 故 $aRa$.

**对称性** 若 $aRb$, 即存在 $g\in G$ 使 $b=gag^{-1}$, 则 $a=g^{-1}bg=g^{-1}b\left(g^{-1}\right)^{-1}$, 故 $bRa$.

**传递性** 若 $aRb$, $bRc$, 即存在 $g,h\in G$ 使 $b=gag^{-1}$, $c=hbh^{-1}$, 则

$$
\begin{aligned}c&=hbh^{-1}\\&=h\left(gag^{-1}\right)h^{-1}\\&=\left(hg\right)a\left(hg\right)^{-1},\end{aligned}
$$

故 $aRc$.

因此共轭关系是等价关系. 由等价关系的一般理论, $G$ 划分为互不相交的共轭类之并. $\blacksquare$

### 习题二

（习题 1.3-9）设 $H,K$ 是群 $G$ 的两个子群. 证明: $H,K$ 中有一个是 $G$ 的正规子群, 则 $HK<G$; 若 $H,K$ 均是 $G$ 的正规子群, 则 $HK\triangleleft G$.

### 解答 习题二

先证 $H,K$ 中有一个正规则 $HK<G$. 不妨设 $H\triangleleft G$.

由**定理 1.3.5**（正规子群的等价条件）, 对任意 $k\in K$ 有 $kH=Hk$. 于是

$$
\begin{aligned}KH&=\bigcup_{k\in K}kH\\&=\bigcup_{k\in K}Hk\\&=HK,\end{aligned}
$$

即 $HK=KH$. 由**基础知识**（子群乘积）, $HK<G$.

再证 $H,K$ 均正规则 $HK\triangleleft G$.

由上述, $HK<G$. 下证正规性. 对任意 $g\in G$, $hk\in HK$, 有

$$
\begin{aligned}g\left(hk\right)g^{-1}&=\left(ghg^{-1}\right)\left(gkg^{-1}\right).\end{aligned}
$$

因 $H\triangleleft G$, 故 $ghg^{-1}\in H$; 因 $K\triangleleft G$, 故 $gkg^{-1}\in K$. 因此 $g\left(hk\right)g^{-1}\in HK$. 由 $g,hk$ 的任意性, $g\left(HK\right)g^{-1}\subseteq HK$. 由**定义 1.3.1**（正规子群）, $HK\triangleleft G$. $\blacksquare$

### 习题三

（习题 1.3-10）若群 $G$ 只有一个阶为 $m$ 的子群 $H$, 证明: $H\triangleleft G$.

### 解答 习题三

对任意 $g\in G$, 考虑共轭子群 $gHg^{-1}$.

首先, $gHg^{-1}$ 是 $G$ 的子群. 事实上, 映射

$$
\varphi:H\to gHg^{-1},\  h\mapsto ghg^{-1}
$$

是双射（其逆为 $x\mapsto g^{-1}xg$）, 且保持乘法运算: $\varphi\left(h_{1}h_{2}\right)=gh_{1}h_{2}g^{-1}=\left(gh_{1}g^{-1}\right)\left(gh_{2}g^{-1}\right)=\varphi\left(h_{1}\right)\varphi\left(h_{2}\right)$. 故 $gHg^{-1}<G$.

其次, 由 $\varphi$ 是双射, $\left|gHg^{-1}\right|=\left|H\right|=m$.

因 $G$ 中只有一个阶为 $m$ 的子群, 故 $gHg^{-1}=H$.

由**定理 1.3.5**（正规子群的等价条件）, $H\triangleleft G$. $\blacksquare$
