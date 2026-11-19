# week3

> **定理 1.2.22 (拉格朗日定理)**
> 
> 设 $G$ 是有限群, $H<{}G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, 其中 $\left[G:H\right]$ 为 $H$ 在 $G$ 中的指数. 从而子群 $H$ 的阶是群 $G$ 的阶的因子, 特别地, 任何元素的阶也是 $\left|G\right|$ 的因子.

> **定理 1.4.10 (凯莱定理)**
> 
> 任何群 $G$ 与对称群 $S_G$ 的一个子群同构; 事实上映射 $L:G\to{L}_G$, $a\mapsto{L}_a$ 是单同态.

> **引理 1.4.13**
> 
> 设 $f:G\to{G}'$ 为群同态, 则 $\mathrm{Im}\,f<{}G'$, $\ker{f}\triangleleft{G}$.

> **例 1.4.17**
> 
> 设 $V$ 是数域 $P$ 上的 $n$ 维线性空间, 则映射 $\det\circ\pi:S_n\to{P}^{*}$, $\sigma\mapsto\det\left(\pi_\sigma\right)$ 是群同态, 其像集为 $\left\{1,-1\right\}$ (当 $n>1$ 时), 该同态的核记为 $A_n$.

> **定理 1.4.19 (群的同态基本定理)**
> 
> 设 $f:G\to{G}'$ 是群的满同态, 则 $G/\ker{f}\cong{G}'$.

> **定理 1.5.5 (循环群的分类)**
> 
> 设 $G$ 是循环群. 若 $G$ 是无限群, 则 $G$ 与 $\left(\mathbb{Z},+\right)$ 同构; 若 $G$ 是 $n$ 阶群, 则 $G$ 与 $\left(\mathbb{Z}_n,+\right)$ 同构. 从而, 两个循环群同构当且仅当它们有相同的阶.

> **定义 1.6.1 (轮换)**
> 
> 设 $\left\{i_1,i_2,\cdots,i_r\right\}\subseteq\left\{1,2,\cdots,n\right\}$. 若 $\sigma\in{S}_n$ 满足 $\sigma\left(i_1\right)=i_2$, $\sigma\left(i_2\right)=i_3$, ..., $\sigma\left(i_r\right)=i_1$, 且 $\sigma$ 固定其余文字, 则称 $\sigma$ 为一个 $r$-轮换, 记为 $\sigma=\left(i_1i_2\cdots{i}_r\right)$. 特别地, $2$-轮换称为对换.

> **命题 1.6.8**
> 
> 任一 $n$ 元置换都可以表为一些对换的乘积.

> **定理 1.6.9 (交错群的单性)**
> 
> 当 $n\ge5$ 时, $A_n$ 是单群.

## 1.5-16

设有限群 $G$ 的不同子群有不同的阶, 证明: $G$ 是循环群.

### 解答 1.5-16

设 $\left|G\right|=n$. 由题设, 对每个正整数 $d$, $G$ 中至多有一个 $d$ 阶子群 (若有两个 $d$ 阶子群, 则其阶相同, 与题设矛盾). 对每个 $d\mid{n}$, 令 $f\left(d\right)$ 为 $G$ 中阶恰为 $d$ 的元素的个数.

断言: 对每个 $d\mid{n}$, $f\left(d\right)\le\varphi\left(d\right)$. 若 $f\left(d\right)=0$, 断言显然. 若 $f\left(d\right)>0$, 取 $a\in{G}$ 使 $a$ 的阶为 $d$, 则 $\left\langle{a}\right\rangle$ 是 $G$ 的 $d$ 阶循环子群. 由题设, $G$ 中至多有一个 $d$ 阶子群, 故 $G$ 中任意 $d$ 阶元 $b$ 都满足 $\left\langle{b}\right\rangle=\left\langle{a}\right\rangle$, 即 $b$ 是 $d$ 阶循环群 $\left\langle{a}\right\rangle$ 的生成元. 由循环群的生成元个数, $d$ 阶循环群中恰有 $\varphi\left(d\right)$ 个生成元, 故 $f\left(d\right)=\varphi\left(d\right)\le\varphi\left(d\right)$. 断言得证.

