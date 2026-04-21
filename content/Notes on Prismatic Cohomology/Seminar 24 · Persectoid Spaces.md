>[!notes]+ Def 24.1
>
> An affinoid perfectoid space is an adic space of the form $\operatorname{Spa}(R, R^+)$ with $R$ perfectoid. A perfectoid space is an adic space that can be covered by affinoid perfectoid spaces.

**Remark 24.2.** It is unknown whether an adic space that is both affinoid and perfectoid is necessarily affinoid perfectoid.

The tilting construction can be glued, so for any perfectoid space $X$, we can define its tilt $X^\flat$.

>[!danger]+ Them 24.3
>
> For any perfectoid space $X$, the functor $Y \mapsto Y^\flat$ induces an equivalence between the categories of perfectoid spaces over $X$ and $X^\flat$.

Recall the following result that was proved earlier in the course.

>[!danger]+ Them 24.4 (Tate, 1967)
>
> Let $K = \mathbb{Q}_p^{\mathrm{cyc}}$. If $L/K$ is a finite extension, then the image of $\operatorname{tr}: \mathcal{O}_L \to \mathcal{O}_K$ contains $\mathfrak{m}_K$.

Tate's result says that any finite extension of $\mathbb{Q}_p^{\mathrm{cyc}}$ is almost unramified.

>[!notes]+ Def 24.5
>
> Let $(R, R^+)$ be a perfectoid Tate-Huber pair. We say that an $R^+$-module $M$ is almost zero if $R^\circ$ annihilates $M$.

>[!example]+ ex 24.6
>
> If $K$ is a perfectoid field, then an $\mathcal{O}_K$-module is almost zero iff it is annihilated by $\mathfrak{m}_K$. One can show that an almost zero $\mathcal{O}_K$-module is a direct sum of copies of the residue field $\mathcal{O}_K/\mathfrak{m}_K$.

An extension of almost zero modules is again almost zero.

**Remark 24.7.** Here it is important that $R$ is perfectoid. Note that for $R = \mathbb{Q}_p$, $R^+ = \mathbb{Z}_p$, then $\mathbb{Z}/p\mathbb{Z}$ is annihilated by $R^\circ = p\mathbb{Z}_p$, but $\mathbb{Z}/p^2\mathbb{Z}$ is not.

In fact, the subcategory of almost zero $R^+$-modules is a thick Serre subcategory, so the following definition makes sense.

>[!notes]+ Def 24.8
>
> The category of almost $R^\circ$-modules, denoted $R^{\circ a}$-mod is the quotient of the category of $R^\circ$-modules by the subcategory of almost zero modules.

If $M$ is an $R^\circ$-module, then we write $M^a$ for the corresponding $R^{\circ a}$-modules. One can similarly define the category of almost $R^+$-modules, but it is equivalent to the category of almost $R^\circ$-modules.

>[!example]+ ex 24.9
>
> If $K$ is a perfectoid field, then $\mathfrak{m}_K^a \to \mathcal{O}_K^a$ is an isomorphism of $\mathcal{O}_K^a$-modules.

>[!danger]+ Them 24.10
>
> Let $(R, R^+)$ be a perfectoid Tate-Huber pair, and let $X = \operatorname{Spa}(R, R^+)$. Then $H^i(X, \mathcal{O}_X^+)$ is almost zero for $i > 0$, and $H^0(X, \mathcal{O}_X^+) = R^+$.

>[!danger]+ Them 24.11
>
> Let $R$ be a perfectoid Tate ring.
> 1. For any finite étale $R$-algebra $S$, $S$ is perfectoid.
> 2. Tilting induces an equivalence between finite étale $R$-algebras and finite étale $R^\flat$ algebras.
> 3. (almost purity) For any finite étale $R$-algebra $S$, $S^\circ$ is almost finite étale over $R^\circ$.

We would like to define a notion of tilting for spaces that are not perfectoid. If we just tried to tilt the rings, we would lose too much information. If $K$ is a finite extension of $\mathbb{Q}_p$, then $\varprojlim_{x \mapsto x^p} K$ is just the residue field of $K$. The solution is to find a perfectoid cover, tilt the cover, and then take a quotient. So for example, the tilt of $\operatorname{Spa}\mathbb{Q}_p$ should be the quotient of $(\operatorname{Spa}\mathbb{Q}_p^{\mathrm{cyc}})^\flat/\mathbb{Z}_p^\times$. The quotient will live in the category of diamonds, which are similar to algebraic spaces.

>[!notes]+ Def 24.12
>
> 1. A morphism $f: X \to Y$ of perfectoid spaces is finite étale if for all $\operatorname{Spa}(B, B^+) \subset Y$ open, the pullback $X \times_Y \operatorname{Spa}(B, B^+)$ is $\operatorname{Spa}(A, A^+)$, where $A$ is a finite étale $B$-algebra, and $A^+$ is the integral closure of the image of $B^+$ in $A$.
> 2. A morphism $f: X \to Y$ is étale if for all $x \in X$ there exists an open $U \ni x$ and $V \supset f(U)$ such that there is a diagram
> 
>```tikz
>\usepackage{tikz-cd}
>
>\begin{document}
>\begin{tikzcd}
>
>U \arrow[rr, "open", hook] \arrow[rd, "f|_U"'] &   & W \arrow[ld, "finte \ \ \acute{e}tale"] \\
>& V &
>
>\end{tikzcd}
>\end{document}
>```
> 
> 3. An étale cover is a jointly surjective family of étale maps.

>[!abstract]+ Prop 24.13
>
> One can construct the étale site $X_{\mathrm{\acute{e}t}}$ from the above definitions. The site $X^\flat_{\mathrm{\acute{e}t}}$ is naturally equivalent to $X_{\mathrm{\acute{e}t}}$. If $X$ is affinoid perfectoid, then $H^i(X_{\mathrm{\acute{e}t}}, \mathcal{O}_X) = 0$ and $H^i(X_{\mathrm{\acute{e}t}}, \mathcal{O}_X^+)^a = 0$ for $i > 0$, and $H^i(X_{\mathrm{\acute{e}t}}, \mathbb{F}_p) = 0$ for $i > 1$.

