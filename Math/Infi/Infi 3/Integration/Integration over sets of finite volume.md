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
>So we conclude that $D(\chi_S \big\vert_A)$ is of measure zero iff $\partial S$ is of measure zero. So by the lebesgue-vitali, the indicator func of S restricted to A is integrable iff S has zero measure boundry.

>But we have not yet shown that the volume of S is well defined, meaning that it does not depand on the choise of A. The following lemm;a should be helpful with that.

>Lemma:
>	A set of measure zero can not only be covered with boxes, but it can be covered in the same way s.t. every point of the set is within the interior of some box.
>	(And we can assume each of the boxes has in its interior some point of A, otherwise, just ignore it, and we still have a cover)
>Proof:
>	We can have a first cover that matches epsilon over 3^k. Then it covers. And taking for each of those boxes the box that is increasing for each edge, its length by 3, yields a box that is of volume exactly 3^k more than the original, and this time every point that was covered by the original, will be in the interior of the new one, becasue the old one is contained in the interior of the new one.

^24e5ab

>Lemma:
>	If a box B has an interior point, that belongs to some other box A, then their intercetion is a Box.
>Proof:
>	First we check what can the intersection of two boxes can be
>	$$\bigtimes\limits_{i=1}^{k} \left([a_i,b_i] \cap [c_i,d_i] \right)$$
>	And for each coordinate we get $[max\left\{ a_i,c_i \right\}, min\left\{ b_i,d_i \right\}]$
>	So it can either be empty, or it can be degenerate, or it can be of real width
>	And since we assumed B has some interior point of A, only the last option is possible.

^817595

>Lemma:
>	A set of measure zero J that is contained in a box A, can be covered with boxes that are all contained in the original box, and with the right volume.
>Proof:
>	From [[#^24e5ab]] we can cover J with boxes s.t. each box has an interior point of J. that point is also of A. So by [[#^817595]] the intercetion of the box with A is also a box. So we get that the collection of intersections covers J and made of good boxes.

^713e7f


>Lemma (3.22):
>	If f (f is bounded) is 0 on the interior of A (a box) then f is integrable on A and the integral is 0
>Proof:
>	For epsilon, Cover the boundry of A (Which is of measure zero [[]]) with boxes such as in [[#^713e7f]]. And from [[Integration over boxes#^063141]] we get that a finite subset of those boxes is enough (Because a boundry is always a closed set wich is compact in a norm space).
>	Now take P a partition of A that includes all the points from all those boxes. And by [[Integration over boxes#^fb2b80]] we have that for every sub-box induced by the partition there is some box in the B boxes, that containes that sub-box. so the sum of the volume of all the boxes in the partition is not more than the volume of the boxes (which was smaller than epsilon).
>	Now we notice that only those boxes that touch the boundry of A can have non zero val of f. So we can sum over the boxes in the partition that involve those boxes that do touch the boundry. And those are contained in the B's.
>	Over all: $$L(f,P) = \sum_{C \in P}m_i V(C) = \sum_{C \in P \text{C touches the boundry of A}}m_i V(C) \geq$$ $$\geq \sum_{C\in P \text{...}} -MV(C) \geq -M\varepsilon$$
>	(Where M is from the boundry on the abs val of f)
>	And similarly for the upper sum. So the lower is bounded from below by -2M$\cdot \varepsilon$ and the lower is no more than 2M$\cdot \varepsilon$.
>	And since epsilon was arbitrary, we get that the difference between the upper and lower is arbitrarily small, meaning 0. So the func is integrable. And since we've shown everything has to tend to 0, the integral is 0.

The last lemma can be shown in simpler terms (such as taking a delta sliver around the boundry of the box similar to how it would be done for [a,b] subset R with [a + delta, b - delta])
But the benefit is that now we get the following proposition in the same way

>Proposition (3.23):
>	If A is a box, and J is a compact subset of A of measure zero, and f is a func from A to R that is zero out of J, than f is integrable over A with integral 0.
>Proof:
>	For the same reasons there is a cover with good boxes, And since J is compact, a finite amount of those boxes is enough, and the ones that do not touch J can be ignored, we can create a partition P that containes all the points from those boxes, and drop the sub-boxes that don't touch J, and the upper and lower sums are bounded in the same way as in the last proof.

>Note: The requirement of compactness is necasery. If you take A = [0,1] and J = Q cut A, then the dirichlet fun (D(x)) is not integrable over A, although it is not zero only on J, which is of measure zero as it is contained in Q which is of measure zero (as it is countable). And that is not a contradiction to the last proposition, because such J is not compact

