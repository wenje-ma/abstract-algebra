# week9

> **Definition 2.5.2 (Associates)**
> 
> Let $R$ be an integral domain and $a,b\in R$. If there exists a unit $u$ in $R$ such that $a=ub$, then $a$ and $b$ are called associates, written $a\sim b$.

> **Definition 2.5.6 (Irreducible Element)**
> 
> Let $R$ be an integral domain and $\alpha\in R^{*}\setminus U$ (i.e. nonzero and not a unit). If $\alpha$ has no nontrivial divisors, then $\alpha$ is called an irreducible element.

> **Definition 2.5.14 (Common Divisors and Greatest Common Divisors)**
> 
> Let $R$ be an integral domain and $a_1,a_2,\cdots,a_n\in R$. If $c\in R$ divides every $a_i$, then $c$ is called a common divisor of them; if a common divisor $d$ is divisible by every common divisor, then $d$ is called a greatest common divisor. If the greatest common divisor of $a,b$ is a unit, then $a,b$ are called coprime.

> **Theorem 2.5.15 (Equivalent Conditions for a Unique Factorization Domain)**
> 
> An integral domain $R$ is a unique factorization domain if and only if $R$ satisfies the factor chain condition and the prime condition; in particular, in a unique factorization domain every irreducible element is a prime element, i.e. $p\mid ab$ implies $p\mid a$ or $p\mid b$.

> **Definition 2.6.1 (Prime Ideal)**
> 
> Let $I$ be an ideal of a ring $R$ with $I\ne R$. If $ab\in I$ implies $a\in I$ or $b\in I$, then $I$ is called a prime ideal of $R$.

> **Definition 2.7.1 (Principal Ideal Ring)**
> 
> A commutative unital ring is called a principal ideal ring if every ideal of it is principal; if a principal ideal ring is also an integral domain, it is called a principal ideal domain.

> **Definition 2.7.9 (Euclidean Ring)**
> 
> Let $R$ be an integral domain. If there exists a map $\delta$ from $R^{*}$ to the set of nonnegative integers such that for any $a,b\in R$ with $b\ne0$, there exist $q,r\in R$ with $a=qb+r$, where $r=0$ or $\delta\left(r\right)< \delta\left(b\right)$, then $\left(R,\delta\right)$ is called a Euclidean ring; briefly, $R$ is a Euclidean ring.

## 2.5-10

Let $R=\mathbb Z\left[\omega\right]$, where $\omega=\frac{1+\sqrt{-3}}{2}$ (the ring of algebraic integers of $\mathbb Q\left(\sqrt{-3}\right)$).

(1) Prove that $R$ is an integral domain under the usual addition and multiplication of numbers;

(2) Prove that all units of $R$ are $\pm1$, $\frac{\pm1\pm\sqrt{-3}}{2}$;

(3) Prove that in $R$ the elements $2$ and $1+\sqrt{-3}$ are associates.

### Solution to 2.5-10

By The Norm on the Ring of Integers $\mathbb Z\left[\omega\right]$, $\omega^{2}=\omega-1$, so

$$
R=\mathbb Z\left[\omega\right]=\left\{m+n\omega\mid m,n\in\mathbb Z\right\}
$$

is closed under multiplication ($\omega^{2}=\omega-1\in R$).

Part (1). $R\subseteq\mathbb C$. $R$ is closed under addition (componentwise), closed under multiplication, and contains the identity $1$. Since $\mathbb C$ has no zero divisors, $R$ is a commutative unital ring without zero divisors, hence an integral domain.

Part (2). By The Norm on the Ring of Integers $\mathbb Z\left[\omega\right]$, define

$$
N\left(m+n\omega\right)=\left(m+n\omega\right)\left(m+n\overline\omega\right)=m^{2}+mn+n^{2},
$$

which is multiplicative, and $\xi$ is a unit if and only if $N\left(\xi\right)=1$. Solving

$$
m^{2}+mn+n^{2}=1,\quad m,n\in\mathbb Z,
$$

