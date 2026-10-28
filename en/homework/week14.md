# week14

> **Basic Knowledge: Ring Automorphisms Fix the Prime Subfield**<br>If $\varphi$ is an automorphism of a field (or of a ring containing $1$), then $\varphi\left(1\right)=1$; since $\varphi$ preserves addition and multiplication and maps $1$ to $1$, it is the identity on the rational field $\mathbb Q$.

> **Basic Knowledge: Order-Preserving Property of the Real Field**<br>A real number $x>0$ if and only if there exists $y\ne0$ with $x=y^{2}$. Hence a field automorphism $\varphi:\mathbb R\to\mathbb R$ maps positive numbers to positive numbers and is therefore strictly increasing; moreover, the rational numbers are dense in $\mathbb R$.

> **Basic Knowledge: An Integral Domain Has No Zero Divisors**<br>An integral domain has no zero divisors, so if $b,d\ne0$ then $bd\ne0$; and from $d\ne0$ together with $d\left(af-be\right)=0$ one may conclude $af=be$.

> **Basic Knowledge: Congruence Relations and Quotient Structures**<br>If an equivalence relation $\sim$ is a congruence for an operation, then that operation is well-defined on the quotient set, and the corresponding commutativity, associativity and distributivity are preserved.

> **Basic Knowledge: Inverses in a Field**<br>Every nonzero element of a field is invertible; if $a,b\ne0$, then $\left(ab^{-1}\right)^{-1}=ba^{-1}$.

> **Definition 2.2.20 (Integral Domain, Division Ring, and Field)**<br>A commutative unital ring without zero divisors is called an integral domain; if a unital ring $R$ satisfies that $R^{*}$ forms a group under multiplication (where $R^{*}=R\setminus\left\{0\right\}$), then $R$ is called a division ring; a commutative division ring is called a field.

> **Definition 2.4.1 (Ring Homomorphism and Isomorphism)**<br>Let $R_1,R_2$ be two rings and $f$ a map from $R_1$ to $R_2$. If for any $a,b\in R_1$ we have $f\left(a+b\right)=f\left(a\right)+f\left(b\right)$ and $f\left(ab\right)=f\left(a\right)f\left(b\right)$, then $f$ is called a homomorphism; an injective homomorphism is called a monomorphism, a surjective homomorphism an epimorphism, and a bijective homomorphism an isomorphism.

---

## 2.4-6

Find all automorphisms of the field

$$
\mathbb Q\left[\sqrt{-1}\right]=\left\{a+b\sqrt{-1}\mid a,b\in\mathbb Q\right\}.
$$

### Solution 2.4-6

Write $i=\sqrt{-1}$. Let $\varphi:\mathbb Q\left[i\right]\to\mathbb Q\left[i\right]$ be a ring automorphism. By **Definition 2.4.1 (Ring Homomorphism and Isomorphism)**, $\varphi$ preserves multiplication and addition; since $\varphi\left(1\right)=1$, by **Basic Knowledge: Ring Automorphisms Fix the Prime Subfield** $\varphi$ is the identity on $\mathbb Q$.

Let $\varphi\left(i\right)=u=a+bi$, $a,b\in\mathbb Q$. Since $i^{2}=-1$ and $\varphi$ preserves multiplication and addition,

$$
u^{2}=\varphi\left(i\right)^{2}=\varphi\left(i^{2}\right)=\varphi\left(-1\right)=-1.
$$

That is,

$$
\left(a+bi\right)^{2}=a^{2}-b^{2}+2abi=-1.
$$

Comparing real and imaginary parts gives $2ab=0$ and $a^{2}-b^{2}=-1$. If $b=0$, then $a^{2}=-1$, which has no solution in $\mathbb Q$; hence $a=0$, $b^{2}=1$, $b=\pm1$. Thus $u=i$ or $u=-i$.

Case one $\varphi\left(i\right)=i$: then for $a,b\in\mathbb Q$, $\varphi\left(a+bi\right)=a+bi$, i.e. the identity automorphism.

Case two $\varphi\left(i\right)=-i$: then $\varphi\left(a+bi\right)=a-bi$, i.e. the complex conjugation map.

