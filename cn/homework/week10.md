# 作业 10

> **定理 1.10.1**（柯西定理）设素数 $p$ 是 $\left|G\right|$ 的因子, 则 $G$ 中存在 $p$ 阶元.

> **定理 1.10.5**（西罗第一定理）设 $\left|G\right|=p^{l}m$, $p$ 为素数, $l\ge1$, $\left(p,m\right)=1$, 则对任意 $k\le l$, $G$ 中存在 $p^{k}$ 阶子群. 特别地, $G$ 存在西罗 $p$-子群 ($p^{l}$ 阶子群).

> **定理 1.10.8**（西罗第二定理）设 $P$ 是 $G$ 的一个西罗 $p$-子群, $H$ 是 $G$ 的一个 $p^{k}$ 阶子群, $k\le l$, 则存在 $g\in G$ 使 $H\subseteq gPg^{-1}$. 特别地, $G$ 的西罗 $p$-子群相互共轭.

> **定理 1.10.10**（西罗第三定理）设 $G$ 的西罗 $p$-子群的个数为 $n_p$, 则 $n_p\mid m$, 且 $n_p\equiv1\pmod p$. 又西罗 $p$-子群正规当且仅当 $n_p=1$.

> **引理 1.8.8**（可解群的遗传性）可解群的子群, 商群都是可解群; 反之, 设 $N\trianglelefteq G$, 且 $N$ 与 $G/N$ 都可解, 则 $G$ 可解.

### 习题一

（习题 1.10-10）设 $\left|G\right|=pq$, 其中 $p,q$ 为不同的素数, 证明: $G$ 为可解群.

### 解答 习题一

不妨设 $p<q$. 由**定理 1.10.10**（西罗第三定理）, 西罗 $q$-子群的个数 $n_q$ 满足 $n_q\mid p$ 且 $n_q\equiv1\pmod q$. 因 $p<q$, $n_q$ 作为 $p$ 的正因子只能是 $1$ 或 $p$. 若 $n_q=p$, 则 $p\equiv1\pmod q$, 即 $q\mid p-1$, 但 $p<q$ 蕴含 $p-1<q$, 矛盾. 故 $n_q=1$.

于是 $G$ 的西罗 $q$-子群 $Q$ 唯一, 由**定理 1.10.10**, $Q\trianglelefteq G$. 又 $\left|Q\right|=q$ 为素数, 故 $Q$ 是循环群, 从而是可解群. 商群 $G/Q$ 的阶为 $p$, 也是素数阶循环群, 亦是可解群.

由**引理 1.8.8**（可解群的遗传性）, $Q$ 与 $G/Q$ 均可解, 故 $G$ 可解. $\blacksquare$

### 习题二

（习题 1.10-12）(弗拉蒂尼)设 $N\trianglelefteq G$, $P$ 为 $N$ 的西罗子群, 则 $G=N_G\left(P\right)N$.

### 解答 习题二

任取 $g\in G$. 因 $N\trianglelefteq G$, 共轭 $gPg^{-1}$ 仍为 $N$ 的子群, 且
$$
\left|gPg^{-1}\right|=\left|P\right|,
$$
故 $gPg^{-1}$ 也是 $N$ 的一个西罗 $p$-子群.

由**定理 1.10.8**（西罗第二定理）, $N$ 的任意两个西罗 $p$-子群在 $N$ 中共轭. 故存在 $n\in N$ 使
$$
gPg^{-1}=nPn^{-1}.
$$
于是
$$
n^{-1}gPg^{-1}n=P,
$$
即 $n^{-1}g\in N_G\left(P\right)$. 记 $h=n^{-1}g\in N_G\left(P\right)$, 则 $g=nh$.

因此 $g\in N_G\left(P\right)N$. 由 $g$ 的任意性,
$$
G=N_G\left(P\right)N.
$$
$\blacksquare$

### 习题三

（习题 1.10-15）设 $p,q$ 都是素数, $p<q$, $p\nmid\left(q-1\right)$, 证明 $pq$ 阶群一定是循环群.

### 解答 习题三

设 $\left|G\right|=pq$. 由**定理 1.10.10**（西罗第三定理）, 西罗 $q$-子群的个数 $n_q$ 满足 $n_q\mid p$ 且 $n_q\equiv1\pmod q$. 因 $p<q$, 如习题一所示, $n_q=1$. 故 $G$ 的西罗 $q$-子群 $Q$ 唯一, $Q\trianglelefteq G$, $\left|Q\right|=q$.

再考虑西罗 $p$-子群的个数 $n_p$. 由**定理 1.10.10**, $n_p\mid q$ 且 $n_p\equiv1\pmod p$. 因 $q$ 为素数, $n_p=1$ 或 $q$. 若 $n_p=q$, 则 $q\equiv1\pmod p$, 即 $p\mid\left(q-1\right)$, 与题设 $p\nmid\left(q-1\right)$ 矛盾. 故 $n_p=1$.

