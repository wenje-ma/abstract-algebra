# Assignment 9

> **Definition 1.9.1** (Group Action) Let $G$ be a group and $X$ a nonempty set. If a map $f:G\times X\to X$ satisfies $f\left(e,x\right)=x$ and
> $$
> f\left(g_1g_2,x\right)=f\left(g_1,f\left(g_2,x\right)\right),
> $$
> then $f$ determines an action of $G$ on $X$, written $f\left(g,x\right)=gx$.

> **Definition 1.9.7** (Transitive Action and Effective Action) If for any $x,y\in X$ there exists $g\in G$ such that $gx=y$, the action is called transitive, and $X$ is called a homogeneous space of $G$. If $gx=x$ for all $x\in X$ implies $g=e$, the action is called effective.

> **Definition 1.9.9** (Orbit and Isotropy Subgroup) Let $G$ act on $X$ and $x\in X$. The set $Ox=\left\{gx\mid g\in G\right\}$ is called the orbit of $x$. The set $F_x=\left\{g\in G\mid gx=x\right\}$ is called the isotropy subgroup of $x$.

> **Corollary 1.9.15** (Orbit–Isotropy Subgroup Theorem) Let a group $G$ act on $X$ and $x\in X$. Then $\left|Ox\right|=\left[G:F_x\right]$, and hence $\left|Ox\right|$ divides $\left|G\right|$.

> **Lemma 1.9.11** (Conjugacy of Isotropy Subgroups) Let $y=gx\in Ox$. Then $F_y=gF_xg^{-1}$.

### Problem 1

(Problem 1.9-4) (1) Denote by $\mathbb R^n$ the set of all $1$-dimensional subspaces of $P^{n-1}\left(\mathbb R\right)$, called the real projective space. For any $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W\in P^{n-1}\left(\mathbb R\right)$, $\rho\left(W\right)$ is again a $1$-dimensional subspace. Verify that this defines a transitive action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$, and find the isotropy subgroup.

(2) Denote by $\mathbb R^n$ the set of all $k$-dimensional subspaces of $\mathrm{Gr}\left(k,n\right)$, called the Grassmann manifold. For any $\rho\in\mathrm{GL}\left(n,\mathbb R\right)$ and $W\in\mathrm{Gr}\left(k,n\right)$, $\rho\left(W\right)$ is again a $k$-dimensional subspace. Verify that this defines a transitive action of $\mathrm{GL}\left(n,\mathbb R\right)$ on $\mathrm{Gr}\left(k,n\right)$, and find the isotropy subgroup.

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
F_{W_0}=\left\{\begin{pmatrix}a & *\0 & A\end{pmatrix}\;\middle|\;a\in\mathbb R^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb R\right)\right\}.
$$

(2) The action is verified similarly: $\rho\left(\tau\left(W\right)\right)=\left(\rho\tau\right)\left(W\right)$.

Transitivity: take any two $k$-dimensional subspaces $W_1,W_2$; take bases $\left\{v_1,\cdots,v_k\right\}$ and $\left\{w_1,\cdots,w_k\right\}$, extend them to bases of $\mathbb R^n$, and define an invertible linear map $\rho$ with $\rho v_i=w_i$; then $\rho\left(W_1\right)=W_2$. Hence the action is transitive.

Isotropy subgroup: take $W_0=\mathrm{span}\left(e_1,\cdots,e_k\right)$. The condition $\rho\left(W_0\right)=W_0$ is equivalent to the entries of the first $\rho$ columns of $k$ in rows $k+1,\cdots,n$ all being zero, i.e. $\rho$ is block upper-triangular:
$$
F_{W_0}=\left\{\begin{pmatrix}A & B\0 & C\end{pmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb R\right),\;C\in\mathrm{GL}\left(n-k,\mathbb R\right),\;B\in\mathbb R^{k\times\left(n-k\right)}\right\}.
$$

(3) The actions of $\mathrm{SL}\left(n,\mathbb R\right)$ on $P^{n-1}\left(\mathbb R\right)$ and $\mathrm{Gr}\left(k,n\right)$ are both transitive: in the above proof, if the determinant of the resulting map is not $1$, multiply the last row by a scalar to adjust the determinant to $1$, without changing the image subspace.

