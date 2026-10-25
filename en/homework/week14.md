# Assignment 14

> **Definition 2.4.1** (Ring Homomorphism and Isomorphism) Let $R_1,R_2$ be two rings and $f$ a map from $R_1$ to $R_2$. If for any $a,b\in R_1$ we have $f\left(a+b\right)=f\left(a\right)+f\left(b\right)$ and $f\left(ab\right)=f\left(a\right)f\left(b\right)$, then $f$ is called a homomorphism; an injective homomorphism is called a monomorphism, a surjective homomorphism an epimorphism, and a bijective homomorphism an isomorphism.

> **Definition 2.2.20** (Integral Domain, Division Ring, and Field) A commutative ring with identity and without zero divisors is called an integral domain; if a ring with identity $R$ satisfies that $R^*$ forms a group under multiplication ($R^*=R\setminus\left\{0\right\}$), then $R$ is called a division ring; a commutative division ring is called a field.

### Problem 1

(Problem 2.4-6) Find all automorphisms of the number field

$$
\mathbb Q\left[\sqrt{-1}\right]=\left\{a+b\sqrt{-1}\mid a,b\in\mathbb Q\right\}
$$

### Solution to Problem 1

Write

 $i=\sqrt{-1}$. Let $\varphi:\mathbb Q\left[i\right]\to\mathbb Q\left[i\right]$ be an automorphism. By **Definition 2.4.1** (Ring Homomorphism and Isomorphism), $\varphi\left(1\right)=1$, so $\varphi$ is the identity on $\mathbb Q$. Write $\varphi\left(i\right)=u=a+bi$ with $a,b\in\mathbb Q$.

Since $i^2=-1$,

$$
\begin{aligned}u^2&=\varphi\left(i\right)^2\\&=\varphi\left(i^2\right)\\&=\varphi\left(-1\right)\\&=-1.\end{aligned}
$$

That is,

$$
\left(a+bi\right)^2=a^2-b^2+2abi=-1.
$$

Comparing real and imaginary parts gives $2ab=0$ and $a^2-b^2=-1$. If $b=0$, then $a^2=-1$, which has no solution in $\mathbb Q$; hence $a=0$, $b^2=1$, and $b=\pm1$. Thus $u=i$ or $u=-i$.

(1) $\varphi\left(i\right)=i$: then $\varphi\left(a+bi\right)=a+bi$, i.e. the identity automorphism.

(2) $\varphi\left(i\right)=-i$: then $\varphi\left(a+bi\right)=a-bi$, i.e. the complex conjugation map.

Both preserve addition and multiplication and are bijective. Hence $\mathbb Q\left[i\right]$ has exactly two automorphisms: the identity and the conjugation map. $\blacksquare$

### Problem 2

(Problem 2.4-7) Prove that the only automorphism of the real field is the identity.

### Solution to Problem 2

Let $\varphi:\mathbb R\to\mathbb R$ be a field automorphism. First, $\varphi$ fixes rationals: $\varphi\left(1\right)=1$, so $\varphi\left(n\right)=n$ and $\varphi\left(m/n\right)=m/n$.

**Order preservation** If $x> 0$, then there exists $y\ne0$ with $x=y^2$, so $\varphi\left(x\right)=\varphi\left(y\right)^2> 0$. Hence when $x> y$, $x-y> 0$ gives $\varphi\left(x\right)-\varphi\left(y\right)> 0$, i.e. $\varphi$ is strictly increasing.

**Identity** Suppose, for contradiction, that there exists $x$ with $\varphi\left(x\right)\ne x$. If $\varphi\left(x\right)> x$, by the density of rationals in $\mathbb R$, take $q\in\mathbb Q$ with $x< q< \varphi\left(x\right)$. From $x< q$ and the monotonicity of $\varphi$, we get $\varphi\left(x\right)< \varphi\left(q\right)=q$, contradicting $q< \varphi\left(x\right)$. If $\varphi\left(x\right)< x$, similarly take $q$ with $\varphi\left(x\right)< q< x$; from the monotonicity of $\varphi$, $q=\varphi\left(q\right)< \varphi\left(x\right)$, a contradiction.

