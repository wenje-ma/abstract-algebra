# week12

> **Lemma 4.1.9 (Field Homomorphisms Are Injective)**
> 
> A field homomorphism $\varphi:F\to E$ is always injective. In particular, a field automorphism preserves the operations and $1$, and hence fixes every element of the prime field ($\mathbb Q$ or $\mathbb F_p$).

> **Definition 4.1.15 (Degree of an Extension)**
> 
> Let $E$ be an extension of $F$. The dimension of $E$ as an $F$-vector space is called the degree of $E$ over $F$, written $\left[E:F\right]$. If $\left[E:F\right]< \infty$, $E$ is a finite extension of $F$; otherwise it is an infinite extension.

> **Theorem 4.1.16 (Tower Law for Extension Degrees)**
> 
> If both $K/F$ and $E/K$ are finite extensions, then $E/F$ is also finite, and $\left[E:F\right]=\left[E:K\right]\left[K:F\right]$.

> **Lemma 4.2.1 (Finite Extensions Are Algebraic)**
> 
> If $E/F$ is a finite extension, then every element of $E$ is algebraic over $F$. Equivalently, if $E$ contains a transcendental element over $F$, then $E/F$ must be an infinite extension.

> **Theorem 4.2.13 (Structure of a Simple Algebraic Extension)**
> 
> A simple algebraic extension $F\left(\alpha\right)$ of a field $F$ is isomorphic to $F\left[x\right]/\left(\mathrm{Irr}\left(\alpha,F\right)\right)$. If $\deg\left(\alpha,F\right)=n$, then $F\left(\alpha\right)$ has dimension $n$ as an $F$-vector space, and $1,\alpha,\alpha^2,\cdots,\alpha^{n-1}$ form an $F$-basis.

## 4.1-4

Find the degrees of the following field extensions:

(1) $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\right]$;

(2) $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]$.

### Solution to 4.1-4

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

## 4.1-10

Prove that $\mathbb R/\mathbb Q$ is an infinite extension.

### Solution to 4.1-10

