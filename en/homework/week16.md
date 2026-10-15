# Assignment 16

> **Definition 2.5.6** (Irreducible Elements) Let $R$ be an integral domain and $\alpha\in R^*\setminus U$. If $\alpha$ has no nontrivial factors, then $\alpha$ is called an irreducible element.

> **Definition 2.6.1** (Prime Ideal) Let $I$ be an ideal of a ring $R$ with $I\ne R$. If $ab\in I$ implies $a\in I$ or $b\in I$, then $I$ is called a prime ideal of $R$.

> **Theorem 2.5.15** (Equivalent Conditions for a Unique Factorization Domain) An integral domain $R$ is a unique factorization domain if and only if $R$ satisfies the divisor chain condition and the prime condition, i.e. in a unique factorization domain every irreducible element is prime: $p\mid ab$ implies $p\mid a$ or $p\mid b$.

### Problem 1

(Problem 2.6-13) Let $R$ be a unique factorization domain and $p\in R^*$. Prove that $p$ is irreducible if and only if the principal ideal $\left(p\right)$ is prime.

### Solution to Problem 1

Assume $p\in R^*\setminus U$ (the conclusion is trivial when $p$ is zero or a unit, so we omit those cases).

**Necessity** Suppose $p$ is irreducible. Since $R$ is a unique factorization domain, by **Theorem 2.5.15** (Equivalent Conditions for a Unique Factorization Domain), $p$ is prime, i.e. $p\mid ab$ implies $p\mid a$ or $p\mid b$. Note that $ab\in\left(p\right)$ is equivalent to $p\mid ab$, and $a\in\left(p\right)$ is equivalent to $p\mid a$. Hence $ab\in\left(p\right)$ implies $a\in\left(p\right)$ or $b\in\left(p\right)$. Also $p$ is not a unit, so $1\notin\left(p\right)$, and thus $\left(p\right)\ne R$. By **Definition 2.6.1** (Prime Ideal), $\left(p\right)$ is a prime ideal.

**Sufficiency** Suppose $\left(p\right)$ is a prime ideal. Assume, for contradiction, that $p$ is reducible, i.e. there exist $a,b\in R$, with $a,b$ neither a unit, such that $p=ab$. Since $ab=p\in\left(p\right)$, by **Definition 2.6.1** (Prime Ideal), $a\in\left(p\right)$ or $b\in\left(p\right)$. If $a\in\left(p\right)$, then there exists $r\in R$ with $a=pr$, and thus $p=ab=prb$. Since $R$ is an integral domain and $p\ne0$, cancelling $p$ gives $1=rb$, so $b$ is a unit, a contradiction. If $b\in\left(p\right)$, symmetrically $a$ is a unit, also a contradiction.

Hence $p$ is irreducible. $\blacksquare$
