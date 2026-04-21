Let $K$ be a nonarchimedean field.

>[!notes]+ Def 23.1
>
> A Tate algebra over $K$ is a Huber ring of the form $K\langle T_1,\dots,T_n\rangle$ for some $n$.

>[!abstract]+ Prop 23.2
>
> Let $A$ be a Tate algebra over $K$.
> 1. $A$ is noetherian.
> 2. Every ideal of $A$ is closed.
>
>> *Proof.* See [Bos14, Proposition 2.2.14 and Corollary 2.3.8].

>[!notes]+ Def 23.3
>
> An affinoid algebra over $K$ is a quotient $A/I$, where $A$ is a Tate algebra and $I$ is an ideal of $A$.

>[!notes]+ Def 23.4
>
> A rigid analytic space is an adic space over $K$ that can be covered by open subspaces of the form $\mathrm{Spa}(A,A^\circ)$, where $A$ is an affinoid algebra over $K$.

**Remark 23.5.** There is an older definition of rigid analytic spaces, due to Tate, that does not use the framework of adic spaces. Tate's category of quasiseparated rigid analytic spaces is equivalent to our category of quasiseparated rigid analytic spaces.

>[!abstract]+ Prop 23.6
>
> The category of rigid analytic spaces over $K$ admits finite fiber products.

>[!notes]+ Def 23.7
>
> A morphism $f: X \to Y$ of rigid analytic spaces over $K$ is separated if the image of the diagonal morphism $\Delta_f: X \to X \times_Y X$ is closed.

>[!notes]+ Def 23.8
>
> A morphism $f: X \to Y$ of rigid analytic spaces over $K$ is universally closed if for every morphism of rigid spaces $Z \to Y$ over $K$, the projection $X \times_Y Z \to Z$ is closed.

>[!notes]+ Def 23.9
>
> A morphism $f: X \to Y$ of rigid analytic spaces over $K$ is proper if it is separated and universally closed.

>[!notes]+ Def 23.10
>
> A morphism $f: X \to Y$ of rigid analytic spaces over $K$ is unramified (resp. smooth, étale) if for any affinoid $K$-algebra $A$ and any ideal $I$ of $A$ with $I^2 = 0$, and any morphism $\mathrm{Spa}(A,A^\circ) \to Y$, the natural map
> $$
> \mathrm{Hom}_Y(\mathrm{Spa}(A,A^\circ),X) \to \mathrm{Hom}_Y(\mathrm{Spa}(A/I,(A/I)^\circ),X)
> $$
> is injective (resp. surjective, bijective).

>[!abstract]+ Prop 23.11
>
> Let $A$ be an affinoid algebra, and let $f: X \to \mathrm{Spa}(A,A^\circ)$ be a morphism of rigid analytic spaces. Then $f$ is smooth if and only if, for every $x \in X$, there exists an open neighborhood $U$ of $x$ and a commutative diagram
> 
> ```tikz
> \usepackage{tikz-cd}
> \usepackage{amssymb}
> 
> \begin{document}
> \begin{tikzcd}
> 
>&  {\mathbb{A}^n_A} \arrow[rd, "\mathrm{pr}"]  & \\
>U \arrow[ru, "g"] \arrow[rr, "f|_U"] &   & {\mathrm{Spa}(A,A^\circ)}
>
>\end{tikzcd}
>
>\end{document}
>```
>
> such that $g$ is étale.
>
>> *Proof.* See [Hub96, Corollary 1.6.10].

Rigid analytic spaces are similar to complex manifolds in some regard, but they are not sufficient for a satisfactory theory of $p$-adic geometry. A complex manifold can be built from unit balls, which are contractible. But the $p$-adic unit disc is not simply connected: the map $z \mapsto z - z^p$ is a $p$-fold cover of the unit disc by itself. To get a better theory, we need to consider perfectoid spaces.

