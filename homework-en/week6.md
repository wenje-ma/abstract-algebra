# week6

> **Lemma 1.7.7**
> 
> Let $A,B$ be subgroups of $G$ with $G=AB$ and $A\cap{B}=\left\{e\right\}$. Then $A$ and $B$ are both normal subgroups of $G$ if and only if $ab=ba$ for all $a\in{A}$ and $b\in{B}$.

> **Lemma 1.8.8 (Heredity of Solvability)**
> 
> Subgroups and quotient groups of a solvable group are solvable; conversely, if $N\trianglelefteq{G}$ and both $N$ and $G/N$ are solvable, then $G$ is solvable.

> **Definition 1.9.1 (Group Action)**
> 
> Let $G$ be a group and $X$ a nonempty set. If a map $f:G\times{X}\to{X}$ satisfies $f\left(e,x\right)=x$ and $f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right)$, then $f$ is said to determine an action of $G$ on $X$, written $f\left(g,x\right)=gx$.

> **Definition 1.9.7 (Transitive and Effective Actions)**
> 
> If for any $x,y\in{X}$ there exists $g\in{G}$ with $gx=y$, the action of $G$ on $X$ is called transitive and $X$ is called a homogeneous space of $G$. If $gx=x$ for all $x\in{X}$ implies $g=e$, the action is called effective. If $gx=x$ for all $g\in{G}$ and $x\in{X}$, the action is called trivial.

> **Definition 1.9.9 (Orbits and Stabilizers)**
> 
> Let $G$ act on $X$ and $x\in{X}$. The set $O_x=\left\{gx\mid{g}\in{G}\right\}$ is called the orbit of $x$. The set $F_x=\left\{g\in{G}\mid{g}x=x\right\}$ is called the stabilizer (isotropy subgroup) of $x$.

> **Corollary 1.9.15 (Orbit-Stabilizer Theorem)**
> 
> Let a group $G$ act on $X$ and $x\in{X}$. Then $\left|O_x\right|=\left|G/F_x\right|=\left[G:F_x\right]$; hence $\left|O_x\right|\mid\left|G\right|$.

> **Theorem 1.10.8 (Sylow's Second Theorem)**
> 
> Let $P$ be a Sylow $p$-subgroup of $G$, and let $H$ be a subgroup of $G$ of order $p^{k}$, $k\le{l}$ (where $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$). Then there exists $g\in{G}$ with $H\subseteq{g}Pg^{-1}$. In particular, the Sylow $p$-subgroups of $G$ are conjugate to one another.

> **Theorem 1.10.10 (Sylow's Third Theorem)**
> 
> Let $n_{p}$ be the number of Sylow $p$-subgroups of $G$. Then (1) a Sylow $p$-subgroup $P$ of $G$ satisfies $P\triangleleft{G}$ if and only if $n_{p}=1$; (2) $n_{p}\mid{m}$ and $n_{p}\equiv1\pmod{p}$, where $\left|G\right|=p^{l}m$, $\left(p,m\right)=1$.

## 1.9-5

Let $V_k\left(\mathbb{R}^n\right)$ denote the set of all ordered $k$-tuples of orthonormal vectors in $\mathbb{R}^n$, called the Stiefel manifold. For any $\rho\in{O}\left(n\right)$ and $\left(\alpha_1,\cdots,\alpha_k\right)\in{V}_k\left(\mathbb{R}^n\right)$, define

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\left(\alpha_1\right),\cdots,\rho\left(\alpha_k\right)\right).
$$

Verify that this is a transitive action of $O\left(n\right)$ on $V_k\left(\mathbb{R}^n\right)$, and find the stabilizer.

### Solution to 1.9-5

Verify the action: By Orthogonal and Unitary Transformations, an orthogonal transformation preserves the inner product, so if $\left(\alpha_1,\cdots,\alpha_k\right)$ is an orthonormal set then $\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)$ is too, i.e. $\rho\left(\alpha_1,\cdots,\alpha_k\right)\in{V}_k\left(\mathbb{R}^n\right)$. Moreover

