
Let $X$ be a proper variety over a $p$-adic field $K$. Recall the comparison isomorphism

$$
H_{\mathrm{dR}}^n(X) \otimes_K B_{\mathrm{dR}} \cong H_{\mathrm{ét}}^n(X_{\overline{K}}, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} B_{\mathrm{dR}}.
\tag{19.1}
$$

This is an isomorphism of filtered vector spaces with $G_K$-action. Here, $B_{\mathrm{dR}}$ has the usual filtration, $H_{\mathrm{ét}}^n(X_{\overline{K}}, \mathbb{Z}_p)$ has the trivial filtration, and the filtration on $H_{\mathrm{dR}}^n(X)$ is given by

$$
\mathrm{Fil}^i H_{\mathrm{dR}}^n(X) = \mathrm{im} \left( \left( H^n(X, \sigma_{\geq i} \Omega_{X/K}^\bullet) \to H^n(X, \Omega_{X/K}^\bullet) \right) \right).
$$

Here, $\sigma_{\geq i} \Omega_{X/K}^\bullet$ is the complex

$$
\Omega_{X/K}^i \to \Omega_{X/K}^{i+1} \to \dots \to \Omega_{X/K}^{\dim X}.
$$

For each $i$, there is a natural long exact sequence

$$
\dots \to H^n(X, \sigma_{\geq i} \Omega_{X/K}^\bullet) \to H^n(X, \sigma_{\geq i-1} \Omega_{X/K}^\bullet) \to H^n(X, \Omega_{X/K}^i[-i]) \to \dots
$$

It is possible to show that the boundary maps are zero. Hence we can show by induction that the maps

$$
H^n(X, \sigma_{\geq i} \Omega_{X/K}^\bullet) \to H^n(X, \Omega_{X/K}^\bullet)
$$

are injective. So we can identify $\mathrm{Fil}^i H_{\mathrm{dR}}^n(X)$ with $H^n(X, \sigma_{\geq i} \Omega_{X/K}^\bullet)$, and

$$
\mathrm{gr}^i H_{\mathrm{dR}}^n(X) \cong H^n(X, \Omega_{X/K}^i[-i]) = H^{n-i}(X, \Omega_{X/K}^i).
$$

Taking the zeroth graded piece of (19.1) gives an isomorphism

$$
\bigoplus_{i=0}^n H^{n-i}(X, \Omega_{X/K}^i) \otimes_K C(-i) \cong H_{\mathrm{ét}}^n(X_{\overline{K}}, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} C.
\tag{19.2}
$$

>[!notes]+ Def
>
> An *abelian variety* over $K$ is proper group scheme over $K$ that is geometrically reduced and irreducible.

If $X$ is an abelian variety, then the decomposition (19.2) can actually be made fairly explicit. In that case, all cohomology groups are wedge powers of $H^1$, so it suffices to consider $n = 1$. Furthermore, $H_{\mathrm{ét}}^1(X_{\overline{K}}, \mathbb{Z}_p)$ is dual to the Tate module $T_p(X) := \varprojlim_n X(\overline{K})[p^n]$. Therefore, giving a $C$-linear map $H^0(X, \Omega_{X/K}^1) \otimes_K C(-1) \to H_{\mathrm{ét}}^1(X_{\overline{K}}, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} C$ is equivalent to giving a map

$$
H^0(X, \Omega_{X/K}^1) \times T_p(X) \to C(1)
$$

that is $K$-linear in the first variable and $\mathbb{Z}_p$-linear in the second.

We will sketch the construction of the map, but we refer the reader to [Fon82] for the technical details.

Let $\mathfrak{X}$ be a proper flat model of $X$ over $\mathcal{O}_K$. Recall that we defined

$$
\Omega^{(1)} = \Omega_{\mathcal{O}_{\overline{K}}/\mathcal{O}_K}^1.
$$

We can define a map

$$
H^0(\mathfrak{X}, \Omega_{\mathfrak{X}/\mathcal{O}_K}^1) \times \mathfrak{X}(\mathcal{O}_{\overline{K}}) \to \Omega^{(1)}
$$

$$
(\omega, x) \mapsto x^*(\omega).
$$

It is possible to use the group law on the generic fiber show that for some $r$, the restriction

$$
p^r H^0(\mathfrak{X}, \Omega_{\mathfrak{X}/\mathcal{O}_K}^1) \times \mathfrak{X}(\mathcal{O}_{\overline{K}}) \to \Omega^{(1)}
$$

is bilinear.

By the valuative criterion of properness, $\mathfrak{X}(\mathcal{O}_{\overline{K}}) = X(K)$. Using $\mathrm{Hom}(\mathbb{Q}_p/\mathbb{Z}_p, X(K)) \cong T_p(X)$ and $\mathrm{Hom}(\mathbb{Q}_p/\mathbb{Z}_p, \Omega^{(1)}) \cong \ker \Theta_K / (\ker \Theta_K)^2$, we obtain a map

$$
p^r H^0(\mathfrak{X}, \Omega_{\mathfrak{X}/\mathcal{O}_K}^1) \times T_p(X) \to (\ker \Theta_K)/(\ker \Theta_K)^2.
$$

Finally, we invert $p$ to get a bilinear map

$$
H^0(X, \Omega_{X/K}^1) \times T_p(X) \to C(1).
$$

Now we have a constructed map (which can be shown to be injective)

$$
H^0(X, \Omega_{X/K}^1) \otimes_K C(-1) \hookrightarrow H_{\mathrm{ét}}^1(X_{\overline{K}}, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} C.
\tag{19.3}
$$

If $X^\vee$ is the dual abelian variety, then we get a map

$$
H^0(X^\vee, \Omega_{X^\vee/K}^1) \otimes_K C(-1) \hookrightarrow H_{\mathrm{ét}}^1(X_{\overline{K}}^\vee, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} C.
$$

The Weil pairing determines a perfect pairing

$$
H_{\mathrm{ét}}^1(X_{\overline{K}}, \mathbb{Z}_p) \times H_{\mathrm{ét}}^1(X_{\overline{K}}^\vee, \mathbb{Z}_p) \to \mathbb{Z}_p(-1)
$$

and there is also a perfect pairing

$$
H^1(X, \mathcal{O}_X) \times H^0(X^\vee, \Omega_{X^\vee/K}^1) \to K.
$$

So we get a map

$$
H^1(X, \mathcal{O}_X)^* \otimes_K C(-1) \hookrightarrow H_{\mathrm{ét}}^1(X_{\overline{K}}, \mathbb{Z}_p)^* \otimes_{\mathbb{Z}_p} C(-1).
$$

Taking the dual and twisting, we get a map

$$
H_{\mathrm{ét}}^1(X_{\overline{K}}, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} C \to H^1(X, \mathcal{O}_X) \otimes_K C.
\tag{19.4}
$$

The composite of (19.3) and (19.4) must be zero since $C(1)^{G_K} = 0$. Then, by dimension counting, the sequence

$$
0 \to H^0(X, \Omega_{X/K}^1) \otimes_K C(-1) \to H_{\mathrm{ét}}^1(X_{\overline{K}}, \mathbb{Z}_p) \otimes_{\mathbb{Z}_p} C \to H^1(X, \mathcal{O}_X) \otimes_K C \to 0
\tag{19.5}
$$

must be exact. Since $H^1(G_K, C(-1)) = 0$ (see **Remark** 13.2), this sequence has a $G_K$-equivariant splitting. Since $C(-1)^{G_K} = 0$, this splitting is unique.
