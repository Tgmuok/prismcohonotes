In $p$-adic Hodge theory, we consider étale cohomology groups $H_{\text{ét}}^i(X_K, \mathbb{Z}_p)$. In general, it is difficult to describe these groups explicitly. In some situations, we can be more explicit. One of these is the case where $X$ is an elliptic curve.

>[!notes]+ Def 3.1
>
> Let $K$ be a field. An elliptic curve over $K$ is pair $(E,O)$, where $E$ is a complete smooth geometrically irreducible curve of genus 1 over $K$ and $O \in E(K)$.

Sometimes, we will abuse notation and call $E$ an elliptic curve.

If $K$ has characteristic $\neq 2$, then any elliptic curve is isomorphic to one of the form

$$
y^2 = x^3 + ax^2 + bx + c,
$$

where $x^3 + ax^2 + bx + c$ is separable. When $E$ is written in this form, we usually take $O$ to be the point at $\infty$.

The curve $E$ has a group structure, meaning that there are morphisms

$$
+: E \times E \to E
$$

$$
-: E \to E
$$

$$
O: \text{Spec } k \to E
$$

(with $O$ being the point chosen above), satisfying the usual group axioms.

The group structure can be described as follows. Given two points $P_1, P_2$ on $E$, there is exactly one other point $Q$ where the line through $P_1, P_2$ intersects $E$. (If $P_1 = P_2$, we use the tangent line through $P_1$.) Define $P_1 + P_2$ to be the reflection of $Q$ about the $x$-axis.

Then the point at infinity is the identity, and the inverse of any point is its reflection about the $x$-axis.

To see that the group operation is associative, we consider line bundles on $E$. Let $dx + ey = f$ be the equation of the line through $P_1, P_2$, and let $g$ be the $x$-coordinate of the third intersection of this line with the elliptic curve. The rational function $\frac{dx+ey-f}{x-g}$ has zeros at $P_1, P_2$ and poles at $P_1 + P_2$ and $O$. It determines an isomorphism of line bundles

$$
\mathcal{O}([P_1] + [P_2] - [O]) \cong \mathcal{O}([P_1 + P_2]).
$$

Given a third point $P_3$, we have

$$
\mathcal{O}([P_1] + [P_2] + [P_3] - 2[O]) \cong \mathcal{O}([(P_1 + P_2) + P_3]) \cong \mathcal{O}([P_1 + (P_2 + P_3)])
$$

Since $E$ does not have genus 0, it cannot have a rational function with a single zero and pole, so we must have $(P_1 + P_2) + P_3 = P_1 + (P_2 + P_3)$.

The above proof is somewhat sketchy. A more rigorous treatment uses the Picard functor. There is a contravariant functor $\text{Pic}: \text{Scheme} \to \text{Ab}$ that sends a scheme $X$ to the group of isomorphism classes of line bundles on $X$, with the group operation being tensor product. For any map of schemes $X \to S$, there is a contravariant functor $\text{Pic}_{X/S}: \text{Scheme}/S \to \text{Ab}$ that sends a scheme $T$ over $S$ to $\text{Pic}(X \times_S T)/\text{Pic}(T)$. For any curve $X$ over $S$, there is a natural transformation $X \mapsto \text{Pic}_{X/S}$. If $X$ is projective, then any invertible sheaf on $X$ has a well-defined degree, so we can write

$$
\text{Pic}_{X/S} = \coprod_{d \in \mathbb{Z}} \text{Pic}_{X/S}^d.
$$

If $X$ is an elliptic curve, then one can show that $X \mapsto \text{Pic}_{X/S}^1$ is an isomorphism. The point $O$ also determines an isomorphism $\text{Pic}_{X/S}^1 \cong \text{Pic}_{X/S}^0$. Since $\text{Pic}_{X/S}$ has a group structure, $E$ does as well. For more details, see [KM85, Theorem 2.1.2].

**Remark 3.2.** If $X$ is a singular curve defined by a Weierstrass equation $y^2 = x^3 + ax^2 + bx + c$, then the nonsingular locus of $X$ still has a group structure. (If a line passes through a singular point of $X$, the intersection multiplicity is at least 2. So if a line intersects the curve at two nonsingular points, then the third intersection point must also be nonsingular.)

For example, the additive group $\mathbb{G}_a = \text{Spec } K[t]$ is isomorphic to the nonsingular locus of the cuspidal cubic $y^2 = x^3$ via the map $t \mapsto (t^{-3}, t^{-2})$. We leave it as an exercise to the reader to check that this map is a homomorphism of groups.

**Remark 3.3.** Although the focus of today's lecture was on elliptic curves over fields, one can define an elliptic curve over an arbitrary scheme $S$. It is a pair $(E,O)$, where $E$ is a smooth proper curve over $S$ with geometrically connected fibers of genus 1, and $O: S \to E$ is a section of $E \to S$.

If $E$ is a smooth degree 3 curve in $\mathbb{P}_S^2$ equipped with a section $O: S \to E$, then $(E,O)$ is an elliptic curve. Even if $E$ is not smooth, the nonsingular locus still has a group structure with identity $O$.