$O\left(n\right)$ acts transitively on $P^{n-1}\left(\mathbb R\right)$: $O\left(n\right)$ is transitive on the unit sphere, and hence on lines. $O\left(n\right)$ also acts transitively on $\mathrm{Gr}\left(k,n\right)$: two orthonormal bases can be mapped to each other by an orthogonal map.

$\mathrm{SO}\left(n\right)$ acts transitively on $P^{n-1}\left(\mathbb R\right)$ when $n\ge3$ (any direction can be mapped to any other by a suitable rotation while keeping determinant $1$); it also acts transitively on $\mathrm{Gr}\left(k,n\right)$ when $n\ge3$. $\blacksquare$

### Problem 2

(Problem 1.9-5) Denote by $V_k\left(\mathbb R^n\right)$ the set of all $\mathbb R^n$-tuple orthonormal vectors in $k$, called the Stiefel manifold. For any $\rho\in O\left(n\right)$ and $\left(\alpha_1,\cdots,\alpha_k\right)\in V_k\left(\mathbb R^n\right)$, define
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

Transitivity: take two orthonormal $\left(\alpha_1,\cdots,\alpha_k\right)$-tuples $\left(\beta_1,\cdots,\beta_k\right)$ and $\mathbb R^n$; extend them to orthonormal bases $\left(\alpha_1,\cdots,\alpha_k,\cdots,\alpha_n\right)$ and $\left(\beta_1,\cdots,\beta_k,\cdots,\beta_n\right)$ of $\rho\alpha_i=\beta_i$. Define a linear map by $i=1,\cdots,n$ ($\rho\in O\left(n\right)$); then 

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\beta_1,\cdots,\beta_k\right).
$$

 and

 $\left(e_1,\cdots,e_k\right)$Hence the action is transitive.$\rho\left(e_i\right)=e_i$. The conditions $i=1,\cdots,k$ ($\rho$) mean that $k$ is the identity on the first $\rho$ standard basis vectors, i.e. 
$$
F=\left\{\begin{pmatrix}I_k & 0\0 & A\end{pmatrix}\;\middle|\;A\in O\left(n-k\right)\right\}.
$$
 is block-diagonal:$\left(e_1,\cdots,e_k\right)$This is the isotropy subgroup of $\blacksquare$

. 

 $4$### Problem 3$5$ is the set of all 

 

 $P^{n-1}\left(\mathbb C\right)$-dimensional complex subspaces of $\mathbb C^n$, and the complex Grassmann manifold $1$ is the set of all $\mathrm{Gr}_{\mathbb C}\left(k,n\right)$-dimensional complex subspaces of $\mathbb C^n$. $k$ acts on both by $\mathrm{GL}\left(n,\mathbb C\right)$; the verification is exactly the same as in the real case, and the actions are both transitive.$\rho\left(W\right)=\rho W$and

 
$$
F_{W_0}=\left\{\begin{pmatrix}a & *\0 & A\end{pmatrix}\;\middle|\;a\in\mathbb C^{*},\;A\in\mathrm{GL}\left(n-1,\mathbb C\right)\right\}
$$
The complex Stiefel manifold 
$$
F_{W_0}=\left\{\begin{pmatrix}A & B\0 & C\end{pmatrix}\;\middle|\;A\in\mathrm{GL}\left(k,\mathbb C\right),\;C\in\mathrm{GL}\left(n-k,\mathbb C\right),\;B\in\mathbb C^{k\times\left(n-k\right)}\right\}.
$$

 is the set of all $V_k\left(\mathbb C^n\right)$-tuple orthonormal vectors (with respect to the standard Hermitian inner product) in $\mathbb C^n$. $k$ acts on it by$U\left(n\right)$and unitary transformations preserve the Hermitian inner product, so the action is well defined. The action is transitive: extend two orthonormal 

$$
\rho\left(\alpha_1,\cdots,\alpha_k\right)=\left(\rho\alpha_1,\cdots,\rho\alpha_k\right)
$$