由**定理 1.2.22 (拉格朗日定理)**, $G$ 中每个元素的阶都整除 $n$, 故 $G$ 中每个元素都恰好落入某个 $d\mid{n}$ 的计数 $f\left(d\right)$ 中, 即

$$
n=\left|G\right|=\sum_{d\mid{n}}f\left(d\right).
$$

又由欧拉函数与整除恒等式, $\sum_{d\mid{n}}\varphi\left(d\right)=n$. 结合上述断言,

$$
n=\sum_{d\mid{n}}f\left(d\right)\le\sum_{d\mid{n}}\varphi\left(d\right)=n.
$$

上式两端相等, 故对每个 $d\mid{n}$ 必有 $f\left(d\right)=\varphi\left(d\right)$.

特别地, $f\left(n\right)=\varphi\left(n\right)>0$, 故 $G$ 中存在 $n$ 阶元 $a$, 从而 $G=\left\langle{a}\right\rangle$ 是循环群.

$\blacksquare$

## 1.6-5

证明:

$$
S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle=\left\langle\left(12\right),\left(12\cdots{n}\right)\right\rangle,\quad{A}_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle.
$$

### 解答 1.6-5

第一部分: 证明 $S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$. 由**命题 1.6.8**, $S_n$ 由所有对换生成. 对任意对换 $\left(ij\right)$, 其中 $i\ne1$, $j\ne1$, 由**定义 1.6.1 (轮换)**的共轭, 取 $\sigma=\left(1i\right)$, 有 $\left(1i\right)\left(1j\right)\left(1i\right)=\left(\sigma\left(1\right)\sigma\left(j\right)\right)=\left(i,j\right)=\left(ij\right)$. 故任意对换 $\left(ij\right)$ 都可由 $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ 表出, 因此 $S_n\subseteq\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$; 反向包含显然, 故 $S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$.

第二部分: 证明 $S_n=\left\langle\left(12\right),\left(12\cdots{n}\right)\right\rangle$. 记 $\sigma=\left(12\cdots{n}\right)$. 由轮换的共轭, 对 $k=1,2,\cdots,n-1$,

$$
\sigma^{k-1}\left(12\right)\sigma^{-\left(k-1\right)}=\left(\sigma^{k-1}\left(1\right)\sigma^{k-1}\left(2\right)\right)=\left(k,k+1\right),
$$

故相邻对换 $\left(12\right),\left(23\right),\cdots,\left(n-1,n\right)$ 均属于 $\left\langle\left(12\right),\sigma\right\rangle$. 而相邻对换生成 $S_n$ (由**命题 1.6.8**, 任何对换 $\left(ij\right)$ 可表为相邻对换之积), 故 $S_n\subseteq\left\langle\left(12\right),\sigma\right\rangle$; 反向包含显然, 故 $S_n=\left\langle\left(12\right),\left(12\cdots{n}\right)\right\rangle$.

第三部分: 证明 $A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$. 由交错群由 3-轮换生成, $A_n$ 由所有 3-轮换生成. 下面证明任意 3-轮换都属于 $\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$.

(1) 含 $1$ 和 $2$ 的 3-轮换即为 $\left(12k\right)$ 或其逆, 已在生成集中.

(2) 含 $1$ 但不含 $2$ 的 3-轮换 $\left(1jk\right)$ ($j,k\ne2$): 直接计算 $\left(12k\right)\left(12j\right)^{-1}=\left(12k\right)\left(1j2\right)=\left(1jk\right)$, 故 $\left(1jk\right)$ 属于生成群.

(3) 不含 $1$ 的 3-轮换 $\left(ijk\right)$: 由 (2), $\left(1ij\right)$ 与 $\left(1ik\right)$ 均属于生成群, 于是 $\left(1ij\right)^{-1}\left(1ik\right)=\left(1ji\right)\left(1ik\right)=\left(ikj\right)$. 因 $\left(ikj\right)=\left(ijk\right)^{-1}$, 故 $\left(ijk\right)$ 属于生成群.

