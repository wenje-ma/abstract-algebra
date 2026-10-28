# week13

> **基础知识: 四元数与共轭**<br>四元数体 $H$ 中元素写成 $\alpha=a+bi+cj+dk$, $a,b,c,d\in\mathbb R$, 其共轭为 $\overline\alpha=a-bi-cj-dk$, 范数为 $N\left(\alpha\right)=\alpha\overline\alpha=a^{2}+b^{2}+c^{2}+d^{2}$. 共轭满足 $\overline{\alpha+\beta}=\overline\alpha+\overline\beta$, $\overline{\alpha\beta}=\overline\beta\,\overline\alpha$, $\overline{\overline\alpha}=\alpha$, 且实数的共轭为其自身. 范数 $N\left(\beta\right)$ 是实数, 故与任意四元数可交换.

> **基础知识: 欧氏范数的三角不等式**<br>把 $H$ 与 $\mathbb R^{4}$ 等同, 则 $N\left(\alpha\right)=\left\|\alpha\right\|^{2}$ (欧氏范数的平方). 对 $\mathbb R^{4}$ 中向量, 三角不等式 $\left\|\alpha+\beta\right\|\le\left\|\alpha\right\|+\left\|\beta\right\|$ 成立, 且等号成立当且仅当 $\alpha,\beta$ 实线性相关.

---

## 2.3-4

在四元数体 $H$ 中定义一个元素 $\alpha\in H$ 的范数为 $N\left(\alpha\right)=\alpha\overline\alpha$. 试证明:

(1) 对任何 $\alpha\in H$, $N\left(\alpha\right)\ge0$, 且 $N\left(\alpha\right)=0$ 当且仅当 $\alpha=0$;

(2) 对任何 $\alpha,\beta\in H$ 有

$$
\sqrt{N\left(\alpha+\beta\right)}\le\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)},
$$

且等号成立当且仅当 $\alpha,\beta$ 实线性相关;

(3) $N\left(\lambda\alpha\right)=\lambda^{2}N\left(\alpha\right)$, $\lambda\in\mathbb R$;

(4) $N\left(\overline\alpha\right)=N\left(\alpha\right)$;

(5) $N\left(\alpha\beta\right)=N\left(\alpha\right)N\left(\beta\right)$.

### 解答 2.3-4

设 $\alpha=a+bi+cj+dk$. 由**基础知识: 四元数与共轭**, 范数为

$$
N\left(\alpha\right)=\alpha\overline\alpha=a^{2}+b^{2}+c^{2}+d^{2}.
$$

**第 (1) 部分.** 因 $a,b,c,d\in\mathbb R$, 各项平方均非负, 故

$$
N\left(\alpha\right)=a^{2}+b^{2}+c^{2}+d^{2}\ge0.
$$

$N\left(\alpha\right)=0$ 当且仅当 $a^{2}+b^{2}+c^{2}+d^{2}=0$, 当且仅当 $a=b=c=d=0$, 即 $\alpha=0$. 故 (1) 得证.

**第 (2) 部分.** 把 $\alpha,\beta$ 看成 $\mathbb R^{4}$ 中的向量, 由**基础知识: 欧氏范数的三角不等式**, $N\left(\alpha\right)=\left\|\alpha\right\|^{2}$, 于是

$$
\sqrt{N\left(\alpha+\beta\right)}=\left\|\alpha+\beta\right\|\le\left\|\alpha\right\|+\left\|\beta\right\|=\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)}.
$$

且等号成立当且仅当 $\alpha,\beta$ 实线性相关 (由**基础知识: 欧氏范数的三角不等式**). 故 (2) 得证.

**第 (3) 部分.** 对 $\lambda\in\mathbb R$, $\lambda\alpha=\lambda a+\lambda b\,i+\lambda c\,j+\lambda d\,k$, 由**基础知识: 四元数与共轭**,

$$
N\left(\lambda\alpha\right)=\left(\lambda a\right)^{2}+\left(\lambda b\right)^{2}+\left(\lambda c\right)^{2}+\left(\lambda d\right)^{2}=\lambda^{2}\left(a^{2}+b^{2}+c^{2}+d^{2}\right)=\lambda^{2}N\left(\alpha\right).
$$

故 (3) 得证.

**第 (4) 部分.** 由**基础知识: 四元数与共轭**, $\overline\alpha=a-bi-cj-dk$, 故

$$
N\left(\overline\alpha\right)=a^{2}+\left(-b\right)^{2}+\left(-c\right)^{2}+\left(-d\right)^{2}=a^{2}+b^{2}+c^{2}+d^{2}=N\left(\alpha\right).
$$

故 (4) 得证.

**第 (5) 部分.** 由共轭的反序性质 $\overline{\alpha\beta}=\overline\beta\,\overline\alpha$ (见**基础知识: 四元数与共轭**), 以及 $N\left(\beta\right)=\beta\overline\beta$ 为实数而可与任意四元数交换, 得

$$
N\left(\alpha\beta\right)=\left(\alpha\beta\right)\overline{\left(\alpha\beta\right)}=\alpha\beta\overline\beta\,\overline\alpha=\alpha\left(\beta\overline\beta\right)\overline\alpha=N\left(\beta\right)\alpha\overline\alpha=N\left(\alpha\right)N\left(\beta\right).
$$

故 (5) 得证. $\blacksquare$
