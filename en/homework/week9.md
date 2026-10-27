# week9

> **Basic Knowledge: Linear Maps Preserve Dimension of Subspaces**<br>An invertible linear transformation maps a $k$-dimensional subspace to a $k$-dimensional subspace; for any two nonzero vectors $v,w$, there exists an invertible linear transformation $\rho$ with $\rho v=w$ (extend $v,w$ to bases of $\mathbb R^n$ and define the linear map).

> **Basic Knowledge: Orthogonal and Unitary Transformations**<br>An orthogonal transformation preserves the inner product, hence maps orthonormal sets to orthonormal sets and $k$-dimensional subspaces to $k$-dimensional subspaces; any two orthonormal bases can be related by an orthogonal (unitary) transformation.

> **Basic Knowledge: Mobius Transformations**<br>The composition of Mobius transformations (fractional linear transformations) $z\mapsto\frac{az+b}{cz+d}$ corresponds to matrix multiplication; a Mobius transformation with infinitely many fixed points must be the identity.

> **Basic Knowledge: Orbit Decomposition of a Group Action**<br>Let $G$ act on $X$. Then $X$ is the disjoint union of its orbits; for $x\in X$, the orbit $O_x$ has size $\left|G\right|/\left|F_x\right|$, where $F_x$ is the stabilizer (isotropy subgroup) of $x$. In particular, when $\mathbb Z_2$ acts on $X$, every orbit of a non-fixed point has exactly $2$ elements, so $\left|X\right|\equiv\left|\mathrm{Fix}\right|\pmod 2$, where $\mathrm{Fix}$ is the set of fixed points.

> **Definition 1.9.1 (Group Action)**<br>Let $G$ be a group and $X$ a nonempty set. If a map $f:G\times X\to X$ satisfies $f\left(e,x\right)=x$ and $f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right)$, then $f$ is said to determine an action of $G$ on $X$, written $f\left(g,x\right)=gx$.

> **Definition 1.9.7 (Transitive and Effective Actions)**<br>If for any $x,y\in X$ there exists $g\in G$ with $gx=y$, the action of $G$ on $X$ is called transitive and $X$ is called a homogeneous space of $G$. If $gx=x$ for all $x\in X$ implies $g=e$, the action is called effective. If $gx=x$ for all $g\in G$ and $x\in X$, the action is called trivial.

> **Definition 1.9.9 (Orbits and Stabilizers)**<br>Let $G$ act on $X$ and $x\in X$. The set $O_x=\left\{gx\mid g\in G\right\}$ is called the orbit of $x$. The set $F_x=\left\{g\in G\mid gx=x\right\}$ is called the stabilizer (isotropy subgroup) of $x$.

> **Corollary 1.9.15 (Orbit-Stabilizer Theorem)**<br>Let a group $G$ act on $X$ and $x\in X$. Then $\left|O_x\right|=\left|G/F_x\right|=\left[G:F_x\right]$; hence $\left|O_x\right|\mid\left|G\right|$.

---

## 1.9-4

(1) Let $P^{n-1}\left(\mathbb R\right)$ denote the set of all $1$-dimensional subspaces of $\mathbb R^n$, called the real projective space. For any $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W\in P^{n-1}\left(\mathbb R\right)$, $\rho\left(W\right)$ is again a $1$-dimensional subspace. Verify that this is a transitive action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$, and find the stabilizer.

(2) Let $\mathrm{Gr}\left(k,n\right)$ denote the set of all $k$-dimensional subspaces of $\mathbb R^n$, called the Grassmannian. For any $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W\in\mathrm{Gr}\left(k,n\right)$, $\rho\left(W\right)$ is again a $k$-dimensional subspace. Verify that this is a transitive action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $\mathrm{Gr}\left(k,n\right)$, and find the stabilizer.

(3) Consider the actions of $\mathrm{SL}\left(n,\mathbb R\right)$, $O\left(n\right)$, $\mathrm{SO}\left(n\right)$ on the above sets and determine their transitivity.

