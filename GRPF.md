Define a category $\mathrm{FGrp}$ of strongly central filtrations the full subcategory of $\mathrm{Fil}(\mathrm{Grp})$ for which
$$
G_0 \hookleftarrow G_1 \hookleftarrow G_2 \hookleftarrow \cdots
$$
viewing each $G_i$ as an element of the poset category $\mathrm{Sub}(G_0)$ 
$$[G_i,\,G_j] \leq G_{i+j}$$
where $[-,-] : \mathrm{Sub} \times \mathrm{Sub} \to \mathrm{Sub}$ is the commutator bifunctor. Note that writing $G_\bullet : \mathbb{N} \to \mathrm{Sub}(G_0)$, we're really asking for a natural transform
$$
[-,-] \circ (G_\bullet \times G_\bullet) \longrightarrow G_\bullet \circ +
$$
Two results. The forgetful functor $\mathrm{FGrp} \to \mathrm{Fil}(\mathrm{Grp})$ creates all pullbacks, and cokernels (though not all pushouts).

***lemma.*** The forgetful functor creates pullbacks.
***proof.*** We must show that the pullback of two strongly central filtrations in $\mathrm{Fil}(\mathrm{Grp})$ is strong central: $[G_i \cap H_i, G_j \cap H_j] \leq G_{i+j} \cap H_{i+j}$. Observe:
$$
\begin{align*}
[G_i \cap H_i, G_j \cap H_j] &\leq [G_i, G_j \cap H_j] \cap [H_i, G_j \cap H_j]\\
&\leq [G_i, G_j] \cap [G_i, H_j] \cap [H_i, G_j] \cap [H_i, H_j]\\
&\leq [G_i, G_j] \cap [H_i, H_j]\\
&\leq G_{i+j} \cap H_{i+j}
\end{align*}
$$
***lemma.*** The forgetful functor creates cokernels.
***proof.*** todo

Define a functor (an extensions of the usual group algebra $\mathrm{Grp} \to \mathrm{Vec}_k^\mathsf{cocHopf}$) $k[-] : \mathrm{FGrp} \to \mathrm{Fil}_k^\mathsf{cocHopf}$ as follows. We write $\mathrm{Fil}_k := \mathrm{Fil}(\mathrm{Vec}_k)$ and $\mathscr{C}^\mathsf{cocHopf}$ for the category of cocommutative hopf objects in $\mathscr{C}$.
$$ 
k[G_\bullet]_n = \Big\langle (g_1 - 1)(g_2 - 1)\cdots (g_k - 1) \,\Big\vert\, g_i\in G_{r_i}, r_1+r_2 + \cdots + r_k \geq n \Big\rangle_k
$$
***lemma.*** $k[-]$ is a left adjoint.
***proof.*** Define $\mathcal{G} : \mathrm{Fil}_k^\mathsf{cocHopf} \to \mathrm{FGrp}$ by
$$
(\mathcal{G}H_\bullet)_n = \Big\{ g \in \mathcal{G}H_0 \,\Big\vert\,g-1\in H_n \Big\}
$$
first let us show that $(\mathcal{G}H)_n \leq (\mathcal{G}H)_{n-1}$. It is clearly it is a subset containing the identity, so it only remains to show that is closed under multiplication and inverses. Suppose, $g,h \in (\mathcal{G}H)_n$. Then, 
$$
gh-1 = gh \pm h - 1 = (g-1)h+(h-1)
$$
because $(g-1)h \in \mathrm{im}(\times : H_n \otimes H_0 \to H_{n+0})$ we have $gh - 1 \in H_n$. Moreover,
$$
g^{-1}-1 = -(g-1)g^{-1} \in H_n
$$
It remains to show $\mathcal{G}H$ is strongly central. (and that is an adjoint to $k[-]$).

Now, define another category, $\mathrm{FGrpLie} = [\mathrm{Grp}, \mathrm{Fil}_\mathbb{Z}^\mathsf{Lie}]$, whose objects are triples $(G,\,L_\bullet,\,\rho)$ where $L_\bullet$ is a filtered lie object (i.e. an object of $\mathrm{Fil}_\mathbb{Z}^\mathsf{Lie}$) equipped with a group action $\rho : G \to \mathrm{Aut}(L_\bullet)$.

***lemma.*** Define a map $\mathrm{g} : \mathrm{FGrp} \to \mathrm{FGrpLie}$ as follows.
$$
\mathrm{g}G_\bullet = \left(G_0/G_1 ,\; \bigoplus_{n\geq 1} G_n/G_{n+1} \right)
$$
this map is well defined, and preserves strict exact sequences.

***lemma.*** Define a map $\mathrm{E} : \mathrm{FGrpLie} \to \mathrm{FGrp}$ as follows.
$$
\mathrm{E}(G,L_\bullet) = \exp(\widehat{\mathbb{Q} \otimes L_\bullet}) \rtimes G
$$
this map is well defined, and preserves strict exact sequences.

***theorem.*** (someone) for characteristic zero $k$, $\hat k[\mathrm{E}\mathrm{g}G] \cong \hat{\mathrm{gr}} k[G]$

***lemma.*** If $k$ is a characteristic zero field then $k[-]$ preserves pullbacks.
***proof.*** todo idk scary might not need