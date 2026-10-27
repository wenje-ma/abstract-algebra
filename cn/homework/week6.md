# week6

> **基础知识: 偶置换与奇置换, 交错群**<br>当一个置换能表为奇(偶)数个对换的乘积时, 称为奇置换(偶置换). $n$ 元偶置换的全体 $A_n$ 是 $S_n$ 的正规子群, 称为 $n$ 元交错群, 且当 $n\ge2$ 时 $\left|A_n\right|=\frac{n!}{2}$.

> **基础知识: 轮换的共轭**<br>对任意 $\sigma\in S_n$ 与 $r$-轮换 $\left(i_1i_2\cdots i_r\right)$, 有 $\sigma\left(i_1i_2\cdots i_r\right)\sigma^{-1}=\left(\sigma\left(i_1\right)\sigma\left(i_2\right)\cdots\sigma\left(i_r\right)\right)$. 故 $S_n$ 中两个轮换共轭当且仅当它们长度相同, 特别地, 所有对换彼此共轭.

> **基础知识: 符号同态**<br>例 1.4.17 中的行列式同态给出 $\mathrm{sgn}:S_n\to\left\{1,-1\right\}$, $\sigma\mapsto\mathrm{sgn}\left(\sigma\right)$, 其中对换的符号为 $-1$; 若 $\sigma$ 表为 $m$ 个对换之积, 则 $\mathrm{sgn}\left(\sigma\right)=\left(-1\right)^{m}$; 特别地, $n$ 个不相交对换之积的符号为 $\left(-1\right)^{n}$, $\ker\mathrm{sgn}=A_n$.

> **基础知识: 交错群由 3-轮换生成**<br>当 $n\ge3$ 时, $A_n$ 由所有 3-轮换生成: 因 $\left(ij\right)\left(ik\right)=\left(jik\right)$, $\left(ij\right)\left(kl\right)=\left(ijk\right)\left(jkl\right)$, 两个对换之积是 3-轮换的乘积, 而 $A_n$ 中元可表为偶数个对换之积.

> **基础知识: 正规子群是共轭类的并**<br>若 $N\triangleleft G$, 则 $N$ 是 $G$ 中若干共轭类之并; 特别地, 若 $x\in N$, 则 $x$ 所在的共轭类含于 $N$.

> **基础知识: 对换的中心化子与对换的识别**<br>在 $S_n$ 中, 对换 $\left(ij\right)$ 的中心化子大小为 $2\left(n-2\right)!$; 当 $n\ne6$ 时, 对换构成 $S_n$ 中唯一的这样大小的二阶元共轭类, 故任一自同构把对换映为对换. 而当 $n=6$ 时 $S_6$ 有外自同构, 把对换映为 6-轮换的平方等二阶元.

> **基础知识: 群的中心与内自同构**<br>设 $G$ 为群, $\mathrm{Ad}:G\to\mathrm{Inn}\left(G\right)$, $a\mapsto\mathrm{Ad}_a$, 其中 $\mathrm{Ad}_a\left(g\right)=aga^{-1}$, 是满同态, $\ker\mathrm{Ad}=C\left(G\right)$ (G 的中心), 故由同态基本定理 $\mathrm{Inn}\left(G\right)\cong G/C\left(G\right)$. 当 $n\ge3$ 时 $S_n$ 的中心 $C\left(S_n\right)=\left\{e\right\}$, 故 $\mathrm{Inn}\left(S_n\right)\cong S_n$.

> **基础知识: 偶数阶群有二阶元**<br>若有限群 $G$ 的阶为偶数, 则 $G$ 中存在二阶元: 将 $G$ 的元素按互逆配对, $e$ 自成一对, 其余非二阶元两两配对, 因 $\left|G\right|$ 为偶数, 必有奇数个二阶元, 故存在非单位二阶元.

> **基础知识: $S_4$ 的共轭类**<br>$S_4$ 的共轭类及大小分别为: $\left\{e\right\}$ (1), 对换 (6), 对换之积 $\left(12\right)\left(34\right)$ 型 (3), 3-轮换 (8), 4-轮换 (6). 且 $K_4=\left\{e,\left(12\right)\left(34\right),\left(13\right)\left(24\right),\left(14\right)\left(23\right)\right\}$ 与 $A_4$ 都是 $S_4$ 的正规子群, $K_4$ 同构于克莱因四元群.

