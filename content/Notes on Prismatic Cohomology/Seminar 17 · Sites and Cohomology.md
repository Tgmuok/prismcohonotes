Recall that in the first lecture, we considered an isomorphism between the singular and de Rham cohomologies of a complex manifold. This isomorphism can be understood in terms of sheaf cohomology.

>[!notes]+ Def 1 (Presheaf & Sheaf)
>
> Let $X$ be a complex manifold. A presheaf of sets on $X$ is a contravariant functor $\mathcal{F}$ from the category of open subsets of $X$ to the category of sets. We say that $\mathcal{F}$ is a sheaf if for every open $U \subset X$ and every covering $U = \bigcup_{i \in I} U_i$,
>
> $$
> \mathcal{F}(U) \longrightarrow \prod_{i \in I} \mathcal{F}(U_i) \rightrightarrows \prod_{i,j \in I} \mathcal{F}(U_i \cap U_j)
> $$
>
> is an equalizer diagram. In other words, $\mathcal{F}(U)$ is the subset of $\prod_{i \in I} \mathcal{F}(U_i)$ such that for each $i,j \in I$, the projections to $\mathcal{F}(U_i)$ and $\mathcal{F}(U_j)$ have the same image in $\mathcal{F}(U_i \cap U_j)$. A morphism of (pre)sheaves $\mathcal{F} \to \mathcal{G}$ is a natural transformation of functors.

The categories of sheaves and presheaves of abelian groups on $X$ are defined similarly. They are abelian categories.

>[!notes]+ Def 2 (Injective Sheaf & Injective Resolution)
>
> A sheaf $\mathcal{I}$ of abelian groups on $X$ is called *injective* if the functor $\operatorname{Hom}(-,\mathcal{I})$ is exact. An *injective resolution* of a sheaf $\mathcal{F}$ of abelian groups on $X$ is a long exact sequence
>
> $$
> 0 \to \mathcal{F} \to \mathcal{I}_0 \to \mathcal{I}_1 \to \cdots
> $$
>
> where $\mathcal{I}_0,\mathcal{I}_1,\dots$ are injective sheaves.

>[!abstract]+ Prop 1 (Existence of Injective Resolution)
>
> It can be shown that every sheaf of abelian groups on $X$ admits an injection into an injective sheaf. This implies that every sheaf of abelian groups on $X$ admits an injective resolution.

>[!notes]+ Def 3 (Sheaf Cohomology)
>
> The cohomology groups $H^n(X,\mathcal{F})$ are defined by the cohomology groups of the complex
>
> $$
> 0 \to \mathcal{I}_0(X) \to \mathcal{I}_1(X) \to \cdots .
> $$
>
> This definition is independent of the injective resolution chosen.

>[!notes]+ Def 4 (Acyclic Sheaf)
>
> A sheaf $\mathcal{G}$ is called *acyclic* if $H^n(X,\mathcal{G}) = 0$ for all $n > 0$.

>[!abstract]+ Prop 2 (Acyclic Resolution for Sheaf Cohomology)
>
> One can actually compute the cohomology groups $H^n(X,\mathcal{F})$ using any resolution of $\mathcal{F}$ by acyclic sheaves.

>[!danger]+ Them 1 (Singular Cohomology ≅ Sheaf Cohomology)
>
> For any complex manifold $X$ and any ring $A$, the complex of singular cochains on $X$ is an acyclic resolution of the constant sheaf $A$. So
>
> $$
> H^i_{\mathrm{sing}}(X,A) = H^i_{\mathrm{sheaf}}(X,A) .
> $$

---

>[!notes]+ Def 5 (Hypercohomology)
>
> If $C^\bullet$ is a complex of sheaves on $X$, then an injective (resp. acyclic) of $C^\bullet$ is a quasi-isomorphism of complexes $C^\bullet \to \mathcal{I}^\bullet$, where the objects of $\mathcal{I}^\bullet$ are injective (resp. acyclic). (A quasi-isomorphism of complexes is a morphism that induces an isomorphism on cohomology.) Then the hypercohomology of $H^*(X,C^\bullet)$ is defined to be the cohomology of the complex
>
> $$
> 0 \to \mathcal{I}_0(X) \to \mathcal{I}_1(X) \to \cdots .
> $$

