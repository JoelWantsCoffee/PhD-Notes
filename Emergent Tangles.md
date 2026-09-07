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


Let us compute $\lambda(\tau_1\tau_2^{-1})$ recall that $\tau_j^{-1}\sigma^{-1}\tau_i\sigma = \sigma^{-1}\tau_i\sigma\tau_j^{-1}$
$$\begin{align*}
\lambda(\tau_1\tau_2^{-1}) &= \Big( \tau_1{\color{red}\tau_2^{-1}}\sigma^{-1}\tau_1\tau_2^{-1}\sigma^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}\sigma \Big)\sigma \tau_2\tau_1^{-1}\\
&= \Big( \tau_1{\color{red}\tau_2^{-1}}\sigma^{-1}\tau_1{\color{lime }\sigma\sigma^{-1}}\tau_2^{-1}\sigma^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}\sigma \Big)\sigma \tau_2\tau_1^{-1}\\
&= \Big( \tau_1\sigma^{-1}\tau_1{\color{lime}\sigma}{\color{red }\tau_2^{-1}}{\color{lime}\sigma^{-1}}\tau_2^{-1}\sigma^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}\sigma \Big)\sigma \tau_2\tau_1^{-1}\\
&= \Big( \tau_1{\color{orange}\sigma^{-1}}\tau_1{\color{orange}\sigma}\tau_2^{-1}{\sigma^{-1}}\tau_2^{-1}{\color{orange}\sigma^{-1}} - \tau_1{\color{orange}\sigma}\tau_1{\color{orange}\sigma^{-1}}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}{\color{orange}\sigma} \Big)\sigma \tau_2\tau_1^{-1}\\
&= \Big( 
\tau_1{\color{orange}(\sigma^{-1} - \sigma)}\tau_1{\color{orange}\sigma}\tau_2^{-1}{\sigma^{-1}}\tau_2^{-1}{\color{orange}\sigma^{-1}} 
+ \tau_1{\color{orange}\sigma}\tau_1{\color{orange}(\sigma - \sigma^{-1})}\tau_2^{-1}{\sigma^{-1}}\tau_2^{-1}{\color{orange}\sigma^{-1}} 
+ \tau_1{\color{orange}\sigma}\tau_1{\color{orange}\sigma^{-1}}\tau_2^{-1}{\sigma^{-1}}\tau_2^{-1}{\color{orange}(\sigma^{-1} - \sigma)}\Big)\sigma \tau_2\tau_1^{-1}\\
&= b\Big( 
-\tau_1\tau_1{\color{orange}\sigma}\tau_2^{-1}{\sigma}\tau_2^{-1}{\color{orange}\sigma} 
+ \tau_1{\color{orange}\sigma}\tau_1\tau_2^{-1}{\sigma}\tau_2^{-1}{\color{orange}\sigma} 
- \tau_1{\color{orange}\sigma}\tau_1{\color{orange}\sigma}\tau_2^{-1}{\sigma}\tau_2^{-1}\Big)\sigma \tau_2\tau_1^{-1}\\
&= b\Big( 
-\tau_1\tau_1{\color{orange}\sigma}\tau_2^{-1}{\sigma}\tau_2^{-1}{\color{orange}\sigma} 
+ \tau_1{\color{orange}\sigma}\tau_1\tau_2^{-1}{\sigma}\tau_2^{-1}{\color{orange}\sigma} 
- \tau_1{\color{orange}\sigma}\tau_1\tau_2^{-1}{\sigma}\tau_2^{-1}{\color{orange}\sigma}\Big)\sigma \tau_2\tau_1^{-1}\\
&= b\Big( 
-\tau_1\tau_1{\color{orange}\sigma}\tau_2^{-1}{\sigma}\tau_2^{-1}{\color{orange}\sigma}\Big)\sigma \tau_2\tau_1^{-1}\\
&=  
-b\tau_1\tau_1\sigma\tau_2^{-1}\sigma{\color{lime}\tau_1^{-1}}\\
&=  
-b\tau_1\tau_1{\color{lime}\tau_1^{-1}}\sigma\tau_2^{-1}\sigma\\
&=  
-b\tau_1\sigma\tau_2^{-1}\sigma\\
\end{align*}$$