gives

$$
\left(m,n\right)=\left(\pm1,0\right),\;\left(0,\pm1\right),\;\left(1,-1\right),\;\left(-1,1\right).
$$

The corresponding elements are $\pm1$, $\pm\omega$, $\pm\left(1-\omega\right)$. Since $\omega=\frac{1+\sqrt{-3}}{2}$ and $1-\omega=\frac{1-\sqrt{-3}}{2}$, all units of $R$ are $\pm1$ and $\frac{\pm1\pm\sqrt{-3}}{2}$.

Part (3). Since $1+\sqrt{-3}=2\omega$ and $\omega$ is a unit ($N\left(\omega\right)=1$), i.e. $1+\sqrt{-3}=2\cdot\omega$ with $\omega$ a unit, by **Definition 2.5.2 (Associates)** the elements $2$ and $1+\sqrt{-3}$ are associates. $\blacksquare$

## 2.5-15

It is known that $\mathbb Q\left[x,y\right]$ is a ring under polynomial addition and multiplication. Prove that $x$ and $y$ are coprime. Is there $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ such that $r\left(x,y\right)x+s\left(x,y\right)y=1$?

### Solution to 2.5-15

By Polynomial Rings over a Field Are Unique Factorization Domains, $\mathbb Q\left[x,y\right]$ is a unique factorization domain, and $x,y$ are both irreducible elements. They are non-associate: their units are exactly the nonzero constants in $\mathbb Q^{*}$, and $x\ne cy$ for any $c\in\mathbb Q^{*}$. Hence the common divisors of $x,y$ are only units, so their greatest common divisor is a unit; by **Definition 2.5.14 (Common Divisors and Greatest Common Divisors)**, $x$ and $y$ are coprime.

But no such $r,s$ exist. Suppose, toward contradiction, that $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ satisfy $r\left(x,y\right)x+s\left(x,y\right)y=1$. Evaluating both sides at $\left(0,0\right)$:

$$
r\left(0,0\right)\cdot0+s\left(0,0\right)\cdot0=1,
$$

i.e. $0=1$, a contradiction.

Hence, although $x$ and $y$ are coprime, there do not exist $r,s\in\mathbb Q\left[x,y\right]$ with $rx+sy=1$. $\blacksquare$

## 2.6-13

Let $R$ be a unique factorization domain and $p\in R^{*}$. Prove: $p$ is an irreducible element if and only if the principal ideal $\left(p\right)$ is a prime ideal.

### Solution to 2.6-13

Suppose $p\in R^{*}\setminus U$ (if $p$ is zero or a unit, the conclusion is trivial and not discussed).

Necessity: Suppose $p$ is an irreducible element. Since $R$ is a unique factorization domain, by **Theorem 2.5.15 (Equivalent Conditions for a Unique Factorization Domain)** $p$ is a prime element, i.e. $p\mid ab$ implies $p\mid a$ or $p\mid b$. By Principal Ideals and Divisibility, $ab\in\left(p\right)$ is equivalent to $p\mid ab$, $a\in\left(p\right)$ to $p\mid a$, and $b\in\left(p\right)$ to $p\mid b$. Hence $ab\in\left(p\right)$ implies $a\in\left(p\right)$ or $b\in\left(p\right)$. Moreover, since $p$ is not a unit, by Principal Ideals and Divisibility $1\notin\left(p\right)$ (otherwise $p\mid1$, making $p$ a unit), so $\left(p\right)\ne R$. By **Definition 2.6.1 (Prime Ideal)**, $\left(p\right)$ is a prime ideal.