于是 $G$ 的西罗 $p$-子群 $P$ 也唯一, $P\trianglelefteq G$, $\left|P\right|=p$.

因 $p,q$ 互素, $P\cap Q=\left\{e\right\}$. 又

$$
\left|PQ\right|=\left|P\right|\left|Q\right|/\left|P\cap Q\right|=pq=\left|G\right|,
$$

故 $G=PQ$.

由**引理 1.7.7** (正规子群交换条件), $P,Q$ 都是 $G$ 的正规子群且 $P\cap Q=\left\{e\right\}$, 故对任意 $a\in P$, $b\in Q$ 有 $ab=ba$. 于是映射
$$
P\times Q\to G,\left(a,b\right)\mapsto ab
$$
是群同构, 即 $G\cong P\times Q$.

又 $P\cong\mathbb Z_p$, $Q\cong\mathbb Z_q$, 而 $p,q$ 互素, 故
$$
G\cong\mathbb Z_p\times\mathbb Z_q\cong\mathbb Z_{pq},
$$
即 $G$ 是 $pq$ 阶循环群. $\blacksquare$

### 习题四

（习题 1.10-20）证明: $60$ 阶非阿贝尔有限单群必同构于 $A_5$.

### 解答 习题四

设 $G$ 是 $60$ 阶非阿贝尔单群. 先求西罗 $5$-子群的个数 $n_5$. 由**定理 1.10.10**（西罗第三定理）, $n_5\mid12$ 且 $n_5\equiv1\pmod5$, 故 $n_5=1$ 或 $6$. 因 $G$ 单, $n_5\ne1$, 故 $n_5=6$.

每个西罗 $5$-子群是 $5$ 阶循环群, 含 $4$ 个 $5$ 阶元; 两个不同的西罗 $5$-子群交为 $\left\{e\right\}$ (交的阶同时整除 $5$, 故只能为 $1$). 因此 $G$ 中共有 $6\times4=24$ 个 $5$ 阶元.

再考虑西罗 $2$-子群的个数 $n_2$. $n_2\mid15$ 且 $n_2\equiv1\pmod2$, 故 $n_2\in\left\{1,3,5,15\right\}$. 因 $G$ 单, $n_2\ne1$.

若 $n_2=3$, $G$ 通过共轭作用在这 $3$ 个西罗 $2$-子群上, 给出同态 $\pi:G\to S_3$. 其核为 $G$ 的正规子群. 因 $G$ 单, $\ker\pi=\left\{e\right\}$ 或 $G$. 作用非平凡, 故 $\ker\pi\ne G$; 但若 $\ker\pi=\left\{e\right\}$, 则 $G$ 同构于 $S_3$ 的子群, 而 $\left|S_3\right|=6<60$, 矛盾. 故 $n_2\ne3$.

若 $n_2=5$, $G$ 共轭作用在 $5$ 个西罗 $2$-子群上, 给出同态 $\pi:G\to S_5$. 同理 $\ker\pi=\left\{e\right\}$, 故 $G$ 同构于 $S_5$ 的一个 $60$ 阶子群. $S_5$ 的阶为 $120$, 指数为 $2$ 的子群必正规, 而 $A_5$ 正是 $S_5$ 唯一的指数 $2$ 子群. 故 $G\cong A_5$.

最后排除 $n_2=15$. 若任意两个不同的西罗 $2$-子群交为 $\left\{e\right\}$, 则每个 $4$ 阶西罗 $2$-子群贡献 $3$ 个非单位元, 共 $15\times3=45$ 个 $2$ 阶或 $4$ 阶元, 加上 $24$ 个 $5$ 阶元, 总数超过 $60$, 矛盾.

故存在两个不同的西罗 $2$-子群 $P,Q$ 使 $\left|P\cap Q\right|=2$. 设 $P\cap Q=\left\{e,x\right\}$, $x$ 为 $2$ 阶元. 因 $P,Q$ 均为 $4$ 阶群 (交换), 都正规于自身, 故 $P,Q\subseteq N_G\left(\left\langle x\right\rangle\right)$. 又 $P\ne Q$, 故 $\left|N_G\left(\left\langle x\right\rangle\right)\right|>4$. 同时 $\left|N_G\left(\left\langle x\right\rangle\right)\right|\mid60$ 且被 $4$ 整除, 故只能为 $12,20$ 或 $60$. 若为 $60$, 则 $\left\langle x\right\rangle\trianglelefteq G$, 与 $G$ 单矛盾. 故 $\left|N_G\left(\left\langle x\right\rangle\right)\right|=12$ 或 $20$, 对应指数 $5$ 或 $3$.

指数 $3$ 时同态 $G\to S_3$ 与前述矛盾, 故指数必为 $5$. 于是 $G$ 有指数 $5$ 的子群, $G$ 通过左平移作用在该子群的 $5$ 个陪集上, 给出单同态 $G\hookrightarrow S_5$. 如前所述, $S_5$ 的 $60$ 阶子群只能是 $A_5$, 故 $G\cong A_5$. $\blacksquare$
