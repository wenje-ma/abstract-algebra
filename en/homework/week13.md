# Assignment 13

> **Basic Knowledge** (Quaternions and Conjugation) Elements of the quaternion division ring are written as $\alpha=a+bi+cj+dk$, $a,b,c,d\in\mathbb R$, with conjugate $\overline\alpha=a-bi-cj-dk$ and norm
> $$
> N\left(\alpha\right)=\alpha\overline\alpha=a^2+b^2+c^2+d^2\in\mathbb R.
> $$
> Conjugation satisfies $\overline{\alpha+\beta}=\overline\alpha+\overline\beta$, $\overline{\alpha\beta}=\overline\beta\overline\alpha$, $\overline{\overline\alpha}=\alpha$, and the conjugate of a real number is itself.

### Problem 1

(Problem 2.3-4) In the quaternion division ring $H$, define the norm of an element $\alpha\in H$ by $N\left(\alpha\right)=\alpha\overline\alpha$. Prove that:
(1) for any $\alpha\in H$, $N\left(\alpha\right)\ge0$, and $N\left(\alpha\right)=0$ if and only if $\alpha=0$;
(2) for any $\alpha,\beta\in H$,

$$
\sqrt{N\left(\alpha+\beta\right)}\le\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)},
$$

with equality if and only if $\alpha,\beta$ are real-linearly dependent;
(3) $N\left(\lambda\alpha\right)=\lambda^2N\left(\alpha\right)$ for $\lambda\in\mathbb R$;
(4) $N\left(\overline\alpha\right)=N\left(\alpha\right)$;
(5) $N\left(\alpha\beta\right)=N\left(\alpha\right)N\left(\beta\right)$.

### Solution to Problem 1

Write $\alpha=a+bi+cj+dk$. By the definition of conjugation,

$$
N\left(\alpha\right)=\alpha\overline\alpha=a^2+b^2+c^2+d^2.
$$

(1)

$$
N\left(\alpha\right)=a^2+b^2+c^2+d^2\ge0.
$$

It is zero if and only if $a=b=c=d=0$, i.e. $\alpha=0$.

(2) Regard $\alpha,\beta$ as vectors in $\mathbb R^4$; then $N\left(\alpha\right)=\left\|\alpha\right\|^2$. Hence

$$
\sqrt{N\left(\alpha+\beta\right)}=\left\|\alpha+\beta\right\|\le\left\|\alpha\right\|+\left\|\beta\right\|=\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)}.
$$

Equality holds if and only if $\alpha,\beta$ are real-linearly dependent.

(3)

$$
N\left(\lambda\alpha\right)=\left(\lambda a\right)^2+\left(\lambda b\right)^2+\left(\lambda c\right)^2+\left(\lambda d\right)^2=\lambda^2\left(a^2+b^2+c^2+d^2\right)=\lambda^2N\left(\alpha\right).
$$

(4) $\overline\alpha=a-bi-cj-dk$, so

$$
N\left(\overline\alpha\right)=a^2+\left(-b\right)^2+\left(-c\right)^2+\left(-d\right)^2=N\left(\alpha\right).
$$

(5) By the reverse-order property of conjugation, $\overline{\alpha\beta}=\overline\beta\overline\alpha$, and $N\left(\beta\right)=\beta\overline\beta$ is a real number and commutes with any quaternion, so

$$
N\left(\alpha\beta\right)=\left(\alpha\beta\right)\overline{\left(\alpha\beta\right)}=\alpha\beta\overline\beta\overline\alpha=\alpha\left(\beta\overline\beta\right)\overline\alpha=N\left(\beta\right)\alpha\overline\alpha=N\left(\alpha\right)N\left(\beta\right).
$$

$\blacksquare$
