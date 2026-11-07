

>Theorem:
>	[[Graphs|The formulation of the theorem for regular graphs]] and [[Multi graphs|The formulation of the theorem for multi-graphs]] are equivalent.
>Proof:
>	>(1) $\impliedby$:
>	>	Let $G = (V,E)$ be a graph that is free of bridges . Since $M = (V,E,Id_E)$ is a multi graph, by the assumption of the right side we get $C_I = \{C_i\}_{i \in I}$ [[A closed walk in a graph|Closed]] [[A path in a graph|Paths]] in $M$ s.t. every edge in $E$ is covered exactly twice.
>	>	Notice that every $C_i$ is also a closed path in $G$ and that $C_I$ satisfies the requirements of the left side.
>	
>	>(2) $\implies$:
>	>	Let $M = (V,E,\phi)$ be a [[Multi graph]] that is free of bridges.
>	>	(a) We will build a graph $G$ from M that is free of bridges.
>	>	(b) We will show that given $C_I$ that double covers $G$ we can build $C_J$ that double covers $M$.
>	
>	>(a):
>	>	$E' := \{ e \in \rho(V) \mid \lvert e \rvert = 2 \wedge \exists u \in E: e = \phi(u) \}$.
>	>	$G := (V,E')$.
>	>	We now show that $M$ is free of bridges:
>	>		Let $e \in E'$. Then there is $u \in E$ s.t. $e = \phi(u)$. Since $M$ is free of bridges, we get $v = (v_0, e_1, v_1,\dots, e_n, v_n)$ s.t.:
>	>		>(1): $v_0 = v_n$,
>	>		
>	>		>(2): $i \ne j \implies v_i \ne v_j$ (Except for when $\{i,j\} = \{0,n\}$),
>	>		
>	>		>(3): $\forall i \in [n]: \{ v_i, v_{i-1}\} = \phi(e_i)$,
>	>		
>	>		>(4): $\exists i \in [n]: \{ v_i, v_{i-1}\} = \phi(u)$.
>	>		
>	>		Thanks to (3), all the edges involved in $v$ are also edges in $E'$. Thanks to (1) + (2), $v$ is a cycle. Combining these two facts together we get that $v$ is a cycle in $G$. And thanks to (4) we get that $e$ is in the cycle $v$. So $e$ is not a bridge in $G$. So $G$ is free of bridges.
>	
>	>(b):
>	>	Let $C_I$ be a collection of cycles that double covers $G$. And let $e \in E$.
>	>	If $e$ is a [[Multi graph#^dcf613|self edge]], then
>	>	>$e$ is not covered by any cycle in $C_I$ (Because cycles in a regular graph do not have steps that lead from a node to itself)
>	>	>There is some $v \in V$ s.t. $\phi(e) = v$.
>	>	>We define $C_e := \{ C_{e_1}, C_{e_2}\}$ where $\forall i \in [2]: C_{e_i} = (v, e, v)$.
>	>	
>	>	>For a pair of two distinct vertices $v_1, v_2 \in V$, denote $E_{\{v_1,v_2\}} := \phi^{-1}(\{v_1,v_2\})$. Now, by the well ordering theorem (TODO: Link to it) $E_{\{v_1,v_2\}}$ either can be broken down into pairs, or it can be broken down into pairs, with one element staying alone.
>	>	>Denote $S(E_{\{v_1,v_2\}}) := \begin{cases} \text{Some arbitrary pair in } E_{\{v_1,v_2\}} & E_{\{v_1,v_2\}} \text{ can be broken down into pairs} \\ \text{The only set of size 1 in } E_{\{v_1,v_2\}} & E_{\{v_1,v_2\}} \text{ can't be broken down into pairs} \end{cases}$
>	>
>	>	Else $e$ is a regular edge that connects two distinct vertices call them $v_1, v_2$, (i.e. $\phi(e) = \{v_1,v_2\}$). And we know that $\phi(e) \in E'$.
>	>	Now, denote $E_{\phi(e)} := \phi^{-1}(\phi(e))$. $E_e$ is not empty ($e \in E_{\phi(e)}$).
>	>	
>	>	>If $e \not\in S(E_{\phi(e)})$ then $e$ is in a regular pair in $E_{\phi(e)}$, say $\{e, e'\}$. Define $C_e := (v_1, e, v_2, e', v_1)$. (Notice that this covers both the edges in the pair once, and also will $C_{e'}$
>	
>	>	>Else $e \in S(E_{\phi(e)})$.
>	>	>Recall that $C_I$ covers every edge in $E'$ exactly twice, so we get $u = (u_0, e_{u_1}, \dots, e_{u_n}, u_n)$, and $w = (w_0, e_{w_1}, \dots, e_{w_n}, w_m)$ with $\exists i \in [n], j \in [m]: \phi(e) = e_{u_i} = e_{w_j}$.
>	>	>If $\lvert S(E_{\phi(e)}) \rvert = 1$: Define $C_e := \{ C_{e_1}, C_{e_2}\}$ where $\forall i \in [2]: C_{e_i} = (v, e, v)$
>	>	
>	The idea is:
>	For any pair of vertices, we look at the set of edges connecting them. If it is empty, we ignore it. Else it can be broken down into pairs, or pairs with one left over. If we have one left over, take it to represent the set. Other wise choose some arbitrary pair of such edges to represent that pair of vertices. Now, pull back $C_I$ from $G$ to $M$, by looking at an edge $e \in E$ that is not a self edge, and picking the two cycles in $C_I$ that cover $\phi(e)$, and choosing 

Do I need infinite induction?


TODO: Complete