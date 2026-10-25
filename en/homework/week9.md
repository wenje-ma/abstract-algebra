# Assignment 9

> **Definition 1.9.1** (Group Action) Let $G$ be a group and $X$ a nonempty set. If a map $f:G\times X\to X$ satisfies $f\left(e,x\right)=x$ and
> $$
> f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right),
> $$
> then $f$ determines an action of $G$ on $X$, written $f\left(g,x\right)=gx$.

> **Definition 1.9.7** (Transitive Action and Effective Action) If for any $x,y\in X$ there exists $g\in G$ such that $gx=y$, the action is called transitive, and $X$ is called a homogeneous space of $G$. If $gx=x$ for all $x\in X$ implies $g=e$, the action is called effective.

> **Definition 1.9.9** (Orbit and Isotropy Subgroup) Let $G$ act on $X$ and $x\in X$. The set $Ox=\left\{gx\mid g\in G\right\}$ is called the orbit of $x$. The set $F_x=\left\{g\in G\mid gx=x\right\}$ is called the isotropy subgroup of $x$.

> **Corollary 1.9.15** (Orbit-Isotropy Subgroup Theorem) Let a group $G$ act on $X$ and $x\in X$. Then $\left|Ox\right|=\left[G:F_x\right]$, and hence $\left|Ox\right|$ divides $\left|G\right|$.

> **Lemma 1.9.11** (Conjugacy of Isotropy Subgroups) Let $y=gx\in Ox$. Then $F_y=gF_xg^{-1}$.

### Problem 1

(Problem 1.9-4) (1) Denote by $P^{n-1}\left(\mathbb R\right)$ the set of all $1$-dimensional subspaces of $\mathbb R^n$, called the real projective space. For any $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W\in P^{n-1}\left(\mathbb R\right)$, $\rho\left(W\right)$ is again a $1$-dimensional subspace. Verify that this defines a transitive action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$, and find the isotropy subgroup.

(2) Denote by $\mathrm{Gr}\left(k,n\right)$ the set of all $k$-dimensional subspaces of $\mathbb R^n$, called the Grassmann manifold. For any $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W\in\mathrm{Gr}\left(k,n\right)$, $\rho\left(W\right)$ is again a $k$-dimensional subspace. Verify that this defines a transitive action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $\mathrm{Gr}\left(k,n\right)$, and find the isotropy subgroup.

(3) Consider the actions of $\mathrm{SL}\left(n,\mathbb R\right)$, $O\left(n\right)$ and $\mathrm{SO}\left(n\right)$ on the above sets, and determine their transitivity.

### Solution to Problem 1

(1) Verify the action: for $\rho,\tau\in\mathrm{GL}\left(n,\mathbb R\right)$ and a $1$-dimensional subspace $W=\mathbb Rv$,
$$
\begin{aligned}\rho\left(\tau\left(W\right)\right)&=\rho\left(\tau\left(\mathbb Rv\right)\right)\\&=\mathbb R\rho\tau\left(v\right)\\&=\left(\rho\tau\right)\left(W\right),\end{aligned}
$$
and the identity matrix $I$ satisfies $I\left(W\right)=W$. By **Definition 1.9.1** (Group Action), this is an action.

Transitivity: take any two lines $W_1=\mathbb Rv$ and $W_2=\mathbb Rw$ with $v,w\ne0$. There exists an invertible matrix $\rho$ with $\rho v=w$ (extend $v,w$ to bases and define a linear map), so $\rho\left(W_1\right)=W_2$. By **Definition 1.9.7** (Transitive Action and Effective Action), the action is transitive.

Isotropy subgroup: take $W_0=\mathbb Re_1$, where $e_1=\left(1,0,\cdots,0\right)^{T}$. The condition $\rho\left(W_0\right)=W_0$ is equivalent to $\rho e_1\in\mathbb Re_1$, i.e. the first column of $\rho$ is $\left(a,0,\cdots,0\right)^{T}$ with $a\ne0$. Hence the isotropy subgroup is
$$
F_{W_0}=\left\{\begin{bmatrix}a & *\\0 & A\end{bmatrix}\;\middle|\;a\in\mathbb R^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb R\right)\right\}.
$$

