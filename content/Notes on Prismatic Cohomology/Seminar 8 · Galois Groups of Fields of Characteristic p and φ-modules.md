It is difficult to write down Galois groups explicitly, which in turn makes it difficult to write down Galois representations explicitly. To deal with this problem, we will introduce $\varphi$-modules and $(\varphi,\Gamma)$-modules, which can be described more explicitly. We will show that categories of these modules are equivalent to categories of Galois representations.

We will exploit the fact that the absolute Galois groups of $p$-adic fields are closely related to the absolute Galois groups of characteristic $p$ fields. For example, we have the following result, which will be proved in a later lecture.

>[!danger]+ Them 8.1
>
>The absolute Galois groups of $\mathbb{Q}_p(\mu_{p^\infty})$ and $\mathbb{F}_p((t))$ are isomorphic (as topological groups).

Now let $E$ be a field of characteristic $p$. Let $G_E = \operatorname{Gal}(E^{\mathrm{sep}}/E)$. Let $\varphi_E: E \to E$ be the Frobenius map $x \mapsto x^p$.

Given an $E$-module $M$, we write $\varphi_E^*(M)$ for its Frobenius pullback $E \otimes_{\varphi_E,E} M$. Any $\varphi_E$-semilinear map $\varphi_M: M \to M$ determines an $E$-linear map $\varphi_E^*(M) \to M$ by $e \otimes m \mapsto e\varphi_M(m)$.

>[!notes]+ Def 8.2
>
>A $\varphi$-module over $E$ is a pair $(M,\varphi_M)$, where $M$ is a finite-dimensional $E$-vector space and $\varphi_M$ is a $\varphi_E$-semilinear endomorphism. We say that $(M,\varphi_M)$ is étale if the $E$-linear map $\varphi_E^*(M) \to M$ induced by $\varphi$ is an isomorphism (equivalently, the image of $\varphi_M$ generates $M$ as an $E$-module).

We will denote the category of étale $\varphi$-modules over $E$ by $\varphi\text{-}\mathrm{Mod}_E^{\text{ét}}$.

Let $\mathrm{Rep}_{\mathbb{F}_p}(G_E)$ denote the category of continuous finite-dimensional $\mathbb{F}_p$-vector space representations of $G_E$.

>[!danger]+ Them 8.3
>
>The functor $D_E: \mathrm{Rep}_{\mathbb{F}_p}(G_E) \to \varphi\text{-}\mathrm{Mod}_E^{\text{ét}}$ defined by
>$$
>V \mapsto (V \otimes_{\mathbb{F}_p} E^{\mathrm{sep}})^{G_E}.
>$$
>and the functor $V_E: \varphi\text{-}\mathrm{Mod}_E^{\text{ét}} \to \mathrm{Rep}_{\mathbb{F}_p}(G_E)$ defined by
>$$
>M \mapsto (M \otimes_E E^{\mathrm{sep}})^{\varphi=1}.
>$$
>determine an equivalence of categories between $\mathrm{Rep}_{\mathbb{F}_p}(G_E)$ and $\varphi\text{-}\mathrm{Mod}_E^{\text{ét}}$.

 **Remark 8.4.** There are a few advantages to working with $\varphi$-modules rather than Galois representations. One is that Galois groups are difficult to describe explicitly, while a $\varphi$-module is described by a matrix with coefficients in $E$. Another reason is that $\varphi$-modules are better suited to working with families of Galois representations. For example, for any $\alpha \in \mathbb{F}_q^\times$, there is a representation $\operatorname{Gal}(\overline{\mathbb{F}}_p/\mathbb{F}_p) \to \mathbb{F}_q^\times$ sending the Frobenius to $\alpha$. We might like to combine these into a representation $\operatorname{Gal}(\overline{\mathbb{F}}_p/\mathbb{F}_p) \to \mathbb{F}_p[t,t^{-1}]^\times$, but this does not work because we cannot raise $t$ to powers in $\widehat{\mathbb{Z}}$. On the other hand, the $\varphi$-module corresponding to $\alpha$ is a 1-dimensional $\mathbb{F}_q$-vector space on which $\varphi$ acts by $\alpha^{-1}$. These combine nicely into a free $\mathbb{F}_p[t,t^{-1}]$-module of rank 1 on which $\varphi$ acts by $t^{-1}$.

**Remark 8.5.** One might think of Theorem 8.3 as a characteristic $p$ version of the Riemann-Hilbert correspondence, with the Frobenius action replacing the connection. For a more geometric analogue, see [Kat73, Proposition 4.1.1].

