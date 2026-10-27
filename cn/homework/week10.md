# week10

> **基础知识: 素数阶群与循环群的可解性**<br>素数阶群是循环群, 因而可解; 任意循环群 (交换群) 都可解.

> **基础知识: 直积中元素的阶**<br>设 $a\in G$, $b\in H$, 则 $\left(a,b\right)$ 在直积 $G\times H$ 中的阶为 $\mathrm{lcm}\left(\mathrm{ord}\,a,\mathrm{ord}\,b\right)$. 故当 $\left(m,n\right)=1$ 时, $\mathbb Z_m\times\mathbb Z_n$ 是 $mn$ 阶循环群, 即 $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$.

> **基础知识: 指数为 $2$ 的子群与 $S_n$ 的交错子群**<br>指数为 $2$ 的子群是正规子群; $S_n$ 的指数为 $2$ 的子群唯一, 即交错群 $A_n$. 特别地, $S_5$ 的指数为 $2$ 的子群就是 $A_5$.

> **基础知识: $4$ 阶群是交换群**<br>$4$ 阶群或为 $4$ 阶循环群, 或为克莱因四元群, 两者皆交换.

> **基础知识: 西罗子群与元素计数**<br>共轭保持阶, 故共轭子群与原子群同阶; 两个不同的素数阶子群交为 $\left\{e\right\}$; 一个 $p^{k}$ 阶西罗 $p$-子群含 $p^{k}-1$ 个非单位的 $p$ 幂阶元素. 有限单群的西罗 $p$-子群个数不能为 $1$ (否则该西罗子群是正规子群).

> **基础知识: 群在陪集空间上的作用**<br>设 $H<G$, 则 $G$ 在左陪集空间 $G/H$ 上以左平移作用, 给出群同态 $G\to S_{\left[G:H\right]}$; 其核 $\bigcap_{g\in G}gHg^{-1}$ 是 $G$ 的正规子群.

> **引理 1.7.7**<br>设 $A,B$ 是 $G$ 的子群, $G=AB$, $A\cap B=\left\{e\right\}$, 则 $A,B$ 都是 $G$ 的正规子群当且仅当对任意 $a\in A$, $b\in B$ 有 $ab=ba$.

> **引理 1.8.8 (可解群的遗传性)**<br>可解群的子群,商群都是可解群; 反之, 设 $N\trianglelefteq G$, 且 $N$ 与 $G/N$ 都可解, 则 $G$ 可解.

> **定理 1.10.8 (西罗第二定理)**<br>设 $P$ 是 $G$ 的一个西罗 $p$-子群, $H$ 是 $G$ 的一个 $p^{k}$ 阶子群, $k\le l$ (其中 $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$), 则存在 $g\in G$ 使 $H\subseteq gPg^{-1}$. 特别地, $G$ 的西罗 $p$-子群相互共轭.

> **定理 1.10.10 (西罗第三定理)**<br>设 $G$ 的西罗 $p$-子群的个数为 $n_{p}$, 则 (1) $G$ 的西罗 $p$-子群 $P\triangleleft G$ 当且仅当 $n_{p}=1$; (2) $n_{p}\mid m$ 且 $n_{p}\equiv1\pmod p$, 其中 $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$.

---

## 1.10-10

设 $\left|G\right|=pq$, 其中 $p,q$ 为不同的素数, 证明: $G$ 为可解群.

### 解答 1.10-10

不妨设 $p<q$. 由**定理 1.10.10 (西罗第三定理)**, 西罗 $q$-子群的个数 $n_{q}$ 满足 $n_{q}\mid p$ 且 $n_{q}\equiv1\pmod q$. 因 $p<q$, $n_{q}$ 作为 $p$ 的正因子只能是 $1$ 或 $p$. 若 $n_{q}=p$, 则 $p\equiv1\pmod q$, 即 $q\mid p-1$; 但 $p<q$ 蕴含 $p-1<q$, 矛盾. 故 $n_{q}=1$.

于是 $G$ 的西罗 $q$-子群 $Q$ 唯一, 由**定理 1.10.10 (西罗第三定理)** (1), $Q\triangleleft G$. 又 $\left|Q\right|=q$ 为素数, 由**基础知识: 素数阶群与循环群的可解性**, $Q$ 是循环群, 从而是可解群. 商群 $G/Q$ 的阶为 $p$, 也是素数阶循环群, 由**基础知识: 素数阶群与循环群的可解性** 亦是可解群.

由**引理 1.8.8 (可解群的遗传性)**, $Q$ 与 $G/Q$ 均可解, 故 $G$ 可解. $\blacksquare$

