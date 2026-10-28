# week24

> **Basic Knowledge: Universal Property of the Field of Fractions**<br>Let $R$ be an integral domain and $E$ its field of fractions. Given any automorphism $\sigma$ of $R$, define $\overline\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\sigma\left(b\right)^{-1}$; then $\overline\sigma$ is well-defined and is an automorphism of $E$.

> **Lemma 4.1.9 (Field Homomorphisms Are Injective)**<br>A field homomorphism $\varphi:F\to E$ is always injective. In particular, a field automorphism preserves the operations and $1$, and hence fixes every element of the prime field ($\mathbb Q$ or $\mathbb F_p$).

> **Definition 4.1.15 (Degree of an Extension)**<br>Let $E$ be an extension of $F$. The dimension of $E$ as an $F$-vector space is called the degree of $E$ over $F$, written $\left[E:F\right]$. If $\left[E:F\right]< \infty$, $E$ is a finite extension of $F$; otherwise it is an infinite extension.

> **Theorem 4.1.16 (Tower Law for Extension Degrees)**<br>If both $K/F$ and $E/K$ are finite extensions, then $E/F$ is also finite, and $\left[E:F\right]=\left[E:K\right]\left[K:F\right]$.

> **Lemma 4.2.1 (Finite Extensions Are Algebraic)**<br>If $E/F$ is a finite extension, then every element of $E$ is algebraic over $F$. Equivalently, if $E$ contains a transcendental element over $F$, then $E/F$ must be an infinite extension.

---

## 4.1-4

Find the degrees of the following field extensions:

(1) $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\right]$;

(2) $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]$.

### Solution 4.1-4

Set $\alpha=\sqrt2+\sqrt3$. First show $\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$.

On one hand, $\alpha\in\mathbb Q\left(\sqrt2,\sqrt3\right)$, so $\mathbb Q\left(\alpha\right)\subseteq\mathbb Q\left(\sqrt2,\sqrt3\right)$.

On the other hand, since $\left(\sqrt2+\sqrt3\right)\left(\sqrt3-\sqrt2\right)=3-2=1$, we have $\alpha^{-1}=\sqrt3-\sqrt2$. Hence $\sqrt2=\frac{\alpha-\alpha^{-1}}{2}\in\mathbb Q\left(\alpha\right)$, and similarly $\sqrt3=\frac{\alpha+\alpha^{-1}}{2}\in\mathbb Q\left(\alpha\right)$, so $\mathbb Q\left(\sqrt2,\sqrt3\right)\subseteq\mathbb Q\left(\alpha\right)$. Thus $\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$.

Now show $\sqrt2\notin\mathbb Q\left(\sqrt3\right)$. Suppose $\sqrt2=a+b\sqrt3$ with $a,b\in\mathbb Q$. Squaring gives $2=a^2+3b^2+2ab\sqrt3$. Since $1,\sqrt3$ are linearly independent over $\mathbb Q$, $ab=0$. If $b=0$, then $2=a^2$, with no rational solution; if $a=0$, then $2=3b^2$, i.e. $b^2=2/3$, also with no rational solution. Hence $\sqrt2\notin\mathbb Q\left(\sqrt3\right)$.

Thus $\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]=2$. Also $\left[\mathbb Q\left(\sqrt3\right):\mathbb Q\right]=2$ (since $x^2-3$ is irreducible). By **Theorem 4.1.16 (Tower Law for Extension Degrees)**,

$$
\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\right]=\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]\left[\mathbb Q\left(\sqrt3\right):\mathbb Q\right]=2\times2=4.
$$

(1) Since $\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$, $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\right]=4$.

(2) Similarly, $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]=2$. $\blacksquare$

---

## 4.1-10

Prove that $\mathbb R/\mathbb Q$ is an infinite extension.

### Solution 4.1-10