故所有 3-轮换都属于 $\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$, 从而 $A_n\subseteq\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$. 反之, 各生成元 $\left(12k\right)$ 都是 3-轮换, 是偶置换 (偶置换与奇置换, 交错群), 故属于 $A_n$, 反向包含成立. 因此 $A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$.

$\blacksquare$

## 1.6-6

证明: $S_n$ 的非平凡正规子群为 $A_n$ 或 $K_4$ (当 $n=4$ 时).

### 解答 1.6-6

设 $N\triangleleft{S}_n$, $N\ne\left\{e\right\}$, $N\ne{S}_n$.

情形 $n\ge5$. 由**定理 1.6.9 (交错群的单性)**, $A_n$ 是单群. 因 $N\triangleleft{S}_n$ 且 $A_n\triangleleft{S}_n$ (由偶置换与奇置换, 交错群), 交 $N\cap{A}_n\triangleleft{A}_n$, 故由 $A_n$ 的单性, $N\cap{A}_n=\left\{e\right\}$ 或 $A_n$.

若 $N\cap{A}_n=A_n$, 则 $A_n\subseteq{N}$. 因 $\left|A_n\right|=\frac{n!}{2}$, $A_n$ 在 $S_n$ 中的指数为 $2$ (偶置换与奇置换, 交错群), 故包含 $A_n$ 的子群只能是 $A_n$ 或 $S_n$; 而 $N\ne{S}_n$, 故 $N=A_n$.

若 $N\cap{A}_n=\left\{e\right\}$, 则对任意 $x,y\in{N}\setminus\left\{e\right\}$, 因 $x,y$ 都是奇置换, $xy$ 是偶置换, 故 $xy\in{N}\cap{A}_n=\left\{e\right\}$, 于是 $y=x^{-1}$, 即 $\left|N\right|\le2$, 且 $N$ 的非单位元是二阶元. 又由正规子群是共轭类的并, $N$ 是若干共轭类之并; 因 $n\ge3$ 时 $S_n$ 的中心平凡 (群的中心与内自同构), $N$ 的非单位元 $x\ne{e}$ 所在的共轭类大小大于 $1$, 与 $\left|N\right|\le2$ 矛盾. 故 $N\cap{A}_n=\left\{e\right\}$ 不可能.

因此 $n\ge5$ 时, $S_n$ 的非平凡正规子群只有 $A_n$.

情形 $n=4$. $\left|S_4\right|=24$, $\left|A_4\right|=12$, $A_4\triangleleft{S}_4$. 由$S_4$ 的共轭类, $S_4$ 的共轭类大小分别为 $1,6,3,8,6$; 由正规子群是共轭类的并及**定理 1.2.22 (拉格朗日定理)**, 正规子群的阶必为若干共轭类大小之和且整除 $24$, 可能的阶为 $1,4,12,24$, 对应正规子群 $\left\{e\right\}$, $K_4$, $A_4$, $S_4$. 故非平凡正规子群为 $A_4$ 与 $K_4$.

情形 $n=3$. $\left|S_3\right|=6$, $\left|A_3\right|=3$, $A_3\triangleleft{S}_3$ 且指数为 $2$. 由正规子群是共轭类的并, $S_3$ 的共轭类大小分别为 $1,3,2$, 可能组成正规子群的阶为 $1,3,6$, 故正规子群为 $\left\{e\right\},A_3,S_3$, 非平凡者为 $A_3$.

情形 $n\le2$. $S_n$ 无非平凡正规子群.

综上, $S_n$ 的非平凡正规子群为 $A_n$ (对所有 $n\ge3$), 以及 $n=4$ 时的 $K_4$.

$\blacksquare$

## 1.6-11

设 $\left|G\right|=2n$, 其中 $n$ 为奇数. 证明: $G$ 有指数为 $2$ 的正规子群.

### 解答 1.6-11

先构造群同态 $\psi:G\to\left\{1,-1\right\}$. 由**定理 1.4.10 (凯莱定理)**, 左正则表示 $\lambda:G\to{S}_G$, $g\mapsto{L}_g$ (其中 $L_g\left(x\right)=gx$) 是单同态; 视 $S_G$ 为 $S_{2n}$ (因 $\left|G\right|=2n$). 由**例 1.4.17** 及符号同态, 符号同态 $\mathrm{sgn}:S_{2n}\to\left\{1,-1\right\}$ 是群同态. 复合得 $\psi=\mathrm{sgn}\circ\lambda:G\to\left\{1,-1\right\}$ 是群同态.