> **基础知识: $S_6$ 的外自同构**<br>$\mathrm{Out}\left(S_6\right)=\mathrm{Aut}\left(S_6\right)/\mathrm{Inn}\left(S_6\right)\cong\mathbb Z_2$, 故 $\left|\mathrm{Aut}\left(S_6\right)\right|=2\left|\mathrm{Inn}\left(S_6\right)\right|=2\cdot6!=1440$.

> **定理 1.2.22 (拉格朗日定理)**<br>设 $G$ 是有限群, $H<G$, 则 $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$.

> **定理 1.4.10 (凯莱定理)**<br>任何群 $G$ 与对称群 $S_G$ 的一个子群同构; 事实上映射 $L:G\to L_G$, $a\mapsto L_a$ 是单同态, 其中 $L_a\left(g\right)=ag$ 为左平移.

> **引理 1.4.13**<br>设 $f:G\to G'$ 为群同态, 则 $\mathrm{Im}\,f<G'$, $\ker f\triangleleft G$.

> **例 1.4.17**<br>设 $V$ 是数域 $P$ 上的 $n$ 维线性空间, 则映射 $\det\circ\pi:S_n\to P^{*}$, $\sigma\mapsto\det\left(\pi_\sigma\right)$ 是群同态, 其像集为 $\left\{1,-1\right\}$ (当 $n>1$ 时), 该同态的核记为 $A_n$.

> **定理 1.4.19 (群的同态基本定理)**<br>设 $f:G\to G'$ 是群的满同态, 则 $G/\ker f\cong G'$.

> **定义 1.6.1 (轮换)**<br>设 $\left\{i_1,i_2,\cdots,i_r\right\}\subseteq\left\{1,2,\cdots,n\right\}$. 若 $\sigma\in S_n$ 满足 $\sigma\left(i_1\right)=i_2$, $\sigma\left(i_2\right)=i_3$, ..., $\sigma\left(i_r\right)=i_1$, 且 $\sigma$ 固定其余文字, 则称 $\sigma$ 为一个 $r$-轮换, 记为 $\sigma=\left(i_1i_2\cdots i_r\right)$. 特别地, $2$-轮换称为对换.

> **定理 1.6.4 (轮换分解)**<br>$S_n$ 中的任何元素 $\sigma$ 都可表为 $S_n$ 中一些不相交轮换之积; 如果不计次序, 表法是唯一的.

> **引理 1.6.7 (轮换的对换分解)**<br>任一个 $r$-轮换都可写成 $r-1$ 个对换的乘积: $\left(i_1i_2\cdots i_r\right)=\left(i_1i_r\right)\left(i_1i_{r-1}\right)\cdots\left(i_1i_3\right)\left(i_1i_2\right)$.

> **命题 1.6.8**<br>任一 $n$ 元置换都可以表为一些对换的乘积.

> **定理 1.6.9 (交错群的单性)**<br>当 $n\ge5$ 时, $A_n$ 是单群.

---

## 1.6-5

证明:

$$
S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle,\quad A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle.
$$

### 解答 1.6-5

**第一部分: 证明 $S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$.** 由**命题 1.6.8**, $S_n$ 由所有对换生成. 对任意对换 $\left(ij\right)$, 其中 $i\ne1$, $j\ne1$, 由**基础知识: 轮换的共轭**, 取 $\sigma=\left(1i\right)$, 有 $\left(1i\right)\left(1j\right)\left(1i\right)=\left(\sigma\left(1\right)\sigma\left(j\right)\right)=\left(i,j\right)=\left(ij\right)$. 故任意对换 $\left(ij\right)$ 都可由 $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ 表出, 因此 $S_n\subseteq\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$; 反向包含显然, 故 $S_n=\left\langle\left(12\right),\left(13\right),\cdots,\left(1n\right)\right\rangle$.

**第二部分: 证明 $S_n=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle$.** 记 $\sigma=\left(12\cdots n\right)$. 由**基础知识: 轮换的共轭**, 对 $k=1,2,\cdots,n-1$,

$$
\sigma^{k-1}\left(12\right)\sigma^{-\left(k-1\right)}=\left(\sigma^{k-1}\left(1\right)\sigma^{k-1}\left(2\right)\right)=\left(k,k+1\right),
$$

