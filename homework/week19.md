# 作业 19

> **定理 3.1.17**（模的同态基本定理）设 $\phi$ 为模 $M_1$ 到 $M_2$ 的满同态, 则商模 $M_1/\ker\phi$ 与 $M_2$ 同构; 且若 $N_1$ 是 $M_1$ 的包含 $\ker\phi$ 的子模, 则 $M_1/N_1\cong M_2/\phi\left(N_1\right)$.

> **命题 3.1.16**（同态的核与像）模同态 $\phi:M_1\to M_2$ 的核 $\ker\phi$ 是 $M_1$ 的子模, 同态像 $\operatorname{Im}\phi$ 是 $M_2$ 的子模.

> **定理 3.1.10**（直和判据）
>
> 设 $M_1,\cdots,M_s$ 为 $R$-模 $M$ 的子模, 则 $M=M_1\oplus\cdots\oplus M_s$ 当且仅当
>
> (1) $M=M_1+\cdots+M_s$;
>
> (2) 对任何 $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

### 习题一

（习题 3.1-11）设 $M$ 为模, $M_1,M_2$ 都是 $M$ 的子模. 试证明:

（1）若 $M_1\subset M_2$, 则 $M/M_2\cong\left(M/M_1\right)/\left(M_2/M_1\right)$;

（2）如果 $M=M_1\oplus M_2$, 则有 $M_1\cong\left(M_1+M_2\right)/M_2$, $M_2\cong\left(M_1+M_2\right)/M_1$.

### 解答 习题一

（1）定义映射 $\pi:M/M_1\to M/M_2$ 为

$$
\pi\left(m+M_1\right)=m+M_2.
$$

它是良定义的: 若 $m+M_1=m'+M_1$, 则 $m-m'\in M_1\subset M_2$, 故 $m+M_2=m'+M_2$. 它显然是模满同态. 求其核:

$$
\begin{aligned}\ker\pi&=\left\{m+M_1\mid m\in M_2\right\}\\&=M_2/M_1.\end{aligned}
$$

由**定理 3.1.17**（模的同态基本定理）,

$$
\begin{aligned}\left(M/M_1\right)/\left(M_2/M_1\right)&=M/\ker\pi\\&\cong\operatorname{Im}\pi\\&=M/M_2.\end{aligned}
$$

（2）考虑商映射 $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$ 在子模 $M_1$ 上的限制 $\rho|_{M_1}$. 它是满同态: 任一元素 $m_1+m_2+M_2=m_1+M_2$ 都是 $m_1\in M_1$ 的像. 其核为

$$
\begin{aligned}\ker\rho|_{M_1}&=\left\{m_1\in M_1\mid m_1\in M_2\right\}\\&=M_1\cap M_2.\end{aligned}
$$

因 $M=M_1\oplus M_2$ 为内直和, 由**定理 3.1.10**（直和判据）, $M_1\cap M_2=\left\{0\right\}$. 再由**定理 3.1.17**,

$$
\begin{aligned}M_1/\left(M_1\cap M_2\right)&=M_1\\&\cong\left(M_1+M_2\right)/M_2.\end{aligned}
$$

同理, $M_2\cong\left(M_1+M_2\right)/M_1$. $\blacksquare$

### 习题二

（习题 3.1-12）设 $M$ 为模, $M_1,M_2$ 是 $M$ 的子模, 试证明 $\left(M_1+M_2\right)/M_2\cong M_1/\left(M_1\cap M_2\right)$.

### 解答 习题二

取商映射 $\rho:M_1+M_2\to\left(M_1+M_2\right)/M_2$, 限制到 $M_1$ 上得到 $\phi=\rho|_{M_1}:M_1\to\left(M_1+M_2\right)/M_2$.

先证 $\phi$ 是满同态. 任一形如 $m_1+m_2+M_2$ 的陪集等于 $m_1+M_2$, 即 $\phi\left(m_1\right)$, 故 $\phi$ 满.

再求核. 由**命题 3.1.16**（同态的核与像）,

$$
\begin{aligned}\ker\phi&=\left\{m_1\in M_1\mid m_1\in M_2\right\}\\&=M_1\cap M_2.\end{aligned}
$$

由**定理 3.1.17**（模的同态基本定理）,

$$
\begin{aligned}M_1/\ker\phi&=M_1/\left(M_1\cap M_2\right)\\&\cong\left(M_1+M_2\right)/M_2.\end{aligned}
$$

此即第二同构定理. $\blacksquare$

### 习题三

（习题 3.1-13）设 $M$ 为模, $M_1,M_2,\cdots,M_s$ 为 $M$ 的子模. 试证明 $M=M_1\oplus\cdots\oplus M_s$ 当且仅当