再证明 $\psi$ 是满射. 由偶数阶群有二阶元, $G$ 中存在二阶元 $a$ (因 $\left|G\right|=2n$ 为偶数). 则 $\lambda\left(a\right)=L_a$, 且对任意 $x\in{G}$, $L_a^2\left(x\right)=a^2x=x$, 故 $L_a$ 是对合; 又 $a\ne{e}$, 若 $L_a\left(x\right)=x$ 即 $ax=x$, 则 $a=e$, 矛盾, 故 $L_a$ 无不动点. 因此 $L_a$ 是 $G$ (共 $2n$ 个文字) 上的 $n$ 个不相交对换之积, 由符号同态, $\mathrm{sgn}\left(L_a\right)=\left(-1\right)^{n}=-1$ (因 $n$ 为奇数). 故 $\psi\left(a\right)=-1$, 而 $\psi\left(e\right)=1$, 于是 $\psi:G\to\left\{1,-1\right\}$ 是满同态.

最后取核得指数为 $2$ 的正规子群. 令 $H=\ker\psi$. 由**引理 1.4.13**, $H\triangleleft{G}$. 由**定理 1.4.19 (群的同态基本定理)**, $G/H\cong\left\{1,-1\right\}$, 故 $\left|G/H\right|=2$, 即 $\left[G:H\right]=2$. 因此 $G$ 有指数为 $2$ 的正规子群 $H$.

$\blacksquare$

## 1.7-11

设

$$
G=G_1\triangleright{G}_2\triangleright\cdots\triangleright{G}_t=\left\{e\right\}
$$

和

$$
G=H_1\triangleright{H}_2\triangleright\cdots\triangleright{H}_s=\left\{e\right\}
$$

是 $G$ 的两个合成序列, 且 $G_2\ne{H}_2$. 令 $K_3=G_2\cap{H}_2$. 任取 $K_3$ 的合成序列 $K_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\}$. 证明:

(1) $G=G_1\triangleright{G}_2\triangleright{K}_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\}$ 与 $G=H_1\triangleright{H}_2\triangleright{K}_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\}$ 也是 $G$ 的合成序列;

(2) 上述 $G$ 的四个合成序列彼此等价.

### 解答 1.7-11

证明 $G_2H_2=G$. 因 $H_2\triangleleft{G}$, 由满同态保持正规子群, 自然同态 $\pi:G\to{G}/G_2$ 的像 $\pi\left(H_2\right)$ 是 $G/G_2$ 的正规子群. 又 $\pi\left(H_2\right)=\left\{hG_2\mid{h}\in{H}_2\right\}=\left(G_2H_2\right)/G_2$ (因 $G_2\subseteq{G}_2H_2$), 故 $\left(G_2H_2\right)/G_2\triangleleft{G}/G_2$. 因 $G/G_2$ 是合成因子, 为单群, 故 $\left(G_2H_2\right)/G_2$ 只能是平凡群或 $G/G_2$, 即 $G_2H_2=G_2$ 或 $G$.

同理, 由 $G_2\triangleleft{G}$, 自然同态 $\pi':G\to{G}/H_2$ 的像 $\pi'\left(G_2\right)=\left(G_2H_2\right)/H_2\triangleleft{G}/H_2$; 因 $G/H_2$ 为单群, 故 $G_2H_2=H_2$ 或 $G$.

断言 $G_2H_2\ne{G}_2$. 若 $G_2H_2=G_2$, 则 $H_2\subseteq{G}_2$. 由上一段 $G_2H_2\in\left\{H_2,G\right\}$, 即 $G_2=H_2$ 或 $G_2=G$; 前者与 $G_2\ne{H}_2$ 矛盾, 后者与 $G_2$ 是 $G$ 的真子群 (因 $G/G_2$ 是非平凡单群) 矛盾. 故 $G_2H_2\ne{G}_2$.

