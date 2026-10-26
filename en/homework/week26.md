# Assignment 26

> **Basic Knowledge** (Frobenius Map in Characteristic $p$) Let a field $F$ have prime characteristic $p$. Then for any $a,b\in F$, $\left(a+b\right)^p=a^p+b^p$. Hence for any $c\in F$, if $\alpha$ is a root of $x^p-c$ in some splitting field (i.e. $\alpha^p=c$), then $x^p-c=\left(x-\alpha\right)^p$; that is, $x^p-c$ has only one root, of multiplicity $p$, in its splitting field.

### Problem 1

(Problem 4.4-5) Let $F$ be a field, $c\in F$, and $\mathrm{char}\,F=p\ne0$. Prove that $x^p-c$ is irreducible in $F\left[x\right]$ if and only if $x^p-c$ has no root in $F$.

### Solution to Problem 1

**Necessity.** Suppose $x^p-c$ has a root $\alpha$ in $F$, i.e. $\alpha^p=c$ with $\alpha\in F$. By **Basic Knowledge** (Frobenius Map in Characteristic $p$),

$$
x^p-c=x^p-\alpha^p=\left(x-\alpha\right)^p.
$$

Since $p\geqslant2$, this gives a nontrivial decomposition of $x^p-c$ in $F\left[x\right]$, so $x^p-c$ is reducible. Hence the contrapositive holds: irreducibility implies that $x^p-c$ has no root in $F$.

**Sufficiency.** Suppose, for contradiction, that $x^p-c$ has no root in $F$ but is reducible in $F\left[x\right]$; i.e. there exist nonconstant monic polynomials $f\left(x\right),g\left(x\right)\in F\left[x\right]$ such that $x^p-c=f\left(x\right)g\left(x\right)$, where $1\leq\deg f=k< p$.

Let $E$ be a splitting field of $x^p-c$, and let $\alpha\in E$ be a root of it. By **Basic Knowledge** (Frobenius Map in Characteristic $p$), in $E\left[x\right]$ we have $x^p-c=\left(x-\alpha\right)^p$. Since $f$ is monic, comparing the decompositions gives $f\left(x\right)=\left(x-\alpha\right)^k$.

In $f\left(x\right)=\left(x-\alpha\right)^k$, the coefficient of $x^{k-1}$ is $-k\alpha$. Since $f\in F\left[x\right]$, this coefficient lies in $F$, so $k\alpha\in F$. Also $1\leq k< p$, and in a field of characteristic $p$, $k\ne0$, so $k$ is invertible in $F$; hence $\alpha=\left(k\alpha\right)\cdot k^{-1}\in F$.

Thus $\alpha^p=c$, i.e. $\alpha$ is a root of $x^p-c$ in $F$, contradicting the assumption. Hence when $x^p-c$ has no root in $F$, it must be irreducible.

In summary, $x^p-c$ is irreducible in $F\left[x\right]$ if and only if it has no root in $F$. $\blacksquare$