$$
\rho\left(\tau\left(\alpha_1,\cdots,\alpha_k\right)\right)=\rho\left(\tau\alpha_1,\cdots,\tau\alpha_k\right)=\left(\rho\tau\alpha_1,\cdots,\rho\tau\alpha_k\right)=\left(\rho\tau\right)\left(\alpha_1,\cdots,\alpha_k\right),
$$

and the identity matrix acts trivially. By **Definition 1.9.1 (Group Action)**, this is an action of $O\left(n\right)$ on $V_k\left(\mathbb{R}^n\right)$.

Transitivity: Take two orthonormal sets $\left(\alpha_1,\cdots,\alpha_k\right)$ and $\left(\beta_1,\cdots,\beta_k\right)$. By Orthogonal and Unitary Transformations, extend them to orthonormal bases $\left(\alpha_1,\cdots,\alpha_k,\cdots,\alpha_n\right)$ and $\left(\beta_1,\cdots,\beta_k,\cdots,\beta_n\right)$ of $\mathbb{R}^n$. Define the linear map $\rho\alpha_i=\beta_i$ for $i=1,\cdots,n$; then $\rho\in{O}\left(n\right)$ and

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\beta_1,\cdots,\beta_k\right).
$$

By **Definition 1.9.7 (Transitive and Effective Actions)**, the action is transitive.

Stabilizer: Take the reference tuple $\left(e_1,\cdots,e_k\right)$. The condition $\rho\left(e_i\right)=e_i$ ($i=1,\cdots,k$) means that $\rho$ is the identity on the first $k$ standard basis vectors, i.e. $\rho$ is a block diagonal matrix. By **Definition 1.9.9 (Orbits and Stabilizers)**, the stabilizer is

$$
F=\left\{\begin{bmatrix}I_k&0\\0&A\end{bmatrix}\;\middle|\;A\in{O}\left(n-k\right)\right\}.
$$

This is the stabilizer of $\left(e_1,\cdots,e_k\right)$. $\blacksquare$

## 1.9-6

Extend the actions in Problems 1.9-4 and 1.9-5 to the complex case.

### Solution to 1.9-6

Complex projective space and complex Grassmannian. Let $P^{n-1}\left(\mathbb{C}\right)$ be the set of all $1$-dimensional complex subspaces of $\mathbb{C}^n$, and let $\mathrm{Gr}_{\mathbb{C}}\left(k,n\right)$ be the set of all $k$-dimensional complex subspaces of $\mathbb{C}^n$. $\mathrm{GL}\left(n,\mathbb{C}\right)$ acts on each by $\rho\left(W\right)=\rho{W}$. By Linear Maps Preserve Dimension of Subspaces and the complex analogue of the real argument, by **Definition 1.9.1 (Group Action)** and **Definition 1.9.7 (Transitive and Effective Actions)** these are two transitive actions.

By **Definition 1.9.9 (Orbits and Stabilizers)**, taking $W_0=\mathbb{C}e_1$ and $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$ respectively, the stabilizers are

$$
F_{W_0}=\left\{\begin{bmatrix}a&*\\0&A\end{bmatrix}\;\middle|\;a\in\mathbb{C}^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb{C}\right)\right\}
$$

and

$$
F_{W_0}=\left\{\begin{bmatrix}A&B\\0&C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb{C}\right),\;C\in\mathrm{GL}\left(n-k,\mathbb{C}\right),\;B\in\mathbb{C}^{k\times\left(n-k\right)}\right\}.
$$

Complex Stiefel manifold. Let $V_k\left(\mathbb{C}^n\right)$ be the set of all ordered $k$-tuples of orthonormal vectors in $\mathbb{C}^n$ (with respect to the standard Hermitian inner product). $U\left(n\right)$ acts on it by

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\alpha_1,\cdots,\rho\alpha_k\right).
$$

By Orthogonal and Unitary Transformations, a unitary transformation preserves the Hermitian inner product, so the definition is well-posed; by **Definition 1.9.1 (Group Action)** this is an action. The action is transitive: by Orthogonal and Unitary Transformations, two orthonormal sets are extended to orthonormal bases, and the corresponding unitary map is the required one. By **Definition 1.9.9 (Orbits and Stabilizers)**, taking the reference $\left(e_1,\cdots,e_k\right)$, the stabilizer is