(2) The action is verified similarly: $\rho\left(\tau\left(W\right)\right)=\left(\rho\tau\right)\left(W\right)$.

Transitivity: take any two $k$-dimensional subspaces $W_1,W_2$; take bases $\left\{v_1,\cdots,v_k\right\}$ and $\left\{w_1,\cdots,w_k\right\}$, extend them to bases of $\mathbb R^n$, and define an invertible linear map $\rho$ with $\rho v_i=w_i$; then $\rho\left(W_1\right)=W_2$. Hence the action is transitive.

Isotropy subgroup: take $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$. The condition $\rho\left(W_0\right)=W_0$ is equivalent to the entries of the first $k$ columns of $\rho$ in rows $k+1,\cdots,n$ all being zero, i.e. $\rho$ is block upper-triangular:
$$
F_{W_0}=\left\{\begin{bmatrix}A & B\\0 & C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb R\right),\;C\in\mathrm{GL}\left(n-k,\mathbb R\right),\;B\in\mathbb R^{k\times\left(n-k\right)}\right\}.
$$

(3) The actions of $\mathrm{SL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$ and $\mathrm{Gr}\left(k,n\right)$ are both transitive: in the above proof, if the determinant of the resulting map is not $1$, multiply the last row by a scalar to adjust the determinant to $1$, without changing the image subspace.

$O\left(n\right)$ acts transitively on $P^{n-1}\left(\mathbb R\right)$: $O\left(n\right)$ is transitive on the unit sphere, and hence on lines. $O\left(n\right)$ also acts transitively on $\mathrm{Gr}\left(k,n\right)$: two orthonormal bases can be mapped to each other by an orthogonal map.

$\mathrm{SO}\left(n\right)$ acts transitively on $P^{n-1}\left(\mathbb R\right)$ when $n\ge3$ (any direction can be mapped to any other by a suitable rotation while keeping determinant $1$); it also acts transitively on $\mathrm{Gr}\left(k,n\right)$ when $n\ge3$. $\blacksquare$

### Problem 2

(Problem 1.9-5) Denote by $V_k\left(\mathbb R^n\right)$ the set of all $k$-tuples of orthonormal vectors in $\mathbb R^n$, called the Stiefel manifold. For any $\rho\in O\left(n\right)$ and $\left(\alpha_1,\cdots,\alpha_k\right)\in V_k\left(\mathbb R^n\right)$, define
$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\left(\alpha_1\right),\cdots,\rho\left(\alpha_k\right)\right).
$$
Verify that this defines a transitive action of $O\left(n\right)$ on $V_k\left(\mathbb R^n\right)$, and find the isotropy subgroup.

### Solution to Problem 2

Verify the action: orthogonal transformations preserve inner products, so if $\left(\alpha_1,\cdots,\alpha_k\right)$ is orthonormal, then $\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)$ is also orthonormal. Also,
$$
\rho\left(\tau\left(\alpha_1,\cdots,\alpha_k\right)\right)=\left(\rho\tau\right)\left(\alpha_1,\cdots,\alpha_k\right),
$$
and the identity matrix acts trivially, so this is a group action.

Transitivity: take two orthonormal $k$-tuples $\left(\alpha_1,\cdots,\alpha_k\right)$ and $\left(\beta_1,\cdots,\beta_k\right)$; extend them to orthonormal bases $\left(\alpha_1,\cdots,\alpha_k,\cdots,\alpha_n\right)$ and $\left(\beta_1,\cdots,\beta_k,\cdots,\beta_n\right)$ of $\mathbb R^n$. Define a linear map by $\rho\alpha_i=\beta_i$ ($i=1,\cdots,n$); then $\rho\in O\left(n\right)$ and
$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\beta_1,\cdots,\beta_k\right).
$$
Hence the action is transitive.

