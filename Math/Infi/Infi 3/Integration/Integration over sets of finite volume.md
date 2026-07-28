>Def (3.21) (The indicator function):
>	...

>Def (Has volume):
>	A set S is said to have volume when there is some box A that contains S s.t. the integral over A of the indicator of S exists.

>Example:
>	The  set $S = \mathbb{Q}^2 \cup [0,1]^2 \subset \mathbb{R}^2$ does not have volume. (Because the indicator of S is similar to the "דיריכלה" func)

>Def (The vol of a set):
>	If S is a set in R that has volume, we call that integral (the integral over some box that contains S of the indicator of S) the volume of S.

>Note:
>	A box has volume, and it is the same as the volume we defined for it [[Integration over boxes#^1ae6d6|here]] (before we had integrals...).
>	To be convinced look [[Integration over boxes#^b86a28|here]].

>Lemma:
>	If A of zero measure and B is not, then B \ A is not.
>Proof:
>	B = B \ A union A and union of zero mesure is zero measure.

>Lemma:
>	If A contained in B and A is not of zero measure than B is also.
>Proof:
>	Obviously if B is of zero than also is A.

>We have seen that the discon point of the indicator of S is the boundry of S.
>We also can see that $\partial S \setminus \partial A \subseteq D(\chi_S \big\vert_A) \subseteq \partial S$.
>And [[Integration over boxes#^2e6e3c|we know]] that the boundry of $A$ is of measure zero.
>So we conclude that $D(\chi_S \big\vert_A)$ is of measure zero iff $\partial S$ is of measure zero. Meaning, S has volume iff it has zero measure boundry.