>[!notes]+ Def 23.12
>
> A complete Tate ring $R$ is perfectoid if $R$ is uniform and there exists a topologically nilpotent unit $\varpi$ such that $\varpi^p \mid p$ in $R^\circ$, and the Frobenius map
> $$
> \Phi: R^\circ/\varpi \to R^\circ/\varpi^p
> $$
> is an isomorphism.

>[!tip]+ Lemma 23.13
>
> A complete Tate ring $R$ is perfectoid iff $R$ is uniform, there exists a topologically nilpotent unit $\varpi$ such that $\varpi^p \mid p$ in $R^\circ$, and the Frobenius map $\Phi: R^\circ/p \to R^\circ/p$ is surjective.
>
>> *Proof.* We first show that $\Phi: R^\circ/\varpi \to R^\circ/\varpi^p$ is always injective. Suppose that $x \in R^\circ$ satisfies $x^p \in \varpi^p R^\circ$. Then $(x/\varpi)^p \in R^\circ$, so $x/\varpi \in R^\circ$ as well.
>> 
>> It is clear that if $\Phi$ is surjective mod $p$, then it is also surjective mod $\varpi^p$. Conversely, if it is surjective mod $\varpi^p$, then by successive approximation we can write $x \in R^\circ$ as $x_0^p + \varpi^p x_1^p + \varpi^{2p} x_2^p + \cdots$; then $(x_0 + \varpi x_1 + \varpi^2 x_2 + \cdots)^p$ is congruent to $x$ mod $p$.

>[!example]+ ex 23.14
>
> The following rings are perfectoid:
> 1. $K = \widehat{\mathbb{Q}_p(p^{1/p^\infty})}$, since $K^\circ/p \cong \mathbb{F}_p[T^{1/p^\infty}]/(T)$ via $p \mapsto T^{1/p^n} \bmod T$.
> 2. $K = \mathbb{Q}_p^{\mathrm{cyc}}$, the completion of $\mathbb{Q}_p(\mu_{p^\infty})$, since $K^\circ/p \cong \mathbb{F}_p[T^{1/p^\infty}]/(T^{1-1/p})$ via $\zeta_{p^n} \mapsto 1 + T^{1/p^n} \bmod T^{1-1/p}$.
> 3. $K = \mathbb{F}_p((T^{1/p^\infty}))$, the completion of $\mathbb{F}_p((T))(T^{1/p^\infty})$
> 4. $\mathbb{Q}_p^{\mathrm{cyc}}\langle T^{1/p^\infty}\rangle$, which is constructed by taking the $p$-adic completion of $\mathbb{Z}_p[T^{1/p^\infty}]$ and inverting $p$.

>[!abstract]+ Prop 23.15
>
> Let $R$ be a Tate ring, and suppose that $p = 0$ in $R$. Then the following are equivalent:
> 1. $R$ is perfectoid
> 2. $R$ is perfect (Frobenius is an isomorphism) and complete.
>
>> *Proof.* Suppose $R$ is perfectoid. Then $R$ is uniform and since $R^\circ = R^\circ/p$, $\Phi: R^\circ \to R^\circ$ is surjective. Then $\Phi: R \to R$ is surjective. Since $R$ is uniform, $\Phi: R \to R$ is injective.

Now assume that $R$ is a perfect complete Tate ring. Let $R_0$ be a ring of definition. By the Banach open mapping theorem, $\Phi(R_0)$ is open in $R_0$. (Note that we can make $\Phi$ linear by an appropriate choice of an $R$-module structure on the target.) So we can find a pseudouniformizer $\varpi$ so that $\varpi R_0 \subset \Phi(R_0)$. Then $\Phi^{-1}(R_0) \subset \varpi^{-1/p} R_0$, $\Phi^{-2}(R_0) \subset \varpi^{-1/p-1/p^2} R_0$, etc., so $R_0' := \bigcup_n \Phi^{-n} R_0$ is bounded; hence it is a ring of definition. Moreover, $R$ is bounded since $R^\circ \subseteq \varpi^{-1} R^\circ \subseteq \varpi^{-1} R_0'$.