断言 $G_2H_2\ne{H}_2$. 若 $G_2H_2=H_2$, 则 $G_2\subseteq{H}_2$. 由 $G_2H_2\in\left\{G_2,G\right\}$, 即 $H_2=G_2$ 或 $H_2=G$; 前者与 $G_2\ne{H}_2$ 矛盾, 后者与 $H_2$ 为真子群矛盾. 故 $G_2H_2\ne{H}_2$.

因此只能有 $G_2H_2=G$.

第 (1) 步: 证明两个细化序列是合成序列. 由**定理 1.4.23 (3) (第二同构定理)**, 取 $H=G_2$, $N=H_2$, 得

$$
G_2/K_3=G_2/\left(G_2\cap{H}_2\right)\cong{G}_2H_2/H_2=G/H_2,
$$

而 $G/H_2$ 是合成因子, 为单群, 故 $G_2/K_3$ 是单群.

同理, 由**定理 1.4.23 (3) (第二同构定理)**, 取 $H=H_2$, $N=G_2$, 得

$$
H_2/K_3=H_2/\left(G_2\cap{H}_2\right)\cong{G}_2H_2/G_2=G/G_2,
$$

亦为单群.

又 $K_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\}$ 是 $K_3$ 的合成序列, 故 $K_i/K_{i+1}$ ($i=3,\cdots,r-1$) 均为单群. 因此序列

$$
G=G_1\triangleright{G}_2\triangleright{K}_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\}
$$

的所有因子 $G/G_2$, $G_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ 均为单群; 且 $G_2\triangleright{K}_3$ 是合法的次正规步 ($K_3=G_2\cap{H}_2$, $H_2\triangleleft{G}$, 故 $K_3\triangleleft{G}_2$). 由**定义 1.7.9 (次正规序列与合成序列)**, 它是 $G$ 的合成序列.

同理, 序列

$$
G=H_1\triangleright{H}_2\triangleright{K}_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\}
$$

的因子 $G/H_2$, $H_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ 均为单群, 故由**定义 1.7.9 (次正规序列与合成序列)** 也是 $G$ 的合成序列.

第 (2) 步: 证明四个合成序列彼此等价. 记四个合成序列为

$$
\begin{aligned}
S_1&:G\triangleright{G}_2\triangleright{G}_3\triangleright\cdots\triangleright{G}_t=\left\{e\right\},\\
S_2&:G\triangleright{H}_2\triangleright{H}_3\triangleright\cdots\triangleright{H}_s=\left\{e\right\},\\
S_3&:G\triangleright{G}_2\triangleright{K}_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\},\\
S_4&:G\triangleright{H}_2\triangleright{K}_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\}.
\end{aligned}
$$

先证 $S_3$ 与 $S_4$ 同构. $S_3$ 的因子集为 $G/G_2$, $G_2/K_3\cong{G}/H_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$; $S_4$ 的因子集为 $G/H_2$, $H_2/K_3\cong{G}/G_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$. 两组因子作为多重集合仅前两项交换: $G/G_2$ 与 $G/H_2$ 互换位置, 其余因子完全相同. 故由**定义 1.7.12 (同构序列)**, $S_3$ 与 $S_4$ 同构.

再证 $S_1$ 与 $S_3$ 同构. $S_1$ 与 $S_3$ 的首因子均为 $G/G_2$. 去掉首项后, 二者的尾段

$$
G_2\triangleright{G}_3\triangleright\cdots\triangleright{G}_t=\left\{e\right\}
\quad\text{与}\quad
G_2\triangleright{K}_3\triangleright{K}_4\triangleright\cdots\triangleright{K}_r=\left\{e\right\}
$$

都是 $G_2$ 的合成序列. 由**定理 1.7.13 (若尔当-赫尔德定理)**, 群 $G_2$ 的这两个合成序列同构. 补上二者共同的首因子 $G/G_2$ 后, 由**定义 1.7.12 (同构序列)**, $S_1$ 与 $S_3$ 同构.