Both maps preserve addition and multiplication (conjugation preserves the operations over $\mathbb Q$) and are bijective, so by **Definition 2.4.1 (Ring Homomorphism and Isomorphism)** they are automorphisms. Hence $\mathbb Q\left[i\right]$ has exactly two automorphisms: the identity and conjugation. $\blacksquare$

---

## 2.4-7

Prove that the only automorphism of the real field is the identity.

### Solution 2.4-7

Let $\varphi:\mathbb R\to\mathbb R$ be a field automorphism. By **Definition 2.4.1 (Ring Homomorphism and Isomorphism)** and **Basic Knowledge: Ring Automorphisms Fix the Prime Subfield**, $\varphi\left(1\right)=1$, so $\varphi$ is the identity on $\mathbb Q$: $\varphi\left(n\right)=n$ for integers $n$, and $\varphi\left(m/n\right)=m/n$ for $\frac{m}{n}\in\mathbb Q$.

**Order preservation**: If $x>0$, by **Basic Knowledge: Order-Preserving Property of the Real Field**, there exists $y\ne0$ with $x=y^{2}$; then

$$
\varphi\left(x\right)=\varphi\left(y^{2}\right)=\varphi\left(y\right)^{2}>0
$$

(since $\varphi\left(y\right)\ne0$, its square is positive). Hence when $x>y$, $x-y>0$ gives $\varphi\left(x\right)-\varphi\left(y\right)=\varphi\left(x-y\right)>0$, i.e. $\varphi$ is strictly increasing.

**Identity**: Suppose, toward contradiction, that there exists $x\in\mathbb R$ with $\varphi\left(x\right)\ne x$. If $\varphi\left(x\right)>x$, by **Basic Knowledge: Order-Preserving Property of the Real Field** (density of rationals), choose $q\in\mathbb Q$ with $x<q<\varphi\left(x\right)$. Since $x<q$ and $\varphi$ is strictly increasing, $\varphi\left(x\right)<\varphi\left(q\right)=q$, contradicting $q<\varphi\left(x\right)$. If $\varphi\left(x\right)<x$, similarly choose $q\in\mathbb Q$ with $\varphi\left(x\right)<q<x$; by the strict monotonicity of $\varphi$ and $q=\varphi\left(q\right)$, we get $q<\varphi\left(x\right)$, a contradiction.

Hence $\varphi\left(x\right)=x$ for all $x\in\mathbb R$, i.e. $\varphi$ is the identity. $\blacksquare$

---

## 2.4-8

Prove that the map $a+b\sqrt{-1}\mapsto a-b\sqrt{-1}$ is an automorphism of the ring $\mathbb C$.

### Solution 2.4-8

Let $\varphi:\mathbb C\to\mathbb C$, $\varphi\left(a+bi\right)=a-bi$, where $a,b\in\mathbb R$.

**Preserves addition**: for $a+bi$, $c+di\in\mathbb C$,

$$
\varphi\left(\left(a+bi\right)+\left(c+di\right)\right)=\varphi\left(\left(a+c\right)+\left(b+d\right)i\right)=\left(a+c\right)-\left(b+d\right)i=\left(a-bi\right)+\left(c-di\right)=\varphi\left(a+bi\right)+\varphi\left(c+di\right).
$$

**Preserves multiplication**:

$$
\varphi\left(\left(a+bi\right)\left(c+di\right)\right)=\varphi\left(\left(ac-bd\right)+\left(ad+bc\right)i\right)=\left(ac-bd\right)-\left(ad+bc\right)i,
$$

whereas

$$
\varphi\left(a+bi\right)\varphi\left(c+di\right)=\left(a-bi\right)\left(c-di\right)=ac-bd-\left(ad+bc\right)i.
$$

The two are equal, so $\varphi$ preserves multiplication.

Moreover, applying $\varphi$ twice returns to the identity, i.e. $\varphi\circ\varphi=\mathrm{id}$, so $\varphi$ is bijective. By **Definition 2.4.1 (Ring Homomorphism and Isomorphism)**, $\varphi$ is an automorphism of $\mathbb C$. $\blacksquare$

