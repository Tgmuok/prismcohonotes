In the case $G = \mathbb{Z}$, there is also a projective resolution

$$
0 \to \mathbb{Z}[\mathbb{Z}] \xrightarrow{[1]-[0]} \mathbb{Z}[\mathbb{Z}] \to \mathbb{Z} \to 0.
$$

So for any $\mathbb{Z}$-module $A$,

$$
H^1(\mathbb{Z}, A) = A / \left([1]a - a \mid a \in A\right).
$$

$$
H^i(\mathbb{Z}, A) = 0 \text{ for all } i > 1.
$$

The above resolution is related to the fact that $S^1 = \mathbb{R}/\mathbb{Z}$. In general, if there is a free action of $G$ on $\mathbb{R}^n$ and $\mathbb{R}^n/G$ admits a triangulation, then every $G$-module has a projective resolution of length $n$, and $H^i(G, A) = 0$ for $i > n$.

The groups $H^1(G, A)$ and $H^2(G, A)$ admit concrete descriptions. The semidirect product $A \rtimes G$ is the group with underlying set $A \times G$, and group operation given by

$$
(a_1, g_1)(a_2, g_2) = (a_1 + g_1 a_2, g_1 g_2).
$$

Consider the set of sections of the projection map $A \rtimes G \to G$. A section is a group homomorphism $G \to A \rtimes G$ of the form

$$
g \mapsto (s(g), g)
$$

for some $s: G \to A$. Such a map is a group homomorphism if and only if

$$
s(g_1 g_2) = s(g_1) + g_1 s(g_2)
$$

for all $g_1, g_2 \in G$. We have

$$
(a, 1)(s(g), g)(-a, 1) = (s(g) + a - g a, g),
$$

Therefore, two sections are conjugate iff their difference is of the form $g \mapsto a - g a$. Therefore, $H^1(G, A)$ classifies sections of the projection $A \rtimes G \to G$ upto $A$-conjugacy.

An extension of $G$ by $A$ is a group $E$ equipped with a short exact sequence $1 \to A \to E \to G \to 1$. There is a bijection between classes in $H^2(G, A)$ and extensions of $G$ by $A$. We omit the details.

The groups $H^n(G, A)$ are functorial in both $G$ and $A$. The functoriality in $G$ can be described as follows. If $f: H \to G$ is a homomorphism of groups and $A$ is a $G$-module, then we write $f^* A$ for the $H$-module with underlying abelian group $A$ and $H$-action determined by $f$. The machinery of derived functors tells us that there are homomorphisms

