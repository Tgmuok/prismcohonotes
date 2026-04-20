 >I want to give a brief introduction of Prismatic Cohomology. In this talk, I will avoid to use the language of $\infty$-Category. But in another talk ( p-adic Hodege Theory ) , I will follow Scholze‘s paper ([Pirsms  and  Prismatic Cohomology](https://arxiv.org/abs/1905.08229)) rigorously to study Prismatic Cohomology systematically. You can regard this seminar as a baby version of Introduction to Prismatic Cohomology, since we won't use profound knowledge overly. 
 
---

## The Main Theorem 

>[!notes]+  The Main Theorem ( Fundamental Theorem of Prismatic Cohomology )
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
> >  $$ 
> >  \mathrm{RT}_\Delta(X/A) \widehat{\otimes}_A^L B \cong \mathrm{RT}_\Delta(Y/B), 
> >  $$ 
> >  where the completion on the left is the derived $(p,J)$-adic completion.
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

## Appendix
>We will cover chapters 1-9 of [BC] and chapters 1-8 of [FO] (these two references cover roughly the same material), chapters 2-13 of [SW], and some additional topics. Depending on interest, these may include [Sch1], [BS1], [BL].

>### Main references

- [BC] O. Brinon and B. Conrad, [CMI summer school notes on p-adic Hodge theory](https://math.stanford.edu/~conrad/papers/notes.pdf)
- [BL] B. Bhatt and J. Lurie, [Absolute prismatic cohomology](https://arxiv.org/pdf/2201.06120)
- [BS1] B. Bhatt and P. Scholze, [Prisms and prismatic cohomology](https://arxiv.org/pdf/1905.08229)
- [FO] J.-M. Fontaine and Y. Ouyang, [Theory of p-adic Galois representations](http://staff.ustc.edu.cn/~yiouyang/galoisrep.pdf)
- [Sch1] P. Scholze, [p-adic Hodge theory for rigid analytic varieties](https://people.mpim-bonn.mpg.de/scholze/pAdicHodgeTheory.pdf)
- [SW] P. Scholze and J. Weinstein, [Berkeley lectures on p-adic geometry](https://people.mpim-bonn.mpg.de/scholze/Berkeley.pdf)

>### Other references
- [Bel] J. Bellaiche, [An introduction to the conjecture of Bloch and Kato](http://virtualmath1.stanford.edu/~conrad/BSDseminar/refs/BKintro.pdf)
- [Ber] L. Berger, [An introduction to the theory of p-adic representations](https://perso.ens-lyon.fr/laurent.berger/articles/article05.pdf)
- [Bos1] S. Bosch, [Lectures on formal and rigid geometry](https://utah-primoprod.hosted.exlibrisgroup.com/permalink/f/1g0gstr/TN_cdi_springer_books_10_1007_978_3_319_04417_0)
- [Bos2] G. Bosco, [On the p-adic pro-étale cohomology of Drinfeld spaces](https://arxiv.org/abs/2110.10683)
- [BS2] B. Bhatt and P. Scholze, [The pro-étale topology for schemes](https://arxiv.org/abs/1309.1198)
-  [ C ] P. Colmez, [Une construction de BdR+](http://www.numdam.org/article/RSMUP_2012__128__109_0.pdf)
- [ F ] J.-M. Fontaine, Formes différentielles et modules de Tate des variétés abéliennes sur les corps locaux
- [ H ] R. Huber, Étale Cohomology of Rigid Analytic Varieties and Adic Spaces
- [K1] K. Kedlaya, [p-adic cohomology: from theory to practice](https://swc-math.github.io/aws/2007/KedlayaNotes11Mar.pdf)
- [K2] K. Kedlaya, [New methods for (φ,Γ)-modules](https://link.springer.com/content/pdf/10.1186/s40687-015-0031-z.pdf)
- [Mil] J. Milne, [Field theory and Galois theory](https://www.jmilne.org/math/CourseNotes/FT.pdf)
- [MW] L. Mann and A. Werner, [Local systems on diamonds and p-adic vector bundles](https://arxiv.org/abs/2005.06855)
- [ R ] K. Rubin, [Euler systems and Kolyvagin systems](https://www.math.uci.edu/~krubin/oldcourses/09.234/lectures.pdf)
- [Sch2] P. Scholze, [Étale Cohomology of Diamonds](https://arxiv.org/abs/1709.07343)
- [Ser] J.-P. Serre, Local fields
- [Sil] J. Silverman, [The arithmetic of elliptic curves](https://utah-primoprod.hosted.exlibrisgroup.com/permalink/f/1g0gstr/TN_cdi_springer_books_10_1007_978_0_387_09494_6)
- [Sta] [Stacks Project](https://stacks.math.columbia.edu/)
- [ T ] J. Tate, [p-divisible groups](https://utah-primoprod.hosted.exlibrisgroup.com/permalink/f/1g0gstr/TN_cdi_crossref_primary_10_1112_jlms_s1_44_1_666a)
- [ W ] J. Weinstein, [Arizona Winter School 2017: Adic spaces](http://swc.math.arizona.edu/aws/2017/2017WeinsteinNotes.pdf)

>If you are looking for exercises, there are some in [BC] and in these two references:

- [ D ] H. Diao, [Period rings and period sheaves](https://swc-math.github.io/aws/2017/2017DiaoProblems.pdf)
- [Mie] Y. Mieda, [Adic spaces and perfectoid spaces](https://swc-math.github.io/aws/2017/2017MiedaProblems.pdf)

---

## Homework & Answer

1. [Week of  Seminar 1](https://dgulotta.github.io/hodge_hw1.pdf)
2. [Week of  Seminar 3](https://dgulotta.github.io/hodge_hw2.pdf)
3. [Week of  Seminar 5](https://dgulotta.github.io/hodge_hw3.pdf)
4. [Week of  Seminar 7](https://dgulotta.github.io/hodge_hw4.pdf)
5. [Week of  Seminar 9](https://dgulotta.github.io/hodge_hw5.pdf)
6. [Week of  Seminar 11](https://dgulotta.github.io/hodge_hw6.pdf)
7. [Week of  Seminar 13](https://dgulotta.github.io/hodge_hw7.pdf)
8. [Week of  Seminar 15](https://dgulotta.github.io/hodge_hw8.pdf)
9. [Week of  Seminar 17](https://dgulotta.github.io/hodge_hw9.pdf)
10. [Week of  Seminar 19](https://dgulotta.github.io/hodge_hw10.pdf)
11. [Week of  Seminar 21](https://dgulotta.github.io/hodge_hw11.pdf)
12. [Week of  Seminar 23](https://dgulotta.github.io/hodge_hw12.pdf)
13. [Week of  Seminar 25](https://dgulotta.github.io/hodge_hw13.pdf)
14. [Week of  Seminar 27](https://dgulotta.github.io/hodge_hw14.pdf)

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

---