故相邻对换 $\left(12\right),\left(23\right),\cdots,\left(n-1,n\right)$ 均属于 $\left\langle\left(12\right),\sigma\right\rangle$. 而相邻对换生成 $S_n$ (由**命题 1.6.8**, 任何对换 $\left(ij\right)$ 可表为相邻对换之积), 故 $S_n\subseteq\left\langle\left(12\right),\sigma\right\rangle$; 反向包含显然, 故 $S_n=\left\langle\left(12\right),\left(12\cdots n\right)\right\rangle$.

**第三部分: 证明 $A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$.** 由**基础知识: 交错群由 3-轮换生成**, $A_n$ 由所有 3-轮换生成. 下面证明任意 3-轮换都属于 $\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$.

(1) 含 $1$ 和 $2$ 的 3-轮换即为 $\left(12k\right)$ 或其逆, 已在生成集中.

(2) 含 $1$ 但不含 $2$ 的 3-轮换 $\left(1jk\right)$ ($j,k\ne2$): 直接计算 $\left(12k\right)\left(12j\right)^{-1}=\left(12k\right)\left(1j2\right)=\left(1jk\right)$, 故 $\left(1jk\right)$ 属于生成群.

(3) 不含 $1$ 的 3-轮换 $\left(ijk\right)$: 由 (2), $\left(1ij\right)$ 与 $\left(1ik\right)$ 均属于生成群, 于是 $\left(1ij\right)^{-1}\left(1ik\right)=\left(1ji\right)\left(1ik\right)=\left(ikj\right)$. 因 $\left(ikj\right)=\left(ijk\right)^{-1}$, 故 $\left(ijk\right)$ 属于生成群.

故所有 3-轮换都属于 $\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$, 从而 $A_n\subseteq\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$. 反之, 各生成元 $\left(12k\right)$ 都是 3-轮换, 是偶置换 (**基础知识: 偶置换与奇置换, 交错群**), 故属于 $A_n$, 反向包含成立. 因此 $A_n=\left\langle\left(123\right),\left(124\right),\cdots,\left(12n\right)\right\rangle$. $\blacksquare$

---

## 1.6-6

证明: $S_n$ 的非平凡正规子群为 $A_n$ 或 $K_4$ (当 $n=4$ 时).

### 解答 1.6-6

设 $N\triangleleft S_n$, $N\ne\left\{e\right\}$, $N\ne S_n$.

**情形 $n\ge5$.** 由**定理 1.6.9 (交错群的单性)**, $A_n$ 是单群. 因 $N\triangleleft S_n$ 且 $A_n\triangleleft S_n$ (由**基础知识: 偶置换与奇置换, 交错群**), 交 $N\cap A_n\triangleleft A_n$, 故由 $A_n$ 的单性, $N\cap A_n=\left\{e\right\}$ 或 $A_n$.

若 $N\cap A_n=A_n$, 则 $A_n\subseteq N$. 因 $\left|A_n\right|=\frac{n!}{2}$, $A_n$ 在 $S_n$ 中的指数为 $2$ (**基础知识: 偶置换与奇置换, 交错群**), 故包含 $A_n$ 的子群只能是 $A_n$ 或 $S_n$; 而 $N\ne S_n$, 故 $N=A_n$.

若 $N\cap A_n=\left\{e\right\}$, 则对任意 $x,y\in N\setminus\left\{e\right\}$, 因 $x,y$ 都是奇置换, $xy$ 是偶置换, 故 $xy\in N\cap A_n=\left\{e\right\}$, 于是 $y=x^{-1}$, 即 $\left|N\right|\le2$, 且 $N$ 的非单位元是二阶元. 又由**基础知识: 正规子群是共轭类的并**, $N$ 是若干共轭类之并; 因 $n\ge3$ 时 $S_n$ 的中心平凡 (**基础知识: 群的中心与内自同构**), $N$ 的非单位元 $x\ne e$ 所在的共轭类大小大于 $1$, 与 $\left|N\right|\le2$ 矛盾. 故 $N\cap A_n=\left\{e\right\}$ 不可能.

因此 $n\ge5$ 时, $S_n$ 的非平凡正规子群只有 $A_n$.

