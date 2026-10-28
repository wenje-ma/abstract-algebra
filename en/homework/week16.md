# week16

> **Basic Knowledge: Principal Ideals and Divisibility**<br>Let $R$ be an integral domain and $p\in R$. Then $a\in\left(p\right)$ if and only if $p\mid a$, i.e. there exists $r\in R$ with $a=pr$.

> **Basic Knowledge: Cancellation in an Integral Domain**<br>An integral domain has no zero divisors; hence if $p\ne0$ and $pa=pb$, then $a=b$.

> **Definition 2.5.6 (Irreducible Element)**<br>Let $R$ be an integral domain and $\alpha\in R^{*}\setminus U$ (i.e. nonzero and not a unit). If $\alpha$ has no nontrivial divisors, then $\alpha$ is called an irreducible element.

> **Theorem 2.5.15 (Equivalent Conditions for a Unique Factorization Domain)**<br>An integral domain $R$ is a unique factorization domain if and only if $R$ satisfies the factor chain condition and the prime condition; in particular, in a unique factorization domain every irreducible element is a prime element, i.e. $p\mid ab$ implies $p\mid a$ or $p\mid b$.

> **Definition 2.6.1 (Prime Ideal)**<br>Let $I$ be an ideal of a ring $R$ with $I\ne R$. If $ab\in I$ implies $a\in I$ or $b\in I$, then $I$ is called a prime ideal of $R$.

---

## 2.6-13

Let $R$ be a unique factorization domain and $p\in R^{*}$. Prove: $p$ is an irreducible element if and only if the principal ideal $\left(p\right)$ is a prime ideal.

### Solution 2.6-13

Suppose $p\in R^{*}\setminus U$ (if $p$ is zero or a unit, the conclusion is trivial and not discussed).

**Necessity**: Suppose $p$ is an irreducible element. Since $R$ is a unique factorization domain, by **Theorem 2.5.15 (Equivalent Conditions for a Unique Factorization Domain)** $p$ is a prime element, i.e. $p\mid ab$ implies $p\mid a$ or $p\mid b$. By **Basic Knowledge: Principal Ideals and Divisibility**, $ab\in\left(p\right)$ is equivalent to $p\mid ab$, $a\in\left(p\right)$ to $p\mid a$, and $b\in\left(p\right)$ to $p\mid b$. Hence $ab\in\left(p\right)$ implies $a\in\left(p\right)$ or $b\in\left(p\right)$. Moreover, since $p$ is not a unit, by **Basic Knowledge: Principal Ideals and Divisibility** $1\notin\left(p\right)$ (otherwise $p\mid1$, making $p$ a unit), so $\left(p\right)\ne R$. By **Definition 2.6.1 (Prime Ideal)**, $\left(p\right)$ is a prime ideal.

**Sufficiency**: Suppose $\left(p\right)$ is a prime ideal. Assume, toward contradiction, that $p$ is reducible, i.e. there exist $a,b\in R$, both non-units, with $p=ab$. Since $ab=p\in\left(p\right)$, by **Definition 2.6.1 (Prime Ideal)** we have $a\in\left(p\right)$ or $b\in\left(p\right)$. If $a\in\left(p\right)$, by **Basic Knowledge: Principal Ideals and Divisibility** there exists $r\in R$ with $a=pr$; then $p=ab=prb$. Since $p\ne0$ (as $p\in R^{*}$) and $R$ is an integral domain, by **Basic Knowledge: Cancellation in an Integral Domain** we cancel $p$ to get $1=rb$, so $b$ is a unit, contradicting that $b$ is not a unit. If $b\in\left(p\right)$, similarly there exists $r\in R$ with $b=pr$, hence $p=ab=apr$; canceling $p$ gives $1=ar$, so $a$ is a unit, also a contradiction.

Hence $p$ is an irreducible element. $\blacksquare$
