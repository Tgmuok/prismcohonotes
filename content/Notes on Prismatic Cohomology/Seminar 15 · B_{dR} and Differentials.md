It is not immediately obvious from the definition of $B_{\mathrm{dR}}$ that it should have anything to do with integrals of differential forms. We will now give an alternate characterization of $B_{\mathrm{dR}}^+$ that suggests a connection to differential forms.

Let $k$ be the residue field of $K$. Let
$$
A_{\mathrm{inf},K} := A_{\mathrm{inf}} \otimes_{W(k)} \mathcal{O}_K .
$$

There is a map $\Theta_K : A_{\mathrm{inf},K} \to \mathcal{O}_C$, and for each positive integer $n$, $B_{\mathrm{dR}}^+/ \mathrm{Fil}^n B_{\mathrm{dR}} \cong A_{\mathrm{inf},K}/(\ker \Theta_K)^n[1/p]$. So
$$
B_{\mathrm{dR}}^+ \cong \varprojlim_n \left( A_{\mathrm{inf},K}/(\ker \Theta_K)^n[1/p] \right) .
$$

Inductively define
$$
\mathcal{O}_{\overline{K}}^{(0)} := \mathcal{O}_{\overline{K}}
$$
$$
\Omega^{(n)} := \mathcal{O}_{\overline{K}} \otimes_{\mathcal{O}_{\overline{K}}^{(n-1)}} \Omega_{\mathcal{O}_{\overline{K}}^{(n-1)}/\mathcal{O}_K}
$$
$$
\mathcal{O}_{\overline{K}}^{(n)} := \ker \left( d^{(n)}: \mathcal{O}_{\overline{K}}^{(n-1)} \to \Omega^{(n)} \right)
$$

>[!danger]+ Them 15.1
>
> (1) For any nonnegative integer $n$, the preimage of $A_{\mathrm{inf},K}/(\ker \Theta_K)^{n+1}$ under the inclusion $\overline{K} \hookrightarrow B_{\mathrm{dR}}^+/ \mathrm{Fil}^{n+1} B_{\mathrm{dR}}$ is $\mathcal{O}_{\overline{K}}^{(n)}$.
>
> (2) For any nonnegative integers $m, n$, the map $\mathcal{O}_{\overline{K}}^{(n)}/p^m \to A_{\mathrm{inf},K}/\left( (\ker \Theta_K)^{n+1}, p^m \right)$ is an isomorphism.
>
> (3) $B_{\mathrm{dR}}^+$ is the completion of $\overline{K}$ for the topology defined by letting the sets $p^m \mathcal{O}_{\overline{K}}^{(n)}$ for nonnegative integers $m, n$ be a basis of open neighborhoods of the identity.
>
> (4) For any nonnegative integer $n$, $d^{(n)}$ is surjective.

>[!done]+ Coro 15.2
>
> The inclusion $\overline{K} \hookrightarrow B_{\mathrm{dR}}^+$ cannot be extended to a continuous map $C \to B_{\mathrm{dR}}^+$.
>
>>*Proof.* Any $x \in \mathrm{Fil}^1 B_{\mathrm{dR}}^+$ can be written as a limit of a sequence elements of $\overline{K}$. By continuity of the projection $B_{\mathrm{dR}}^+ \to C$, any such sequence converges to $0$ in $C$. So there cannot be any map $C \to B_{\mathrm{dR}}^+$ extending the inclusion $\overline{K} \hookrightarrow B_{\mathrm{dR}}^+$ that preserves sequential limits.

>[!tip]+ lemma 15.3
>
> The image of $\mathcal{O}_{\overline{K}}^{(n)}$ in $B_{\mathrm{dR}}^+$ is contained in $A_{\mathrm{inf},K} + \mathrm{Fil}^{n+1} B_{\mathrm{dR}}$.
>
>>*Proof.* We will use induction on $n$. The case $n = 0$ follows from the surjectivity of $\Theta$.
>>
>>Let $x \in \mathcal{O}_{\overline{K}}^{(n-1)}$. By the induction hypothesis, the image of $x$ in $B_{\mathrm{dR}}^+$ can be expressed as $x_0 + \epsilon$, with $x_0 \in A_{\mathrm{inf}}$ and $\epsilon \in \mathrm{Fil}^n B_{\mathrm{dR}}$. Recall that $A_{\mathrm{inf}} \cap \mathrm{Fil}^n B_{\mathrm{dR}} = (\ker \Theta_K)^n$. Consider the map
>>$$
>>\mathcal{O}_{\overline{K}}^{(n-1)} \to \mathrm{Fil}^n B_{\mathrm{dR}}/ \left( (\ker \Theta_K)^n + \mathrm{Fil}^{n+1} B_{\mathrm{dR}} \right)
>>$$
>>$$
>>x \mapsto \epsilon
>>$$
>>This map is an $\mathcal{O}_K$-linear derivation taking values in a $\mathcal{O}_{\overline{K}}$-module. By the universal property of $\Omega^{(n)}$, the map factors through $d^{(n)}$. In particular, its kernel contains $\ker d^{(n)} = \mathcal{O}_{\overline{K}}^{(n)}$.

>[!tip]+ lemma 15.4
>
> Let $x \in \mathcal{O}_{\overline{K}}$. Let $P \in \mathcal{O}_K[X]$ be a polynomial satisfying $P(x) = 0$, and let $r$ be a nonnegative integer such that $P'(x) \mid p^r$ in $\mathcal{O}_{\overline{K}}$. For each nonnegative integer $n$, let $a_n = (2^n - 1)r$, $b_n = (2^{n+1} - 2n - 1)r$. Then for any positive integer $m$, $p^{a_n}x^m \in \mathcal{O}_{\overline{K}}^{(n)}$, and $x^{p^{b_n}} \in \mathcal{O}_{\overline{K}}^{(n)}$.
>
>>*Proof.* Use induction on $n$. The base case $n = 0$ is trivial. Now assume that for some fixed $n$ and all $m$, $p^{a_n}x^m \in \mathcal{O}_{\overline{K}}^{(n)}$, and $x^{p^{b_n}} \in \mathcal{O}_{\overline{K}}^{(n)}$. By repeated use of the product rule, we see that
>>$$
>>d^{(n+1)}(p^{2a_n}x^m) = m p^{a_n} x^{m-1} d^{(n+1)}(p^{a_n}x)
>>$$
>>for each $m$. In particular, this implies
>>$$
>>0 = d^{(n+1)}(p^{2a_n}P(x)) = p^{a_n} P'(x) d^{(n+1)}(p^{a_n}x) .
>>$$
>>Hence
>>$$
>>0 = d^{(n+1)}(p^{2a_n + r}x) .
>>$$
>>Then multiplying (15.5) by $p^r$ and applying (15.6) yields
>>$$
>>0 = d^{(n+1)}(p^{2a_n + r}x^m) = d^{(n+1)}(p^{a_{n+1}}x^m) .
>>$$
>>In the case $m = p^{b_n}$, since $p^r \mid m$, we get the stronger result
>>$$
>>0 = d^{(n+1)} \left( p^{2a_n}x^{p^{b_n}} \right) = p^{2a_n} d^{(n+1)} \left( x^{p^{b_n}} \right) .
>>$$
>>Then
>>$$
>>d^{(n+1)} \left( x^{p^{b_{n+1}}} \right) = d^{(n+1)} \left( x^{p^{b_n + 2a_n}} \right) = p^{2a_n} (x^{p^{b_n}})^{p^{2a_n} - 1} d^{(n+1)} \left( x^{p^{b_n}} \right) = 0 .
>>$$
