Let $\pi$ be a uniformizer of $K$.

> [!tip]+ Lemma 16.1
> 
> For any $n$, the map $\mathcal{O}_{\overline{K}}^{(n)} \to \mathcal{O}_C/\pi = \mathcal{O}_{\overline{K}}/\pi$ is surjective.
> 
>> *Proof.* Let $x \in \mathcal{O}_{\overline{K}}$, and let $P$ be the minimal polynomial for $x$ over $k$. Let $x_m$ satisfy $x_m^{p^m} + \pi x_m = x$. Then $x_m^{p^m} \equiv x \pmod{\pi}$. We claim that for sufficiently large $m$, $x_m^{p^m} \in \mathcal{O}_{\overline{K}}^{(n)}$. Indeed, let $P_m(X) = P(X^{p^m} + \pi X)$; then $P_m(x_m) = 0$ and $P_m'(x_m) = (p^m x_m^{p^m - 1} + \pi)P'(x)$, so $|P_m'(x_m)| = |\pi||P'(x)|$. Then the claim follows from Lemma 15.4.

By Lemma 15.3, the map $\mathcal{O}_{\overline{K}}^{(n)} \hookrightarrow B_{\text{dR}}^+/\text{Fil}^{n+1} B_{\text{dR}}^+$ factors through $A_{\text{inf},K}/(\ker \Theta_K)^{n+1}$.

> [!tip]+ Lemma 16.2
> 
> For any $n,m$,
> 
> $$
> \mathcal{O}_{\overline{K}}^{(n)} \to A_{\text{inf},K}/(\pi^m, (\ker \Theta_K)^{n+1})
> $$
> 
> is surjective.
> 
>> *Proof.* Observe that $A_{\text{inf}}/(\pi^m, (\ker \Theta_K)^{n+1})$ is generated as an $\mathcal{O}_K$-module by the elements $[x]$ for $x \in \mathcal{O}_{K^\flat}$. By Lemma 16.1, for any $r$, we can find $\tilde{x}_r \in \mathcal{O}_{\overline{K}}^{(n)}$ such that $\tilde{x}_r$ and $x^{(r)}$ have the same image in $\mathcal{O}_C/p$. So the image of $\tilde{x}_r$ in $A_{\text{inf},K}/(\ker \Theta_K)^{n+1}$ will be congruent to $[x^{p^{-r}}]$ modulo $(\pi, (\ker \Theta_K))$. If $r$ is sufficiently large, then the image of $\tilde{x}_r^{p^r}$ will be congruent to $[x]$ modulo $(\pi^m, (\ker \Theta_K)^n)$. (Note that the bound on $r$ does not depend on $x$, only on $m$ and $n$.)

> [!tip]+ Lemma 16.3
> 
> Let $m,n$ be nonnegative integers. Consider the map
> 
> $$
> \theta_{m,n}: \mathcal{O}_{\overline{K}}^{(n)}/p^m \to \mathcal{O}_C/p^m.
> $$
> 
> We have
> 
> $$
> (\ker \theta_{m,n})^{n+1} = 0.
> $$
> 
>> *Proof.* We will use induction on $n$. The base case $n = 0$ is trivial. Assume $(\ker \theta_{m,n-1})^n = 0$. It suffices to show that for $x \in \ker \theta_{m,n}$, $y \in (\ker \theta_{m,n})^n$, $xy = 0$. Choose lifts $\tilde{x}, \tilde{y} \in \mathcal{O}_{\overline{K}}^{(n)}$. By the induction hypothesis, $\tilde{y} \in p^m \mathcal{O}_{\overline{K}}^{(n-1)}$. Then $\tilde{x} \cdot p^{-m}\tilde{y} \in \mathcal{O}_{\overline{K}}^{(n-1)}$ and
>> 
>> $$
>> d^{(n)}(\tilde{x} \cdot p^{-m}\tilde{y}) = p^{-m}\tilde{y} \cdot d^{(n)}\tilde{x} + p^{-m}\tilde{x} \cdot d^{(n)}\tilde{y} = 0.
>> $$
>> 
>> So $\tilde{x}\tilde{y}$ is a multiple of $p^m$ in $\mathcal{O}_{\overline{K}}^{(n)}$, implying $xy = 0$.

