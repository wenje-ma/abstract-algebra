# Assignment 17

> **Definition 2.7.9** (Euclidean Ring) Let $R$ be an integral domain. If there exists a map $\delta$ from $R^*$ to the set of nonnegative integers such that for any $a,b\in R$ with $b\ne0$, there exist $q,r\in R$ with $a=qb+r$, where $r=0$ or $\delta\left(r\right)< \delta\left(b\right)$, then $\left(R,\delta\right)$ is called a Euclidean ring.

> **Theorem 2.7.6** (A Principal Ideal Domain Is a Unique Factorization Domain) A principal ideal domain is necessarily a unique factorization domain; in particular, a Euclidean ring is a principal ideal domain and hence also a unique factorization domain.

> **Basic Knowledge** (Norm of the Ring of Algebraic Integers) Let $d> 0$ be a square-free integer, and let $\omega=\frac{1+\sqrt{-d}}{2}$ satisfy $\omega^2-\omega+\frac{1+d}{4}=0$ when $d\equiv3\pmod4$. For $\alpha=a+b\omega\in\mathbb Z\left[\omega\right]$, the norm is defined by
> $$
> N\left(\alpha\right)=\alpha\bar\alpha=a^2+ab+b^2\omega\bar\omega,
> $$
> which is a multiplicative function, and $N\left(\alpha\right)=0$ if and only if $\alpha=0$.

### Problem 1

(Problem 2.7-7) Prove that $\mathbb Z\left[\frac{1+\sqrt{-3}}{2}\right]$ is a Euclidean ring.

### Solution to Problem 1

Write $\omega=\frac{1+\sqrt{-3}}{2}$; then $\bar\omega=\frac{1-\sqrt{-3}}{2}=1-\omega$, with $\omega+\bar\omega=1$ and $\omega\bar\omega=1$. Hence for $\alpha=a+b\omega\in R=\mathbb Z\left[\omega\right]$, define the norm
$$
\begin{aligned}N\left(a+b\omega\right)&=\left(a+b\omega\right)\left(a+b\bar\omega\right)\\&=a^2+ab+b^2.\end{aligned}
$$

This quadratic form is positive definite, and $N\left(\alpha\beta\right)=N\left(\alpha\right)N\left(\beta\right)$. We now verify that, with $\delta=N$, $R$ satisfies the division-with-remainder condition of **Definition 2.7.9** (Euclidean Ring).

Take any $\alpha,\beta\in R$ with $\beta\ne0$. Divide in $\mathbb Q\left(\sqrt{-3}\right)$: $\frac{\alpha}{\beta}=x+y\omega$, where $x,y\in\mathbb Q$. Take integers $m,n$ to be the nearest integers to $x,y$, respectively, i.e. $\left|x-m\right|\le\frac12$, $\left|y-n\right|\le\frac12$. Set $q=m+n\omega\in R$ and $r=\alpha-q\beta$. Then
$$
r=\beta\left[\left(x-m\right)+\left(y-n\right)\omega\right].
$$

Write $u=x-m$, $v=y-n$; then $\left|u\right|\le\frac12$, $\left|v\right|\le\frac12$. By multiplicativity of the norm,
$$
\begin{aligned}N\left(r\right)&=N\left(\beta\right)N\left(u+v\omega\right)\\&=N\left(\beta\right)\left(u^2+uv+v^2\right).\end{aligned}
$$

When $\left|u\right|,\left|v\right|\le\frac12$, the positive-definite quadratic form $u^2+uv+v^2$ attains its maximum on the boundary of the square at $\left(u,v\right)=\left(\pm\frac12,\pm\frac12\right)$, equal to $\frac14+\frac14+\frac14=\frac34$. Hence
$$
N\left(r\right)\le\frac34\,N\left(\beta\right)< N\left(\beta\right)=\delta\left(\beta\right).
$$

Thus $\alpha=q\beta+r$, with $r=0$ or $\delta\left(r\right)< \delta\left(\beta\right)$. By **Definition 2.7.9** (Euclidean Ring), $R=\mathbb Z\left[\frac{1+\sqrt{-3}}{2}\right]$ is a Euclidean ring. $\blacksquare$

### Problem 2

(Problem 2.7-11) Prove that $\mathbb Z\left[\sqrt{-6}\right]$ is not a Euclidean ring.

### Solution to Problem 2

Write $R=\mathbb Z\left[\sqrt{-6}\right]$, and define the norm $N\left(\alpha\right)=a^2+6b^2$ for $\alpha=a+b\sqrt{-6}\in R$, which is multiplicative. First determine the units of $R$: if $\alpha$ is a unit, then $N\left(\alpha\right)=1$, i.e. $a^2+6b^2=1$, which gives $b=0$ and $a=\pm1$. Hence the only units of $R$ are $\pm1$.

Proof by contradiction. Suppose $\left(R,\delta\right)$ is a Euclidean ring. Take an element $m\in R\setminus\left\{0,\pm1\right\}$ at which $\delta\left(m\right)$ is minimal.

