>[!notes]+ Def 27.1
>
> A perfectoid space is strictly totally disconnected if it is quasi-compact and quasiseparated and every étale cover splits.

>[!notes]+ Def 27.2
>
> Let $\mathrm{Perf}$ be the site of perfectoid spaces of characteristic $p$ with the pro-étale topology.
>
> We say that a map $f: \mathcal{F} \to \mathcal{G}$ of sheaves on $\mathrm{Perf}$ is étale if for every perfectoid space $Y$ with a map $Y \to \mathcal{G}$, the pullback $\mathcal{F} \times_\mathcal{G} Y$ is represented by a perfectoid space $X$ and $X \to Y$ is étale.
>
> We say that $f$ is quasi-pro-étale if it is locally separated and for all strictly totally disconnected perfectoid spaces $Y$ with a map $Y \to \mathcal{G}$, the pullback $\mathcal{F} \times_\mathcal{G} Y$ is represented by a perfectoid space $X$ and $X \to Y$ is pro-étale.

>[!abstract]+ Prop 27.3
>
> A pro-étale sheaf $Y$ on $\mathrm{Perf}$ is a diamond if and only if there is a surjective quasi-pro-étale map $X \to Y$ from a perfectoid space $X$.

>[!tip]+ lemma 27.4
>
> Let $f: X \to Y$ be a quasi-pro-étale map of pro-étale sheaves. If $Y$ is a diamond, then $X$ is also a diamond. Conversely, if $f$ is surjective and $X$ is a diamond, then $Y$ is a diamond.

>[!notes]+ Def 27.5
>
> We say that a diamond $X$ is spatial if it is qcqs and its underlying topological space is a spectral space. We say that $X$ locally spatial if $|X|$ can be covered by open sets $U_i$ such that the restriction of $X$ to each $U_i$ is spatial.

>[!notes]+ Def 27.6
>
> Let $X$ be a locally spatial diamond. The site $X_{\text{ét}}$ is the site whose objects are locally separated étale maps $X' \to X$, where $X'$ is a diamond, with coverings given by families of jointly surjective maps.
>
> Let $X$ be a diamond. The site $X_{\text{qproét}}$ is the site whose objects are locally separated quasi-pro-étale maps $X' \to X$, where $X'$ is a diamond, with coverings given by families of jointly surjective maps.

>[!abstract]+ Prop 27.7
>
> If $X$ is an analytic adic space over $\mathrm{Spa}(\mathbb{Z}_p, \mathbb{Z}_p)$, then there is an equivalence of sites $X_{\text{ét}} \cong X_{\text{ét}}^\diamond$.

>[!notes]+ Def 27.8
>
> Let $X$ be an analytic adic space over $\mathrm{Spa}(\mathbb{Z}_p, \mathbb{Z}_p)$. Define $X_{\text{qproét}} = X_{\text{qproét}}^\diamond$.

>[!abstract]+ Prop 27.9
>
> Let $X$ be a diamond, and let $\nu: X_{\text{qproét}} \to X_{\text{ét}}$ be the projection map. Then the functor $\nu^*$ from sheaves on $X_{\text{ét}}$ to sheaves on $X_{\text{qproét}}$ is fully faithful.
>
> Let $\mathcal{F}$ be sheaf on $X_{\text{ét}}$. Then the natural map $\mathcal{F} \to \nu_* \nu^* \mathcal{F}$ is an isomorphism. If $\mathcal{F}$ is a sheaf of abelian groups, then $R^i \nu_* \nu^* \mathcal{F} = 0$ for all $i > 0$.
>
> Now let $X$ be rigid analytic space over a nonarchimedean field $F$ of characteristic zero. We will write $X_{\text{qproét}}$ for $X_{\text{qproét}}^\diamond$.