>[!tip]+ Lemma 23.16
>
> Let $(R,R^+)$ be a perfectoid Huber pair, and let $X = \mathrm{Spa}(R,R^+)$ For any rational subset $U$, $\mathcal{O}_X(U)$ is again perfectoid. Therefore $(R,R^+)$ is stably uniform, hence sheafy.

>[!notes]+ Def 23.17
>
> Let $R$ be a perfectoid Tate ring. The tilt of $R$ is
> $$
> R^\flat := \varprojlim_{x\mapsto x^p} R.
> $$
>
> We define a ring structure on $R$ as follows. Multiplication is defined in the obvious way. Addition is defined by
> $$
> (x^{(0)},x^{(1)},\dots) + (y^{(0)},y^{(1)},\dots) = (z^{(0)},z^{(1)},\dots)
> $$
> where
> $$
> z^{(i)} = \lim_{n\to\infty} (x^{(i+n)} + y^{(i+n)})^{p^n}.
> $$

>[!tip]+ Lemma 23.18
>
> The above limit exists, and $R^\flat$ is a topological $\mathbb{F}_p$-algebra that is a complete Tate ring. The subring $R^{\flat\circ}$ of power-bounded elements is given by
> $$
> R^{\flat\circ} = \varprojlim_{x\mapsto x^p} R^\circ \cong \varprojlim_{\Phi} R^\circ/p \cong \varprojlim_{\Phi} R^\circ/\varpi
> $$
> where $\varpi$ is a pseudouniformizer that divides $p$ in $R^\circ$.
>
> Furthermore, there exists a pseudouniformizer $\varpi \in R^\circ$ with $\varpi \mid \pi \in R^\circ$ admitting a compatible sequence of $p$th power roots $\varpi^{1/p^n}$. Then $\varpi^\flat = (\varpi,\varpi^{1/p},\dots)$ is a pseudouniformizer of $R^\flat$, and $R^\flat = R^{\flat\circ}[1/\varpi^\flat]$.
>
>> *Proof.* The key step is to check that $\varprojlim_{x\mapsto x^p} R^\circ \to \varprojlim_{\Phi} R^\circ/p$ is a bijection. Suppose we have a sequence $(\bar{x}_0,\bar{x}_1,\dots) \in \varprojlim_{\Phi} R^\circ/p$, choose any lift $(y_0,y_1,\dots) \in (R^\circ)^\mathbb{N}$, and let $x_i = \lim_{n\to\infty} y_{i+n}^{p^n}$. Note that if $y \equiv y' \pmod{p}$, then $y^{p^n} \equiv y'^{p^n} \pmod{p^{n+1}}$. So the $x_i$ do not depend on the choice of $y_i$, and $x_{i+1}^p = x_i$ for each $i$.
>> 
>> Let $\varpi_0$ be a pseudouniformizer of $R$ satisfying $\varpi_0^p \mid p$ in $R^\circ$. Since $R$ is perfectoid, we can find $(\bar{x}_0,\bar{x}_1,\dots) \in \varprojlim_{\Phi} R^\circ/p$ with $\bar{x}_0 = \varpi_0 \bmod \varpi_0^p$. Let $\varpi^\flat$ be the corresponding element $R^{\flat\circ}$; it is a pseudouniformizer and $\varpi := \varpi^{\flat\sharp}$ is the desired pseudouniformizer of $R$.

>[!tip]+ Lemma 23.19
>
> The set of rings of integral elements $R^+ \subset R^\circ$ is in bijection with the set of rings of integral elements $R^{\flat+} \subset R^{\flat\circ}$ via $R^{\flat+} = \varprojlim_{x\mapsto x^p} R^+$. Also, $R^{\flat+}/\varpi^\flat = R^+/\varpi$.

>[!danger]+ Them 23.20
>
> Let $(R,R^+)$ be a perfectoid Huber pair, with tilt $(R^\flat,R^{\flat+})$. The map $\sharp: R^\flat \to R$ induces a homeomorphism $X := \mathrm{Spa}(R,R^+) \cong X^\flat := \mathrm{Spa}(R^\flat,R^{\flat+})$. This homeomorphism preserves rational subsets. For any rational subset $U \subset X$ with image $U^\flat \subset X^\flat$, $\mathcal{O}_X(U)$ is perfectoid with tilt $\mathcal{O}_{X^\flat}(U^\flat)$.

