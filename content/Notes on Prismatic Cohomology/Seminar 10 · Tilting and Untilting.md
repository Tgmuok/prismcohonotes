>[!example]+ ex 10.1
>
> We claim that $(\mathbb{Q}_p^{\mathrm{cyc}})^\flat$ is isomorphic to the completion of the perfection of $\mathbb{F}_p((t))$. We have
>
> $$
> \mathcal{O}_{\mathbb{Q}_p^{\mathrm{cyc}}}/p \cong \varprojlim_n \mathbb{Z}_p[\zeta_{p^n}]/p \cong \varprojlim_n \mathbb{Z}_p[\zeta_{p^n} - 1]/p^n.
> $$
>
> The minimal polynomial of $\zeta_{p^n} - 1$ is
>
> $$
> \frac{(1 + T)^{p^n} - 1}{(1 + T)^{p^{n-1}} - 1} \cong T^{p^n - p^{n-1}} \pmod{p}.
> $$
>
> Since $\zeta_{p^n} - 1 \cong (\zeta_{p^{n+1}} - 1)^p \pmod{p}$ for each $n$, we can write
>
> $$
> \mathcal{O}_{\mathbb{Q}_p^{\mathrm{cyc}}}/p \cong \varprojlim_n \mathbb{F}_p[t^{p^{-n}}]/(t^{1-1/p}).
> $$
>
> Then
>
> $$
> (\mathcal{O}_{\mathbb{Q}_p^{\mathrm{cyc}}})^\flat = \varprojlim_\Phi \varprojlim_n \mathbb{F}_p[t^{p^{-n}}]/(t^{1-1/p}) = \varprojlim_m \varprojlim_n \mathbb{F}_p[t^{p^{-n}}]/(t^{p^m - p^{m-1}})
> $$
>
> $$
> (\mathbb{Q}_p^{\mathrm{cyc}})^\flat = (\mathcal{O}_{\mathbb{Q}_p^{\mathrm{cyc}}})^\flat[1/t]
> $$

>[!notes]+ Def 10.2
>
> Let $K$ be a perfectoid field of characteristic $p$. An untilt of $K$ is a perfectoid field $K^\sharp$, along with an isomorphism $(K^\sharp)^\flat \xrightarrow{\sim} K$.

We would like to classify the untilts of a given characteristic $p$ perfectoid field $K$. In order to do that, we will need to introduce the ring $W(\mathcal{O}_K)$.

>[!notes]+ Def 10.3
>
> An $\mathbb{F}_p$-algebra $R$ is perfect if the Frobenius endomorphism of $R$ is an isomorphism.

>[!notes]+ Def 10.4
>
> An abelian group $A$ is $p$-adically complete and separated if $A \to \varprojlim_n A/p^n A$ is an isomorphism.

>[!notes]+ Def 10.5
>
> A strict $p$-ring is a ring $A$ that is $p$-adically complete and separated, such that $A/pA$ is a perfect $\mathbb{F}_p$-algebra, and $p$ is not a zero divisor in $A$.

>[!example]+ ex 10.6
>
> If $K$ is the completion of an unramified extension of $\mathbb{Q}_p$, then $\mathcal{O}_K$ is a strict $p$-ring. The $p$-adic completion of $\mathbb{Z}[x^{p^{-\infty}}]$ is also a strict $p$-ring.

The main goal of this section is to prove the following theorem.

>[!danger]+ Them 10.7
>
> The functor $A \mapsto A/pA$ from strict $p$-rings to perfect $\mathbb{F}_p$-algebras is an equivalence of categories.

We will write $W$ for the functor from perfect $\mathbb{F}_p$-algebras to strict $p$-rings determined by the above equivalence. For $R$ a perfect $\mathbb{F}_p$-algebra, the ring $W(R)$ is called the ring of $p$-typical Witt vectors of $R$.

>[!tip]+ lemma 10.8
>
> Let $A$ be a strict $p$-ring.
>
> (1) There is a unique section $[\cdot]$ of the reduction map $A \to A/pA$ that is a homomorphism of multiplicative monoids.
>
> (2) Every element of $A$ can be written uniquely in the form
>
> $$
> \sum_{n=0}^\infty p^n [a_n], \quad a_n \in A/pA.
> $$
>
>>Proof. For the first part, observe that for any $x \in R/pR$, we must have
>>
>>$$
>>[x] = \lim_{n \to \infty} (x_n)^{p^n}
>>$$
>>
>>where $x_n$ is a lift of $x^{p^{-n}}$. The argument that the limit exists and is independent of the choice of lifts follows from Lemma 9.19.
>>
>>Since $A$ is $p$-adically complete and separated, the second part follows immediately from the first.

>[!tip]+ lemma 10.9
>
> Let $A$ be a strict $p$-ring, and let $a,b \in A$. Suppose that $a = \sum_{n=0}^\infty [a_n]p^n$, $b = \sum_{n=0}^\infty [b_n]p^n$, $a + b = \sum_{n=0}^\infty [s_n]p^n$, $ab = \sum_{n=0}^\infty [t_n]p^n$. Then $s_n$ and $t_n$ are polynomials in the $a_i^{p^{i-n}}$, $b_i^{p^{i-n}}$ for $0 \leq i \leq n$. Furthermore, $s_n$ is homogeneous of degree 1 (where each $a_i$ and $b_i$ has degree 1), and $t_n$ is homogeneous in the $a_i$ and $b_i$ separately, each of degree 1.
>
>>Proof. Repeatedly use the identity
>>
>>$$
>>[x + y] \equiv ([x^{p^{-n}}] + [y^{p^{-n}}])^{p^n} \pmod{p^{n+1}},
>>$$
>>
>>which follows from Lemma 9.19.