>[!tip]+ lemma 27.10
>
> The site $X_{\text{qproét}}$ has a basis consisting of affinoid perfectoid objects $\mathrm{Spa}(R, R^+)$, such that there exists a filtered system of finite étale maps $\mathrm{Spa}(R_i, R_i^+) \to X$ under $\mathrm{Spa}(R^\sharp, R^{\sharp +}) \to X$, for which $\varinjlim_i R_i \to R^\sharp$ is injective with dense image.
>
> We will define the following sheaves on $X_{\text{qproét}}$.
>
> $$
> \mathcal{O}_X = \nu^* \mathcal{O}_{X_{\text{ét}}}
> $$
>
> $$
> \mathcal{O}_X^+ = \nu^* \mathcal{O}_{X_{\text{ét}}}^+
> $$
>
> Let $\widehat{\mathcal{O}}_X$ (resp. $\widehat{\mathcal{O}}_X^+$) be the sheaf that sends an affinoid perfectoid $\mathrm{Spa}(R, R^+)$ to $R^\sharp$ (resp. $R^{\sharp +}$).

>[!example]+ ex 27.11
>
> Let $\mathbb{T} = \mathrm{Spa}(\mathbb{Q}_p \langle T^{\pm 1} \rangle)$, and let $\mathbb{T}_\infty$ be the perfectoid pro-étale cover $\mathrm{Spa}(\mathbb{Q}_p^{\mathrm{cyc}} \langle T^{\pm 1/p^\infty} \rangle)$. Then
>
> $$
> \mathcal{O}_{\mathbb{T}}(\mathbb{T}_\infty) = \varinjlim_n \mathbb{Q}(\mu_{p^n}) \langle T^{\pm 1/p^n} \rangle
> $$
>
> $$
> \widehat{\mathcal{O}}_{\mathbb{T}}(\mathbb{T}_\infty) = \mathbb{Q}_p^{\mathrm{cyc}} \langle T^{\pm 1/p^\infty} \rangle.
> $$

>[!tip]+ lemma 27.12
>
> $$
> \widehat{\mathcal{O}}_X^+ = \varprojlim_n \mathcal{O}_X^+/p^n
> $$

>[!done]+ Coro 27.13
>
> For any pseudouniformizer $\varpi$ of $F$,
>
> $$
> \nu_* \widehat{\mathcal{O}}_X^+/\varpi \cong \mathcal{O}_{X_{\text{ét}}}^+/\varpi.
> $$

>[!done]+ Coro 27.14
>
> $$
> H^i(X_{\text{ét}}, \mathbb{F}_p) \cong H^i(X_{\text{qproét}}, \mathbb{F}_p).
> $$
>
> For any pseudouniformizer $\varpi$ of $K$,
>
> $$
> H^i(X_{\text{ét}}, \mathcal{O}_{X_{\text{ét}}}^+/\varpi) \cong H^i(X_{\text{qproét}}, \widehat{\mathcal{O}}_X^+/\varpi).
> $$
>
>> *Proof.* The first claim follows from Proposition 27.9, and the second follows from Corollary 27.13.

>[!danger]+ Them 27.15 (Primitive comparison theorem)
>
> Let $C$ be a complete algebraically closed extension of $\mathbb{Q}_p$, and let $X$ be a proper smooth rigid analytic space over $C$. Then the natural maps
>
> $$
> H^i(X_{\text{ét}}, \mathbb{F}_p) \otimes_{\mathbb{F}_p} \mathcal{O}_C^a/p \to H^i(X_{\text{ét}}, \mathcal{O}_{X_{\text{ét}}}^{+a}/p)
> $$
>
> $$
> H^i(X_{\text{qproét}}, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} \mathcal{O}_C^a \to H^i(X_{\text{qproét}}, \widehat{\mathcal{O}}_X^{+a})
> $$
>
> $$
> H^i(X_{\text{qproét}}, \mathbb{Q}_p) \otimes_{\mathbb{Q}_p} C \to H^i(X_{\text{qproét}}, \widehat{\mathcal{O}}_X)
> $$
>
> are isomorphisms.
>
> A key idea in the proof is to use the Artin-Schreier exact sequence
>
> $$
> 0 \to \mathbb{F}_p \to \widehat{\mathcal{O}}_X^+ \xrightarrow{x \mapsto x - x^p} \widehat{\mathcal{O}}_X^+ \to 0.
> $$