---

## 2.4-19

This problem proves the existence and uniqueness of the fraction field of an integral domain. Let an integral domain $R$ be a subring of a field $F$. If for every $a\in F$ there exist $b,c\in R$ with $a=bc^{-1}$, then $F$ is called a fraction field of $R$. Define addition and multiplication on the set $R\times R^{*}$ as follows:

$$
\left(a,b\right)+\left(c,d\right)=\left(ad+bc,bd\right),
$$

$$
\left(a,b\right)\left(c,d\right)=\left(ac,bd\right),
$$

where $\left(a,b\right),\left(c,d\right)\in R\times R^{*}$.

(1) Prove that $R\times R^{*}$ becomes a commutative monoid under both of the above addition and multiplication, with identity elements $\left(0,1\right)$ and $\left(1,1\right)$ respectively;

(2) On $R\times R^{*}$ define the relation $\left(a,b\right)\sim\left(c,d\right)$ if and only if $ad=bc$. Prove that $\sim$ is an equivalence relation and is a congruence for both the above multiplication and addition;

(3) Let $F=\left(R\times R^{*}\right)/\sim$ be the set of equivalence classes, and write the class of $\left(a,b\right)$ as $a/b$. Define on $F$ the operations

$$
\frac{a}{b}+\frac{c}{d}=\frac{ad+bc}{bd},
$$

$$
\frac{a}{b}\cdot\frac{c}{d}=\frac{ac}{bd}.
$$

Prove that $F$ becomes a field under the above addition and multiplication;

(4) Prove that the map $a\mapsto a/1$ from $R$ to $F$ is a monomorphism, so that $R$ may be viewed as a subring of $F$; thereby prove that $F$ is a fraction field of $R$;

(5) Let $K$ be a field containing $R$. Prove that $K$ contains a subfield $F_2$ with $F_2\supseteq R$ such that $F_2$ is a fraction field of $R$; hence the fraction field is the smallest field containing $R$.

### Solution 2.4-19

**Part (1).** Since $R$ is an integral domain, by **Basic Knowledge: An Integral Domain Has No Zero Divisors**, when $b,d\ne0$ we have $bd\ne0$, so $R\times R^{*}$ is closed under addition and multiplication. Commutativity and associativity follow directly componentwise from the corresponding laws in $R$. For addition, $\left(a,b\right)+\left(0,1\right)=\left(a\cdot1+b\cdot0,b\cdot1\right)=\left(a,b\right)$; for multiplication, $\left(a,b\right)\left(1,1\right)=\left(a\cdot1,b\cdot1\right)=\left(a,b\right)$. Hence the two operations are commutative monoids with identities $\left(0,1\right)$ and $\left(1,1\right)$ respectively.

**Part (2). Equivalence relation**: Reflexive: $\left(a,b\right)\sim\left(a,b\right)$ means $ab=ba$, which holds. Symmetric: $ad=bc$ is the same as $bc=ad$, so $\left(a,b\right)\sim\left(c,d\right)$ implies $\left(c,d\right)\sim\left(a,b\right)$. Transitive: suppose $\left(a,b\right)\sim\left(c,d\right)$ and $\left(c,d\right)\sim\left(e,f\right)$, i.e. $ad=bc$, $cf=de$. Multiplying the two equations by $f$ and $b$ respectively gives $adf=bcf=bde$, i.e. $d\left(af\right)=d\left(be\right)$; since $d\ne0$, by **Basic Knowledge: An Integral Domain Has No Zero Divisors** we cancel to get $af=be$, hence $\left(a,b\right)\sim\left(e,f\right)$. Thus $\sim$ is an equivalence relation.

**Congruence (multiplication)**: suppose $\left(a,b\right)\sim\left(a',b'\right)$ and $\left(c,d\right)\sim\left(c',d'\right)$, i.e. $ab'=a'b$, $cd'=c'd$. Then

$$
\left(ab'\right)\left(cd'\right)=\left(a'b\right)\left(c'd\right),
$$

