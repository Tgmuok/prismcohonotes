As before, let $E$ be a field of characteristic $p$. We will now turn our attention to $\mathbb{Z}_p$-representations of $G_E$. Let $\operatorname{Rep}_{\mathbb{Z}_p} G_E$ denote the category of finitely generated (not necessarily free) $\mathbb{Z}_p$-modules with continuous $G_E$-action.

>[!notes]+ Def 9.1
>
> Let $E$ be a field of characteristic $p$. A Cohen ring for $E$ is a complete discrete valuation ring $\mathcal{O}_\mathcal{E}$ such that the residue field of $\mathcal{O}_\mathcal{E}$ is $E$, and $p$ is a uniformizer of $\mathcal{O}_\mathcal{E}$.

>[!danger]+ Them 9.2 ([Mat86, Theorems 29.1 and 29.2])
>
> Any field $E$ of characteristic $p$ admits a Cohen ring $\mathcal{O}_\mathcal{E}$. The Cohen ring is unique up to isomorphism. The Frobenius automorphism of $E$ lifts to an automorphism of $\mathcal{O}_\mathcal{E}$.

>[!example]+ ex 9.3
>
> If $E = \mathbb{F}_{p^n}$, then $\mathcal{O}_\mathcal{E}$ is the ring of integers of $\mathbb{Q}_{p^n}$, the unramified extension of $\mathbb{Q}_p$ of degree $n$. More generally, if $E$ is perfect, then $\mathcal{O}_\mathcal{E} \cong W(E)$, the ring of $p$-typical Witt vectors over $E$. If $E = \mathbb{F}_p((T))$, then we can take
> $$
> \mathcal{O}_\mathcal{E} = \left\{ \sum_{n=-\infty}^\infty a_n T^n \,\bigg|\, a_n \in \mathbb{Z}_p,\ \lim_{n \to -\infty} a_n = 0 \right\}.
> $$
> A commonly used choice of Frobenius action is $T \mapsto (1+T)^p - 1$.

>[!tip]+ lemma 9.4
>
> There is an equivalence of categories between étale $E$-algebras and étale $\mathcal{O}_E$-algebras.

In particular, $E^{\text{sep}}$ is a direct limit of étale $E$-algebras. The corresponding direct limit of étale $\mathcal{O}_E$-algebras is called $\mathcal{O}_E^{\text{sh}}$, the strict Henselization of $\mathcal{O}_E$.

>[!notes]+ Def 9.5
>
> The category $\varphi\operatorname{-Mod}_{\mathcal{O}_\mathcal{E}}^{\text{ét}}$ of étale $\varphi$-modules over $\mathcal{O}_\mathcal{E}$ consists of pairs $(M, \varphi_M)$ where $M$ is a finitely generated $\mathcal{O}_\mathcal{E}$-module and $\varphi_M$ is a $\varphi$-semilinear endomorphism of $M$ such that $\varphi_{\mathcal{O}_\mathcal{E}}^*(M) \to M$ is an isomorphism.

>[!notes]+ Def 9.6
>
> Now let $\check{\mathcal{O}}_\mathcal{E} = \widehat{\mathcal{O}_\mathcal{E}^{\text{sh}}}$ be the completion of the strict henselization of $\mathcal{O}_\mathcal{E}$. There is a unique continuous Frobenius on $\check{\mathcal{O}}_\mathcal{E}$ that extends the Frobenius on $\mathcal{O}_\mathcal{E}$ and $E^{\text{sep}}$.

>[!danger]+ Them 9.7
>
> The functor $D_{\mathcal{O}_\mathcal{E}} : \operatorname{Rep}_{\mathbb{Z}_p} G_E \to \varphi\operatorname{-Mod}_{\mathcal{O}_\mathcal{E}}^{\text{ét}}$ defined by
> $$
> V \mapsto (V \otimes_{\mathbb{Z}_p} \check{\mathcal{O}}_\mathcal{E})^{G_E}
> $$
> and the functor $V_{\mathcal{O}_\mathcal{E}} : \varphi\operatorname{-Mod}_{\mathcal{O}_\mathcal{E}}^{\text{ét}} \to \operatorname{Rep}_{\mathbb{Z}_p} G_E$ defined by
> $$
> M \mapsto (M \otimes_{\mathcal{O}_\mathcal{E}} \check{\mathcal{O}}_\mathcal{E})^{\varphi=1}
> $$
> determine an equivalence of categories between $\operatorname{Rep}_{\mathbb{Z}_p} G_E$ and $\varphi\operatorname{-Mod}_{\mathcal{O}_\mathcal{E}}^{\text{ét}}$.