$$
F=\left\{\begin{bmatrix}I_k&0\\0&A\end{bmatrix}\;\middle|\;A\in{U}\left(n-k\right)\right\}.
$$

Transitivity. $\mathrm{SL}\left(n,\mathbb{C}\right)$ acts transitively on the complex projective space and the complex Grassmannian (adjust the determinant as in the real case); $U\left(n\right)$ acts transitively on the complex projective space, the complex Grassmannian and the complex Stiefel manifold; $\mathrm{SU}\left(n\right)$ acts transitively on the corresponding sets when the dimension is large enough. $\blacksquare$

## 1.9-8

Let

$$
H=\left\{z=x+iy\in\mathbb{C}\mid{y}>0\right\},
$$

called the Poincare upper half-plane. For any

$$
g=\begin{bmatrix}a&b\\c&d\end{bmatrix}\in\mathrm{SL}\left(2,\mathbb{R}\right),
$$

and $z\in{H}$, define

$$
g\circ{z}=\frac{az+b}{cz+d}.
$$

Verify that this defines an action of $\mathrm{SL}\left(2,\mathbb{R}\right)$ on $H$ (called a Mobius transformation or fractional linear transformation), determine its transitivity and effectiveness, and find the stabilizer of $i$.

### Solution to 1.9-8

Step 1: verify that $g\circ{z}\in{H}$. For $z=x+iy$ ($y>0$), since $\det{g}=ad-bc=1$, computing the imaginary part directly:

$$
\mathrm{Im}\left(\frac{az+b}{cz+d}\right)=\frac{\left(ad-bc\right)y}{\left|cz+d\right|^{2}}=\frac{y}{\left|cz+d\right|^{2}}>0,
$$

so $g\circ{z}\in{H}$ and the definition is well-posed.

Step 2: verify the action axioms. The identity matrix $I=\begin{bmatrix}1&0\\0&1\end{bmatrix}$ gives $I\circ{z}=z$. By Mobius Transformations, composition of fractional linear transformations corresponds to matrix multiplication, i.e. $\left(g_1g_2\right)\circ{z}=g_1\circ\left(g_2\circ{z}\right)$. By **Definition 1.9.1 (Group Action)**, this is an action of $\mathrm{SL}\left(2,\mathbb{R}\right)$ on $H$.

Step 3: determine transitivity. For any $z=x+iy\in{H}$ ($y>0$), take

$$
g=\begin{bmatrix}\sqrt{y}&x/\sqrt{y}\\0&1/\sqrt{y}\end{bmatrix},
$$

whose determinant is $1$, and

$$
g\circ{i}=\frac{\sqrt{y}\cdot{i}+x/\sqrt{y}}{0\cdot{i}+1/\sqrt{y}}=\left(\sqrt{y}\cdot{i}+\frac{x}{\sqrt{y}}\right)\sqrt{y}=yi+x=z.
$$

Hence $i$ can be mapped to any $z\in{H}$; by **Definition 1.9.7 (Transitive and Effective Actions)**, the action is transitive.

Step 4: determine effectiveness. If $g\circ{z}=z$ for all $z\in{H}$, then the fractional linear transformation $\frac{az+b}{cz+d}$ has infinitely many fixed points; by Mobius Transformations, it must be the identity, so $c=0$, $b=0$, $a=d$; combined with $\det{g}=ad-bc=a^{2}=1$, we get $g=\pm{I}$. Here $-I=\begin{bmatrix}-1&0\\0&-1\end{bmatrix}$ also satisfies $\left(-I\right)\circ{z}=\frac{-z}{-1}=z$ for all $z$. Hence the kernel of the action is $\left\{\pm{I}\right\}$; by **Definition 1.9.7 (Transitive and Effective Actions)**, the action is not effective; its effective quotient group is

$$
\mathrm{PSL}\left(2,\mathbb{R}\right)=\mathrm{SL}\left(2,\mathbb{R}\right)/\left\{\pm{I}\right\}.
$$

Step 5: find the stabilizer of $i$. From $g\circ{i}=i$, i.e.

$$
\frac{ai+b}{ci+d}=i,\quad\Longrightarrow\quad{a}i+b=i\left(ci+d\right)=ci^{2}+di=-c+di.
$$

