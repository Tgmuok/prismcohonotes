 I want to give a brief introduction of Prismatic Cohomology. In this talk, I will avoid to use the language of $\infty$-Category. But in another talk (p-adic Hodege Theory) , I will follow Scholze‘s paper ([Pirsms  and  Prismatic Cohomology](https://arxiv.org/abs/1905.08229)) rigorously to study Prismatic Cohomology systematically. You can regard this seminar as a baby version of Introduction to Prismatic Cohomology, since we won't use profound knowledge overly. 
 
---

## The Main Theorem 

>[!notes]+  The Main Theorem (Fundamental Theorem of Prismatic Cohomology). 
>
>Let $(A,I)$ be a bounded prism, and let $X$ be a smooth $p$-adic formal scheme over $A/I$. Let 
>$$ 
>\mathrm{RT}_\Delta(X/A) := R\Gamma\left( (X/A)_\Delta, \mathcal{O}_\Delta \right), 
>$$ 
>
>which is a commutative algebra in the derived category $D(A)$ of $A$-modules, and comes equipped with a $\phi_A$-linear endomorphism $\phi$.
>
> >(1) **Crystalline Comparison** 
> >
>> If $I = (p)$, then there is a canonical $\phi$-equivariant isomorphism 
>> $$
>>  \mathrm{RT}_{\mathrm{crys}}(X/A) \cong \mathrm{RT}_\Delta(X/A) 
>> \widehat{\otimes}_{A,\phi_A}^L A 
>> $$ 
>> of commutative algebras in $D(A)$. 
>> 
> >(2) **Hodge-Tate Comparison** 
> >
> >If $X$ is affine, say $X = \mathrm{Spf}\, R$, there is a canonical $R$-module isomorphism 
> >$$
> >\Omega^i_{R/(A/I)}\{-i\} \cong H^i\left( \mathrm{RT}_\Delta(X/A) \otimes_A^L A/I \right). 
> >$$
> > Here we write $M\{i\} = M \otimes_{A/I} (I/I^2)^{\otimes i}$ for any $A/I$-module $M$.
> >
> > (3) **de Rham Comparison** 
> > 
> > There is a canonical isomorphism 
> > $$ 
> > \mathrm{RT}_{\mathrm{dR}}(X/(A/I)) \cong \mathrm{RT}_\Delta(X/A) \widehat{\otimes}_{A,\phi_A}^L A/I 
> > $$ 
> > of commutative algebras in $D(A)$. Moreover, it can be upgraded naturally to an isomorphism of commutative differential graded algebras.
> > 
> >  (4) **Étale Comparison** 
> >  
> >  Assume $A$ is perfect. Let $X_\eta$ be the generic fibre of $X$ over $\mathbb{Q}_p$, as a (pre-)adic space. For any $n \geq 0$, there is a canonical isomorphism 
> >  $$ 
> >  \mathrm{RT}_{\text{ét}}(X_\eta, \mathbb{Z}/p^n\mathbb{Z}) \cong \left( \mathrm{RT}_\Delta(X/A)/p^n\left[\tfrac{1}{p}\right] \right)^{\phi=1} 
> >  $$
> >  of commutative algebras in $D(\mathbb{Z}/p^n)$. 
> >  
> >  (5) **Base Change** 
> >  
> >  Let $(A,I) \to (B,J)$ be a map of bounded prisms, and let $Y = X \times_{\mathrm{Spf}(A/I)} \mathrm{Spf}(B/J)$. Then the natural map induces an isomorphism
> >$$
> >\mathrm{RT}_\Delta(X/A) \widehat{\otimes}_A^L B \cong \mathrm{RT}_\Delta(Y/B),
> >$$
> >where the completion on the left is the derived $(p,J)$-adic completion.
> >
> >   (6) **Image of $\phi$**
> >
> >   The linearization 
> >   $$
> >    \phi^* \mathrm{RT}_\Delta(X/A) \to \mathrm{RT}_\Delta(X/A) 
> >    $$ 
> >    of $\phi$ becomes an isomorphism after inverting $I$. More precisely, if $I = (d)$ is principal, there is a map $V_i : H^i_\Delta(X/A) \to H^i(\phi^* \mathrm{RT}_\Delta(X/A))$ such that $V_i \phi = \phi V_i = d^i$.
> 
> In particular, it follows from the **Hodge-Tate Composition** that $R\Gamma_{\Delta}(X,A)$ is a perfect complex of $A$-modules if X is proper.
---
## Content
[[Seminar 1 · Motivation ：Complex Hodge Theory]]

[[Seminar 2 · Infinity Galois Theory]]

[[Seminar 3 · Elliptic Curves]]

[[Seminar 4 · Formal Groups]]

[[Seminar 5 & 6 · Elliptic Curves , continued]]

[[Seminar 7 · Elliptic Curves over p-adic Fields]]

[[Seminar 8 · Galois Groups of Fields of Characteristic p and φ-modules]]

[[Seminar 9 · Generalization of φ-modules , Perfectoid Fields]]

[[Seminar 10 · Tilting and Untilting]]

[[Seminar 11 · Tilting and Field Extensions , Group Cohomology]]

[[Seminar 12 · Group Cohomology]]

[[Seminar 13 · Ax-Sen-Tate Theorem]]

[[Seminar 14 · The Ring B_{dR}]]

[[Seminar 15 · B_{dR} and Differentials]]

[[Seminar 16 · B_{dR} and Differentials , continued]]

[[Seminar 17 · Sites and Cohomology]]

[[Seminar 18 · Sites , étale and proétale Cohomology]]

[[Seminar 19 · Hodge-Tate Decomposition for Abelian Varieties ]]

[[Seminar 20 · Huber Rings ]]

[[Seminar 21 · Adic Spaces]]

[[Seminar 22 · Examples of Adic Spaces , Analytic Adic Spaces]]

[[Seminar 23 · Rigid Analytic Spaces , Perfectoid Rings]]

[[Seminar 24 · Persectoid Spaces]]

[[Seminar 25 · Pro-étale Sites and Diamonds]]

[[Seminar 26 · More Examples of Diamonds]]

[[Seminar 27 · Quasi-Pro-étale Sites]]

[[Seminar 28 · Period Sheaves]]

[[Seminar 29 · Prismatic Cohomology]]

---
## Notations I will use

> [!caution]- Remark
> remark

>[!notes]+ Def 
>definition

>[!danger]+ Them
>theorem

>[!abstract]+ Prop 
>proposition

> [!tip]+ lemma 
> lemma

>[!done]+ Coro 
>corollary

>[!example]+ ex 
>example

>[!question]+ Question
>question

>[!info]+ Notation
>notation