Sufficiency: Suppose $\left(p\right)$ is a prime ideal. Assume, toward contradiction, that $p$ is reducible, i.e. there exist $a,b\in R$, both non-units, with $p=ab$. Since $ab=p\in\left(p\right)$, by **Definition 2.6.1 (Prime Ideal)** we have $a\in\left(p\right)$ or $b\in\left(p\right)$. If $a\in\left(p\right)$, by Principal Ideals and Divisibility there exists $r\in R$ with $a=pr$; then $p=ab=prb$. Since $p\ne0$ (as $p\in R^{*}$) and $R$ is an integral domain, by Cancellation in an Integral Domain we cancel $p$ to get $1=rb$, so $b$ is a unit, contradicting that $b$ is not a unit. If $b\in\left(p\right)$, similarly there exists $r\in R$ with $b=pr$, hence $p=ab=apr$; canceling $p$ gives $1=ar$, so $a$ is a unit, also a contradiction.

Hence $p$ is an irreducible element. $\blacksquare$

## 2.7-7

Prove that $\mathbb Z\left[\frac{1+\sqrt{-3}}{2}\right]$ is a Euclidean ring.

### Solution to 2.7-7

Write $\omega=\frac{1+\sqrt{-3}}{2}$. Then $\overline\omega=\frac{1-\sqrt{-3}}{2}=1-\omega$, and $\omega+\overline\omega=1$, $\omega\overline\omega=1$. By The Norm on the Ring of Algebraic Integers, define the norm on $\alpha=a+b\omega\in R=\mathbb Z\left[\omega\right]$ as

$$
N\left(a+b\omega\right)=\left(a+b\omega\right)\left(a+b\overline\omega\right)=a^{2}+ab\left(\omega+\overline\omega\right)+b^{2}\omega\overline\omega=a^{2}+ab+b^{2},
$$

which is a positive definite quadratic form and is multiplicative. We verify that $R$ satisfies the division-with-remainder condition of **Definition 2.7.9 (Euclidean Ring)** under the map $\delta=N$.

Take any $\alpha,\beta\in R$ with $\beta\ne0$. Perform the division in $\mathbb Q\left(\sqrt{-3}\right)$: $\frac{\alpha}{\beta}=x+y\omega$, where $x,y\in\mathbb Q$. Choose integers $m,n$ nearest to $x,y$ respectively, i.e. $\left|x-m\right|\le\frac12$, $\left|y-n\right|\le\frac12$. Put $q=m+n\omega\in R$ and $r=\alpha-q\beta$. Then

$$
r=\beta\left[\left(x-m\right)+\left(y-n\right)\omega\right].
$$

Write $u=x-m$, $v=y-n$; then $\left|u\right|\le\frac12$, $\left|v\right|\le\frac12$. By the multiplicativity of the norm (see The Norm on the Ring of Algebraic Integers),

$$
N\left(r\right)=N\left(\beta\right)N\left(u+v\omega\right)=N\left(\beta\right)\left(u^{2}+uv+v^{2}\right).
$$

By A Bound for a Quadratic Form, when $\left|u\right|,\left|v\right|\le\frac12$ we have $u^{2}+uv+v^{2}\le\frac34$. Hence

$$
N\left(r\right)\le\frac34\,N\left(\beta\right)< N\left(\beta\right).
$$

Thus $\alpha=q\beta+r$ with $r=0$ or $N\left(r\right)< N\left(\beta\right)$. By **Definition 2.7.9 (Euclidean Ring)**, $R=\mathbb Z\left[\frac{1+\sqrt{-3}}{2}\right]$ is a Euclidean ring. $\blacksquare$

## 2.7-11

Prove that $\mathbb Z\left[\sqrt{-6}\right]$ is not a Euclidean ring.

### Solution to 2.7-11

Write $R=\mathbb Z\left[\sqrt{-6}\right]$. For $\alpha=a+b\sqrt{-6}\in R$, by The Norm on the Ring of Algebraic Integers define the norm $N\left(\alpha\right)=a^{2}+6b^{2}$, which is multiplicative. First determine the units of $R$: if $\alpha$ is a unit, then $N\left(\alpha\right)=1$, i.e. $a^{2}+6b^{2}=1$; this forces $b=0$, $a=\pm1$. Hence the units of $R$ are only $\pm1$.