同理证 $S_2$ 与 $S_4$ 同构. $S_2$ 与 $S_4$ 的首因子均为 $G/H_2$; 尾段 $H_2\triangleright{H}_3\triangleright\cdots\triangleright\left\{e\right\}$ 与 $H_2\triangleright{K}_3\triangleright{K}_4\triangleright\cdots\triangleright\left\{e\right\}$ 都是 $H_2$ 的合成序列, 由**定理 1.7.13 (若尔当-赫尔德定理)** 它们同构, 补上共同首因子 $G/H_2$ 后, $S_2$ 与 $S_4$ 同构.

综上, $S_1\cong{S}_3\cong{S}_4\cong{S}_2$, 即四个合成序列彼此等价.

$\blacksquare$

## 1.8-12

设 $G$ 为 $n$ 阶可解群, $B$ 为可逆的复上三角矩阵的全体. 证明: $G$ 同构于 $B$ 的某个子群. 如果 $G$ 为 $n$ 阶幂零群, $N$ 为对角线元全为 $1$ 的复上三角矩阵的全体, $G$ 是否同构于 $N$ 的某个子群?

### 解答 1.8-12

先证第一部分. 由群到置换矩阵的忠实表示及**定理 1.4.10 (凯莱定理)**, $n$ 阶可解群 $G$ 同构于 $\mathrm{GL}\left(V\right)$ 的一个子群, 其中 $V=\mathbb{C}^{n}$; 由可解性在同构下保持, 可设 $G$ 本身是 $\mathrm{GL}\left(V\right)$ 的可解子群. 下面对 $\dim{V}$ 作归纳, 证明 $G$ 可同时上三角化, 即 $G$ 共轭于上三角矩阵群 $B$ 的子群.

归纳基础: 当 $\dim{V}=1$ 时, $\mathrm{GL}\left(V\right)\cong\mathbb{C}^{*}$ 本身就是上三角矩阵群, 结论显然成立.

归纳步: 设 $\dim{V}=n>1$. 由**定义 1.8.7 (可解群与幂零群)**, $G$ 的换位子群 $G^{\prime}=\left[G,G\right]$ 是 $G$ 的真正规子群; 由**引理 1.8.5**, $G/G^{\prime}$ 为 阿贝尔群. 由**引理 1.8.8 (可解群的遗传性)**, $G^{\prime}$ 是可解群. 由归纳假设 (对 $G^{\prime}$ 在 $V$ 上反复运用基础情形的结果), $G^{\prime}$ 在 $V$ 上有公共特征向量; 设 $\lambda$ 是 $G^{\prime}$ 的一个特征标, 记其特征子空间为

$$
V_{\lambda}=\left\{v\in{V}\mid\sigma{v}=\lambda\left(\sigma\right)v,\forall\sigma\in{G}^{\prime}\right\}.
$$

因 $G^{\prime}\trianglelefteq{G}$, 对任意 $\tau\in{G}$, $\sigma\in{G}^{\prime}$ 及 $v\in{V}_{\lambda}$, 由**引理 1.8.3 (换位子性质)** (2) (取 $\varphi=\mathrm{Ad}_{\tau}$), $\tau\sigma\tau^{-1}\in{G}^{\prime}$, 且

$$
\sigma\left(\tau{v}\right)=\tau\left(\tau^{-1}\sigma\tau\right)v=\tau\lambda\left(\tau^{-1}\sigma\tau\right)v=\lambda\left(\tau^{-1}\sigma\tau\right)\tau{v},
$$

故由特征标与公共特征子空间, $\tau{v}\in{V}_{\lambda^{\tau}}$, 其中 $\lambda^{\tau}\left(\sigma\right)=\lambda\left(\tau^{-1}\sigma\tau\right)$. 由于 $G/G^{\prime}$ 是 阿贝尔群, $G$ 在 $G^{\prime}$ 的特征标集上的共轭作用轨道有限, 取其中一个轨道对应的特征子空间之和, 即得一个非零的 $G$-不变子空间 $W$.

