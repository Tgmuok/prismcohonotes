In the remaining part of the course, we will do some geometry. We are interested in developing a theory similar to the theory of schemes, but where the rings are allowed to have topology. Clausen–Scholze have proposed a very general framework for analytic geometry, and you have seen some of this framework in the learning seminar on real local Langlands. This theory is very technical and involves the use of condensed mathematics and $\infty$-categories. We will instead use the older, less general framework of adic spaces, developed by Huber. In the cases where Huber's theory works, it should be equivalent to that of Clausen–Scholze.

An example of the type of space we want to consider is the closed $p$-adic unit disc over $\mathbb{Q}_p$. A function on the disc should be an element of

$$
\mathbb{Q}_p \langle T \rangle = \left\{ \sum_{n=0}^\infty a_n T^n \bigg| a_n \in \mathbb{Q}_p, \lim_{n \to \infty} a_n = 0 \right\}.
$$

Let $\mathbb{Z}_p \langle T \rangle \subset \mathbb{Q}_p \langle T \rangle$ be the subring consisting of power series with coefficients in $\mathbb{Z}_p$. Then it is natural to give $\mathbb{Q}_p \langle T \rangle$ a topology by letting the sets $p^n \mathbb{Z}_p \langle T \rangle$ be a basis of open neighborhoods of 0.

>[!notes]+ Def 20.1
>
>A Huber ring is a (Hausdorff) topological ring $A$ such that there exists an open subring $A_0 \subset A$ and a finitely generated ideal $I \subset A_0$ so that $A_0$ has the $I$-adic topology (powers of $I$ form a basis of neighborhoods of the identity).
>
>We say that $A_0$ is a *ring of definition* of $A$ and $I$ is an *ideal of definition* of $A_0$.

**Remark 20.2.** Huber rings are "solid" in the sense of Clausen–Scholze.

>[!example]+ ex 20.3
>
>The following topological rings are Huber rings.
>
>- Any ring with the discrete topology ($A_0 =$ any subring, $I = 0$).
>- $\mathbb{Z}_p$, ($A_0 = \mathbb{Z}_p$, $I = (p)$)
>- $\mathbb{Q}_p$, ($A_0 = \mathbb{Z}_p$, $I = (p)$)
>- More generally, any field $K$ with a nonarchimedean norm ($A_0 = \mathcal{O}_K := \{x \in K \mid |x| \leq 1\}$, $I = (\pi)$) for any $\pi \in K^\times$ satisfying $|\pi| < 1$. Note that if $|K^\times|$ is not discrete, then the maximal ideal of $\mathcal{O}_K$ is not finitely generated, so we cannot take $I$ to be the maximal ideal of $\mathcal{O}_K$.
>- The Tate algebra $K \langle T \rangle = \{\sum_{n=0}^\infty a_n T^n \mid \lim_{n \to \infty} a_n = 0\}$ ($A_0 = \mathcal{O}_K \langle T \rangle :=$ series with $|a_n| \leq 1$ for all $n$, $I = (\pi)$)
>- $\mathbb{Z}_p [\![ T ]\!]$ ($A_0 = \mathbb{Z}_p [\![ T ]\!]$, $I = (p,T)$)
>- $W(\mathcal{O}_{K^\flat})$ for a perfectoid field $K$ ($A = W(\mathcal{O}_{K^\flat})$, $I = (p, [\pi])$ where $\pi \in \mathcal{O}_{K^\flat}$ satisfies $0 < |\pi| < 1$)

>[!notes]+ Def 20.4
>
>Let $A$ be a ring. A *valuation* on $A$ is a map $|\cdot|: A \to \Gamma \cup \{0\}$, where $\Gamma$ is a totally ordered abelian group (written multiplicatively), satisfying the following properties:
>
>1. $|xy| = |x||y|$ for all $x,y \in A$
>2. $|x + y| \leq \max(|x|, |y|)$ for all $x,y \in A$
>3. $|0| = 0$, $|1| = 1$
>
>If $A$ is a topological ring, then we say that a valuation is *continuous* if for all $\gamma \in \Gamma$, $\{a \in A : |a| < \gamma\}$ is open.
>
>We say that two valuations $|\cdot|$ and $|\cdot|'$ are *equivalent* if $|a| \leq |b| \iff |a|' \leq |b|'$ for all $a,b \in A$.


>[!notes]+ Def 20.5
>
>Let $A$ be a topological ring. Define $\mathrm{Cont}(A)$ to be the set of equivalence classes of continuous valuations of $A$.
>
>Give $\mathrm{Cont}(A)$ the topology with a sub-basis of open sets consisting of sets the form
>$$
>\{x \mid |f(x)| \leq |g(x)| \neq 0 \}.
>$$
>for $f,g \in A$. Here $|f(x)|$, $|g(x)|$ denote the valuations of $f$ and $g$ under a representative of the equivalence class $x$.

>[!notes]+ Def 20.6
>
>Let $A$ be a topological ring. A subset $S$ of $A$ is *bounded* if for all open neighborhoods $U$ of 0, there is an open neighborhood $V$ of 0 such that $VS \subset U$.

>[!notes]+ Def 20.7
>
>Let $A$ be a Huber ring. An element $f \in A$ is *power-bounded* if $\{f^n \mid n \in \mathbb{N}\}$ is bounded.
>
>We will write $A^\circ$ for the subring of power-bounded elements of $A$.