>[!tip]+ lemma 8.6 (Galois descent)
>
>Let $L/K$ be a Galois extension of fields (of any characteristic). Let $V$ be a finite-dimensional $L$-vector space equipped with a semilinear $\operatorname{Gal}(L/K)$-action (meaning that the identities
>$$
>\sigma(v_1 + v_2) = \sigma(v_1) + \sigma(v_2)
>$$
>$$
>\sigma(\lambda v_1) = \sigma(\lambda)\sigma(v_1)
>$$
>hold for for each $\sigma \in \operatorname{Gal}(L/K), v_1,v_2 \in V, \lambda \in L$).
>
>Suppose that for each $v \in V$, the stabilizer of $v$ in $\operatorname{Gal}(L/K)$ is open. Then the natural map
>$$
>L \otimes_K V^{\operatorname{Gal}(L/K)} \to V
>$$
>is an isomorphism.
>
>>Proof. The case of $L/K$ finite is [Sil09, Lemma II.5.8.1]. In general, we use the fact that a basis for $V$ has open stabilizer to reduce to the finite case.

>Proof of Theorem 8.3. Let $V \in \mathrm{Rep}_{\mathbb{F}_p}(G_E)$. We will check that $D_E(V) \in \varphi\text{-}\mathrm{Mod}_E^{\text{ét}}$, and that there is a natural isomorphism $V_E(D_E(V)) \xrightarrow{\sim} V$. By Galois descent, the $\varphi$- and $G_E$-equivariant map
>$$
>D_E(V) \otimes_E E^{\mathrm{sep}} \to V \otimes_{\mathbb{F}_p} E^{\mathrm{sep}}
>$$
>is an isomorphism. Therefore, $\dim_E D_E(V) = \dim_{\mathbb{F}_p} V$; in particular, $D_E(V)$ is finite dimensional.
>
To show that $D_E(V)$ is étale, we just need to check that the matrix of Frobenius in some (equivalently, any) basis is invertible. By base change, the matrix of Frobenius on $D_E(V)$ is invertible iff the matrix of Frobenius on $D_E(V) \otimes_E E^{\mathrm{sep}} = V \otimes_{\mathbb{F}_p} E^{\mathrm{sep}}$ is invertible iff the matrix of Frobenius on $V$ is invertible. The action of Frobenius on $V$ is the identity.
>
Taking $\varphi$-invariants of (8.7) gives an isomorphism $V_E(D_E(V)) \xrightarrow{\sim} V$.
>
>Now let $M \in \varphi\text{-}\mathrm{Mod}_E^{\text{ét}}$. We want to show that the natural map
>$$
>E^{\mathrm{sep}} \otimes_{\mathbb{F}_p} V_E(M) \to E^{\mathrm{sep}} \otimes_E M
>$$
>is an isomorphism. First we will show that it is injective. It suffices to show that if some vectors in $V_E(M) = (E^{\mathrm{sep}} \otimes_E M)^{\varphi=1}$ are linearly independent over $\mathbb{F}_p$, then they are also linearly independent over $E^{\mathrm{sep}}$. Suppose that there is a minimal counterexample $v_1,\dots,v_r \in V_E(M)$, with $\sum_{i=1}^r a_i v_i = 0$ for $a_i \in E^{\mathrm{sep}}$. WLOG we may take $a_1 = 1$. Using $\varphi(v_i) = v_i$ and $\varphi(a_1) = a_1$, we obtain $0 = \sum_{i=2}^r (a_i - \varphi(a_i))v_i$. By minimality of the counterexample, we must have $(a_i - \varphi(a_i)) = 0$ for all $i$. Hence $a_i \in \mathbb{F}_p$ for all $i$, which is a contradiction. Note that we did not need to use the fact that $M$ is étale to prove injectivity.
>
>Now we show that (8.8) is surjective. Let $c_{ij}$ be the matrix coefficients of Frobenius in some basis. Let $X$ be the scheme over $E$ defined by the equations
>$$
>x_i^p = \sum_j c_{ij} x_j.
>$$
>Surjectivity of (8.8) is equivalent to $|X(E^{\mathrm{sep}})| = p^{\dim_E M}$. Since $X$ is finite locally free over $\operatorname{Spec} E$ of degree $p^{\dim_E M}$, it suffices to show that $X$ is étale over $E$, or equivalently that $\Omega_{X/E} = 0$. The module $\Omega_{X/E}$ is generated by the $dx_i$ subject to the relations $\sum_j c_{ij} x_j = 0$. Since the $c_{ij}$ define an invertible matrix, $\Omega_{X/E} = 0$. This concludes the proof that (8.8) is an isomorphism.
>
>From (8.8), we see that $V_E(M)$ is finite dimensional over $\mathbb{F}_p$. Then $V_E(M) = (M \otimes_E F)^{\varphi=1}$ for some finite separable extension $F/E$, so the $G_E$-action on $V_E(M)$ is continuous. Therefore $V_E(M) \in \mathrm{Rep}_{\mathbb{F}_p} G_E$. Taking Galois invariants of (8.8) gives an isomorphism $D_E(V_E(M)) \xrightarrow{\sim} M$. Hence we have shown that the functors $D_E$ and $V_E$ are essential inverses of each other.