The number $\pi\in\mathbb R$ is transcendental over $\mathbb Q$ (Lindemann's theorem), i.e. $\pi$ is not a root of any nonzero rational-coefficient polynomial.

If $\mathbb R/\mathbb Q$ were a finite extension, then by **Lemma 4.2.1 (Finite Extensions Are Algebraic)**, every element of $\mathbb R$ would be algebraic over $\mathbb Q$; in particular $\pi$ would be algebraic over $\mathbb Q$, a contradiction.

Hence $\mathbb R/\mathbb Q$ is not a finite extension, i.e. $\mathbb R/\mathbb Q$ is an infinite extension. $\blacksquare$

## 4.1-11

Let $E$ be the field of fractions of an integral domain $R$. For any automorphism $\sigma$ of $R$, define $\overline\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\left(\sigma\left(b\right)\right)^{-1}$. Prove that $\overline\sigma$ is an automorphism of $E$.

### Solution to 4.1-11

By Universal Property of the Field of Fractions, verify in three steps.

Well-definedness. Suppose $ab^{-1}=cd^{-1}$ with $a,b,c,d\in R$, $b,d\ne0$. Then $ad=bc$. Since $\sigma$ is a ring homomorphism, $\sigma\left(a\right)\sigma\left(d\right)=\sigma\left(ad\right)=\sigma\left(bc\right)=\sigma\left(b\right)\sigma\left(c\right)$, so $\sigma\left(a\right)\sigma\left(b\right)^{-1}=\sigma\left(c\right)\sigma\left(d\right)^{-1}$, i.e. $\overline\sigma\left(ab^{-1}\right)=\overline\sigma\left(cd^{-1}\right)$. The definition is independent of the choice of representatives.

Ring homomorphism. For $x=ab^{-1}$ and $y=cd^{-1}\in E$,

$$
\overline\sigma\left(xy\right)=\overline\sigma\left(ac\left(bd\right)^{-1}\right)=\sigma\left(ac\right)\sigma\left(bd\right)^{-1}=\sigma\left(a\right)\sigma\left(c\right)\sigma\left(b\right)^{-1}\sigma\left(d\right)^{-1}=\overline\sigma\left(x\right)\overline\sigma\left(y\right),
$$

and

$$
\overline\sigma\left(x+y\right)=\overline\sigma\left(\left(ad+bc\right)\left(bd\right)^{-1}\right)=\sigma\left(ad+bc\right)\sigma\left(bd\right)^{-1}=\frac{\sigma\left(a\right)}{\sigma\left(b\right)}+\frac{\sigma\left(c\right)}{\sigma\left(d\right)}=\overline\sigma\left(x\right)+\overline\sigma\left(y\right).
$$

Also $\overline\sigma\left(1\right)=\sigma\left(1\right)\sigma\left(1\right)^{-1}=1$, so $\overline\sigma$ is a ring homomorphism.

Bijectivity. Since $\sigma$ is an automorphism of $R$, its inverse $\tau=\sigma^{-1}$ is also an automorphism of $R$. A direct check shows that $\overline\tau$ is the inverse of $\overline\sigma$: for $x=ab^{-1}\in E$,

$$
\overline\tau\circ\overline\sigma\left(x\right)=\overline\tau\left(\sigma\left(a\right)\sigma\left(b\right)^{-1}\right)=\tau\left(\sigma\left(a\right)\right)\tau\left(\sigma\left(b\right)\right)^{-1}=ab^{-1}=x.
$$

Similarly $\overline\sigma\circ\overline\tau=\mathrm{id}$. Hence $\overline\sigma$ is invertible and is an automorphism of $E$. $\blacksquare$

## 4.1-13

Prove that $\mathrm{Aut}\left(\mathbb R\right)$ is the trivial group.

### Solution to 4.1-13

Let $\sigma\in\mathrm{Aut}\left(\mathbb R\right)$. By **Lemma 4.1.9 (Field Homomorphisms Are Injective)**, $\sigma$ is a field automorphism preserving the multiplicative identity, so $\sigma\left(1\right)=1$. Hence for every $n\in\mathbb Z$, $\sigma\left(n\right)=n$; for every $m/n\in\mathbb Q$, $\sigma\left(m/n\right)=m/n$, i.e. $\sigma$ fixes every element of $\mathbb Q$.

Now show that $\sigma$ preserves order. If $x> 0$, then there exists $y\in\mathbb R$, $y\ne0$, with $x=y^2$. Hence $\sigma\left(x\right)=\sigma\left(y^2\right)=\sigma\left(y\right)^2> 0$, where $\sigma\left(y\right)\ne0$ (since $\sigma$ is injective and $y\ne0$). Thus $\sigma$ sends positive numbers to positive numbers, so when $a< b$, i.e. $b-a> 0$, $\sigma\left(b\right)-\sigma\left(a\right)=\sigma\left(b-a\right)> 0$, i.e. $\sigma\left(a\right)< \sigma\left(b\right)$. Hence $\sigma$ is order-preserving.

Suppose, for contradiction, that $\sigma\ne\mathrm{id}$; then there exists $x\in\mathbb R$ with $\sigma\left(x\right)\ne x$.

If $\sigma\left(x\right)> x$, by the density of $\mathbb Q$ in $\mathbb R$, choose $q\in\mathbb Q$ with $x< q< \sigma\left(x\right)$. Since $\sigma$ is order-preserving, $x< q$ gives $\sigma\left(x\right)< \sigma\left(q\right)=q$, contradicting $q< \sigma\left(x\right)$.

If $\sigma\left(x\right)< x$, similarly choose $q\in\mathbb Q$ with $\sigma\left(x\right)< q< x$. From $q< x$ we get $q=\sigma\left(q\right)< \sigma\left(x\right)$, contradicting $\sigma\left(x\right)< q$.

Hence $\sigma\left(x\right)=x$ for all $x\in\mathbb R$, i.e. $\sigma=\mathrm{id}$. Therefore $\mathrm{Aut}\left(\mathbb R\right)$ contains only the identity and is the trivial group. $\blacksquare$

## 4.2-5

Let $F\left(\alpha\right)$ be a simple algebraic extension of $F$ with $\deg\left(\alpha,F\right)=n$. Prove that $F\left(\alpha\right)$ is an $n$-dimensional $F$-vector space and that $1,\alpha,\cdots,\alpha^{n-1}$ form a basis of $F\left(\alpha\right)$.

### Solution to 4.2-5

By **Theorem 4.2.13 (Structure of a Simple Algebraic Extension)**, $F\left(\alpha\right)\cong F\left[x\right]/\left(\mathrm{Irr}\left(\alpha,F\right)\right)$. Let $f\left(x\right)=\mathrm{Irr}\left(\alpha,F\right)$ be the monic irreducible polynomial of degree $n$.

Every element of the quotient ring $F\left[x\right]/\left(f\left(x\right)\right)$ can be uniquely written as $a_0+a_1x+\cdots+a_{n-1}x^{n-1}$ (by division with remainder, the remainder has degree less than $n$). Under the isomorphism, $x$ corresponds to $\alpha$, so every element of $F\left(\alpha\right)$ is uniquely written as $a_0+a_1\alpha+\cdots+a_{n-1}\alpha^{n-1}$ with $a_i\in F$.

Hence $1,\alpha,\cdots,\alpha^{n-1}$ generate $F\left(\alpha\right)$ and are linearly independent over $F$ (if $\sum_{i=0}^{n-1}a_i\alpha^i=0$, then $\sum a_ix^i$ is a polynomial of degree less than $n$ having $\alpha$ as a root, contradicting that $f$ is the minimal polynomial). Thus they form an $F$-basis of $F\left(\alpha\right)$, and $\dim_F F\left(\alpha\right)=n$. $\blacksquare$

## 4.2-6

Prove that for every positive integer $n$, there is an algebraic extension $K$ of $\mathbb Q$ with $\left[K:\mathbb Q\right]=n$.

### Solution to 4.2-6

Take $K=\mathbb Q\left(2^{1/n}\right)$, the extension generated by a root $\theta=2^{1/n}$ of the polynomial $x^n-2$.

For $f\left(x\right)=x^n-2\in\mathbb Z\left[x\right]$, take the prime $p=2$. By Eisenstein's Criterion, $2\nmid1$ (leading coefficient), $2\mid0$ (all intermediate coefficients are $0$), and $2^2=4\nmid-2$ (constant term), so $f\left(x\right)$ is irreducible over $\mathbb Q\left[x\right]$.

Hence $\deg\left(\theta,\mathbb Q\right)=n$. By **Theorem 4.2.13 (Structure of a Simple Algebraic Extension)**, $\left[K:\mathbb Q\right]=\left[\mathbb Q\left(\theta\right):\mathbb Q\right]=n$. Since $K/\mathbb Q$ is a simple algebraic extension, it is an algebraic extension. $\blacksquare$

## 4.2-9

If $a,b\in\mathbb Q$ satisfy $\sqrt a+\sqrt b\ne0$, prove that $\mathbb Q\left(\sqrt a,\sqrt b\right)=\mathbb Q\left(\sqrt a+\sqrt b\right)$.

### Solution to 4.2-9

Set $\alpha=\sqrt a+\sqrt b$. Since $\alpha\in\mathbb Q\left(\sqrt a,\sqrt b\right)$, we have $\mathbb Q\left(\alpha\right)\subseteq\mathbb Q\left(\sqrt a,\sqrt b\right)$; it remains to prove the reverse inclusion.

By assumption $\alpha\ne0$. Computing, $\alpha^2=a+b+2\sqrt{ab}$, so $\sqrt{ab}=\frac{\alpha^2-a-b}{2}\in\mathbb Q\left(\alpha\right)$. Also $\sqrt a-\sqrt b=\frac{\left(\sqrt a-\sqrt b\right)\left(\sqrt a+\sqrt b\right)}{\sqrt a+\sqrt b}=\frac{a-b}{\alpha}\in\mathbb Q\left(\alpha\right)$.

Hence $\sqrt a=\frac{1}{2}\left(\alpha+\frac{a-b}{\alpha}\right)\in\mathbb Q\left(\alpha\right)$ and $\sqrt b=\frac{1}{2}\left(\alpha-\frac{a-b}{\alpha}\right)\in\mathbb Q\left(\alpha\right)$.

Thus $\mathbb Q\left(\sqrt a,\sqrt b\right)\subseteq\mathbb Q\left(\alpha\right)$. Together with the reverse inclusion, $\mathbb Q\left(\sqrt a,\sqrt b\right)=\mathbb Q\left(\sqrt a+\sqrt b\right)$. $\blacksquare$

## 4.2-10

Let $E=\mathbb F_p\left(t\right)$ be a simple transcendental extension of $\mathbb F_p$.

(1) Prove that $x^p-t\in E\left[x\right]$ is irreducible;

(2) Let $\theta$ be a root of $x^p-t$. Factor $x^p-t$ over $E\left(\theta\right)$ into irreducible factors.

### Solution to 4.2-10

(1) Suppose, for contradiction, that $x^p-t$ has a nontrivial factorization in $E\left[x\right]$, $x^p-t=f\left(x\right)g\left(x\right)$, with $f,g$ monic and $1\le\deg f=k< p$.

Let $\theta$ be a root of $x^p-t$ in some splitting field; then $\theta^p=t$. By Frobenius Map in Characteristic $p$, $\left(x-\theta\right)^p=x^p-\theta^p=x^p-t$. Hence in the splitting field $x^p-t=\left(x-\theta\right)^p$, so $f\left(x\right)=\left(x-\theta\right)^k$.

The coefficient of $x^{k-1}$ in $f\left(x\right)$ is $-k\theta$. Since $f\in E\left[x\right]$, this coefficient lies in $E$, so $k\theta\in E$. Also $1\le k< p$, and in characteristic $p$, $k\ne0$, so $k$ is invertible; hence $\theta\in E$.

But $\theta\in E=\mathbb F_p\left(t\right)$ means there are coprime polynomials $f_0\left(t\right),g_0\left(t\right)\in\mathbb F_p\left[t\right]$ with $\theta=f_0\left(t\right)/g_0\left(t\right)$. From $\theta^p=t$ we get $f_0\left(t\right)^p=t\,g_0\left(t\right)^p$. Comparing degrees: the left side has degree $p\deg f_0$, the right side $1+p\deg g_0$. The left side is divisible by $p$, while the right side is congruent to $1$ modulo $p$, a contradiction. Hence $\theta\notin E$, and $x^p-t$ is irreducible in $E\left[x\right]$.

(2) In $E\left(\theta\right)$, by Frobenius Map in Characteristic $p$, $x^p-t=x^p-\theta^p=\left(x-\theta\right)^p$. Here $x-\theta$ is already linear and hence irreducible. Thus the irreducible factorization of $x^p-t$ over $E\left(\theta\right)$ is $\left(x-\theta\right)^p$. $\blacksquare$

## 4.2-13

Let $F\left(\alpha\right)$ be a simple transcendental extension of $F$, and let $u\in F\left(\alpha\right)$ with $u\notin F$. Prove that $\alpha$ is algebraic over the field $F\left(u\right)$.

### Solution to 4.2-13

Since $u\in F\left(\alpha\right)$ and $F\left(\alpha\right)$ is the field of fractions of $F\left[\alpha\right]$, there exist coprime polynomials $f\left(x\right),g\left(x\right)\in F\left[x\right]$ with $g\left(x\right)\ne0$ such that $u=\frac{f\left(\alpha\right)}{g\left(\alpha\right)}$.

Consider the polynomial $h\left(x\right)=u\,g\left(x\right)-f\left(x\right)\in F\left(u\right)\left[x\right]$. Substituting $x=\alpha$, $h\left(\alpha\right)=u\,g\left(\alpha\right)-f\left(\alpha\right)=0$.

Now show $h\left(x\right)\ne0$. Suppose $h\left(x\right)=0$; then in $F\left(u\right)\left[x\right]$, $u\,g\left(x\right)=f\left(x\right)$.

If $g\left(x\right)$ is a constant polynomial, then $f\left(x\right)$ must be nonconstant (otherwise $u=f/g\in F$, a contradiction); then $\deg\left(u\,g\right)=0$ while $\deg f> 0$, contradicting $ug=f$.

If $g\left(x\right)$ is nonconstant, then $\deg\left(ug\right)=\deg g$ ($u$ is a nonzero element of $F\left(u\right)$ and does not change the polynomial degree). From $ug=f$, $\deg f=\deg g$; comparing leading coefficients, $u\cdot\mathrm{lc}\left(g\right)=\mathrm{lc}\left(f\right)$, i.e. $u=\mathrm{lc}\left(f\right)/\mathrm{lc}\left(g\right)\in F$, contradicting $u\notin F$.

Thus $h\left(x\right)\ne0$, while $h\left(\alpha\right)=0$; i.e. $\alpha$ is a root of the nonzero polynomial $h$ over $F\left(u\right)$, and hence $\alpha$ is algebraic over $F\left(u\right)$. $\blacksquare$

## 4.4-5

Let $F$ be a field, $c\in F$, and $\mathrm{char}\,F=p\ne0$. Prove that $x^p-c$ is irreducible in $F\left[x\right]$ if and only if $x^p-c$ has no root in $F$.

### Solution to 4.4-5

Necessity. Suppose $x^p-c$ has a root $\alpha$ in $F$, i.e. $\alpha^p=c$ with $\alpha\in F$. By Frobenius Map in Characteristic $p$, $x^p-c=x^p-\alpha^p=\left(x-\alpha\right)^p$. Since $p\ge2$, this gives a nontrivial factorization of $x^p-c$ in $F\left[x\right]$, so $x^p-c$ is reducible. Hence the contrapositive holds: irreducible implies $x^p-c$ has no root in $F$.

Sufficiency. Suppose, for contradiction, that $x^p-c$ has no root in $F$ but is reducible in $F\left[x\right]$, i.e. there exist nonconstant monic polynomials $f\left(x\right),g\left(x\right)\in F\left[x\right]$ with $x^p-c=f\left(x\right)g\left(x\right)$, where $1\le\deg f=k< p$.

Let $E$ be a splitting field of $x^p-c$, and let $\alpha\in E$ be a root. By Frobenius Map in Characteristic $p$, in $E\left[x\right]$ we have $x^p-c=\left(x-\alpha\right)^p$. Since $f$ is monic, comparing factorizations gives $f\left(x\right)=\left(x-\alpha\right)^k$.

The coefficient of $x^{k-1}$ in $f\left(x\right)=\left(x-\alpha\right)^k$ is $-k\alpha$. Since $f\in F\left[x\right]$, this coefficient lies in $F$, so $k\alpha\in F$. Also $1\le k< p$, and in characteristic $p$, $k\ne0$, so $k$ is invertible in $F$; hence $\alpha=\left(k\alpha\right)\cdot k^{-1}\in F$.

Thus $\alpha^p=c$, i.e. $\alpha$ is a root of $x^p-c$ in $F$, contradicting the assumption. Hence when $x^p-c$ has no root in $F$, it must be irreducible.

In summary, $x^p-c$ is irreducible in $F\left[x\right]$ if and only if it has no root in $F$. $\blacksquare$