>[!abstract]+ Prop 27.16
>
> Let $X$ be a smooth rigid analytic space over $C$. Let $\lambda: X_{\text{qproét}} \to X_{\text{an}}$ be the projection. Then $R^j \lambda_* \widehat{\mathcal{O}}_X^+ \cong \Omega_X^j(-j)$.
>
>> *Sketch of proof.* Locally, $X$ admits an étale map to a torus $\mathbb{T} = \mathrm{Spa}\, C \langle T_1^{\pm 1}, \dots, T_n^{\pm 1} \rangle$. The torus has an explicit perfectoid cover $\mathbb{T}_\infty = \mathrm{Spa}\, C \langle T_1^{\pm 1/p^\infty}, \dots, T_n^{\pm 1/p^\infty} \rangle$, which is a $\mathbb{Z}_p(1)^n$-torsor. We know that the structure sheaf on this perfectoid cover is acyclic. The proposition then reduces to a computation of the cohomology group
>>
>> $$
>> H_{\text{cts}}^j \left( \mathbb{Z}_p(1)^n, C \left\langle T_1^{\pm 1/p^\infty}, \dots, T_n^{\pm 1/p^\infty} \right\rangle \right).
>> $$
>>
>> It is possible to show that the map
>>
>> $$
>> H_{\text{cts}}^j(\mathbb{Z}_p(1)^n, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} C \langle T_1^{\pm 1}, \dots, T_n^{\pm n} \rangle \to H_{\text{cts}}^j \left( \mathbb{Z}_p^n, C \left\langle T_1^{\pm 1/p^\infty}, \dots, T_n^{\pm 1/p^\infty} \right\rangle \right)
>> $$
>>
>> is an isomorphism. Moreover, the cup product determines an isomorphism
>>
>> $$
>> H_{\text{cts}}^j(\mathbb{Z}_p(1)^n, \mathbb{Z}_p) \cong \wedge^j H_{\text{cts}}^1(\mathbb{Z}_p^n, \mathbb{Z}_p),
>> $$
>>
>> and there is a natural isomorphism
>>
>> $$
>> H_{\text{cts}}^1(\mathbb{Z}_p(1)^n, \mathbb{Z}_p) \cong \mathrm{Hom}(\mathbb{Z}_p(1)^n, \mathbb{Z}_p).
>> $$

>[!done]+ Coro 27.17 (Hodge–Tate decomposition)
>
> Let $X$ be a proper smooth rigid analytic space over a $p$-adic field $K$, and let $C = \widehat{\overline{K}}$. Then
>
> $$
> H_{\text{ét}}^n(X_C, \mathbb{Q}_p) \otimes_{\mathbb{Q}_p} C \cong \bigoplus_{i+j=n} H^i(X, \Omega_X^j) \otimes_K C(-j).
> $$
>
>> *Sketch of proof.* First use the primitive comparison theorem to write $H_{\text{ét}}^n(Y_C, \mathbb{Q}_p) = H^n(Y_{C,\text{qproét}}, \widehat{\mathcal{O}}_Y)$. There is a Leray spectral sequence
>>
>> $$
>> H^i(Y_C, R^j \lambda_* \widehat{\mathcal{O}}_Y) \Rightarrow H^{i+j}(Y_{C,\text{qproét}}, \widehat{\mathcal{O}}_Y).
>> $$
>>
>> Because there are no nonzero Galois-equivariant maps between $C(-j)$ and $C(-j')$ for $j \neq j'$, we must have
>>
>> $$
>> H^n(Y_{C,\text{qproét}}, \widehat{\mathcal{O}}_Y) = \bigoplus_{i+j=n} H^i(Y_C, R^j \lambda_* \widehat{\mathcal{O}}_Y).
>> $$