Isotropy subgroup: take the standard orthonormal set $\left(e_1,\cdots,e_k\right)$. The condition $\rho\left(e_i\right)=e_i$ ($i=1,\cdots,k$) means that $\rho$ is the identity on the first $k$ standard basis vectors, i.e. $\rho$ is block-diagonal:
$$
F=\left\{\begin{bmatrix}I_k & 0\\0 & A\end{bmatrix}\;\middle|\;A\in O\left(n-k\right)\right\}.
$$
This is the isotropy subgroup of $\left(e_1,\cdots,e_k\right)$. $\blacksquare$

### Problem 3

(Problem 1.9-6) Generalize the actions in the previous two problems to the complex setting.

### Solution to Problem 3

The complex projective space $P^{n-1}\left(\mathbb C\right)$ is the set of all $1$-dimensional complex subspaces of $\mathbb C^n$, and the complex Grassmann manifold $\mathrm{Gr}_{\mathbb C}\left(k,n\right)$ is the set of all $k$-dimensional complex subspaces of $\mathbb C^n$. $\mathrm{GL}\left(n,\mathbb C\right)$ acts on both by $\rho\left(W\right)=\rho W$; the verification is exactly the same as in the real case, and the actions are both transitive.

The isotropy subgroups are respectively
$$
F_{W_0}=\left\{\begin{bmatrix}a & *\\0 & A\end{bmatrix}\;\middle|\;a\in\mathbb C^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb C\right)\right\}
$$
and
$$
F_{W_0}=\left\{\begin{bmatrix}A & B\\0 & C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb C\right),\;C\in\mathrm{GL}\left(n-k,\mathbb C\right),\;B\in\mathbb C^{k\times\left(n-k\right)}\right\}.
$$

The complex Stiefel manifold $V_k\left(\mathbb C^n\right)$ is the set of all $k$-tuples of orthonormal vectors (with respect to the standard Hermitian inner product) in $\mathbb C^n$. $U\left(n\right)$ acts on it by
$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\alpha_1,\cdots,\rho\alpha_k\right),
$$
and unitary transformations preserve the Hermitian inner product, so the action is well defined. The action is transitive: extend two orthonormal $k$-tuples to orthonormal bases, and the corresponding unitary map is the desired element. The isotropy subgroup is
$$
F=\left\{\begin{bmatrix}I_k & 0\\0 & A\end{bmatrix}\;\middle|\;A\in U\left(n-k\right)\right\}.
$$

Moreover, the transitivity of the actions of $\mathrm{SL}\left(n,\mathbb C\right)$, $U\left(n\right)$ and $\mathrm{SU}\left(n\right)$ on the above sets parallels the real case: $\mathrm{SL}\left(n,\mathbb C\right)$ acts transitively on complex projective space and the complex Grassmann manifold; $U\left(n\right)$ acts transitively on complex projective space, the complex Grassmann manifold and the complex Stiefel manifold; $\mathrm{SU}\left(n\right)$ also acts transitively on the corresponding sets when the dimension is sufficiently large. $\blacksquare$

### Problem 4

(Problem 1.9-8) Let
$$
H=\left\{z=x+iy\in\mathbb C\mid y>0\right\},
$$
called the Poincaré upper half-plane. For any
$$
g=\begin{bmatrix}a & b\\c & d\end{bmatrix}\in\mathrm{SL}\left(2,\mathbb R\right),
$$
and $z\in H$, define
$$
g\circ z=\frac{az+b}{cz+d}.
$$
Verify that this defines an action of $\mathrm{SL}\left(2,\mathbb R\right)$ on $H$ (called a Möbius transformation or fractional linear transformation), determine its transitivity and effectiveness, and find the isotropy subgroup of $i$.

### Solution to Problem 4

First verify $g\circ z\in H$. For $z=x+iy$ with $y>0$, a direct computation of the imaginary part gives
$$
\mathrm{Im}\left(\frac{az+b}{cz+d}\right)=\frac{y}{\left|cz+d\right|^{2}}>0,
$$
so $g\circ z\in H$.

Verify the action axioms: the identity matrix $I=\begin{bmatrix}1&0\\0&1\end{bmatrix}$ gives $I\circ z=z$. Also, composition of fractional linear transformations corresponds to matrix multiplication (when the determinant is $1$), i.e. $\left(g_1g_2\right)\circ z=g_1\circ\left(g_2\circ z\right)$. Hence by **Definition 1.9.1** (Group Action), this is an action of $\mathrm{SL}\left(2,\mathbb R\right)$ on $H$.