---

## 1.10-12

(弗拉蒂尼) 设 $N\triangleleft G$, $P$ 为 $N$ 的西罗子群, 则 $G=N_{G}\left(P\right)N$.

### 解答 1.10-12

任取 $g\in G$. 因 $N\triangleleft G$, 共轭 $gPg^{-1}$ 仍为 $N$ 的子群; 又共轭保持阶, 由**基础知识: 西罗子群与元素计数**, $\left|gPg^{-1}\right|=\left|P\right|$, 故 $gPg^{-1}$ 也是 $N$ 的一个西罗 $p$-子群.

由**定理 1.10.8 (西罗第二定理)** (应用于子群 $N$), $N$ 的任意两个西罗 $p$-子群在 $N$ 中共轭, 故存在 $n\in N$ 使

$$
gPg^{-1}=nPn^{-1}.
$$

于是

$$
n^{-1}gPg^{-1}n=P,
$$

即 $n^{-1}g\in N_{G}\left(P\right)$ (它把 $P$ 共轭回 $P$). 记 $h=n^{-1}g\in N_{G}\left(P\right)$, 则 $g=nh$.

因此 $g\in N_{G}\left(P\right)N$. 由 $g\in G$ 的任意性, $G=N_{G}\left(P\right)N$. $\blacksquare$

---

## 1.10-15

设 $p,q$ 都是素数, $p<q$, $p\nmid\left(q-1\right)$, 证明 $pq$ 阶群一定是循环群.

### 解答 1.10-15

设 $\left|G\right|=pq$. 由**定理 1.10.10 (西罗第三定理)**, 西罗 $q$-子群的个数 $n_{q}$ 满足 $n_{q}\mid p$ 且 $n_{q}\equiv1\pmod q$. 因 $p<q$, 如 1.10-10 题所示, $n_{q}=1$. 故 $G$ 的西罗 $q$-子群 $Q$ 唯一, 由**定理 1.10.10 (西罗第三定理)** (1), $Q\triangleleft G$, $\left|Q\right|=q$.

再考虑西罗 $p$-子群的个数 $n_{p}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{p}\mid q$ 且 $n_{p}\equiv1\pmod p$. 因 $q$ 为素数, $n_{p}=1$ 或 $q$. 若 $n_{p}=q$, 则 $q\equiv1\pmod p$, 即 $p\mid\left(q-1\right)$, 与题设 $p\nmid\left(q-1\right)$ 矛盾. 故 $n_{p}=1$.

于是 $G$ 的西罗 $p$-子群 $P$ 也唯一, 由**定理 1.10.10 (西罗第三定理)** (1), $P\triangleleft G$, $\left|P\right|=p$.

因 $p,q$ 互素, $P\cap Q=\left\{e\right\}$. 又

$$
\left|PQ\right|=\left|P\right|\left|Q\right|/\left|P\cap Q\right|=pq=\left|G\right|,
$$

故 $G=PQ$.

由**引理 1.7.7**, $P,Q$ 都是 $G$ 的正规子群且 $P\cap Q=\left\{e\right\}$, 故对任意 $a\in P$, $b\in Q$ 有 $ab=ba$. 于是映射

$$
P\times Q\to G,\quad\left(a,b\right)\mapsto ab
$$

保持乘法 (因 $ab=ba$) 且为双射 (单射由 $P\cap Q=\left\{e\right\}$, 满射由 $G=PQ$), 故它是群同构, 即 $G\cong P\times Q$.

又 $P\cong\mathbb Z_p$, $Q\cong\mathbb Z_q$, 而 $p,q$ 互素, 由**基础知识: 直积中元素的阶**, $\mathbb Z_p\times\mathbb Z_q\cong\mathbb Z_{pq}$, 故

$$
G\cong\mathbb Z_p\times\mathbb Z_q\cong\mathbb Z_{pq},
$$

即 $G$ 是 $pq$ 阶循环群. $\blacksquare$

---

## 1.10-20

证明: $60$ 阶非阿贝尔有限单群必同构于 $A_5$.

### 解答 1.10-20

设 $G$ 是 $60$ 阶非阿贝尔单群. 先求西罗 $5$-子群的个数 $n_{5}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{5}\mid12$ 且 $n_{5}\equiv1\pmod5$, 故 $n_{5}=1$ 或 $6$. 由**基础知识: 西罗子群与元素计数**, $G$ 单故 $n_{5}\ne1$, 于是 $n_{5}=6$.

