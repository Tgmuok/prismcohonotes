>[!done]+ Coro 11.1
>
> Let $K$ be a perfectoid field. Then tilting induces an equivalence of categories between perfectoid extensions of $K$ and perfectoid extensions of $K^\flat$.
> 
> Moreover, if $L/K$ is an extension of perfectoid fields, then $L/K$ is finite iff $L^\flat/K^\flat$ is finite.

>[!tip]+ lemma 11.2
>
> If $K$ is a perfectoid field and $K^\flat$ is algebraically closed, then so is $K$.
>
>>*Proof.* Let $P(X) = X^d + a_{d-1}X^{d-1} + \cdots + a_0 \in K[X]$ be a monic irreducible polynomial. Since $K^\flat$ is algebraically closed, $|K^{\flat\times}|$ is a $\mathbb{Q}$-vector space, so $|K^\times|$ is as well. Therefore, by scaling the variable, we may assume that $a_0 \in \mathcal{O}_K^\times$. Since $P$ is irreducible, its Newton polygon must be a straight line, so $a_i \in \mathcal{O}_K$ for all $i$.
>>
>>Let $Q(X) \in \mathcal{O}_{K^\flat}[X]$ be a monic polynomial such that $P$ and $Q$ have the same image in $(\mathcal{O}_K/p\mathcal{O}_K)[X]$. Let $y \in \mathcal{O}_{K^\flat}$ be a root of $Q(X)$. Then $p \mid P(y^\sharp)$. If $P(y^\sharp) \neq 0$, choose $c \in \mathcal{O}_K$ so that $|c|^d = |P(y^\sharp)|$. Then replace $P(X)$ with $c^{-d}P(cX + y^\sharp)$. By repeating this process, we find a sequence of elements of $\mathcal{O}_K$ converging to a root of $P$.

