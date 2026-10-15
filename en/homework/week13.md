# Assignment 13

> **Basic Knowledge** (Quaternions and Conjugation) Elements of the quaternion division ring are written as $\alpha=a+bi+cj+dk$, $a,b,c,d\in\mathbb R$, with conjugate $\bar\alpha=a-bi-cj-dk$ and norm
> $$
> N\left(\alpha\right)=\alpha\bar\alpha=a^2+b^2+c^2+d^2\in\mathbb R.
> $$
> Conjugation satisfies $\overline{\alpha+\beta}=\bar\alpha+\bar\beta$, $\overline{\alpha\beta}=\bar\beta\bar\alpha$, $\overline{\bar\alpha}=\alpha$, and the conjugate of a real number is itself.

### Problem 1

(Problem 2.3-4) In the quaternion division ring $H$, define the norm of an element $\alpha\in H$ by $N\left(\alpha\right)=\alpha\bar\alpha$. Prove that:
(1) for any $\alpha\in H$, $N\left(\alpha\right)\ge0$, and $N\left(\alpha\right)=0$ if and only if $\alpha=0$;
(2) for any $\alpha,\beta\in H$,

$$
\sqrt{N\left(\alpha+\beta\right)}\le\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)},
$$

with equality if and only if $\alpha,\beta$ are real-linearly dependent;
(3) $N\left(\lambda\alpha\right)=\lambda^2N\left(\alpha\right)$ for $\lambda\in\mathbb R$;
(4) $N\left(\bar\alpha\right)=N\left(\alpha\right)$;
(5) $N\left(\alpha\beta\right)=N\left(\alpha\right)N\left(\beta\right)$.

### Solution to Problem 1

Write $\alpha=a+bi+cj+dk$. By the definition of conjugation,

$$
\begin{aligned}N\left(\alpha\right)&=\alpha\bar\alpha\\&=a^2+b^2+c^2+d^2.\end{aligned}
$$

(1)

$$
N\left(\alpha\right)=a^2+b^2+c^2+d^2\ge0.
$$

It is zero if and only if $a=b=c=d=0$, i.e. $\alpha=0$.

(2) Regard $\alpha,\beta$ as vectors in $\mathbb R^4$; then $N\left(\alpha\right)=\left\|\alpha\right\|^2$. Hence

$$
\begin{aligned}\sqrt{N\left(\alpha+\beta\right)}&=\left\|\alpha+\beta\right\|\\&\le\left\|\alpha\right\|+\left\|\beta\right\|\\&=\sqrt{N\left(\alpha\right)}+\sqrt{N\left(\beta\right)}.\end{aligned}
$$

Equality holds if and only if $\alpha,\beta$ are real-linearly dependent.

(3)

$$
\begin{aligned}N\left(\lambda\alpha\right)&=\left(\lambda a\right)^2+\left(\lambda b\right)^2+\left(\lambda c\right)^2+\left(\lambda d\right)^2\\&=\lambda^2\left(a^2+b^2+c^2+d^2\right)\\&=\lambda^2N\left(\alpha\right).\end{aligned}
$$

(4) $\bar\alpha=a-bi-cj-dk$, so

$$
\begin{aligned}N\left(\bar\alpha\right)&=a^2+\left(-b\right)^2+\left(-c\right)^2+\left(-d\right)^2\\&=N\left(\alpha\right).\end{aligned}
$$

(5) By the reverse-order property of conjugation, $\overline{\alpha\beta}=\bar\beta\bar\alpha$, and $N\left(\beta\right)=\beta\bar\beta$ is a real number and commutes with any quaternion, so

$$
\begin{aligned}N\left(\alpha\beta\right)&=\left(\alpha\beta\right)\overline{\left(\alpha\beta\right)}\\&=\alpha\beta\bar\beta\bar\alpha\\&=\alpha\left(\beta\bar\beta\right)\bar\alpha\\&=N\left(\beta\right)\alpha\bar\alpha\\&=N\left(\alpha\right)N\left(\beta\right).\end{aligned}
$$

$\blacksquare$