**情形 $n=4$.** $\left|S_4\right|=24$, $\left|A_4\right|=12$, $A_4\triangleleft S_4$. 由**基础知识: $S_4$ 的共轭类**, $S_4$ 的共轭类大小分别为 $1,6,3,8,6$; 由**基础知识: 正规子群是共轭类的并**及**定理 1.2.22 (拉格朗日定理)**, 正规子群的阶必为若干共轭类大小之和且整除 $24$, 可能的阶为 $1,4,12,24$, 对应正规子群 $\left\{e\right\}$, $K_4$, $A_4$, $S_4$. 故非平凡正规子群为 $A_4$ 与 $K_4$.

**情形 $n=3$.** $\left|S_3\right|=6$, $\left|A_3\right|=3$, $A_3\triangleleft S_3$ 且指数为 $2$. 由**基础知识: 正规子群是共轭类的并**, $S_3$ 的共轭类大小分别为 $1,3,2$, 可能组成正规子群的阶为 $1,3,6$, 故正规子群为 $\left\{e\right\},A_3,S_3$, 非平凡者为 $A_3$.

**情形 $n\le2$.** $S_n$ 无非平凡正规子群.

综上, $S_n$ 的非平凡正规子群为 $A_n$ (对所有 $n\ge3$), 以及 $n=4$ 时的 $K_4$. $\blacksquare$

---

## 1.6-11

设 $\left|G\right|=2n$, 其中 $n$ 为奇数. 证明: $G$ 有指数为 $2$ 的正规子群.

### 解答 1.6-11

**第一步: 构造群同态 $\psi:G\to\left\{1,-1\right\}$.** 由**定理 1.4.10 (凯莱定理)**, 左正则表示 $\lambda:G\to S_G$, $g\mapsto L_g$ (其中 $L_g\left(x\right)=gx$) 是单同态; 视 $S_G$ 为 $S_{2n}$ (因 $\left|G\right|=2n$). 由**例 1.4.17** 及**基础知识: 符号同态**, 符号同态 $\mathrm{sgn}:S_{2n}\to\left\{1,-1\right\}$ 是群同态. 复合得 $\psi=\mathrm{sgn}\circ\lambda:G\to\left\{1,-1\right\}$ 是群同态.

**第二步: 证明 $\psi$ 是满射.** 由**基础知识: 偶数阶群有二阶元**, $G$ 中存在二阶元 $a$ (因 $\left|G\right|=2n$ 为偶数). 则 $\lambda\left(a\right)=L_a$, 且对任意 $x\in G$, $L_a^2\left(x\right)=a^2x=x$, 故 $L_a$ 是对合; 又 $a\ne e$, 若 $L_a\left(x\right)=x$ 即 $ax=x$, 则 $a=e$, 矛盾, 故 $L_a$ 无不动点. 因此 $L_a$ 是 $G$ (共 $2n$ 个文字) 上的 $n$ 个不相交对换之积, 由**基础知识: 符号同态**, $\mathrm{sgn}\left(L_a\right)=\left(-1\right)^{n}=-1$ (因 $n$ 为奇数). 故 $\psi\left(a\right)=-1$, 而 $\psi\left(e\right)=1$, 于是 $\psi:G\to\left\{1,-1\right\}$ 是满同态.

**第三步: 取核得指数为 $2$ 的正规子群.** 令 $H=\ker\psi$. 由**引理 1.4.13**, $H\triangleleft G$. 由**定理 1.4.19 (群的同态基本定理)**, $G/H\cong\left\{1,-1\right\}$, 故 $\left|G/H\right|=2$, 即 $\left[G:H\right]=2$. 因此 $G$ 有指数为 $2$ 的正规子群 $H$. $\blacksquare$

---

## 1.6-14

证明: 当 $n\ne2,6$ 时, $\mathrm{Aut}\left(S_n\right)\cong S_n$. 并求 $\mathrm{Aut}\left(S_2\right)$ 与 $\mathrm{Aut}\left(S_6\right)$.

### 解答 1.6-14

**先证 $n\ne2,6$ 时 $\mathrm{Aut}\left(S_n\right)\cong S_n$.** 由**基础知识: 群的中心与内自同构**, $\mathrm{Inn}\left(S_n\right)\cong S_n/C\left(S_n\right)$, 而当 $n\ge3$ 时 $C\left(S_n\right)=\left\{e\right\}$, 故 $\mathrm{Inn}\left(S_n\right)\cong S_n$. 于是只需证明 $\mathrm{Aut}\left(S_n\right)=\mathrm{Inn}\left(S_n\right)$, 即任一自同构都是内自同构.

