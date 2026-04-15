
## 5. ELLIPTIC CURVES, CONTINUED

>[!notes]+ Definition 5.1.
>
>Let $(E,O)$, $(E',O')$ be elliptic curves over $K$. A morphism $(E,O) \to (E',O')$ is a morphism $E \to E'$ sending $O$ to $O'$.

> [!tip]+ Lemma 5.2
> 
> Any morphism $\phi: (E,O) \to (E',O')$ of elliptic curves is a group homomorphism.
> 
> *Proof.* If $\phi$ is constant, then it is a group homomorphism. Otherwise, $\phi$ is a finite locally free morphism, so there is an induced homomorphism $\phi_*: \mathrm{Pic}^0_{E/K} \to \mathrm{Pic}^0_{E'/K}$. Since we can identify $E,E'$ with $\mathrm{Pic}^0_{E/K}$, $\mathrm{Pic}^0_{E'/K}$, respectively, $\phi$ must also be a group homomorphism.

We will write $\mathrm{Hom}(E,E')$ for the set of morphisms $(E,O) \to (E',O')$, and $\mathrm{End}(E)$ for $\mathrm{Hom}(E,E')$. Lemma 5.2 implies that $\mathrm{End}(E)$ is a (not necessarily commutative) ring.

> [!tip]+ Lemma 5.3
> 
> Let $E$ be an elliptic curve.
> 1. $\mathrm{End}\, E$ has no zero divisors.
> 2. For any nonzero integer $n$, the multiplication by $n$ map $E \to E$ is not zero.
> 
> *Proof.* For the first item, observe that any nonzero element of $\mathrm{End}\, E$ is surjective, and the composition of two surjections is a surjection. For the second item, see [Sil09, Proposition III.4.2(a)].

Since the Picard functor is contravariant, any homomorphism $\phi: E \to E'$ also induces a homomorphism $\hat{\phi}: \mathrm{Pic}^0_{E'/K} \to \mathrm{Pic}^0_{E/K}$, or equivalently, a homomorphism $\hat{\phi}: E' \to E$.

> [!tip]+ Lemma 5.4
> 
> 1. For any $\phi \in \mathrm{Hom}(E,E')$, $\hat{\phi}\phi$ is multiplication by $\deg \phi$.
> 2. For any $\phi \in \mathrm{Hom}(E,E')$, $\psi \in \mathrm{Hom}(E',E'')$, $\widehat{\psi\phi} = \hat{\phi}\hat{\psi}$.
> 3. For any $\phi,\psi \in \mathrm{Hom}(E,E')$, $\widehat{\phi + \psi} = \hat{\phi} + \hat{\psi}$.
> 4. For any integer $n$, the image of $n$ in $\mathrm{Hom}(E,E)$ is self dual.
> 5. For any $\phi \in \mathrm{Hom}(E,E')$, $\deg \hat{\phi} = \deg \phi$.
> 6. $\hat{\hat{\phi}} = \phi$
> 
> *Proof.* See [Sil09, Theorem 6.1 and 6.2].

> [!done]+ Coro 5.5
> 
> The degree map $\deg: \mathrm{Hom}(E,E') \to \mathbb{Z}$ is a positive definite quadratic form.

> [!done]+ Coro 5.6
> 
> For any elliptic curve $E$, the multiplication by $N$ map has degree $N^2$.

For any positive integer $N$, let
$$
E(K^{\mathrm{sep}})[N] = \{ P \in E(K^{\mathrm{sep}}) \mid NP = 0 \}.
$$

> [!done]+ Coro 5.7
> 
> If the characteristic of $K$ does not divide $N$, then $E(K^{\mathrm{sep}})[N] \cong (\mathbb{Z}/N\mathbb{Z})^2$.

Note that $\mathrm{Gal}(K^{\mathrm{sep}}/K)$ acts on $E(K^{\mathrm{sep}})[N]$. For any prime $p$, define the Tate module
$$
T_p(E) = \varprojlim_n E(K^{\mathrm{sep}})[p^n].
$$

If the characteristic of $K$ is different from $p$, then $T_p(E)$ is a free $\mathbb{Z}_p$-module of rank 2.

> [!danger]+ Them 5.8
> 
> Suppose the characteristic of $K$ is different from $p$. Then the natural map
> $$
> \mathrm{Hom}(E,E') \otimes \mathbb{Z}_p \to \mathrm{Hom}_{\mathbb{Z}_p}(T_p(E), T_p(E'))
> $$
> is injective.
> 
> *Proof.* See [Sil09, Theorem III.7.4].

> [!done]+ Coro 5.9
> 
> $\mathrm{Hom}(E,E')$ is a free $\mathbb{Z}$-module of rank at most 4.

> [!done]+ Coro 5.10
> 
> $\mathrm{End}(E) \otimes \mathbb{Q}$ is isomorphic to one of the following:
> 1. $\mathbb{Q}$;
> 2. An imaginary quadratic extension of $\mathbb{Q}$;
> 3. A quaternion algebra over $\mathbb{Q}$, ramified at $p = \mathrm{char}\, K$ and $\infty$, and at no other places.

A quaternion algebra over $\mathbb{Q}$ is a division algebra $D$ with center $\mathbb{Q}$ satisfying $[D: \mathbb{Q}] = 4$. By "ramified at $p$ and $\infty$", we mean that $D \otimes \mathbb{Q}_p$ and $D \otimes \mathbb{R}$ are division algebras, while $D \otimes \mathbb{Q}_\ell \cong M_2(\mathbb{Q}_\ell)$ is the ring of $2 \times 2$ matrices for all $\ell \neq p$.

**Remark 5.11.** If $L$ is an extension of $K$, then $\mathrm{End}(E_L)$ can be larger than $\mathrm{End}(E)$. For example, if $E$ is the elliptic curve $y^2 = x^3 - x$ over $\mathbb{Q}$, then $\mathrm{End}\, E = \mathbb{Z}$, but $\mathrm{End}\, E_{\mathbb{Q}(i)} = \mathbb{Z}[i]$, where $i$ acts by $(x,y) \mapsto (-x,iy)$.

**Remark 5.12.** The action of $G_K$ on $T_p(E)$ commutes with endomorphisms of $E$. From the classification of Theorem 5.10 we deduce:
- If $\mathrm{End}(E) \otimes \mathbb{Q}$ is an imaginary quadratic extension $F$ of $\mathbb{Q}$, then the map $G_K \to \mathrm{End}(T_p(E))$ factors through $(\mathbb{Z}_p \otimes_{\mathbb{Q}} F)^\times$.
- If $\mathrm{End}(E) \otimes \mathbb{Q}$ is a quaternion algebra, then $G_K$ acts by scalars on $T_p(E)$.

**Remark 5.13.** Tate modules are closely related to étale cohomology. If $E$ is an elliptic curve over a field $K$, then
$$
H^i_{\text{ét}}(E_{\overline{K}}, \mathbb{Z}_p) =
\begin{cases}
\mathbb{Z}_p \quad (\text{with trivial } G_K\text{-action}), & i = 0 \\
\mathrm{Hom}_{\mathbb{Z}_p}(T_p(E), \mathbb{Z}_p), & i = 1 \\
\mathbb{Z}_p(-1), & i = 2 \\
0, & \text{otherwise}.
\end{cases}
$$

---
## 6. ELLIPTIC CURVES, CONTINUED

Étale cohomology is supposed to satisfy many of the same properties as singular cohomology. In particular, it is expected to satisfy Poincaré duality. For elliptic curves, this means that there should be an antisymmetric cup product map
$$
H^1_{\text{ét}}(E_{\overline{K}}, \mathbb{Z}_p) \times H^1_{\text{ét}}(E_{\overline{K}}, \mathbb{Z}_p) \to H^2_{\text{ét}}(E_{\overline{K}}, \mathbb{Z}_p)
$$
that is a perfect pairing. Since
$$
H^1_{\text{ét}}(E_{\overline{K}}, \mathbb{Z}_p) = T_p(E)^*
$$
$$
H^2_{\text{ét}}(E_{\overline{K}}, \mathbb{Z}_p) = \mathbb{Z}_p(-1),
$$
specifying the cup product map is equivalent to specifying a perfect pairing
$$
T_p(E) \times T_p(E) \to \mathbb{Z}_p(1).
$$
This map can be constructed using the Weil pairing.

For each $N$ and each extension $L$ of $K$, there is a Weil pairing
$$
e_N: E(L)[N] \times E(L)[N] \to \mu_N(L).
$$
It can be defined as follows. Let $P,Q \in E(L)[N]$. Then
$$
\sum_{m=0}^{N-1} ([P + mQ] - [mQ])
$$
is a principal divisor. Let $g$ be a function with this divisor. Let $T_Q g$ denote the translation of $g$ by $Q$. Then $T_Q g$ and $g$ have the same divisor, so $T_Q g = \omega g$ for some constant $\omega$. Since $T_Q^N$ is the identity, $\omega$ is an $N$th root of unity. We define $e_N(P,Q) = \omega$.

> [!danger]+ Them 6.1
> 
> The Weil pairing has the following properties:
> 1. It is bilinear:
>    $$
>    e_N(P + Q,R) = e_N(P,R) + e_N(Q,R), \quad e_N(P,Q + R) = e_N(P,Q) + e_N(P,R)
>    $$
> 2. It is alternating:
>    $$
>    e_N(P,P) = 1
>    $$
> 3. If $N$ does not divide the characteristic of $K$, then it is a perfect pairing.
> 4. It is $\mathrm{Aut}(L/K)$-invariant: for $\sigma \in \mathrm{Aut}(L/K)$,
>    $$
>    e_N(P^\sigma, Q^\sigma) = e_N(P,Q)^\sigma
>    $$
> 5. The Weil pairings for various $N$ are compatible: if $P \in E(L)[MN], Q \in E(L)[M]$,
>    $$
>    e_{MN}(P,Q) = e_M(NP,Q).
>    $$

If the characteristic of $K$ is not $p$, then we can take inverse limits to get a perfect pairing
$$
T_p(E) \times T_p(E) \to \mathbb{Z}_p(1).
$$
(Recall that $\mathbb{Z}_p(1) = \varprojlim_n \mu_{p^n}(K^{\mathrm{sep}})$, where $\mu_{p^n}(K^{\mathrm{sep}})$ is the group of $p^n$th roots of unity of $K^{\mathrm{sep}}$.)

We are particularly interested in elliptic curves over $p$-adic fields. We still need to define what these are.

>[!notes]+ Def 6.2.
>
>A nonarchimedean field is a field $K$ that is complete with respect to a norm $|\cdot|: K \to \mathbb{R}^{\geq 0}$ such that:
> - $|xy| = |x||y|$ and $|x + y| \leq \max(|x|,|y|)$ for all $x,y \in K$
> - $|0| = 0$, $|1| = 1$
> - $0 < |x| < 1$ for some $x \in K$
> 
>We will write
>$$
>\mathcal{O}_K = \{ x \in K \mid |x| \leq 1 \}
>$$
>$$
>\mathfrak{m}_K = \{ x \in K \mid |x| < 1 \}.
>$$
>
>We say that $K$ is discretely valued if the image of $K^\times$ under $|\cdot|$ is a discrete subset of $\mathbb{R}^{>0}$. Equivalently,
>$$
>\sup_{x \in \mathfrak{m}_K} |x| < 1.
>$$

> [!example]+ ex 6.3
> 
> Let $p$ be a prime. We can define a norm $|\cdot|$ on $\mathbb{Q}$ by $|p^m \frac{r}{s}| = p^{-m}$ for all integers $r,s$ not divisible by $p$. Then $\mathbb{Q}_p$ is defined to be the completion of $\mathbb{Q}$ with respect to this norm. It is a nonarchimedean field.

> [!tip]+ Lemma 6.4
> 
> Let $K$ be a nonarchimedean field, and let $L/K$ be an algebraic extension. Then there is a unique nonarchimedean absolute value on $L$ extending the absolute value on $K$.
> 
> *Proof.* See [Bos14, Theorem A.3].

**Remark 6.5.** If $L/K$ is finite, and the norms on $K,L$ are denoted by $|\cdot|_K, |\cdot|_L$, respectively, then
$$
|x|_L = |N_{L/K}(x)|_K^{1/[L:K]}.
$$
It takes some work to show that the right-hand side satisfies the triangle inequality.

> [!done]+ Coro 6.6
> 
> Any finite extension of $\mathbb{Q}_p$ is nonarchimedean, as is the completion of any infinite algebraic extension of $\mathbb{Q}_p$.

>[!notes]+ Def 6.7. 
>
>A field $K$ is perfect if every irreducible polynomial in $K[x]$ is separable.

> [!abstract]+ Prop 6.8
> 
> Every field of characteristic 0 is perfect. A field of characteristic $p > 0$ is perfect iff every element is a $p$th power.

For the remainder of the lecture, we will fix a prime $p$.

>[!notes]+ Def 6.9.  
>
>A $p$-adic field is a discretely valued nonarchimedean field $K$ of characteristic zero, such that its residue field $\mathcal{O}_K/\mathfrak{m}_K$ is perfect of characteristic $p$.

> [!example]+ ex 6.10
> 
> The field $\mathbb{Q}_p$ is a $p$-adic field, as is any finite extension of $\mathbb{Q}_p$. The completion of an infinite algebraic extension of $\mathbb{Q}_p$ may or may not be a $p$-adic field.

Let $K$ be a $p$-adic field, and let $k = \mathcal{O}_K/\mathfrak{m}_K$ be its residue field. There is a surjection $\mathrm{Gal}(\overline{K}/K) \to \mathrm{Gal}(\overline{k}/k)$. The $kernel$ is called the inertia subgroup of $\mathrm{Gal}(\overline{K}/K)$.

>[!notes]+ Def 6.11. 
>
>We say that a representation of $\mathrm{Gal}(\overline{K}/K)$ is unramified if it factors through $\mathrm{Gal}(\overline{k}/k)$. Otherwise, we say that it is ramified.

> [!example]+ ex 6.12
> 
> For $\ell \neq p$, $\mathbb{Z}_\ell(1)$ is unramified, since all $\ell$-power roots of unity in $\overline{K}$ have distinct images in $\overline{k}$. But $\mathbb{Z}_p(1)$ is ramified since all $p$-power roots of unity in $\overline{K}$ map to 1 in $\overline{k}$.
---
