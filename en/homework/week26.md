# Assignment 26

> **Basic Knowledge** (Frobenius Map in Characteristic $p$) Let a field $F$ have prime characteristic $p$. Then for any $a,b\in F$, $\left(a+b\right)^p=a^p+b^p$. Hence for any $c\in F$, if $\alpha$ is a root of $x^p-c$ in some splitting field (i.e. $\alpha^p=c$), then $x^p-c=\left(x-\alpha\right)^p$; that is, $x^p-c$ has only one root of multiplicity $p$ in its splitting field.

### Problem 1

(Problem 4.4-5) Let $F$ be a field, $c\in F$, and $\mathrm{char}\,F=p\ne0$. Prove that $x^p-c$ is irreducible in $F\left[x\right]$ if and only if $x^p-c$ has no root in $F$.

### Solution to Problem 1

**Necessity** Suppose $x^p-c$ has a root $F$ in $\alpha$, i.e. $\alpha^p=c$ with $\alpha\in F$. By **Basic Knowledge** (Frobenius Map in Characteristic $p$),

$$
\begin{aligned}x^p-c&=x^p-\alpha^p\\&=\left(x-\alpha\right)^p.\end{aligned}
$$

Since $p\geqslant2$, this gives a nontrivial decomposition of $x^p-c$ in $F\left[x\right]$, so $x^p-c$ is reducible. Hence the contrapositive holds: irreducible implies that $x^p-c$ has no root in $F$.

**Sufficiency** Suppose, for contradiction, that $x^p-c$ has no root in $F$ but is reducible in $x^p-c$, i.e. there exist nonconstant monic polynomials $F\left[x\right]$ with $f\left(x\right),g\left(x\right)\in F\left[x\right]$, where $x^p-c=f\left(x\right)g\left(x\right)$.$1\leq\deg f=k<p$ be a splitting field of 

 $E$, and let $x^p-c$ be a root. By **Basic Knowledge** (Frobenius Map in Characteristic $\alpha\in E$), in $p$ we have $E\left[x\right]$. Since $x^p-c=\left(x-\alpha\right)^p$ is monic, comparing decompositions gives $f$.$f\left(x\right)=\left(x-\alpha\right)^k$, the coefficient of 

$f\left(x\right)=\left(x-\alpha\right)^k$ is $x^{k-1}$. Since $-k\alpha$, this coefficient lies in $f\in F\left[x\right]$, so $F$. Also $k\alpha\in F$, and in a field of characteristic $1\leq k<p$, $p$, so $k\ne0$ is invertible in $k$; hence $F$.$\alpha=\left(k\alpha\right)\cdot k^{-1}\in F$, i.e. 

 $\alpha^p=c$ is a root of $\alpha$ in $x^p-c$, contradicting the assumption. Hence when $F$ has no root in $x^p-c$, it must be irreducible.$F$ is irreducible in 

 $x^p-c$ if and only if it has no root in $F\left[x\right]$. $F$ $\blacksquare$