### Solution 1.9-4

**Part (1): the action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$.** By **Basic Knowledge: Linear Maps Preserve Dimension of Subspaces**, for $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and a $1$-dimensional subspace $W=\mathbb Rv$, $\rho\left(W\right)$ is again a $1$-dimensional subspace. For $\rho,\tau\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W=\mathbb Rv$,

$$
\rho\left(\tau\left(W\right)\right)=\rho\left(\tau\left(\mathbb Rv\right)\right)=\rho\left(\mathbb R\tau\left(v\right)\right)=\mathbb R\rho\left(\tau\left(v\right)\right)=\left(\rho\tau\right)\left(W\right),
$$

and the identity matrix $I$ satisfies $I\left(W\right)=W$. By **Definition 1.9.1 (Group Action)**, this is an action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$.

**Transitivity**: Take any two lines $W_1=\mathbb Rv$, $W_2=\mathbb Rw$ ($v,w\ne0$). By **Basic Knowledge: Linear Maps Preserve Dimension of Subspaces**, there exists an invertible matrix $\rho$ with $\rho v=w$, so $\rho\left(W_1\right)=W_2$. By **Definition 1.9.7 (Transitive and Effective Actions)**, the action is transitive.

**Stabilizer**: Take $W_0=\mathbb Re_1$, where $e_1=\left(1,0,\cdots,0\right)^{\top}$. The condition $\rho\left(W_0\right)=W_0$ is equivalent to $\rho e_1\in\mathbb Re_1$, i.e. the first column of $\rho$ is $\left(a,0,\cdots,0\right)^{\top}$ with $a\ne0$. Hence by **Definition 1.9.9 (Orbits and Stabilizers)**, the stabilizer of $W_0$ is

$$
F_{W_0}=\left\{\begin{bmatrix}a & *\\0 & A\end{bmatrix}\;\middle|\;a\in\mathbb R^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb R\right)\right\}.
$$

**Part (2): the action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $\mathrm{Gr}\left(k,n\right)$.** Similarly $\rho\left(\tau\left(W\right)\right)=\left(\rho\tau\right)\left(W\right)$ and $I\left(W\right)=W$, so by **Definition 1.9.1 (Group Action)** this is an action.

**Transitivity**: Take two $k$-dimensional subspaces $W_1,W_2$ with bases $\left\{v_1,\cdots,v_k\right\}$ and $\left\{w_1,\cdots,w_k\right\}$; extend them to bases of $\mathbb R^n$. By **Basic Knowledge: Linear Maps Preserve Dimension of Subspaces**, define an invertible linear map $\rho$ with $\rho v_i=w_i$ ($i=1,\cdots,k$); then $\rho\left(W_1\right)=W_2$. By **Definition 1.9.7 (Transitive and Effective Actions)**, the action is transitive.

**Stabilizer**: Take $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$. The condition $\rho\left(W_0\right)=W_0$ is equivalent to $\rho$ mapping each $e_i$ ($i\le k$) back into $W_0$, i.e. the first $k$ columns of $\rho$ have zero entries in rows $k+1,\cdots,n$, namely $\rho$ is a block upper triangular matrix. Hence by **Definition 1.9.9 (Orbits and Stabilizers)**, the stabilizer is

$$
F_{W_0}=\left\{\begin{bmatrix}A & B\\0 & C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb R\right),\;C\in\mathrm{GL}\left(n-k,\mathbb R\right),\;B\in\mathbb R^{k\times\left(n-k\right)}\right\}.
$$