Hence $\varphi\left(x\right)=x$ for all $x\in\mathbb R$, i.e. $\varphi$ is the identity automorphism. $\blacksquare$

### Problem 3

(Problem 2.4-8) Prove that the map $a+b\sqrt{-1}\mapsto a-b\sqrt{-1}$ is an automorphism of the ring $\mathbb C$.

### Solution to Problem 3

Write $\varphi\left(a+bi\right)=a-bi$.

**Preservation of addition**

$$
\begin{aligned}\varphi\left(\left(a+bi\right)+\left(c+di\right)\right)&=\varphi\left(\left(a+c\right)+\left(b+d\right)i\right)\\&=\left(a+c\right)-\left(b+d\right)i\\&=\left(a-bi\right)+\left(c-di\right)\\&=\varphi\left(a+bi\right)+\varphi\left(c+di\right).\end{aligned}
$$

**Preservation of multiplication**

$$
\begin{aligned}\varphi\left(\left(a+bi\right)\left(c+di\right)\right)&=\varphi\left(\left(ac-bd\right)+\left(ad+bc\right)i\right)\\&=\left(ac-bd\right)-\left(ad+bc\right)i,\end{aligned}
$$

while

$$
\begin{aligned}\varphi\left(a+bi\right)\varphi\left(c+di\right)&=\left(a-bi\right)\left(c-di\right)\\&=ac-bd-\left(ad+bc\right)i.\end{aligned}
$$

The two are equal. Also, applying the map twice returns to the original element, so $\varphi$ is bijective. By **Definition 2.4.1** (Ring Homomorphism and Isomorphism), $\varphi$ is an automorphism of $\mathbb C$. $\blacksquare$

### Problem 4

(Problem 2.4-19) This problem proves the existence and uniqueness of the field of fractions of an integral domain. Let an integral domain $R$ be a subring of a field $F$; if for any $a\in F$ there exist $b,c\in R$ with $a=bc^{-1}$, then $F$ is called the field of fractions of $R$. On the set $R\times R^*$, define addition and multiplication by

$$
\left(a,b\right)+\left(c,d\right)=\left(ad+bc,bd\right).
$$

$$
\left(a,b\right)\left(c,d\right)=\left(ac,bd\right),
$$

where $\left(a,b\right),\left(c,d\right)\in R\times R^*$.
(1) Prove that $R\times R^*$ with the above addition and multiplication are both commutative monoids, with identity elements $\left(0,1\right)$ and $\left(1,1\right)$ respectively;
(2) Define a relation on $R\times R^*$ by $\left(a,b\right)\sim\left(c,d\right)$ if and only if $ad=bc$. Prove that $\sim$ is an equivalence relation and is a congruence relation for both the above multiplication and addition;
(3) Let $F=\left(R\times R^*\right)/\sim$ be the set of equivalence classes, and write the class of $\left(a,b\right)$ as $a/b$. On $F$ define

$$
\frac{a}{b}+\frac{c}{d}=\frac{ad+bc}{bd}.
$$

$$
\frac{a}{b}\cdot\frac{c}{d}=\frac{ac}{bd}.
$$

Prove that $F$ with the above addition and multiplication is a field;
(4) Prove that the map $R$ from $F$ to $a\mapsto a/1$ is a monomorphism, so that $R$ can be regarded as a subring of $F$, and hence $F$ is a field of fractions of $R$;
(5) Let $K$ be a field containing $R$. Prove that $K$ contains a subfield $F_2$ with $F_2\supseteq R$, and that $F_2$ is a field of fractions of $R$; hence the field of fractions is the smallest field containing $R$.

### Solution to Problem 4