Finally, we consider $\mathbb{Q}_p$-representations of $G_E$. Let $\operatorname{Rep}_{\mathbb{Q}_p} G_E$ denote the category of finite-dimensional $\mathbb{Q}_p$-vector space representation of $G_E$. Let $\mathcal{E} := \mathcal{O}_\mathcal{E}[1/p], \check{\mathcal{E}} := \check{\mathcal{O}}_\mathcal{E}[1/p]$.

>[!notes]+ Def 9.8
>
> The category $\varphi\operatorname{-Mod}_\mathcal{E}^{\text{ét}}$ of étale $\varphi$-modules over $\mathcal{E}$ consists of pairs $(M, \varphi_M)$ where $M$ is a finite-dimensional $\mathcal{E}$-vector space and $\varphi_M$ is a $\varphi$-semilinear endomorphism of $M$ such that $\varphi_\mathcal{E}^*(M) \to M$ is an isomorphism, and $M$ admits a $\varphi_M$-stable $\mathcal{O}_\mathcal{E}$-lattice.

>[!danger]+ Them 9.9
>
> The functor $D_\mathcal{E} : \operatorname{Rep}_{\mathbb{Q}_p} G_E \to \varphi\operatorname{-Mod}_\mathcal{E}^{\text{ét}}$ defined by
> $$
> V \mapsto (V \otimes_{\mathbb{Q}_p} \check{\mathcal{E}})^{G_E}
> $$
> and the functor $V_\mathcal{E} : \varphi\operatorname{-Mod}_\mathcal{E}^{\text{ét}} \to \operatorname{Rep}_{\mathbb{Q}_p} G_E$ defined by
> $$
> M \mapsto (M \otimes_\mathcal{E} \check{\mathcal{E}})^{\varphi=1}
> $$
> determine an equivalence of categories between $\operatorname{Rep}_{\mathbb{Q}_p} G_E$ and $\varphi\operatorname{-Mod}_\mathcal{E}^{\text{ét}}$.

The Galois group $\operatorname{Gal}(\overline{\mathbb{Q}}_p/\mathbb{Q}_p)$ contains the closed normal subgroup $\operatorname{Gal}(\overline{\mathbb{Q}}_p/\mathbb{Q}_p(\mu_{p^\infty})) \cong \operatorname{Gal}(\mathbb{F}_p((t))^{\text{sep}}/\mathbb{F}_p((t)))$. Moreover, this isomorphism can be extended to a map
$$
\operatorname{Gal}(\overline{\mathbb{Q}}_p/\mathbb{Q}_p) \hookrightarrow \operatorname{Aut}(\mathbb{F}_p((t))^{\text{sep}}).
$$

This motivates us to consider the following setup.
Let $G$ be a profinite group containing $G_E$ as a closed normal subgroup. Let $\Gamma = G/G_E$. Suppose that we are given a continuous action of $\Gamma$ on $\mathcal{O}_\mathcal{E}$ that commutes with Frobenius. There is an induced action of $G$ on $\check{\mathcal{O}}_\mathcal{E}$ (again because compatible endomorphisms on $E^{\text{sep}}$ and $\mathcal{O}_\mathcal{E}$ extend uniquely to $\check{\mathcal{O}}_\mathcal{E}$).

>[!notes]+ Def 9.10
>
> A $(\varphi, \Gamma)$-module over $\mathcal{O}_\mathcal{E}$ is a $\varphi$-module over $\mathcal{O}_\mathcal{E}$ equipped with a semilinear $\Gamma$-action commuting with the $\varphi$-action. We say that a $(\varphi, \Gamma)$-module is étale if it is étale as a $\varphi$-module.

Write $(\varphi, \Gamma)\operatorname{-Mod}_{\mathcal{O}_\mathcal{E}}^{\text{ét}}$ for the category of étale $(\varphi, \Gamma)$-modules over $\mathcal{O}_\mathcal{E}$, and write $\operatorname{Rep}_{\mathbb{Z}_p} G$ for the category of finitely generated $\mathbb{Z}_p$-modules with $G$-action.

>[!danger]+ Them 9.11
>
> The functor $D_\mathcal{E} : \operatorname{Rep}_{\mathbb{Z}_p} G \to (\varphi, \Gamma)\operatorname{-Mod}_{\mathcal{O}_\mathcal{E}}^{\text{ét}}$ defined by
> $$
> V \mapsto (V \otimes_{\mathbb{Z}_p} \check{\mathcal{O}}_\mathcal{E})^{G_E}
> $$
> and the functor $V_\mathcal{E} : (\varphi, \Gamma)\operatorname{-Mod}_{\mathcal{O}_\mathcal{E}}^{\text{ét}} \to \operatorname{Rep}_{\mathbb{Z}_p} G$ defined by
> $$
> M \mapsto (M \otimes_{\mathcal{O}_\mathcal{E}} \check{\mathcal{O}}_\mathcal{E})^{\varphi=1}
> $$
> determine an equivalence of categories between $\operatorname{Rep}_{\mathbb{Z}_p} G$ and $(\varphi, \Gamma)\operatorname{-Mod}_{\mathcal{O}_\mathcal{E}}^{\text{ét}}$.