Comparing real and imaginary parts gives $b=-c$, $a=d$. Also

$$
\det{g}=ad-bc=a^{2}-\left(-c\right)c=a^{2}+c^{2}=1.
$$

By **Definition 1.9.9 (Orbits and Stabilizers)**, the stabilizer of $i$ is

$$
F_i=\left\{\begin{bmatrix}a&b\\-b&a\end{bmatrix}\;\middle|\;a^{2}+b^{2}=1\right\}\cong{S}O\left(2\right).
$$

$\blacksquare$

## 1.9-19

(Fermat's two-squares theorem) Let $p=4k+1$ be a prime,

$$
X=\left\{\left(x,y,z\right)\in\mathbb{N}^{3}\mid{x}^{2}+4yz=p\right\}.
$$

Let

$$
p_1:\left(x,y,z\right)\mapsto\left(x,z,y\right),
$$

$$
p_2:\left(x,y,z\right)\mapsto
\begin{cases}
\left(x+2z,z,y-x-z\right),&x<{}y-z,\\
\left(2y-x,y,x-y+z\right),&y-z\le{x}<2y,\\
\left(x-2y,x-y+z,y\right),&x\ge2y.
\end{cases}
$$

Prove that the two maps above respectively define two actions of $\mathbb{Z}_2$ on $X$. Find the number of fixed points of the two actions, and thereby prove that when $p=4k+1$, the equation $x^{2}+y^{2}=p$ has a solution in positive integers.

### Solution to 1.9-19

First verify that $p_1$ defines an action of $\mathbb{Z}_2$. $p_1$ swaps $y,z$; clearly $p_1^{2}=\mathrm{id}$, and

$$
x^{2}+4zy=x^{2}+4yz=p,
$$

so $p_1\left(X\right)\subseteq{X}$. By **Definition 1.9.1 (Group Action)**, $p_1$ is an involution on $X$, defining an action of $\mathbb{Z}_2=\left\{1,p_1\right\}$ on $X$.

Next verify $p_2$. A direct substitution verifies that in all three branches $p_2$ preserves the equation $x^{2}+4yz=p$, and $p_2^{2}=\mathrm{id}$ (the three branches are mutual inverses and agree on the boundaries). By **Definition 1.9.1 (Group Action)**, $p_2$ is also an involution on $X$, defining another action of $\mathbb{Z}_2$.

Find the fixed points of $p_2$. Setting $p_2\left(x,y,z\right)=\left(x,y,z\right)$ in each of the three cases:

Case one $x<{}y-z$: from $x+2z=x$ we get $z=0$, contradicting $z\in\mathbb{N}^{+}$; no fixed points.

Case two $y-z\le{x}<2y$: from $2y-x=x$ we get $x=y$; the third coordinate $x-y+z=z$ holds automatically. Substituting into the equation:

$$
x^{2}+4yz=x^{2}+4xz=x\left(x+4z\right)=p.
$$

Since $p$ is prime and $x$, $x+4z$ are positive integers, we have $x=1$, $x+4z=p$, i.e. $z=\left(p-1\right)/4=k$. The corresponding fixed point is $\left(1,1,k\right)$.

Case three $x\ge2y$: from $x-2y=x$ we get $y=0$, a contradiction.

Hence $\left|\mathrm{Fix}\left(p_2\right)\right|=1$, exactly one fixed point.

By Orbit Decomposition of a Group Action, every orbit of a non-fixed point of $p_2$ has size $2$, so

$$
\left|X\right|\equiv\left|\mathrm{Fix}\left(p_2\right)\right|\equiv1\pmod2,
$$

i.e. $\left|X\right|$ is odd.

Similarly, every orbit of a non-fixed point of $p_1$ has size $2$, so

$$
\left|\mathrm{Fix}\left(p_1\right)\right|\equiv\left|X\right|\equiv1\pmod2.
$$

Hence $\left|\mathrm{Fix}\left(p_1\right)\right|\ge1$, i.e. $p_1$ has at least one fixed point.

A fixed point of $p_1$ satisfies $y=z$. Substituting into the equation gives

$$
x^{2}+4y^{2}=p,
$$

i.e.

$$
p=x^{2}+\left(2y\right)^{2}.
$$

Set $a=x$, $b=2y$; then $a^{2}+b^{2}=p$, and $a,b$ are positive integers (since $p$ is an odd prime, $x\ne0$; since $y=z\ge1$, $b=2y\ge2$).

Therefore, when $p=4k+1$, the equation $x^{2}+y^{2}=p$ has a solution in positive integers. $\blacksquare$

## 1.9-20

(Burnside's lemma) Let a group $G$ act on a set $X$, and let $t$ denote the number of orbits of $X$ under the action of $G$. For any $g\in{G}$, let $F\left(g\right)$ denote the number of fixed points of $X$ under $g$, i.e.

$$
F\left(g\right)=\left|\left\{x\in{X}\mid{g}x=x\right\}\right|.
$$

Prove that

$$
\sum_{g\in{G}}F\left(g\right)=t\left|G\right|.
$$

### Solution to 1.9-20

Consider the set

$$
S=\left\{\left(g,x\right)\in{G}\times{X}\mid{g}x=x\right\}.
$$

Counting by $g$: For fixed $g\in{G}$, there are exactly $F\left(g\right)$ elements $x$ with $gx=x$, so

$$
\left|S\right|=\sum_{g\in{G}}F\left(g\right).
$$

Counting by $x$: For fixed $x\in{X}$, the elements $g$ with $gx=x$ are exactly the elements of the stabilizer $F_x=\left\{g\in{G}\mid{g}x=x\right\}$, so

$$
\left|S\right|=\sum_{x\in{X}}\left|F_x\right|.
$$

By **Corollary 1.9.15 (Orbit-Stabilizer Theorem)**, for the orbit $O_x$ of $x$,

$$
\left|O_x\right|=\left[G:F_x\right]=\left|G\right|/\left|F_x\right|,
$$

i.e. $\left|F_x\right|=\left|G\right|/\left|O_x\right|$.

Decompose $X$ into the disjoint union of its orbits. Suppose $X$ has $t$ orbits $O_1,\cdots,O_t$. For any $x$ in the orbit $O_i$, $\left|O_x\right|=\left|O_i\right|$, so $\left|F_x\right|=\left|G\right|/\left|O_i\right|$. Hence

$$
\sum_{x\in{X}}\left|F_x\right|=\sum_{i=1}^{t}\sum_{x\in{O}_i}\left|F_x\right|=\sum_{i=1}^{t}\left|O_i\right|\cdot\frac{\left|G\right|}{\left|O_i\right|}=\sum_{i=1}^{t}\left|G\right|=t\left|G\right|.
$$

Combining the two counting methods, we get

$$
\sum_{g\in{G}}F\left(g\right)=t\left|G\right|.
$$

$\blacksquare$

## 1.10-10

Let $\left|G\right|=pq$, where $p,q$ are distinct primes. Prove that $G$ is solvable.

### Solution to 1.10-10

Without loss of generality suppose $p<{}q$. By **Theorem 1.10.10 (Sylow's Third Theorem)**, the number $n_{q}$ of Sylow $q$-subgroups satisfies $n_{q}\mid{p}$ and $n_{q}\equiv1\pmod{q}$. Since $p<{}q$, as a positive divisor of $p$ the number $n_{q}$ is either $1$ or $p$. If $n_{q}=p$, then $p\equiv1\pmod{q}$, i.e. $q\mid{p}-1$; but $p<{}q$ implies $p-1<{}q$, a contradiction. Hence $n_{q}=1$.

Thus the Sylow $q$-subgroup $Q$ of $G$ is unique, and by **Theorem 1.10.10 (Sylow's Third Theorem)** (1), $Q\triangleleft{G}$. Since $\left|Q\right|=q$ is prime, by Solvability of Prime-Order and Cyclic Groups, $Q$ is cyclic and hence solvable. The quotient group $G/Q$ has order $p$, also a cyclic group of prime order, and by Solvability of Prime-Order and Cyclic Groups is also solvable.

By **Lemma 1.8.8 (Heredity of Solvability)**, since both $Q$ and $G/Q$ are solvable, $G$ is solvable. $\blacksquare$

## 1.10-12

(Frattini) Let $N\triangleleft{G}$, and let $P$ be a Sylow subgroup of $N$. Then $G=N_{G}\left(P\right)N$.

### Solution to 1.10-12

Take any $g\in{G}$. Since $N\triangleleft{G}$, the conjugate $gPg^{-1}$ is still a subgroup of $N$; and conjugation preserves order, so by Sylow Subgroups and Element Counting, $\left|gPg^{-1}\right|=\left|P\right|$. Hence $gPg^{-1}$ is also a Sylow $p$-subgroup of $N$.

By **Theorem 1.10.8 (Sylow's Second Theorem)** (applied to the subgroup $N$), any two Sylow $p$-subgroups of $N$ are conjugate in $N$, so there exists $n\in{N}$ with

$$
gPg^{-1}=nPn^{-1}.
$$

Hence

$$
n^{-1}gPg^{-1}n=P,
$$

i.e. $n^{-1}g\in{N}_{G}\left(P\right)$ (it conjugates $P$ back to $P$). Write $h=n^{-1}g\in{N}_{G}\left(P\right)$; then $g=nh$.

Therefore $g\in{N}_{G}\left(P\right)N$. Since $g\in{G}$ was arbitrary, $G=N_{G}\left(P\right)N$. $\blacksquare$

## 1.10-15

Let $p,q$ be primes with $p<{}q$ and $p\nmid\left(q-1\right)$. Prove that a group of order $pq$ is cyclic.

### Solution to 1.10-15

Let $\left|G\right|=pq$. By **Theorem 1.10.10 (Sylow's Third Theorem)**, the number $n_{q}$ of Sylow $q$-subgroups satisfies $n_{q}\mid{p}$ and $n_{q}\equiv1\pmod{q}$. Since $p<{}q$, as shown in Problem 1.10-10, we have $n_{q}=1$. Hence the Sylow $q$-subgroup $Q$ of $G$ is unique; by **Theorem 1.10.10 (Sylow's Third Theorem)** (1), $Q\triangleleft{G}$ and $\left|Q\right|=q$.

Now consider the number $n_{p}$ of Sylow $p$-subgroups. By **Theorem 1.10.10 (Sylow's Third Theorem)**, $n_{p}\mid{q}$ and $n_{p}\equiv1\pmod{p}$. Since $q$ is prime, $n_{p}=1$ or $q$. If $n_{p}=q$, then $q\equiv1\pmod{p}$, i.e. $p\mid\left(q-1\right)$, contradicting the hypothesis $p\nmid\left(q-1\right)$. Hence $n_{p}=1$.

Thus the Sylow $p$-subgroup $P$ of $G$ is also unique, and by **Theorem 1.10.10 (Sylow's Third Theorem)** (1), $P\triangleleft{G}$, $\left|P\right|=p$.

Since $p,q$ are coprime, $P\cap{Q}=\left\{e\right\}$. Also

$$
\left|PQ\right|=\left|P\right|\left|Q\right|/\left|P\cap{Q}\right|=pq=\left|G\right|,
$$

so $G=PQ$.

By **Lemma 1.7.7**, since $P,Q$ are both normal subgroups of $G$ and $P\cap{Q}=\left\{e\right\}$, we have $ab=ba$ for all $a\in{P}$, $b\in{Q}$. Hence the map

$$
P\times{Q}\to{G},\quad\left(a,b\right)\mapsto{a}b
$$

preserves multiplication (because $ab=ba$) and is bijective (injective since $P\cap{Q}=\left\{e\right\}$, surjective since $G=PQ$); therefore it is a group isomorphism, i.e. $G\cong{P}\times{Q}$.

Moreover $P\cong\mathbb{Z}_p$ and $Q\cong\mathbb{Z}_q$, and $p,q$ are coprime, so by Order of Elements in a Direct Product, $\mathbb{Z}_p\times\mathbb{Z}_q\cong\mathbb{Z}_{pq}$; hence

$$
G\cong\mathbb{Z}_p\times\mathbb{Z}_q\cong\mathbb{Z}_{pq},
$$

i.e. $G$ is a cyclic group of order $pq$. $\blacksquare$
