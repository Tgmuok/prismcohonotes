 Let R be a ring. Let $\displaystyle{E=Proj \ R[X,Y,Z]/ <X^3+aX^2Z+bXZ^2+cZ^3-Y^2Z>}$.
 The nonsingular locus  $E_{{ns}}$  of E admits a group structure .Take the identity to be the point $O=[0:1:0]$ corresponding to the ideal $<X,Z>$.
 
 Consider the formal completion of E at O. The locus Y $\ne$ 0 is the affine Spec A, where $A=R[x,z]/<x^3+ax^2z+bxz^2+cz^2-z>$ and $x=\frac{X}{Y},\ z=\frac{Z}{Y}$.
 
 The point O corresponds  to the ideal <x,z>. The formal completion of E along O is $\hat{{E}}=Spf \ \hat{{A}}$, where $\hat{A}=\varprojlim \ A/I^n \cong R[[z]]$.
 
 >[!attention]- Remark
 >·设$B=R[x]$ , $I = <x>$ , 则 $\varprojlim\ B/I^n=R[[x]]$. 
 > ·$\hat{A}=\varprojlim A/I^n=R[[x,z]]/<x^3+ax^2z+bxz^2+cz^3-z>$.
 > 从而在$\hat{A}$中, $x^3=z(1-ax^2-bxz-cz^2)$. 并且由于$1-ax^2-bxz-cz^2$的常数项可逆，其本身在形式幂级数环中是可逆元，即$x^3$与$z$是相伴的.由 *[交换环上的形式幂级数隐函数定理](https://www.mat.univie.ac.at/~slc/s/s61Asokal2.pdf) *：$\exists \ ! \ z(x)\in R[[x]]\ ,\ s.t.z(0)=0,\ F(x,z(x))=0,$其中$F(x,z)=x^3+ax^2z+bxz^2+cz^3-z$.从而z可表示为x的形式幂级数，即 $\hat{A}\cong R[[x]]\cong R[[z]]$.
 
 (Do not worry about if you are not familiar with formal schemes, as we just work with the formal power series $R[[z]]$. The group operation $E_{ns}\times_{R} E_{ns}\rightarrow E_{ns}$ indues a group operation $\hat{E}\times_{R} \hat{E} \rightarrow \hat{E}$. This gives us a continuous map of power series rings:
$$ \begin{align} R[[z]]\cong\hat{A}\rightarrow \hat{A}\hat{\otimes}_{R}\hat{A}\cong R[[z_{1},z_{2}]]\end{align} $$
Note that any continuous map $R[[z]]\rightarrow R[[z_{1},z_{2}]]$ is determined by the image of $z$ (Denote the image of $z$ by $F(z_{1},z_{2})$).Similarly, there is an inverse may $\hat{E}\rightarrow \hat{E}$,which corresponds to a continuous map of power series rings $R[[z]]\rightarrow R[[z]]$, and donote the image of $z$ by $i(z)$.

Since the group operation is commutative and associative, we will have
$$\begin{align}  \\
     F(z_{1,}z_{2})=F(z_{2},z_{1}) ,  \\
 \end{align}$$
$$ \begin{align}  \\
    F(z_{1},F(z_{2},z_{3}))=F(F(z_{1},z_{2}),z_{3}).  \\
	\end{align} $$
	
Similarly, since $i$ is the inverse operation ,and $z=0$ is the identity,

$$\begin{align}
	F(z,i(z))=0
\end{align}$$
The above analysis leads us to consider the notion of a $formal \ group \ law$.
