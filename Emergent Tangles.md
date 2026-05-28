Fix a handle body $D_p \times I$ and let $\def\T{\tilde{\mathcal{T}}}\T(S)$ denote the $\mathbb{C}$-span of framed tangles in that handle body with skeleton $S$. For convenience sake, fix some skeleton $S$ and omit it from writing. 

Now, we can draw this tangle space is in two equivalent ways: projection to the back, and projection to the bottom. In both cases, we our diagrams consist of paths with over/under information at each crossing. Turns out, it doesn't matter.

Define the strand filtration $(\T_n)_{n \in \mathbb{N}}$ on $\T$ by taking $\T_n$ to be the span of tangles with at least $n$ strand framing changes or strand crossing changes $\mathrm{span}_\mathbb{C}\{\looparrowright - \Rsh, \mathrlap{\nearrow}{\nwarrow} - \mathrlap{\nearrow}{\nwarrow}\}$ (obviously the diagrams should have crossing over/under info).

***Recall.*** A strand framing change is an untwisting $(\looparrowright) \mapsto (\Rsh)$. In particular, viewing our framed strand as ribbon, a framing change is an addition or removal of a 360 degree twist. A crossing change is a switching of an over-crossing to an under-crossing, or vice versa.

> [!example] 
> The quotient $\T^{0/1}(\bigcirc) := \T_0(\bigcirc)/\T_1(\bigcirc)$ is isomorphic to the space spanned by homotopy classes of loops in $D_p$.

Define the doubling map $c : \T(\vert) \to \T(\vert\vert)$ in the (not so) obvious way on basis elements and extended linearly, and compare it to the stacking map, defined by $s(\gamma) = \gamma \sigma\gamma\sigma^{-1}$ extended linearly. Note that both are filtered. Write $$ \lambda(\gamma) = (c-s)(\gamma)\gamma^{-1} $$Define another quotient, the conway quotient, as $\T_\nabla = \T / \big\langle\,\,\mathrlap{\nearrow}{\nwarrow} - \mathrlap{\nearrow}{\nwarrow} = b\uparrow\uparrow\big\rangle$. This space inherits a filtration by image.

To summarise.
1. We have spaces of framed tangles with a given skeleton.
2. On these spaces there are two filtrations.
3. Augment by $[[a]]$ and define the conway quotient.
4. Define $\T_\nabla^{1/2}(\vert) \hookrightarrow \T_\nabla^{/1}(\vert)$
5. Define $\lambda : \T_\nabla^{/2}(\vert) \to \T_\nabla^{/2}(\vert\vert)$

