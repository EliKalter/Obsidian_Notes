>Def (Closed box) (תיבה סגורה):
>	A closed  bos in $\mathbb{R}^k$ is a set $A \subset \mathbb{R}^k$ of the form $A = \bigtimes_{i=1}^{k} [a_i,b_i]$ for $a_i < b_i$.

^34f352

>Def (The volume of a closed box):
>	Let $A = \bigtimes_{i=1}^{k} [a_i,b_i]$ be a box in $\mathbb{R}^k$. Then we define the volume of $A$ to be $V(A) := \prod\limits_{i = 1}^{k} (b_i - a_i)$.

^1ae6d6

>Def (A partition of a box):
>	Let $A = \bigtimes_{i=1}^{k} [a_i,b_i]$ be a box in $\mathbb{R}^k$. And assume for every $j \in [k]$ there is a partition (Partition in the infi 2 def [[]]) of the segment $[a_j, b_j]$ $P_j = \left\{ t_j^i \right\}_{i=0}^{m_j}$ s.t. $t_j^0 = a_j$, $t_j^{m_j} = b_j$ and $t_j^{i-1} < t_j^i$ for all $i \in [m_j]$. (The "size" of the partition $P_j$ is $m_j$)
>	We will define "a partition of $A$ induced by the $P_j$-'s" to be $P:=\bigtimes\limits_{i=1}^{k} P_i$.

>Def (The sub-boxes of a partition of a box):
>	Let $A = \bigtimes_{i=1}^{k} [a_i,b_i]$ be a box in $\mathbb{R}^k$, And $P=\bigtimes\limits_{i=1}^{k} P_i$ a partition of $A$ induced by the partitions $P_j = \left\{ t_j^i \right\}_{i=0}^{m_j}$. Then for every $I = \left( i_1, \dots i_k \right) \in \bigtimes\limits_{i=1}^{k} [m_i]$ we will define "The $I$-'th sub-box in $P$" to be $C_I:= \bigtimes\limits_{j=1}^{k} [t_j^{i_j-1}, t_j^{i_j}]$.

Note: In such partition, there are exactly $\prod\limits_{j=1}^{k} m_j$ such boxes.

>Lemma:
>	The volume of a box is equal to the sum of the volumes of the sub-boxes. j. In particu j. In particu
>	Let $A = \bigtimes_{i=1}^{k} [a_i,b_i]$ be a box in $\mathbb{R}^k$, And $P=\bigtimes\limits_{i=1}^{k} P_i$ a partition of $A$ induced by the partitions $P_j = \left\{ t_j^i \right\}_{i=0}^{m_j}$.  Then $$V(A) = \sum\limits_{I \in \bigtimes\limits_{i=1}^{k} [m_i]} V(C_I)$$
>Proof:
>	It is highly intuitive and I'll skip the proof for now. The proof can be in induction on the dimension. Did in the ipad.

>Lemma (3.1):
>	Let $P$ be a partition of box $A$. And let $B \subseteq A$ be a box s.t. the vertices of $B$ are in $P$ (Meaning $B = \bigtimes\limits_{i=1}^{k} [c_i, d_i]$ and $\left\{ c_i, d_i\right\}_{i \in [k]} \subseteq P$). Then for every $x \in B$ there exist $C$ a sub-box  of $P$ (Induced by $P$) s.t. $x \in C \subseteq B$.
>Proof:
>	By look at it...

^fb2b80

>Def (A refinement of a partition):
>	Let $P, P'$ be partitions of a box $A$.
>	The  $P'$ is a refinement of $P$ when $P \subseteq P'$.

^59898e

>Result from [[#^fb2b80|the lemma]]:
>	If $P'$ is [[#^59898e|a refinement of]] $P$, then for every box $C^{P'}$ induced by $P'$ there is a box $C^P$ incduced by $P$ s.t. $C^{P'} \subseteq C^P$.

^a7dcab