hmmm.
$$\begin{align*}
\lambda(\tau_1\tau_2^{-1}) &= \Big( \tau_1\tau_2^{-1}{\color{orange}\sigma}\tau_1\tau_2^{-1}\sigma^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}\sigma \Big)\sigma \tau_2\tau_1^{-1}\\
&= \Big( \tau_1\tau_2^{-1}{\color{orange}(\sigma-\sigma^{-1})}\tau_1\tau_2^{-1}\sigma^{-1}
+ \tau_1\tau_2^{-1}{\color{orange}\sigma^{-1}}\tau_1\tau_2^{-1}\sigma^{-1}
- \tau_1\sigma\tau_1\sigma^{-1}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}\sigma \Big)\sigma \tau_2\tau_1^{-1}\\
&= {\color{orange}b}\tau_1\tau_2^{-1} + 
\Big( \tau_1\tau_2^{-1}{\color{orange}\sigma^{-1}}\tau_1\tau_2^{-1}\sigma^{-1}
- \tau_1\sigma\tau_1\sigma^{-1}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}\sigma \Big)\sigma \tau_2\tau_1^{-1}\\
&\cong \tau_1\tau_2^{-1}\otimes 1 - \tau_1 \otimes \tau_2^{-1}\\
\end{align*}$$
ggggggnnnn $\sigma\tau\sigma\tau^{-1} = \tau^{-1}\sigma\tau\sigma$
$$
\begin{align*}
\lambda(\tau_1\tau_2^{-1}) &= \Big( \tau_1\sigma^{-1}\tau_1{\color{lime}\sigma^{-1}\sigma}\tau_2^{-1}{\color{orange}\sigma}\tau_2^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}\sigma \Big)\sigma \tau_2\tau_1^{-1}\\
&= b\tau_1\sigma\tau_1\tau_2^{-1}\tau_2^{-1}\sigma\tau_2\tau_1^{-1} + 

\Big( \tau_1\sigma^{-1}\tau_1{\color{lime}\sigma\sigma^{-1}}\tau_2^{-1}{\color{orange} \sigma^{-1}}\tau_2^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2^{-1}\sigma^{-1}\tau_2^{-1}\sigma \Big)\sigma \tau_2\tau_1^{-1}\\
\end{align*}
$$

mmhhh
$$\begin{align*}
\Big(\tau\sigma^{-1}\tau\sigma - \tau\sigma\tau\sigma^{-1}\Big)\sigma\tau^{-1} &= b\Big(-\tau + \sigma\tau\Big)\\
\Big(\tau\sigma\tau\sigma^{-1} - \tau\sigma\tau\sigma^{-1}\Big) &= 0\\
\end{align*}$$
hmm. $\sigma^{-1}\tau\sigma\tau = \tau\sigma\tau\sigma^{-1}$
$$
\begin{align*}
\Big(\tau\sigma^{-1}\tau\sigma^{-1} - \tau\sigma\tau\sigma^{-1}\Big)\sigma\tau^{-1} &= -b\tau\\
\Big(\tau\sigma\tau\sigma^{-1} - \tau\sigma\tau\sigma^{-1}\Big) &= 0\\
\end{align*}
$$
hmmm
$$\begin{align*}
&= \Big(\tau^{2}\sigma\tau^{2}\sigma^{-1} - \tau\sigma\tau\sigma^{-1}\tau\sigma\tau\sigma^{-1}\Big)\sigma\tau^{-1}\\
&= \Big(\tau\sigma\tau\sigma^{-1} - \tau\sigma^{-1}\tau\sigma^{-1}\Big)\sigma\tau^{-1}\\
&= b\tau\\
\end{align*}$$


