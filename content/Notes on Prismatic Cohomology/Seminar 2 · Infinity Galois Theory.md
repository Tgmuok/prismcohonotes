>[!notes]+ Def 2.1
>
> Let $L/K$ be extension of fields. Let $\operatorname{Aut}(L/K)$ denote the group of automorphisms of $L$ fixing each element of $K$.
>
> Give $\operatorname{Aut}(L/K)$ the weakest topology such that the stabilizer of any finite subset of $L$ is open.

>[!example]+ ex 2.2
>
> The group $\operatorname{Aut}(\mathbb{Q}(\sqrt{2})/\mathbb{Q})$ has two elements. The nontrivial element sends $\sqrt{2} \mapsto -\sqrt{2}$.

>[!example]+ ex 2.3
>
> The group $\operatorname{Aut}(\mathbb{Q}(\sqrt[3]{2})/\mathbb{Q})$ is trivial. If $\omega$ is a nontrivial cube root of unity, then $\operatorname{Aut}(\mathbb{Q}(\sqrt[3]{2},\omega)/\mathbb{Q})$ permutes $\{\sqrt[3]{2},\omega\sqrt[3]{2},\omega^2\sqrt[3]{2}\}$, and this permutation action induces an isomorphism $\operatorname{Aut}(\mathbb{Q}(\sqrt[3]{2},\omega)/\mathbb{Q}) \cong S_3$.

>[!example]+ ex 2.4
>
> Let $p$ be a prime number. For each positive integer $n$, there is a field $\mathbb{F}_{p^n}$ with $p^n$ elements. It is unique up to isomorphism. We have $\operatorname{Aut}(\mathbb{F}_{p^n}/\mathbb{F}_p) \cong \mathbb{Z}/n\mathbb{Z}$, where the Frobenius automorphism $x \mapsto x^p$ corresponds to the element $1 \in \mathbb{Z}/n\mathbb{Z}$. Then
>
> $$
> \operatorname{Aut}(\overline{\mathbb{F}}_p/\mathbb{F}_p) = \widehat{\mathbb{Z}} = \varprojlim_n \mathbb{Z}/n\mathbb{Z}
> $$
>

>[!example]+ ex 2.5
>
> For each positive integer $n$, there is a field $\mathbb{Q}(\mu_{p^n})$ obtained by adjoining all $p$-power roots of unity to $\mathbb{Q}$. There is an isomorphism
>
> $$
> \operatorname{Aut}(\mathbb{Q}(\mu_{p^n})/\mathbb{Q}) \cong (\mathbb{Z}/p^n\mathbb{Z})^\times
> $$
>
> $$
> (\zeta \mapsto \zeta^m) \leftrightarrow m.
> $$
>
> Let
>
> $$
> \mathbb{Q}(\mu_{p^\infty}) = \varinjlim_n \mathbb{Q}(\mu_{p^n}).
> $$
>
> Then
>
> $$
> \operatorname{Aut}(\mathbb{Q}(\mu_{p^\infty})/\mathbb{Q}) \cong \varprojlim_n \mathbb{Z}/p^n\mathbb{Z} = \mathbb{Z}_p^\times.
> $$
>
> Similarly,
>
> $$
> \operatorname{Aut}(\mathbb{Q}_p(\mu_{p^\infty})/\mathbb{Q}_p) \cong \mathbb{Z}_p^\times.
> $$
>

>[!example]+ ex 2.6
>
> Let $K$ be a field. Then $\operatorname{Aut}(K(t)/K) = \operatorname{PGL}_2(K)$, with the discrete topology.

>[!tip]+ lemma 2.7
>
> If $L/K$ is finite, then $\operatorname{Aut}(L/K)$ has the discrete topology.
>
> Proof. Choose a $K$-vector space basis for $L$. An automorphism of $L$ fixing this basis must be the identity.

>[!tip]+ lemma 2.8
>
> If $L/K$ is algebraic, then the map
>
> $$
> \operatorname{Aut}(L/K) \to \varprojlim_{K'} \operatorname{Aut}(K'/K)
> $$
>
> is an isomorphism of topological groups, where $K'$ runs over $\operatorname{Aut}(L/K)$-stable finite extensions of $K$.
>
> Proof. Since $L/K$ is algebraic, any $\alpha \in L$ has finite orbit under $\operatorname{Aut}(L/K)$. So the field obtained by adjoining the orbit of $\alpha$ to $K$ is a finite $\operatorname{Aut}(L/K)$-stable extension of $K$. Specifying compatible automorphisms of each $K'$ is equivalent to specifying an automorphism of $L$.

>[!notes]+ Def 2.9
>
> A topological space is profinite if it is the inverse limit of a collection of finite sets having the discrete topology.