**Part (3): determine transitivity.** The action of $\mathrm{SL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$ and on $\mathrm{Gr}\left(k,n\right)$ is transitive: in the map $\rho$ constructed in Parts (1)(2), if its determinant is not $1$, multiply the last row by a nonzero scalar to adjust the determinant to $1$, without changing the action on subspaces.

$O\left(n\right)$ acts transitively on $P^{n-1}\left(\mathbb R\right)$: by **Basic Knowledge: Orthogonal and Unitary Transformations**, any two unit lines can be related by an orthogonal transformation. $O\left(n\right)$ also acts transitively on $\mathrm{Gr}\left(k,n\right)$: bases of two $k$-dimensional subspaces can be extended to two orthonormal bases, which are related by an orthogonal map by **Basic Knowledge: Orthogonal and Unitary Transformations**.

$\mathrm{SO}\left(n\right)$ acts transitively on $P^{n-1}\left(\mathbb R\right)$ when $n\ge3$ (by a suitable rotation one can send any direction to any direction while keeping determinant $1$); it also acts transitively on $\mathrm{Gr}\left(k,n\right)$ when $n\ge3$. $\blacksquare$

---

## 1.9-5

Let $V_k\left(\mathbb R^n\right)$ denote the set of all ordered $k$-tuples of orthonormal vectors in $\mathbb R^n$, called the Stiefel manifold. For any $\rho\in O\left(n\right)$ and $\left(\alpha_1,\cdots,\alpha_k\right)\in V_k\left(\mathbb R^n\right)$, define

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\left(\alpha_1\right),\cdots,\rho\left(\alpha_k\right)\right).
$$

Verify that this is a transitive action of $O\left(n\right)$ on $V_k\left(\mathbb R^n\right)$, and find the stabilizer.

### Solution 1.9-5

**Verify the action**: By **Basic Knowledge: Orthogonal and Unitary Transformations**, an orthogonal transformation preserves the inner product, so if $\left(\alpha_1,\cdots,\alpha_k\right)$ is an orthonormal set then $\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)$ is too, i.e. $\rho\left(\alpha_1,\cdots,\alpha_k\right)\in V_k\left(\mathbb R^n\right)$. Moreover

$$
\rho\left(\tau\left(\alpha_1,\cdots,\alpha_k\right)\right)=\rho\left(\tau\alpha_1,\cdots,\tau\alpha_k\right)=\left(\rho\tau\alpha_1,\cdots,\rho\tau\alpha_k\right)=\left(\rho\tau\right)\left(\alpha_1,\cdots,\alpha_k\right),
$$

and the identity matrix acts trivially. By **Definition 1.9.1 (Group Action)**, this is an action of $O\left(n\right)$ on $V_k\left(\mathbb R^n\right)$.

**Transitivity**: Take two orthonormal sets $\left(\alpha_1,\cdots,\alpha_k\right)$ and $\left(\beta_1,\cdots,\beta_k\right)$. By **Basic Knowledge: Orthogonal and Unitary Transformations**, extend them to orthonormal bases $\left(\alpha_1,\cdots,\alpha_k,\cdots,\alpha_n\right)$ and $\left(\beta_1,\cdots,\beta_k,\cdots,\beta_n\right)$ of $\mathbb R^n$. Define the linear map $\rho\alpha_i=\beta_i$ for $i=1,\cdots,n$; then $\rho\in O\left(n\right)$ and

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\beta_1,\cdots,\beta_k\right).
$$

By **Definition 1.9.7 (Transitive and Effective Actions)**, the action is transitive.

**Stabilizer**: Take the reference tuple $\left(e_1,\cdots,e_k\right)$. The condition $\rho\left(e_i\right)=e_i$ ($i=1,\cdots,k$) means that $\rho$ is the identity on the first $k$ standard basis vectors, i.e. $\rho$ is a block diagonal matrix. By **Definition 1.9.9 (Orbits and Stabilizers)**, the stabilizer is

$$
F=\left\{\begin{bmatrix}I_k & 0\\0 & A\end{bmatrix}\;\middle|\;A\in O\left(n-k\right)\right\}.
$$

This is the stabilizer of $\left(e_1,\cdots,e_k\right)$. $\blacksquare$

---

## 1.9-6

Extend the actions in Problems 1.9-4 and 1.9-5 to the complex case.

### Solution 1.9-6