每个西罗 $5$-子群是 $5$ 阶循环群, 由**基础知识: 西罗子群与元素计数**, 含 $4$ 个 $5$ 阶元; 两个不同的西罗 $5$-子群交为 $\left\{e\right\}$ (交的阶同时整除 $5$, 故只能为 $1$). 因此 $G$ 中共有 $6\times4=24$ 个 $5$ 阶元.

再考虑西罗 $2$-子群的个数 $n_{2}$. 由**定理 1.10.10 (西罗第三定理)**, $n_{2}\mid15$ 且 $n_{2}\equiv1\pmod2$, 故 $n_{2}\in\left\{1,3,5,15\right\}$. 由**基础知识: 西罗子群与元素计数**, $G$ 单故 $n_{2}\ne1$.

**排除 $n_{2}=3$.** 由**基础知识: 群在陪集空间上的作用**, $G$ 通过共轭作用在 $3$ 个西罗 $2$-子群上, 给出同态 $\pi:G\to S_3$. 其核 $\ker\pi$ 是 $G$ 的正规子群. 因 $G$ 单, $\ker\pi=\left\{e\right\}$ 或 $G$. 作用可递故非平凡, $\ker\pi\ne G$; 若 $\ker\pi=\left\{e\right\}$, 则 $G$ 同构于 $S_3$ 的子群, 而 $\left|S_3\right|=6<60$, 矛盾. 故 $n_{2}\ne3$.

**处理 $n_{2}=5$.** 由**基础知识: 群在陪集空间上的作用**, $G$ 共轭作用在 $5$ 个西罗 $2$-子群上, 给出同态 $\pi:G\to S_5$. 同理 $\ker\pi$ 为正规子群且非 $G$; 若 $\ker\pi=\left\{e\right\}$, 则 $G$ 同构于 $S_5$ 的一个 $60$ 阶子群. $S_5$ 的阶为 $120$, 该 $60$ 阶子群指数为 $2$, 由**基础知识: 指数为 $2$ 的子群与 $S_n$ 的交错子群** 必为正规子群且唯一, 即 $A_5$. 故 $G\cong A_5$, 结论成立.

**排除 $n_{2}=15$.** 若任意两个不同的西罗 $2$-子群交为 $\left\{e\right\}$, 则每个 $4$ 阶西罗 $2$-子群贡献 $3$ 个非单位元 (由**基础知识: $4$ 阶群是交换群** 与**基础知识: 西罗子群与元素计数**), 共 $15\times3=45$ 个 $2$ 阶或 $4$ 阶元, 加上 $24$ 个 $5$ 阶元, 总数 $45+24=69>60$, 矛盾. 故存在两个不同的西罗 $2$-子群 $P,Q$ 使 $\left|P\cap Q\right|=2$.

设 $P\cap Q=\left\langle x\right\rangle$, 其中 $x$ 为 $2$ 阶元. 因 $P,Q$ 均为 $4$ 阶群, 由**基础知识: $4$ 阶群是交换群** 皆交换, 且 $x\in P\cap Q$, 故 $P,Q\subseteq N_{G}\left(\left\langle x\right\rangle\right)$. 又 $P\ne Q$, 故 $\left|N_{G}\left(\left\langle x\right\rangle\right)\right|>4$. 同时 $\left|N_{G}\left(\left\langle x\right\rangle\right)\right|\mid60$ 且被 $4$ 整除 (因含 $4$ 阶子群 $P$), 故只能为 $12,20$ 或 $60$. 若为 $60$, 则 $\left\langle x\right\rangle\triangleleft G$, 与 $G$ 单矛盾. 故 $\left|N_{G}\left(\left\langle x\right\rangle\right)\right|=12$ 或 $20$, 对应指数 $5$ 或 $3$.

指数 $3$ 时, 由**基础知识: 群在陪集空间上的作用**, $G$ 左平移作用在 $3$ 个陪集上给出同态 $G\to S_3$, 与前述 $n_{2}=3$ 的矛盾相同, 故指数必为 $5$. 于是 $G$ 有指数 $5$ 的子群 $N_{G}\left(\left\langle x\right\rangle\right)$; 由**基础知识: 群在陪集空间上的作用**, $G$ 左平移作用在 $5$ 个陪集上给出同态 $G\to S_5$, 其核为正规子群且非 $G$, 因 $G$ 单故核为 $\left\{e\right\}$, 得单同态 $G\hookrightarrow S_5$. 如前所述, $S_5$ 的 $60$ 阶子群只能是 $A_5$, 故 $G\cong A_5$. $\blacksquare$