>[!abstract]+ Prop 10.10
>
> Let $A$ be a strict $p$-ring, and let $B$ be a $p$-adically complete ring. Let $\sharp: A/pA \to B$ be a multiplicative map that induces a homomorphism of rings $A/pA \to B/pB$. Then the formula
>
> $$
> \Theta\left( \sum_{n=0}^\infty p^n [x_n] \right) = \sum_{n=0}^\infty p^n x_n^\sharp
> $$
>
> defines a $p$-adically continuous homomorphism $\Theta: A \to B$ such that $\Theta \circ [\cdot] = \sharp$.

We are especially interested in applying this result in the case where $A = W(\mathcal{O}_{K^\flat})$ and $B = \mathcal{O}_K$ for some perfectoid field $K$.

>Proof of Theorem 10.7. Full faithfulness follows from Proposition 10.10.
>
>To prove essential surjectivity, let $R$ be a perfect ring of characteristic $p$, and write $R = \mathbb{F}_p[X^{p^{-\infty}}]/\overline{I}$ for some set $X$ and ideal $\overline{I} \subset \mathbb{F}_p[X^{p^{-\infty}}]$. Let $A_0$ be the $p$-adic completion of $\mathbb{Z}_p[X^{p^{-\infty}}]$; then one can check that $A_0$ is a strict $p$-ring and $A_0/pA_0 = \mathbb{F}_p[X^{p^{-\infty}}]$. Let $I \subset A_0$ be the set of elements of the form $\sum_{n=0}^\infty p^n [x_n]$ with $x_n \in \overline{I}$. Then one can check that $I$ is an ideal of $A_0$ and $A := A_0/I$ is a strict $p$-ring with $R = A/pA$.

Let $K$ be a perfectoid field.

>[!notes]+ Def 10.11
>
> An ideal $I$ of $W(\mathcal{O}_{K^\flat})$ is primitive of degree 1 if it is generated by an element of the form $p + [\pi]\alpha$ for some $\pi \in \mathfrak{m}_{K^\flat}$, $\alpha \in W(\mathcal{O}_{K^\flat})$.

>[!abstract]+ Prop 10.12
>
> The map
>
> $$
> \Theta: W(\mathcal{O}_{K^\flat}) \to \mathcal{O}_K
> $$
>
> defined in Proposition 10.10 has the following properties:
>
> (1) $\Theta$ is surjective.
>
> (2) $\ker \Theta$ is primitive of degree 1.
>
>>Proof. By Lemma 9.18(4), the map $\sharp$ is surjective mod $p$. So by successive approximation, every element of $\mathcal{O}_K$ can be written as $\sum_{n=0}^\infty a_n^\sharp p^n$ for some $a_n \in \mathcal{O}_{K^\flat}$. Therefore, $\Theta$ is surjective.
>>
>>If $K$ has characteristic $p$, then $\ker \Theta = (p)$ is primitive of degree 1. Now suppose $K$ has characteristic 0. Choose $\pi^\flat \in \mathcal{O}_{K^\flat}$ so that $\pi := (\pi^\flat)^\sharp$ satisfies $|\pi| = |p|$. Choose $x \in W(\mathcal{O}_{K^\flat})$ satisfying $\Theta(x) = -p/\pi$. Since $\Theta(x)$ is a unit of $K$, the constant term in the Teichmuller expansion of $x$ must be a unit; then $x$ is also a unit. Let $\xi = p + [\pi^\flat]x$; then $\xi \in \ker \Theta$. We claim that in fact $\xi$ generates $\ker \Theta$. Observe that $\ker \Theta \subseteq ([\pi^\flat],p) = (\xi,p)$. So any element of $\ker \Theta$ can be written as $a\xi + bp$ with $\Theta(pb) = p\Theta(b) = 0$. Since $p$ is not a zero divisor in $\mathcal{O}_K$, we get $\Theta(b) = 0$. By successive $p$-adic approximation, we see that $\ker \Theta = (\xi)$.

**Remark 10.13**. If you find it dissatisfying that we used a separate argument for $p = 0$, see [BMS18, Lemma 3.2ii, Lemma 3.10] for a version of the argument that generalizes better. Essentially, the idea is to use Lemma 10.9 to prove that $W(\mathcal{O}_{K^\flat})$ is complete for the $[\pi^\flat]$-adic topology; then we can use $[\pi^\flat]$-adic approximation and we can assume $|p| \leq |\pi| = 1$ instead of $|\pi| = |p|$.

>[!abstract]+ Prop 10.14
>
> The category of perfectoid fields is equivalent to the category of pairs $(K,I)$, where $K$ is a perfectoid field of characteristic $p$ and $I \subset W(\mathcal{O}_K)$ is an ideal that is primitive of degree 1.
