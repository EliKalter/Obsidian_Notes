>Theorem:
>	Let $U \subseteq \mathbb{R}^k$ be an open set.
>	Let $f,g_1,\dots ,g_m \in C^1(U, \mathbb{R})$ for $m < k$.
>	Denote $S := \bigcup\limits_{i=1}^{m} S_i$ for $S_i:=\left\{ x \in U \mid g_i(x) = 0 \right\} = g_i^{-1}(0)$.
>	Let $a \in S$ be a local extremum point of $f\big\vert_S$.
>	Then the set $\left\{ \nabla f(a) \right\} \cup \left\{ \nabla g_i(a) \right\}_{i=1}^{m}$, is [[]] linearly dependent.
>Proof:
>	ddd

>Result:
>	In the same setting, assume $\left\{ \nabla g_i(a) \right\}_{i=1}^{m}$ is linearly independent. Then there are $\alpha_1,\dots,\alpha_m \in \mathbb{R}$ s.t. $\nabla f(a) = \sum\limits_{i=1}^{m} \alpha_i \cdot \nabla g_i(a)$
>Proof:
>	Trivial.

^561a24

>Result:
>	Assume $m = 1$ (i.e. there is $g \in C^1(U, \mathbb{R})$) and $\nabla g(a) \neq 0_{\mathbb{R}^k}$, then there is $\alpha \in \mathbb{R}$ s.t. $\nabla f(a) = \alpha \cdot \nabla g(a)$
>Proof:
>	Just applying [[#^561a24|the last result]] to the $m=1$ case.

