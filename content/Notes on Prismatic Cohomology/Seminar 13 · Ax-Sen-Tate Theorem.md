Let $K$ be a $p$-adic field, and let $C := \widehat{\overline{K}}$ be the completion of its algebraic closure with respect to the norm topology. In a previous lecture, I claimed that there is no element ' $2\pi i$ ' in $C$ so that $G_K$ acts on ' $2\pi i$ ' $\cdot \mathbb{Q}_p$ by the cyclotomic character $\chi$.

> [!danger]+ Them 13.1
> 
> $C^{G_K} = K$.
> 
> Let $K_\infty := K(\mu_{p^\infty})$, $K^{\mathrm{cyc}} := \widehat{K_\infty}$, $\Gamma := \mathrm{Gal}(K_\infty/K)$. If $\chi: \Gamma \to K^\times$ has infinite order, then $C(\chi)^{G_K} = 0$.

**Remark 13.2.** One can also show that $H^1(G_K,C)$ is a one-dimensional $K$-vector space and that $H^1(G_K,C(\chi)) = 0$. In the interest of space, we omit the proof. See [Tat67, §3].

For an elementary (but calculation-heavy) proof that $C^{G_K} = K$, see [Ax70] or [FO, Proposition 3.8].

The proof breaks down into the following steps.

> [!tip]+ lemma 13.3
> 
> Let $k$ be the residue field of $K$, and let $K_0 = W(k)[1/p]$. Let $\pi$ be a uniformizer of $K$, and let $e = \frac{\log |p|}{\log |\pi|}$. Then $[K : K_0] = e$.
>
>>*Proof.* Every element of $\mathcal{O}_K$ can be written as $\sum_{i=0}^\infty [a_i]\pi^i$ with $a_i \in k$. We can write $\pi^e = [u]p + \sum_{i=e+1}^\infty [b_i]\pi^i$ with $u \in k^\times$, $b_i \in K$. Then by repeated substitution, every element of $\mathcal{O}_K$ can be written in the form $\sum_{i=0}^\infty \sum_{j=0}^{e-1} [c_i] p^i \pi^j$. Hence $1, \pi, \dots, \pi^{e-1}$ form a basis for $\mathcal{O}_K$ as a $W(k)$-module.

> [!tip]+ lemma 13.4
> 
> The field $K^{\mathrm{cyc}}$ is perfectoid.
>
>>*Proof.* Let $k$ be the residue field of $K$. Then $W(k)[1/p]^{\mathrm{cyc}}$ is perfectoid by the same argument as in Lemma 9.16. Since $K$ is finite extension of $W(k)[1/p]$, the result follows from Lemma 11.4.

> [!abstract]+ Prop 13.5
> 
> If $L$ is a perfectoid field, then $(\widehat{\overline{L}})^{G_L} = L$. In particular, $C^{\mathrm{Gal}(\overline{K}/K_\infty)} = K^{\mathrm{cyc}}$.

> [!abstract]+ Prop 13.6
> 
> $(K^{\mathrm{cyc}})^\Gamma = K$.
> 
> If $\chi: \Gamma \to K^\times$ has infinite order, then $K^{\mathrm{cyc}}(\chi)^\Gamma = 0$.

To prove Proposition 13.5, we will need a few lemmas.

> [!tip]+ lemma 13.7
> 
> Let $M/L$ be a finite extension of perfectoid fields. Then $\mathrm{tr}_{M/L}(\mathfrak{m}_M) = \mathfrak{m}_L$.
>
>>*Proof.* Since $M^\flat/L^\flat$ is separable, $\mathrm{tr}_{M^\flat/L^\flat}(\mathfrak{m}_{M^\flat})$ is a nonzero ideal of $\mathcal{O}_{L^\flat}$. By applying the inverse of Frobenius, we see that it must be all of $\mathfrak{m}_{L^\flat}$. Since there are compatible surjective ring homomorphisms $\mathcal{O}_{M^\flat} \to \mathcal{O}_M/p\mathcal{O}_M$, $\mathcal{O}_{L^\flat} \to \mathcal{O}_L/p\mathcal{O}_L$, this implies that $\mathrm{tr}_{M/L}(\mathfrak{m}_M) = \mathfrak{m}_L$.

> [!tip]+ lemma 13.8
> 
> Let $L$ be a perfectoid field, and let $y \in \overline{L}$. Let $c > 1$ be a real number. Then there exists $z \in L$ so that
> 
> $$
> |y - z| \leq c \max_{\sigma \in G_L} |\sigma y - y|.
> $$
>
>>*Proof.* Choose a finite extension $M$ of $L$ containing $y$. We will write $\mathrm{tr}$ for the trace from $M$ to $L$. By Lemma 13.7, we can find $x \in M$ with $|x| < 1$, $|\mathrm{tr}\, x| \geq c^{-1}$. Let $z = \frac{\mathrm{tr}(xy)}{\mathrm{tr}\, x}$. Then
>>
>>$$
>>y - z = \frac{\sum_{\sigma \in \mathrm{Gal}(M/L)} (\sigma x)(y - \sigma y)}{\mathrm{tr}\, x}.
>>$$
>>
>>Hence $|y - z| \leq c \max_{\sigma \in H_K} |\sigma y - y|$, as desired.