Suppose, toward contradiction, that $\left(R,\delta\right)$ is a Euclidean ring. Choose $m\in R\setminus\left\{0,\pm1\right\}$ with $\delta\left(m\right)$ minimal.

Apply division with remainder to $a=2$, $b=m$: $2=qm+r$, where $r=0$ or $\delta\left(r\right)< \delta\left(m\right)$. By the minimality of $m$, in the latter case $r$ must be $\pm1$ (a nonzero element with $\delta\left(r\right)< \delta\left(m\right)$ can only be a unit $\pm1$). Hence

$$
qm=2-r\in\left\{2,1,3\right\}.
$$

Taking norms, $N\left(q\right)N\left(m\right)\in\left\{4,1,9\right\}$. Since $m$ is not a unit, $N\left(m\right)> 1$. The equations $a^{2}+6b^{2}=2$ and $a^{2}+6b^{2}=3$ have no integer solutions, so $N\left(m\right)\notin\left\{2,3\right\}$ and can only be $4$ or $9$. Hence $N\left(q\right)=1$, $q=\pm1$, so $m=\pm2$ or $m=\pm3$.

Now apply division with remainder to $a=\sqrt{-6}$, $b=m$: $\sqrt{-6}=q'm+r'$, and similarly $r'\in\left\{0,\pm1\right\}$. Write $q'=a'+b'\sqrt{-6}$.

If $m=\pm2$, then

$$
\pm2q'=2a'\pm2b'\sqrt{-6}=\sqrt{-6}+r'.
$$

Comparing the coefficient of $\sqrt{-6}$ gives $2b'=1$, i.e. $b'=\frac12\notin\mathbb Z$, a contradiction.

If $m=\pm3$, comparing the coefficient of $\sqrt{-6}$ similarly gives $3b'=1$, i.e. $b'=\frac13\notin\mathbb Z$, a contradiction.

Both cases lead to contradictions, so no such Euclidean map $\delta$ exists. By **Definition 2.7.9 (Euclidean Ring)**, $R=\mathbb Z\left[\sqrt{-6}\right]$ is not a Euclidean ring. $\blacksquare$

## 2.7-14

This problem proves that the integral domain $R=\mathbb Z\left[\frac{1+\sqrt{-19}}{2}\right]$ is a principal ideal domain but not a Euclidean ring, writing $\omega=\frac{1+\sqrt{-19}}{2}$.

(1) Prove that the units of $R$ are only $1$ and $-1$;

(2) Prove that $2$ and $3$ are irreducible elements of $R$;

(3) Prove that $R$ is not a Euclidean ring (hint: by contradiction. If $\left(R,\delta\right)$ is a Euclidean ring, choose $m\in R$ with $m\ne0,\pm1$ and $\delta\left(m\right)=\min\left\{\delta\left(a\right)\mid a\ne0,a\ne\pm1\right\}$. First divide $2$ by $m$, from which one proves $m=\pm2$ or $\pm3$; then divide $\omega$ by $m$ to derive a contradiction);

(4) Let $I$ be a nonzero ideal of $R$, and choose $b\in I$ with $\left|b\right|\le\left|c\right|$ for all $c\in I$, where $\left|\cdot\right|$ denotes the complex modulus. Prove: for any $a\in I$, there exists $q\in R$ such that $a-qb\in I$ and $\left|a-qb\right|< \left|b\right|$;

(5) Prove: when the rational coordinate $y$ of $a/b=x+y\omega$ is far from $\frac12$, there exist integers $m,n$ with $N\left(a/b-\left(m+n\omega\right)\right)< 1$;

(6) Prove: when $y$ is near $\frac12$, using $2a\in I$ and an integer translation one still obtains $\left|a-qb\right|< \left|b\right|$;

(7) Prove that $R$ is a principal ideal domain.

### Solution to 2.7-14

