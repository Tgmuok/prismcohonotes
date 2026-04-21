Now we define the ring $B_{\mathrm{dR}}$ mentioned in the first lecture.

Let $K$ be a $p$-adic field, and let $C$ be the completion of its algebraic closure with respect to the norm topology. We define the ring
$$
A_{\mathrm{inf}} := W(\mathcal{O}_{C^\flat}).
$$
By Proposition 10.10, there is a homomorphism
$$
\Theta: A_{\mathrm{inf}} \to \mathcal{O}_C.
$$
We will consider the localization
$$
\Theta_{\mathbb{Q}}: A_{\mathrm{inf}}[1/p] \to C.
$$

> [!tip]+ lemma 14.1
>
> For each positive integer $n$, $(\ker \Theta_{\mathbb{Q}})^n \cap A_{\mathrm{inf}} = (\ker \Theta)^n$, and $\bigcap_n (\ker \Theta_{\mathbb{Q}})^n = 0$.
>
>Let
>$$
>B_{\mathrm{dR}}^+ := \varprojlim_n A_{\mathrm{inf}}[1/p]/(\ker \Theta_{\mathbb{Q}})^n.
>$$
>Then $B_{\mathrm{dR}}^+$ is a complete discrete valuation ring with residue field $C$.
>
>>*Proof.* Left as an exercise to the reader.

Define
$$
B_{\mathrm{dR}} := \mathrm{Frac}\, B_{\mathrm{dR}}^+.
$$

Define a decreasing filtration on $B_{\mathrm{dR}}$ by letting $\mathrm{Fil}^i B_{\mathrm{dR}}$ be the fractional ideal $(\ker \Theta_{\mathbb{Q}})^i$. Now we will define an element $t \in B_{\mathrm{dR}}^+$ that is the $p$-adic analogue of $2\pi i$. Let $\epsilon \in \mathcal{O}_{C^\flat}$ be an element with $\epsilon_0 = 1$, $\epsilon_1 \neq 1$. Then $[\epsilon] - 1 \in \ker \Theta$, so it makes sense to define
$$
t := \log[\epsilon] = \sum_{n=1}^\infty (-1)^{n+1} \frac{([\epsilon] - 1)^n}{n}.
$$

> [!tip]+ lemma 14.2
>
> For any $a \in \mathbb{Q}_p$, $\log([\epsilon^a]) = a \log[\epsilon]$. Hence $G_K$ acts on $t \cdot \mathbb{Q}_p$ by the cyclotomic character.
>
>>*Proof.* It is formal that for $a \in \mathbb{Q}$, $\log([\epsilon^a]) = a \log[\epsilon]$.
>>
>>We would like to argue that the equality holds for $a \in \mathbb{Q}_p$ by continuity. But the $G_K$-action on $B_{\mathrm{dR}}^+$ is not jointly continuous for the $\ker \Theta$-adic topology, so we need to find a "better" topology.
>>
>>Let $\xi$ be a generator of $\ker \Theta$. Using Lemma 10.9 and the fact that the $G_K$-action on $\mathcal{O}_{C^\flat}$ is jointly continuous, we can verify that the $G_K$-action on $A_{\mathrm{inf}}$ is jointly continuous for the $(p,\xi)$-adic topology on $A_{\mathrm{inf}}$. Give $A_{\mathrm{inf}}/\xi^n$ the quotient topology. Extend this topology to $A_{\mathrm{inf}}[1/p]/\xi^n$ by letting $A_{\mathrm{inf}}/\xi^n$ be open. Finally, give $B_{\mathrm{dR}}^+ = \varprojlim_n A_{\mathrm{inf}}[1/p]/\xi^n$ the inverse limit topology. Then $G_K$ acts jointly continuously for this topology, and $\log$ is continuous on the open set $1 + \mathfrak{m}_{A_{\mathrm{inf}}} + \xi B_{\mathrm{dR}}^+ \subset B_{\mathrm{dR}}^+$, where $\mathfrak{m}_{A_{\mathrm{inf}}}$ is the maximal ideal of $A_{\mathrm{inf}}$.