>[!tip]+ lemma 2.10 ([Sta, Tag 08ZY])
>
> A topological space is profinite if and only if it is totally disconnected and compact.
>
> If $H$ is a group acting on a field $K$, we denote by $K^H$ the subfield of $K$ fixed by $H$.

>[!notes]+ Def 2.11
>
> We say that $L/K$ is Galois if it is algebraic and $L^{\operatorname{Aut}(L/K)} = K$.
>
> If $L/K$ is Galois, then we will also denote $\operatorname{Aut}(L/K)$ by $\operatorname{Gal}(L/K)$.

>[!example]+ ex 2.12
>
> Of the extensions mentioned in Examples 2.2–2.5：
> 
> $\mathbb{Q}(\sqrt{2})/\mathbb{Q}$, $\mathbb{Q}(\sqrt[3]{2},\omega)/\mathbb{Q}$, $\overline{\mathbb{F}}_p/\mathbb{F}_p$, $\mathbb{Q}(\mu_{p^\infty})/\mathbb{Q}$, $\mathbb{Q}_p(\mu_{p^\infty})/\mathbb{Q}_p$ 
> 
> are Galois. The extension $\mathbb{Q}(\sqrt[3]{2})/\mathbb{Q}$ is not Galois since the fixed field of the automorphism group is $\mathbb{Q}(\sqrt[3]{2})$. The extension $K(t)/K$ is not Galois since it is not algebraic.
>
> There is a more concrete characterization of Galois extensions in terms of splitting fields.

>[!notes]+ Def 2.13
>
> Let $K$ be a field. A polynomial $f(x) \in K[x]$ factors completely if it can be written in the form $f(x) = c\prod_{i=1}^n (x-x_i)$ with $n \in \mathbb{Z}_{\geq 0}$, $c,x_1,\dots,x_n \in K$ and $c \neq 0$.

>[!notes]+ Def 2.14
>
> Let $L/K$ be an algebraic extension, and let $P \subset K[x] \setminus \{0\}$. We say that $L$ is a splitting field for $P$ if every element of $P$ factors completely over $L$, and no proper subfield of $L$ has this property.

>[!tip]+ lemma 2.15
>
> Every subset of $K[x] \setminus \{0\}$ admits a splitting field. It is unique up to isomorphism.
>
> Proof. First, suppose $P$ consists of a single element $f(x)$. Then we can construct a splitting field inductively as follows. Letting $K_0 = K$, and for $i \geq 0$, let $f_i(x)$ be an irreducible factor of $f(x)$ of degree $> 1$ over $K_i[x]$, and let $K_{i+1} = K[x]/f_i(x)$. Eventually, $f(x)$ factors completely in some $K_n$, and this $K_n$ is a splitting field for $\{f(x)\}$.
>
> If $L$ is any splitting field of $\{f(x)\}$, we can construct an isomorphism $K_n \xrightarrow{\sim} L$ as follows. For each $i$, we construct an embedding $K_{i+1} \hookrightarrow L$ by sending the generator of $K_{i+1}$ to some root of the polynomial $f_i(x)$ in $L$ (using the map $K_i \hookrightarrow L$ to consider $f_i(x)$ as an element of $L[x]$). Since $f$ does not factor completely over any subfield of $L$, $K_n \to L$ must be surjective, hence an isomorphism.
>
> To prove the lemma for arbitrary $P$, we use Zorn's lemma.

>[!notes]+ Def 2.16
>
> A polynomial $f(x) \in K[x]$ is separable if $f(x)$ and $f'(x)$ generate the unit ideal.

>[!tip]+ lemma 2.17
>
> Suppose the polynomial $f(x) \in K[x]$ factors completely. The factors are distinct if and only if $f$ is separable.
>
> Proof. Suppose $f(x)$ is divisible by $(x-\alpha)^2$ for some $\alpha \in K$. Then $f'(x)$ is divisible by $x-\alpha$. So $(f(x),f'(x)) \subset (x-\alpha)$.
>
> Conversely, suppose $f(x) = \prod_{i=1}^n (x-\alpha_i)$ has no repeated factors. By the Chinese remainder theorem, $f(x)$ and $f'(x)$ generate the unit ideal if and only if $f'(\alpha_i) \neq 0$ for all $i$. In fact, we have
>
> $$
> f'(\alpha_i) = \prod_{j \neq i} (\alpha_i - \alpha_j) \neq 0.
> $$
>