A similar result holds for $\mathbb{F}_p$- and $\mathbb{Q}_p$-representations.

>[!example]+ ex 9.12
>
> Let $G = G_{\mathbb{Q}_p}$, $E = \mathbb{F}_p((T))$, and embed $G$ in $\operatorname{Aut} E^{\text{sep}}$ using Theorem 8.1. We have $\Gamma = \operatorname{Gal}(\mathbb{Q}_p(\mu_{p^\infty})/\mathbb{Q}_p) \cong \mathbb{Z}_p^\times$. The action of $\Gamma$ on $\mathbb{F}_p((T))$ is given by
> $$
> \gamma \cdot T = (1+T)^\gamma - 1.
> $$
> The action of $\Gamma$ on $\mathcal{O}_\mathcal{E}$ can then also be taken to be $\gamma \cdot T = (1+T)^\gamma - 1$.

We have claimed that $\mathbb{Q}_p(\mu_{p^\infty})$ and $\mathbb{F}_p((t))$ have isomorphic Galois groups. To prove the isomorphism, we will make use of the concept of perfectoid fields and the tilting correspondence.

Recall that a nonarchimedean field $K$ is a field that is complete with respect to a nontrivial nonarchimedean absolute value $|\cdot|$, and that we write
$$
\mathcal{O}_K := \{ x \in K \mid |x| \leq 1 \}
$$
$$
\mathfrak{m}_K := \{ x \in K \mid |x| < 1 \}.
$$

>[!notes]+ Def 9.13
>
> A nonarchimedean field $K$ of residue characteristic $p$ is perfectoid if its value group is nondiscrete and the Frobenius map
> $$
> \Phi : \mathcal{O}_K / p \to \mathcal{O}_K / p
> $$
> is surjective.

**Remark 9.14.** Like most references but unlike [Ked15], we do not require that $K$ have characteristic zero.

>[!example]+ ex 9.15
>
> - The field $\mathbb{C}_p$ is perfectoid. More generally, any complete algebraically closed nonarchimedean field of residue characteristic $p$ is perfectoid.
> - A nonarchimedean field of characteristic $p$ is perfectoid if and only if it is perfect.

>[!tip]+ lemma 9.16
>
> The field $\mathbb{Q}_p^{\text{cyc}} := \widehat{\mathbb{Q}_p(\mu_{p^\infty})}$ is perfectoid.
>
>> Proof. Let $\{ \zeta_{p^n} \}_{n \geq 0}$ denote a system of $p$-power roots of unity. Note that
>> $$
> >\mathcal{O}_{\mathbb{Q}_p^{\text{cyc}}} / p \cong \varprojlim_n \mathbb{Z}_p[\zeta_{p^n}] / p.
> >$$
> >Since $\zeta_{p^n} = (\zeta_{p^{n+1}})^p$ for each $n$, the Frobenius map is surjective.

>[!notes]+ Def 9.17
>
> Let $K$ be a perfectoid field. The tilt of $K$, denoted $K^\flat$, is defined by
> $$
> K^\flat := \varprojlim_{z \mapsto z^p} K.
> $$
> Define addition on $K^\flat$ by $(a_n) + (b_n) = (c_n)$, where
> $$
> c_n = \lim_{m \to \infty} (a_{m+n} + b_{m+n})^{p^m}
> $$
> and define multiplication on $K^\flat$ by componentwise multiplication.

Define a homomorphism of multiplicative monoids $\sharp : K^\flat \to K$ by $(a_n)^\sharp = a_0$.

>[!tip]+ lemma 9.18
>
> (1) The limit in Definition 9.17 exists.
>
> (2) $K^\flat$ is a field of characteristic $p$.
>
> (3) The function $(a_n) \mapsto |(a_n)^\sharp| = |a_0|$ is a nonarchimedean norm on $K^\flat$, and $K^\flat$ is a perfectoid field.
>
> (4) We have
> $$
> \mathcal{O}_{K^\flat} = \varprojlim_{z \mapsto z^p} \mathcal{O}_K,
> $$
> and there is an isomorphism of rings
> $$
> \mathcal{O}_{K^\flat} \cong \varprojlim_\Phi \mathcal{O}_K / p.
> $$
>
> (5) $|K^\times| = |K^{\flat \times}|$.
>
> >Proof. Left as an exercise to the reader. Parts (1) and (4) use the following lemma.

>[!tip]+ lemma 9.19
>
> Let $R$ be a ring, let $x, y \in R$, and let $n$ be a positive integer. If $x \equiv y \pmod{p^n}$, then $x^p \equiv y^p \pmod{p^{n+1}}$.