Perform a distressing argument.
1. LET $S$ is strict short exact sequence in $\mathsf{Exp}(\mathrm{gr})$.
2. LET $(0,\bar\lambda,0) : US \to US$ is a morphism of strict short exact sequences in $\mathsf{Filt}(\mathsf{Vect}_\mathbb{C})$.
3. NOW Every $0$ map is formal
4. PROVE $\mathrm{Alt}\,\mathrm{cl}$ is formal
5. NOW there is a strict exact sequence morphism $(\mathrm{Alt}\,\mathrm{cl}, \beta, 1) : S \to E$ in $\mathsf{Exp}(\mathrm{gr})$, created by the extension in $\mathsf{Filt}(\mathsf{Vect}_\mathbb{C})$.
6. PROVE $\beta\bar\lambda$ is formal
7. CONCLUDE $\zeta = \eta_{\beta\gamma}$ is formal.
In the following diagram, all arrows are filtered, the green arrows are formal, the red are not, and the blue are formal if the pink arrows are.
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMTYsWzMsMCwiXFxtYXRoY2Fse1R9X1xcbmFibGFeey8yfSh8KSJdLFs1LDAsIlxcbWF0aGNhbHtUfV9cXG5hYmxhXnsvMX0ofCkiXSxbNiwwLCIwIl0sWzEsMywiXFxtYXRoY2Fse1R9X1xcbmFibGFeey8xfShcXGJpZ2NpcmMpIFxcb3RpbWVzIFxcbWF0aGNhbHtUfV9cXG5hYmxhXnsvMX0oXFxiaWdjaXJjKSJdLFsxLDQsIlxcbWF0aGNhbHtUfV9cXG5hYmxhXnsvMX0oXFxiaWdjaXJjKSBcXG90aW1lcyBcXG1hdGhjYWx7VH1fXFxuYWJsYV57LzF9KFxcYmlnY2lyYykiXSxbMSwwLCJcXG1hdGhjYWx7VH1fXFxuYWJsYV57MS8yfSh8KSJdLFsxLDIsIlxcbWF0aGNhbHtUfV9cXG5hYmxhXnsxLzJ9KHx8KSJdLFszLDIsIlxcbWF0aGNhbHtUfV9cXG5hYmxhXnsvMn0ofHwpIl0sWzAsMiwiMCJdLFs1LDIsIlxcbWF0aGNhbHtUfV9cXG5hYmxhXnsvMX0ofHwpIl0sWzMsNCwiXFxidWxsZXQiXSxbNSw0LCJcXG1hdGhjYWx7VH1fXFxuYWJsYV57LzF9KHwpIl0sWzAsNCwiMCJdLFs2LDIsIjAiXSxbNiw0LCIwIl0sWzAsMCwiMCJdLFsxLDIsIiIsMCx7ImNvbG91ciI6WzEyMCw2MCw2MF19XSxbMCwxLCIiLDAseyJjb2xvdXIiOlsxMjAsNjAsNjBdLCJzdHlsZSI6eyJoZWFkIjp7Im5hbWUiOiJlcGkifX19XSxbMyw0LCJBbHQiLDIseyJjb2xvdXIiOlszMDAsNjAsNjBdfSxbMzAwLDYwLDYwLDFdXSxbMSw0LCJcXHpldGEiLDEseyJjdXJ2ZSI6LTQsImNvbG91ciI6WzI0MCw2MCw2MF0sInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX0sWzI0MCw2MCw2MCwxXV0sWzYsMywiY2wiLDIseyJjb2xvdXIiOlszMDAsNjAsNjBdfSxbMzAwLDYwLDYwLDFdXSxbNiw3LCIiLDAseyJjb2xvdXIiOlsxMjAsNjAsNjBdLCJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzUsNiwiMCIsMix7ImNvbG91ciI6WzEyMCw2MCw2MF19LFsxMjAsNjAsNjAsMV1dLFs4LDYsIiIsMCx7ImNvbG91ciI6WzEyMCw2MCw2MF19XSxbNyw5LCIiLDIseyJjb2xvdXIiOlsxMjAsNjAsNjBdLCJzdHlsZSI6eyJoZWFkIjp7Im5hbWUiOiJlcGkifX19XSxbMSw5LCIwIiwwLHsiY29sb3VyIjpbMTIwLDYwLDYwXX0sWzEyMCw2MCw2MCwxXV0sWzEsNiwiXFxldGEiLDEseyJsYWJlbF9wb3NpdGlvbiI6NzAsImN1cnZlIjoyLCJjb2xvdXIiOlswLDYwLDYwXSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fSxbMCw2MCw2MCwxXV0sWzQsMTAsIiIsMix7ImNvbG91ciI6WzI0MCw2MCw2MF0sInN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifSwiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzEwLDExLCIiLDIseyJjb2xvdXIiOlsyNDAsNjAsNjBdLCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbOSwxMSwiMSIsMCx7ImNvbG91ciI6WzEyMCw2MCw2MF19LFsxMjAsNjAsNjAsMV1dLFsxMiw0LCIiLDAseyJjb2xvdXIiOlsxMjAsNjAsNjBdfV0sWzcsMTAsIlxcYmV0YSIsMSx7ImxhYmVsX3Bvc2l0aW9uIjo2MCwiY29sb3VyIjpbMjQwLDYwLDYwXSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fSxbMjQwLDYwLDYwLDFdXSxbOSwxMywiIiwwLHsiY29sb3VyIjpbMTIwLDYwLDYwXX1dLFsxMSwxNCwiIiwwLHsiY29sb3VyIjpbMTIwLDYwLDYwXX1dLFsxNSw1LCIiLDAseyJjb2xvdXIiOlsxMjAsNjAsNjBdfV0sWzAsMTAsIiIsMSx7ImN1cnZlIjoyLCJjb2xvdXIiOlszMDAsNjAsNjBdLCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTAsNiwiIiwwLHsic3R5bGUiOnsibmFtZSI6ImNvcm5lci1pbnZlcnNlIn19XSxbNCwxMSwiMCIsMSx7ImN1cnZlIjo0LCJjb2xvdXIiOlsxMjAsNjAsNjBdfSxbMTIwLDYwLDYwLDFdXSxbNSwwLCIiLDAseyJjb2xvdXIiOlsxMjAsNjAsNjBdLCJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzAsNywiXFxsYW1iZGEiLDEseyJsYWJlbF9wb3NpdGlvbiI6NjAsImNvbG91ciI6WzAsNjAsNjBdfSxbMCw2MCw2MCwxXV1d&embed" width="100%" height="300" style="border-radius: 8px; border: none;"></iframe>
It remains to show that:
- [x] $\text{Alt} \circ \text{cl}$ is formal. ✅ 2026-05-21
- [ ] $\beta \circ \lambda$ is formal.