$$\begin{align*}
\lambda(\tau_1\tau_2) &= \Big( \tau_1\tau_2{\sigma^{-1}}{\color{orange}\tau_1}\tau_2\sigma^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2\sigma\tau_2\sigma^{-1} \Big)\sigma \tau_2^{-1}\tau_1^{-1}\\
&= \Big( \tau_1{\color{lime}\sigma^{-1}\sigma}\tau_2{\sigma^{-1}}{\color{orange}\tau_1}\tau_2\sigma^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2\sigma\tau_2\sigma^{-1} \Big)\sigma \tau_2^{-1}\tau_1^{-1}\\
&= \Big( \tau_1{\color{lime}\sigma^{-1}}{\color{orange}\tau_1}{\color{lime}\sigma}\tau_2{\sigma^{-1}}\tau_2\sigma^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2\sigma\tau_2\sigma^{-1} \Big)\sigma \tau_2^{-1}\tau_1^{-1}\\
&= \Big( \tau_1{\color{red}\sigma^{-1}}{\tau_1}{\color{red}\sigma}\tau_2{\color{red}\sigma^{-1}}\tau_2\sigma^{-1} - \tau_1\sigma\tau_1\sigma^{-1}\tau_2\sigma\tau_2\sigma^{-1} \Big)\sigma \tau_2^{-1}\tau_1^{-1}\\
&= b\Big( 
- \tau_1{\tau_1}{\color{red}\sigma}\tau_2{\color{red}\sigma^{-1}}\tau_2\sigma^{-1}
+ \tau_1{\color{red}\sigma^{-1}}{\tau_1} \tau_2{\color{red}\sigma^{-1}}\tau_2\sigma^{-1}
- \tau_1{\color{red}\sigma^{-1}}{\tau_1}{\color{red}\sigma}\tau_2\tau_2\sigma^{-1} \Big)\sigma \tau_2^{-1}\tau_1^{-1}\\
&= b\Big( 
- \tau_1{\tau_1}{\color{red}\sigma}\tau_2{\color{red}\sigma^{-1}}\tau_1^{-1}
+ \tau_1{\color{red}\sigma^{-1}}{\tau_1} \tau_2{\color{red}\sigma^{-1}}\tau_1^{-1}
- \tau_1{\color{red}\sigma^{-1}}{\tau_1}{\color{red}\sigma}\tau_2\tau_1^{-1} \Big)\\
&\cong -\tau_1\otimes \tau_2 + 1\otimes\tau_1\tau_2-\tau_2\otimes\tau_1 
\end{align*}$$
but with the better sigma. $\tau_1\sigma\tau_2\sigma^{-1}=\sigma\tau_2\sigma^{-1}\tau_1$
$$\begin{align*}
\lambda(\tau_1\tau_2) &\cong \tau_1\tau_2\otimes 1  -\tau_1\otimes \tau_2 + 1\otimes\tau_1\tau_2-\tau_2\otimes\tau_1 
\end{align*}$$