> [!danger]+ Them 15.1
> 
> (1) The preimage of $A_{\text{inf},K}/(\ker \Theta_K)^{n+1}$ under the inclusion $\overline{K} \hookrightarrow B_{\text{dR}}^+/\text{Fil}^{n+1} B_{\text{dR}}$ is $\mathcal{O}_{\overline{K}}^{(n)}$.
> 
> (2) The map
> 
> $$
> \mathcal{O}_{\overline{K}}^{(n)}/p^m \to A_{\text{inf},K}/(p^m, (\ker \Theta_K)^{n+1})
> $$
> 
> is an isomorphism.
> 
> (3) [Follows immediately from items (1) and (2).]
> 
> (4) Each element of $\Omega^{(n)}$ is of the form $\sum_i x_i d^{(n)} y_i$ for $x_i \in \mathcal{O}_{\overline{K}}$ and $y_i \in \mathcal{O}_{\overline{K}}^{(n-1)}$.
> 
>> *Proof of (2).* First, we prove item (2), that the map
>> 
>> $$
>> \mathcal{O}_{\overline{K}}^{(n)}/p^m \to A_{\text{inf},K}/(p^m, (\ker \Theta_K)^{n+1})
>> $$
>> 
>> is an isomorphism. Denote this map by $f_{m,n}$. We will construct an inverse map
>> 
>> $$
>> g_{m,n}: A_{\text{inf}}/(p^m, (\ker \Theta_K)^{n+1}) \to \mathcal{O}_{\overline{K}}^{(n)}/p^m.
>> $$
>> 
>> By a generalization of Proposition 10.10, to construct a ring homomorphism
>> 
>> $$
>> A_{\text{inf},K}/p^m \to \mathcal{O}_{\overline{K}}^{(n)}/p^m,
>> $$
>> 
>> it suffices to construct a multiplicative map
>> 
>> $$
>> \mathcal{O}_{C^\flat} \to \mathcal{O}_{\overline{K}}^{(n)}/p^m
>> $$
>> 
>> such that the induced map
>> 
>> $$
>> \mathcal{O}_{C^\flat} \to \mathcal{O}_{\overline{K}}^{(n)}/\pi
>> $$
>> 
>> is a ring homomorphism. For $x \in \mathcal{O}_{C^\flat}$ and $r$ a nonnegative integer, let $\tilde{x}_r \in \mathcal{O}_{\overline{K}}^{(n)}/\pi^m$ such that $\tilde{x}_r$ and $x^{(r)}$ have the same image on $\mathcal{O}_C/\pi^m$. It follows from 16.3 that for sufficiently large $r$, $\tilde{x}_r^{p^r}$ will not depend on the choice of $\tilde{x}_r$. Then we choose the map $x \mapsto \tilde{x}_r^{p^r}$. The associated map $A_{\text{inf},K}/\pi^m \to \mathcal{O}_{\overline{K}}^{(n)}$ is given by (16.4)
>> 
>> $$
>> \sum_i [x_i]\pi^i \mapsto \sum_i \tilde{x}_{i,r}^{p^r} \pi^i.
>> $$
>> 
>> By Lemma 16.3, this map actually factors through $A_{\text{inf},K}/(p^m, (\ker \Theta_K)^{n+1})$. So we have constructed $g_{m,n}$. It is clear that $f_{m,n} \circ g_{m,n} = 1$.
>> 
>> Now we prove that $g_{m,n} \circ f_{m,n} = 1$. Since $\mathcal{O}_{\overline{K}}^{(n)}$ has no $p$-torsion, $\widehat{\mathcal{O}_{\overline{K}}^{(n)}}$ also has no $p$-torsion. So it suffices to show that the induced maps
>> 
>> $$
>> f_n: \widehat{\mathcal{O}_{\overline{K}}^{(n)}}[1/p] \to B_{\text{dR}}^+/\text{Fil}^{n+1} B_{\text{dR}}^+
>> $$
>> 
>> $$
>> g_n: B_{\text{dR}}^+/\text{Fil}^{n+1} B_{\text{dR}}^+ \to \widehat{\mathcal{O}_{\overline{K}}^{(n)}}[1/p]
>> $$
>> 
>> satisfy $g_n \circ f_n = 1$. We can construct a map $\overline{K} \hookrightarrow \widehat{\mathcal{O}_{\overline{K}}^{(n)}}[1/p]$ by the same method as for $\overline{K} \to B_{\text{dR}}$. It is not hard to see that $g_n \circ f_n$ fixes $K$, so $g_n \circ f_n$ must send $\overline{K}$ to itself. Since $g_n \circ f_n$ induces the identity on the residue field $C$, it must fix $\overline{K}$. But $\overline{K}$ is dense in $\widehat{\mathcal{O}_{\overline{K}}^{(n)}}[1/p]$, so $g_n \circ f_n = 1$. This concludes the proof of item (2).
> 
>> *Proof of (1,3,4).* Next, we prove item (1), that the preimage of $A_{\text{inf},K}/(\ker \Theta_K)^{n+1}$ under the inclusion $\overline{K} \hookrightarrow B_{\text{dR}}^+/\text{Fil}^{n+1} B_{\text{dR}}$ is $\mathcal{O}_{\overline{K}}^{(n)}$. Denote the preimage by $\mathcal{O}'$.
>> 
>> Let $x \in \mathcal{O}'$. Then by Lemma 15.4, there exists $m$ so that $p^m x \in \mathcal{O}_{\overline{K}}^{(n)}$. By item (2), $\mathcal{O}_{\overline{K}}^{(n)}/p^m \to A_{\text{inf}}/(p^m, (\ker \Theta_K)^{(n+1)})$ is injective, so $p^m x$ must be a multiple of $p^m$ in $\mathcal{O}_{\overline{K}}^{(n)}$ as well. Hence $x \in \mathcal{O}_{\overline{K}}^{(n)}$.
>> 
>> Item (3) follows immediately from items (1) and (2).
>> 
>> Finally, we prove item (4). Each element of $\Omega^{(n)}$ is of the form $\sum_i x_i d^{(n)} y_i$ for $x_i \in \mathcal{O}_{\overline{K}}$ and $y_i \in \mathcal{O}_{\overline{K}}^{(n-1)}$. By Lemma 15.4, we can find $m_i$ so that $p^{m_i} d^{(n)} y_i = 0$, and by Lemma 16.2, we can find $z_i \in \mathcal{O}_{\overline{K}}^{(n)}$ so that $x_i - z_i \in p^{m_i} \mathcal{O}_{\overline{K}}$. Then $\sum_i x_i d^{(n)} y_i = \sum_i z_i d^{(n)} y_i = \sum_i d^{(n)} (y_i z_i)$.

