# week7

> **基础知识: 满同态保持正规子群**<br>设 $f:G\to G'$ 是满同态, 若 $H\triangleleft G$, 则 $f\left(H\right)\triangleleft G'$.

> **定理 1.4.23 (3) (第二同构定理)**<br>设 $G$ 是群, $N\triangleleft G$, $H<G$, 则 $HN/N\cong H/\left(H\cap N\right)$.

> **定义 1.7.9 (次正规序列与合成序列)**<br>群 $G$ 中的子群序列 $G=G_1\trianglerighteq G_2\trianglerighteq\cdots\trianglerighteq G_t\trianglerighteq G_{t+1}=\left\{e\right\}$, 若满足 $G_{i+1}\trianglelefteq G_i$ ($i=1,\cdots,t$), 则称为次正规序列, 称 $G_i/G_{i+1}$ 为此序列的因子群. 若诸因子 $G_i/G_{i+1}$ 都是单群, 则称该次正规序列为 $G$ 的合成序列, 称 $G_i/G_{i+1}$ 为 $G$ 的合成因子.

> **定义 1.7.12 (同构序列)**<br>群 $G$ 的两个次正规序列 $G=G_1\supset G_2\supset\cdots\supset G_t=\left\{e\right\}$ 与 $G=H_1\supset H_2\supset\cdots\supset H_s=\left\{e\right\}$ 称为同构的, 如果这两个序列的因子集之间有一一对应, 且对应的因子同构.

> **定理 1.7.13 (若尔当-赫尔德定理)**<br>设群 $G$ 存在合成序列, 则 $G$ 的任意两个合成序列同构. 特别地, $G$ 的任意两个主序列也同构.

---

## 1.7-11

设

$$
G=G_1\triangleright G_2\triangleright\cdots\triangleright G_t=\left\{e\right\}
$$

和

$$
G=H_1\triangleright H_2\triangleright\cdots\triangleright H_s=\left\{e\right\}
$$

是 $G$ 的两个合成序列, 且 $G_2\ne H_2$. 令 $K_3=G_2\cap H_2$. 任取 $K_3$ 的合成序列 $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$. 证明:

(1) $G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ 与 $G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ 也是 $G$ 的合成序列;

(2) 上述 $G$ 的四个合成序列彼此等价.

### 解答 1.7-11

**第一步: 证明 $G_2H_2=G$.** 因 $H_2\triangleleft G$, 由**基础知识: 满同态保持正规子群**, 自然同态 $\pi:G\to G/G_2$ 的像 $\pi\left(H_2\right)$ 是 $G/G_2$ 的正规子群. 又 $\pi\left(H_2\right)=\left\{hG_2\mid h\in H_2\right\}=\left(G_2H_2\right)/G_2$ (因 $G_2\subseteq G_2H_2$), 故 $\left(G_2H_2\right)/G_2\triangleleft G/G_2$. 因 $G/G_2$ 是合成因子, 为单群, 故 $\left(G_2H_2\right)/G_2$ 只能是平凡群或 $G/G_2$, 即 $G_2H_2=G_2$ 或 $G$.

同理, 由 $G_2\triangleleft G$, 自然同态 $\pi':G\to G/H_2$ 的像 $\pi'\left(G_2\right)=\left(G_2H_2\right)/H_2\triangleleft G/H_2$; 因 $G/H_2$ 为单群, 故 $G_2H_2=H_2$ 或 $G$.

**断言 $G_2H_2\ne G_2$.** 若 $G_2H_2=G_2$, 则 $H_2\subseteq G_2$. 由上一段 $G_2H_2\in\left\{H_2,G\right\}$, 即 $G_2=H_2$ 或 $G_2=G$; 前者与 $G_2\ne H_2$ 矛盾, 后者与 $G_2$ 是 $G$ 的真子群 (因 $G/G_2$ 是非平凡单群) 矛盾. 故 $G_2H_2\ne G_2$.

**断言 $G_2H_2\ne H_2$.** 若 $G_2H_2=H_2$, 则 $G_2\subseteq H_2$. 由 $G_2H_2\in\left\{G_2,G\right\}$, 即 $H_2=G_2$ 或 $H_2=G$; 前者与 $G_2\ne H_2$ 矛盾, 后者与 $H_2$ 为真子群矛盾. 故 $G_2H_2\ne H_2$.