The number $\pi\in\mathbb R$ is transcendental over $\mathbb Q$ (Lindemann's theorem), i.e. $\pi$ is not a root of any nonzero rational-coefficient polynomial.

If $\mathbb R/\mathbb Q$ were a finite extension, then by **Lemma 4.2.1 (Finite Extensions Are Algebraic)**, every element of $\mathbb R$ would be algebraic over $\mathbb Q$; in particular $\pi$ would be algebraic over $\mathbb Q$, a contradiction.

Hence $\mathbb R/\mathbb Q$ is not a finite extension, i.e. $\mathbb R/\mathbb Q$ is an infinite extension. $\blacksquare$

---

## 4.1-11

Let $E$ be the field of fractions of an integral domain $R$. For any automorphism $\sigma$ of $R$, define $\overline\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\left(\sigma\left(b\right)\right)^{-1}$. Prove that $\overline\sigma$ is an automorphism of $E$.

### Solution 4.1-11

By **Basic Knowledge: Universal Property of the Field of Fractions**, verify in three steps.

**Well-definedness.** Suppose $ab^{-1}=cd^{-1}$ with $a,b,c,d\in R$, $b,d\ne0$. Then $ad=bc$. Since $\sigma$ is a ring homomorphism, $\sigma\left(a\right)\sigma\left(d\right)=\sigma\left(ad\right)=\sigma\left(bc\right)=\sigma\left(b\right)\sigma\left(c\right)$, so $\sigma\left(a\right)\sigma\left(b\right)^{-1}=\sigma\left(c\right)\sigma\left(d\right)^{-1}$, i.e. $\overline\sigma\left(ab^{-1}\right)=\overline\sigma\left(cd^{-1}\right)$. The definition is independent of the choice of representatives.

**Ring homomorphism.** For $x=ab^{-1}$ and $y=cd^{-1}\in E$,

$$
\overline\sigma\left(xy\right)=\overline\sigma\left(ac\left(bd\right)^{-1}\right)=\sigma\left(ac\right)\sigma\left(bd\right)^{-1}=\sigma\left(a\right)\sigma\left(c\right)\sigma\left(b\right)^{-1}\sigma\left(d\right)^{-1}=\overline\sigma\left(x\right)\overline\sigma\left(y\right),
$$

and

$$
\overline\sigma\left(x+y\right)=\overline\sigma\left(\left(ad+bc\right)\left(bd\right)^{-1}\right)=\sigma\left(ad+bc\right)\sigma\left(bd\right)^{-1}=\frac{\sigma\left(a\right)}{\sigma\left(b\right)}+\frac{\sigma\left(c\right)}{\sigma\left(d\right)}=\overline\sigma\left(x\right)+\overline\sigma\left(y\right).
$$

Also $\overline\sigma\left(1\right)=\sigma\left(1\right)\sigma\left(1\right)^{-1}=1$, so $\overline\sigma$ is a ring homomorphism.

**Bijectivity.** Since $\sigma$ is an automorphism of $R$, its inverse $\tau=\sigma^{-1}$ is also an automorphism of $R$. A direct check shows that $\overline\tau$ is the inverse of $\overline\sigma$: for $x=ab^{-1}\in E$,

$$
\overline\tau\circ\overline\sigma\left(x\right)=\overline\tau\left(\sigma\left(a\right)\sigma\left(b\right)^{-1}\right)=\tau\left(\sigma\left(a\right)\right)\tau\left(\sigma\left(b\right)\right)^{-1}=ab^{-1}=x.
$$

Similarly $\overline\sigma\circ\overline\tau=\mathrm{id}$. Hence $\overline\sigma$ is invertible and is an automorphism of $E$. $\blacksquare$

---

## 4.1-13

Prove that $\mathrm{Aut}\left(\mathbb R\right)$ is the trivial group.

### Solution 4.1-13

Let $\sigma\in\mathrm{Aut}\left(\mathbb R\right)$. By **Lemma 4.1.9 (Field Homomorphisms Are Injective)**, $\sigma$ is a field automorphism preserving the multiplicative identity, so $\sigma\left(1\right)=1$. Hence for every $n\in\mathbb Z$, $\sigma\left(n\right)=n$; for every $m/n\in\mathbb Q$, $\sigma\left(m/n\right)=m/n$, i.e. $\sigma$ fixes every element of $\mathbb Q$.

Now show that $\sigma$ preserves order. If $x> 0$, then there exists $y\in\mathbb R$, $y\ne0$, with $x=y^2$. Hence $\sigma\left(x\right)=\sigma\left(y^2\right)=\sigma\left(y\right)^2> 0$, where $\sigma\left(y\right)\ne0$ (since $\sigma$ is injective and $y\ne0$). Thus $\sigma$ sends positive numbers to positive numbers, so when $a< b$, i.e. $b-a> 0$, $\sigma\left(b\right)-\sigma\left(a\right)=\sigma\left(b-a\right)> 0$, i.e. $\sigma\left(a\right)< \sigma\left(b\right)$. Hence $\sigma$ is order-preserving.

Suppose, for contradiction, that $\sigma\ne\mathrm{id}$; then there exists $x\in\mathbb R$ with $\sigma\left(x\right)\ne x$.

If $\sigma\left(x\right)> x$, by the density of $\mathbb Q$ in $\mathbb R$, choose $q\in\mathbb Q$ with $x< q< \sigma\left(x\right)$. Since $\sigma$ is order-preserving, $x< q$ gives $\sigma\left(x\right)< \sigma\left(q\right)=q$, contradicting $q< \sigma\left(x\right)$.

If $\sigma\left(x\right)< x$, similarly choose $q\in\mathbb Q$ with $\sigma\left(x\right)< q< x$. From $q< x$ we get $q=\sigma\left(q\right)< \sigma\left(x\right)$, contradicting $\sigma\left(x\right)< q$.

Hence $\sigma\left(x\right)=x$ for all $x\in\mathbb R$, i.e. $\sigma=\mathrm{id}$. Therefore $\mathrm{Aut}\left(\mathbb R\right)$ contains only the identity and is the trivial group. $\blacksquare$
