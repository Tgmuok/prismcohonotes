 Let R be a ring. Let $\displaystyle{E=Proj \ R[X,Y,Z]/ <X^3+aX^2Z+bXZ^2+cZ^3-Y^2Z>}$.
 The nonsingular locus  $E_{{ns}}$  of E admits a group structure .Take the identity to be the point $O=[0:1:0]$ corresponding to the ideal $<X,Z>$.
 
 Consider the formal completion of E at O. The locus Y $\ne$ 0 is the affine Spec A, where $A=R[x,z]/<x^3+ax^2z+bxz^2+cz^2-z>$ and $x=\frac{X}{Y},\ z=\frac{Z}{Y}$.
 
 The point O corresponds  to the ideal $<x,z>$. The formal completion of E along O is $\hat{{E}}=Spf \ \hat{{A}}$, where $\hat{A}=\varprojlim \ A/I^n \cong R[[z]]$.
 
 >[!attention]- Remark
 >
 >·设$B=R[x]$ , $I = <x>$ , 则 $\varprojlim\ B/I^n=R[[x]]$. 
 >
 > ·$\hat{A}=\varprojlim A/I^n=R[[x,z]]/<x^3+ax^2z+bxz^2+cz^3-z>$. 
 > 从而在$\hat{A}$中, $x^3=z(1-ax^2-bxz-cz^2)$. 并且由于$1-ax^2-bxz-cz^2$的常数项可逆，其本身在形式幂级数环中是可逆元，即$x^3$与$z$是相伴的.由 *[交换环上的形式幂级数隐函数定理](https://www.mat.univie.ac.at/~slc/s/s61Asokal2.pdf) *：$\exists \ ! \ z(x)\in R[[x]]\ ,\ s.t.z(0)=0,\ F(x,z(x))=0,$其中$F(x,z)=x^3+ax^2z+bxz^2+cz^3-z$.从而z可表示为x的形式幂级数，即 $\hat{A}\cong R[[x]]\cong R[[z]]$.
 
 (Do not worry about if you are not familiar with formal schemes, as we just work with the formal power series $R[[z]]$. The group operation $E_{ns}\times_{R} E_{ns}\rightarrow E_{ns}$ indues a group operation $\hat{E}\times_{R} \hat{E} \rightarrow \hat{E}$. This gives us a continuous map of power series rings:
 
$$
\begin{align*} 
R[[z]]\cong\hat{A}\rightarrow \hat{A}\hat{\otimes}_{R}\hat{A}\cong R[[z_{1},z_{2}]]
\end{align*} 
$$

Note that any continuous map $R[[z]]\rightarrow R[[z_{1},z_{2}]]$ is determined by the image of $z$ (Denote the image of $z$ by $F(z_{1},z_{2})$).Similarly, there is an inverse may $\hat{E}\rightarrow \hat{E}$,which corresponds to a continuous map of power series rings $R[[z]]\rightarrow R[[z]]$, and donote the image of $z$ by $i(z)$.

Since the group operation is commutative and associative, we will have
$$
\begin{align*}  \\
     F(z_{1,}z_{2})=F(z_{2},z_{1}) ,  \\
 \end{align*}
 $$
 
$$ 
\begin{align*}  \\
    F(z_{1},F(z_{2},z_{3}))=F(F(z_{1},z_{2}),z_{3}).  \\
	\end{align*} 
$$
	
Similarly, since $i$ is the inverse operation ,and $z=0$ is the identity,

$$
\begin{align*}
	F(z,i(z))=0
\end{align*}
$$
The above analysis leads us to consider the notion of a $formal \ group \ law$.

>[!notes]+ Def 4.1
>
>A $one-paralmeter\  commutative \ formal \ froup$ over a ring R is a power series $F(X,Y) \in R[[X,Y]]$ satisfying the following conditions:
>>(1) : $F(X,0)=X$ and $F(0,Y)=Y$
>>(2) : $F(X,F(Y,Z))=F(F(X,Y),Z)$
>>(3) : $F(X,Y)=F(Y,X)$
>>(4) : There is a power series $i(T)\in R[[T]]$ satisfying $i(0)=0$ and $F(T,i(T))=0$.

>[!example]+ Ex 4.2
>
>The formal additive group $\hat{\mathbb{G}}_a$ is defined by: 
>>$$F(X,Y)=X+Y$$

>[!example]+ Ex 4.3
>
>The formal multiplicative group $\hat{\mathbb{G}}_m$ is defined by : 
>>$$F(X,Y)=(1+X)(1+Y)-1=X+Y+XY$$

>[!notes]+ Def 4.3
>
>A homomorphism of formal groups $F \rightarrow G$ is a power series $\phi \in R[[T]]$ such that  
>>$$\phi(F(X,Y))=G(\phi(X),\phi(Y))$$

>[!example]+ Ex 4.4
>
>For any integer m, we can define a multiplicative-by-m homomorphism [m] : $F\rightarrow G$ inductively by
>
>>$$[0](T)=0$$
>>$$[m+1](T)=F([m]T,T)$$
>>$$[m-1](T)=F([m]T,i(T))$$
>
>If $F=\mathbb{G}_{a}$, then $[m](T)=mT$.
>
>If $F=\mathbb{G}_m$, then $[m](T)=(1+T)^m-1$

>[!tips]+ lemma 4.6 
>
>Let  $F=a_{1}T+a_{2}T^2+\cdots \in TR[[T]]$,
>with $a_1\in R^{\times}$.Then there is a unique power series $G\in TR[[T]]$ such that $F(G(T))=G(F(T))=T$.
>>pf: See [^1][Sil 09,Lemma IV 2.4]

^9e4360

>[!tips]+ lemma 4,7
>
>Let F be a formal froup over R, and let m be an integer that is invertible in R. Then [m] is an automorphism.
>>pf: It is clear that multiplication by m sends $T\mapsto mT+O(T)$.
>>Any such map is an automorphism of $R[[T]]$ by [[#^9e4360|lemma 4.6]] 

^dd866a

Now let $K$ be a complete discretely valued nonarchimedean field, and let $R = \mathcal{O}_K$. Let $\mathfrak{m}_K$ be the maximal ideal of $\mathcal{O}_K$, and let $k = \mathcal{O}_K/\mathfrak{m}_K$ be the residue field. For every $x \in \mathfrak{m}_K$, there is a unique continuous homomorphism $\mathcal{O}_K [\![ T ]\!] \to \mathcal{O}_K$ sending $T \mapsto x$, and conversely, all continuous homomorphisms $\mathcal{O}_K [\![ T ]\!] \to \mathcal{O}_K$ are of this form. Similarly, homomorphisms $\mathcal{O}_K [\![ T_1, T_2 ]\!] \to \mathcal{O}_K$ are in bijection with $\mathfrak{m}_K \times \mathfrak{m}_K$. If $F$ is a formal group, we will denote by $F(\mathfrak{m}_K)$ the set $\mathfrak{m}_K$, with the group operation $+_F$ given by $$x +_F y = F(x,y).$$
> [!example]+ Example 4.8  
> We can identify $\widehat{\mathbb{G}}_a(\mathfrak{m}_K)$ with the additive group $\mathfrak{m}_K$, and there is an exact sequence 
> $$0 \to \mathfrak{m}_K \to \mathcal{O}_K \to k \to 0.$$

> [!example]+ Example 4.9 
> We can identify $\widehat{\mathbb{G}}_m(\mathfrak{m}_K)$ with the multiplicative group $1 + \mathfrak{m}_K$, and there is an exact sequence 
> $$1 \to (1 + \mathfrak{m}_K) \to \mathcal{O}_K^\times \to k^\times \to 1.$$

> [!tip]+ Lemma 4.10 
> For each positive integer $n$, the operation $+_F$ induces the usual additive group structure on $\mathfrak{m}_K^n/\mathfrak{m}_K^{n+1}$.

> [!tip]+ Lemma 4.11 
>  If $x \in F(\mathfrak{m}_K)$ has finite order, then its order is a power of the characteristic of $k$. 
 > > *Proof.* This follows from [[#^dd866a|lemma 4,7]].

> [!notes]+ Definition 4.12 
> An invariant differential for $F$ is an expression of the form $P(T) dT$, where $P(T) \in \mathcal{O}_K [\![ T ]\!]$, such that $$(4.13) \quad P(F(X,Y))F^{(1,0)}(X,Y) = P(X)$$  as formal power series. 

^f70ff0

> [!danger]+ Theorem 4.14 >
>  Let 
>  $$(4.15) \quad \omega_F = F^{(1,0)}(0,T)^{-1} dT.$$ 
>  Then the invariant differentials for $F$ are precisely the constant multiples of $\omega_F$. 
> > *Proof.* When $X = 0$, the identity [[#^f70ff0|(4.13)]] becomes > $$P(Y)F^{(1,0)}(0,Y) = P(0).$$ 
>  Since $F^{(1,0)}(0,Y)$ has constant term 1, it is invertible. So the only possible invariant differentials are multiples of $\omega_F$. To see that these are actually invariant differentials, differentiate the associative law 
>  $$F(X, F(Y,Z)) = F(F(X,Y), Z).$$
>  with respect to $U$. We obtain
$$F^{(1,0)}(X,F(Y,Z)) = F^{(1,0)}(F(X,Y),Z)F^{(1,0)}(X,Y).$$
>When $X = 0$, this becomes
$$F^{(1,0)}(0,F(Y,Z)) = F^{(1,0)}(Y,Z)F^{(1,0)}(0,Z).$$

> [!tip]+ Corollary 4.16 
>  If $\phi: F \to G$ is a homomorphism of formal group laws, then 
>  $$\omega_G \circ \phi = \phi'(0)\omega_F.$$ 

> [!tip]+ Corollary 4.17
> Let $F$ be a formal group over $\mathcal{O}_K$, and suppose the multiplication-by-$p$ map sends 
>$$T \mapsto G(T).$$ 
> Then $G'(T)$ is divisible by $p$. Equivalently,  
> $$G(T) = pH(T) + I(T^p)$$ 
> for some formal power series $H$, $I$.


> [!danger]+ Theorem 4.18 
>  Let $F$ be a formal group over $\mathcal{O}_K$, and let $x \in F(\mathfrak{m}_K)$. Suppose that $x$ has exact order $p^n$, meaning that $p^n x = 0$ but $p^{n-1}x \neq 0$. Then $|x| \geq |p|^{1/(p^n - p^{n-1})}$.
> > *Proof.* We use induction on $n$. Suppose $n = 1$. Let $G(T)$ be as in Corollary 4.17. Then $x$ satisfies $G(x) = 0$. The linear term of $G(x)$ is $px$. All other terms with exponent not divisible by $p$ are also multiples of $p$, so they have strictly smaller absolute values. Among the terms with exponent divisible by $p$, the largest possible absolute value is $|x|^p$. So we must have $|px| \leq |x|^p$. We can rewrite this equality as $|x| \geq |p|^{1/(p-1)}$. 
> > Now assume that all points of exact order $n$ satisfy $|x| \geq |p|^{1/(p^n - p^{n-1})}$, and let $y$ be a point of exact order $n + 1$. In order for any of the terms of $G(y)$ to have absolute value greater than or equal to $|x|$, we must have $|y| \geq |p|^{1/(p^{n+1} - p^n)}$. This completes the induction.

[^1]: J. H. Silverman. The arithmetic of elliptic curves, volume 106 of Grad. Texts Math. New York, NY: Springer, 2nd ed. edition, 2009.