设 $\varphi\in\mathrm{Aut}\left(S_n\right)$. 自同构保持元素的阶, 故二阶元 (对合) 映为对合. 由**基础知识: 对换的中心化子与对换的识别**, 当 $n\ne6$ 时, $S_n$ 中对换是唯一的这样的二阶元共轭类 (其中心化子大小为 $2\left(n-2\right)!$), 而自同构保持共轭类与中心化子大小, 故 $\varphi$ 必将对换映为对换.

设 $\varphi\left(12\right)=\left(ab\right)$. 用内自同构 $\mathrm{Ad}_{\sigma}$ 复合 $\varphi$, 其中 $\sigma\in S_n$ 满足 $\sigma\left(a\right)=1$, $\sigma\left(b\right)=2$, 则 $\mathrm{Ad}_{\sigma}\varphi\left(12\right)=\left(\sigma\left(a\right)\sigma\left(b\right)\right)=\left(12\right)$. 故可不妨设 $\varphi\left(12\right)=\left(12\right)$.

对 $k=3,\cdots,n$, 因 $\left(12\right)\left(1k\right)=\left(1k2\right)$ 是 3-轮换, 阶为 $3$, 故 $\varphi\left(1k\right)$ 是与 $\varphi\left(12\right)=\left(12\right)$ 的乘积为 3-轮换的对换, 因而 $\varphi\left(1k\right)$ 必与 $\left(12\right)$ 恰好共享一个文字, 即 $\varphi\left(1k\right)=\left(1,j_k\right)$ 或 $\left(2,j_k\right)$ ($j_k\ne1,2$). 若存在 $k$ 使 $\varphi\left(1k\right)=\left(2,j_k\right)$, 用保持 $\left(12\right)$ 不变的内自同构 $\mathrm{Ad}_{\left(12\right)}$ (即交换文字 $1,2$) 复合, 可统一把每个 $\varphi\left(1k\right)$ 写成 $\left(1,\sigma\left(k\right)\right)$ 的形式, 其中 $\sigma\in S_{n-1}$ 是 $\left\{3,\cdots,n\right\}$ 的一个排列 (保持 $1,2$ 不动). 于是 $\varphi$ 在生成元 $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ 上的作用等于内自同构 $\mathrm{Ad}_{\sigma}$ 的作用.

由**习题 1.6-5 第一部分**, $\left(12\right),\left(13\right),\cdots,\left(1n\right)$ 生成 $S_n$, 故 $\varphi$ 与 $\mathrm{Ad}_{\sigma}$ 在生成元上一致, 从而在 $S_n$ 上一致, 即 $\varphi=\mathrm{Ad}_{\sigma}\in\mathrm{Inn}\left(S_n\right)$.

上述证明在 $n=6$ 时失效, 因 $S_6$ 存在外自同构 (由**基础知识: 对换的中心化子与对换的识别**与**基础知识: $S_6$ 的外自同构**). 故当 $n\ne2,6$ 时,

$$
\mathrm{Aut}\left(S_n\right)=\mathrm{Inn}\left(S_n\right)\cong S_n.
$$

**求 $\mathrm{Aut}\left(S_2\right)$.** $S_2=\left\{e,\left(12\right)\right\}$ 是二阶循环群, 自同构必须保持单位元 $e$, 故 $\mathrm{Aut}\left(S_2\right)=\left\{\mathrm{id}\right\}$ 是平凡群.

**求 $\mathrm{Aut}\left(S_6\right)$.** 由**基础知识: $S_6$ 的外自同构**, $\mathrm{Out}\left(S_6\right)\cong\mathbb Z_2$ 且 $\left|\mathrm{Inn}\left(S_6\right)\right|=\left|S_6\right|=720$ (因 $C\left(S_6\right)=\left\{e\right\}$), 故 $\left|\mathrm{Aut}\left(S_6\right)\right|=\left|\mathrm{Out}\left(S_6\right)\right|\cdot\left|\mathrm{Inn}\left(S_6\right)\right|=2\cdot720=1440$. $\blacksquare$