we use $\sigma\tau_2\sigma^{-1}\tau_1^{-1}=\tau_1^{-1}\sigma\tau_2\sigma^{-1}$
$$\begin{align*}
\lambda(\tau_2\tau_1^{-1}) &= \Big(\tau_2{\color{red}\tau_1^{-1}}\sigma\tau_2\tau_1^{-1}\sigma^{-1} - \tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}\sigma^{-1}\tau_1^{-1}\sigma\Big)\sigma\tau_1\tau_2^{-1}\\
&= \Big(\tau_2{\color{red}\tau_1^{-1}}\sigma\tau_2{\color{lime}\sigma^{-1}\sigma}\tau_1^{-1}\sigma^{-1} - \tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}\sigma^{-1}\tau_1^{-1}\sigma\Big)\sigma\tau_1\tau_2^{-1}\\
&= \Big(\tau_2\sigma\tau_2{\color{lime}\sigma^{-1}{\color{red}\tau_1^{-1}}\sigma}\tau_1^{-1}\sigma^{-1} - \tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}\sigma^{-1}\tau_1^{-1}\sigma\Big)\sigma\tau_1\tau_2^{-1}\\
&= \Big(\tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}{\color{orange}\sigma}\tau_1^{-1}{\color{orange}\sigma^{-1}} - \tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}\sigma^{-1}\tau_1^{-1}\sigma\Big)\sigma\tau_1\tau_2^{-1}\\
&= \Big(\tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}{\color{orange}\sigma}\tau_1^{-1}{\color{orange}(\sigma^{-1} - \sigma)} + \tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}{\color{orange}(\sigma - \sigma^{-1})}\tau_1^{-1}{\color{orange}\sigma}\Big)\sigma\tau_1\tau_2^{-1}\\
&\cong {\color{orange}b}\Big(-\tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}{\color{orange}\sigma}\tau_1^{-1} + \tau_2\sigma\tau_2\sigma^{-1}\tau_1^{-1}\tau_1^{-1}{\color{orange}\sigma}\Big)\sigma\tau_1\tau_2^{-1}\\
&\cong -1\otimes\tau_2\tau_1^{-1}+\tau_1\otimes \tau_2
\end{align*}$$
we use $\sigma^{-1}\tau\sigma\tau = \tau\sigma\tau\sigma^{-1}$
$$\begin{align*}
\lambda(\tau^2) &= \Big(\tau^2\sigma{\color{orange}\tau^2}\sigma - \tau\sigma\tau\sigma\tau\sigma\tau\sigma\Big)\sigma\tau^{-2}\\
&= \Big(\tau{\color{lime}\sigma\sigma^{-1}}\tau\sigma{\color{orange}\tau^2}\sigma - \tau\sigma\tau\sigma\tau\sigma\tau\sigma\Big)\sigma\tau^{-2}\\
&= \Big(\tau{\color{lime}\sigma}\tau\sigma{\color{orange}\tau}{\color{lime}\sigma^{-1}}{\color{orange}\tau}\sigma - \tau\sigma\tau\sigma\tau\sigma\tau\sigma\Big)\sigma\tau^{-2}\\
&= \Big(\tau{\color{lime}\sigma}\tau\sigma{\color{orange}\tau}({\color{lime}\sigma^{-1}} - \sigma){\color{orange}\tau}\sigma\Big)\sigma\tau^{-2}\\
&\cong b \tau{\color{lime}\sigma}\tau\sigma{\color{orange}\tau}{\color{orange}\tau}\sigma\sigma\tau^{-2}\\
&\cong b \tau{\color{lime}\sigma}\tau\sigma\\
&\cong \tau \otimes \tau
\end{align*}
$$Alright lock in:
$$\begin{align*}
\lambda(g_1g_2\cdots g_k) &= g_1\sigma^*g_1\sigma^*\cdots g_k\sigma^*g_k\sigma^* - g_1\cdots g_k\sigma g_1\cdots g_k\sigma\\
&= g_1\sigma^*g_1\sigma^*\cdots g_k\sigma^*g_k\sigma^* - g_1\cdots g_k\sigma g_1\cdots g_k\sigma\\
\end{align*}$$
$$\begin{align*}
\lambda(t') &= [t'st's - t's't's](st)\\
&= [t'(s - s')t's]st\\
&= b[t't's]st\\
&= b[t']\\
&\cong t'\otimes 1\\
\lambda(t) &= [tsts-tsts'](st')\\
&= [tst(s-s')](st')\\
&= b[tst](st')\\
&= b[tstst']\\
&\cong 1 \otimes t\\
\lambda(t_1't_2) &= t_2't_1[t_1't_2st_1't_2s - t_1's'{\color{orange}t_1'}st_2st_2s']s\\
&= t_2't_1[t_1't_2st_1't_2s - t_1's'{\color{orange}t_1'}st_2{\color{lime}s's}st_2s']s\\
&= t_2't_1[t_1't_2st_1't_2s - t_1's'st_2{\color{lime}s'{\color{orange}t_1'}s}st_2s']s\\
&= t_2't_1[t_1't_2st_1'ss't_2s - t_1't_2s't_1'sst_2s']s\\
&= [st_1'ss't_2s - s't_1'sst_2s']s\\
&= [st_1'ss't_2s \pm \ldots \pm \ldots - s't_1'sst_2s']s\\
&= [(s-s')t_1'ss't_2s + s't_1's(s'-s)t_2s + s't_1'sst_2(s-s')]s\\
&= b[t_1'ss't_2s - s't_1'st_2s + s't_1'sst_2]s\\
&= b[t_1't_2 - s't_1'st_2 + s't_1't_2]\\
&\cong t_1't_2\otimes 1 - t_1'\otimes t_2 + 1 \otimes t_1't_2\\
\end{align*}$$
recall: $\tau_2\sigma^{-1}\tau_1^{-1}\sigma=\sigma^{-1}\tau_1^{-1}\sigma\tau_2$
$$\begin{align*}
\lambda(t) &= t'[ts'ts' - tsts']s\\
&\cong t \otimes 1\\
\lambda(t') &= t[t's't's' - t's't's]s\\
&= b[-s't]s\\
&\cong -1 \otimes t\\
\lambda(t_1't_2) &= t_2't_1(t_1't_2s't_1't_2s' - t_1's't_1'st_2st_2s')s\\
&= t_2'(t_2s't_1'ss't_2 - s't_1'st_2st_2)\\
&= t_2'(s't_1'st_2s't_2 - s't_1'st_2st_2)\\
&= t_2'(t_2s't_1'ss't_2 - t_2s't_1'sst_2)\\
&= (s't_1'ss't_2 - s't_1'sst_2)\\
&= - bs't_1'st_2\\
&\cong t_1' \otimes t_2
\end{align*}$$