因此只能有 $G_2H_2=G$.

**第 (1) 步: 证明两个细化序列是合成序列.** 由**定理 1.4.23 (3) (第二同构定理)**, 取 $H=G_2$, $N=H_2$, 得

$$
G_2/K_3=G_2/\left(G_2\cap H_2\right)\cong G_2H_2/H_2=G/H_2,
$$

而 $G/H_2$ 是合成因子, 为单群, 故 $G_2/K_3$ 是单群.

同理, 由**定理 1.4.23 (3) (第二同构定理)**, 取 $H=H_2$, $N=G_2$, 得

$$
H_2/K_3=H_2/\left(G_2\cap H_2\right)\cong G_2H_2/G_2=G/G_2,
$$

亦为单群.

又 $K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}$ 是 $K_3$ 的合成序列, 故 $K_i/K_{i+1}$ ($i=3,\cdots,r-1$) 均为单群. 因此序列

$$
G=G_1\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

的所有因子 $G/G_2$, $G_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ 均为单群; 且 $G_2\triangleright K_3$ 是合法的次正规步 ($K_3=G_2\cap H_2$, $H_2\triangleleft G$, 故 $K_3\triangleleft G_2$). 由**定义 1.7.9 (次正规序列与合成序列)**, 它是 $G$ 的合成序列.

同理, 序列

$$
G=H_1\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

的因子 $G/H_2$, $H_2/K_3$, $K_3/K_4$, ..., $K_{r-1}/K_r$ 均为单群, 故由**定义 1.7.9 (次正规序列与合成序列)** 也是 $G$ 的合成序列.

**第 (2) 步: 证明四个合成序列彼此等价.** 记四个合成序列为

$$
\begin{aligned}
S_1&:G\triangleright G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\},\\
S_2&:G\triangleright H_2\triangleright H_3\triangleright\cdots\triangleright H_s=\left\{e\right\},\\
S_3&:G\triangleright G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\},\\
S_4&:G\triangleright H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}.
\end{aligned}
$$

**先证 $S_3$ 与 $S_4$ 同构.** $S_3$ 的因子集为 $G/G_2$, $G_2/K_3\cong G/H_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$; $S_4$ 的因子集为 $G/H_2$, $H_2/K_3\cong G/G_2$, $K_3/K_4$, ..., $K_{r-1}/K_r$. 两组因子作为多重集合仅前两项交换: $G/G_2$ 与 $G/H_2$ 互换位置, 其余因子完全相同. 故由**定义 1.7.12 (同构序列)**, $S_3$ 与 $S_4$ 同构.

**再证 $S_1$ 与 $S_3$ 同构.** $S_1$ 与 $S_3$ 的首因子均为 $G/G_2$. 去掉首项后, 二者的尾段

$$
G_2\triangleright G_3\triangleright\cdots\triangleright G_t=\left\{e\right\}
\quad\text{与}\quad
G_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright K_r=\left\{e\right\}
$$

都是 $G_2$ 的合成序列. 由**定理 1.7.13 (若尔当-赫尔德定理)**, 群 $G_2$ 的这两个合成序列同构. 补上二者共同的首因子 $G/G_2$ 后, 由**定义 1.7.12 (同构序列)**, $S_1$ 与 $S_3$ 同构.

**同理证 $S_2$ 与 $S_4$ 同构.** $S_2$ 与 $S_4$ 的首因子均为 $G/H_2$; 尾段 $H_2\triangleright H_3\triangleright\cdots\triangleright\left\{e\right\}$ 与 $H_2\triangleright K_3\triangleright K_4\triangleright\cdots\triangleright\left\{e\right\}$ 都是 $H_2$ 的合成序列, 由**定理 1.7.13 (若尔当-赫尔德定理)** 它们同构, 补上共同首因子 $G/H_2$ 后, $S_2$ 与 $S_4$ 同构.

综上, $S_1\cong S_3\cong S_4\cong S_2$, 即四个合成序列彼此等价. $\blacksquare$