Transitivity: take any $z=x+iy\in H$ with $y>0$, and take
$$
g=\begin{bmatrix}\sqrt y & x/\sqrt y\\0 & 1/\sqrt y\end{bmatrix},
$$
which has determinant $1$ and satisfies
$$
\begin{aligned}g\circ i&=\frac{\sqrt y\cdot i+x/\sqrt y}{1/\sqrt y}\\&=yi+x\\&=z.\end{aligned}
$$
Hence $i$ can be mapped to any $z\in H$, and the action is transitive.

Effectiveness: if $g\circ z=z$ for all $z\in H$, then the fractional linear transformation $\left(az+b\right)/\left(cz+d\right)$ has infinitely many fixed points, so it must be the identity transformation, i.e. $g=\pm I$. Here $-I=\begin{bmatrix}-1&0\\0&-1\end{bmatrix}$ also satisfies $\left(-I\right)\circ z=z$ for all $z$. Therefore the kernel of the action is $\left\{\pm I\right\}$, and the action is not effective; its effective quotient is
$$
\mathrm{PSL}\left(2,\mathbb R\right)=\mathrm{SL}\left(2,\mathbb R\right)/\left\{\pm I\right\}.
$$

The isotropy subgroup of $i$: from $g\circ i=i$, i.e.
$$
\begin{aligned}\frac{ai+b}{ci+d}=i,\\&\Longrightarrow\;ai+b&=i\left(ci+d\right)\\&=-c+di.\end{aligned}
$$
Comparing real and imaginary parts gives $b=-c$, $a=d$. Also,
$$
\det g=ad-bc=a^{2}+c^{2}=1.
$$
Hence
$$
F_i=\left\{\begin{bmatrix}a & b\\-b & a\end{bmatrix}\;\middle|\;a^{2}+b^{2}=1\right\}\cong SO\left(2\right).
$$
$\blacksquare$

### Problem 5

