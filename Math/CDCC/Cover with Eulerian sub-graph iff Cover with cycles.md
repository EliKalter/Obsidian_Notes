
>Theorem:
	Let $G = (V,E)$ be  a finite [[Graph]].
	Let $S \subseteq E$. Then:
	There is a collection of cycles ([[A closed walk in a graph|Closed]] [[A path in a graph|Path]]s) $C_I = \{C_i\}_{i \in I}$ that coven each edge in $S$ exactly once $\iff$ There is an [[Eulerian sub-graph]] $G' = (V', E')$ of $G$ s.t. $E' = S$.
>Proof:
>	>$\implies$:
>	>	For $i \in I$ denote $C_i = (v_j^i)_{j = 0}^{n_i}$, $V_i := \{ v_j^i \}_{j = 1}^{n_i}$ And $E_i := \{ v_j^i, v_{j - 1}^i \}_{j = 1}^{n_i} \subseteq E$
>	>	Define $V' := \bigcup\limits_{i \in I} V_i$ And $E' := \bigcup\limits_{i \in I} E_i$.
>	>	Now $G' := (V', E')$. Clearly $S = E'$ as $E'$ is exactly the edges covered by $C_I$, and $C_I$ was given to cover every edge in $S$ exactly once. We want to show that $G'$ is an Eulerian sub-graph.
>	>	Let $v \in V'$. Denote $E_v := \{ e \in E' \mid v \in e\}$ we want to show that $\lvert E_v \rvert$ is even. Denote $C_v := \{ C_i \in C \mid v \in V_i\}$. For every $C \in C_v$ There is $i \in I$ s.t. $C = C_i$. Since $C$ is a cycle that contains $v$, there are $e_{i_1}, e_{i_2}$ s.t. $e_{i_1} \ne e_{i_2}$ and $v \in e_{i_1} \cap e_{i_2}$. Denote $E_v^i := \{e_{i_1}, e_{i_2}\}$. We have $\lvert E_v^i \rvert = 2$, $\forall i,j \in I: i \ne j \implies E_v^i \cap E_v^j = \emptyset$ and $E_v = \bigcup\limits_{i \in I} E_v^i$.
>	>	Thus $\lvert E_v \rvert = \sum_{i \in I} \lvert E_v^i \rvert = 2 \lvert C_v \rvert$
>	
>	>$\impliedby$:
>	>	Let $G' = (V', E')$ a sub-graph of $G$ with $E' = S$.
>	>	Let $l$ be the number of [[connected components]] (TODO: Define) in $G'$.
>	>	Assume we have $\{C_{I_j}\}_{j = 1}^l$ collections of cycles s.t. $C_{I_j}$ covers every edge in the $j$'th connected component of $G'$ exactly once. Then $I := \bigcup\limits_{j=1}^l I_j$, and $C_I := {C_i}_{i \in I}$ is a cover of $S$ that covers each edge exactly once. So all we need to show it that we can find a cover with cycles for one connected component.
>	>	Assume $G'$ is connected. Now $G'$ being a connected eulerian graph, [[means that there is an eulerian circuit]] (TODO: Prove that eulerian circuit iff connected and even degree) in $G'$. Let $v = (v_i)_{i=1}^n$ be such a circuit. 