>[!tip]+ lemma 11.3 (Krasner's lemma)
>
> Let $K$ be a nonarchimedean field, and let $\alpha, \beta \in \overline{K}$, with $\alpha$ separable over $K(\beta)$. Suppose that for all $\sigma \in \operatorname{Gal}(K(\beta)^{\mathrm{sep}}/K(\beta))$, either $\sigma(\alpha) = \alpha$ or $|\alpha - \sigma(\alpha)| > |\alpha - \beta|$. Then $\alpha \in K(\beta)$.
>
>>*Proof.* Let $\sigma \in \operatorname{Gal}(K(\beta)^{\mathrm{sep}}/K(\beta))$. Then
>>$$
>>|\alpha - \sigma(\alpha)| \leq \max(|\alpha - \beta|, |\sigma(\alpha) - \beta|) = |\alpha - \beta|.
>>$$
>>By assumption, we must have $\sigma(\alpha) = \alpha$. Since this holds for all $\sigma$, we must have $\alpha \in K(\beta)$.

>[!abstract]+ Prop 11.4
>
> Any finite extension of a perfectoid field is perfectoid.
>
>>*Proof.* Let $K$ be a perfectoid field, and let $C^\flat$ be the completion of an algebraic closure of $K^\flat$. By Corollary 11.1, $C^\flat$ has an untilt $C$ over $K$. Furthermore, $C$ is algebraically closed by Lemma 11.2. Let $C_0$ be the union of the untilts of all finite extensions of $K^\flat$; then $C_0$ is dense in $C$ since the union of all finite extensions of $C^\flat$ is dense in $C^\flat$. It follows from Krasner's lemma that a dense subfield of an algebraically closed nonarchimedean field is separably closed. Then $C_0$ must contain all finite extensions of $K$. So any finite extension $L/K$ is contained in a Galois extension $M/K$ that is an untilt of some $M^\flat/K^\flat$. By Galois theory, any subfield of $M$ containing $K$ must be the untilt of a subfield of $M^\flat$ containing $K^\flat$.

>[!danger]+ Them 11.5
>
> Let $K$ be a perfectoid field. There is an equivalence of categories between finite extensions of $K$ and finite extensions of $K^\flat$.
> 
> Hence there is an injection
>$$
>\operatorname{Aut}_{\mathrm{cts}}(\overline{K}) \hookrightarrow \operatorname{Aut}_{\mathrm{cts}}(\overline{K^\flat})
>$$
>inducing an isomorphism
>$$
>\operatorname{Gal}(\overline{K}/K) \cong \operatorname{Gal}(\overline{K^\flat}/K^\flat).
>$$
>
>>*Proof.* Combine Corollary 11.1 and Proposition 11.4.

>[!done]+ Coro 11.6
>
> The fields $\mathbb{Q}_p(\mu_{p^\infty})$, $\mathbb{Q}_p^{\mathrm{cyc}} = \widehat{\mathbb{Q}_p(\mu_{p^\infty})}$, $\mathbb{F}_p((t^{p^{-\infty}}))$, and $\mathbb{F}_p((t))$ have isomorphic Galois groups.
>
>>*Proof.* By the above theorem, $\mathbb{Q}_p^{\mathrm{cyc}} = \widehat{\mathbb{Q}_p(\mu_{p^\infty})}$ and $\mathbb{F}_p((t^{p^{-\infty}}))$ have isomorphic Galois groups. By Krasner's lemma, taking completions does not change the Galois group, and taking perfections also does not change the Galois group.

Let $G$ be a group. A $G$-module is an abelian group $A$ along with a homomorphism $G \to \operatorname{Aut} A$.

We write $A^G$ for the $G$-invariants of $A$. Then $(-)^G$ is a functor from the category of $G$-modules to the category of abelian groups. Observe that $A^G = \operatorname{Hom}_G(\mathbb{Z}, A)$, where $\mathbb{Z}$ has the trivial $G$-action. It is left exact, meaning that given an exact sequence
$$
0 \to A \to A' \to A'',
$$
the sequence
$$
0 \to A^G \to (A')^G \to (A'')^G
$$
is also exact. However, it is not right exact.

The forgetful functor from $G$-modules to abelian groups has a left adjoint $G \mapsto \mathbb{Z}[G]$. We have
$$
\mathbb{Z}[G] = \bigoplus_{g \in G} \mathbb{Z} \cdot [g],
$$
with
$$
[g][h] = [gh].
$$

A $G$-module $A$ is called projective if the functor $\operatorname{Hom}_G(A, -)$ is exact. A (possibly infinite) direct sum of copies of $\mathbb{Z}[G]$ is projective.

Given a projective resolution
$$
\cdots \to P_n \to P_{n-1} \to \cdots \to P_0 \to \mathbb{Z} \to 0,
$$
we define a cochain complex $K^\bullet$ by $K^n = \operatorname{Hom}_G(P_n, A)$, with differentials induced by the maps $P_n \to P_{n-1}$. Define
$$
H^n(G, A) = H^n(K^\bullet).
$$

A standard result in homological algebra is that this definition is independent of the resolution chosen. Then $A^G = H^0(G, A)$. Given any short exact sequence of $G$-modules
$$
0 \to A \to B \to C \to 0,
$$
there is a long exact sequence
$$
0 \to H^0(G, A) \to H^0(G, B) \to H^0(G, C) \to H^1(G, A) \to \cdots.
$$

A useful choice of projective resolution of $\mathbb{Z}$ is the following. Let $P_n = \mathbb{Z}[G^{n+1}]$. We consider $P_n$ as a $G$-module via
$$
g[g_0, \dots, g_n] = [gg_0, \dots, gg_n].
$$

The differentials are given by
$$
d[g_0, \dots, g_n] = \sum_{j=0}^n (-1)^j [g_0, \dots, \hat{g}_j, \dots, g_n],
$$
where $\hat{g}_j$ indicates that $g_j$ is omitted. (Most texts use the "bar resolution", which is equivalent but written slightly differently. I think the description given here is a bit more elegant, but maybe the bar resolution is more convenient for calculations?)

For example, $H^1(G, A)$ is the space of $G$-equivariant maps $\phi: G \times G \to A$ satisfying
$$
\phi(y, z) - \phi(x, z) + \phi(x, y) = 0
$$
for all $x, y, z \in G$, modulo the space of maps of the form
$$
\phi(x, y) = \psi(y) - \psi(x)
$$
for some $G$-equivariant $\psi: G \to A$.

Since $\psi$ is homogeneous, we can write
$$
\phi(x, y) = x\tilde{\phi}(x^{-1}y),
$$
where
$$
\tilde{\phi}(y) = \phi(1, y).
$$

Similarly
$$
\psi(x) = x\tilde{\psi},
$$
where
$$
\tilde{\psi} = \psi(1).
$$

So we can also think of $H^1(G, A)$ as the space of maps $\tilde{\phi}: G \to A$ satisfying
$$
y\tilde{\phi}(y^{-1}z) - \tilde{\phi}(z) + \tilde{\phi}(y) = 0
$$
modulo the space of maps of the form
$$
\tilde{\phi}(y) = y\tilde{\psi} - \tilde{\psi}.
$$

By making the substitution $z = yw$, we can rewrite the constraint as
$$
\tilde{\phi}(y) - \tilde{\phi}(yw) + y\tilde{\phi}(w) = 0.
$$

If $A$ has the trivial $G$-action, then the constraint simplifies to
$$
\tilde{\phi}(y) - \tilde{\phi}(yw) + y\tilde{\phi}(w) = 0,
$$
and $\tilde{\psi} - y\tilde{\psi}$ is always zero. So in that case,
$$
H^1(G, A) = \operatorname{Hom}(G, A).
$$