(Problem 1.9-19) (Fermat's two-square theorem) Let $p=4k+1$ be a prime, and
$$
X=\left\{\left(x,y,z\right)\in\mathbb N^{3}\mid x^{2}+4yz=p\right\}.
$$
Let
$$
p_1:\left(x,y,z\right)\mapsto\left(x,z,y\right),
$$
$$
p_2:\left(x,y,z\right)\mapsto
\begin{cases}
\left(x+2z,\,z,\,y-x-z\right), & x<y-z,\\
\left(2y-x,\,y,\,x-y+z\right), & y-z\le x<2y,\\
\left(x-2y,\,x-y+z,\,y\right), & x\ge 2y.
\end{cases}
$$
Prove that these two maps each define an action of $\mathbb Z_2$ on $X$. Find the number of fixed points of the two actions, and hence prove that when $p=4k+1$, $x^{2}+y^{2}=p$ has positive integer solutions.

### Solution to Problem 5

First verify that $p_1$ defines an action of $\mathbb Z_2$. $p_1$ swaps $y,z$, and clearly $p_1^{2}=\mathrm{id}$. Also,
$$
\begin{aligned}x^{2}+4zy&=x^{2}+4yz\\&=p,\end{aligned}
$$
so $p_1\left(X\right)\subseteq X$. Hence $p_1$ is an involution of order $2$ on $X$, defining the action of $\mathbb Z_2=\left\{1,p_1\right\}$ on $X$.

Now verify $p_2$. Direct substitution shows that in all three pieces, $p_2$ preserves the equation $x^{2}+4yz=p$, and $p_2^{2}=\mathrm{id}$ (the three pieces are mutually inverse maps and agree on the boundaries). Hence $p_2$ is also an involution on $X$, defining another action of $\mathbb Z_2$.

Find the fixed points of $p_2$. In each of the three cases, set $p_2\left(x,y,z\right)=\left(x,y,z\right)$:

Case 1, $x<y-z$: $x+2z=x$ gives $z=0$, contradicting $z\in\mathbb N^{+}$; no fixed points.

Case 2, $y-z\le x<2y$: $2y-x=x$ gives $x=y$; the third coordinate $x-y+z=z$ holds automatically. Substituting into the equation:
$$
\begin{aligned}x^{2}+4xz&=x\left(x+4z\right)\\&=p.\end{aligned}
$$
Since $p$ is prime and both $x$ and $x+4z$ are positive integers, $x=1$ and $x+4z=p$, i.e. $z=\left(p-1\right)/4=k$. The corresponding fixed point is $\left(1,1,k\right)$.

Case 3, $x\ge2y$: $x-2y=x$ gives $y=0$, a contradiction.

Hence $\left|\mathrm{Fix}\left(p_2\right)\right|=1$, exactly one fixed point.

Since every non-fixed orbit of $p_2$ has size $2$,
$$
\left|X\right|\equiv\left|\mathrm{Fix}\left(p_2\right)\right|\equiv1\pmod 2,
$$
i.e. $\left|X\right|$ is odd.

Similarly, the non-fixed orbits of $p_1$ also have size $2$, so
$$
\left|\mathrm{Fix}\left(p_1\right)\right|\equiv\left|X\right|\equiv1\pmod 2.
$$
Therefore $\left|\mathrm{Fix}\left(p_1\right)\right|\ge1$, i.e. $p_1$ has at least one fixed point.

A fixed point of $p_1$ satisfies $y=z$. Substituting into the equation gives
$$
x^{2}+4y^{2}=p,
$$
i.e.
$$
p=x^{2}+\left(2y\right)^{2}.
$$
Let $a=x$, $b=2y$; then $a^{2}+b^{2}=p$, and both $a,b$ are positive integers (since $p$ is an odd prime, $x\ne0$; and $y=z\ge1$, so $b=2y\ge2$).

Hence when $p=4k+1$, $x^{2}+y^{2}=p$ has positive integer solutions. $\blacksquare$

### Problem 6

(Problem 1.9-20) (Burnside's lemma) Let a group $G$ act on a set $X$, and let $t$ denote the number of orbits of $X$ under the action of $G$. For any $g\in G$, let $F\left(g\right)$ denote the number of fixed points of $X$ under $g$, i.e.
$$
F\left(g\right)=\left|\left\{x\in X\mid gx=x\right\}\right|.
$$
Prove that
$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$

### Solution to Problem 6

Consider the set
$$
S=\left\{\left(g,x\right)\in G\times X\mid gx=x\right\}.
$$

Counting by $g$: for fixed $g\in G$, there are exactly $F\left(g\right)$ values of $x$ with $gx=x$, so
$$
\left|S\right|=\sum_{g\in G}F\left(g\right).
$$

Counting by $x$: for fixed $x\in X$, the $g$ satisfying $gx=x$ are precisely the elements of the isotropy subgroup $F_x=\left\{g\in G\mid gx=x\right\}$ of $x$, so
$$
\left|S\right|=\sum_{x\in X}\left|F_x\right|.
$$

By **Corollary 1.9.15** (Orbit-Isotropy Subgroup Theorem), for the orbit $Ox$ containing $x$,
$$
\left|Ox\right|=\left[G:F_x\right]=\left|G\right|/\left|F_x\right|,
$$
i.e. $\left|F_x\right|=\left|G\right|/\left|Ox\right|$.

Decompose $X$ into a disjoint union of orbits. Let $X$ have $t$ orbits $O_1,\cdots,O_t$. For any $x$ in orbit $O_i$, $\left|Ox\right|=\left|O_i\right|$, so $\left|F_x\right|=\left|G\right|/\left|O_i\right|$. Hence
$$
\begin{aligned}\sum_{x\in X}\left|F_x\right|&=\sum_{i=1}^{t}\sum_{x\in O_i}\left|F_x\right|\\&=\sum_{i=1}^{t}\left|O_i\right|\cdot\frac{\left|G\right|}{\left|O_i\right|}\\&=\sum_{i=1}^{t}\left|G\right|\\&=t\left|G\right|.\end{aligned}
$$

Combining the two counting methods gives
$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$
$\blacksquare$
