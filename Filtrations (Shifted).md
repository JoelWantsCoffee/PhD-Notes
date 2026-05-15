First, define $S : \mathsf{Filt}(\A) \to \mathsf{Filt}(\A)$ by $$S(A_0 \hookleftarrow A_1 \hookleftarrow \cdots) \;=\; (A_0 \xlongequal{\,\,} A_0 \hookleftarrow A_1 \hookleftarrow \cdots)$$that is, repeat the first item of the sequence with the identity. A few fun facts.
1. $S$ preserves kernels and cokernels
2. $S$ is additive
3. there's a natural transformation $\sigma : 1 \to S$ 

Let's generalise for a minute.

> [!def]
> Given a category $\A$, an endofunctor $S : \A \to \A$, and a natural transform $\sigma : 1 \to S$, define a new category $\A_\sigma$ as follows. This is called (at least by this [reference](https://doi.org/10.1016/S1571-0661(05)80350-0)) the kliesli category of the pointed endofunctor $(S,\,\sigma)$.
> - objects: just the objects of $\A$
> - morphisms: $\mathrm{Hom}_{\A_\sigma}(A,B) = \displaystyle\coprod_{k \in \mathbb{N}} \mathrm{Hom}_\A(A,S^k B)\; \big/ \sim$ where $f \sim g$ if, for some $p,q \in \mathbb{N}$, $\sigma^pf=\sigma^qg$.

> [!lemma] 
> Suppose $\A$ is preabelian and $S$ is additive and preserves kernels and cokernels. Then $\A_\sigma$ is preabelian, and the obvious inclusion $I : \A \to \A_\sigma$ is additive and preserves kernels and cokernels.

***proof.*** I'm lazy, but I think this is true. It might be because my construction is a lax colimit in the 2-category of preabelian categories, exact functors, and natural transforms, but I'm not sure.

> [!lemma]
> Suppose a functor $F : \A \to \A$ and transform $\eta : FS \to SF$ are such that $(\sigma F)\eta = \eta (F\sigma)$. Then there is a functor $F_\sigma : \A_\sigma \to \A_\sigma$ with $F_\sigma I \cong I F$.

***proof.*** First we take $F_\sigma = F$ on objects. We can't quite pull the same trick on objects because the types don't line up. Define $F[ f : A \to S^n B ] = [ \eta^n Ff ]$, so that (if it is well defined) it has the desired property. $$ F_\sigma I f = F_\sigma [ f : A \to S^0 B ] = [ \eta^0 Ff ] = IFf $$
It remains to show $f$ is well defined. We need to show that $g \in [f]$ implies $\eta^n Fg \in F_\sigma[f]$. $\quad\square$
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsNyxbMCwwLCJGQSJdLFsyLDAsIkZTXnAgQiJdLFswLDIsIkZTXnEgQiJdLFsyLDIsIkYgU15uIEIiXSxbMywxLCJTXnAgRiBCIl0sWzEsMywiU15xIEYgQiJdLFszLDMsIlNebiBGIEIiXSxbMCwxLCJGZiJdLFswLDIsIkZnIiwyXSxbMSwzLCJGXFxzaWdtYV57bi1wfSIsMl0sWzIsMywiRlxcc2lnbWFee24tcX0iXSxbMiw1LCJcXGV0YV5xIiwyXSxbMSw0LCJcXGV0YV5wIl0sWzUsNiwiXFxzaWdtYV57bi1xfUYiLDJdLFs0LDYsIlxcc2lnbWFee24tcH1GIl0sWzMsNiwiXFxldGFebiIsMV1d&embed" width="100%" height="300" style="border-radius: 8px; border: none;"></iframe>
> [!lemma]
> In our case, $S : \mathsf{Filt}(\A) \to \mathsf{Filt}(\A)$, two morphisms $f : A \to S^i B$ and $g : A \to S^j B$ are equivalent if and only if $f_0 = g_0$.

> [!lemma]
> Suppose $\A$ is monoidal, and there is a transform $$\eta : S^i(\A) \otimes S^j(B) \to S^{i+j}(A \otimes B)$$then $\A_\sigma$ is monoidal.

***proof.*** We inherit the monoidal product on objects, define it on morphisms by
$$
\otimes_\sigma : (X,\,S^i Y) \times (Z,\,S^j W) \xrightarrow{\otimes} (X\otimes Z,\,S^i Y \otimes S^j W) \xrightarrow{\eta \,\circ\, -}(X\otimes Z,\,S^{i+j} (Y \otimes W))
$$
***let's apply this lemma to filtrations.***
We're need to construct a transform $\eta : S(A) \otimes B \to S(A \otimes B)$ 

| $B \otimes \sigma(A)$ | $A_0$    | $A_0$    | $A_1$    | $A_2$    | $\sigma(B \otimes A)$ | $A_0$    | $A_1$    | $A_2$    |
| --------------------- | -------- | -------- | -------- | -------- | --------------------- | -------- | -------- | -------- |
| $B_0$                 | $\cdots$ | 1        | 2        | 3        | $B_0$                 | 1        | 2        | 3        |
| $B_1$                 | 1        | 2        | 3        | $\cdots$ | $B_1$                 | 2        | 3        | $\cdots$ |
| $B_2$                 | 2        | 3        | $\cdots$ | $\cdots$ | $B_2$                 | 3        | $\cdots$ | $\cdots$ |
| $B_3$                 | 3        | $\cdots$ | $\cdots$ | $\cdots$ | $B_3$                 | $\cdots$ | $\cdots$ | $\cdots$ |
First, for $k>0$ note we have:
$$\begin{align*}
\big(\sigma(A) \otimes B\big)_k &= (A_0 \otimes B_k) \cup \Big( \bigcup_{i=0}^{k-1} A_{i} \otimes B_{k-1-i} \Big)\\
\sigma(A \otimes B)_k &= \Big( \bigcup_{i=0}^{k-1} A_{i} \otimes B_{k-1-i} \Big)
\end{align*}$$
So, in particular, $(\sigma(A) \otimes B)_k = (A_0 \otimes B_k) \cup (A \otimes B)_{k-1}$, that is $\sigma(A) \otimes B = (A_0 \boxtimes B) \oplus \sigma(A \otimes B)$  
We construct the transform $\eta_{A,B}$ as follows.
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXGRpc3BsYXlzdHlsZShBXzAgXFxvdGltZXMgQl9rKSBcXG9wbHVzIFxcQmlnKCBcXGJpZ29wbHVzX3tpPTB9XntrLTF9IEFfe2l9IFxcb3RpbWVzIEJfe2staX0gXFxCaWcpIl0sWzIsMCwiXFxkaXNwbGF5c3R5bGUoQV8wIFxcb3RpbWVzIEJfe2stMX0pIFxcb3BsdXMgXFxCaWcoIFxcYmlnb3BsdXNfe2k9MH1ee2stMX0gQV97aX0gXFxvdGltZXMgQl97ay1pfSBcXEJpZykiXSxbNCwwLCJcXGRpc3BsYXlzdHlsZSAgXFxCaWcoIFxcYmlnb3BsdXNfe2k9MH1ee2stMX0gQV97aX0gXFxvdGltZXMgQl97ay1pfSBcXEJpZykiXSxbMCwxLCIoMSBcXG90aW1lcyBiX3trLTF9KSBcXG9wbHVzIDEiXSxbMSwyLCJcXG5hYmxhX3tBXzAgXFxvdGltZXMgQl97ay0xfX0gXFxvcGx1cyAxIl1d&embed" width="100%" height="100" style="border-radius: 8px; border: none;"></iframe>
So, $\mu : A \otimes A \to SA$. The question is, what does $\mu(\mu \otimes 1)$ mean?
$$\begin{align*}
\bigoplus_{i+j=n} A_i \otimes A_j &= (A \otimes A)_n\\
&\;\Bigg\downarrow \; \mu_n \\[2mm]
A_{n-1} &= (SA)_n
\end{align*}$$