> [!tip]+ lemma 14.3
>
> $t$ is a uniformizer of $B_{\mathrm{dR}}^+$.
>
>>*Proof.* It is clear that $t \in \mathrm{Fil}^1 B_{\mathrm{dR}}^+$, so we just need to check that $t \notin \mathrm{Fil}^2 B_{\mathrm{dR}}^+$. For this, it is enough to check that $[\epsilon] - 1 \notin \mathrm{Fil}^2 B_{\mathrm{dR}}^+$, or equivalently, $[\epsilon] - 1 \notin (\ker \Theta)^2$.
>>
>>For simplicity, we will assume $p \neq 2$. See [BC, Proposition 4.4.8] for the case $p = 2$.
>>
>>Recall from the proof of Proposition 10.12 that $\ker \Theta \subset (p, [\pi^\flat])$, where $\pi^\flat \in \mathcal{O}_{C^\flat}$ satisfies $|\pi^\flat| = |p|$. So it is enough to check that $[\epsilon] - 1 \notin (p, [\pi^\flat]^2)$, i.e. $|\epsilon - 1| > |p|^2$.
>>
>>Recall that if $\zeta_{p^n}$ is a primitive $n$th root of unity, then $|\zeta_{p^n} - 1| = |p|^{1/p^{n-1}(p-1)}$. Therefore,
>>$$
>>|\epsilon - 1| = \lim_{n \to \infty} |\zeta_{p^n} - 1|^{p^n} = |p|^{p/(p-1)} > |p|^2.
>>$$

> [!abstract]+ Prop 14.4
>
> There is a natural Galois-equivariant inclusion $\overline{K} \hookrightarrow B_{\mathrm{dR}}$.
>
>>*Proof.* Let $\overline{k}$ be the residue field of $\overline{K}$. There is a natural inclusion $\overline{k} \hookrightarrow \mathcal{O}_{C^\flat}$ sending $x \mapsto [x^{p^{-n}}]$, which induces inclusions $W(\overline{k}) \hookrightarrow A_{\mathrm{inf}}$, $W(\overline{k})[1/p] \hookrightarrow B_{\mathrm{dR}}^+$. Any $x \in \overline{K}$ satisfies an irreducible monic polynomial over $W(\overline{k})[1/p]$. This polynomial splits completely in $C$, the residue field of $B_{\mathrm{dR}}^+$, so it also splits in $B_{\mathrm{dR}}^+$ by Hensel's lemma. So there is a unique inclusion $\overline{K} \hookrightarrow B_{\mathrm{dR}}^+$ that makes the following diagram commute.
>>```tikz
>>\usepackage{tikz-cd}
>>
>>\begin{document}
>>\begin{tikzcd}
>>
>> {W(\overline{k})[1/p]} \arrow[rr, hook] \arrow[dd, hook] &  & B_{\mathrm{dR}}^+ \arrow[dd, two heads] \\
>>&  & \\
>>\overline{K} \arrow[rr, hook] \arrow[rruu, dashed, hook] &  & C  
>>
>>\end{tikzcd}
>>
>>\end{document}
>>```

