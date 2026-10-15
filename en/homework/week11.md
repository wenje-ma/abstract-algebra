# Assignment 11

> **Definition 2.1.1** (Ring) Let $R$ be a nonempty set on which two binary operations $R$ and $+$ are defined, satisfying:$\cdot$ is an abelian group;
> (2) $\left[R;+\right]$ is a semigroup (multiplication is associative);
> (3) multiplication is left and right distributive over addition: $\left[R;\cdot\right]$, 
 $a\left(b+c\right)=ab+ac$.$\left(a+b\right)c=ac+bc$ is called a ring.
> **Basic Knowledge** (Properties of Invertible Elements in a Ring with Identity) Let $R$ be a ring with identity and 

 $R$ its identity element. If $e$ are invertible, then $u,v\in R$ is invertible and $uv$. If $\left(uv\right)^{-1}=v^{-1}u^{-1}$, the finite geometric series gives$x^{m}=0$### Problem 1
(Problem 2.1-3) Let $$
> \left(e+x\right)^{-1}=e-x+x^{2}-\cdots+\left(-1\right)^{m-1}x^{m-1}.
> $$

 be a set on which addition and multiplication are defined. If the addition 

 $R=\left\{a,b,c\right\}$ and multiplication $R$ tables are respectively$+$determine whether $\cdot$ forms a ring.
$$
\begin{array}{c\left|ccc}
+ & a & b & c\\hline
a & a & b & c\\
b & b & c & a\\
c & c & a & b
\end{array}
\begin{array}{c\right|ccc}
\cdot & a & b & c\\hline
a & a & a & a\\
b & a & a & a\\
c & a & b & a
\end{array}
$$
 is the additive identity, and $R$ (via 

 

 $a$, $\left(R,+\right)\cong\mathbb Z_3$, $a\mapsto0$), so $b\mapsto1$ is an abelian group, satisfying condition (1) of **Definition 2.1.1** (Ring).$c\mapsto2$, $\left(R,+\right)$, 

 $x=b$. From the addition table, $y=c$. From the multiplication table, $z=b$, $b+c=a$, $a\cdot b=a$.$b\cdot b=a$Now compute the right-hand side:$c\cdot b=b$Since 

 
$$
\begin{aligned}\left(x+y\right)z&=\left(b+c\right)b\\&=a\cdot b\\&=a.\end{aligned}
$$

,
$$
\begin{aligned}xz+yz&=bb+cb\\&=a+b\\&=b.\end{aligned}
$$

Left distributivity fails. Moreover, multiplication is also not associative: take $a\ne b$, 
$$
\left(b+c\right)b\ne bb+cb.
$$

, $x=c$; from the multiplication table, $y=c$, $z=b$, $c\cdot c=a$, so$c\cdot b=b$while$a\cdot b=a$The two are unequal.
$$
\begin{aligned}\left(c\cdot c\right)\cdot b&=a\cdot b\\&=a,\end{aligned}
$$
 does not satisfy the distributive law or associativity of multiplication, and 
$$
\begin{aligned}c\cdot\left(c\cdot b\right)&=c\cdot b\\&=b.\end{aligned}
$$
 does not form a ring. 

 $R$### Problem 2$R$ be a ring with identity, $\blacksquare$

 its identity element, and 

 $R$. If there exists $e$ such that $a\in R$, then $\exists m\in\mathbb N$ is called nilpotent. Prove that if $a^{m}=0$ is nilpotent, then $a$ is invertible.$a$. Construct$e+a$Compute the product:

 

 $a^{m}=0$where all intermediate terms cancel and 
$$
b=e-a+a^{2}-a^{3}+\cdots+\left(-1\right)^{m-1}a^{m-1}.
$$

. Similarly,
$$
\begin{aligned}\left(e+a\right)b&=\left(e+a\right)\left(e-a+a^{2}-\cdots+\left(-1\right)^{m-1}a^{m-1}\right)\\&=e+\left(-1\right)^{m-1}a^{m}\\&=e,\end{aligned}
$$

Hence $a^{m}=0$ is the inverse of 
$$
\begin{aligned}b\left(e+a\right)&=e+\left(-1\right)^{m-1}a^{m}\\&=e.\end{aligned}
$$