>[!tip]+ lemma 2.18
>
> An extension $L/K$ is Galois iff it is the splitting field of a set of separable polynomials.
>
> Proof. Suppose $L/K$ is Galois. Let $\alpha \in L$. Then $\alpha$ is a zero of some polynomial over $K$. Any element of the $\operatorname{Gal}(L/K)$-orbit of $\alpha$ is also a zero of this polynomial. So the orbit is finite. Let $\{\alpha_1 = \alpha, \alpha_2, \dots, \alpha_n\}$ be the orbit. Then
>
> $$
> \prod_{i=1}^n (x - \alpha_i)
> $$
>
> is a polynomial that is $\operatorname{Gal}(L/K)$-invariant. Since $L/K$ is Galois, the polynomial has coefficients in $K$. Then $L$ is a splitting field for the set of all polynomials that can be constructed in this way.
>
> Conversely, suppose $L/K$ is the splitting field of a set of separable polynomials over $K$. WLOG we may assume that they are irreducible over $K$. If $\alpha, \alpha' \in L$ are two roots of the same irreducible polynomial, then the construction of Lemma 2.15 produces an automorphism of $L$ fixing $K$ and sending $\alpha$ to $\alpha'$.

>[!tip]+ lemma 2.19
>
> Let $L/K$ be a Galois extension. If $K'$ is a subfield of $L$ containing $K$, then $L/K'$ is Galois, and $\operatorname{Gal}(L/K')$ is closed in $\operatorname{Gal}(L/K)$.
>
> Proof. By Lemma 2.18, $L$ is a splitting field for some set of polynomials over $K$. Then $L$ is a splitting field for the same set of polynomials over $K'$, so $L/K'$ is Galois.
>
> By Lemma 2.10, $\operatorname{Gal}(L/K')$ and $\operatorname{Gal}(L/K)$ are compact Hausdorff spaces. So $\operatorname{Gal}(L/K')$ must be closed in $\operatorname{Gal}(L/K)$.

>[!tip]+ lemma 2.20
>
> If $L$ is a field and $H \subset \operatorname{Aut} L$ is a finite subgroup, then the map $H \to \operatorname{Gal}(L/L^H)$ is an isomorphism.
>
> Proof. The map is injective, so it suffices to prove that $|H| \geq |\operatorname{Gal}(L/L^H)|$. From the construction of Lemma 2.15, we see that $|\operatorname{Gal}(L/L^H)| = [L : L^H]$. We will show that $[L : L^H] \leq |H|$.
>
> Let $H = \{\sigma_1 = 1, \sigma_2, \dots, \sigma_n\}$. Let $\alpha_1, \dots, \alpha_{n+1} \in L$. The system
>
> $$
> \sum_{j=1}^{n+1} \sigma_i(\alpha_j) X_j = 0
> $$
>
> has $n + 1$ variables and $n$ equations, so it has a nonzero solution. Among all solutions, choose a solution $(c_1, \dots, c_{n+1})$ with the fewest nonzero elements. After reordering the $\alpha_j$ and multiplying by a scalar, we may assume $c_1 \neq 0$ and $c_1 \in F$. For any $i$,
>
> $$
> (c_1 - \sigma(c_1), \dots, c_{n+1} - \sigma(c_{n+1}))
> $$
>
> is a solution to (2.21) with fewer nonzero terms, so it must be zero. So the $c_j$'s are all in $F$, and $\alpha_1, \dots, \alpha_{n+1}$ are linearly dependent over $F$. Therefore, $[L : L^H] \leq |H|$, as desired.

>[!danger]+ Them 2.22 (Fundamental theorem of infinite Galois theory)
>
> There is a bijection between closed subgroups $H$ of $\operatorname{Gal}(L/K)$ and subfields $K'$ of $L$ containing $K$, given by
>
> $$
> H \mapsto L^H
> $$
>
> $$
> K' \mapsto \operatorname{Gal}(L/K').
> $$
>
> Proof. By Lemma 2.19, for any subfield $K'$ of $L$ containing $K$, $L^{\operatorname{Gal}(L/K')} = L$.
>
> Conversely, suppose $H$ is a closed subgroup of $\operatorname{Gal}(L/K)$, and suppose $\sigma \in \operatorname{Gal}(L/K) \setminus H$. Since $H$ is closed, we can find some finite Galois extension $K''$ of $K$ such that the action of $\sigma$ on $K''$ does not agree with the action of any element of $H$. By Lemma 2.20, $\sigma$ cannot fix $(K'')^H$. So it cannot fix $L^H$. Therefore, $H \to \operatorname{Gal}(L/L^H)$ is an isomorphism.

>[!notes]+ Def 2.23
>
> A separable closure of a field $K$ is a splitting field for the set of all separable polynomials in $K[x]$.
> 
> We denote a separable closure of $K$ by $K^{\mathrm{sep}}$. We will sometimes write $G_K$ for $\operatorname{Gal}(K^{\mathrm{sep}}/K)$. If $K$ has characteristic zero, then a separable closure is the same thing as an algebraic closure.