>[!notes]+ Def 6 (de Rham Complex)
>
> The de Rham complex $\Omega_X^\bullet$ is the complex
>
> $$
> 0 \to \mathcal{O}_X \xrightarrow{d} \Omega^1_{X/\mathbb{C}} \xrightarrow{d} \cdots \xrightarrow{d} \Omega^n_{X/\mathbb{C}} \to 0 .
> $$

If $X$ is an open subset of $\mathbb{C}^n$, then the $\Omega^i_{X/\mathbb{C}}$ are already acyclic. We implicitly used this fact in the first lecture when computing the de Rham cohomology of $\mathbb{C}^\times$.

>[!notes]+ Def 7 (Analytic de Rham Cohomology)
>
> The analytic de Rham cohomology of $X$ is defined to be the hypercohomology of $\Omega_X^\bullet$.

>[!danger]+ Them 2 (Poincaré Lemma & Analytic de Rham Theorem)
>
> The Poincaré lemma states that $\mathbb{C}[0] \to \Omega_X^\bullet$ is a quasi-isomorphism. Therefore,
>
> $$
> H^i_{\mathrm{dR}}(X) = H^i_{\mathrm{sheaf}}(X,\mathbb{C}) .
> $$

>[!notes]+ Def 8 (Algebraic de Rham Cohomology)
>
> If $X$ is a smooth algebraic variety over a field $K$, then we can define the algebraic de Rham cohomology similarly.

>[!danger]+ Them 3 (GAGA Isomorphism for de Rham Cohomology)
>
> If $X$ is a proper variety over $\mathbb{C}$, then there is an isomorphism
>
> $$
> H^i_{\mathrm{dR}}(X) \cong H^i_{\mathrm{dR}}(X(\mathbb{C})),
> $$
>
> where $X(\mathbb{C})$ is considered as a complex analytic space.

>[!abstract]+ Prop 3 (Failure of Algebraic Poincaré Lemma)
>
> However, the Poincaré lemma does not hold for the algebraic de Rham complex: $K[0] \to \Omega_{X/K}^\bullet$ is generally not a quasi-isomorphism. For example, if $X = \mathbb{A}^1_K \setminus \{0\}$, then $\frac{dz}{z}$ does not have an antiderivative locally in the Zariski topology. The cohomology $H^i(X,K)$ is not very interesting: it is zero if $i > 0$.

>[!abstract]+ Prop 4 (Čech–de Rham Complex for Algebraic de Rham Cohomology)
>
> In practice, we usually use Čech cohomology to compute de Rham cohomology. If $X$ is an affine algebraic variety, then the sheaves $\Omega^i_{X/K}$ are acyclic. More generally, if $X$ is a separated algebraic variety, then we can write $X$ as a finite union $X = \bigcup_{i \in I} X_i$, where the $X_i$'s are affine, and the intersections of the $X_i$'s are also affine. Define a complex $C^\bullet$ as follows. Let
>
> $$
> C^n = \bigoplus_{J \subset I} \Omega^{n-|J|} \left( \bigcap_{j \in J} X_j \right) .
> $$
>
> Given $\omega \in \Omega^{n-|J|} \left( \bigcap_{j \in J} X_j \right)$, the $\Omega^{n+1-|J|} \left( \bigcap_{j \in J} X_j \right)$-part of its differential is $d\omega$. Choose an ordering of $I$. If $i \notin J$, then the $\Omega^{n+1-|J \cup \{i\}|} \left( \bigcap_{j \in J \cup \{i\}} X_j \right)$-part of the differential of $\omega$ is $(-1)^{n+|\{j \in J | j < i\}|}$ times the restriction of $\omega$. All other parts are zero. Then the de Rham cohomology of $X$ is the cohomology of $C^\bullet$.