**Complex projective space and complex Grassmannian.** Let $P^{n-1}\left(\mathbb C\right)$ be the set of all $1$-dimensional complex subspaces of $\mathbb C^n$, and let $\mathrm{Gr}_{\mathbb C}\left(k,n\right)$ be the set of all $k$-dimensional complex subspaces of $\mathbb C^n$. $\mathrm{GL}\left(n,\mathbb C\right)$ acts on each by $\rho\left(W\right)=\rho W$. By **Basic Knowledge: Linear Maps Preserve Dimension of Subspaces** and the complex analogue of the real argument, by **Definition 1.9.1 (Group Action)** and **Definition 1.9.7 (Transitive and Effective Actions)** these are two transitive actions.

By **Definition 1.9.9 (Orbits and Stabilizers)**, taking $W_0=\mathbb Ce_1$ and $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$ respectively, the stabilizers are

$$
F_{W_0}=\left\{\begin{bmatrix}a & *\\0 & A\end{bmatrix}\;\middle|\;a\in\mathbb C^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb C\right)\right\}
$$

and

$$
F_{W_0}=\left\{\begin{bmatrix}A & B\\0 & C\end{bmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb C\right),\;C\in\mathrm{GL}\left(n-k,\mathbb C\right),\;B\in\mathbb C^{k\times\left(n-k\right)}\right\}.
$$

**Complex Stiefel manifold.** Let $V_k\left(\mathbb C^n\right)$ be the set of all ordered $k$-tuples of orthonormal vectors in $\mathbb C^n$ (with respect to the standard Hermitian inner product). $U\left(n\right)$ acts on it by

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\alpha_1,\cdots,\rho\alpha_k\right).
$$

By **Basic Knowledge: Orthogonal and Unitary Transformations**, a unitary transformation preserves the Hermitian inner product, so the definition is well-posed; by **Definition 1.9.1 (Group Action)** this is an action. The action is transitive: by **Basic Knowledge: Orthogonal and Unitary Transformations**, two orthonormal sets are extended to orthonormal bases, and the corresponding unitary map is the required one. By **Definition 1.9.9 (Orbits and Stabilizers)**, taking the reference $\left(e_1,\cdots,e_k\right)$, the stabilizer is

$$
F=\left\{\begin{bmatrix}I_k & 0\\0 & A\end{bmatrix}\;\middle|\;A\in U\left(n-k\right)\right\}.
$$

**Transitivity**. $\mathrm{SL}\left(n,\mathbb C\right)$ acts transitively on the complex projective space and the complex Grassmannian (adjust the determinant as in the real case); $U\left(n\right)$ acts transitively on the complex projective space, the complex Grassmannian and the complex Stiefel manifold; $\mathrm{SU}\left(n\right)$ acts transitively on the corresponding sets when the dimension is large enough. $\blacksquare$

---

## 1.9-8

Let

$$
H=\left\{z=x+iy\in\mathbb C\mid y>0\right\},
$$

called the Poincare upper half-plane. For any

$$
g=\begin{bmatrix}a & b\\c & d\end{bmatrix}\in\mathrm{SL}\left(2,\mathbb R\right),
$$

and $z\in H$, define

$$
g\circ z=\frac{az+b}{cz+d}.
$$

Verify that this defines an action of $\mathrm{SL}\left(2,\mathbb R\right)$ on $H$ (called a Mobius transformation or fractional linear transformation), determine its transitivity and effectiveness, and find the stabilizer of $i$.

### Solution 1.9-8

**Step 1: verify that $g\circ z\in H$.** For $z=x+iy$ ($y>0$), since $\det g=ad-bc=1$, computing the imaginary part directly:

$$
\mathrm{Im}\left(\frac{az+b}{cz+d}\right)=\frac{\left(ad-bc\right)y}{\left|cz+d\right|^{2}}=\frac{y}{\left|cz+d\right|^{2}}>0,
$$

so $g\circ z\in H$ and the definition is well-posed.

