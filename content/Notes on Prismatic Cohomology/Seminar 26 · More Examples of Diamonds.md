>[!notes]+ Def 26.1
>
> Let $X$ be an analytic adic space over $\mathrm{Spa}(\mathbb{Z}_p, \mathbb{Z}_p)$. Define a presheaf $X^\diamondsuit$ on $\mathrm{Perf}$ as follows. For $Y \in \mathrm{Perf}$, let $X^\diamondsuit(Y)$ be the set of isomorphism classes of triples $(Y^\sharp, (Y^\sharp)^\flat \xrightarrow{\sim} Y, Y^\sharp \to X)$, where $Y^\sharp$ is a perfectoid space.

>[!danger]+ Them 26.2
>
> $X^\diamondsuit$ is a diamond.

A key lemma in the proof is the following.

>[!tip]+ lemma 26.3
>
> Let $R$ be a Tate $\mathbb{Z}_p$-algebra. Let $R_\infty := \varinjlim_i R_i$ be a filtered direct limit of algebras $R_i$ finite étale over $R$, that admits no nonsplit finite étale covers. Give $R_\infty$ the topology making $\varinjlim_i R_i^\circ$ open and bounded. Let $\tilde{R}$ be the completion of $R_\infty$. Then $\tilde{R}$ is perfectoid.
>
>> *Proof.* First, find a pseudouniformizer $\varpi \in \tilde{R}$ satisfying $\varpi^p \mid p$. Let $\varpi_0$ be a pseudouniformizer of some $R_i$. For some integer $N$, $\varpi_0 \mid p^N$ in $\tilde{R}^\circ$. We can find $\varpi \in \tilde{R}^\circ$ satisfying $\varpi^{p^N} - \varpi_0 \varpi = \varpi_0$; then $\varpi^{p^N} \mid \varpi_0$ in $\tilde{R}^\circ$.
>>
>> It remains to check that $\tilde{R}^\circ / \varpi \to \tilde{R}^\circ / \varpi^p$ is surjective. Observe that for any $f \in R_i^\circ$, the equation $x^p - \varpi^p x - f = 0$ has a solution in $\tilde{R}$.

>[!notes]+ Def 26.4
>
> A ring $A$ is seminormal if the map $A \to \{(x,y) \in A^2 | y^2 = x^3\}$ given by $t \mapsto (t^2, t^3)$ is a bijection.
>
> A rigid analytic space is seminormal if it is locally of the form $\mathrm{Spa}(A, A^+)$ with $A$ seminormal.

>[!abstract]+ Prop 26.5
>
> For any nonarchimedean field $K$ over $\mathbb{Q}_p$, the functor
> $$
> \{\text{seminormal rigid analytic spaces}/K\} \to \{\text{diamonds}/\mathrm{Spd}\, K\}
> $$
> $$
> X \mapsto X^\diamondsuit
> $$
> is fully faithful.

>[!example]+ ex 26.6
>
> Here are some examples of morphisms of rigid spaces that induce isomorphisms of diamonds:
> 1. Frobenius, if $K$ has characteristic $p$.
> 2. $X^\mathrm{red} \to X$ for any rigid space $X$, since perfectoid rings do not have nilpotents.
> 3. $\mathbb{A}^1 \to Y$, where $Y$ is the cuspidal cubic. To prove this, one uses the fact that a qcqs map of diamonds is an isomorphism iff it induces a bijection on $(K, K^+)$ points for every $(K, K^+)$.

>[!notes]+ Def 26.7
>
> Let $D$ be a diamond, and choose a presentation $D = X/R$. The underlying topological space of $D$ is the quotient $|D| = |X|/|R|$.
>
> It can be shown that this definition is independent of the presentation.

>[!abstract]+ Prop 26.8
>
> If $X$ is an analytic adic space over $\mathbb{Z}_p$, then there is a natural homeomorphism $|X| \cong |X^\diamondsuit|$.

>[!example]+ ex 26.9
>
> Let $\mathrm{Spd}\,\mathbb{Z}_p$ be the presheaf that sends $Y \in \mathrm{Perf}$ to the set of isomorphism classes of pairs $(Y^\sharp, (Y^\sharp)^\flat \xrightarrow{\sim} Y)$. Then $\mathrm{Spd}\,\mathbb{Z}_p$ is not a diamond (because $\mathbb{Z}_p$ is not an analytic Huber ring). But it is a sheaf. Moreover, it turns out that $\mathrm{Spd}\,\mathbb{Z}_p$ is an "absolute diamond": its product with any diamond is again a diamond. In a later lecture, we construct, for any $S \in \mathrm{Perf}$, an analytic adic space whose diamond is $\mathrm{Spd}\,\mathbb{Z}_p \times S$.

