# Assignment 24

> **Definition 4.1.15** (Degree of an Extension) Let $E$ be an extension of $F$. The dimension of $E$ as an $F$-vector space is called the degree of $E$ over $F$, denoted $\left[E:F\right]$. If $\left[E:F\right]<\infty$, $E$ is called a finite extension of $F$; otherwise it is called an infinite extension.$E$ and $F$ are finite extensions, then 

 $K/F$ is also a finite extension, and $E/K$.$E/F$ be a finite extension. Then every element of $\left[E:F\right]=\left[E:K\right]\left[K:F\right]$ is algebraic over 

 $E/F$. Equivalently, if $E$ contains an element transcendental over $F$, then $E$ must be an infinite extension.$F$ is always injective. In particular, a field automorphism preserves the field operations and $E/F$, and hence fixes every element of the prime field (

 $\varphi:F\to E$ or $1$).$\mathbb Q$ be an integral domain and $\mathbb F_p$ its field of fractions. Given any automorphism 

 $R$ of $E$, define the map $R$; then $\sigma$ is well defined and is an automorphism of $\bar\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\sigma\left(b\right)^{-1}$.$\bar\sigma$;$E$### Solution to Problem 1

Write 

 
 $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\right]$. First prove that 
 

$$
\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right].
$$

.

On the one hand, $\alpha=\sqrt2+\sqrt3$, so $\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$.

On the other hand, since$\alpha\in\mathbb Q\left(\sqrt2,\sqrt3\right)$we have $\mathbb Q\left(\alpha\right)\subseteq\mathbb Q\left(\sqrt2,\sqrt3\right)$. Hence

 

$$
\left(\sqrt2+\sqrt3\right)\left(\sqrt3-\sqrt2\right)=3-2=1,
$$

and similarly $\alpha^{-1}=\sqrt3-\sqrt2$, so 

$$
\sqrt2=\frac{\alpha-\alpha^{-1}}{2}\in\mathbb Q\left(\alpha\right),
$$

. Therefore $\sqrt3=\frac{\alpha+\alpha^{-1}}{2}\in\mathbb Q\left(\alpha\right)$.$\mathbb Q\left(\sqrt2,\sqrt3\right)\subseteq\mathbb Q\left(\alpha\right)$. Suppose, for contradiction, that $\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$ with 

 $\sqrt2\notin\mathbb Q\left(\sqrt3\right)$. Squaring gives $\sqrt2=a+b\sqrt3$. Since $a,b\in\mathbb Q$ are linearly independent over $2=a^2+3b^2+2ab\sqrt3$, we must have $1,\sqrt3$. If $\mathbb Q$, then $ab=0$, which has no rational solution; if $b=0$, then $2=a^2$, i.e. $a=0$, which also has no rational solution. Hence $2=3b^2$.$b^2=2/3$Also $\sqrt2\notin\mathbb Q\left(\sqrt3\right)$ (since 

 

$$
\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]=2.
$$

 is irreducible). By **Theorem 4.1.16** (Telescope Rule for Degrees),$\left[\mathbb Q\left(\sqrt3\right):\mathbb Q\right]=2$(1) Since $x^2-3$, we have 

$$
\begin{aligned}\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\right]&=\left[\mathbb Q\left(\sqrt2,\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]\left[\mathbb Q\left(\sqrt3\right):\mathbb Q\right]\\&=2\times2\\&=4.\end{aligned}
$$

.$\mathbb Q\left(\alpha\right)=\mathbb Q\left(\sqrt2,\sqrt3\right)$ $\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\right]=4$### Problem 2

(Problem 4.1-10) Prove that 

$$
\left[\mathbb Q\left(\sqrt2+\sqrt3\right):\mathbb Q\left(\sqrt3\right)\right]=2.
$$