**Step 2: verify the action axioms.** The identity matrix $I=\begin{bmatrix}1&0\\0&1\end{bmatrix}$ gives $I\circ z=z$. By **Basic Knowledge: Mobius Transformations**, composition of fractional linear transformations corresponds to matrix multiplication, i.e. $\left(g_1g_2\right)\circ z=g_1\circ\left(g_2\circ z\right)$. By **Definition 1.9.1 (Group Action)**, this is an action of $\mathrm{SL}\left(2,\mathbb R\right)$ on $H$.

**Step 3: determine transitivity.** For any $z=x+iy\in H$ ($y>0$), take

$$
g=\begin{bmatrix}\sqrt y & x/\sqrt y\\0 & 1/\sqrt y\end{bmatrix},
$$

whose determinant is $1$, and

$$
g\circ i=\frac{\sqrt y\cdot i+x/\sqrt y}{0\cdot i+1/\sqrt y}=\left(\sqrt y\cdot i+\frac{x}{\sqrt y}\right)\sqrt y=yi+x=z.
$$

Hence $i$ can be mapped to any $z\in H$; by **Definition 1.9.7 (Transitive and Effective Actions)**, the action is transitive.

**Step 4: determine effectiveness.** If $g\circ z=z$ for all $z\in H$, then the fractional linear transformation $\frac{az+b}{cz+d}$ has infinitely many fixed points; by **Basic Knowledge: Mobius Transformations**, it must be the identity, so $c=0$, $b=0$, $a=d$; combined with $\det g=ad-bc=a^{2}=1$, we get $g=\pm I$. Here $-I=\begin{bmatrix}-1&0\\0&-1\end{bmatrix}$ also satisfies $\left(-I\right)\circ z=\frac{-z}{-1}=z$ for all $z$. Hence the kernel of the action is $\left\{\pm I\right\}$; by **Definition 1.9.7 (Transitive and Effective Actions)**, the action is not effective; its effective quotient group is

$$
\mathrm{PSL}\left(2,\mathbb R\right)=\mathrm{SL}\left(2,\mathbb R\right)/\left\{\pm I\right\}.
$$

**Step 5: find the stabilizer of $i$.** From $g\circ i=i$, i.e.

$$
\frac{ai+b}{ci+d}=i,\quad\Longrightarrow\quad ai+b=i\left(ci+d\right)=ci^{2}+di=-c+di.
$$

Comparing real and imaginary parts gives $b=-c$, $a=d$. Also

$$
\det g=ad-bc=a^{2}-\left(-c\right)c=a^{2}+c^{2}=1.
$$

By **Definition 1.9.9 (Orbits and Stabilizers)**, the stabilizer of $i$ is

$$
F_i=\left\{\begin{bmatrix}a & b\\-b & a\end{bmatrix}\;\middle|\;a^{2}+b^{2}=1\right\}\cong SO\left(2\right).
$$

$\blacksquare$

---

## 1.9-19

