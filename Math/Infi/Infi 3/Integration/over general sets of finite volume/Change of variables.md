A generalization of [[Infi/Infi 2/Change of variables|1 D change of variables]].

>Theorem (3.38) (Change of variables formula):
>	>Setting:
>	>	Let $U \subseteq \mathbb{R}^k$ be an open set.
>	>	Let $g \in C^1(U, \mathbb{R}^k)$ be one-to-one, s.t. $J_g(u) \neq 0$ for all $u \in U$. (Does this wording make sense? Given [[]] reverse funciton theorem, doesn't having non zero determinent everywhere mean you are reversable and thus one to one?).
>	>	Let $A \subset g(U)$ be a compact set (Compact is closed while the image of g is open becasue of the open mapping theorem [[]]) of volume.
>	
>	>Then:
>	>	For every integrable $f:A\to\mathbb{R}$ we have $$\int_A f(x)dx = \int_{g^{-1}(A)} f \circ g (x) \cdot \left\vert J_g(u) \right\vert du$$
>	>	That is, the integration can be "pulled back" into the pre image.
>	
>	>Proof:
>	>	Here we will not show the full proof, saving time. But we will mention the relevant leamms.

>Note:
>	The theorem implies that:
>	>(a): $f \circ g (x) \cdot \left\vert J_g(u) \right\vert$ is integrable
>	
>	>(b): $g^{-1}(A)$ is a set of volume

>Lemma:
>	The image of a set of measure zero, under a map that has bounded derivative (for example cont drivative), is of measure zero.

>Lemma:
>	If the derivative is ivertable in the interior, and tha map has cont drivative everywhere, then the image also has volume.

>Use:
>	We can notice that for $h = g^{-1}$, it matches the requirements for $h$ from the lemma, and it is applied to $A$ a compact set of volume. Thus, the lemma gives that the image is a set of volume.

>Note:
>	$f \circ g$ is integrable because g is cont, so every discontinuity comes from f, that is to say that $D(f \circ g) = D(f)$, and we are given that $D(f)$ is of measure zero.

