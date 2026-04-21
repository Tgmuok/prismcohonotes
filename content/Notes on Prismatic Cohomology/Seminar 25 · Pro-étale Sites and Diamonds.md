>[!abstract]+ Prop 25.1
>
> Let $X_i = \operatorname{Spa}(R_i, R_i^+)$ be a directed system of affinoid perfectoid spaces. Then the limit $\varprojlim_i X_i$ exists in the category of perfectoid spaces, and is isomorphic to $\operatorname{Spa}(R, R^+)$, where $R^+$ is the completion of $\varinjlim_i R_i^+$ for the $\varpi$-adic topology and $R = R^+[1/\varpi]$. Here $\varpi$ is the image of an arbitrarily chosen pseudouniformizer of some $R_i$.

**Remark 25.2.**
(1) The $\varpi$-adic topology is generally weaker than the direct limit topology.
(2) The limit generally does not exist in the category of adic spaces. Given maps $(R_i, R_i^+) \to (S, S^+)$, the induced map $R \to S$ is continuous for the topology defined above if $S$ is uniform, but not for more general $S$. To give a concrete example, the limit $\varprojlim_n \operatorname{Spa}(\mathbb{Q}_p \langle p^n T \rangle, \mathbb{Z}_p \langle p^n T \rangle)$ in the category of sousperfectoid spaces is a single point $\operatorname{Spa}(\mathbb{Q}_p, \mathbb{Z}_p)$, but this is not the limit in the category of adic spaces, as can be seen by looking at $\mathbb{Q}_p[\varepsilon]/(\varepsilon^2)$-valued points.

>[!notes]+ Def 25.3
>
> Let $f: Y \to X$ be a map of perfectoid spaces. We say that $f$ is affinoid pro-étale if $Y$ and $X$ are affinoid, $f$ can be written as a cofiltered inverse limit of étale maps $Y_i \to X$, with $Y_i$ affinoid perfectoid. We say that $f$ is pro-étale if for all $y \in Y$, there exist open sets $V \subset Y$, $U \subset X$ with $y \in V$, $f(V) \subset U$ and $f|_V: V \to U$ is affinoid pro-étale.

**Remark 25.4.** Scholze's $p$-adic Hodge theory paper uses a different definition of pro-étale morphisms.

>[!example]+ ex 25.5
>
> Let $X$ be a perfectoid space, and let $S$ be a profinite set. Write $S = \varprojlim_i S_i$, where $S_i$ are finite sets. Then we can define $X \times \underline{S} := \varprojlim_i \underline{S_i}$. The projection $X \times \underline{S} \to X$ is proétale. More generally, this is true if $X \times \underline{S} \to X$ is proétale if $S$ is locally profinite.

>[!example]+ ex 25.6
>
> Let $X$ be a perfectoid space, and let $x = \operatorname{Spa}(K, \mathcal{O}_K)$ be a point of $X$. Then $x = \varprojlim_{U \ni x} U$. Since each $U \hookrightarrow X$ is étale, $x \to X$ is proétale. In particular, this means that proétale morphisms are not necessarily open.

>[!notes]+ Def 25.7
>
> Consider the following categories:
> - $\mathrm{Perfd}$, the category of perfectoid spaces.
> - $\mathrm{Perf}$, the category of perfectoid spaces in characteristic $p$.
> - $X_{\mathrm{proét}}$, the category of perfectoid spaces proétale over a perfectoid space $X$.
> 
> We give each of these categories the structure of a site by saying that a collection of morphisms $\{f_i: Y_i \to Y\}$ is a covering if the $f_i$ are pro-étale, and for all quasicompact open $U \subset Y$, there exists a finite index set $I_U$ and quasicompact open subsets $U_i \subset Y_i$ for $i \in I_U$, such that $U = \bigcup_{i \in I_U} f_i(U_i)$.