>*Proof of Proposition 13.5.* Let $x \in (\widehat{\overline{L}})^{G_L}$. Then for any real $\epsilon > 0$, we can find $y \in \overline{L}$ so that $|x - y| < \epsilon$. By the strong triangle inequality, for all $\sigma \in G_L$,
>
>$$
>|\sigma y - y| \leq \max(|\sigma y - z|, |y - z|) = |y - z| < \epsilon.
>$$
>
>By Lemma 13.8, for any $c > 1$, we can find $z \in L$ so that $|y - z| \leq c\epsilon$. Hence $|x - z| < c\epsilon$. Since this is true for any $\epsilon$, and $L$ is complete, $x \in L$.

In order to prove Proposition 13.6, there is no harm in replacing $K$ with a finite Galois extension. So we may assume $K$ contains a $p$th root of unity. This implies that $\Gamma \cong \mathbb{Z}_p$. Let $\gamma$ be a topological generator of $\Gamma$.

Let $t: K_\infty \to K$ be the "normalized trace map" satisfying $t|_L = \frac{1}{[L:K]} \mathrm{tr}_{L/K}$ for every finite extension $L/K$ inside $K_\infty$.

> [!tip]+ lemma 13.9
> 
> For any $x \in K_\infty$,
> 
> $$
> |x - t(x)| \leq |p|^{-1}|x - \gamma x|.
> $$
>
>>*Proof.* For each $n$, let $K_n$ be the fixed field of $p^n\Gamma$. We will prove the inequality on each $K_n$ by induction. The base case $n = 0$ is trivial. Since $1 - \gamma$ divides $p - \left(1 + \gamma^{p^{n-1}} + \dots + \gamma^{p^{n-1}(p-1)}\right)$, we have
>>
>>$$
>>|px - \mathrm{tr}_{K_n/K_{n-1}} x| \leq |((1 - \gamma)x)|.
>>$$
>>
>>or equivalently,
>>
>>$$
>>|x - p^{-1} \mathrm{tr}_{K_n/K_{n-1}} x| \leq |p|^{-1}|((1 - \gamma)x)|.
>>$$
>>
>>By the induction hypothesis,
>>
>>$$
>>|p^{-1} \mathrm{tr}_{K_n/K_{n-1}} - t(x)| \leq |p|^{-1}|(1 - \gamma)(p^{-1} \mathrm{tr}_{K_n/K_{n-1}} x)| \leq |p|^{-1}|((1 - \gamma)x)|,
>>$$
>>
>>where we used the fact that $1 - \gamma$ commutes with the normalized trace in the last inequality. Then the claim follows from the triangle inequality.

> [!done]+ Coro 13.10
> 
> For any $x \in K_\infty$,
> 
> $$
> |t(x)| \leq |p|^{-1}|x|.
> $$

So the function $t$ is continuous. Moreover, $1 - \gamma$ is invertible on $\ker t$, and its inverse is continuous.

Hence $t$ can be extended to a continuous function $\hat{t}: K^{\mathrm{cyc}} \to K$, and the restriction of $1 - \gamma$ to $\ker \hat{t}$ has a continuous inverse.

>*Proof of Proposition 13.6.* We have
>
>$$
>K^{\mathrm{cyc}} = K \oplus \ker \hat{t}
>$$
>
>$$
>(K^{\mathrm{cyc}})^\Gamma = K^\Gamma \oplus (\ker \hat{t})^\Gamma = K \oplus 0 = K.
>$$
>
>Finally, suppose that $\chi: \Gamma \to K^\times$ is a character of infinite order. We will show that $K^{\mathrm{cyc}}(\chi^{-1})^\Gamma = 0$. For sufficiently large $n$, we must have $|\chi(\gamma^{p^n}) - 1| < |p|$. Since there is no harm with replacing $K$ by a finite Galois extension, we may assume $|\chi(\gamma) - 1| < |p|$. On $\ker \hat{t}$,
>
>$$
>\gamma - \chi(\gamma) = (\gamma - 1)(1 - (\chi(\gamma) - 1)(\gamma - 1)^{-1})
>$$
>
>and $(1 - (\chi(\gamma) - 1)(\gamma - 1)^{-1})^{-1}$ has a convergent power series, so $\gamma - \chi(\gamma)$ is invertible. On $K$, $\gamma - \chi(\gamma) = 1 - \chi(\gamma)$ is invertible since $\chi$ has infinite order.