(I understand why the [[#^a7dcab|result from the lemma]] is true, but not why it results from the lemma.)

>Def (3.2) (Lower and upper sums):
>	Let $A$ be a box in $\mathbb{R}^k$, $P$ a partition of $A$, And assume $\left\{A_j\right\}_{j \in [r]}$ are the sub-boxes of $P$.
>	And let $f:A \to \mathbb{R}$ be a bounded function.
>	We will denote $m_i:= \underset{x \in A_i}{\text{inf}} f(x)$ And $M_i:= \underset{x \in A_i}{\text{sup}} f(x)$. And define the "lower sum of $f$ with respect to $P$" to be $$L\left(f,P\right):=\sum\limits_{i=1}^{r} m_i\cdot V\left(A_i\right)$$
>	And similarly the "upper sum of $f$ with respect to $P$" $$U\left(f,P\right):=\sum\limits_{i=1}^{r} M_i\cdot V\left(A_i\right)$$

^be80ac

>Proposition (3.3):
>	Let $P, P'$ be partitions of a box $A$ s.t. $P'$ is a refinement of $P$. Then $$L\left(f, P\right) \leq L\left(f, P'\right) \leq U\left(f, P'\right) \leq U\left(f, P\right)$$
>Proof:
>	Intuitive. Just like in [[]](infi 2. need to complete).

>Corollary (3.4):
>	Let $A$ be a box in $\mathbb{R}^k$. And $P,Q$ two partitions of $A$. Then $L\left(f, P\right) \leq U\left(f, Q\right)$.
>Proof:
>	[[#^dc0309|By the lemma]], there is a partition $R$ such that $R$ is a refinement of both $P$ and $Q$ and now $$L\left(f, P\right) \leq L\left(f, R\right) \leq U\left(f, R\right) \leq U\left(f, Q\right)$$

>Lemma:
	Let $A$ be a box in $\mathbb{R}^k$, and $S \subset A$ a finite set. Then there is $P$ a partition of $A$ s.t. $S \subseteq P$.

^a2e56b

>Proof:
>	Let $r = \left\vert S \right\vert$ and $S = \left\{ \left( {x_i}^1, \dots {x_i}^k \right) \right\}_{i=1}^r$. Then for every $j \in [k]$ define $X_j:= \left\{ x_i^j \right\}_{i=1}^r$ (The $j$-'th coordinate from all the points in $S$). And $P_j:=X_j \cup \left\{a_j, b_j\right\}$ then $P_j$ is a partition of $[a_j, b_j]$ and $P:=\bigtimes\limits_{j=1}^{k} P_j$ is a partition of $A$ that obviously contains all points from $S$.
en for ever
>Lemma (A common refinement):
>	Let $A$ be a box in $\mathbb{R}^k$. And $P,Q$ two partitions of $A$. There there is $R$ a partition of $A$ s.t. $R$ is a refinement of both $P$ and $Q$.
>Proof:
>	Denote $S = P \cup Q$. Then by [[#^a2e56b|the last lemma]] we will get $R$ a partition of $A$ s.t. $P \cup Q \subseteq R$ and since $P,Q \subseteq P \cup Q$ we conclude $P,Q \subseteq R$, and [[#^59898e|by definition]] $R$ is a refinement of bot $P$ and $Q$.

^dc0309

>Def (3.5) (Lower and upper integrals):
>	Let $A$ and $f$ [[#^be80ac|as above]]. Then we define the "lower integral of $f$ over the box $A$" by $$\underline{\int}_A f(x)dx := \text{sup} \left\{ L\left(f,P\right) \mid P \text{ partition of } A \right\}$$
>	And similarly the "upper integral of $f$ over the box $A$" is $$\overline{\int}_A f(x)dx := \text{inf} \left\{ U\left(f,P\right) \mid P \text{ partition of } A \right\}$$

^0449b3

>Def (The trivial partition of a box):
>	Let $A = \bigtimes_{i=1}^{k} [a_i,b_i]$ be a box in $\mathbb{R}^k$, then $K:=\bigtimes\limits_{i=1}^{k} \left\{a_i, b_i\right\}$ is called "the trivial partition of $A$".

^65afc8

Note: Those are well defined becaue $L\left(f,P\right) \leq U\left(f, K\right)$ for all $P$ a partition of $A$ ($K$ [[#^65afc8|the trivial partition]]). And similarly for $U$.

>Def (3.6) (Riemann integrability):
>	[[#^0449b3|Such function]] $f$ is called "riemann integrable on $A$" when $$\underline{\int}_A f(x)dx = \overline{\int}_A f(x)dx$$

>	In that case we will call that value "The integral of $f$ over $A$". And denote it $\int_A f(x)dx$ Or $\int_A f(x_1, \dots, x_k)dx_1dx_2\cdots dx_k$.

>Corollary (3.7):
>	Let $A$ be a box in $\mathbb{R}^k$, $f,g:A\to\mathbb{R}$ riemann integrable over $A$, and $c \in \mathbb{R}$. Then
>	>(1): $f + g$ is integrable, and
>	>	$\int_A (f+g)(x)dx = \int_A f(x)dx + \int_A g(x)dx$
>	
>	>(2): $cf$ is integrable and
>	>	$\int_A cf(x)dx = c\int_A f(x)dx$

>	>(3): The constant func $1$ is integrable, and
>	>	$\int_A 1(x)dx = V\left(A\right)$

^b86a28

>	>(4): If $f \geq 0$ then $\int_A f(x)dx \geq 0$

>Corollary (3.8):
>	If $f \leq g$ then $\int_A f(x)dx \leq \int_A g(x)dx$
>Proof:
>	define $h = g -f$. then $h \geq 0$. then int g - int f = int (g-f) = int h >= 0. 

>Corollay (3.9):
>	If abs(f) <= M. Then Abs(int f) <= MV(A)
>Proof:
>	We will get that from the fact that MV(A) is the upper sum of the trivial partition and from M = M $\cdot$ 1. Maybe we need to show first that Abs(int f) <= int(abs(f)). Or maybe just show that int(f) <= MV and int(f) >= -MV.

>Theorem (3.10):
>	Let $A, B$...
>Proof:
>	(Starting from P_A a partition of And P_B a partition of B we have P the common refinement)
>	For one directioin we have L(f, P_A) + L(f, P_B) <= L(f, P cut A) + L(f, P cut B) = L(f, P) <= U(f, P) = U(P cut A) + U(P cut B) <= U(P_A) + U(P_B) And the edges are as small as we want so we have a sandwich in the middle.
>	And for the other side, we can find P partition of A cup B with small omega, and the omega on A is smaller than the omega on A cup B (Because the omega on B is non negtive). And hence we can find partitions of A with small omega as we want so f is integral on A.
>	For finite union, we notice that we can always build it from smaller boxes. meaning, the union is made up of two unions, both are boxes. and by induction.

We will now consider under what conditions a function is integrable.

>Proposition (3.11):
>	A function that is continuous on a box, is also integrable.
>Proof:
>	A box is compact. Thus continuous means uniformly continuous. So we can find a diameter such that every two points are close enough. And since the norms are equivalent, we can have it in the inf norm. Meaning 2 point in the same box are close enough. Now we create a partition of that radious (or smaller). and thus on each sub-box the dist from max to min will be small enough. and the elements in the entire sum can have the same common epsilon, so epsilon comes out, and the sum over the volumes of the sub-boxes is the volume of A, but we took delta so that cancels.

>Def (3.12) (A set of measure zero):
>	Can be covered with a countable collection of boxes with arbitrary small volume together

>Lemma (3.13):
>	A countable union of sets of measure zero is of measure zero.
>Proof:
>	Let $\varepsilon_n = \frac{\varepsilon}{n^2}$ Then the i'th set can be covered in less than eps_n vol. and the vol of everything together will be eps $\cdot$ "inf sum of 1 over n^2" which is finite. so we could have chosen eps' to be the first one times 1 over that. and everything would work.

^aa5125

>Example:
>	>(1): A singleton is of measure zero. And by [[#^aa5125|the lemma]] we will get that also any countable set, because every countable set can we written as a contable union on its singletons.
>	
>	>(2): A set with non empty interior is not of measure zero.
>	>	Because it has a inner point, wich has a ball around it in the inf norm, meaning a box. and every covering of the entire set would cover that box and have volume bigger than that box. so can't get arbitrarily small.

>Lemma (3.14):
>	If A is of zero measure, then it can be covered with delta small boxes, and have it such that every point of every box is no farther from A than delta.
>Proof:
>	Take the Bi. cut it into small boxes that are smaller than delta. Ignore the ones that do not intect A. Now the volume is right, the edge length is right, and since the tiny boxes are in the balls of radious delta (over 2? the point is that the edge length should be less than delta and the dist in them is also no more than delta) and each one contains a point from A and the other points in it are no frther than delta from it.

>Exercise (3.1):
>	Show that the boundry of a box is of measure zero.

^2e6e3c

>Sol:
>	There are $k^2$ sides.
>	A side looks like $\bigtimes\limits_{j = 1}^{i - 1} [a_j,b_j] \times \underset{\text{Or } b_i}{\left\{a_i\right\}} \times \bigtimes\limits_{j = i + 1}^{k} [a_j,b_j]$.
>	For $\delta > 0$ $V([a_1, a_1 + \delta]\times \bigtimes\limits_{j = 2}^{k} [a_j,b_j]) = \delta\cdot\prod\limits_{j=2}^{k} (b_j - a_j)$. So we can choose $\delta$ small enough and cover the side $\left\{a_1\right\}\times \bigtimes\limits_{j = 2}^{k} [a_j,b_j]$
>(We also need to show that $\partial A = \bigcup \text{"The sides of A"}$)

>Propositon (3.15):
>	>(1): If B_1...B_n are boxes, then there are C_1...C_m such that the union of the C_j's is the same is the union on the B_i's, and the C_i's  interior are disjoint. In addition, the same is true for a countable collection of boxes.
>	
>	>(2): Any box B can be partitioned into boxes that have aspect ratio of less than or equal to 2.
>	
>	>(3): If B is a box in R^k with aspect ratio at most 2, then there is a cube C such that B $\subseteq$ C, and V(C) <= 2^{k-1}V(B)

>Proof (as exercise):
>	>(1):
>	>	We will show the helper lemma That if we have D_i's boxes such that their interior is disjoint, and B a box, then there are C_j's such that their inter is disjoint and that the union on of the C_j's is the same as the D_i's with B.
>	>	It is true because in the set of points that define all of them together, every 
>	
>	>Or we can instead go directly, every finite set of boxes has a finite set of point that define them. look at the partition created by all of them such as in [[#^a2e56b|here]]. Every sub-box here is either contained in some box from the original ones, or its interior is disjoind from all of them. we take the ones we need.
>	
>	>For the countable case: again, in every coordinate, there is a countable subset of R of points that participate. we take the closest ones from both sides in each coordinate, and check if we need to add this to the collection or not. Why do we finish with countable amount? The set of all points did not have to be bounded... Interesting.
>	
>	>(2): If we take $n \geq log_2(\frac{b}{2\cdot [a]^b})$ (Where $[a]^b$ is the remainder of $\frac{a}{b}$ in $a = nb + r$ i.e. $[a]^b = r$.) then $2^n \geq \frac{b}{2\cdot [a]^b}$ and so $\frac{\frac{b}{2^n}}{[a]^b} \leq 2$. And we can have the witdth by puting $2^n$ such bricks (of size $\frac{b}{2^n}$). And the a wall by puting such b lengths until we can't anymore, and then the sliver that is left can be covered with boxes of size $\frac{b}{2^n} \times [a]^b$ and we chose n to have this be of the right ratio.
>	>We did assume that a can't be divided into b, other wise it is trivial becaseu sqaure boxes with side b will do the job.
>	>This solves the 2 D case. For the more general case, we need to think more.
>	>We might need to go about it by deviding the box into 2 sub-boxes along the longest edge, and notice that the one that was the smallest never gets devided, and that eventually all the resulted length are small enough, because you can only cut in half an edge so many times before it is small enough.
>	
>	>(3): We will increase the length of every edge of B to be as the longest edge. So we got a cube. And the size can be easily calculated to match the requirement.

>Corollary (3.16):
>	If A is a set of measure zero, than A can be covered with cubes, which size is still less than epsilon.
>Proof:
>	df

>Theorem (3.17) (Lebesgue-Vitali):
>	f is integrable over A iff the set of discontinuity (of f in A or the func was on A to begin with) is of measure zero.
>The proof will come later.

^f3e2f8

>Lemma: A continuous func is bounded over bounded close sets.
>Proof:
>	Remember we are in a norm space. So the bounded close set is compact. So this is direct from the max val theorem.
^d1fdf8

>Corollary (3.18):
>	f_1,...f_m are int over A. And phi is continuous from R^m to R then phi of (f_1, ... , f_m) is also integral
>Proof:
>	Since phi is continuous, it is bounded over bounded close sets ([[#^d1fdf8|See the lemma]]). And since each of the f_i's is integral, it is bounded, so the entire image of all of the together is in some ball around the origin, of radious M (in the inf norm). Over that closed box, phi is bounded, so it is also bounded over the image of the f_i's. So phi(f_1...f_m) is bounded.
>	And the discon points of phi(f_1,...f_m) is contained in the union of the dicon sets of the f_i's. So it is also of measure zero (Because in any point where all are cont, the composition of a cont on a cont is cont). So from [[#^f3e2f8|Lebesgue-Vitali]] we obtain that it is int.

>Theorem (3.19) (The topological def of compactness):
>	A is compact (sequentially) iff any cover has a finite sub cover
>Proof: In topology course.

>Proposition (3.20):
>	A compact set of measure zero can be covered with a finite num of open boxes (and have their volume smaller than epsilon).
>Proof:
>	Take a cover with boxes that is garenteed from the measure zero that matches half epsilon. For each box, take a box that is slightly larger, such that the new volume will still be less than (or equal to) twice as the original box, and such that the interior of the new box will contain the old box. Now the vol of the new boxes is small enough, and obviously covers the set. Now from the last theorem, it has a finite sub cover, and that is a cover with less vol than the original one, so for sure less than epsilon, and it is finite of open boxes.

^063141
