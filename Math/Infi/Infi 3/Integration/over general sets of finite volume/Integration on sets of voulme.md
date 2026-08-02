>Def (3.29):
>	Let S be a set of volume in R^k. and f from S to R bounded. We say that f is riemann integrable over S if there is a box A s.t. $S \subseteq A$, and s.t. the integral $$\int_A \widetilde{f}(x)dx$$ exists, for $$\widetilde{f}(x) = \begin{cases} f(x) & x \in S \\ 0 & x \not\in S \end{cases}$$
>	In that case we define $$\int_S f(x)dx := \int_A \widetilde{f}(x)dx$$

>Comment:
>	>(1): As in [[The volume of sets#^e20776]] we need to show that well-definedness (Does not depand on the choise of the box). But as it is a very similar proof, we skip it.
>	
>	>(2): Here we also need to show all the properties of the integral, but as we already did it for boxes, and the definition for general sets uses the one for boxes, we get it for free.
>	
>	>(3): It easy to see that $D(f) \subseteq D(\widetilde{f}) \subseteq D(f) \cup \partial S$.
>	>	The $D(f) \subseteq D(\widetilde{f})$ is because a point that is "bad" for f, is one where f takes too many values in every neighborhood of that point, and $\widetilde{f}$ will get those same values. And the $D(\widetilde{f}) \subseteq D(f) \cup \partial S$ is because if a point is in the interior of S, then it has a ball around it for which f and $\widetilde{f}$ agree, and if f was cont there, so will be $\widetilde{f}$. And out of S $\widetilde{f}$ is zero always so very continuous.
>	>And since we know that $\partial S$ is of measure zero, we get that $\widetilde{f}$ is integrable over A iff $D(f)$ is of measure zero.
>	>So we get that [[Integration over boxes#^f3e2f8|lebesgue-vitali]] holds for integration of general sets of volume.

Similar to [[Integration over boxes#^5ddb9a]]
>Propositoin (3.30):
>	If A, B are sets of volume in R^k, and f a bounded func, then f is integrable over A cup B iff it is integrable over A and it is integrable over B. In the it is, we have $$\int_{A \cup B} f = \int_A + \int_B$$
>Proof:
>	We take D a box that containes both A and B. And we have on that box $\overset{A \cup B}{f} = \overset{A}{f} + \overset{B}{f} - \overset{A \cap B}{f}$ (For $\overset{S}{f} = \begin{cases} f(x) & x \in S \\ 0 & x \not\in S \end{cases}$). And we notice that $\overset{A}{f} = \overset{A \cap B}{f} \cdot \chi_A$ and $\overset{B}{f} = \overset{A \cap B}{f} \cdot \chi_B$ and $\overset{A \cap B}{f} = \overset{A \cap B}{f} \cdot \chi_{A \cap B} = \overset{A \cap B}{f} \cdot \chi_{A} \cdot \chi_{B}$.
>	Also, $A \cap B \subseteq \partial A \cup \partial B$ (not used, and because both A and B have volume, we have that their boundry is of measure zero, so also $A \cap B$) so for $J = \partial A \cup \partial B$ (Which is compact as a union of compact [[]]) we get that $\overset{A \cap B}{f}$ is 0 out of $J$. And if $\overset{A \cap B}{f}$ is bounded over D then by [[The volume of sets#^ad52ba]] we get that $\overset{A \cap B}{f}$ is integrable over D with integral 0.
>	Now, if f is integral on both A and B, then clearly $\overset{A}{f}$,$\overset{B}{f}$ are (Its the same func...). Also f is bounded over $A \cap B$ because it is bounded in general. And we get that it is integrable over $A \cap B$ with integral 0. Thus from (mark the line above that says $\overset{A \cup B}{f} = \overset{A}{f} + \overset{B}{f} - \overset{A \cap B}{f}$) we get that $\overset{A \cup B}{f}$ is integrable over D as a sum of integrable, and the appropriate equality.
>	Conversely, if f is integrable over $A \cup B$, then $\overset{A \cup B}{f}$ is integrable over D. And because A,B have volume, also $\chi_A$ and $\chi_B$ are. So because ($\overset{A}{f} = \overset{A \cap B}{f} \cdot \chi_A$) we conclude that $\overset{A}{f}$ is integrable over D as a product of two integrable funcs, and by definition that means f is integrable over A. And the same goes for B.

>Prop (3.31):
>	If A is a set of volume, and $f:\overline{A}\to\mathbb{R}$ bounded, then f is integrable over A iff over $\overline{A}$ iff $A^\circ$ and in that case $$\int_{A} f = \int_{\overline{A}} f = \int_{A^\circ} f$$
>Proof:
>	[[The volume of sets#^8f9ec4|We know]] that $\overline{A}$ and $A^\circ$ are of volume. We need to show that the set of discon points are of zero measure together. Indeed $$D(f \big\vert_{A^\circ}) \subseteq D(f\big\vert_A) \subseteq D(f)$$ And also $\overline{A} \setminus A^\circ = \partial A$ is a set of measure zero (because we are told that A is of volume). So even if every point in $\partial A$ is a discontinouity point of f, if $D(f\big\vert_{A^\circ})$ was of zero measure, then also $D(f)$ would be because $D(f) \subseteq D(f\big\vert_{A^\circ}) \cup \partial A$ which is a union of sets of measure zero which is also of measure zero.
>	Lastly we need to show the equality. We will notice that $A^\circ \subseteq A \subseteq \overline{A}$ and that $A \setminus A^\circ \subseteq \partial A \wedge \overline{A} \setminus A \subseteq \partial A$. And use the lemma

>Lemma:
>	Let C,D sets of volume, $D \subseteq C$ s.t. $C \setminus D$ is contained in a compact set of measure zero. $f:C\to\mathbb{R}^k$ integrable on $C,D$ then $\int_C f = \int_D f$
>Proof:
>	We can notice that for all x in C $f(x) = f\big\vert_{C \cap D} (x) + f\big\vert_{C \setminus D} (x)$. And since $f\big\vert_{C \setminus D}$ is 0 out of J, we will get by a previos lemma () that it is integrable with integral 0. And since $D \subseteq C$ we get that $C \cap D = D$ and so $f\big\vert_{C \cap D} = f\big\vert_D$ and we get that $\int_C f = \int_C f\big\vert_{C \cap D} + \int_C f\big\vert_{C \setminus D} = \int_C f\big\vert_{C \cap D}$ (I don't know how to cont.)