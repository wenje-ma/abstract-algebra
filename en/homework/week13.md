# week13

> **Basic Knowledge: Quaternions and Conjugation**<br>An element of the quaternion division ring $H$ is written $\alpha=a+bi+cj+dk$, $a,b,c,d\in\mathbb R$, with conjugate $\overline\alpha=a-bi-cj-dk$ and norm $N\left(\alpha\right)=\alpha\overline\alpha=a^{2}+b^{2}+c^{2}+d^{2}$. Conjugation satisfies $\overline{\alpha+\beta}=\overline\alpha+\overline\beta$, $\overline{\alpha\beta}=\overline\beta\,\overline\alpha$, $\overline{\overline\alpha}=\alpha$, and the conjugate of a real number is itself. The norm $N\left(\beta\right)$ is a real number, hence commutes with every quaternion.

> **Basic Knowledge: Triangle Inequality for the Euclidean Norm**<br>Identify $H$ with $\mathbb R^{4}$; then $N\left(\alpha\right)=\left\|\alpha\right\|^{2}$ (the square of the Euclidean norm). For vectors in $\mathbb R^{4}$ the triangle inequality $\left\|\alpha+\beta\right\|\le\left\|\alpha\right\|+\left\|\beta\right\|$ holds, with equality if and only if $\alpha,\beta$ are real-linearly dependent.

---

## 2.3-4

In the quaternion division ring $H$, define the norm of an element $\alpha\in H$ as $N\left(\alpha\right)=\alpha\overline\alpha$. Prove:

(1) For every $\alpha\in H$, $N\left(\alpha\right)\ge0$, and $N\left(\alpha\right)=0$ if and only if $\alpha=0$;

(2) For every $\alpha,\beta\in H$,

$$
\sqrt{N\left(\alpha+\beta\right)}\le\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)},
$$

with equality if and only if $\alpha,\beta$ are real-linearly dependent;

(3) $N\left(\lambda\alpha\right)=\lambda^{2}N\left(\alpha\right)$, $\lambda\in\mathbb R$;

(4) $N\left(\overline\alpha\right)=N\left(\alpha\right)$;

(5) $N\left(\alpha\beta\right)=N\left(\alpha\right)N\left(\beta\right)$.

### Solution 2.3-4

Write $\alpha=a+bi+cj+dk$. By **Basic Knowledge: Quaternions and Conjugation**, the norm is

$$
N\left(\alpha\right)=\alpha\overline\alpha=a^{2}+b^{2}+c^{2}+d^{2}.
$$

**Part (1).** Since $a,b,c,d\in\mathbb R$, each squared term is nonnegative, so

$$
N\left(\alpha\right)=a^{2}+b^{2}+c^{2}+d^{2}\ge0.
$$

$N\left(\alpha\right)=0$ if and only if $a^{2}+b^{2}+c^{2}+d^{2}=0$, if and only if $a=b=c=d=0$, i.e. $\alpha=0$. Hence (1) is proved.

**Part (2).** Viewing $\alpha,\beta$ as vectors in $\mathbb R^{4}$, by **Basic Knowledge: Triangle Inequality for the Euclidean Norm**, $N\left(\alpha\right)=\left\|\alpha\right\|^{2}$, so

$$
\sqrt{N\left(\alpha+\beta\right)}=\left\|\alpha+\beta\right\|\le\left\|\alpha\right\|+\left\|\beta\right\|=\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)}.
$$

Equality holds if and only if $\alpha,\beta$ are real-linearly dependent (by **Basic Knowledge: Triangle Inequality for the Euclidean Norm**). Hence (2) is proved.

**Part (3).** For $\lambda\in\mathbb R$, $\lambda\alpha=\lambda a+\lambda b\,i+\lambda c\,j+\lambda d\,k$; by **Basic Knowledge: Quaternions and Conjugation**,

$$
N\left(\lambda\alpha\right)=\left(\lambda a\right)^{2}+\left(\lambda b\right)^{2}+\left(\lambda c\right)^{2}+\left(\lambda d\right)^{2}=\lambda^{2}\left(a^{2}+b^{2}+c^{2}+d^{2}\right)=\lambda^{2}N\left(\alpha\right).
$$

Hence (3) is proved.

**Part (4).** By **Basic Knowledge: Quaternions and Conjugation**, $\overline\alpha=a-bi-cj-dk$, so

$$
N\left(\overline\alpha\right)=a^{2}+\left(-b\right)^{2}+\left(-c\right)^{2}+\left(-d\right)^{2}=a^{2}+b^{2}+c^{2}+d^{2}=N\left(\alpha\right).
$$

Hence (4) is proved.

**Part (5).** By the reverse-order property of conjugation $\overline{\alpha\beta}=\overline\beta\,\overline\alpha$ (see **Basic Knowledge: Quaternions and Conjugation**), and since $N\left(\beta\right)=\beta\overline\beta$ is real and hence commutes with every quaternion,

$$
N\left(\alpha\beta\right)=\left(\alpha\beta\right)\overline{\left(\alpha\beta\right)}=\alpha\beta\overline\beta\,\overline\alpha=\alpha\left(\beta\overline\beta\right)\overline\alpha=N\left(\beta\right)\alpha\overline\alpha=N\left(\alpha\right)N\left(\beta\right).
$$

Hence (5) is proved. $\blacksquare$