-tuples to orthonormal bases, and the corresponding unitary map is the desired element. The isotropy subgroup is
$$
F=\left\{\begin{pmatrix}I_k & 0\0 & A\end{pmatrix}\;\middle|\;A\in U\left(n-k\right)\right\}.
$$

Moreover, the transitivity of the actions of $\mathrm{SL}\left(n,\mathbb C\right)$, $U\left(n\right)$ and $\mathrm{SU}\left(n\right)$ on the above sets parallels the real case: $\mathrm{SL}\left(n,\mathbb C\right)$ acts transitively on complex projective space and the complex Grassmann manifold; $U\left(n\right)$ acts transitively on complex projective space, the complex Grassmann manifold and the complex Stiefel manifold; $\mathrm{SU}\left(n\right)$ also acts transitively on the corresponding sets when the dimension is sufficiently large. $\blacksquare$

### Problem 4

(Problem 1.9-8) Let
$$
H=\left\{z=x+iy\in\mathbb C\mid y>0\right\},
$$
called the Poincaré upper half-plane. For any

$$
g=\begin{pmatrix}a & b\c & d\end{pmatrix}\in\mathrm{SL}\left(2,\mathbb R\right),
$$

$z\in H$, define
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

Verify the action axioms: the identity matrix $I=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ gives $I\circ z=z$. Also, composition of fractional linear transformations corresponds to matrix multiplication (when the determinant is $1$), i.e. $\left(g_1g_2\right)\circ z=g_1\circ\left(g_2\circ z\right)$. Hence by **Definition 1.9.1** (Group Action), this is an action of $\mathrm{SL}\left(2,\mathbb R\right)$ on $H$.

Transitivity: take any $z=x+iy\in H$ with $y>0$, and take
$$
g=\begin{pmatrix}\sqrt y & x/\sqrt y\0 & 1/\sqrt y\end{pmatrix},
$$
which has determinant $1$ and satisfies
$$
\begin{aligned}g\circ i&=\frac{\sqrt y\cdot i+x/\sqrt y}{1/\sqrt y}\\&=yi+x\\&=z.\end{aligned}
$$
Hence $i$ can be mapped to any $z\in H$, and the action is transitive.

Effectiveness: if $g\circ z=z$ for all $z\in H$, then the fractional linear transformation $\left(az+b\right)/\left(cz+d\right)$ has infinitely many fixed points, so it must be the identity transformation, i.e. $g=\pm I$. Here $-I=\begin{pmatrix}-1&0\\0&-1\end{pmatrix}$ also satisfies $z$ for all $\left(-I\right)\circ z=z$. Therefore the kernel of the action is $\left\{\pm I\right\}$, and the action is not effective; its effective quotient is

$$
\mathrm{PSL}\left(2,\mathbb R\right)=\mathrm{SL}\left(2,\mathbb R\right)/\left\{\pm I\right\}.
$$

$i$: from $g\circ i=i$, i.e.
$$
\begin{aligned}\frac{ai+b}{ci+d}=i,\\&\Longrightarrow\;ai+b&=i\left(ci+d\right)\\&=-c+di.\end{aligned}
$$
Comparing real and imaginary parts gives $b=-c$, $a=d$. Also,

$$
\det g=ad-bc=a^{2}+c^{2}=1.
$$

Hence
$$
F_i=\left\{\begin{pmatrix}a & b\-b & a\end{pmatrix}\;\middle|\;a^{2}+b^{2}=1\right\}\cong SO\left(2\right).
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
so $p_1\left(X\right)\subseteq X$. Hence $p_1$ is an involution of order $X$ on $\mathbb Z_2=\left\{1,p_1\right\}$, defining the action of $X$ on 

 $p_2$.$p_2$. Direct substitution shows that in all three pieces, $x^{2}+4yz=p$ preserves the equation $p_2^{2}=\mathrm{id}$, and $p_2$ (the three pieces are mutually inverse maps and agree on the boundaries). Hence $X$ is also an involution on $\mathbb Z_2$, defining another action of 

 $p_2$.$p_2\left(x,y,z\right)=\left(x,y,z\right)$. In each of the three cases, set 

 $x<y-z$:$x+2z=x$. $z=0$ gives $z\in\mathbb N^{+}$, contradicting 

 $y-z\le x<2y$; no fixed points.$2y-x=x$. $x=y$ gives $x-y+z=z$; the third coordinate 