在 $W$ 上, 因 $G/G^{\prime}$ 为 阿贝尔群而 $G^{\prime}$ 在 $W$ 上以标量作用, 故 $G$ 在 $W$ 上的像的换位子群为标量群, $G$ 的像在 $\mathrm{GL}\left(W\right)$ 中是 阿贝尔化的; 由交换线性变换族的公共特征向量, $W$ 中存在 $G$ 的公共特征向量, 即存在一维 $G$-不变子空间 $L\subseteq{V}$.

于是 $G$ 在商空间 $V/L$ 上诱导一个可解子群 (由可解性在同构下保持与商群的可解性, 或**引理 1.8.8 (可解群的遗传性)**), 由归纳假设, $G$ 在 $V/L$ 上可上三角化. 因而在 $V$ 中可取一组基, 使 $L$ 为第一个基向量张成的子空间, 而商空间的上三角化给出 $G$ 在 $V$ 上的上三角矩阵表示. 故 $G$ 共轭于 $B$ 的一个子群, 即 $G$ 同构于 $B$ 的某个子群.

$\blacksquare$

再回答第二部分. 答案是否定的: 非平凡的有限幂零群 $G$ 不能同构于 $N$ 的子群.

事实上, 设 $A\in{N}$, 即 $A$ 是对角线元全为 $1$ 的复上三角矩阵, 则 $A=I+M$, 其中 $M$ 是严格上三角矩阵. 由幂零矩阵与有限阶元, $M$ 是幂零矩阵, 且若 $A$ 是有限阶元, 则 $M=0$, 即 $A=I$. 这说明 $N$ 中的有限阶元只有单位矩阵 $I$ 自身.

因此 $N$ 的有限子群只能是平凡群 $\left\{I\right\}$. 而 $G$ 是有限的非平凡幂零群, 由有限群元素皆有有限阶, $G$ 含有非单位的有限阶元, 故 $G$ 不能同构于 $N$ 的某个子群.

$\blacksquare$

## 1.9-4

(1) 记 $\mathbb{R}^n$ 的所有 $1$ 维子空间的全体为 $P^{n-1}\left(\mathbb{R}\right)$, 称为实射影空间. 对任意 $\rho\in\mathrm{GL}\left(n,\mathbb{R}\right)$, $W\in{P}^{n-1}\left(\mathbb{R}\right)$, $\rho\left(W\right)$ 也是一个 $1$ 维子空间. 试验证这是 $\mathrm{GL}\left(n,\mathbb{R}\right)$ 在 $P^{n-1}\left(\mathbb{R}\right)$ 上的可递作用, 并求迷向子群.

(2) 记 $\mathbb{R}^n$ 的所有 $k$ 维子空间的全体为 $\mathrm{Gr}\left(k,n\right)$, 称为格拉斯曼流形. 对任意 $\rho\in\mathrm{GL}\left(n,\mathbb{R}\right)$, $W\in\mathrm{Gr}\left(k,n\right)$, $\rho\left(W\right)$ 也是一个 $k$ 维子空间. 试验证这是 $\mathrm{GL}\left(n,\mathbb{R}\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上的可递作用, 并求迷向子群.

(3) 考虑 $\mathrm{SL}\left(n,\mathbb{R}\right)$, $O\left(n\right)$, $\mathrm{SO}\left(n\right)$ 在上述集合上的作用并判断其可递性.

### 解答 1.9-4

第 (1) 部分: $\mathrm{GL}\left(n,\mathbb{R}\right)$ 在 $P^{n-1}\left(\mathbb{R}\right)$ 上的作用. 由线性映射保持子空间维数, 对 $\rho\in\mathrm{GL}\left(n,\mathbb{R}\right)$ 与 $1$ 维子空间 $W=\mathbb{R}v$, $\rho\left(W\right)$ 仍是 $1$ 维子空间. 对 $\rho,\tau\in\mathrm{GL}\left(n,\mathbb{R}\right)$ 及 $W=\mathbb{R}v$,

$$
\rho\left(\tau\left(W\right)\right)=\rho\left(\tau\left(\mathbb{R}v\right)\right)=\rho\left(\mathbb{R}\tau\left(v\right)\right)=\mathbb{R}\rho\left(\tau\left(v\right)\right)=\left(\rho\tau\right)\left(W\right),
$$

且单位矩阵 $I$ 满足 $I\left(W\right)=W$. 由**定义 1.9.1 (群作用)**, 这是 $\mathrm{GL}\left(n,\mathbb{R}\right)$ 在 $P^{n-1}\left(\mathbb{R}\right)$ 上的一个作用.

可递性: 任取两条直线 $W_1=\mathbb{R}v$, $W_2=\mathbb{R}w$ ($v,w\ne0$). 由线性映射保持子空间维数, 存在可逆矩阵 $\rho$ 使 $\rho{v}=w$, 故 $\rho\left(W_1\right)=W_2$. 由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

迷向子群: 取 $W_0=\mathbb{R}e_1$, 其中 $e_1=\left(1,0,\cdots,0\right)^{\top}$. 条件 $\rho\left(W_0\right)=W_0$ 等价于 $\rho{e}_1\in\mathbb{R}e_1$, 即 $\rho$ 的第一列为 $\left(a,0,\cdots,0\right)^{\top}$, $a\ne0$. 故由**定义 1.9.9 (轨道与迷向子群)**, $W_0$ 的迷向子群为

$$
F_{W_0}=\left\{\begin{bmatrix}a&*\\0&A\end{bmatrix}\;\middle|\;a\in\mathbb{R}^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb{R}\right)\right\}.
$$

