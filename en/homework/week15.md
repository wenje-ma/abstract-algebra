# week15

> **Basic Knowledge: The Norm on the Ring $\mathbb Z\left[\sqrt{-5}\right]$**<br>For $x+y\sqrt{-5}\in\mathbb Z\left[\sqrt{-5}\right]$, define $N\left(x+y\sqrt{-5}\right)=x^{2}+5y^{2}$. Then $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$, and $\xi$ is a unit if and only if $N\left(\xi\right)=1$; $N$ takes nonnegative integer values, and there is no element of norm $3$ (the equation $x^{2}+5y^{2}=3$ has no integer solution).

> **Basic Knowledge: The Norm on the Ring of Integers $\mathbb Z\left[\omega\right]$**<br>Let $\omega=\frac{1+\sqrt{-3}}{2}$. Then $\omega^{2}=\omega-1$, $\overline\omega=\frac{1-\sqrt{-3}}{2}$, and $\mathbb Z\left[\omega\right]=\left\{m+n\omega\mid m,n\in\mathbb Z\right\}$. Define $N\left(m+n\omega\right)=\left(m+n\omega\right)\left(m+n\overline\omega\right)=m^{2}+mn+n^{2}$; then $N\left(\xi\eta\right)=N\left(\xi\right)N\left(\eta\right)$, and $\xi$ is a unit if and only if $N\left(\xi\right)=1$.

> **Basic Knowledge: Polynomial Rings over a Field Are Unique Factorization Domains**<br>Polynomial rings in one or several variables over a field are unique factorization domains; in $\mathbb Q\left[x,y\right]$, the elements $x$ and $y$ are non-associate irreducible elements (its units are exactly the nonzero constants).

> **Definition 2.5.2 (Associates)**<br>Let $R$ be an integral domain and $a,b\in R$. If there exists a unit $u$ in $R$ such that $a=ub$, then $a$ and $b$ are called associates, written $a\sim b$.

> **Definition 2.5.6 (Irreducible Element)**<br>Let $R$ be an integral domain and $\alpha\in R^{*}\setminus U$ (i.e. nonzero and not a unit). If $\alpha$ has no nontrivial divisors, then $\alpha$ is called an irreducible element; otherwise $\alpha$ is called a reducible element.

> **Definition 2.5.14 (Common Divisors and Greatest Common Divisors)**<br>Let $R$ be an integral domain and $a_1,a_2,\cdots,a_n\in R$. If $c\in R$ divides every $a_i$, then $c$ is called a common divisor of them; if a common divisor $d$ is divisible by every common divisor, then $d$ is called a greatest common divisor. If the greatest common divisor of $a,b$ is a unit, then $a,b$ are called coprime.

---

## 2.5-8

Let $R=\mathbb Z\left[\sqrt{-5}\right]$.

(1) Prove: if $a^{2}+5b^{2}=9$, then $a+b\sqrt{-5}$ is an irreducible element;

(2) Prove: the elements $\alpha=6+3\sqrt{-5}$, $\beta=9$ have no greatest common divisor in $R$.

### Solution 2.5-8

By **Basic Knowledge: The Norm on the Ring $\mathbb Z\left[\sqrt{-5}\right]$**, define the norm on $R$ by $N\left(x+y\sqrt{-5}\right)=x^{2}+5y^{2}$; then $N$ is multiplicative and $\xi$ is a unit if and only if $N\left(\xi\right)=1$.

**Part (1).** Let $\gamma=a+b\sqrt{-5}$; then $N\left(\gamma\right)=a^{2}+5b^{2}=9\ne1$, so $\gamma$ is not a unit, i.e. $\gamma\in R^{*}\setminus U$. Suppose, toward contradiction, that $\gamma=\xi\eta$ is a nontrivial factorization (with both $\xi,\eta$ non-units). Then

$$
N\left(\xi\right)N\left(\eta\right)=N\left(\gamma\right)=9.
$$

By **Basic Knowledge: The Norm on the Ring $\mathbb Z\left[\sqrt{-5}\right]$**, $N$ takes nonnegative integer values and there is no element of norm $3$. Hence $N\left(\xi\right),N\left(\eta\right)$ can only be $1$ or $9$: if $N\left(\xi\right)=1$ then $\xi$ is a unit, and if $N\left(\xi\right)=9$ then $N\left(\eta\right)=1$, so $\eta$ is a unit. In either case, one factor of $\gamma$ is a unit, contradicting that $\gamma=\xi\eta$ is nontrivial. Hence $\gamma$ has no nontrivial divisor, so by **Definition 2.5.6 (Irreducible Element)** $\gamma$ is irreducible.

**Part (2).** First factor:

$$
\beta=9=\left(2+\sqrt{-5}\right)\left(2-\sqrt{-5}\right),
$$

$$
\alpha=6+3\sqrt{-5}=3\left(2+\sqrt{-5}\right).
$$

Here $N\left(3\right)=9$ and $N\left(2+\sqrt{-5}\right)=N\left(2-\sqrt{-5}\right)=9$, so by Part (1) the elements $3$, $2+\sqrt{-5}$, $2-\sqrt{-5}$ are all irreducible.

Both $3$ and $2+\sqrt{-5}$ divide $\alpha$ and $\beta$ ($9=3\cdot3$, and $2+\sqrt{-5}$ divides both), so both are common divisors.