(1) $M=M_1+M_2+\cdots+M_s$;

(2) 对任何 $2\le j\le s$, $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

### 解答 习题三

**必要性** 设 $M=M_1\oplus\cdots\oplus M_s$ 为内直和, 则 (1) 显然. 若 $x\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)$, 则 $x$ 既可写成 $M_j$ 中元素, 又可写成 $M_1,\cdots,M_{j-1}$ 中元素之和, 这给出 $0$ 的一个非平凡表示（除 $M_j$ 分量外其余分量和为 $-x$）, 与直和分解的唯一性矛盾. 故 $M_j\cap\left(M_1+\cdots+M_{j-1}\right)=\left\{0\right\}$.

**充分性** 设 (1)(2) 成立. 只需证 $M$ 中零元素的表示唯一. 设

$$
m_1+m_2+\cdots+m_s=0,\  m_i\in M_i.
$$

设 $j$ 为最大的使 $m_j\ne0$ 的下标, 则 $j\ge2$（否则 $m_1=0$）. 移项得

$$
\begin{aligned}m_j&=-\left(m_1+\cdots+m_{j-1}\right)\\&\in M_j\cap\left(M_1+\cdots+M_{j-1}\right)\\&=\left\{0\right\},\end{aligned}
$$

故 $m_j=0$, 矛盾. 因此所有 $m_i=0$, 零元素表示唯一. 由**定理 3.1.10**（直和判据）, $M=M_1\oplus\cdots\oplus M_s$. $\blacksquare$

### 习题四

（习题 3.1-14）试问将上题的条件 (2) 改为 $M_i\cap M_j=\left\{0\right\}$, $\forall i\ne j$, 结论还成立吗？说明理由.

### 解答 习题四

结论不成立. 两两交为零不能保证内直和分解.

反例. 取数域 $\mathbb R$ 上二维线性空间 $M=\mathbb R^2$ 作为 $\mathbb R$-模, 基为 $e_1,e_2$. 令 $M_1=\mathbb R e_1$, $M_2=\mathbb R e_2$, $M_3=\mathbb R\left(e_1+e_2\right)$.

它们都是 $M$ 的一维子空间. 任意两个不同的一维子空间之交为零, 即

$$
M_i\cap M_j=\left\{0\right\},\  i\ne j.
$$

且 $M_1+M_2+M_3=\mathbb R e_1+\mathbb R e_2=M$, 即条件 (1) 成立. 但存在非平凡关系

$$
e_1+e_2-\left(e_1+e_2\right)=0,
$$

其中 $e_1\in M_1$, $e_2\in M_2$, $-\left(e_1+e_2\right)\in M_3$, 三项均非零, 故零元素表示不唯一, $M\ne M_1\oplus M_2\oplus M_3$.

因此两两交为零只是直和的必要条件而非充分条件, 不能替代上题的嵌套交条件. $\blacksquare$

### 习题五

（习题 3.1-15）设 $M$ 为模, $M_1,M_2,\cdots,M_s$ 为 $M$ 的子模, 且 $M=M_1\oplus M_2\oplus\cdots\oplus M_s$, 又 $N$ 是 $M$ 的子模, 且 $N=N_1\oplus N_2\oplus\cdots\oplus N_s$, 其中 $N_i\subset M_i$, $i=1,2,\cdots,s$. 试证明 $M/N\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s$.

### 解答 习题五

任一 $m\in M$ 可唯一写成 $m=m_1+\cdots+m_s$, $m_i\in M_i$. 定义映射

$$
\phi:M\to M_1/N_1\oplus\cdots\oplus M_s/N_s,\  \phi\left(m_1+\cdots+m_s\right)=\left(m_1+N_1,\cdots,m_s+N_s\right).
$$

由直和分解的唯一性, $\phi$ 是良定义的模同态.

它是满同态: 任取 $\left(m_1'+N_1,\cdots,m_s'+N_s\right)$, 取 $m=m_1'+\cdots+m_s'\in M$, 则 $\phi\left(m\right)$ 即为该元素.

求核. 由**命题 3.1.16**（同态的核与像）,

$$
\begin{aligned}\ker\phi&=\left\{m_1+\cdots+m_s\mid m_i+N_i=0,\ 1\le i\le s\right\}\\&=\left\{m_1+\cdots+m_s\mid m_i\in N_i\right\}\\&=N_1\oplus\cdots\oplus N_s\\&=N.\end{aligned}
$$

由**定理 3.1.17**（模的同态基本定理）,

$$
M/N=M/\ker\phi\cong M_1/N_1\oplus M_2/N_2\oplus\cdots\oplus M_s/N_s.
$$

$\blacksquare$
