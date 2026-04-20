Let $K$ be a $p$-adic field.

>[!notes]+ Def 7.1
>
> We say that a proper smooth variety $X$ over $K$ has good reduction if it can be extended to a proper smooth scheme of finite type over $\mathcal{O}_K$.
>
> Otherwise, we say that it has bad reduction.

>[!example]+ ex 7.2
>
> If $p \neq 2$, then the elliptic curve $E$ over $K$ defined by $y^2 = x(x - 1)(x + 1)$ has good reduction, since $y^2 = x(x - 1)(x + 1)$ defines a nonsingular curve over $\mathcal{O}_K$. It is possible to show that $E$ does not have good reduction at $2$.

Recall that an elliptic curve over $\mathcal{O}_K$ is a pair $(E, O)$, where $E$ is a proper smooth scheme over $\mathcal{O}_K$ such that $E_K$ and $E_k$ are geometrically connected curves of genus $1$, and $O$ is an $\mathcal{O}_K$-point of $E$.

>[!tip]+ lemma 7.3
>
> Let $X$ be a proper scheme over $\mathcal{O}_K$. Then the restriction map $X(\mathcal{O}_K) \to X(K)$ is a bijection. In particular, there is a natural reduction map $X(K) \to X(k)$.
> 
>>Proof. This follows from the valuative criterion of properness.

>[!danger]+ Them 7.4
>
> If $E$ is an elliptic curve over $\mathcal{O}_K$, then there is an exact sequence
>
> $$
> 0 \to \hat{E}(\mathfrak{m}_K) \to E(K) \to E(k) \to 0
> $$

>[!done]+ Coro 7.5
>
> If $E$ is an elliptic curve over $\mathcal{O}_K$, and $\ell$ is a prime different form $\operatorname{char} K$, then the reduction maps
>
> $$
> E(K)[\ell^n] \to E(k)[\ell^n]
> $$
>
> and
>
> $$
> T_\ell(E_K) \to T_\ell(E_k)
> $$
>
> are isomorphisms.
>
>>Proof. For each $n$, there is an exact sequence
>>
>>$$
>>\hat{E}(\mathfrak{m}_K)[\ell^n] \to E(K)[\ell^n] \to E(k)[\ell^n] \to \hat{E}(\mathfrak{m}_K)/\ell^n
>>$$
>>
>>But multiplication by $\ell$ is invertible on $\hat{E}(\mathfrak{m}_K)$, so the outer terms are zero. So the maps $E(K)[\ell^n] \to E(k)[\ell^n]$ are isomorphisms. Taking the direct limit over algebraic extensions of $K$ and inverse limit over $n$ shows that $T_\ell(E_K) \to T_\ell(E_k)$ is an isomorphism.

>[!done]+ Coro 7.6
>
> If an elliptic curve $E$ over $K$ has good reduction, then $T_\ell(E)$ is unramified for every prime $\ell \neq p$.

The converse is also true, although we will not give a proof.

>[!danger]+ Them 7.7 (Néron-Ogg-Shafarevich)
>
> Let $\ell$ be a prime different from $p$. An elliptic curve $E$ over $K$ has good reduction if and only if $T_\ell(E)$ is unramified. More generally, an abelian variety $X$ over $K$ has good reduction if and only if $T_\ell(X)$ is unramified.

By contrast, $T_p(X)$ is never unramified. If $X$ is an elliptic curve, then it follows from the Weil pairing that $\wedge^2 T_\ell(X) \cong \mathbb{Z}_\ell(1)$, and we saw that this representation is ramified if $\ell = p$.

However, it is possible to determine if $X$ has good reduction from $T_p(X)$. The criterion uses the notion of a crystalline representation, which we will define in a later lecture.

>[!danger]+ Them 7.8
>
> An abelian variety $X$ over $K$ has good reduction if and only if $T_p(X) \otimes_{\mathbb{Z}_p} \mathbb{Q}_p$ is crystalline.