>[!abstract]+ Prop 25.8
>
> (1) The functors $X \mapsto \mathcal{O}_X(X)$, $X \mapsto \mathcal{O}_X^+(X)$ are sheaves on the pro-étale site of $\mathrm{Perfd}$. If $X$ is affinoid, then $H^i(X_{\mathrm{proét}}, \mathcal{O}_X) = 0$ and $H^i(X_{\mathrm{proét}}, \mathcal{O}_X^+)^a = 0$ for $i > 0$.
> (2) For any perfectoid space $X$, the functor $h_X = \operatorname{Hom}(-, X)$ is a sheaf on the pro-étale site of $\mathrm{Perfd}$.

>[!notes]+ Def 25.9
>
> A diamond is a pro-étale sheaf $D$ on $\mathrm{Perf}$ such that one can write $D = X/R$, where $X$ is a perfectoid space and $R \subset X \times X$ is a perfectoid space with $s,t: R \to X$ pro-étale.

>[!notes]+ Def 25.10
>
> Let $Y$ be a perfectoid space in characteristic $p$. An untilt of $Y$ is a pair $(Y^\sharp, (Y^\sharp)^\flat \xrightarrow{\sim} Y)$, where $Y^\sharp$ is a perfectoid space.

>[!example]+ ex 25.11
>
> Let $\operatorname{Spd}\mathbb{Q}_p$ be the functor that sends $X \in \mathrm{Perf}$ to the set of isomorphism classes of characteristic zero untilts of $X$. We claim that $\operatorname{Spd}\mathbb{Q}_p$ is a diamond.
> 
> Write $\operatorname{Spd}\mathbb{Q}_p^{\mathrm{cyc}}$ for $\operatorname{Spa}(\mathbb{Q}_p^{\mathrm{cyc}})^\flat$. The tilting equivalence gives us a morphism $\operatorname{Spd}\mathbb{Q}_p^{\mathrm{cyc}} \to \operatorname{Spd}\mathbb{Q}_p$. This is a surjection of pro-étale sheaves since every characteristic zero perfectoid space has a pro-étale cover that admits a map to $\operatorname{Spa}\mathbb{Q}_p^{\mathrm{cyc}}$. So $\operatorname{Spd}\mathbb{Q}_p$ is the quotient of $\operatorname{Spd}\mathbb{Q}_p^{\mathrm{cyc}}$ by an equivalence relation $R \subset \operatorname{Spd}\mathbb{Q}_p^{\mathrm{cyc}} \times \operatorname{Spd}\mathbb{Q}_p^{\mathrm{cyc}}$. We claim that in fact $R$ can be identified with $\operatorname{Spd}\mathbb{Q}_p^{\mathrm{cyc}} \times \underline{\mathbb{Z}_p^\times}$, where $\underline{\mathbb{Z}_p^\times}$ is a constant group sheaf. This is equivalent to checking that $\operatorname{Spa}\mathbb{Q}_p^{\mathrm{cyc}} \times \underline{\mathbb{Z}_p^\times} \to \operatorname{Spa}\mathbb{Q}_p^{\mathrm{cyc}} \times \operatorname{Spa}\mathbb{Q}_p^{\mathrm{cyc}}$ is an isomorphism of presheaves on $\mathrm{Perfd}$. By Galois theory,
> $$
> \operatorname{Spa}\mathbb{Q}_p(\mu_{p^n}) \times (\mathbb{Z}/p^n\mathbb{Z})^\times \xrightarrow{\sim} \operatorname{Spa}\mathbb{Q}_p(\mu_{p^n}) \times \operatorname{Spa}\mathbb{Q}_p(\mu_{p^n})
> $$
> and then taking the inverse limit proves the claim. Then $R \rightrightarrows \operatorname{Spd}\mathbb{Q}_p^{\mathrm{cyc}}$ are proétale morphisms, so $\operatorname{Spd}\mathbb{Q}_p$ is a diamond.
