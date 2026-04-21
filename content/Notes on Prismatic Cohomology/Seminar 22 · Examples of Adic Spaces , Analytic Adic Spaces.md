>[!example]+ ex 22.1
>
>The closed disc over $\mathbb{C}_p$ is $\mathrm{Spa}(\mathbb{C}_p \langle X \rangle, \mathcal{O}_{\mathbb{C}_p} \langle X \rangle)$. Similarly, the closed disc over $\mathbb{Q}_p$ is $\mathrm{Spa}(\mathbb{Q}_p \langle X \rangle, \mathbb{Z}_p \langle X \rangle)$.

>[!example]+ ex 22.2
>
>$\mathrm{Cont}\,\mathbb{C}_p \langle X \rangle = \mathrm{Spa}(\mathbb{C}_p \langle X \rangle, A^+)$ where
>
>$$
>A^+ = \left\{ \sum_{i=0}^{\infty} a_i X^i \,\bigg|\, a_0 \in \mathcal{O}_{\mathbb{C}_p},\, a_i \in \mathfrak{m}_{\mathbb{C}_p} \text{ for } i > 0,\, \lim_{i \to \infty} a_i = 0 \right\}
>$$

>[!example]+ ex 22.3
>
>Let $r \in \mathbb{Q}$. Let $A$ be the ring of power series $\sum_{n=0}^{\infty} a_n T^n$ with $a_n \in \mathbb{Q}_p$ and $|a_n||p|^{nr} \to 0$ as $n \to \infty$. Let $A^+$ be the subring consisting of series with $|a_n||p|^{nr} \in \mathbb{Z}_p$ for all $n$. We give $A$ the topology such that $A^+$ is open in $A$, and $A^+$ has the $p$-adic topology. Then $\mathrm{Spa}(A, A^+)$ is the closed disc of radius $|p|^r$.

>[!example]+ ex 22.4
>
>The open disc of radius 1 over $\mathbb{Q}_p$ is the union of the closed discs of radius $< 1$.

>[!example]+ ex 22.5
>
>The affine line $\mathbb{A}^1$ is the union of closed discs of radius $p^r$.

>[!example]+ ex 22.6
>
>The projective line $\mathbb{P}^1$ is the union of two closed discs, glued along an annulus.

>[!example]+ ex 22.7
>
>Consider $D = \mathrm{Spa}(\mathbb{Z}_p [\![ T ]\!], \mathbb{Z}_p [\![ T ]\!])$. It contains the open disc of radius 1 over $\mathbb{Q}_p$. It has exactly two additonal points, correspoding to the trivial norm on the quotient $\mathbb{F}_p$, and the $T$-adic norm on $\mathbb{F}_p [\![ T ]\!]$.

>[!example]+ ex 22.8
>
>The closed disc over $\mathbb{Z}$ (with the discrete topology on $\mathbb{Z}$) is $\mathrm{Spa}(\mathbb{Z}[T], \mathbb{Z}[T])$. It represents the functor $X \mapsto \mathcal{O}_X^+(X)$.

>[!example]+ ex 22.9
>
>The affine line over $\mathbb{Z}$ is $\mathrm{Spa}(\mathbb{Z}[T], \mathbb{Z})$. It represents the functor $X \mapsto \mathcal{O}_X(X)$. Unlike the affine line over $\mathbb{Q}_p$, it is affinoid.

>[!example]+ ex 22.10
>
>Let $S$ be a profinite set, and let $A$ be the space of continuous (i.e. locally constant) functions $S \to \mathbb{Z}$, with the discrete topology. Then $\mathrm{Spa}(A, A)$ represents the functor $X \mapsto \mathrm{Hom}(|X|, S)$.

>[!notes]+ Def 22.11
>
>Let $X$ be an adic space. A point $x \in X$ is *analytic* if it has a neighborhood of the form $\mathrm{Spa}(A, A^+)$, with $A$ Tate. We say $X$ is *analytic* if all of its points are analytic.

>[!abstract]+ Prop 22.12
>
>Let $(A, A^+)$ be a sheafy Huber pair. Then a point $x \in \mathrm{Spa}(A, A^+)$ is analytic iff the kernel of $|\cdot|_x$ is not open.
>
>>*Proof.* Let $I = (a_0, \dots, a_n)$ be an ideal of definition of a ring of definition of $A$. Suppose that the kernel of $|\cdot|_x$ is not open. Then $I \not\subset \ker |\cdot|_x$. So the $|a_i|_x$ are not all zero. WLOG assume $|a_0|_x \geq |a_1|_x, \dots, |a_n|_x$. Then, on the rational subset defined by $|a_0| \geq |a_1|, \dots, |a_n|$, $a_0$ is a topologically nilpotent unit. In particular, this rational subset is the adic spectrum of a Tate ring.
>>
>>Conversely, suppose that the kernel of $|\cdot|_x$ is open. Let $\mathrm{Spa}(B, B^+)$ be an affinoid subspace of $\mathrm{Spa}(A, A^+)$ containing $x$. We claim that $\mathrm{Spa}(B, B^+)$ cannot be Tate. Let $\mathrm{Spa}(C, C^+)$ be a rational subset of $\mathrm{Spa}(A, A^+)$ containing $x$ and contained in $\mathrm{Spa}(B, B^+)$. Since the image of a topologically nilpotent unit in $\mathrm{Spa}(B, B^+)$ would be a topologically nilpotent unit in $\mathrm{Spa}(C, C^+)$, it suffices to prove that $C$ is not Tate.
>>
>>Since the kernel of $|\cdot|_x$ is open, it contains some power of $I$. Since $|\cdot|_x$ is multiplicative, the kernel must contain $I$. The generators of $I$ also generate an ideal of definition of $C$. Therefore, when $|\cdot|_x$ is extended to $C$, its kernel is still open. Hence $C$ cannot have a topologically nilpotent unit.

>[!example]+ ex 22.13
>
>The adic space $\mathrm{Spa}(\mathbb{Z}_p, \mathbb{Z}_p)$ consists of two points: a closed point $s$ given by
>
>$$
>|a|_s =
>\begin{cases}
>1, & a \in \mathbb{Z}_p^\times \\
>0, & a \in p\mathbb{Z}_p
>\end{cases},
>$$
>
>and a generic point $\eta$ given by the $p$-adic norm. The kernel of $|\cdot|_s$ is $p\mathbb{Z}_p$, which is open, so $s$ is not analytic. The kernel of $|\cdot|_\eta$ is $0$, which is not open, so $\eta$ is analytic.
>
>Analytic adic spaces are somewhat nicer than general adic spaces.

**Remark 22.14.** There exist complete Huber pairs $(A, A^+)$ such that $\mathrm{Spa}(A, A^+)$ is analytic, but $A$ is not Tate. See [Ked, §1].