From $\omega=\frac{1+\sqrt{-19}}{2}$ we get $\overline\omega=\frac{1-\sqrt{-19}}{2}$, and $\omega+\overline\omega=1$, $\omega\overline\omega=5$. By The Norm on the Ring of Algebraic Integers, the norm on $\alpha=a+b\omega\in R$ is

$$
N\left(a+b\omega\right)=\left(a+b\omega\right)\left(a+b\overline\omega\right)=a^{2}+ab\left(\omega+\overline\omega\right)+b^{2}\omega\overline\omega=a^{2}+ab+5b^{2},
$$

which is a positive definite quadratic form and is multiplicative. Note that when $\left|b\right|\ge1$,

$$
a^{2}+ab+5b^{2}=\left(a+\frac{b}{2}\right)^{2}+\frac{19}{4}b^{2}\ge\frac{19}{4}> 4.
$$

Part (1). If $\alpha=a+b\omega$ is a unit, by The Norm on the Ring of Algebraic Integers we have $N\left(\alpha\right)=1$. If $b\ne0$, the inequality above gives $N\left(\alpha\right)\ge\frac{19}{4}> 1$, a contradiction. Hence $b=0$, $a^{2}=1$, $a=\pm1$. Thus the units of $R$ are only $1$ and $-1$.

Part (2). First prove $2$ is irreducible. If $2=\alpha\beta$ is a nontrivial factorization, then $\alpha,\beta$ are both non-units and $N\left(\alpha\right)N\left(\beta\right)=N\left(2\right)=4$; by The Norm on the Ring of Algebraic Integers, $N\left(\alpha\right),N\left(\beta\right)> 1$, so $N\left(\alpha\right)=2$. But $a^{2}+ab+5b^{2}=2$ has no integer solution: for $b=0$ we need $a^{2}=2$, impossible; for $\left|b\right|\ge1$ the left side is $\ge\frac{19}{4}> 2$. A contradiction, so $2$ is irreducible.

Similarly, if $3=\alpha\beta$ is a nontrivial factorization, then $N\left(\alpha\right)=3$, but $a^{2}+ab+5b^{2}=3$ also has no integer solution (by the same argument). Hence $3$ is irreducible.

Part (3). By contradiction. Suppose $\left(R,\delta\right)$ is a Euclidean ring, and choose $m\in R\setminus\left\{0,\pm1\right\}$ with $\delta\left(m\right)$ minimal. Apply division with remainder to $a=2$, $b=m$: $2=qm+r$; by the minimality of $m$, $r\in\left\{0,\pm1\right\}$, so $qm\in\left\{1,2,3\right\}$. Taking norms, $N\left(q\right)N\left(m\right)\in\left\{1,4,9\right\}$.

By the estimate in Part (1), the smallest norm of $R$ greater than $1$ is $4$ (attained by $\pm2$), and the next is $5$ (attained by $\omega$ etc., since $N\left(\omega\right)=5$). Since $5$ divides none of $1,4,9$, $N\left(m\right)$ can only be $4$ or $9$, and $N\left(q\right)=1$. Hence $q=\pm1$, so $m=\pm2$ or $m=\pm3$.

Now apply division with remainder to $a=\omega$, $b=m$: $\omega=q'm+r'$, and similarly $r'\in\left\{0,\pm1\right\}$. Write $q'=a'+b'\omega$. If $m=\pm2$, then

$$
\pm2q'=\pm2a'\pm2b'\omega=\omega+r',
$$

and comparing the coefficient of $\omega$ gives $2b'=1$, so $b'=\frac12\notin\mathbb Z$, a contradiction. If $m=\pm3$, comparing the coefficient of $\omega$ gives $3b'=1$, so $b'=\frac13\notin\mathbb Z$, a contradiction. Hence $R$ is not a Euclidean ring.

Part (4). Take any nonzero ideal $I$, and choose $b\in I$ of minimal complex modulus $\left|b\right|$. For any $a\in I$, put

$$
z=\frac{a}{b}=x+y\omega\in\mathbb Q\left(\sqrt{-19}\right).
$$