**$2-\sqrt{-5}$ does not divide $\alpha$**: if there were $\gamma\in R$ with $\gamma\left(2-\sqrt{-5}\right)=\alpha=3\left(2+\sqrt{-5}\right)$, multiplying both sides by $2+\sqrt{-5}$ and using $\left(2+\sqrt{-5}\right)\left(2-\sqrt{-5}\right)=9$ gives

$$
\gamma\cdot9=3\left(2+\sqrt{-5}\right)^{2}=3\left(-1+4\sqrt{-5}\right),
$$

so $\gamma=\left(-1+4\sqrt{-5}\right)/3=-\frac{1}{3}+\frac{4}{3}\sqrt{-5}\notin R$, a contradiction.

**$3$ and $2+\sqrt{-5}$ do not divide each other**: $3\nmid\left(2+\sqrt{-5}\right)$ (otherwise $\left(2+\sqrt{-5}\right)/3\notin R$); and $\left(2+\sqrt{-5}\right)\nmid3$, since otherwise $3/\left(2+\sqrt{-5}\right)=\left(2-\sqrt{-5}\right)/3\notin R$.

Suppose $d$ is a greatest common divisor of $\alpha,\beta$. By **Definition 2.5.14 (Common Divisors and Greatest Common Divisors)**, every common divisor divides $d$; in particular $3\mid d$ and $\left(2+\sqrt{-5}\right)\mid d$. Also $d\mid\beta=9$, and the divisors of $9$ up to associates are only $1,3,2+\sqrt{-5},2-\sqrt{-5},9$ (by Part (1), the divisors of norm $9$ are only $3,2\pm\sqrt{-5}$, and there is no element of norm $3$). Checking each: $d=1$ is not divisible by $3$; $d=3$ is not divisible by $2+\sqrt{-5}$; $d=2+\sqrt{-5}$ is not divisible by $3$; $d=2-\sqrt{-5}$ does not divide $\alpha$ (as shown); $d=9$ does not divide $\alpha$ (otherwise $\alpha/9=\left(2+\sqrt{-5}\right)/3\notin R$). All contradict the simultaneous requirements $3\mid d$, $\left(2+\sqrt{-5}\right)\mid d$, $d\mid\alpha$.

Hence $\alpha,\beta$ have no greatest common divisor in $R$. $\blacksquare$

---

## 2.5-10

Let $R=\mathbb Z\left[\omega\right]$, where $\omega=\frac{1+\sqrt{-3}}{2}$ (the ring of algebraic integers of $\mathbb Q\left(\sqrt{-3}\right)$).

(1) Prove that $R$ is an integral domain under the usual addition and multiplication of numbers;

(2) Prove that all units of $R$ are $\pm1$, $\frac{\pm1\pm\sqrt{-3}}{2}$;

(3) Prove that in $R$ the elements $2$ and $1+\sqrt{-3}$ are associates.

### Solution 2.5-10

By **Basic Knowledge: The Norm on the Ring of Integers $\mathbb Z\left[\omega\right]$**, $\omega^{2}=\omega-1$, so

$$
R=\mathbb Z\left[\omega\right]=\left\{m+n\omega\mid m,n\in\mathbb Z\right\}
$$

is closed under multiplication ($\omega^{2}=\omega-1\in R$).

**Part (1).** $R\subseteq\mathbb C$. $R$ is closed under addition (componentwise), closed under multiplication, and contains the identity $1$. Since $\mathbb C$ has no zero divisors, $R$ is a commutative unital ring without zero divisors, hence an integral domain.

**Part (2).** By **Basic Knowledge: The Norm on the Ring of Integers $\mathbb Z\left[\omega\right]$**, define

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

**Part (3).** Since $1+\sqrt{-3}=2\omega$ and $\omega$ is a unit ($N\left(\omega\right)=1$), i.e. $1+\sqrt{-3}=2\cdot\omega$ with $\omega$ a unit, by **Definition 2.5.2 (Associates)** the elements $2$ and $1+\sqrt{-3}$ are associates. $\blacksquare$

---

## 2.5-15

It is known that $\mathbb Q\left[x,y\right]$ is a ring under polynomial addition and multiplication. Prove that $x$ and $y$ are coprime. Is there $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ such that $r\left(x,y\right)x+s\left(x,y\right)y=1$?

### Solution 2.5-15

By **Basic Knowledge: Polynomial Rings over a Field Are Unique Factorization Domains**, $\mathbb Q\left[x,y\right]$ is a unique factorization domain, and $x,y$ are both irreducible elements. They are non-associate: their units are exactly the nonzero constants in $\mathbb Q^{*}$, and $x\ne cy$ for any $c\in\mathbb Q^{*}$. Hence the common divisors of $x,y$ are only units, so their greatest common divisor is a unit; by **Definition 2.5.14 (Common Divisors and Greatest Common Divisors)**, $x$ and $y$ are coprime.

But no such $r,s$ exist. Suppose, toward contradiction, that $r\left(x,y\right),s\left(x,y\right)\in\mathbb Q\left[x,y\right]$ satisfy $r\left(x,y\right)x+s\left(x,y\right)y=1$. Evaluating both sides at $\left(0,0\right)$:

$$
r\left(0,0\right)\cdot0+s\left(0,0\right)\cdot0=1,
$$

i.e. $0=1$, a contradiction.

Hence, although $x$ and $y$ are coprime, there do not exist $r,s\in\mathbb Q\left[x,y\right]$ with $rx+sy=1$. $\blacksquare$
