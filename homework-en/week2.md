# week2

> **Definition 1.2.1 (Subgroup)**
> 
> Let $H$ be a nonempty subset of a group $G$. If $H$ forms a group under the operation of $G$, then $H$ is called a subgroup of $G$, denoted $H<{}G$.

> **Theorem 1.2.2 (Subgroup Criterion)**
> 
> Let $H$ be a nonempty subset of a group $G$. Then the following conditions are equivalent: (1) $H$ is a subgroup of $G$; (2) for all $a,b\in{H}$, $ab\in{H}$ and $a^{-1}\in{H}$; (3) for all $a,b\in{H}$, $ab^{-1}\in{H}$.

> **Lemma 1.2.12 (Coset Coincidence Criterion)**
> 
> Let $H$ be a subgroup of a group $G$ and $a,b\in{G}$. Then $aH$ and $bH$ are either disjoint or identical, and $aH=bH$ if and only if $a^{-1}b\in{H}$.

> **Theorem 1.2.22 (Lagrange's Theorem)**
> 
> Let $G$ be a finite group and $H<{}G$. Then $\left|G\right|=\left[G:H\right]\cdot\left|H\right|$, where $\left[G:H\right]$ is the index of $H$ in $G$. Hence the order of the subgroup $H$ is a divisor of the order of the group $G$; in particular, the order of any element is also a divisor of $\left|G\right|$.

> **Corollary 1.2.23 (Multiplicativity of the Index)**
> 
> Let $G$ be a finite group, $K<{}G$, $H<{}K$. Then $\left[G:H\right]=\left[G:K\right]\cdot\left[K:H\right]$.

## 1.2-8

Let $a,b$ be elements of orders $m,n$ respectively in a group $G$, with $ab=ba$.

(1) Prove that the order of $ab$ is $mn$ if $\left(m,n\right)=1$;

(2) Prove that the order of $ab$ is $\left[m,n\right]$ if $\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle=\left\{e\right\}$;

(3) If $\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle\ne\left\{e\right\}$, discuss the order of $ab$. Does $G$ necessarily contain an element of order $\left[m,n\right]$?

### Solution to 1.2-8

(1) Prove that the order of $ab$ is $mn$. By Distribution of Powers in Commutative Groups, since $ab=ba$, we have $\left(ab\right)^{k}=a^{k}b^{k}$ for every integer $k$. Hence

$$
\left(ab\right)^{mn}=a^{mn}b^{mn}=\left(a^{m}\right)^{n}\left(b^{n}\right)^{m}=e,
$$

so by Order of an Element and Generated Subgroup, the order of $ab$ divides $mn$.

Conversely, suppose $\left(ab\right)^{k}=e$. Then by $\left(ab\right)^{k}=a^{k}b^{k}$ we get $a^{k}b^{k}=e$, i.e. $a^{k}=b^{-k}$. The left side $a^{k}\in\left\langle{a}\right\rangle$ and the right side $b^{-k}\in\left\langle{b}\right\rangle$, so $a^{k}\in\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle$. By **Theorem 1.2.22 (Lagrange's Theorem)**, $\left|\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle\right|$ divides both $\left|\left\langle{a}\right\rangle\right|=m$ and $\left|\left\langle{b}\right\rangle\right|=n$, hence divides $\left(m,n\right)=1$; therefore $\left|\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle\right|=1$, i.e. $\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle=\left\{e\right\}$. Hence $a^{k}=b^{-k}\in\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle=\left\{e\right\}$, i.e. $a^{k}=e$ and $b^{k}=e$. By Order of an Element and Generated Subgroup, $m\mid{k}$ and $n\mid{k}$. Since $\left(m,n\right)=1$, by Greatest Common Divisor and Least Common Multiple, $mn\mid{k}$.

In summary, the order of $ab$ divides $mn$ and $mn$ divides the order of $ab$; hence the order of $ab$ is $mn$.

(2) Prove that the order of $ab$ is $\left[m,n\right]$. Write $d=\left[m,n\right]$. By Distribution of Powers in Commutative Groups, $\left(ab\right)^{d}=a^{d}b^{d}$. Since $m\mid{d}$ and $n\mid{d}$, we have $a^{d}=\left(a^{m}\right)^{\frac{d}{m}}=e$ and $b^{d}=\left(b^{n}\right)^{\frac{d}{n}}=e$, so $\left(ab\right)^{d}=e$; by Order of an Element and Generated Subgroup, the order of $ab$ divides $d$.

Conversely, suppose $\left(ab\right)^{k}=e$. Then by $\left(ab\right)^{k}=a^{k}b^{k}$ we get $a^{k}=b^{-k}$. Since $b^{-k}\in\left\langle{b}\right\rangle$ and $a^{k}\in\left\langle{a}\right\rangle$, we have $a^{k}\in\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle=\left\{e\right\}$, i.e. $a^{k}=e$, hence $b^{k}=e$. By Order of an Element and Generated Subgroup, $m\mid{k}$ and $n\mid{k}$, and by Greatest Common Divisor and Least Common Multiple, $\left[m,n\right]\mid{k}$.

In summary, the order of $ab$ divides $d$ and $d$ divides the order of $ab$; hence the order of $ab$ is $\left[m,n\right]$.

(3) Discuss the order of $ab$. When $\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle\ne\left\{e\right\}$, the argument of (2) shows that the order of $ab$ still divides $\left[m,n\right]$, but may be strictly smaller than $\left[m,n\right]$.

Example: take $G=\mathbb{Z}_4\times\mathbb{Z}_4$, $a=\left(1,0\right)$, $b=\left(1,2\right)$. Then both $a,b$ have order $4$, and

$$
\left\langle{a}\right\rangle=\left\{\left(0,0\right),\left(1,0\right),\left(2,0\right),\left(3,0\right)\right\},\quad\left\langle{b}\right\rangle=\left\{\left(0,0\right),\left(1,2\right),\left(2,0\right),\left(3,2\right)\right\},
$$

whose intersection is $\left\langle{a}\right\rangle\cap\left\langle{b}\right\rangle=\left\{\left(0,0\right),\left(2,0\right)\right\}\ne\left\{e\right\}$. Moreover $ab=\left(2,2\right)$ and $2ab=\left(0,0\right)$, so the order of $ab$ is $2<4=\left[4,4\right]$.

As for whether $G$ necessarily contains an element of order $\left[m,n\right]$, the answer is yes. Since $ab=ba$, the subgroup $H=\left\langle{a},b\right\rangle$ is commutative. Let $m=\prod_{p}p^{\alpha_p}$, $n=\prod_{p}p^{\beta_p}$ be the prime factorizations (Prime Factorization and Highest Powers). For each prime $p$: if $\alpha_p\ge\beta_p$, then by Order of a Power of an Element, $a^{m/p^{\alpha_p}}$ has order $\frac{m}{\left(m,m/p^{\alpha_p}\right)}=\frac{m}{m/p^{\alpha_p}}=p^{\alpha_p}$; if $\beta_p>\alpha_p$, then $b^{n/p^{\beta_p}}$ has order $\frac{n}{\left(n,n/p^{\beta_p}\right)}=p^{\beta_p}$. Thus for each $p$ we obtain an element $x_p\in{H}$ of order $p^{\max\left(\alpha_p,\beta_p\right)}$, and for distinct primes $p$ these orders are pairwise coprime. Since $H$ is commutative, these $x_p$ commute pairwise, and applying Order of a Product of Commuting Elements of Coprime Order repeatedly, the product $\prod_px_p$ has order $\prod_pp^{\max\left(\alpha_p,\beta_p\right)}=\left[m,n\right]$. Hence $G$ necessarily contains an element of order $\left[m,n\right]$. $\blacksquare$

## 1.2-13

Let $SL\left(n,\mathbb{Z}\right)$ be the set of all $n\times{n}$ matrices whose entries are integers and whose determinant is $1$.

(1) Prove that $SL\left(n,\mathbb{Z}\right)$ is a subgroup of $GL\left(n,\mathbb{R}\right)$;

(2) Let $S=\begin{bmatrix}0&-1\\1&0\end{bmatrix}$, $T=\begin{bmatrix}1&1\\0&1\end{bmatrix}$, $R=\begin{bmatrix}0&-1\\1&1\end{bmatrix}$, $U=\begin{bmatrix}1&0\\1&1\end{bmatrix}$. Prove that any two of them generate $SL\left(2,\mathbb{Z}\right)$.

### Solution to 1.2-13

(1) Prove that $SL\left(n,\mathbb{Z}\right)<{}GL\left(n,\mathbb{R}\right)$. The identity matrix $I_n$ has integer entries and $\left|I_n\right|=1$, so $SL\left(n,\mathbb{Z}\right)$ is nonempty. For any $A,B\in{S}L\left(n,\mathbb{Z}\right)$, $B$ has integer entries and $\left|B\right|=1$, so by Adjugate Matrices and Determinants of Integer Matrices, all entries of $B^{-1}$ are integers, hence all entries of $AB^{-1}$ are integers. Moreover, by Adjugate Matrices and Determinants of Integer Matrices, $\left|AB^{-1}\right|=\frac{\left|A\right|}{\left|B\right|}=\frac{1}{1}=1$. Hence $AB^{-1}\in{S}L\left(n,\mathbb{Z}\right)$. By **Theorem 1.2.2 (Subgroup Criterion)** (condition (3)), $SL\left(n,\mathbb{Z}\right)<{}GL\left(n,\mathbb{R}\right)$.

(2) Prove that any two of $S,T,R,U$ generate $SL\left(2,\mathbb{Z}\right)$. First verify $S,T,R,U\in{S}L\left(2,\mathbb{Z}\right)$: all entries of each matrix are integers, and direct computation gives $\left|S\right|=\left|T\right|=\left|R\right|=\left|U\right|=1$.

First prove $\left\langle{S},T\right\rangle=SL\left(2,\mathbb{Z}\right)$. For any $A=\begin{bmatrix}a&b\\c&d\end{bmatrix}\in{S}L\left(2,\mathbb{Z}\right)$, by Elementary Row Operations and the Euclidean Algorithm, repeatedly multiplying on the left by $T^{k}$ and $U^{k}$ (i.e. the two kinds of elementary row operations) together with the Euclidean algorithm reduces $A$ to a diagonal matrix; since $\left|A\right|=1$ and elementary row operations do not change the absolute value of the determinant, the diagonal entries of the resulting diagonal matrix are $\pm1$ with product $\pm1$. Since $S^{2}=-I$ expresses $-I$, $A$ can be reduced to the identity $I$ using $S,T$. Conversely, $S,T\in{S}L\left(2,\mathbb{Z}\right)$, so $\left\langle{S},T\right\rangle=SL\left(2,\mathbb{Z}\right)$.

We now prove that the subgroup generated by each of the remaining pairs equals $\left\langle{S},T\right\rangle$.

$\left\langle{S},R\right\rangle$ and $\left\langle{T},R\right\rangle$. Direct computation gives

$$
ST=\begin{bmatrix}0&-1\\1&0\end{bmatrix}\begin{bmatrix}1&1\\0&1\end{bmatrix}=\begin{bmatrix}0&-1\\1&1\end{bmatrix}=R.
$$

Hence $R=ST$, so $R\in\left\langle{S},T\right\rangle$, and $T=S^{-1}R\in\left\langle{S},R\right\rangle$, $S=RT^{-1}\in\left\langle{T},R\right\rangle$. Thus $\left\langle{S},R\right\rangle\supseteq\left\langle{S},T\right\rangle$ and $\left\langle{T},R\right\rangle\supseteq\left\langle{S},T\right\rangle$; since $S,T$ appear in the expressions in terms of $S,R$ (or $T,R$), the reverse inclusions are obvious, so $\left\langle{S},R\right\rangle=\left\langle{T},R\right\rangle=\left\langle{S},T\right\rangle=SL\left(2,\mathbb{Z}\right)$.

$\left\langle{S},U\right\rangle$. Compute $S^{-1}TS$:

$$
S^{-1}TS=\begin{bmatrix}0&1\\-1&0\end{bmatrix}\begin{bmatrix}1&1\\0&1\end{bmatrix}\begin{bmatrix}0&-1\\1&0\end{bmatrix}=\begin{bmatrix}1&0\\-1&1\end{bmatrix}=U^{-1}.
$$

Hence $T=SU^{-1}S^{-1}\in\left\langle{S},U\right\rangle$, so $\left\langle{S},U\right\rangle\supseteq\left\langle{S},T\right\rangle$. Also $U=S^{-1}T^{-1}S\in\left\langle{S},T\right\rangle$, so $\left\langle{S},U\right\rangle\subseteq\left\langle{S},T\right\rangle$. Therefore $\left\langle{S},U\right\rangle=\left\langle{S},T\right\rangle=SL\left(2,\mathbb{Z}\right)$.

$\left\langle{T},U\right\rangle$. $T=\begin{bmatrix}1&1\\0&1\end{bmatrix}$ and $U=\begin{bmatrix}1&0\\1&1\end{bmatrix}$ are precisely the two kinds of elementary transformation matrices in Elementary Row Operations and the Euclidean Algorithm; by the Euclidean algorithm, using only these two kinds of elementary row operations reduces any element of $SL\left(2,\mathbb{Z}\right)$ to $\pm{I}$, so $\left\langle{T},U\right\rangle=SL\left(2,\mathbb{Z}\right)$.

$\left\langle{R},U\right\rangle$. From $R=ST$ we get $T=S^{-1}R$, and $U^{-1}=S^{-1}TS$; substituting gives

$$
U^{-1}=S^{-1}\left(S^{-1}R\right)S=S^{-2}RS.
$$

Since $S^{2}=-I$, we have $S^{-2}=\left(-I\right)^{-1}=-I$, hence $U^{-1}=-IRS=-RS$, i.e. $S=-R^{-1}U^{-1}$. Direct computation gives $R^{3}=\begin{bmatrix}-1&0\\0&-1\end{bmatrix}=-I$, so $-I=R^{3}\in\left\langle{R},U\right\rangle$, and hence

$$
S=\left(-I\right)\left(-S\right)=\left(-I\right)\left(R^{-1}U^{-1}\right)=R^{3}R^{-1}U^{-1}=R^{2}U^{-1}\in\left\langle{R},U\right\rangle.
$$

Then $T=S^{-1}R\in\left\langle{R},U\right\rangle$, so $\left\langle{R},U\right\rangle\supseteq\left\langle{S},T\right\rangle$. Since $R,U\in{S}L\left(2,\mathbb{Z}\right)$, the reverse inclusion $\left\langle{R},U\right\rangle\subseteq\left\langle{S},T\right\rangle$ is obvious. Hence $\left\langle{R},U\right\rangle=\left\langle{S},T\right\rangle=SL\left(2,\mathbb{Z}\right)$.

In summary, any two of $S,T,R,U$ generate $SL\left(2,\mathbb{Z}\right)$. $\blacksquare$
