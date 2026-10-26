# 作业 13

> **基础知识**（四元数与共轭）四元数体中元素写成 $\alpha=a+bi+cj+dk$, $a,b,c,d\in\mathbb R$, 其共轭为 $\bar\alpha=a-bi-cj-dk$, 范数
> $$
> N\left(\alpha\right)=\alpha\bar\alpha=a^2+b^2+c^2+d^2\in\mathbb R.
> $$
> 共轭满足 $\overline{\alpha+\beta}=\bar\alpha+\bar\beta$, $\overline{\alpha\beta}=\bar\beta\bar\alpha$, $\overline{\bar\alpha}=\alpha$, 且实数的共轭为其自身.

### 习题一

（习题 2.3-4）在四元数体 $H$ 中定义一个元素 $\alpha\in H$ 的范数为 $N\left(\alpha\right)=\alpha\bar\alpha$. 试证明:
(1)对任何 $\alpha\in H$, $N\left(\alpha\right)\ge0$, 且 $N\left(\alpha\right)=0$ 当且仅当 $\alpha=0$;
(2)对任何 $\alpha,\beta\in H$ 有

$$
\sqrt{N\left(\alpha+\beta\right)}\le\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)},
$$

且等号成立当且仅当 $\alpha,\beta$ 实线性相关;
(3)$N\left(\lambda\alpha\right)=\lambda^2N\left(\alpha\right)$, $\lambda\in\mathbb R$;
(4)$N\left(\bar\alpha\right)=N\left(\alpha\right)$;
(5)$N\left(\alpha\beta\right)=N\left(\alpha\right)N\left(\beta\right)$.

### 解答 习题一

设 $\alpha=a+bi+cj+dk$. 由共轭定义,

$$
N\left(\alpha\right)=\alpha\bar\alpha=a^2+b^2+c^2+d^2.
$$

(1)

$$
N\left(\alpha\right)=a^2+b^2+c^2+d^2\ge0.
$$

其为零当且仅当 $a=b=c=d=0$, 即 $\alpha=0$.

(2)把 $\alpha,\beta$ 看成 $\mathbb R^4$ 中的向量, 则 $N\left(\alpha\right)=\left\|\alpha\right\|^2$. 于是

$$
\sqrt{N\left(\alpha+\beta\right)}=\left\|\alpha+\beta\right\|\le\left\|\alpha\right\|+\left\|\beta\right\|=\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)}.
$$

等号成立当且仅当 $\alpha,\beta$ 实线性相关.

(3)

$$
N\left(\lambda\alpha\right)=\left(\lambda a\right)^2+\left(\lambda b\right)^2+\left(\lambda c\right)^2+\left(\lambda d\right)^2=\lambda^2\left(a^2+b^2+c^2+d^2\right)=\lambda^2N\left(\alpha\right).
$$

(4)$\bar\alpha=a-bi-cj-dk$, 故

$$
N\left(\bar\alpha\right)=a^2+\left(-b\right)^2+\left(-c\right)^2+\left(-d\right)^2=N\left(\alpha\right).
$$

(5)由共轭反序性质 $\overline{\alpha\beta}=\bar\beta\bar\alpha$, 且 $N\left(\beta\right)=\beta\bar\beta$ 为实数, 与任意四元数可交换,

$$
N\left(\alpha\beta\right)=\left(\alpha\beta\right)\overline{\left(\alpha\beta\right)}=\alpha\beta\bar\beta\bar\alpha=\alpha\left(\beta\bar\beta\right)\bar\alpha=N\left(\beta\right)\alpha\bar\alpha=N\left(\alpha\right)N\left(\beta\right).
$$

$\blacksquare$