> [!tip]+ Lemma 16.5
> 
> For any abelian group $A$, we have an isomorphism
> 
> $$
> \text{Ext}^1_{\mathbb{Z}}(\mathbb{Q}_p/\mathbb{Z}_p, A) \cong \varprojlim_n A/p^n A.
> $$
> 
> The right-hand side is the $p$-adic completion of $A$.
> 
>> *Proof.* There is a projective resolution
>> 
>> $$
>> 0 \to \bigoplus_{i=1}^\infty \mathbb{Z} \to \bigoplus_{i=1}^\infty \mathbb{Z} \to \mathbb{Q}_p/\mathbb{Z}_p \to 0.
>> $$
>> 
>> If we denote the basis elements of $\mathbb{Z}^{\oplus \mathbb{N}}$ by $e_i$, then the first map is given by
>> 
>> $$
>> e_i \mapsto
>> \begin{cases}
>> p e_1, & i = 1 \\
>> p e_i - e_{i-1}, & i > 1
>> \end{cases}
>> $$
>> 
>> and the second map is given by
>> 
>> $$
>> e_i \mapsto p^{-i}.
>> $$
>> 
>> So $\text{Ext}^1_{\mathbb{Z}}(\mathbb{Q}_p/\mathbb{Z}_p, A)$ is the space of sequences $a_0, a_1, a_2, \dots \in A$ modulo sequences of the form $(p b_0, p b_1 - b_0, p b_2 - b_1, \dots)$. For each $n$, $\sum_{i=1}^n p^{i-1} a_i$ is determined modulo $p^n$. Together, these sums determine an element of $\varprojlim_n A/p^n A$.

> [!tip]+ Lemma 16.6
> 
> For each positive integer $n$, there is a natural isomorphism
> 
> $$
> \text{Hom}_{\mathbb{Z}_p}(\mathbb{Q}_p, \Omega^{(n)}) \cong \text{Fil}^n B_{\text{dR}}/\text{Fil}^{n+1} B_{\text{dR}}.
> $$
> 
>> *Proof.* By Theorem 15.1(4), there is an exact sequence
>> 
>> $$
>> 0 \to \mathcal{O}_{\overline{K}}^{(n)} \to \mathcal{O}_{\overline{K}}^{(n-1)} \to \Omega^{(n)} \to 0.
>> $$
>> 
>> So we get an exact sequence
>> 
>> $$
>> 0 \to \text{Hom}_{\mathbb{Z}}(\mathbb{Q}_p/\mathbb{Z}_p, \Omega^{(n)}) \to A_{\text{inf},K}/(\ker \Theta_K)^{n+1} \to A_{\text{inf},K}/(\ker \Theta_K)^n \to 0,
>> $$
>> 
>> where we used Lemma 16.5 and Theorem 15.1(2) to compute the $\text{Ext}^1$ groups. Observe that $\text{Hom}_{\mathbb{Z}}(\mathbb{Q}_p/\mathbb{Z}_p, \Omega^{(n)}) \cong \text{Hom}_{\mathbb{Z}_p}(\mathbb{Q}_p/\mathbb{Z}_p, \Omega^{(n)})$, and since $\Omega^{(n)}$ is $p$-power torsion, $\text{Hom}_{\mathbb{Z}_p}(\mathbb{Q}_p/\mathbb{Z}_p, \Omega^{(n)}) \otimes_{\mathbb{Z}_p} \mathbb{Q}_p \cong \text{Hom}_{\mathbb{Z}_p}(\mathbb{Q}_p, \Omega^{(n)})$. Then inverting $p$ gives an exact sequence
>> 
>> $$
>> 0 \to \text{Hom}_{\mathbb{Z}_p}(\mathbb{Q}_p, \Omega^{(n)}) \to B_{\text{dR}}^+/\text{Fil}^{n+1} B_{\text{dR}}^+ \to B_{\text{dR}}^+/\text{Fil}^n B_{\text{dR}}^+ \to 0.
>> $$