(1) Since $R$ is an integral domain, $b,d\ne0$ when $bd\ne0$, so the above operations are closed. Commutativity and associativity of addition and multiplication follow directly from the corresponding operations in $R$. For addition, $\left(a,b\right)+\left(0,1\right)=\left(a,b\right)$; for multiplication, $\left(a,b\right)\left(1,1\right)=\left(a,b\right)$. Hence the two are commutative monoids with identity elements $\left(0,1\right)$ and $\left(1,1\right)$ respectively.

(2) **Equivalence relation** Reflexivity: $ab=ba$. Symmetry: $ad=bc$ is the same as $bc=ad$. Transitivity: suppose $\left(a,b\right)\sim\left(c,d\right)$ and $\left(c,d\right)\sim\left(e,f\right)$; then $ad=bc$ and $cf=de$. Multiplying these equations by $f$ and $b$ respectively gives $adf=bcf=bde$, and cancelling $d\ne0$ gives $af=be$, so $\left(a,b\right)\sim\left(e,f\right)$.

**Congruence relation** Suppose $\left(a,b\right)\sim\left(a',b'\right)$ and $\left(c,d\right)\sim\left(c',d'\right)$, i.e. $ab'=a'b$ and $cd'=c'd$. Then

$$
\left(ab'\right)\left(cd'\right)=\left(a'b\right)\left(c'd\right),
$$

i.e. $ac\cdot b'd'=bd\cdot a'c'$, so

$$
\left(a,b\right)\left(c,d\right)\sim\left(a',b'\right)\left(c',d'\right).
$$

Addition is similar:

$$
\begin{aligned}\left(ad+bc\right)b'd'&=ab'dd'+cd'bb'\\&=a'bdd'+c'dbb'\\&=bd\left(a'd'+b'c'\right),\end{aligned}
$$

so the sums are also equivalent. Hence the operations are well defined on equivalence classes.

(3) By (2), the operations on $F$ are well defined and preserve commutativity, associativity and distributivity. $0/1$ is the zero element and $1/1$ is the identity. The negative of $a/b$ is $\left(-a\right)/b$. If $a/b\ne0/1$, then $a\ne0$ (otherwise $\left(a,b\right)\sim\left(0,1\right)$ means $a=0$), and its inverse is $b/a$. Hence $F$ is a commutative ring with identity in which every nonzero element is invertible. By **Definition 2.2.20** (Integral Domain, Division Ring, and Field), $F$ is a field.

(4) Consider $\iota:R\to F$, $\iota\left(a\right)=a/1$. Then

$$
\begin{aligned}\iota\left(a+b\right)&=\frac{a+b}{1}\\&=\frac{a}{1}+\frac{b}{1}\\&=\iota\left(a\right)+\iota\left(b\right),\end{aligned}
$$

$$
\begin{aligned}\iota\left(ab\right)&=\frac{ab}{1}\\&=\frac{a}{1}\cdot\frac{b}{1}\\&=\iota\left(a\right)\iota\left(b\right).\end{aligned}
$$

Also, $a/1=0/1$ if and only if $a=0$, so $\iota$ is a monomorphism. Hence $R$ can be identified with $\iota\left(R\right)\subseteq F$. For any $a/b\in F$, $a/b=\left(a/1\right)\left(b/1\right)^{-1}$, i.e. every element of $F$ can be written as a quotient of two elements of $R$, so $F$ is a field of fractions of $R$.

(5) In $K$, set

$$
F_2=\left\{ab^{-1}\mid a,b\in R,\;b\ne0\right\}.
$$

$F_2$ is closed under addition, subtraction and multiplication, and the inverse of a nonzero element $ab^{-1}$ is $ba^{-1}$, so $F_2$ is a subfield of $K$. Also $a=a\cdot1^{-1}\in F_2$, so $R\subseteq F_2$. Any field containing $R$ must contain all $ab^{-1}$, and hence must contain $F_2$. Therefore $F_2$ is the smallest field containing $R$, i.e. the field of fractions of $R$. $\blacksquare$