, i.e. $b$ is invertible. $e+a$### Problem 3$e+a$ be a ring with identity, $\blacksquare$

 its identity element, and 

 $R$. If an element $e$ satisfies $a\in R$ ($c$), then $ca=e$ is called a right inverse (left inverse) of $ac=e$. If $c$ is both a left and right inverse of $a$, then $c$ is called the inverse of $a$, and $a$ is called invertible. Prove that for any $c$, $a$ is invertible if and only if $a$ is invertible.$a,b\in R$ is invertible, and write its inverse as $e-ab$. Construct$e-ba$Verify that 

 

 $e-ab$ is the inverse of $c=\left(e-ab\right)^{-1}$:
$$
d=e+bca.
$$

where we used $d$. Similarly,$e-ba$where we used 
$$
\begin{aligned}\left(e-ba\right)d&=\left(e-ba\right)\left(e+bca\right)\\&=e-ba+bca-babca\\&=e-ba+b\left(e-ab\right)ca\\&=e-ba+ba\\&=e,\end{aligned}
$$

. Hence $\left(e-ab\right)c=e$ is the inverse of 
$$
\begin{aligned}d\left(e-ba\right)&=\left(e+bca\right)\left(e-ba\right)\\&=e-ba+bca-bcaba\\&=e-ba+bc\left(e-ab\right)a\\&=e-ba+ba\\&=e,\end{aligned}
$$

, and $c\left(e-ab\right)=e$ is invertible.$d=e+bca$ is invertible, interchanging $e-ba$ in the above argument shows that $e-ba$ is invertible.

Therefore $e-ba$ is invertible if and only if $a,b$ is invertible. $e-ab$### Problem 4

(Problem 2.1-16) (Hua Loo-Keng) Let $e-ab$ be a ring with identity, $e-ba$ its identity element, and $\blacksquare$

. Prove that if both 

 $R$ and $e$ are invertible, then $a,b\in R$ is invertible, and $ab$ is also invertible, with$ab-e$### Solution to Problem 4$a-b^{-1}$ is invertible,$\left(a-b^{-1}\right)^{-1}-a^{-1}$By assumption 
$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$

 is invertible, and 

 $b$ is invertible; by **Basic Knowledge** (Properties of Invertible Elements in a Ring with Identity), the product of invertible elements is invertible, so 
$$
a-b^{-1}=\left(ab-e\right)b^{-1}.
$$

 is invertible, and$ab-e$Write $b^{-1}$; then $a-b^{-1}$ exists. We want to prove that
$$
\left(a-b^{-1}\right)^{-1}=b\left(ab-e\right)^{-1}.
$$

is invertible, with inverse $X=ab-e$.$X^{-1}$By the Hua identity in Problem 3,
$$
\left(a-b^{-1}\right)^{-1}-a^{-1}=bX^{-1}-a^{-1}
$$
Note that $aba-a=a\left(ba-e\right)$, so 

 
$$
\begin{aligned}\left(bX^{-1}-a^{-1}\right)\cdot a\left(ba-e\right)&=bX^{-1}a\left(ba-e\right)-a^{-1}a\left(ba-e\right)\\&=\left[bX^{-1}a-e\right]\left(ba-e\right).\end{aligned}
$$

. Then

$$
\left(e-ba\right)^{-1}=e+b\left(e-ab\right)^{-1}a.
$$

Therefore,$X=ab-e=-\left(e-ab\right)$Also $X^{-1}=-\left(e-ab\right)^{-1}$, so
$$
\begin{aligned}bX^{-1}a&=-b\left(e-ab\right)^{-1}a\\&=-\left[\left(e-ba\right)^{-1}-e\right]\\&=e-\left(e-ba\right)^{-1}.\end{aligned}
$$
Symmetrically, the product in the other direction is also 
$$
bX^{-1}a-e=-\left(e-ba\right)^{-1}.
$$
. Hence $ba-e=-\left(e-ba\right)$ is the inverse of
$$
\begin{aligned}\left[bX^{-1}a-e\right]\left(ba-e\right)&=\left(-\left(e-ba\right)^{-1}\right)\cdot\left(-\left(e-ba\right)\right)\\&=\left(e-ba\right)^{-1}\left(e-ba\right)\\&=e.\end{aligned}
$$
i.e.$e$ $a\left(ba-e\right)=aba-a$ 
$$
bX^{-1}-a^{-1}=\left(a-b^{-1}\right)^{-1}-a^{-1}
$$
is the inverse, i.e.
$$
\left(\left(a-b^{-1}\right)^{-1}-a^{-1}\right)^{-1}=aba-a.
$$
$\blacksquare$