$\blacksquare$

 is transcendental over 

 $\mathbb R/\mathbb Q$ (Lindemann's theorem), i.e. 

 

 $\pi\in\mathbb R$ is not a root of any nonzero polynomial with rational coefficients.$\mathbb Q$ were a finite extension, then by **Lemma 4.2.1** (Finite Extensions Are Algebraic), every element of $\pi$ would be algebraic over 

 $\mathbb R/\mathbb Q$; in particular, $\mathbb R$ would be algebraic over $\mathbb Q$, a contradiction.$\pi$ is not a finite extension, i.e. $\mathbb Q$ is an infinite extension. 

 $\mathbb R/\mathbb Q$### Problem 3$\mathbb R/\mathbb Q$ be the field of fractions of an integral domain $\blacksquare$

. For any automorphism 

 $E$ of $R$, define $R$. Prove that $\sigma$ is an automorphism of $\bar\sigma\left(ab^{-1}\right)=\sigma\left(a\right)\left(\sigma\left(b\right)\right)^{-1}$.$\bar\sigma$, with $E$ and 

 

 

 $ab^{-1}=cd^{-1}$. Then $a,b,c,d\in R$. Since $b,d\ne0$ is a ring homomorphism,$ad=bc$so $\sigma$, i.e. 

$$
\begin{aligned}\sigma\left(a\right)\sigma\left(d\right)&=\sigma\left(ad\right)\\&=\sigma\left(bc\right)\\&=\sigma\left(b\right)\sigma\left(c\right),\end{aligned}
$$

. The definition is independent of the choice of representative.$\sigma\left(a\right)\sigma\left(b\right)^{-1}=\sigma\left(c\right)\sigma\left(d\right)^{-1}$ and $\bar\sigma\left(ab^{-1}\right)=\bar\sigma\left(cd^{-1}\right)$,

 $x=ab^{-1}$and$y=cd^{-1}\in E$Also 

$$
\begin{aligned}\bar\sigma\left(xy\right)&=\bar\sigma\left(ac\left(bd\right)^{-1}\right)\\&=\sigma\left(ac\right)\sigma\left(bd\right)^{-1}\\&=\sigma\left(a\right)\sigma\left(c\right)\sigma\left(b\right)^{-1}\sigma\left(d\right)^{-1}\\&=\bar\sigma\left(x\right)\bar\sigma\left(y\right),\end{aligned}
$$

, so 

$$
\begin{aligned}\bar\sigma\left(x+y\right)&=\bar\sigma\left(\left(ad+bc\right)\left(bd\right)^{-1}\right)\\&=\sigma\left(ad+bc\right)\sigma\left(bd\right)^{-1}\\&=\frac{\sigma\left(a\right)}{\sigma\left(b\right)}+\frac{\sigma\left(c\right)}{\sigma\left(d\right)}\\&=\bar\sigma\left(x\right)+\bar\sigma\left(y\right).\end{aligned}
$$

 is a ring homomorphism.$\bar\sigma\left(1\right)=\sigma\left(1\right)\sigma\left(1\right)^{-1}=1$ is an automorphism of $\bar\sigma$, its inverse 

 $\sigma$ is also an automorphism of $R$. A direct check shows that $\tau=\sigma^{-1}$ is the inverse of $R$: for $\bar\tau$,$\bar\sigma$Symmetrically, $x=ab^{-1}\in E$. Hence 

$$
\begin{aligned}\bar\tau\circ\bar\sigma\left(x\right)&=\bar\tau\left(\sigma\left(a\right)\sigma\left(b\right)^{-1}\right)\\&=\tau\left(\sigma\left(a\right)\right)\tau\left(\sigma\left(b\right)\right)^{-1}\\&=ab^{-1}\\&=x.\end{aligned}
$$

 is invertible and is an automorphism of $\bar\sigma\circ\bar\tau=\mathrm{id}$. $\bar\sigma$### Problem 4$E$ is the trivial group.$\blacksquare$

. By **Lemma 4.1.9** (Field Homomorphisms Are Injective), 

 $\mathrm{Aut}\left(\mathbb R\right)$ is a field automorphism and preserves the multiplicative identity, so 

 

 $\sigma\in\mathrm{Aut}\left(\mathbb R\right)$. Hence for any $\sigma$, $\sigma\left(1\right)=1$; and for any $n\in\mathbb Z$, $\sigma\left(n\right)=n$, i.e. $m/n\in\mathbb Q$ fixes every element of $\sigma\left(m/n\right)=m/n$.$\sigma$ preserves order. If $\mathbb Q$, then there exists 

 $\sigma$, $x>0$, with $y\in\mathbb R$. Hence$y\ne0$where $x=y^2$ (since 
$$
\begin{aligned}\sigma\left(x\right)&=\sigma\left(y^2\right)\\&=\sigma\left(y\right)^2>0,\end{aligned}
$$
 is injective and $\sigma\left(y\right)\ne0$). Hence $\sigma$ sends positive numbers to positive numbers; therefore, when $y\ne0$, i.e. $\sigma$,$a<b$i.e. $b-a>0$. Thus 
$$
\sigma\left(b\right)-\sigma\left(a\right)=\sigma\left(b-a\right)>0,
$$
 is order-preserving.$\sigma\left(a\right)<\sigma\left(b\right)$; then there exists $\sigma$ with 
 $\sigma\ne\mathrm{id}$.$x\in\mathbb R$, by the density of $\sigma\left(x\right)\ne x$ in 
 $\sigma\left(x\right)>x$, choose $\mathbb Q$ with $\mathbb R$. Since $q\in\mathbb Q$ is order-preserving, $x<q<\sigma\left(x\right)$ gives $\sigma$, contradicting $x<q$.$\sigma\left(x\right)<\sigma\left(q\right)=q$, symmetrically choose $q<\sigma\left(x\right)$ with 
 $\sigma\left(x\right)<x$. From $q\in\mathbb Q$ we get $\sigma\left(x\right)<q<x$, contradicting $q<x$.$q=\sigma\left(q\right)<\sigma\left(x\right)$ for all $\sigma\left(x\right)<q$, i.e. 
 $\sigma\left(x\right)=x$. Therefore $x\in\mathbb R$ contains only the identity element and is the trivial group. $\sigma=\mathrm{id}$ $\mathrm{Aut}\left(\mathbb R\right)$ contains only the identity element and is the trivial group. $\blacksquare$
