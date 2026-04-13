 Let $R$ be a ring. Let $\displaystyle{E=Proj \ R[X,Y,Z]/ <X^3+aX^2Z+bXZ^2+cZ^3-Y^2Z>}$.
 The nonsingular locus  $E_{{ns}}$  of $E$ admits a group structure .
 Take the identity to be the point $O=[0:1:0]$ corresponding to the ideal $<X,Z>$.
 
 Consider the formal completion of $E$ at $O$. The locus $Y \ne 0$ is the affine $Spec A$, where 
 $$
 A=R[x,z]/<x^3+ax^2z+bxz^2+cz^2-z>
 $$ 
 and $x=\frac{X}{Y},\ z=\frac{Z}{Y}$.
 
 The point $O$ corresponds  to the ideal $<x,z>$. The formal completion of $E$ along $O$ is $\hat{{E}}=Spf \ \hat{{A}}$, where $\hat{A}=\varprojlim \ A/I^n \cong R[[z]]$.
 
 >[!attention]- Remark
 >
 >·设$B=R[x]$ , $I = <x>$ , 则 $\varprojlim\ B/I^n=R[[x]]$. 
 >
 > ·$\hat{A}=\varprojlim A/I^n=R[[x,z]]/<x^3+ax^2z+bxz^2+cz^3-z>$. 
 > 从而在$\hat{A}$中, $x^3=z(1-ax^2-bxz-cz^2)$. 并且由于$1-ax^2-bxz-cz^2$的常数项可逆，其本身在形式幂级数环中是可逆元，即$x^3$与$z$是相伴的.由 *[交换环上的形式幂级数隐函数定理](https://www.mat.univie.ac.at/~slc/s/s61Asokal2.pdf) *：
 > $$
 > \exists \ ! \ z(x)\in R[[x]]\ ,\ s.t.z(0)=0,\ F(x,z(x))=0,
 > $$
 > 其中$F(x,z)=x^3+ax^2z+bxz^2+cz^3-z$.从而z可表示为x的形式幂级数，即 $\hat{A}\cong R[[x]]\cong R[[z]]$.
 
 (Do not worry about if you are not familiar with formal schemes, as we just work with the formal power series $R[[z]]$. The group operation $E_{ns}\times_{R} E_{ns}\rightarrow E_{ns}$ indues a group operation $\hat{E}\times_{R} \hat{E} \rightarrow \hat{E}$. This gives us a continuous map of power series rings:
 
$$
R[[z]]\cong\hat{A}\rightarrow \hat{A}\otimes_{R}\hat{A}\cong R[[z_{1},z_{2}]]
$$

Note that any continuous map $R[[z]]\rightarrow R[[z_{1},z_{2}]]$ is determined by the image of $z$ (Denote the image of $z$ by $F(z_{1},z_{2})$).Similarly, there is an inverse may $\hat{E}\rightarrow \hat{E}$,which corresponds to a continuous map of power series rings $R[[z]]\rightarrow R[[z]]$, and donote the image of $z$ by $i(z)$.

>[!attention]- Remark
>
>·$E_{ns}$是概形$E$的非奇异轨迹，其具有群结构，是$R$上的一个群概形，配备群运算. 由$Jacobian$判别法，可以得到$O$是$E$的光滑点，从而$O\in E_{{ns}}$，则$\hat{E}$是$E$（由于$O\in E_{{ns}}$，并且完备化是在刻画$O$的无穷小领域，从而等价于$E$沿着$O$做完备化）沿着闭子概形$\left\{ O\right\}$的完备化.并且借助形式完备化的性质：若有概形态射$f:X\rightarrow Y$将$X$的闭子概形$Z$映射到$Y$的闭子概形$W$，则存在$f$诱导唯一的形式完备化态射$\hat{f}:\hat{X}_{/Z}\rightarrow \hat{Y}_{/W}$.可知$E_{ns}$上的群结构可以诱导出$\hat{E}$上的群结构.

Since the group operation is commutative and associative, we will have
$$
     F(z_{1,}z_{2})=F(z_{2},z_{1}) ,  
 $$
$$ 
    F(z_{1},F(z_{2},z_{3}))=F(F(z_{1},z_{2}),z_{3}).  \\
$$
Similarly, since $i$ is the inverse operation ,and $z=0$ is the identity,
$$
	F(z,i(z))=0
$$
The above analysis leads us to consider the notion of a $formal \ group \ law$.
>[!attention]- Remark
>
>我们明确一下这里的交换律为什么反映在形式幂级数中是交换两个变元.定义扭转态射
>
>$$
>\tau : E_{ns}\times_{R} E_{ns}\rightarrow  E_{ns}\times_{R} E_{ns}
>$$
>
>$$
>(P,Q)\mapsto(Q,P)
>$$
>
>这样交换律就可以表示为$m \circ \tau=m$.从而回到对应的环同态为$\hat{\tau}^{*}\circ\hat{m}^{*}=\hat{m}^{*}$，其作用在$z$上，右边为$F(z_1,z_2)$，左边为$F(z_{2},z_{1})$.

>[!notes]+ Def 4.1
>
>A $one-parameter\  commutative \ formal \ froup$ over a ring R is a power series $F(X,Y) \in R[[X,Y]]$ satisfying the following conditions:
>>(1) : $F(X,0)=X$ and $F(0,Y)=Y$
>>(2) : $F(X,F(Y,Z))=F(F(X,Y),Z)$
>>(3) : $F(X,Y)=F(Y,X)$
>>(4) : There is a power series $i(T)\in R[[T]]$ satisfying $i(0)=0$ and $F(T,i(T))=0$.

>[!example]+ Ex 4.2
>
>The formal additive group $\hat{\mathbb{G}}_a$ is defined by: 
>>$$
>>F(X,Y)=X+Y
>>$$

>[!example]+ Ex 4.3
>
>The formal multiplicative group $\hat{\mathbb{G}}_m$ is defined by : 
>>$$
>>F(X,Y)=(1+X)(1+Y)-1=X+Y+XY
>>$$

>[!notes]+ Def 4.4
>
>A homomorphism of formal groups $F \rightarrow G$ is a power series $\phi \in R[[T]]$ such that  
>>$$
>>\phi(F(X,Y))=G(\phi(X),\phi(Y))
>>$$

>[!example]+ Ex 4.5
>
>For any integer m, we can define a multiplicative-by-m homomorphism $(R[[T]] \ni )[m]: F\rightarrow F$ inductively by
>
>>$$
>>[0](T)=0
>>$$
>>$$
>>[m+1](T)=F([m]T,T)
>>$$
>>$$
>>[m-1](T)=F([m]T,i(T))
>>$$
>
>· If $F=\mathbb{G}_{a}$, then $[m](T)=mT$.
>
>· If $F=\mathbb{G}_m$, then $[m](T)=(1+T)^m-1$

>[!tips]+  lemma 4.6
>
>Let  $F=a_{1}T+a_{2}T^2+\cdots \in TR[[T]]=\left\{ F(T)\in R[[T]] \ |\ F(0)=0\right\}$ , with $a_1\in R^{\times}$.
>Then there is a unique power series $G\in TR[[T]]$ such that $F(G(T))=G(F(T))=T$. 
>>pf: See [^1][Sil 09,Lemma IV 2.4] 

^69156c

>[!warning]- Remark
>
>· [[#^69156c|lemma 4.6]]是微积分中[反函数存在定理]的形式幂级数版本：即无常数项的形式幂级数只要一次项系数可逆（对应形式导函数不为0），就存在唯一的形式逆幂级数.


>[!tips]+ lemma 4,7
>
>Let $F$ be a formal group over $R$, and let m be an integer that is invertible in $R$. Then $[m]$ is an automorphism.
>>pf: It is clear that multiplication by $m$ sends $T\mapsto mT+O(T^2)$, where $O(T^2)$ are the $degree \ge 2$ 's monomials.
>>Any such map is an automorphism of $R[[T]]$ by [[#^69156c|lemma 4.6]]

^dd866a

Now let $K$ be a complete discretely valued nonarchimedean field (i.e. local field ), and let $R = \mathcal{O}_K$. Let $\mathfrak{m}_K$ be the maximal ideal of $\mathcal{O}_K$, and let $k = \mathcal{O}_K/\mathfrak{m}_K$ be the residue field. Now we focus on the formal group on $\mathcal{O}_{K}$.

For every $x \in \mathfrak{m}_K$, there is a unique continuous homomorphism $\mathcal{O}_K [\![ T ]\!] \to \mathcal{O}_K$ sending $T \mapsto x$, and conversely, all continuous homomorphisms $\mathcal{O}_K [\![ T ]\!] \to \mathcal{O}_K$ are of this form. Similarly, homomorphisms $\mathcal{O}_K [\![ T_1, T_2 ]\!] \to \mathcal{O}_K$ are in bijection with $\mathfrak{m}_K \times \mathfrak{m}_K$.

>[!attention]- Remark
>
> ·由于赋值的原因，只有落在极大理想中的元素会对应形式群的“点”. 这是因为一元形式幂级数环 $\mathcal{O}[[T]]$ 的连续同态完全由生成元 $T$ 决定，且只能映射到 $\mathfrak{m}_{K}$ 中的元素，否则在形式幂级数中代入 $x \notin \mathfrak{m}_{K}$ ，则 $\nu(x) \le 0$ , $x^n$ 不会趋向于0，幂级数会发散. 从而此类同态与 $\mathfrak{m}_{K}$ 中的元素是一一对应的. 同理，二元形式幂级数环的连续同态由 $T_1.T_2$ 的像完全决定，因此和 $\mathfrak{m}_{K} \times  \mathfrak{m}_{K}$ 一一对应，这恰好适配形式群$F(X,Y)$.

If $F$ is a formal group, we will denote by $F(\mathfrak{m}_K)$ the set $\mathfrak{m}_K$, with the group operation $+_F$ given by 
$$
x +_F y = F(x,y).
$$

> [!example]+ Example 4.8  
> 
> We can identify $\widehat{\mathbb{G}}_a(\mathfrak{m}_K)$ with the additive group $\mathfrak{m}_K$, and there is an exact sequence 
> $$
> 0 \to \mathfrak{m}_K \to \mathcal{O}_K \to k \to 0 \ ,
> $$
> 
> where the first map is injection , and the second may is quotient map.

> [!example]+ Example 4.9 
> 
> We can identify $\widehat{\mathbb{G}}_m(\mathfrak{m}_K)$ with the multiplicative group $1 + \mathfrak{m}_K$, and there is an exact sequence 
> $$
> 1 \to (1 + \mathfrak{m}_K) \to \mathcal{O}_K^\times \to k^\times \to 1\ ,
> $$
> 
> where the first map is injection , and the second may is quotient map.

> [!tip]+ Lemma 4.10 
> For each positive integer $n$, the operation $+_F$ induces the usual additive group structure on $\mathfrak{m}_K^n/\mathfrak{m}_K^{n+1}$.

>[!attention]- Remark
>
>$\mathfrak{m}_{K}^n=\left\{ x\in \mathcal{O}_{K}\ | \ \nu(x)\ge n\right\}$ , $F(X,Y)=X+Y+(degree \ge 2 \ parts)$, 从对高次项取赋值后会发现其全部落在$\mathfrak{m}_{K}^{n+1}$中，在商中被消去，最终得到：
>$$ 
>x+_{F}y=F(x,y) \equiv x+y \  \ mod \ \ \mathfrak{m}_{K}^{n+1}
>$$

> [!tip]+ Lemma 4.11 
> 
>  If $x \in F(\mathfrak{m}_K)$ has finite order, then its order is a power of the characteristic of $k$. 
>  
 > > Pf.This follows from [[#^dd866a|lemma 4,7]].

>[!attention]- Remark
>
>Skipping of  lemma 4.11:借助于lemma 4.7：如果整数 $m\in \mathcal{O}_K$中可逆，则同态 $[m]$ 是形式群的自同构，从而 $[m](x)=0$ 当且仅当 $x=0$. 利用反证法，设 $x$ 的阶为$m$，可以证明 $m$ 不能有与 $char(k)$ 互素的素因子，即 $m$ 必须是 $p$ 的幂.

> [!notes]+ Def 4.12 
> 
> An $invariant  \ \ differential$ for $F$ is an expression of the form $P(T) \ dT \ (\in \Omega_{\mathcal{O}_{K}[[T]]/\mathcal{O}_K})$, where $P(T) \in \mathcal{O}_K [\![ T ]\!]$, such that 
> $$
> (4.13) \quad P(F(X,Y))F^{(1,0)}(X,Y) = P(X)
> $$  
> as formal power series, where 
>$$
>\displaystyle{F^{(1,0)}(X,Y) = \frac{\partial F}{\partial X}}.
>$$

^f70ff0

>[!attention]- Remark
>
>·这个定义是$\textbf{李群左不变微分形式的形式群版本}$，此处的“不变”指的是在形式群的平移作用下保持不变. 并且一维交换形式群的不变微分在相差一个$\mathcal{O}_{K}$中单位的意义下是唯一的. 并且我们可以得到标准不变微分：
>$$
>\displaystyle \omega=\frac{dT}{F^{(1,0)}(0,T)}.
>$$
>
>·不变微分是形式群理论的核心工具，它是形式群的李代数的对偶基，对不变微分积分可以得到$\textbf{形式群的对数映射}$：
>$$
>\log_{F}(T)= \int P(T)\ dT\ , 
>$$
>这是$p-adic$分析中把形式群同构到形式加法群的核心工具.

> [!danger]+ Theorem 4.14 
> 
>  Let 
>  $$
>  (4.15) \quad \omega_F = F^{(1,0)}(0,T)^{-1} dT.
>  $$ 
>  Then the invariant differentials for $F$ are precisely the constant multiples of $\omega_F$ with the coefficient in $\mathcal{O}_{K}$.
>  
> > Pf：
> > 
> >· When $X = 0$, the identity [[#^f70ff0|(4.13)]] becomes  
> > $$
> > P(Y)F^{(1,0)}(0,Y) = P(0).
> > $$ 
>>  Since $F^{(1,0)}(0,Y)$ has constant term 1, it is invertible. So the only possible invariant differentials are multiples of $\omega_F$, i.e.
>>  $$
>>  P(Y)=P(0)\cdot F^{(1,0)}(0,Y)^{-1}
>>  $$
>>  
>> ·To see that these are actually invariant differentials, differentiate the associative law 
>> $$
> > F(X, F(Y,Z)) = F(F(X,Y), Z).
> > $$
>>  with respect to $U$. We obtain
>>$$
> > F^{(1,0)}(X,F(Y,Z)) = F^{(1,0)}(F(X,Y),Z)F^{(1,0)}(X,Y).
> >$$
> >When $X = 0$, this becomes
> >$$
> >F^{(1,0)}(0,F(Y,Z)) = F^{(1,0)}(Y,Z)F^{(1,0)}(0,Y).
> >$$
> >take the inverse and multiply $F^{(1,0)}(Y,Z)$ , we get:
> >$$
> >F^{(1,0)}(0,F(Y,Z))^{-1} \cdot F^{(1,0)}(Y,Z)= F^{(1,0)}(0,Y)^{-1}.
> >$$
> >
> >which is the invariant differential by [[#^f70ff0|Def (4.12)]]

^7dd266

> [!tip]+ Corollary 4.16 
> 
>  If $\phi: F \to G$ is a homomorphism of formal group laws, then 
>  $$
>  \omega_G \circ \phi = \phi'(0)\omega_F.
>  $$ 

^8be727

>[!attention]- Remark
>
>$\omega_G \circ \phi$表示的是微分形式的拉回，即把$\omega_G$中的形式变量$T$替换为$\phi(T)$，同时按照微分法则计算$d\phi(T)$ :
>$$
>\phi^{\star}\omega_{G}=\omega_G \circ \phi(T)=G^{(1,0)}(0,\phi(T))^{-1}\cdot \phi^{'}(T)\ dT
>$$
> 其中$\phi^{'}(T)$是$\phi(T)$的形式导数.
> 由于$\phi^{\star}\omega_{G}$是$F$上的不变微分，由 [[#^7dd266|Them 4.14]]，其必为$\omega_{F}$的常数倍，即存在$c\in \mathcal{O}_{K}$，使得$\phi^{\star}\omega_{G}=c\cdot \omega_{{F}}$.在$T=0$处计算两边系数可得$c=\phi^{'}(0)$.

> [!tip]+ Corollary 4.17
> 
> Let $F$ be a formal group over $\mathcal{O}_K$, and suppose the multiplication-by-$p$ map sends 
>$$
>T \mapsto G(T).
>$$ 
> Then $G'(T)$ is divisible by $p$. 
> Equivalently,  
> $$
> G(T) = pH(T) + I(T^p)
> $$ 
> for some formal power series $H$, $I$.

^d4857d

>[!attention]- Remark
>
>·$[p]=pT+O(T^2)$是形式群 $F$的自同构，令[[#^8be727|corollary 4.16]] 中$\phi =[p]$，代入
>$$
>\phi^{\star}\omega_{G}=\omega_G \circ \phi(T)
>$$
>得到：
>$$
>F^{(1,0)}(0,G(T)^{-1}\cdot G^{'}(T))dT=p\cdot F^{(1,0)}(0,T)^{-1}dT
>$$
>消去 $dT$ 即可.（请注意此处的 $dT$ 并非是微积分中的“无穷小微分”，而是纯代数的形式微分，其来自于微分模，对于一元形式幂级数环$R=\mathcal{O}_{{K}}[[T]]$，$\Omega_{R/{\mathcal{O}_{K}}}$是一个$\textbf{秩为1的自由R-模}$，消去 $dT$ 本质上是因为任何形式微分都可以唯一的表示为$P(T)\cdot dT$的形式，在此基础上取自由模在基 $dT$ 下的坐标.）
>
>·由于$G^{'}(T)$被$p$整除 ,设$\displaystyle{ G(T)=\Sigma a_{n}T^n}$,则$G^{'}(T)=\Sigma na_{n}T^{n-1}$，从而所有的 $na_n$ 要被 $p$ 整除，则要么$n$被$p$整除，要么$a_n$被 $p$ 整除，这样$G(T)$就可以拆分为：
>$$
>G(T)=p\cdot H(T)+I(T^p).
>$$
>

> [!danger]+ Theorem 4.18 
> 
>  Let $F$ be a formal group over $\mathcal{O}_K$, and let $x \in F(\mathfrak{m}_K)$. Suppose that $x$ has exact order $p^n$, meaning that $p^n x = 0$ but $p^{n-1}x \neq 0$. Then $|x| \geq |p|^{1/(p^n - p^{n-1})}$.
>  
> > Pf. We use induction on $n$. 
>>
> > $\bf{Step \ 1 :}$ Suppose $n = 1$. Let $G(T)=pH(x)+I(x^p)$ be as in [[#^d4857d|Corollary 4.17]]. Then $x$ satisfies $G(x)= 0$. The linear term of $G(x)$ is $px$ by [[#^dd866a|lemma 4.7]]. 
> > 
> > All other terms with exponent not divisible by $p$ (i.e. $pH(x)-px$) are also multiples of $p$, so they have strictly smaller absolute values. 
> > i.e. $|pH(x)|=|px|$
> > 
> > Among the terms with exponent divisible by $p$ (i.e. $I(x^p)$), the largest possible absolute value is $|x|^p$. 
> > i.e.$|I(x^p)|\le |x|^p$
> > 
> > Since $G(x)=pH(x)+I(x^p)=0$ , we have $pH(x)=-I(x^p)$. So $|pH(x)|=|I(x^p)|$.
> > 
> > So we must have $|px| \leq |x|^p$. We can rewrite this equality as $|x| \geq |p|^{1/(p-1)}$. 
> >  
> > $\bf{Step \ 2 :}$Now assume that all points of exact order $p^n$ satisfy $|x| \geq |p|^{1/(p^n - p^{n-1})}$, and let $y$ be a point of exact order $p^{n + 1}$. 
> > Notice that $G(y)$ satisfies the induction assumption , we can divide $G(y)$ into $2$ parts: 
> > $$
> > G(y)=A(y)+B(y)
> > $$
> > and be similar to $\bf{Step \ 1}$:$|A(y)|=|py|\ ,\ |B(y)| \le |y|^p$ .
> >So 
> >$$
> >|G(y)|=|A(y)+B(y)|\le \max \left\{ |A(y)| , |B(y)| \right\}
> >$$
> >i.e.
> >$$
> >\max \left\{ |py| , |y|^p \right\}\ge |p|^{1/(p^n - p^{n-1})}
> >$$
> > If we assume that $|y|\le |p|^{1/(p^n - p^{n-1})}$, then we will obtain that $\max \left\{ |py| , |y|^p \right\} <|p|^{1/(p^n - p^{n-1})}$, which is a paradox.
> > This completes the induction. 

[^1]: J. H. Silverman. The arithmetic of elliptic curves, volume 106 of Grad. Texts Math. New York, NY: Springer, 2nd ed. edition, 2009.