第 (2) 部分: $\mathrm{GL}\left(n,\mathbb{R}\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上的作用. 同理 $\rho\left(\tau\left(W\right)\right)=\left(\rho\tau\right)\left(W\right)$ 且 $I\left(W\right)=W$, 由**定义 1.9.1 (群作用)** 这是作用.

可递性: 任取两个 $k$ 维子空间 $W_1,W_2$, 分别取基 $\left\{v_1,\cdots,v_k\right\}$ 与 $\left\{w_1,\cdots,w_k\right\}$, 扩充为 $\mathbb{R}^n$ 的基, 由线性映射保持子空间维数 定义可逆线性映射 $\rho$ 使 $\rho{v}_i=w_i$ ($i=1,\cdots,k$), 则 $\rho\left(W_1\right)=W_2$. 由**定义 1.9.7 (可递作用与有效作用)**, 作用可递.

迷向子群: 取 $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$. 条件 $\rho\left(W_0\right)=W_0$ 等价于 $\rho$ 把每个 $e_i$ ($i\le{k}$) 仍映回 $W_0$, 即 $\rho$ 的前 $k$ 列在第 $k+1,\cdots,n$ 行的分量为零, 亦即 $\rho$ 为分块上三角阵. 故由**定义 1.9.9 (轨道与迷向子群)**, 迷向子群为

$$
F_{W_0}=\left\{\begin{bmatrix}A&B\\0&C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb{R}\right),\;C\in\mathrm{GL}\left(n-k,\mathbb{R}\right),\;B\in\mathbb{R}^{k\times\left(n-k\right)}\right\}.
$$

第 (3) 部分: 判断可递性. $\mathrm{SL}\left(n,\mathbb{R}\right)$ 在 $P^{n-1}\left(\mathbb{R}\right)$ 与 $\mathrm{Gr}\left(k,n\right)$ 上的作用均可递: 在第 (1)(2) 部分构造的映射 $\rho$ 中, 若其行列式不为 $1$, 可在最后一行乘一个非零标量把行列式调整为 $1$, 而不改变对子空间的作用.

$O\left(n\right)$ 在 $P^{n-1}\left(\mathbb{R}\right)$ 上可递: 由正交与酉变换, 任意两条单位直线可由正交变换互相映射. $O\left(n\right)$ 在 $\mathrm{Gr}\left(k,n\right)$ 上亦可递: 两组 $k$ 维子空间的基可扩充为两组标准正交基, 由正交与酉变换 存在正交映射互相映射.

$\mathrm{SO}\left(n\right)$ 在 $P^{n-1}\left(\mathbb{R}\right)$ 上, 当 $n\ge3$ 时可递 (可用适当旋转把任一方向映到任一方向而保持行列式为 $1$); 在 $\mathrm{Gr}\left(k,n\right)$ 上, 当 $n\ge3$ 时亦可递.

$\blacksquare$
