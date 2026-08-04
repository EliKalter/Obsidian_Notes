
>Proposition:
>	Let $A \subset \mathbb{R}^k$ be [[Integration over boxes#^34f352|a box]]. $f:A\to\mathbb{R}$ bounded.
>	Denote $D(f)$ the set of discontinuity points of $f$. $D(f) := \left\{ a \in A \mid f \text{ is not continuous at }a \right\}$
>	Then $f$ is [[Integration over boxes#^8930a7|riemann integrable]] over $A$ (a.k.a. $\int_A f(x)dx$ exists) $\iff$ $D(f)$ is [[Integration over boxes#^a327cd|a set of measure zero]].

^b93f08

In order to prove it, we will need to do some work first to better understand $D(f)$.

>Def (The diameter of a set in a metric space):
>	Let $(\mathbb{X}, d)$ be a metric space, and $C \subseteq \mathbb{X}$. We denote $$diam(C) := \underset{x_1,x_2 \in \mathbb{X}}{sup} d(x_1,x_2)$$ and call it "The diameter of $C$"
>	
>	>Note: $diam:2^{\mathbb{X}}\to \mathbb{R}_+ \cup \left\{\infty\right\}$

>Lemma (The monotonicity of $diam$):
>	Let $(\mathbb{X}, d)$ be a metric space, $C_1 \subseteq C_2 \subseteq \mathbb{X}$.
>	Then $diam(C_1) \leq dima(C_2)$.
>Proof:
>	Immediate from the [[]] same property for sup, and by def.

^3e6782

>Def (3.35):
>	Let $(\mathbb{X}, d)$ and $(\mathbb{Y}, \rho)$ be metric spaces. And $x \in \mathbb{X}$.
>	>(1): We define $$\omega_f(x) := \underset{\delta\to 0^+}{\text{lim}} \text{ diam} \left( f\left( B_\delta \left(x\right) \right) \right)$$
>	
>	>Note: This is a limit of a function with images in $\mathbb{R} \cup {\infty}$. But the limit always exist. Because if $\delta_1 \leq \delta_2$ then $B_{\delta_1} (x) \subseteq B_{\delta_2}$ and thus $f\left( B_{\delta_1} (x) \right) \subseteq f\left( B_{\delta_2} (x) \right)$ so [[#^3e6782|from the lemma]] $diam(f\left( B_{\delta_1} (x) \right)) \leq diam(f\left( B_{\delta_2} (x) \right))$. Thus, if there is some $\delta_0 > 0$ such that $diam(f(B_{\delta_0}(x))) < \infty$, then the function $\delta \mapsto diam(f(B_\delta(x))):(0,\delta_0)\to\mathbb{R}$  is monotonic (decreasing) and non negative (bounded from below by 0),  so it has a limit. And if $\forall \delta > 0$ $diam(f(B_{\delta}(x))) = \infty$, we get that $\underset{\delta\to 0^+}{\text{lim}} \text{ diam} \left( f\left( B_\delta \left(x\right) \right) \right) = \underset{\delta\to 0^+}{\text{lim}} \infty = \infty$.
>	
>	>Note: $\omega_f:\mathbb{X}\to\mathbb{R}_+ \cup \left\{\infty\right\}$

^763fd9

>	>(2): Also define for $\varepsilon > 0$  $$F_\epsilon := \left\{ x \in \mathbb{X} \mid \omega_f (x) \geq \varepsilon \right\}$$

>Remark:
>	In the setup of [[#^763fd9|the definition]] of $\omega_f$, $f$ is continuous at $x$ $\iff$ $\omega_f(x) = 0$
>Proof:
>	Skipping. From the definitions

>Result:
>	In the same setup, it is obvious that $f$ is continuous $\iff$ $\forall\varepsilon > 0: F_\varepsilon = \emptyset$.

>Conclusion:
>	$D(f) = \bigcup\limits_{\varepsilon > 0} F_\varepsilon = \bigcup\limits_{n \in \mathbb{N}} F_{\frac{1}{n}}$.
>Proof:
>	If $x \in D(f)$, then $\omega_f(x) > 0$ then $x \in F_{\frac{\omega_f(x)}{2}}$. and because we can find $n \in \mathbb{N}$ s.t. $\frac{1}{n}  \leq \frac{\omega_f(x)}{2}$ we will get that $x \in F_{1/n}$ (Note that the func $\varepsilon \mapsto F_\varepsilon$ is monotonic, i.e. $\varepsilon_1 \leq \varepsilon_2 \implies F_{\varepsilon_1} \supseteq F_{\varepsilon_2}$)
>	And the other way is also trivial. Skipping

^88bf44

>Lemma (3.54):
>	In the [[#^763fd9|same context]] let $\varepsilon > 0$, Then $F_\varepsilon \subseteq \mathbb{X}$ ise a closed st.
>Proof:
>	We need to take a series in $F_\varepsilon$ that converges in $\mathbb{X}$ and show taht the  limit is in $F_\varepsilon$.
>	Let $\left(x_n\right)_{n = 1}^\infty \in F_\varepsilon^\mathbb{N}$ and $x \in \mathbb{X}$ s.t. $x_n \overset{d}{\rightarrow} x$.
>	Denote $d_n = d(x_n, x)$.
>	Since $x_n \in F_\varepsilon$, we have that $diam(f(B_{d_n}(x_n))) \geq \varepsilon$.
>	And since $B_{d_n}(x_n) \subseteq B_{2d_n}(x)$ (Because $d(y,x_n) < d_n \implies d(y,x) \leq d(y,x_n) + d(x_n,x) = d(y,x_n) + d_n < d_n + d_n = 2d_n \implies y \in B_{2d_n}(x)$), we get that $diam(f(B_{2d_n}(x))) \geq diam(f(B_{d_n}(x_n))) \geq \varepsilon$.
>	Now, since $d_n \overset{n\to\infty}{\longrightarrow} 0$ we get that $2d_n \overset{n\to\infty}{\longrightarrow} 0$, So by "היינה" we get that $\omega_f(x) \geq \varepsilon$, meaning $x \in F_\varepsilon$ $\blacksquare$

>Theorem (3.55) (Equiv formulation of the lebesgue-vitali theorem):
>	>In the same setting as [[Lebesgue-Vitali#^b93f08|the original formulation]], $f$ is integrable $\iff$ $\forall n \in \mathbb{N}: F_{\frac{1}{n}} \text{ is of measure zero}$
>	
>	>Note: The equivalance is because of ([[#^88bf44]], [[Integration over boxes#^aa5125]]).
>	
>	>[[#^9aa31c|The proof]]

^96b479


>Proof of [[#^96b479|the equiv formulation of Lebesgue-Vitali]]:
>Skippint typing for now. Takes time...K
>	>**$\text{measure zero} \implies \text{integrability}$**:
>	>	dfd
>	
>	>**$\text{integrability} \implies \text{measure zero}$**:
>	>	dfdf
^9aa31c
