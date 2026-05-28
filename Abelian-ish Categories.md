***Lemma.*** Suppose $\def\A{\mathscr{A}} \A$ is an additive category. It follows that $\def\Mor{\mathsf{Mor}}\Mor(\A)$ is additive.
***proof.*** First, recall that $\Mor(\A) = [I, \A]$ so, because functor categories inherit (co)limits from the codomain, $\Mor(\A)$ admits finite coproducts. It remains to show that it is Ab-enriched.

An additive category is called preabelian if it has all kernels and cokernels.

***Lemma.*** If $\A$ is preabelian, then (co)kernel is an additive functor $\Mor(\A)$.

A morphism of an preabelian category is called strict if its image and coimage are isomorphic.

> [!def] Strict
> A morphism $f : A \to B$ of a preabelian category is strict if $\mathrm{im} f \cong \mathrm{coim} f$

***Lemma.*** For every morphism $f$ of a preab cat.
1. $\mathrm{ker}f$ is monic and strict.
2. $\mathrm{coker}f$ is epic and strict.
3. $f$ is strict if and only if it can be written as $me$ for strict monic $m$ and strict epic $e$.
4. A pullback of a strict mono is a strict mono.
5. A pushout of a strict epi is a strict epi.
***proof.*** See [this paper](https://doi.org/10.1007/BF02674106)

### snakey lemmas

***Lemma.*** Given a diagram of the following form in a preabelian category, with strict exact rows, there is a unique map $\eta$ which commutes with it.
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsOCxbMSwwLCJcXGJ1bGxldCJdLFsyLDAsIlxcYnVsbGV0Il0sWzMsMCwiXFxidWxsZXQiXSxbNCwwLCIwIl0sWzEsMSwiXFxidWxsZXQiXSxbMiwxLCJcXGJ1bGxldCJdLFszLDEsIlxcYnVsbGV0Il0sWzAsMSwiMCJdLFsyLDNdLFsxLDVdLFswLDQsIjAiLDJdLFswLDFdLFsxLDIsIiIsMSx7InN0eWxlIjp7ImhlYWQiOnsibmFtZSI6ImVwaSJ9fX1dLFs0LDUsIiIsMSx7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19XSxbNSw2XSxbMiw0LCJcXGV0YSIsMSx7ImxhYmVsX3Bvc2l0aW9uIjo3MCwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzcsNF0sWzIsNiwiMCJdXQ==&embed" width="100%" height="200" style="border-radius: 8px; border: none;"></iframe>
***proof.*** Observe.
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMTAsWzEsMSwiQSJdLFszLDEsIkIiXSxbNSwxLCJDIl0sWzYsMSwiMCJdLFsxLDMsIkEnIl0sWzMsMywiQiciXSxbNSwzLCJDJyJdLFswLDMsIjAiXSxbMyw0LCJcXGtlciBnJyJdLFszLDAsIlxcb3BlcmF0b3JuYW1le2Nva30gZiJdLFswLDEsImYiXSxbMSwyLCJnIiwwLHsic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fV0sWzIsM10sWzQsNSwiZiciLDIseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzUsNiwiZyciLDJdLFsxLDUsIlxcbGFtYmRhIiwxXSxbNyw0XSxbOCw1LCJcXGlvdGEiLDIseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzIsNiwiMCJdLFsyLDUsIlxcbWF0aHR0eyhyKX0iLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMSw0LCJcXG1hdGh0dHsobCl9IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzEsOCwiXFx2YXJwaGkiLDEseyJjdXJ2ZSI6LTQsImNvbG91ciI6WzI0MCw2MCw2MF0sInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX0sWzI0MCw2MCw2MCwxXV0sWzAsNCwiMCIsMl0sWzEsOSwiIiwxLHsic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fV0sWzksOCwiIiwxLHsiY3VydmUiOjMsImNvbG91ciI6WzMwLDYwLDYwXSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzksMiwiIiwxLHsiY3VydmUiOi0yLCJsZXZlbCI6Miwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs0LDgsIiIsMSx7ImN1cnZlIjoyLCJsZXZlbCI6Miwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==&embed" width="100%" height="300" style="border-radius: 8px; border: none;"></iframe>
We start by establishing the two isomorphisms, $\operatorname{dom}\ker g' \cong A'$ and $\operatorname{cod} \operatorname{cok} f \cong C$.$$\begin{align*}
\ker g' &\cong \ker \operatorname{cok} f' & \operatorname{cok} f &\cong \operatorname{cok} \ker g\\
&\cong \operatorname{im} f' & &\cong \operatorname{coim} g\\
&\cong f' & &\cong g
\end{align*}$$Now, by square $\texttt{(r)}$ we have $g'\circ\lambda = 0\circ g = 0$. It follows that $\lambda$ factors the kernel of $g'$. Denote this map (blue arrow) as $\varphi$, so that $\lambda = \iota \circ \varphi$. Finally, we create the orange arrow. It suffices to show that $\varphi f = 0$. Observe, starting with square $\texttt{(l)}$ we have$$\begin{align*}
f'\circ 0 &= \lambda\circ f\\
\iota \circ 0 &= \iota \circ \varphi \circ f\\
0 &= \varphi \circ f\\
\end{align*}$$This concludes the proof.

This is really an example of the connecting morphism of the snake lemma. More generally:

***Lemma.*** Suppose $\A$ is an quasi-abelian category. Given a morphism $(\alpha,\beta,\gamma)$ of strict short exact sequences (wherein each morphism component is strict), we obtain a connecting morphism, $\delta : \ker \gamma \to \operatorname{cok}\alpha$. Moreover, we obtain the following long exact sequence.$$\ker\alpha \to \ker \beta \to \ker \gamma \xrightarrow\delta \operatorname{cok}\alpha \to \operatorname{cok}\beta \to \operatorname{cok}\gamma$$***proof.*** See [this paper](https://doi.org/10.1007/BF02674106)

***Lemma.*** Suppose $\A$ is an quasi-abelian category, in which the top row of the following diagram is a strict exact sequence and $f$ is a morphism. If the pushout square exists, then the following extension is a strict exact sequence.
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMTAsWzEsMCwiXFxidWxsZXQiXSxbMywwLCJcXGJ1bGxldCJdLFs1LDAsIlxcYnVsbGV0Il0sWzYsMCwiMCJdLFswLDAsIjAiXSxbMSwyLCJcXGJ1bGxldCJdLFswLDIsIjAiXSxbMywyLCJcXGJ1bGxldCJdLFs1LDIsIlxcYnVsbGV0Il0sWzYsMiwiMCJdLFswLDEsIiIsMCx7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19XSxbMiwzXSxbNCwwXSxbMCw1LCJmIiwyXSxbNSw3LCJtIiwyLHsic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibW9ubyJ9fX1dLFsxLDddLFs3LDAsIiIsMix7InN0eWxlIjp7Im5hbWUiOiJjb3JuZXItaW52ZXJzZSJ9fV0sWzgsOV0sWzEsMiwiIiwwLHsic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fV0sWzYsNV0sWzcsOCwiXFxvcGVyYXRvcm5hbWV7Y29rZXJ9IG0iLDIseyJzdHlsZSI6eyJoZWFkIjp7Im5hbWUiOiJlcGkifX19XSxbMiw4LCIiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XV0=&embed" width="100%" height="200" style="border-radius: 8px; border: none;"></iframe>
***proof.*** Because $\A$ is quasi-abelian, $m$ inherits strictness from the morphism above it. Every cokernel is strict. Because $m$ is strict, $\ker \operatorname{coker} m = m$. Done.

***Lemma.*** Suppose $\bullet \xrightarrow{(0,\lambda,0)} \bullet \xrightarrow{(\alpha,\beta,\gamma)} \bullet$ is a diagram of strict exact sequences in a preabelian category. Then $\eta_{\beta\lambda} = \alpha \eta_\lambda$.
***proof.*** Indeed,
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMTMsWzEsMCwiXFxidWxsZXQiXSxbMiwwLCJcXGJ1bGxldCJdLFszLDAsIlxcYnVsbGV0Il0sWzQsMCwiMCJdLFsxLDEsIlxcYnVsbGV0Il0sWzIsMSwiXFxidWxsZXQiXSxbMywxLCJcXGJ1bGxldCJdLFswLDEsIjAiXSxbNCwxLCIwIl0sWzEsMiwiXFxidWxsZXQiXSxbMiwyLCJcXGJ1bGxldCJdLFszLDIsIlxcYnVsbGV0Il0sWzAsMiwiMCJdLFsyLDNdLFsxLDUsIlxcbGFtYmRhIiwwLHsiY29sb3VyIjpbMzAsNjAsNjBdfSxbMzAsNjAsNjAsMV1dLFswLDQsIjAiLDJdLFswLDFdLFsxLDIsImUiLDAseyJjb2xvdXIiOlswLDYwLDYwXSwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fSxbMCw2MCw2MCwxXV0sWzQsNSwibSciLDEseyJjb2xvdXIiOls2MCw2MCw2MF0sInN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19LFs2MCw2MCw2MCwxXV0sWzUsNl0sWzIsNCwiXFxldGFfXFxsYW1iZGEiLDEseyJsYWJlbF9wb3NpdGlvbiI6NzAsImNvbG91ciI6WzYwLDYwLDYwXSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fSxbNjAsNjAsNjAsMV1dLFsyLDYsIjAiXSxbNyw0XSxbNiw4XSxbNSwxMCwiXFxiZXRhIiwwLHsiY29sb3VyIjpbMzAsNjAsNjBdfSxbMzAsNjAsNjAsMV1dLFs5LDEwLCJtIiwyLHsiY29sb3VyIjpbMCw2MCw2MF0sInN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19LFswLDYwLDYwLDFdXSxbMTAsMTFdLFsxMiw5XSxbNCw5LCJcXGFscGhhIiwyLHsiY29sb3VyIjpbMTIwLDYwLDYwXX0sWzEyMCw2MCw2MCwxXV0sWzYsMTEsIlxcZ2FtbWEiXSxbMiw5LCJcXGV0YV97XFxiZXRhXFxsYW1iZGF9IiwxLHsibGFiZWxfcG9zaXRpb24iOjgwLCJjb2xvdXIiOlswLDYwLDYwXSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fSxbMCw2MCw2MCwxXV1d&embed" width="100%" height="250" style="border-radius: 8px; border: none;"></iframe>
That is, we have $$\begin{align*}
m\eta_{\beta\lambda}e &= \beta\lambda\\
&= \beta m'\eta_{\lambda}e\\
&= m\alpha\eta_{\lambda}e
\end{align*}$$Cancelling the epi and mono, we have our result.