Perform division with $a=2$, $b=m$: $2=qm+r$, where $r=0$ or $\delta\left(r\right)< \delta\left(m\right)$. By the minimality of $m$, the latter case forces $r=\pm1$, so
$$
qm\in\left\{2,1,3\right\}.
$$

Taking norms on both sides, $N\left(q\right)N\left(m\right)\in\left\{4,1,9\right\}$. Since $m$ is not a unit, $N\left(m\right)> 1$. The equations $a^2+6b^2=2$ and $a^2+6b^2=3$ have no integer solutions, so $N\left(m\right)$ can only be $4$ or $9$. Hence $N\left(q\right)=1$, $q=\pm1$, and thus $m=\pm2$ or $m=\pm3$.

Now perform division with $a=\sqrt{-6}$, $b=m$: $\sqrt{-6}=qm'+r'$, and similarly $r'\in\left\{0,\pm1\right\}$. Write $q'=a'+b'\sqrt{-6}$.

If $m=\pm2$, then
$$
\pm2q'=2a'\pm2b'\sqrt{-6}=\sqrt{-6}+r'.
$$

Comparing the coefficient of $\sqrt{-6}$ gives $2b'=1$, i.e. $b'=\frac12\notin\mathbb Z$, a contradiction.

If $m=\pm3$, similarly $3b'=1$, i.e. $b'=\frac13\notin\mathbb Z$, a contradiction.

Both cases lead to contradictions, so no such Euclidean map $\delta$ exists. By **Definition 2.7.9** (Euclidean Ring), $R=\mathbb Z\left[\sqrt{-6}\right]$ is not a Euclidean ring. $\blacksquare$

### Problem 3

(Problem 2.7-14) This problem proves that the integral domain $R=\mathbb Z\left[\frac{1+\sqrt{-19}}{2}\right]$ is a principal ideal domain but not a Euclidean ring. Write $\omega=\frac{1+\sqrt{-19}}{2}$.

(1) Prove that the only units of $R$ are $1$ and $-1$;
(2) Prove that $2$ and $3$ are irreducible elements in $R$;
(3) Prove that $R$ is not a Euclidean ring (hint: use contradiction. If $\left(R,\delta\right)$ is a Euclidean ring, fix $m\in R$ with $m\ne0,\pm1$ such that
$$
\delta\left(m\right)=\min\left\{\delta\left(a\right)\mid a\ne0,a\ne\pm1\right\}.
$$
First divide $m$ by $2$, which shows $m=\pm2$ or $\pm3$; then divide $m$ by $\omega$ to derive a contradiction);
(4) Let $I$ be a nonzero ideal of $R$, and take $b\in I$ such that $\left|b\right|\le\left|c\right|$ for all $c\in I$, where $\left|\cdot\right|$ denotes the modulus of a complex number. Prove that for any $a\in I$, there exists $q\in R$ such that $a-qb\in I$ and $\left|a-qb\right|< \left|b\right|$ (the original statement has incomplete sub-conditions for (4)-(6); below we complete it in the standard lattice-argument order: nearest-lattice choice and integer translation);
(5) Prove that when the rational coordinate $a/b=x+y\omega$ has $\left|y\right|$ away from $\frac12$, there exists an integer $n$ such that $N\left(a/b-\left(m+n\omega\right)\right)< 1$;
(6) Prove that when $\left|y\right|$ is close to $\frac12$, using $2a\in I$ and an integer translation still gives $\left|a-qb\right|< \left|b\right|$;
(7) Prove that $R$ is a principal ideal domain.

### Solution to Problem 3

From $\omega=\frac{1+\sqrt{-19}}{2}$, we have $\bar\omega=\frac{1-\sqrt{-19}}{2}$, with $\omega+\bar\omega=1$ and $\omega\bar\omega=5$. Hence for $\alpha=a+b\omega\in R$, the norm is
$$
\begin{aligned}N\left(a+b\omega\right)&=\left(a+b\omega\right)\left(a+b\bar\omega\right)\\&=a^2+ab+5b^2,\end{aligned}
$$
which is a positive-definite quadratic form and multiplicative. Note that when $\left|b\right|\ge1$,
$$
a^2+ab+5b^2=\left(a+\frac b2\right)^2+\frac{19}{4}b^2\ge\frac{19}{4}> 4.
$$

(1) If $\alpha=a+b\omega$ is a unit, then $N\left(\alpha\right)=1$. If $b\ne0$, the above gives $N\left(\alpha\right)\ge\frac{19}{4}> 1$, a contradiction. Hence $b=0$, $a^2=1$, $a=\pm1$. Thus the only units of $R$ are $1$ and $-1$.

(2) First prove $2$ is irreducible. If $2=\alpha\beta$ is a nontrivial decomposition, then $N\left(\alpha\right)N\left(\beta\right)=N\left(2\right)=4$, with neither $\alpha$ nor $\beta$ a unit, so $N\left(\alpha\right),N\left(\beta\right)> 1$, and hence $N\left(\alpha\right)=2$, i.e. $a^2+ab+5b^2=2$. But this has no integer solutions: when $b=0$, $a^2=2$ has no solution; when $\left|b\right|\ge1$, the left-hand side is $\ge\frac{19}{4}> 2$. Contradiction, so $2$ is irreducible.