(Fermat's two-squares theorem) Let $p=4k+1$ be a prime,

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
\left(x-2y,\,x-y+z,\,y\right), & x\ge2y.
\end{cases}
$$

Prove that the two maps above respectively define two actions of $\mathbb Z_2$ on $X$. Find the number of fixed points of the two actions, and thereby prove that when $p=4k+1$, the equation $x^{2}+y^{2}=p$ has a solution in positive integers.

### Solution 1.9-19

**First verify that $p_1$ defines an action of $\mathbb Z_2$.** $p_1$ swaps $y,z$; clearly $p_1^{2}=\mathrm{id}$, and

$$
x^{2}+4zy=x^{2}+4yz=p,
$$

so $p_1\left(X\right)\subseteq X$. By **Definition 1.9.1 (Group Action)**, $p_1$ is an involution on $X$, defining an action of $\mathbb Z_2=\left\{1,p_1\right\}$ on $X$.

**Next verify $p_2$.** A direct substitution verifies that in all three branches $p_2$ preserves the equation $x^{2}+4yz=p$, and $p_2^{2}=\mathrm{id}$ (the three branches are mutual inverses and agree on the boundaries). By **Definition 1.9.1 (Group Action)**, $p_2$ is also an involution on $X$, defining another action of $\mathbb Z_2$.

**Find the fixed points of $p_2$.** Setting $p_2\left(x,y,z\right)=\left(x,y,z\right)$ in each of the three cases:

Case one $x<y-z$: from $x+2z=x$ we get $z=0$, contradicting $z\in\mathbb N^{+}$; no fixed points.

Case two $y-z\le x<2y$: from $2y-x=x$ we get $x=y$; the third coordinate $x-y+z=z$ holds automatically. Substituting into the equation:

$$
x^{2}+4yz=x^{2}+4xz=x\left(x+4z\right)=p.
$$

Since $p$ is prime and $x$, $x+4z$ are positive integers, we have $x=1$, $x+4z=p$, i.e. $z=\left(p-1\right)/4=k$. The corresponding fixed point is $\left(1,1,k\right)$.

Case three $x\ge2y$: from $x-2y=x$ we get $y=0$, a contradiction.

Hence $\left|\mathrm{Fix}\left(p_2\right)\right|=1$, exactly one fixed point.

By **Basic Knowledge: Orbit Decomposition of a Group Action**, every orbit of a non-fixed point of $p_2$ has size $2$, so

$$
\left|X\right|\equiv\left|\mathrm{Fix}\left(p_2\right)\right|\equiv1\pmod 2,
$$

i.e. $\left|X\right|$ is odd.

Similarly, every orbit of a non-fixed point of $p_1$ has size $2$, so

$$
\left|\mathrm{Fix}\left(p_1\right)\right|\equiv\left|X\right|\equiv1\pmod 2.
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

---

## 1.9-20

(Burnside's lemma) Let a group $G$ act on a set $X$, and let $t$ denote the number of orbits of $X$ under the action of $G$. For any $g\in G$, let $F\left(g\right)$ denote the number of fixed points of $X$ under $g$, i.e.

$$
F\left(g\right)=\left|\left\{x\in X\mid gx=x\right\}\right|.
$$

Prove that

$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$

### Solution 1.9-20

Consider the set

$$
S=\left\{\left(g,x\right)\in G\times X\mid gx=x\right\}.
$$

**Counting by $g$**: For fixed $g\in G$, there are exactly $F\left(g\right)$ elements $x$ with $gx=x$, so

$$
\left|S\right|=\sum_{g\in G}F\left(g\right).
$$

**Counting by $x$**: For fixed $x\in X$, the elements $g$ with $gx=x$ are exactly the elements of the stabilizer $F_x=\left\{g\in G\mid gx=x\right\}$, so

$$
\left|S\right|=\sum_{x\in X}\left|F_x\right|.
$$

By **Corollary 1.9.15 (Orbit-Stabilizer Theorem)**, for the orbit $O_x$ of $x$,

$$
\left|O_x\right|=\left[G:F_x\right]=\left|G\right|/\left|F_x\right|,
$$

i.e. $\left|F_x\right|=\left|G\right|/\left|O_x\right|$.

Decompose $X$ into the disjoint union of its orbits. Suppose $X$ has $t$ orbits $O_1,\cdots,O_t$. For any $x$ in the orbit $O_i$, $\left|O_x\right|=\left|O_i\right|$, so $\left|F_x\right|=\left|G\right|/\left|O_i\right|$. Hence

$$
\sum_{x\in X}\left|F_x\right|=\sum_{i=1}^{t}\sum_{x\in O_i}\left|F_x\right|=\sum_{i=1}^{t}\left|O_i\right|\cdot\frac{\left|G\right|}{\left|O_i\right|}=\sum_{i=1}^{t}\left|G\right|=t\left|G\right|.
$$

Combining the two counting methods, we get

$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$

$\blacksquare$
