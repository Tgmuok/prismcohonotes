Étale cohomology is supposed to be an analogue of singular cohomology for more general kinds of spaces. To define étale cohomology, we need to use sites.

> [!notes]+ Def 18.1
> 
> A site is a category $\mathcal{C}$ along a set $\operatorname{Cov}(\mathcal{C})$ of morphisms with fixed target $\{U_i \to U\}_{i\in I}$, satisfying the following axioms:
> 
> (1) If $V \to U$ is an isomorphism then $\{V \to U\} \in \operatorname{Cov}(\mathcal{C})$.
> (2) If $\{U_i \to U\}_{i\in I} \in \operatorname{Cov}(\mathcal{C})$ and for each $i \in I$, $\{V_{ij} \to U_i\}_{j\in J_i} \in \operatorname{Cov}(\mathcal{C})$, then $\{V_{ij} \to U\}_{i\in I,j\in J_i} \in \operatorname{Cov}(\mathcal{C})$.
> (3) If $\{U_i \to U\}_{i\in I} \in \operatorname{Cov}(\mathcal{C})$ and $V \to U$ is a morphism in $\mathcal{C}$, then for all $i \in I$, $U_i \times_U V$ exists, and $\{U_i \times_U V\}_{i\in I} \in \operatorname{Cov}(\mathcal{C})$

For any topological space $X$, we can define a site by taking $\mathcal{C}$ to be the category of open sets of $X$ and coverings to be open coverings in the usual sense. Note that the fiber product is just intersection.

Now let $X$ be a scheme. Recall that a morphism of schemes $Y \to Z$ is called étale if it is smooth of relative dimension 0. Define the small étale site $X_{\text{ét}}$ as follows. The underlying category is the category of étale morphisms $U \to X$. A collection $U_i \to X$ is a covering if the images of the $U_i$ cover $X$. (There is also a big étale site, where the category includes all schemes over $X$, but morphisms are still jointly surjective collections of étale maps.)

Sheaves and cohomology can be defined on any site. One can show that if $X$ is an algebraic variety over $\mathbb{C}$, then for any $N$,

$$
H^i(X(\mathbb{C}), \mathbb{Z}/N\mathbb{Z}) \cong H^i(X_{\text{ét}}, \mathbb{Z}/N\mathbb{Z}) .
$$

The reason that we need to use $\mathbb{Z}/N\mathbb{Z}$ coefficients is that finite covers of $X(\mathbb{C})$ are in bijection with finite covers of $X$, but the same is not true of infinite covers. To deal with this issue, we define

$$
H_{\text{ét}}^i(X, \mathbb{Z}_p) = \varprojlim_n H^i(X, \mathbb{Z}/p^n\mathbb{Z})
$$

$$
H_{\text{ét}}^i(X, \mathbb{Q}_p) = H^i(X, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} \mathbb{Q}_p
$$

for any algebraic variety $X$. Using this definition, if $X$ is an algebraic variety over $\mathbb{C}$, then

$$
H^i(X(\mathbb{C}), \mathbb{Z}_p) \cong H^i(X_{\text{ét}}, \mathbb{Z}_p) .
$$

$$
H^i(X(\mathbb{C}), \mathbb{Q}_p) \cong H^i(X_{\text{ét}}, \mathbb{Q}_p) .
$$

Normally, we consider cohomology of varieties over an algebraically closed field, as the notion of cohomology most closely matches our geometric intuition in that case. For example, if $K$ is a field, then

$$
H^i((\operatorname{Spec} K)_{\text{ét}}, \Lambda) = H_{\text{cts}}^i(\operatorname{Gal}(K^{\text{sep}}/K), \Lambda) .
$$

So the cohomology of the spectrum of a non-algebraically closed field can be quite complicated.

If $X$ is a variety over a field $K$ (that is not necessarily algebraically closed), then we can consider the cohomology groups $H^i(X_{K^{\text{sep}},\text{ét}}, \Lambda)$, and these have a $\operatorname{Gal}(K^{\text{sep}}/K)$ action.

The cohomology $H^i(X_{\text{ét}}, \Lambda)$ (without the base change to $K^{\text{sep}}$) is sometimes useful. See for example [LZ] for an application to Euler systems.

Actually, there is a way to define $H_{\text{ét}}^i(X, \mathbb{Z}_p)$ as cohomology on an actual site, called the "proétale site". A morphism of schemes $f: X \to Y$ is called weakly étale if $f$ and $\Delta_f: X \to X \times_Y X$ are both flat. Coverings in the proétale site are defined to be collections of weakly étale maps $X_i \to Y$ such that for each affine open $V \subset Y$, there is a finite collection of affine opens $U_i \subset X_i$ whose images cover $V$. Then

$$
H_{\text{ét}}^i(X, \mathbb{Z}_p) = H^i(X_{\text{proét}}, \mathbb{Z}_p) .
$$

The site is called the "proétale site" because, if we have a tower

$$
\cdots \to X_2 \to X_1 \to X
$$

of schemes with étale and affine transition maps, then the projection

$$
\varprojlim_i X_i \to X
$$

is weakly étale. It turns out that the property of being proétale is not local, so it's better to use the property of being weakly étale for defining a site.

If $X$ is an algebraic variety over a $p$-adic field $K$, we now know the definitions of the objects appearing in the de Rham comparison isomorphism

$$
H_{\text{dR}}^i(X) \otimes_K B_{\text{dR}} \cong H_{\text{ét}}^i(X_{\overline{K}}, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} B_{\text{dR}} .
$$

(However, proving the theorem requires getting much deeper in to $p$-adic geometry.)