$$
\begin{aligned}x^{2}+4xz&=x\left(x+4z\right)\\&=p.\end{aligned}
$$
 holds automatically. Substituting into the equation:$p$Since $x,x+4z$ is prime and both $x=1$ and $x+4z=p$ are positive integers, $z=\left(p-1\right)/4=k$ and $\left(1,1,k\right)$, i.e. 

 $x\ge2y$. The corresponding fixed point is $x-2y=x$.$y=0$. 

 $\left|\mathrm{Fix}\left(p_2\right)\right|=1$ gives 

 $p_2$, a contradiction.$2$, exactly one fixed point.
$$
\left|X\right|\equiv\left|\mathrm{Fix}\left(p_2\right)\right|\equiv1\pmod 2,
$$
 has size $\left|X\right|$,

 $p_1$i.e. $2$ is odd.
$$
\left|\mathrm{Fix}\left(p_1\right)\right|\equiv\left|X\right|\equiv1\pmod 2.
$$
 also has size $\left|\mathrm{Fix}\left(p_1\right)\right|\ge1$, so$p_1$Therefore 

$p_1$, i.e. $y=z$ has at least one fixed point.
$$
x^{2}+4y^{2}=p,
$$
 satisfies 
$$
p=x^{2}+\left(2y\right)^{2}.
$$
. Substituting into the equation gives$a=x$i.e.$b=2y$Let $a^{2}+b^{2}=p$ and $a,b$; then $p$, and both $x\ne0$ are positive integers (since $y=z\ge1$ is an odd prime, $b=2y\ge2$; 

 $p=4k+1$ so $x^{2}+y^{2}=p$).$\blacksquare$

, 

 $G$ has positive integer solutions. $X$### Problem 6$t$ act on a set $X$, and let $G$ denote the number of orbits of $g\in G$ under the action of $F\left(g\right)$. For any $X$, let $g$ denote the number of fixed points of 

$$
F\left(g\right)=\left|\left\{x\in X\mid gx=x\right\}\right|.
$$

 under the action of 
$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$

, i.e.

 
$$
S=\left\{\left(g,x\right)\in G\times X\mid gx=x\right\}.
$$

Prove that$g$### Solution to Problem 6$g\in G$Counting by $gx=x$: for fixed $x$, there are exactly $F\left(g\right)$ values of 
$$
\left|S\right|=\sum_{g\in G}F\left(g\right).
$$

 with $x$, so$x\in X$Counting by $gx=x$: for fixed $g$, the $x$ satisfying $F_x=\left\{g\in G\mid gx=x\right\}$ are precisely the elements of the isotropy subgroup 
$$
\left|S\right|=\sum_{x\in X}\left|F_x\right|.
$$

 of $x$, so$Ox$By **Corollary 1.9.15** (Orbit–Isotropy Subgroup Theorem), for the orbit 

$$
\left|Ox\right|=\left[G:F_x\right]=\left|G\right|/\left|F_x\right|,
$$
 containing $\left|F_x\right|=\left|G\right|/\left|Ox\right|$,
 $X$i.e. $X$.$t$ into a disjoint union of orbits. Let $O_1,\cdots,O_t$ have $O_i$ orbits $x$. For any $\left|Ox\right|=\left|O_i\right|$ in orbit $\left|F_x\right|=\left|G\right|/\left|O_i\right|$, 
$$
\begin{aligned}\sum_{x\in X}\left|F_x\right|&=\sum_{i=1}^{t}\sum_{x\in O_i}\left|F_x\right|\\&=\sum_{i=1}^{t}\left|O_i\right|\cdot\frac{\left|G\right|}{\left|O_i\right|}\\&=\sum_{i=1}^{t}\left|G\right|\\&=t\left|G\right|.\end{aligned}
$$
, so 
$$
\sum_{g\in G}F\left(g\right)=t\left|G\right|.
$$
$\blacksquare$
