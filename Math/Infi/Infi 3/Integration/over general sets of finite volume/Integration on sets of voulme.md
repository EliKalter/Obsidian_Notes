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

>Prop (3.32):
>	Let S subset A subset R^k of volume s.t. S closed and A open. then there exists for all natural i $S_i \subseteq S \subseteq S'_i \subseteq A$ s.t. both S_i and S'_i are a union of finitely many boxes with disjoint anterior, and for every func $f:A\to\mathbb{R}$ integrable $$\int_S f = \underset{i\to\infty}{lim} \int_{S_i} f = \underset{i\to\infty}{lim} \int_{S'_i} f$$
>	>As a direct result we get that $$V(S) = \underset{i\to\infty}{lim} V(S_i) = \underset{i\to\infty}{lim} V(S'_i)$$
>Proof:
>	Maybe later Flag for avi

>Theorem (3.33) (fubini):
>	>(1 The proposition): Let $A \subset \mathbb{R}^k$ and $B \subset \mathbb{R}^m$ be closed boxes. $f:A\times B\to \mathbb{R}$ integrable. Then the integrals $$\int_B \left( \underline{\int}_A f(x,y) dx \right) dy \quad \text{and} \quad \int_B \left( \overline{\int}_A f(x,y) dx \right) dy$$ exist, and we have the equality $$\int_{A\times B} f(x,y) dxdy = \int_B \left( \underline{\int}_A f(x,y) dx \right) = \int_B \left( \overline{\int}_A f(x,y) dx \right) dy$$
>	
>	>(2 Comments):
>	>	>(a): Obviously the rolls of x and y can be interchanged
>	>	
>	>	>(b): The simbol $dxdy$ does not have any meaning except for representing that we integrate over both x and y. Most importantly, in this context $dydx$ and $dxdy$ mean the exact same thing. Sometimes when it can get confusing we might use a different notation and say it clearly (such as $dV$)
>	>	
>	
>	>(3 Proof):
>	>	In the records and with more elaboration in the ipad. Need to complete. It is not a small one to say the least. Can be shown only for one of them ($\int_B \left( \underline{\int}_A f(x,y) dx \right) dy$ for example i.e. the H func), the other one is just the same.
>	>	The core of it all is to understand why $L(f,P) \leq L(H, P_B)$, everything else is fairly simple.
>	>	We split P into P_A and P_B. We notice that iterating over P can be broken into a double sum.
>	>	We use the fact that $inf f(x) + inf g(x) \leq inf (f(x)+g(x))$ with the $\lambda_i(y) = V(A_i)\cdot \underset{x \in A_i}{f(x,y)}$ and get the main ineqaulity. The rest kinda fals into place.

^5d070f

>Corollary (3.34):
>	>Prop: If in the last theorem, if for every $y \in B$ $G(y) = H(y)$ meaning that $f_y$ is integrable over B, i.e. $\int_A f_y(x) dx = \int_A f(x,y) dx$ exists, then $\int_{A\times B} f(x,y)dxdy = \int_B\left( \int_A f(x,y)dx \right)dy$.
>	
>	>Note: The same goes for the other way arround, so if for every $x \in A$ the integral $\int_B f_x(y) dy$ exists, then $\int_{A\times B} f(x,y)dxdy = \int_A\left( \int_B f(x,y)dy \right)dx$
>	
>	>Result: In case for all $x,y \in A \times B$ we have ...

>Note:
>	[[#^5d070f|In fubinis theorem]], there is no assumption that for all $y \in B$ $\overline{\int}_A f(x,y) dx = \underline{\int}_A f(x,y) dx$.

>Example (Of  the use of fubini):
>	Calculating the area of a disk
>	Flag for avi

>Example (Of  the use of fubini):
>	Calculating the area of a body of revolution

>Corollary:
>	Kinda intuitive, only for $k = 2,3$. We go about proving the 3 case using the 2 case...? And what is the proof for the 2 case? We need to convert everything to the language of fubini, so we box it all (we can as g, h are cont over a compact set and thus get max and min). And on that box, f_x(y) is integrable, becaues it is cont in where it defined, so we get that we can split the dims by fubini, and the int over the inner dim is the same as the integral on the D area ([g0(x),g1(x)]) (We need to explain the change from $\int_{[a,b]} f(x)dx = \int_a^b f(x) dx$, and why we can change to the smaller box in one dim, and ignore the bigger one.)

>Now we maybe have the tools to calc the volume of the unit ball
>Flag for avi

The folowing proposition will be very similar to how we defined the area of a set that is traped between the axes and the graph of a cont non neg func
It will now make that old definition make much more sense.

>Prop (3.36):
>	Let S in R^k be a set of volume, and $f:\overline{S}\to [0,\infty) \subset \mathbb{R}$.
>	Denote $A_{f,S} = \left\{ (x,y) \in \mathbb{R}^{k+1 }\mid x \in S \wedge y \in [0,f(x)] \right\}$
>	Then $V(A_{f,S}) = \int_S f(x)dx$
>Proof:
>	First, the set $A_{f,S}$ has volume [[The volume of sets#^724338|from here]].
>	Let $B$ be a box that contains $S$.
>	And let $M := \underset{x \in S}{max} \: f(x)$ (It exists because f is cont over a closed bounded set in a normed space which is compact)
>	So we have $B \times [0,M]$ covers $A_{f,S}$
>	Now $$V(A_{f,S}) \overset{def}{=} \int_{B \times [0,M]} \chi_{A_{f,S}}(x,y) dxdy \overset{\text{fubini (*1)}}{=} $$
>	$$= \int_B \left( \int_{[0,M]} \chi_{A_{f,S}}(x,y)dy \right) dx \overset{def}{=} \int_B \left( \int_0^M \chi_{A_{f,S}}(x,y)dy \right) dx \overset{(*2)}{=} $$
>	$$= \int_B \widetilde{f}(x) dx \overset{def}{=} \int_S f(x) dx$$
>	>(*1*): Because $S$ has volume, the indicator func is integrable. And it is clearly then also integrable when we fix some of the coordinates (Because of lebesgue vitali).
>	
>	>(*2*): We want to show that for fixed $x \in B$ $$\int_0^M \chi_{A_{f,S}} (x,y) dy = \widetilde{f} (x)$$
>	>Where $\widetilde{f}$ is the extension func of $f$ to $B$ that is defined to be 0 where f is not defined.
>	>We notice that $\chi_{A_{f,S}} (x,y) = \chi_{S}(x) \cdot \chi_{[0,f(x)]} (y)$. Now for $x_0 \not\in S$ we get $\int_0^M \chi_{A_{f,S}} (x_0,y) dy = 0 = \widetilde{f} (x_0)$. And for $x_0 \in S$ we get $$\int_0^M \chi_{A_{f,S}} (x,y) dy = \int_0^M \chi_{[0,f(x_0)]} (y) dy =$$
>	>$$= \int_0^{f(x_0)} dy = f(x_0)  = \widetilde{f}(x_0)$$