Before we move on, I want to do a little bit of $p$-adic analysis. Previously, we claimed that $\operatorname{Gal}(\mathbb{Q}_p(\mu_{p^n})/\mathbb{Q}_p) \cong (\mathbb{Z}/p^n\mathbb{Z})^\times$. We will now give a proof using the theory of Newton polygons. (It is possible to give a more elementary proof using Eisenstein's criterion, but the method of Newton polygons is more general, so it is useful to know.)

Let $K$ be a nonarchimedean field with absolute value $|\cdot|$. Define a "valuation" $v: K \to \mathbb{R} \cup \{\infty\}$ by $v(x) = -\log |x|$.

>[!notes]+ Def 7.9
>
> Let $f(x) = \sum_{i=0}^n a_i x^i$ be a polynomial with $a_0, a_n \neq 0$. The Newton polygon of $f$ is the lower envelope of the points $(i, v(a_i)) \in \mathbb{R}^2$.

>[!abstract]+ Prop 7.10
>
> Let
>
> $$
> f(x) = \prod_{i=1}^n (x - \alpha_i)
> $$
>
> with
>
> $$
> v(\alpha_1) \leq v(\alpha_2) \leq \cdots \leq v(\alpha_n)
> $$
>
> Then the slope of the segment of the Newton polygon beginning at $x = n - i$ and ending at $x = n - i + 1$ is $-v(\alpha_i)$.
>
>>Proof. Let $1 \leq m \leq n$. Then the coefficient of $x^{n-m}$ is the sum of all products of $m$ of the $\alpha_i$'s. Each term in the sum has valuation at least $\sum_{i=1}^m v(\alpha_i)$, so the valuation of the sum is at least this large. If $v(\alpha_m) < v(\alpha_{m+1})$, then only one term has this valuation, so the sum is exactly this large.

>[!done]+ Coro 7.11
>
> If $f(x)$, $g(x)$ are any polynomials with nonzero constant term, then the Newton polygon of $f(x)g(x)$ is obtained from the Newton polygons of $f(x)$ and $g(x)$ by rearranging segments in order of slope.

>[!abstract]+ Prop 7.12
>
> If a polynomial $f(x)$ is irreducible, then its Newton polygon has only one slope. Conversely, if $f$ has degree $n$ and the $y$-coordinates of the Newton polygon at $x = 1, \dots, n-1$ are not in the image of $v$, then $f$ is irreducible.
>
>>Proof. The first claim follows from Hensel's lemma; see [Bos14, Lemma 4] for the statement and proof of the lemma. The second claim follows from Corollary 7.11.

>[!example]+ ex 7.13
>
> The group $\operatorname{Gal}(\mathbb{Q}_p(\mu_{p^n})/\mathbb{Q}_p)$ must send a $p^n$th root of unity to another $p^n$th root of unity, so there is a natural injection $\operatorname{Gal}(\mathbb{Q}_p(\mu_{p^n})/\mathbb{Q}_p) \hookrightarrow (\mathbb{Z}/p^n\mathbb{Z})^\times$. To show that this map is an isomorphism, it suffices to show that both groups have the same number of elements.
>
> We claim that the polynomial
>
> $$
> \frac{(1 + T)^{p^n} - 1}{(1 + T)^{p^{n-1}} - 1}
> $$
>
> is irreducible. It has integer coefficients, and the coefficient of the constant term is $p$. If we normalize $v$ so that $v(p) = 1$, then the Newton polygon is the line segment from $(0,0)$ to $(p^n - p^{n-1}, 1)$. By Proposition 7.12, the polynomial is irreducible. So
>
> $$
> |\operatorname{Gal}(\mathbb{Q}_p(\mu_{p^n})/\mathbb{Q}_p)| = [\mathbb{Q}_p(\mu_{p^n}) : \mathbb{Q}_p] = p^n - p^{n-1} = |(\mathbb{Z}/p^n\mathbb{Z})^\times|
> $$