i.e. $ac\cdot b'd'=bd\cdot a'c'$, so

$$
\left(a,b\right)\left(c,d\right)=\left(ac,bd\right)\sim\left(a'c',b'd'\right)=\left(a',b'\right)\left(c',d'\right).
$$

**Congruence (addition)**: likewise,

$$
\left(ad+bc\right)b'd'=ab'dd'+cd'bb'=a'bdd'+c'dbb'=bd\left(a'd'+b'c'\right),
$$

so $\left(ad+bc,bd\right)\sim\left(a'd'+b'c',b'd'\right)$, i.e. $\left(a,b\right)+\left(c,d\right)\sim\left(a',b'\right)+\left(c',d'\right)$. Hence $\sim$ is a congruence for both multiplication and addition.

**Part (3).** By Part (2) and **Basic Knowledge: Congruence Relations and Quotient Structures**, the addition and multiplication on $F$ are well-defined and preserve commutativity, associativity and distributivity. $0/1$ is the additive zero and $1/1$ is the multiplicative identity. The negative of $a/b$ is $\left(-a\right)/b$, because $\frac{a}{b}+\frac{-a}{b}=\frac{ab-ab}{b\cdot b}=\frac{0}{b^{2}}=\frac{0}{1}$. If $a/b\ne0/1$, then $a\ne0$ (otherwise $\left(a,b\right)\sim\left(0,1\right)$ means $a\cdot1=b\cdot0$, so $a=0$); then by **Basic Knowledge: Inverses in a Field** its multiplicative inverse is $b/a$, since $\frac{a}{b}\cdot\frac{b}{a}=\frac{ab}{ab}=\frac{1}{1}$. Hence $F$ is a commutative unital ring in which every nonzero element is invertible. By **Definition 2.2.20 (Integral Domain, Division Ring, and Field)**, $F$ is a field.

**Part (4).** Consider the map $\iota:R\to F$, $\iota\left(a\right)=a/1$. Then

$$
\iota\left(a+b\right)=\frac{a+b}{1}=\frac{a}{1}+\frac{b}{1}=\iota\left(a\right)+\iota\left(b\right),
$$

$$
\iota\left(ab\right)=\frac{ab}{1}=\frac{a}{1}\cdot\frac{b}{1}=\iota\left(a\right)\iota\left(b\right),
$$

and $a/1=0/1$ if and only if $a\cdot1=1\cdot0$, i.e. $a=0$, so $\iota$ is a monomorphism (by **Definition 2.4.1 (Ring Homomorphism and Isomorphism)**). Hence $R$ may be identified with $\iota\left(R\right)\subseteq F$. For any $a/b\in F$, we have $a/b=\left(a/1\right)\left(b/1\right)^{-1}$, i.e. every element of $F$ can be written as a quotient of two elements of $R$ (via the embedding $\iota$); hence $F$ is a fraction field of $R$ (by the definition in the problem).

**Part (5).** Inside $K$, let

$$
F_2=\left\{ab^{-1}\mid a,b\in R,\;b\ne0\right\}.
$$

$F_2$ is closed under addition ($ab^{-1}+cd^{-1}=\left(ad+bc\right)\left(bd\right)^{-1}$, where $ad+bc,bd\in R$ and $bd\ne0$ by **Basic Knowledge: An Integral Domain Has No Zero Divisors**), closed under multiplication ($\left(ab^{-1}\right)\left(cd^{-1}\right)=\left(ac\right)\left(bd\right)^{-1}$), and the inverse of a nonzero element $ab^{-1}$ (with $a\ne0$) is $\left(ab^{-1}\right)^{-1}=ba^{-1}\in F_2$ (by **Basic Knowledge: Inverses in a Field**). Hence $F_2$ is a subfield of $K$. Also $a=a\cdot1^{-1}\in F_2$, so $R\subseteq F_2$. Any field containing $R$ must contain all $ab^{-1}$ ($a,b\in R$, $b\ne0$), hence must contain $F_2$. Thus $F_2$ is the smallest field containing $R$, i.e. a fraction field of $R$. $\blacksquare$