>[!example]+ ex 26.10
>
> Let $X_i$ be a directed system of rigid spaces with qcqs transition maps. Then $\varinjlim_i X_i^\diamondsuit$ is a diamond.

>[!notes]+ Def 26.11
>
> For each $n$, the define the sheaf $B^+_{\mathrm{dR}} / \mathrm{Fil}^n$ on $\mathrm{Perf}$ as follows. Let $(R, R^+)$ be a perfectoid Huber-Tate pair in characteristic $p$. Then $B^+_{\mathrm{dR}} / \mathrm{Fil}^n (R, R^+)$ will be the set of isomorphism classes of pairs of an untilt $R^\sharp$ of $R$ and an element of $W(R^\circ)[1/p]/(\ker \theta)^n$ where $\theta: W(R^\circ)[1/p] \to R^\sharp$ is the obvious map.

>[!abstract]+ Prop 26.12
>
> $B^+_{\mathrm{dR}} / \mathrm{Fil}^n$ is a diamond.
>
>> *Proof.* Let $\widehat{\mathbb{G}_m}$ be the formal multiplicative group $(\widehat{\mathbb{G}_m}(R, R^+) = 1 + R^{\circ\circ})$, and let $\widetilde{\mathbb{G}_m}$ be its universal cover $(\widetilde{\mathbb{G}_m}(R, R^+) = \varprojlim_{x \mapsto x^p} 1 + R^{\circ\circ})$. Then $\widetilde{\mathbb{G}_m}^n \times \mathrm{Spa}\,\mathbb{Q}_p^{\mathrm{cyc}}$ is perfectoid, and $(\widetilde{\mathbb{G}_m}^n \times \mathrm{Spa}\,\mathbb{Q}_p^{\mathrm{cyc}})^\flat \cong \widetilde{\mathbb{G}_m}^n \times \mathrm{Spa}(\mathbb{Q}_p^{\mathrm{cyc}})^\flat$. There is a map $\widetilde{\mathbb{G}_m}^n \times \mathrm{Spa}(\mathbb{Q}_p^{\mathrm{cyc}})^\flat \to B^+_{\mathrm{dR}} / \mathrm{Fil}^n$ that sends $(z_0, z_1, \dots, z_{n-1}) \mapsto \sum_{i=0}^n (\log[z_i])(\log[\epsilon])^i \in B^+_{\mathrm{dR}} / \mathrm{Fil}^n$. The map is pro-étale. To see this, recall that $\log: (\widehat{\mathbb{G}_m})_{\mathbb{Q}_p} \to \mathbb{A}^1_{\mathbb{Q}_p}$ is an étale covering with Galois group $\mathbb{Q}_p/\mathbb{Z}_p$, and $(\widetilde{\mathbb{G}_m})_{\mathbb{Q}_p} \to (\widehat{\mathbb{G}_m})_{\mathbb{Q}_p}$ is an étale covering with Galois group $\mathbb{Z}_p$, so $(\widetilde{\mathbb{G}_m})_{\mathbb{Q}_p}$ is a $\mathbb{Q}_p$-torsor over $\mathbb{A}^1_{\mathbb{Q}_p}$.

>[!example]+ ex 26.13
>
> Here is an example of a diamond that is not of the form $X^\diamondsuit$. Let $T$ be a compact Hausdorff space, and let $\underline{T}$ be the functor on $\mathrm{Perf}$ that sends $X$ to the set of continuous maps $|X| \to T$. We claim that for any perfectoid field $K$ of characteristic $p$, $\underline{T} \times \mathrm{Spa}(K, \mathcal{O}_K)$ is a diamond. If $T$ is profinite, then $\underline{T} \times \mathrm{Spa}(K, \mathcal{O}_K)$ is perfectoid. In general, $T$ admits a surjection from a profinite set $S$ (take the Stone-Cech compactification of $T$ considered as a discrete set). The equivalence relation $R = S \times_T S$ is a closed subspace of $S \times S$, so it is also profinite. One can check that $\underline{R} \times \mathrm{Spa}(K, \mathcal{O}_K) \rightrightarrows \underline{S} \times \mathrm{Spa}(K, \mathcal{O}_K)$ is pro-étale, and $\underline{T} \times \mathrm{Spa}(K, \mathcal{O}_K)$ is isomorphic to the quotient $(\underline{S} \times \mathrm{Spa}(K, \mathcal{O}_K))/(\underline{R} \times \mathrm{Spa}(K, \mathcal{O}_K))$. The underlying topological space of $\underline{T} \times \mathrm{Spa}(K, \mathcal{O}_K)$ is $T$. The underlying topological space of any diamond of the form $X^\diamondsuit$ is a locally spectral space. So $\underline{T} \times \mathrm{Spa}(K, \mathcal{O}_K)$ is of the form $X^\diamondsuit$ iff $T$ is profinite.