>[!danger]+ Them 23.21
>
> Let $R$ be a perfectoid ring with tilt $R^\flat$. Then there is an equivalence of categories between perfectoid $R$ algebras and perfectoid $R^\flat$-algebras, via $S \mapsto S^\flat$.

>[!notes]+ Def 23.22
>
> Let $(R,R^+)$ be a perfectoid Huber pair in characteristic $p$. An element $\xi \in W(R^+)$ is primitive of degree one if $\xi = p + [\varpi]\alpha$, where $\varpi \in R^+$ is a pseudouniformizer.

>[!tip]+ Lemma 23.23
>
> Let $(R,R^+)$ be a perfectoid Huber pair in characteristic $p$. Let $(R^\sharp,R^{\sharp+})$ be an untilt of $(R,R^+)$, i.e. a perfectoid Tate ring $R^\sharp$ along with an isomorphism $R^{\sharp\flat} \xrightarrow{\sim} R$ identifying $R^{\sharp+}$ with $R^+$.
> 1. There is a canonical surjective ring homomorphism
> $$
> \theta: W(R^+) \to R^{\sharp+}
> $$
> $$
> \sum_{n=0}^\infty [r_n]p^n \mapsto \sum_{n\geq 0} r_n^{\sharp} p^n.
> $$
> 2. The kernel of $\theta$ is generated by an element $\xi$ that is primitive of degree one.

>[!tip]+ Lemma 23.24
>
> A primitive degree one element of $W(R^+)$ is not a zero divisor.

>[!danger]+ Them 23.25
>
> There is an equivalence of categories between:
> 1. Perfectoid Tate-Huber pairs $(S,S^+)$
> 2. Triples $(R,R^+,J)$, where $(R,R^+)$ is a perfectoid Tate-Huber pair of characteristic $p$ and $J \subset W(R^+)$ is primitive of degree 1. The functors are
> $$
> (S,S^+) \mapsto (S^\flat,S^{\flat+},\ker \theta)
> $$
> $$
> (R,R^+,J) \mapsto (W(R^+)[[\varpi]^{-1}]/J,W(R^+)/J)
> $$

>[!notes]+ Def 23.26
>
> Let $R$ be a complete Tate $\mathbb{Z}_p$-algebra. We say that $R$ is sousperfectoid if there exists a perfectoid Tate ring $\tilde{R}$ and an injection $R \hookrightarrow \tilde{R}$ that splits as a map of topological $R$-modules.

>[!example]+ ex 23.27
>
> 1. Any perfectoid ring is sousperfectoid.
> 2. The ring $R = \mathbb{Q}_p\langle T\rangle$ is sousperfectoid, by taking $\tilde{R} = \mathbb{Q}_p^{\mathrm{cyc}}\langle T^{1/p^\infty}\rangle$.
> 3. Similarly, $\mathbb{Q}_p\langle T^{1/p^\infty}\rangle$ is sousperfectoid.

>[!abstract]+ Prop 23.28
>
> Let $R$ be a complete Tate $\mathbb{Z}_p$-algebra with a ring of integral elements $R^+ \subset R$, and assume that $R$ is sousperfectoid.
> 4. If $U \subset X = \mathrm{Spa}(R,R^+)$ is a rational subset, then $\mathcal{O}_X(U)$ is sousperfectoid.
> 5. If $S$ is a finite étale $R$-algebra, then $S$ is sousperfectoid.
> 6. For all $n \geq 0$, the ring $R\langle T_1,\dots,T_n\rangle$ is sousperfectoid.

>[!abstract]+ Prop 23.29
>
> Let $(R,R^+)$ be a Tate-Huber pair such that $(R,R^+)$ is sousperfectoid. Then $(R,R^+)$ is stably uniform, hence sheafy.
