# 作业 7

> **定义 1.7.9**（次正规序列与合成序列）群 $G$ 中的子群序列
> $$
> G=G_1\trianglerighteq G_2\trianglerighteq\cdots\trianglerighteq G_t\trianglerighteq G_{t+1}=\left\{e\right\}
> $$
> 若满足 $G_{i+1}\trianglelefteq G_i$, 则称为次正规序列, 称 $G_i/G_{i+1}$ 为其因子. 若诸因子 $G_i/G_{i+1}$ 都是单群, 则称该次正规序列为 $G$ 的合成序列, 称 $G_i/G_{i+1}$ 为 $G$ 的合成因子.

> **定义 1.7.12**（同构序列）群 $G$ 的两个次正规序列称为同构的, 如果这两个序列的因子集之间有一一对应, 且对应的因子同构.

> **定理 1.7.13**（若尔当-赫尔德定理）设群 $G$ 存在合成序列, 则 $G$ 的任意两个合成序列同构.

> **基础知识**（第二同构定理）设 $A,B$ 是 $G$ 的子群且 $B\trianglelefteq G$, $A\le G$, 则 $A\cap B\trianglelefteq A$ 且 $A/\left(A\cap B\right)\cong AB/B$. 特别地, 若 $A,B$ 均为 $G$ 的正规子群, 则 $AB/\!A\cong B/\left(A\cap B\right)$.

### 习题一

（习题 1.7-11）设
$$
G=G_1\triangleright G_2\triangleright\cdots\triangleright G_t=\left\{e\right\},
$$
和
$$
G=H_1\triangleright H_2\triangleright\cdots\triangleright H_s=\left\{e\right\},
$$
是 $G$ 的两个合成序列, 且 $G_2\ne H_2$. 令 $K_3=G_2\cap H_2$. 任取 $K_3$ 的合成序列
$$
K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}.
$$
证明:
(1)

$$
G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\},\
G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

也是 $G$ 的合成序列;
(2)上述 $G$ 的四个合成序列彼此等价.

### 解答 习题一

先证明 $G_2H_2=G$. 因 $G_2,H_2$ 都是 $G$ 的正规子群, 故 $G_2H_2\trianglelefteq G$, 且 $G_2H_2\supseteq G_2$. 又 $G/G_2$ 是合成因子, 为单群, 故 $G_2H_2/G_2$ 作为 $G/G_2$ 的正规子群只能是平凡群或 $G/G_2$, 即 $G_2H_2=G_2$ 或 $G$.

若 $G_2H_2=G_2$, 则 $H_2\subseteq G_2$, 从而 $G_2H_2=G_2\ne H_2$. 另一方面, $G_2H_2/H_2\trianglelefteq G/H_2$, 而 $G/H_2$ 也是单群, 故 $G_2H_2=H_2$ 或 $G$. 由 $G_2H_2\ne H_2$ 得 $G_2H_2=G$. 于是 $G_2=G$, 与 $G_2\triangleleft G$ 矛盾. 故 $G_2H_2\ne G_2$.

同理 $G_2H_2\ne H_2$. 因此只能有
$$
G_2H_2=G.
$$

(1)由 $G_2H_2=G$ 及**基础知识**（第二同构定理）,
$$
G_2/K_3=G_2/\left(G_2\cap H_2\right)\cong G_2H_2/H_2=G/H_2,
$$
而 $G/H_2$ 是合成因子, 为单群, 故 $G_2/K_3$ 为单群.

同理,
$$
H_2/K_3=H_2/\left(G_2\cap H_2\right)\cong G_2H_2/G_2=G/G_2,
$$
亦为单群.

又 $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ 是 $K_3$ 的合成序列, 故 $K_i/K_{i+1}$ ($i=3,\cdots,r-1$) 均为单群. 因此序列
$$
G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$
的所有因子 $G/G_2$, $G_2/K_3$, $K_3/K_4,\cdots,K_{r-1}/K_r$ 均为单群. 由**定义 1.7.9**（次正规序列与合成序列）, 它是 $G$ 的合成序列.

同理, 序列
$$
G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$
的因子 $G/H_2$, $H_2/K_3$, $K_3/K_4,\cdots,K_{r-1}/K_r$ 亦均为单群, 故也是 $G$ 的合成序列.

(2)记四个合成序列为
$$
S_1:\;G\triangleright G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\},;S_2:\;G\triangleright H_2\triangleright H_3\triangleright\cdots\triangleright H_s=\left\{e\right\},;S_3:\;G\triangleright G_2\triangleright K_3\triangleright\cdots\triangleright K_r=\left\{e\right\},;S_4:\;G\triangleright H_2\triangleright K_3\triangleright\cdots\triangleright K_r=\left\{e\right\}.
$$

先证 $S_3$ 与 $S_4$ 同构. $S_3$ 的因子为
$$
G/G_2, G_2/K_3\cong G/H_2, K_3/K_4,\cdots, K_{r-1}/K_r;
$$
$S_4$ 的因子为
$$
G/H_2, H_2/K_3\cong G/G_2, K_3/K_4,\cdots, K_{r-1}/K_r.
$$
两组因子作为多重集合仅前两项次序不同, 而 $G/G_2$ 与 $G/H_2$ 恰互换位置, 其余因子完全相同. 由**定义 1.7.12**（同构序列）, $S_3$ 与 $S_4$ 同构.

再证 $S_1$ 与 $S_3$ 同构. $S_1$ 与 $S_3$ 的首因子均为 $G/G_2$. 去掉首项后, 二者的尾段
$$
G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\}
$$
与
$$
G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$
都是 $G_2$ 的合成序列. 因 $\left|G_2\right|< \left|G\right|$, 对群的阶归纳, 由**定理 1.7.13**（若尔当-赫尔德定理）, $G_2$ 的这两个合成序列同构. 因而补上共同的首因子 $G/G_2$ 后, $S_1$ 与 $S_3$ 同构.

同理, $S_2$ 与 $S_4$ 的首因子均为 $G/H_2$, 尾段 $H_2\triangleright\cdots\triangleright\left\{e\right\}$ 与 $H_2\triangleright K_3\triangleright\cdots\triangleright\left\{e\right\}$ 都是 $H_2$ 的合成序列, 由归纳假设它们同构, 故 $S_2$ 与 $S_4$ 同构.

综上, $S_1\cong S_3\cong S_4\cong S_2$, 即四个合成序列彼此等价. $\blacksquare$