> [!abstract]+ Prop 14.5
>
> The natural inclusions $K = \overline{K}^{G_K} \hookrightarrow (B_{\mathrm{dR}}^+)^{G_K} \hookrightarrow B_{\mathrm{dR}}^{G_K}$ are isomorphisms.
>
>>*Proof.* For any $n$, by Lemma 14.2, we have an exact sequence
>>$$
>>0 \to \mathrm{Fil}^{n+1} B_{\mathrm{dR}} \to \mathrm{Fil}^n B_{\mathrm{dR}} \to C(n) \to 0.
>>$$
>>(Here, $C(n) = C \otimes_{\mathbb{Z}_p} (\mathbb{Z}_p(1)^{\otimes n})$.) It induces an exact sequence
>>$$
>>0 \to (\mathrm{Fil}^{n+1} B_{\mathrm{dR}})^{G_K} \to (\mathrm{Fil}^n B_{\mathrm{dR}})^{G_K} \to C(n)^{G_K}.
>>$$
>>By Theorem 13.1, $C^{G_K} = K$ and $C(n)^{G_K} = 0$ if $n \neq 0$. We can then show that for all $n > 1$, the inclusion
>>$$
>>(\mathrm{Fil}^n B_{\mathrm{dR}}^+)^{G_K} \hookrightarrow (\mathrm{Fil}^1 B_{\mathrm{dR}}^+)^{G_K}
>>$$
>>is an isomorphism. Since $\bigcap_n \mathrm{Fil}^n B_{\mathrm{dR}}^+ = 0$,
>>$$
>>(\mathrm{Fil}^1 B_{\mathrm{dR}})^{G_K} = 0.
>>$$
>>Then the map $(B_{\mathrm{dR}}^+)^{G_K} \to C^{G_K} = K$ is injective. We already know that $(B_{\mathrm{dR}}^+)^{G_K}$ contains $\overline{K}^{G_K} = K$, so it must equal $K$. Finally, we can show that for all $n \leq 0$,
>>$$
>>(B_{\mathrm{dR}}^+)^{G_K} \hookrightarrow (\mathrm{Fil}^n B_{\mathrm{dR}})^{G_K}
>>$$
>>is an isomorphism, implying that
>>$$
>>(B_{\mathrm{dR}}^+)^{G_K} \hookrightarrow (B_{\mathrm{dR}})^{G_K}
>>$$
>>is an isomorphism.

> [!notes]+ Def 14.6
>
> Let $V$ be a finite-dimensional $\mathbb{Q}_p$-representation $V$ of $G_K$. Let $D_{\mathrm{dR}}(V)$ be the filtered $K$-vector space $(V \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}})^{G_K}$.

> [!abstract]+ Prop 14.7
>
> Let $V$ be a finite-dimensional $\mathbb{Q}_p$-representation $V$ of $G_K$. Let
> $$
> \alpha_V: D_{\mathrm{dR}}(V) \otimes_K B_{\mathrm{dR}} \to V \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}
> $$
> be the restriction of the map
> $$
> V \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}} \otimes_K B_{\mathrm{dR}} \to V \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}
> $$
> induced by multiplication on $B_{\mathrm{dR}}$. Then $\alpha_V$ is an injection. In particular,
> $$
> \dim_K D_{\mathrm{dR}}(V) \leq \dim_{\mathbb{Q}_p} V
> $$
> with equality iff $\alpha_V$ is an isomorphism.
>
>>*Proof.* See [BC, Theorem 5.2.1(1)].

> [!notes]+ Def 14.8
>
> We say that $V$ is de Rham if $\dim_K D_{\mathrm{dR}}(V) = \dim_{\mathbb{Q}_p} V$.
>
> If $V$ is de Rham, then the Hodge–Tate weights of $V$ are the integers $i$ such that $\mathrm{gr}^i D_{\mathrm{dR}}(V) \neq 0$.

> [!example]+ ex 14.9
>
> The Hodge–Tate weight of $\mathbb{Q}_p(n)$ is $-n$.

> [!danger]+ Them 14.10
>
> If $X$ is a proper smooth variety over $K$, then $H^i_{\text{ét}}(X_{\overline{K}}, \mathbb{Q}_p)$ is de Rham, with Hodge–Tate weights between $0$ and $i$, inclusive.

This is proved as part of the de Rham comparison theorem.

> [!tip]+ lemma 14.11
>
> Let $L$ be a finite extension of $K$. Then a representation of $G_K$ is de Rham if and only if its restriction to $G_L$ is de Rham.
>
>>*Proof.* This follows from Galois descent.