$$
H^n(G, A) \to H^n(G', f^* A).
$$

If the cohomology is calculated using the resolution $\cdots \to \mathbb{Z}[G \times G] \to \mathbb{Z}[G] \to \mathbb{Z}$ mentined above, then this map sends a homogeneous cocycle $\phi: G^{n+1} \to A$ to $(f \times \cdots \times f) \circ \phi$.

If $f: H \to G$ is an injection, then the functor $f^*$ is called restriction and is denoted by $\operatorname{Res}$. We sometimes also denote the corresponding $H^n(G, A) \to H^n(H, A)$ by $\operatorname{Res}$.

The restriction functor $\operatorname{Res}$ has a right adjoint called $\operatorname{Ind}$. Given an $H$-module $B$, the $G$-module $\operatorname{Ind} B$ is given by

$$
\operatorname{Ind} B = \operatorname{Hom}_{\mathbb{Z}[H]}(\mathbb{Z}[G], B),
$$

where we view $\mathbb{Z}[G]$ as an $H$-module via multiplication on the left, and as a $G$-module via multiplication on the right. Recall that “right adjoint” means that for any $G$-module $A$ and $H$-module $B$, there is a natural isomorphism

$$
\operatorname{Hom}_{\mathbb{Z}[H]}(\operatorname{Res} A, B) \cong \operatorname{Hom}_{\mathbb{Z}[G]}(A, \operatorname{Ind} B).
$$

We also have

$$
H^n(H, B) = H^n(G, \operatorname{Ind} B).
$$

Modules in the image of the functor $\operatorname{Ind}$ are called “coinduced modules”. (There is also a functor called $\operatorname{ind}$ that is left adjoint to $\operatorname{Res}$, and modules in the image of $\operatorname{ind}$ are called “induced modules”. But we will not use $\operatorname{ind}$.)

Given a normal subgroup $H$ of $G$, the composite

$$
H^n(G/H, A^H) \to H^n(G, A^H) \to H^n(G, A)
$$

is called an inflation map and denoted $\operatorname{Inf}$.

We would like to allow our groups and modules to have a topology. The right way to do this is probably to use condensed mathematics, but as far as I know, no one has worked out the details yet. So instead, we make the following ad hoc definition. Let $G$ be a topological group, and let $A$ be a topological $G$-module (i.e. a $G$-module such that the $G$-action is continuous). Define a cochain complex $K_{\mathrm{cts}}$ by letting $K_{\mathrm{cts}}^n$ be the set of continuous $G$-equivariant homomorphisms $G^{n+1} \to A$. Define $H_{\mathrm{cts}}^n(G, A)$ to be the $n$th cohomology group of $K_{\mathrm{cts}}$.

Warning: a short exact sequence of modules does not always give us a long exact sequence of cohomology groups. For example, we have a short exact sequence of abelian groups

$$
0 \to \mathbb{Z} \to \mathbb{R} \to S^1 \to 0.
$$

If we consider these as $S^1$-modules with trivial $S^1$-action, then

$$
H_{\mathrm{cts}}^1(S^1, \mathbb{R}) = \operatorname{Hom}_{\mathrm{cts}}(S^1, \mathbb{R}) = 0
$$

$$
H_{\mathrm{cts}}^1(S^1, S^1) = \operatorname{Hom}_{\mathrm{cts}}(S^1, S^1) = \mathbb{Z}
$$

$$
H_{\mathrm{cts}}^2(S^1, \mathbb{Z}) = 0.
$$

This is why it would probably be better to use condensed mathematics.

However, given a short exact sequence $0 \to A \to B \to C \to 0$, we do always get a long exact sequence

$$
0 \to A^G \to B^G \to C^G \to H_{\mathrm{cts}}^1(G, A) \to H_{\mathrm{cts}}^1(G, B) \to H_{\mathrm{cts}}^1(G, C).
$$

We get the full long exact sequence if the map $B \to C$ admits a continuous section (as a map of topological spaces; the section need not be a $G$-module homomorphism).

> [!tip]+ lemma 12.1
>
> Let $G$ be a profinite group, and let $A$ be a topological $G$-module.
> 1. If $A$ has the discrete topology, then every vector in $A$ has an open stabilizer, and
> $$
> H_{\mathrm{cts}}^i(G, A) = \varprojlim_{H \subset G} H^i(G/H, A^H),
> $$
> where the limit runs over open normal subgroups of $G$.
> 2. If $H_{\mathrm{cts}}^i(G, \mathbb{F}_p)$ is finite for all $i$, and $A$ is a finite free $\mathbb{Z}_p$-module, then
> $$
> H_{\mathrm{cts}}^i(G, A) = \varprojlim_n H_{\mathrm{cts}}^i(G, A/p^n A)
> $$
> 3. If $H_{\mathrm{cts}}^i(G, \mathbb{F}_p)$ is finite for all $i$, and $A$ is a finite-dimensional $\mathbb{Q}_p$-vector space, then for any $G$-stable lattice $\Lambda \subset A$,
> $$
> H_{\mathrm{cts}}^i(G, A) = H_{\mathrm{cts}}^i(G, \Lambda) \otimes_{\mathbb{Z}_p} \mathbb{Q}_p
> $$
> (Since $G$ is compact, such a lattice always exists.)

> [!tip]+ lemma 12.2
>
> 4. Let $K$ be a finite extension of $\mathbb{Q}_p$. Then $H_{\mathrm{cts}}^i(\operatorname{Gal}(\overline{K}/K), \mathbb{F}_p)$ is finite for all $i$.
> 5. Let $K$ be a finite extension of $\mathbb{Q}$, and let $S$ be a finite set of places of $K$. Let $K_S$ be the largest algebraic extension of $K$ unramified outside $S$. Then $H_{\mathrm{cts}}^i(\operatorname{Gal}(K_S/K), \mathbb{F}_p)$ is finite for all $i$.
