
> [!def] filtration category
> Given a ((pre)ableian) category $\def\A{\mathscr{A}}\A$, one obtains a new (preabelian) category, the category of (descending) filtrations on $\A$: as the diagram category:
> $$\mathsf{Filt}(\A) = [\mathbb{N}_\geq, \A]$$
> $$\bullet \longleftarrow \bullet \longleftarrow \bullet \longleftarrow \cdots$$
> One sometimes insists we restrict to mono-preseriving functors. Let's call this the category of mono filtrations.

[relevant](https://doi.org/10.1016/j.jpaa.2018.01.004)

> [!lemma]
> If $\A$ is preabelian then so is $\mathsf{Filt}(\A)$, and the forgetful $\mathsf{Filt}(\A) \to \A$ is additive.

***proof.*** See [stacks](https://stacks.math.columbia.edu/tag/0122).

> [!lemma]
> If $\A$ is abelian and monoidal then $\mathsf{Filt}(\A)$ is monoidal, and the forgetful $\mathsf{Filt}(\A) \to \A$ is monoidal.

***proof.*** Take $A_\bullet \otimes B_\bullet = \big(\bigcup_{i + j = n} A_i \otimes B_j \big)_{n}$ and take the unit object as $I \hookleftarrow I \hookleftarrow I \hookleftarrow \cdots$. We have
$$
\bigcup_{i + j = n} A_i \otimes B_j  \xhookleftarrow{ (1 \otimes b_0)\,\cup\, \bigcup_{k=0}^n (a_i \otimes 1) } \bigcup_{i + j = n+1} A_i \otimes B_j
$$

> [!lem]
> An epi in $\mathsf{Filt}(\A)$ is a such that $f_0$ is an epi. A mono is map such that each $f_i$ is a mono.

Now, given one object $A_\bullet \in \mathsf{Filt}(\A)$ and one object $B \in \A$. Consider the two constructions for a filtration on $B$. The stacks project gives special cases (mono-filtrations over vector spaces) of the following [here](https://stacks.math.columbia.edu/tag/0121).
* ***The induced filtration***: Given $f : B \to A_0$, take $B_i$ to be the pullback of $f$ and $A_i \to A_0$.
	* $I : \mathsf{Mor} \times_{\mathrm{cod}, U} \mathsf{Filt} \to \mathsf{Mor}\mathsf{Filt}$
	* Filtration morphisms $f : A \to B$ factor as $f = I(f_0,B) \circ \tilde f$
* ***quotient filtration***: Given $f : A_0 \to B$, take $B_i = \mathrm{im}(A_i \to B)$
	* $Q : \mathsf{Mor} \times_{\mathrm{dom}, U} \mathsf{Filt} \to \mathsf{Mor}\mathsf{Filt}$
	* Filtration morphisms $f : A \to B$ factor as $f = \tilde f \circ Q(f_0,A)$
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMTYsWzYsMCwiQV8xIl0sWzUsMCwiQV8wIl0sWzUsMSwiQiJdLFs3LDAsIkFfMiJdLFs2LDEsIlxcbWF0aHJte2ltfShmIGFfMCkiXSxbMCwwLCJCIl0sWzAsMSwiQV8wIl0sWzEsMSwiQV8xIl0sWzMsMSwiXFxjZG90cyJdLFsxLDAsIkIgXFxjYXAgQV8xIl0sWzMsMCwiXFxjZG90cyJdLFs3LDEsIlxcbWF0aHJte2ltfShmIGFfMGFfMSkiXSxbOCwwLCJcXGNkb3RzIl0sWzgsMSwiXFxjZG90cyJdLFsyLDAsIkIgXFxjYXAgQV8yIl0sWzIsMSwiQV8yIl0sWzAsMSwiYV8wIiwyXSxbMSwyLCJmIiwyXSxbMywwLCJhXzEiLDJdLFswLDRdLFs0LDJdLFs1LDYsImYiLDJdLFs3LDZdLFs5LDVdLFs5LDddLFs5LDYsIiIsMSx7InN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dLFsxMCw4XSxbMywxMV0sWzExLDQsIiIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMiwzXSxbMTMsMTFdLFsxMCwxNF0sWzgsMTVdLFsxNSw3XSxbMTAsMTUsIiIsMSx7InN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dLFsxNCw5XSxbMTQsMTVdLFsxNCw3LCIiLDIseyJzdHlsZSI6eyJuYW1lIjoiY29ybmVyIn19XV0=&embed" width="100%" height="150" style="border-radius: 8px; border: none;"></iframe>
Given a morphism of filtered objects $f_\bullet : A_\bullet \to B_\bullet$, we compute the kernel and the cokernel as follows. First, note that a morphism of filtered objects is just a diagram $\downarrow\; \leftarrow\; \downarrow\; \leftarrow\; \cdots$ in $\mathsf{Mor}(\A)$. We obtain our kernel/cokernel filtrations by applying the kernel/cokernel functor to this diagram. 
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMjQsWzAsMSwiWF8wIl0sWzEsMSwiWF8xIl0sWzIsMSwiWF8yIl0sWzAsMiwiWV8wIl0sWzEsMiwiWV8xIl0sWzIsMiwiWV8yIl0sWzAsMCwiXFxrZXIgZl8wIl0sWzEsMCwiXFxrZXIgZl8xIl0sWzIsMCwiXFxrZXIgZl8yIl0sWzMsMSwiXFxjZG90cyJdLFszLDIsIlxcY2RvdHMiXSxbMywwLCJcXGNkb3RzIl0sWzQsMCwiWF8wIl0sWzUsMCwiWF8xIl0sWzYsMCwiWF8yIl0sWzcsMCwiXFxjZG90cyJdLFs3LDEsIlxcY2RvdHMiXSxbNywyLCJcXGNkb3RzIl0sWzQsMSwiWV8wIl0sWzUsMSwiWV8xIl0sWzYsMSwiWV8yIl0sWzQsMiwiXFxtYXRocm17Y29rZXJ9IGZfMCJdLFs1LDIsIlxcbWF0aHJte2Nva2VyfSBmXzEiXSxbNiwyLCJcXG1hdGhybXtjb2tlcn0gZl8yIl0sWzEsMF0sWzIsMV0sWzAsMywiZl8wIl0sWzQsM10sWzUsNF0sWzEsNCwiZl8xIl0sWzYsMCwiXFxrZXIgZl8wIl0sWzcsMSwiXFxrZXIgZl8xIl0sWzcsNiwiISIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsyLDUsImZfMiJdLFs4LDIsIlxca2VyIGZfMiJdLFs4LDcsIiEiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTAsNV0sWzksMl0sWzExLDhdLFs3LDMsIjAiLDEseyJsYWJlbF9wb3NpdGlvbiI6NzAsImN1cnZlIjotMiwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZG90dGVkIn19fV0sWzgsNCwiMCIsMSx7ImxhYmVsX3Bvc2l0aW9uIjo3MCwiY3VydmUiOi0yLCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkb3R0ZWQifX19XSxbMTMsMTJdLFsxNCwxM10sWzIwLDE5XSxbMTksMThdLFsxNSwxNF0sWzE2LDIwXSxbMTcsMjNdLFsyMywyMiwiISIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsyMiwyMSwiISIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMiwxOCwiZl8wIl0sWzEzLDE5LCJmXzEiXSxbMTQsMjAsImZfMiJdLFsxOCwyMSwiXFxtYXRocm17Y29rZXJ9IGZfMCJdLFsxOSwyMiwiXFxtYXRocm17Y29rZXJ9IGZfMSJdLFsyMCwyMywiXFxtYXRocm17Y29rZXJ9IGZfMiJdLFsxMywyMSwiMCIsMSx7ImxhYmVsX3Bvc2l0aW9uIjo3MCwiY3VydmUiOi0yLCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkb3R0ZWQifX19XSxbMTQsMjIsIjAiLDEseyJsYWJlbF9wb3NpdGlvbiI6NzAsImN1cnZlIjotMiwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZG90dGVkIn19fV1d&embed" width="100%" height="300" style="border-radius: 8px; border: none;"></iframe>
We ought to compare these constructions (for filtrations), to those for mono-filtrations (which are discussed in the [the stacks projects](https://stacks.math.columbia.edu/tag/0122)). The non-mono-filtration kernel construction aligns with mono-filtration kernel construction from stacks (in which the kernel of $f_\bullet$ is the filtration induced by $\mathrm{ker} f_0$) when restricted to the category of mono-filtrations. That is, when we put a mono-filtration-morphism through our construction, we get a mono-filtration back – the same one produced by the stacks construction. It's not so simple with cokernels. Our construction for cokernel, does not always produce from a mono-filtration from a mono-filtration morphism – so it's plain different to the stacks construction (in which the cokernel of $f_\bullet$ is the quotient filtration on $\mathrm{coker}f_0$). See the right diagram below. There is a non-mono-filtration map from our cokernel to the stacks cokernel, though.
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMTQsWzEsMSwiQl8xIl0sWzAsMSwiQl8wIl0sWzAsMCwiQV8wIl0sWzEsMCwiQV8xIl0sWzAsMiwiXFxtYXRocm17Y29rZXJ9IGZfMCJdLFsxLDIsIlxcbWF0aHJte2Nva2VyfSBmXzEiXSxbMiwzLCJcXG1hdGhybXtpbX0oXFxtYXRocm17Y29rZXJ9KGZfMCkgYl8wKSJdLFs0LDAsIlxcWiJdLFs1LDAsIlxcWiJdLFs0LDEsIlxcWiJdLFs1LDEsIlxcWiJdLFs0LDIsIjAiXSxbNSwyLCJcXFovMlxcWiJdLFs2LDMsIjAiXSxbMCwxLCJiXzAiLDJdLFsyLDEsImZfMCIsMl0sWzMsMCwiZl8xIl0sWzMsMl0sWzEsNCwiXFxtYXRocm17Y29rZXJ9IGZfMCIsMix7InN0eWxlIjp7ImhlYWQiOnsibmFtZSI6ImVwaSJ9fX1dLFswLDUsIiIsMix7InN0eWxlIjp7ImhlYWQiOnsibmFtZSI6ImVwaSJ9fX1dLFs1LDQsIiIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFswLDYsIiIsMCx7ImN1cnZlIjotM31dLFs2LDQsIiIsMCx7ImN1cnZlIjotMywic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibW9ubyJ9fX1dLFszLDYsIjAiLDEseyJjdXJ2ZSI6LTV9XSxbNSw2LCIiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMyw0LCIwIiwxLHsibGFiZWxfcG9zaXRpb24iOjgwLCJjdXJ2ZSI6LTF9XSxbOCwxMCwiXFxjZG90IDIiXSxbOCw3LCJcXGNkb3QyIiwyLHsic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibW9ubyJ9fX1dLFsxMCw5LCIiLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzcsOV0sWzksMTEsIiIsMix7InN0eWxlIjp7ImhlYWQiOnsibmFtZSI6ImVwaSJ9fX1dLFsxMCwxMiwiIiwyLHsic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fV0sWzEyLDExXSxbMTIsMTMsIiIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMCwxMywiIiwxLHsiY3VydmUiOi0zLCJzdHlsZSI6eyJoZWFkIjp7Im5hbWUiOiJlcGkifX19XSxbMTMsMTEsIiIsMSx7ImN1cnZlIjotMywic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibW9ubyJ9fX1dXQ==&embed" width="100%" height="300" style="border-radius: 8px; border: none;"></iframe>
> [!lemma]
> When the underlying category $\A$ is abelian, the two definitions of cokernel agree (cokernel is computed component-wise) on induced filtrations. That is, 
> $$(\mathrm{coker}(\mathrm{ind}f))_i = \mathrm{coker}((\mathrm{ind}f)_i)$$

***proof.*** It suffices to show that $\mathrm{coker} f' \cong \mathrm{im}(\mathrm{coker}(f)g)$ given any pullback diagram:
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsNCxbMCwxLCJZIl0sWzEsMSwiWiJdLFsxLDAsIlAiXSxbMCwwLCJYIl0sWzEsMCwiZyJdLFszLDAsImYiLDJdLFsyLDMsImcnIiwyXSxbMiwxLCJmJyJdLFsyLDAsIiIsMSx7InN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dXQ==&embed" width="100%" height="200" style="border-radius: 8px; border: none;"></iframe>
This isomorphism follows from the up-to-isomorphism uniqueness of of epi-mono factorisations and the fact that the unique map $h : \mathrm{coker}(f') \to  \mathrm{coker}(f)$ is mono. I'm not actually sure if this latter statement is true – I haven't been able to prove it. I appeal to [stack exchange](https://math.stackexchange.com/questions/1827766/any-straightforward-proof-of-in-an-abelian-category-a-pullback-yields-a-monomo).
### Pullbacks, Pushouts, and Monification

> [!lem] 
> Pullbacks in $\mathsf{Filt}(\A)$ are computed component-wise

***proof.*** Observe.
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMjMsWzIsMSwiXFxidWxsZXQiXSxbMiwzLCJCXzEiXSxbMyw0LCJBXzEiXSxbMywyLCJDXzEiXSxbMCwxLCJcXGJ1bGxldCJdLFsxLDIsIkMiXSxbMCwzLCJCIl0sWzEsNCwiQSJdLFszLDAsIlxcYnVsbGV0Il0sWzUsMSwibXg9bXkiXSxbNSwyLCJwX0JteD1wX0JteSJdLFs1LDMsImJxX0J4PWJxX0J5Il0sWzUsNCwicV9CeD1xX0J5Il0sWzYsNCwicV9DeD1xX0N5Il0sWzYsMSwibXg9bXkiXSxbNiwyLCJwX0NteD1wX0NteSJdLFs2LDMsImNxX0N4PWNxX0N5Il0sWzQsMiwiXFxjZG90cyJdLFs0LDQsIlxcY2RvdHMiXSxbMywzLCJcXGNkb3RzIl0sWzUsMCwiXFx0ZXh0e3Byb29mIH1tXFx0ZXh0eyBpcyBtb25vLn0iXSxbNyw0LCJcXHRleHR7YXBwbHkgam9pbnQgbW9uby1uZXNzLn0iXSxbNywxLCJcXHRleHR7KGRlZil9Il0sWzUsN10sWzYsN10sWzIsNywiYSIsMSx7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19XSxbMSwyXSxbMywyXSxbMCwxLCJxX0IiLDEseyJsYWJlbF9wb3NpdGlvbiI6NzAsImNvbG91ciI6WzAsNjAsNjBdfSxbMCw2MCw2MCwxXV0sWzMsNSwiYyIsMSx7ImxhYmVsX3Bvc2l0aW9uIjozMCwiY29sb3VyIjpbMTIwLDYwLDYwXSwic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibW9ubyJ9fX0sWzEyMCw2MCw2MCwxXV0sWzAsMywicV9DIiwxLHsiY29sb3VyIjpbMTIwLDYwLDYwXX0sWzEyMCw2MCw2MCwxXV0sWzQsNSwicF9DIiwxLHsiY29sb3VyIjpbMTIwLDYwLDYwXX0sWzEyMCw2MCw2MCwxXV0sWzEsNiwiYiIsMSx7ImxhYmVsX3Bvc2l0aW9uIjozMCwiY29sb3VyIjpbMCw2MCw2MF0sInN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19LFswLDYwLDYwLDFdXSxbMCw0LCJtIiwxLHsiY29sb3VyIjpbNjAsNjAsNjBdLCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19LFs2MCw2MCw2MCwxXV0sWzgsMCwieCIsMSx7ImN1cnZlIjoyfV0sWzgsMCwieSIsMSx7ImN1cnZlIjotMn1dLFs0LDYsInBfQiIsMSx7ImNvbG91ciI6WzAsNjAsNjBdfSxbMCw2MCw2MCwxXV0sWzAsMiwiIiwxLHsic3R5bGUiOnsibmFtZSI6ImNvcm5lciJ9fV0sWzQsNywiIiwxLHsic3R5bGUiOnsibmFtZSI6ImNvcm5lciJ9fV0sWzE3LDMsIiIsMSx7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19XSxbMTgsMiwiIiwxLHsic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibW9ubyJ9fX1dLFsxOSwxLCIiLDEseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV1d&embed" width="100%" height="300" style="border-radius: 8px; border: none;"></iframe>
> [!lem]
> Let $i : \mathsf{Filt}(\A) \to [\mathbb{N}_\geq,\,\A]$ be the obvious inclusion functor. The left adjoint $m \dashv i$ is the monoficiation functor $m : [\mathbb{N}_\geq,\,\A] \to \mathsf{Filt}(\A)$, defined as follows using the universal property of image factorings. <iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsOCxbMCwwLCJBXzAiXSxbMSwwLCJBXzEiXSxbMiwwLCJBXzIiXSxbMywwLCJcXGNkb3RzIl0sWzAsMSwiQV8wIl0sWzEsMSwiXFxtYXRocm17aW19KGFfMCkiXSxbMiwxLCJcXG1hdGhybXtpbX0oYV8wYV8xKSJdLFszLDEsIlxcY2RvdHMiXSxbMiwxLCJhXzEiLDJdLFsxLDAsImFfMCIsMl0sWzMsMiwiYV8yIiwyXSxbNSw0LCIiLDIseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzcsNiwiIiwyLHsic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibW9ubyJ9LCJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNiw0LCIiLDIseyJjdXJ2ZSI6LTMsInN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19XSxbNiw1LCIiLDIseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn0sImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFs3LDQsIiIsMCx7ImN1cnZlIjotNSwic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibW9ubyJ9fX1dXQ==&embed" width="100%" height="150" style="border-radius: 8px; border: none;"></iframe>

***proof.*** todo

> [!lem]
> Pushouts in $\mathsf{Filt}(\A)$ are computed as the monofication of the componentwise computation.

***proof.*** Follows from monoficiation function being a left adjoint.

> [!lem]
> The forgetful functor $-_0 : \mathsf{Filt}(\A) \to \A$ is exact, that is, it preserves finite biproducts, kernels, and cokernels.

***proof.*** obvious.

Note that $-_0$ does not reflect kernels/cokernels. Indeed, the functor
$$\begin{align*}
\mathrm{dumb} : \mathsf{Filt}(\A) &\to \mathsf{Filt}(\A)\\
(A_n)_n &\mapsto (A_0)_n
\end{align*}$$
is such that $(\mathrm{dumb} f)_0 = f_0$, but it clearly destroys kernels/cokernels.

Recall that a category is quasi-abelian if the pushout of every kernel is a kernel, and the pullback of every cokernel is a cokernel. I'm hopeful that $\mathsf{Filt}(\A)$ is quasi-abelian.

### Strict morphisms
The stacks project gives a definition for strictness specific to filtered vector spaces. It says that a morphisms $f_\bullet : A_\bullet \to B_\bullet$ of filtered vector spaces is strict if 
$$
\begin{align*}
f_i(A_i) &= f_0(A_0) \cap B_i\\
\mathrm{im} f_i &= \mathrm{im} f_0 \cap B_i\\
% \\
% f_0a_0\ldots a_i(A_i) &= f_0(A_0) \cap B_i\\
% \mathrm{quo}(f_0)_i &= \mathrm{ind}(f_0)_i
\end{align*}
$$
We can express the stacks definition diagrammatically:
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsOSxbMSwxLCJcXG1hdGhybXtpbX0gZl8xIl0sWzEsMiwiQl8xIl0sWzEsMCwiQV8xIl0sWzAsMiwiQl8wIl0sWzAsMSwiXFxtYXRocm17aW19IGZfMCJdLFswLDAsIkFfMCJdLFsyLDAsIlxcY2RvdHMiXSxbMiwxLCJcXGNkb3RzIl0sWzIsMiwiXFxjZG90cyJdLFswLDFdLFsxLDNdLFswLDRdLFs0LDNdLFs1LDRdLFsyLDVdLFswLDMsIiIsMSx7InN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dLFsyLDBdLFs2LDJdLFs3LDBdLFs4LDFdLFs3LDEsIiIsMCx7InN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dXQ==&embed" width="100%" height="200" style="border-radius: 8px; border: none;"></iframe>
> [!lemma]
> Our two definitions agree: if $\mathcal{A}$ is abelian, then a morphism $f_\bullet : A_\bullet \to B_\bullet$ in $\mathsf{Filt}(\mathcal{A})$ is strict if and only if $\mathrm{im} f_i = \mathrm{im} f_0 \cap B_i$ (where $\cap$ is pullback).

***proof.*** Observe.
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMjAsWzIsNSwiXFxtYXRocm17aW19IGZfMFxcY2FwIEJfaSJdLFsyLDYsIkJfaSJdLFsyLDEsIkFfaSJdLFswLDYsIkJfMCJdLFswLDUsIlxcbWF0aHJte2ltfSBmXzAiXSxbMCwxLCJBXzAiXSxbMywxLCJcXGNkb3RzIl0sWzMsNSwiXFxjZG90cyJdLFszLDYsIlxcY2RvdHMiXSxbMCwyLCJcXG1hdGhybXtjb2ltfSBmXzAiXSxbMiwyLCJcXG1hdGhybXtpbX0oXFxtYXRocm17Y29pbX0oZl8wKWFfMFxcY2RvdHMgYV9pKSJdLFswLDAsIlxca2VyIGZfMCJdLFsyLDAsIlxca2VyIGZfaSJdLFszLDAsIlxcY2RvdHMiXSxbMywyLCJcXGNkb3RzIl0sWzAsNywiXFxtYXRocm17Y29rZXJ9Zl8wIl0sWzIsNywiXFxtYXRocm17aW19KFxcbWF0aHJte2Nva2VyfShmXzApYl8wXFxjZG90cyBiX2kpIl0sWzMsNywiXFxjZG90cyJdLFsyLDQsIlxcbWF0aHJte2ltfSBmX2kiXSxbMiwzLCJcXG1hdGhybXtjb2ltfSBmX2kiXSxbMSwzLCJcXGNkb3RzIiwxXSxbNCwzLCIiLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzIsNSwiXFxjZG90cyIsMV0sWzYsMl0sWzcsMF0sWzgsMV0sWzUsOSwiIiwwLHsic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fV0sWzIsMTAsIiIsMCx7InN0eWxlIjp7ImhlYWQiOnsibmFtZSI6ImVwaSJ9fX1dLFsxMSw1LCIiLDIseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzEyLDIsIiIsMix7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19XSxbMTIsMTEsIlxcY2RvdHMiLDFdLFsxMywxMl0sWzE0LDEwXSxbMywxNSwiIiwwLHsic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fV0sWzEsMTYsIiIsMCx7InN0eWxlIjp7ImhlYWQiOnsibmFtZSI6ImVwaSJ9fX1dLFsxNiwxNSwiXFxjZG90cyIsMV0sWzE3LDE2XSxbMCw0LCJcXGNkb3RzIiwxXSxbOSw0LCJcXHRleHR0dHtBYkNhdH0iLDAseyJsZXZlbCI6Miwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxMCw5LCJcXGNkb3RzIiwxXSxbMCwxLCIiLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzEwLDE5LCJcXHRleHR0dHtMZW1tYX0iLDAseyJsZXZlbCI6Miwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxOSwxOCwiXFx0ZXh0dHR7QWJDYXR9IiwwLHsibGV2ZWwiOjIsInN0eWxlIjp7ImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTgsMCwiXFx0ZXh0dHR7ZGVzaXJlZCByZXN1bHR9IiwwLHsibGV2ZWwiOjIsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzAsMjAsIiIsMSx7ImxldmVsIjoxLCJzdHlsZSI6eyJuYW1lIjoiY29ybmVyIn19XSxbMTIsMjIsIiIsMSx7ImxldmVsIjoxLCJzdHlsZSI6eyJuYW1lIjoiY29ybmVyIn19XSxbNywyNSwiIiwwLHsibGV2ZWwiOjEsInN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dLFsxMywyMywiIiwxLHsibGV2ZWwiOjEsInN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dXQ==&embed" width="100%" height="500" style="border-radius: 8px; border: none;"></iframe>
This lemma says that, for filtrations over an abelian category, strictness measures if image (really cokernel) is computed component-wise.

***Lemma.*** $\coker(\mathrm{ind}(f)) = \mathrm{quot}(\coker f)$

***Lemma.*** Suppose $A_\bullet \in \mathsf{Filt}(\A)$ and $x,y:X,\, Y \hookrightarrow A_0$. Then 
$$\mathrm{quot}(\mathrm{quot}(x)_0y) \cong \mathrm{quot}(x + y)$$
***Question:*** suppose $\A$ is monoidal closed. Is $\mathsf{filt}(\A)$?