> [!tip]+ lemma 14.12
>
> A tensor product of two de Rham representations is de Rham. Subrepresentations and quotients of a de Rham representation are de Rham.
>
>>*Proof.* Suppose $V_1$ and $V_2$ are de Rham representations. Multiplication on $B_{\mathrm{dR}}$ induces a map
>>$$
>>D_{\mathrm{dR}}(V_1) \otimes_K D_{\mathrm{dR}}(V_2) \to D_{\mathrm{dR}}(V_1 \otimes_{\mathbb{Q}_p} V_2).
>>$$
>>To show that $V_1 \otimes V_2$ is de Rham, it suffices to show that the above map is injective. Then it also suffices to check injectivity of the map
>>$$
>>D_{\mathrm{dR}}(V_1) \otimes_K D_{\mathrm{dR}}(V_2) \to (V_1 \otimes_{\mathbb{Q}_p} V_2) \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}
>>$$
>>and likewise of the map
>>$$
>>D_{\mathrm{dR}}(V_1) \otimes_K D_{\mathrm{dR}}(V_2) \otimes_K B_{\mathrm{dR}} \to (V_1 \otimes_{\mathbb{Q}_p} V_2) \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}, \tag{14.13}
>>$$
>>After rewriting the LHS as
>>$$
>>(D_{\mathrm{dR}}(V_1) \otimes_K B_{\mathrm{dR}}) \otimes_{B_{\mathrm{dR}}} (D_{\mathrm{dR}}(V_2) \otimes_K B_{\mathrm{dR}})
>>$$
>>and the RHS as
>>$$
>>(V_1 \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}) \otimes_{B_{\mathrm{dR}}} (V_2 \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}),
>>$$
>>we see that Proposition 14.7 implies that (14.13) is an isomorphism.
>>
>>We can check injectivity after tensoring with $B_{\mathrm{dR}}$. Since $V_1$ and $V_2$ are de Rham, we can identify
>>$$
>>\begin{aligned}
>>D_{\mathrm{dR}}(V_1) \otimes_K D_{\mathrm{dR}}(V_2) \otimes_K B_{\mathrm{dR}} &\cong (D_{\mathrm{dR}}(V_1) \otimes_K B_{\mathrm{dR}}) \otimes_{B_{\mathrm{dR}}} (D_{\mathrm{dR}}(V_2) \otimes_K B_{\mathrm{dR}}) \\
>>&\cong (V_1 \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}) \otimes_{B_{\mathrm{dR}}} (V_2 \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}) \cong (V_1 \otimes V_2) \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}
>>\end{aligned}
>>$$
>>Therefore, we are reduced to showing that the induced map
>>$$
>>(V_1 \otimes_{\mathbb{Q}_p} V_2) \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}} \to D_{\mathrm{dR}}(V_1 \otimes_{\mathbb{Q}_p} V_2) \otimes_{\mathbb{Q}_p} B_{\mathrm{dR}}
>>$$
>>is injective.
>>
>>Suppose we have an exact sequence of representations
>>$$
>>0 \to V' \to V \to V'' \to 0
>>$$
>>with $V$ de Rham. Then we have a left exact sequence
>>$$
>>0 \to D_{\mathrm{dR}}(V') \to D_{\mathrm{dR}}(V) \to D_{\mathrm{dR}}(V''),
>>$$
>>so
>>$$
>>\dim_K D_{\mathrm{dR}}(V') + \dim_K D_{\mathrm{dR}}(V'') \geq \dim_K D_{\mathrm{dR}} V.
>>$$
>>On the other hand,
>>$$
>>\dim_K D_{\mathrm{dR}}(V') \leq \dim_{\mathbb{Q}_p} V'
>>$$
>>$$
>>\dim_K D_{\mathrm{dR}}(V'') \leq \dim_{\mathbb{Q}_p} V''
>>$$
>>$$
>>\dim_K D_{\mathrm{dR}}(V) = \dim_{\mathbb{Q}_p} V.
>>$$
>>So all inequalities must actually be equalities.

> [!example]+ ex 14.14
>
> Let $\psi: \mathbb{Z}_p^\times \to \mathbb{Z}_p^\times$ be a character, and let $\chi: G_K \to \mathbb{Z}_p^\times$ be the cyclotomic character. The character $\psi \circ \chi: G_K \to \mathbb{Z}_p^\times$ is de Rham if and only if $\psi$ is a product of a finite order character and a character of the form $z \mapsto z^n$ for some $n \in \mathbb{Z}$. In particular, there exist characters that are not de Rham. The "only if" direction follows from Theorem 13.1 by the same argument as in Proposition 14.5. For the "if" direction, we can use Lemma 14.11 to reduce to the case where the finite order character is trivial, and then apply Lemma 14.2.