Part (5). If $y$ is far from $\frac12$ (i.e. $\left|v\right|\le\frac{2}{\sqrt{19}}$, where $v$ is the deviation of $y$ from the nearest integer), then by A Bound for a Quadratic Form, $N\left(u+v\omega\right)=\left(u+\frac v2\right)^{2}+\frac{19}{4}v^{2}$ attains its minimum in $u$ at $u=-\frac v2$. Choose the integer $m$ as the nearest integer to $x+\frac v2$ and the integer $n$ as the nearest integer to $y$, and put $q=m+n\omega$; then $\left|u+\frac v2\right|\le\frac12$ and

$$
N\left(z-q\right)=N\left(u+v\omega\right)=\left(u+\frac v2\right)^{2}+\frac{19}{4}v^{2}\le\frac14+\frac{19}{4}\cdot\frac{4}{19}=\frac54.
$$

This estimate is not enough to guarantee $< 1$. Precisely, we may not obtain $u=-\frac v2$ exactly, but we can choose an integer $m$ with $\left|u+\frac v2\right|\le\frac12$; since $\left|v\right|\le\frac{2}{\sqrt{19}}$, we have $\frac{19}{4}v^{2}\le1$. If $\frac{19}{4}v^{2}< 1$, then choosing $\left|u+\frac v2\right|$ small enough yields $N\left(z-q\right)< 1$; if $\frac{19}{4}v^{2}=1$ (i.e. $\left|v\right|=\frac{2}{\sqrt{19}}$), then $v$ cannot be altered by an integer translation, but this case is handled in Part (6) using $2a\in I$. Hence, when $\left|v\right|$ is away from $\frac{2}{\sqrt{19}}$, there exist $m,n\in\mathbb Z$ with

$$
N\left(z-q\right)< 1.
$$

Part (6). If the direct choice above cannot achieve $N\left(z-q\right)< 1$, then $\left|v\right|$ must be near $\frac12$ (hence $\frac{19}{4}v^{2}> 1$ and $v$ near $\pm\frac12$). In this case consider $2z=\frac{2a}{b}=2x+2y\omega$, whose $\omega$-coordinate is $2y$. Since $y$ is near $\frac12$, $2y$ is near $1$, so the deviation $\left|v'\right|$ of $2y$ from the nearest integer satisfies $\left|v'\right|\le\frac14< \frac{2}{\sqrt{19}}$; by Part (5) there exists $q'\in R$ with

$$
N\left(2z-q'\right)< 1,
$$

i.e. $N\left(2a-q'b\right)=N\left(b\right)N\left(2z-q'\right)< N\left(b\right)$, equivalently $\left|2a-q'b\right|< \left|b\right|$. Since $2a\in I$ and $q'b\in\left(b\right)\subseteq I$, we have $2a-q'b\in I$; by the minimality of $\left|b\right|$, $2a-q'b=0$, i.e. $2a=q'b$.

Now handle $a$ itself: since $2a=q'b$ and $a\in I$, applying Part (5) or the above argument to $a$ again (dividing by $2$ repeatedly if necessary) ultimately yields some $q\in R$ with $a-qb=0$, i.e. $a\in\left(b\right)$. Hence for every $a\in I$ there exists $q\in R$ with $a-qb=0$ and $\left|a-qb\right|=0< \left|b\right|$, satisfying the requirement of Part (4).

Part (7). By Parts (5) and (6), for every $a\in I$ there exists $q\in R$ with $a=qb\in\left(b\right)$, so $I\subseteq\left(b\right)$. Conversely, since $b\in I$ and $I$ is an ideal, $\left(b\right)\subseteq I$. Hence $I=\left(b\right)$, i.e. every nonzero ideal of $R$ is principal (the zero ideal $\left\{0\right\}$ is also principal). By **Definition 2.7.1 (Principal Ideal Ring)**, $R$ is a principal ideal domain. Combined with Part (3), $R$ is a principal ideal domain but not a Euclidean ring. $\blacksquare$