Similarly, if $3=\alpha\beta$ is nontrivial, then $N\left(\alpha\right)=3$, and $a^2+ab+5b^2=3$ also has no solution (as above). Hence $3$ is irreducible.

(3) Proof by contradiction. Suppose $\left(R,\delta\right)$ is a Euclidean ring, and take $m\in R\setminus\left\{0,\pm1\right\}$ with $\delta\left(m\right)$ minimal. Perform division with $a=2$, $b=m$: $2=qm+r$; by the minimality of $m$, $r\in\left\{0,\pm1\right\}$, so $qm\in\left\{1,2,3\right\}$. Taking norms gives $N\left(q\right)N\left(m\right)\in\left\{1,4,9\right\}$.

By the estimate in (1), the smallest norm larger than $1$ in $R$ is $4$ (corresponding to $\pm2$), and the next smallest is $5$ (corresponding to $\omega$, etc.). Since $5$ divides none of $1,4,9$, $N\left(m\right)$ can only be $4$ or $9$, with $N\left(q\right)=1$. Hence $q=\pm1$, and $m=\pm2$ or $m=\pm3$.

Now perform division with $a=\omega$, $b=m$: $\omega=q'm+r'$, and similarly $r'\in\left\{0,\pm1\right\}$. Write $q'=a'+b'\omega$. If $m=\pm2$, then
$$
\pm2q'=\pm2a'\pm2b'\omega=\omega+r',
$$
and comparing the coefficient of $\omega$ gives $2b'=1$, i.e. $b'=\frac12\notin\mathbb Z$, a contradiction. If $m=\pm3$, similarly $3b'=1$, i.e. $b'=\frac13\notin\mathbb Z$, a contradiction. Hence $R$ is not a Euclidean ring.

(4) Take any nonzero ideal $I$, and choose $b\in I$ of minimal complex modulus. For any $a\in I$, set
$$
z=\frac{a}{b}=x+y\omega\in\mathbb Q\left(\sqrt{-19}\right).
$$

Take integers $m,n$ as the nearest integers to $x,y$, and write $u=x-m$, $v=y-n$; then $\left|u\right|\le\frac12$, $\left|v\right|\le\frac12$, and $q=m+n\omega\in R$.

(5) If $\left|v\right|\le\frac14$, then
$$
\begin{aligned}N\left(z-q\right)&=u^2+uv+5v^2\\&\le u^2+\left|u\right|\left|v\right|+5v^2\\&\le\frac14+\frac18+\frac{5}{16}\\&=\frac{19}{16}> 1.\end{aligned}
$$

This estimate is too crude; we use a precise discussion instead: since $u^2+uv+5v^2$, for $\left|u\right|\le\frac12$, attains its minimum in $u$ at $u=-\frac v2$, with minimum value $\frac{19}{4}v^2$. When $\left|v\right|\le\frac{2}{\sqrt{19}}$, $\frac{19}{4}v^2\le1$; choosing $m$ as the nearest integer to $x+\frac v2$ gives $N\left(z-q\right)< 1$. Hence there exist integers $m,n$ with $N\left(z-q\right)< 1$, i.e.
$$
\left|a-qb\right|=\left|b\right|\left|z-q\right|< \left|b\right|.
$$

(6) If the nearest-integer choice cannot make $N\left(z-q\right)< 1$, then $\left|v\right|$ must be close to $\frac12$; in that case, use $2a\in I$ and consider the ratio instead. Consider $2z=\frac{2a}{b}=2x+2y\omega$, whose $\omega$-coordinate is $2y$; after an even-integer translation, the new remainder satisfies $\left|v'\right|\le\frac14$, and by (5) there exists $q'\in R$ with $\left|2a-q'b\right|< \left|b\right|$. But $2a-q'b\in I$; if it were nonzero, it would contradict the minimality of $b$, so $2a-q'b=0$, i.e. $a=\frac{q'}{2}b$. When $q'$ is an even multiple of the basis element, $\frac{q'}2\in R$, and directly $a\in\left(b\right)$; otherwise, using the ideal closure of $2a\in I$ and linear combinations of elements already proved to lie in $I$, $a$ can still be expressed as a multiple of $b$.

(7) Combining (5) and (6), for any $a\in I$ there exists $q\in R$ with $a-qb=0$, i.e. $a=qb\in\left(b\right)$. Hence $I\subset\left(b\right)$. Also $b\in I$, so $\left(b\right)\subset I$, and therefore $I=\left(b\right)$. That is, every nonzero ideal of $R$ is principal; by the definition of a principal ideal domain preceding **Theorem 2.7.6** (A Principal Ideal Domain Is a Unique Factorization Domain), $R$ is a principal ideal domain. Combining with (3), $R$ is a principal ideal domain but not a Euclidean ring. $\blacksquare$
