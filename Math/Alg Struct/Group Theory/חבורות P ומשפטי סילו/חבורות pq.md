משפט (5.23)
If $p < q$ primes and $G$ a group such that $\lvert G \rvert = p \cdot q$,

1) Then $Syl_q(G) = \left\{ Q \right\}$ ($\iff$ $Q \trianglelefteq G$). ^451ec8

If in addition $q \not\equiv 1 \: mod \: p$,

2) Then G is cyclic. ^8a6f46

^c5ba23

Proof:
[[#^451ec8 | (1):]]  From [[משפט סילו 3 | Sylow theorem 3]] we have that:
	(a) $n_q \: \Big\vert \: m \quad (m = p)$
	(b) $n_q \equiv 1 \: mod \: q$
	And since $p < q$ we conclude that $n_q = 1$.
[[#^8a6f46 | (2):]] From [[משפט סילו 3 | Sylow theorem 3]] we have that (a)$\: n_p \: \Big\vert \: q$ $\quad\wedge\quad$ (b)$\: n_p \equiv 1 \: mod \: p$.
	From (a) we have $n_p \in \left\{ 1,q \right\}$
	And from (b) we have $n_p \not = q$
	So we conclude that $n_p = 1$.
	Now, we have $G \trianglerighteq P  \in Syl_p(G)$ and $G \trianglerighteq Q  \in Syl_q(G)$. Thus $G \geq P \cdot Q \cong P \times Q$. And since $P \cap Q = \left\{ e \right\}$ (Look at the order of the elements in each...), we have that $\left\vert P \cap Q \right\vert = p \cdot q = \left\vert G \right\vert$. So $G = P \cdot Q$.
	And, since Both $P$ and $Q$ are cyclic (Prime sizes...) we have $P \cong \mathbb{Z_p} \quad\wedge\quad Q \cong \mathbb{Z_q}$ And thus $P \times Q \cong \mathbb{Z_p} \times \mathbb{Z_q}$
	And all combined we get that $G = P \cdot Q \cong P \times Q \cong \mathbb{Z_p} \times \mathbb{Z_q}$.
	Now from [[The Chinese remainder theorem]] we conclude that G is cyclic.
*Note: Here we used the knowledge about the way a group can be broken down as a product of subgroups, I have not written it yet, so we need to refer back to it when it is available in the graph*

Comment (5.25): If $q \equiv 1 \: mod \: p$ then there is a non-abelian group of size $p \cdot q$. (The semidirect product of P and Q...).

(For example, let $p = 2$ and $q = 3$. $3 \equiv 1 \: mod \: 2$, and indeed we have $S_3$ which is a non-abelian group of size 6)

Exercise (5.26): Proof that there are only 2 groups of size 6 (Up to isomorphism)
Solution: 