>[!notes]+ Def 20.8
>
>Let $A$ be a Huber ring. A subring $A^+ \subset A^\circ$ is a *ring of integral elements* if it is open and integrally closed in $A$.
>
>A *Huber pair* is a pair $(A, A^+)$, where $A$ is a Huber ring, and $A^+ \subset A$ is a ring of integral elements.
>
>For a Huber pair $(A, A^+)$, define $\mathrm{Spa}(A, A^+) \subset \mathrm{Cont}(A)$ to be the subspace consisting of those valuations $x$ for which $|f(x)| \leq 1$ for all $f \in A^+$.

>[!example]+ ex 20.9
>
>The points of $\mathrm{Spa}(\mathbb{Z}, \mathbb{Z})$ are as follows:
>
>1. $\eta$: $|n(\eta)| = \begin{cases} 1, & n \neq 0 \\ 0, & n = 0 \end{cases}$
>2. For each prime $p$, $s_p$: $|n(s_p)| = \begin{cases} 1, & p \nmid n \\ 0, & p \mid n \end{cases}$
>3. For each prime $p$, $\eta_p$: $|n(\eta_p)| = |n|_p$ (the usual $p$-adic absolute value)
>
>The point $s_p$ is closed, while $\overline{\{\eta_p\}} = \{\eta_p, s_p\}$ and $\overline{\{\eta\}} = \mathrm{Spa}(\mathbb{Z}, \mathbb{Z})$.

>[!example]+ ex 20.10
>
>Let $K$ be a nonarchimedean field, and let $\mathcal{O}_K$ be its ring of integral elements. The space $\mathrm{Spa}(K \langle T \rangle, \mathcal{O}_K \langle T \rangle)$ is called the *closed unit disc over $K$*.
>
>Let $C$ be an algebraically closed nonarchimedean field. Let $k$ be the residue field of $C$. The points on the closed unit disc over $C$ can be classified into five types:
>
>- For any $\alpha \in \mathcal{O}_C$, there is a point $f \mapsto |f(\alpha)|$. These are called "Type 1" points.
>- For $\alpha \in \mathcal{O}_C$, $r \in (0,1]$, let $B(\alpha, r)$ denote the closed ball of radius $r$ centered at $\alpha$ in $\mathcal{O}_{\mathbb{C}_p}$. Then
>$$
>f \mapsto \sup_{\alpha \in B(\alpha,r)} |f(\alpha)|
>$$
>is a point of $D$. Equivalently, we can describe this norm by
>$$
>\sum_{n=0}^\infty a_n (T - \alpha)^n \mapsto \sup_n |a_n| r^n.
>$$
>We call this point "Type 2" if $r \in \mathbb{Q}_{>0}$ (i.e. it is the valuation of some element of $\mathcal{O}_C$), and "Type 3" otherwise.
>- The ring $C$ is may not spherically complete, i.e. there may exist descending sequences $B_1 \subset B_2 \subset \cdots$ of closed balls with empty intersection. (Since $\mathbb{C}_p$ is complete, any descending sequence of discs whose radii go to zero have a common interesection point. But this need not be the case if the radii do not go to zero.) For example, $\widehat{\overline{\mathbb{Q}}}_p$ is not spherically complete.
>
>There is a valuation
>$$
>f \mapsto \inf_i \sup_{\alpha \in B_i} |f(\alpha)|.
>$$
>These are called Type 4 points or "dead ends".
>- As mentioned before, we can consider the value group $\mathbb{R}_{>0} \times \mathbb{R}_{>0}$ with lexicographic ordering. For any $B(\alpha, r)$ with $r$ rational, we can define the norms
>$$
>\sum_{n=0}^\infty a_n (T - \alpha)^n \mapsto \sup_n (|a_n| r^n, p^{-n})
>$$
>$$
>\sum_{n=0}^\infty a_n (T - \alpha)^n \mapsto \sup_n (|a_n| r^n, p^{n})
>$$
>(If $r = 1$, then the latter norm belongs to $\mathrm{Cont}\, \mathbb{C}_p \langle T \rangle$ but not to the closed unit disc.) These are called Type 5 points. Note that for $r$ irrational, the above definition makes sense, but we end up with a norm that is equivalent to the Type 3 norm described above.
>
>All points except for Type 2 points are closed. The closure of a Type 2 point looks like $\mathbb{P}^1_{\overline{\mathbb{F}}_p}$ (or $\mathbb{A}^1_{\overline{\mathbb{F}}_p}$ if $r = 1$). The Type 2 point is the generic point and the Type 5 points are the closed points.


>[!example]+ ex 20.11
>
>The ring $\mathcal{O}_K + \mathfrak{m}_K T \mathcal{O}_K \langle T \rangle$ is also a ring of integral elements of $K \langle T \rangle$. Then $\mathrm{Spa}(K \langle T \rangle, \mathcal{O}_K + \mathfrak{m}_K T \mathcal{O}_K \langle T \rangle)$ contains all points of $\mathrm{Spa}(K \langle T \rangle, \mathcal{O}_K \langle T \rangle)$, plus one additional point where $|T|$ is infinitesimally greater than 1.

>[!example]+ ex 20.12
>
>In the previous examples, the ring of integral elements is also a ring of definition. But this is not always the case. For example, if $A = \mathbb{Q}_p[\epsilon]/(\epsilon^2)$, then the only possible ring of integral elements is $A^\circ = \mathbb{Z}_p + \mathbb{Q}_p \epsilon$, but this ring is not a ring of definition.

>[!notes]+ Def 20.13
>
>A *spectral space* is a topological space that is homeomorphic to the spectrum of some ring. Equivalently, a spectral space is a limit of finite $T_0$ spaces.

>[!danger]+ Them 20.14
>
>For any Huber pair $(A, A^+)$, $\mathrm{Spa}(A, A^+)$ is spectral.
