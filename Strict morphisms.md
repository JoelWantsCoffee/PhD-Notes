> [!quote] Strict
> A morphism $f : A \to B$ of a preabelian category is strict if $\mathrm{im} f \cong \mathrm{coim} f$

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
> [!info] Lemma.
> Our two definitions agree: if $\mathcal{A}$ is abelian, then a morphism $f_\bullet : A_\bullet \to B_\bullet$ in $\mathsf{Filt}(\mathcal{A})$ is strict if and only if $\mathrm{im} f_i = \mathrm{im} f_0 \cap B_i$ (where $\cap$ is pullback).

***Proof.*** Observe:
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMjAsWzIsNSwiXFxtYXRocm17aW19IGZfMFxcY2FwIEJfaSJdLFsyLDYsIkJfaSJdLFsyLDEsIkFfaSJdLFswLDYsIkJfMCJdLFswLDUsIlxcbWF0aHJte2ltfSBmXzAiXSxbMCwxLCJBXzAiXSxbMywxLCJcXGNkb3RzIl0sWzMsNSwiXFxjZG90cyJdLFszLDYsIlxcY2RvdHMiXSxbMCwyLCJcXG1hdGhybXtjb2ltfSBmXzAiXSxbMiwyLCJcXG1hdGhybXtpbX0oXFxtYXRocm17Y29pbX0oZl8wKWFfMFxcY2RvdHMgYV9pKSJdLFswLDAsIlxca2VyIGZfMCJdLFsyLDAsIlxca2VyIGZfaSJdLFszLDAsIlxcY2RvdHMiXSxbMywyLCJcXGNkb3RzIl0sWzAsNywiXFxtYXRocm17Y29rZXJ9Zl8wIl0sWzIsNywiXFxtYXRocm17aW19KFxcbWF0aHJte2Nva2VyfShmXzApYl8wXFxjZG90cyBiX2kpIl0sWzMsNywiXFxjZG90cyJdLFsyLDQsIlxcbWF0aHJte2ltfSBmX2kiXSxbMiwzLCJcXG1hdGhybXtjb2ltfSBmX2kiXSxbMSwzLCJcXGNkb3RzIiwxXSxbNCwzLCIiLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzIsNSwiXFxjZG90cyIsMV0sWzYsMl0sWzcsMF0sWzgsMV0sWzUsOSwiIiwwLHsic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fV0sWzIsMTAsIiIsMCx7InN0eWxlIjp7ImhlYWQiOnsibmFtZSI6ImVwaSJ9fX1dLFsxMSw1LCIiLDIseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzEyLDIsIiIsMix7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1vbm8ifX19XSxbMTIsMTEsIlxcY2RvdHMiLDFdLFsxMywxMl0sWzE0LDEwXSxbMywxNSwiIiwwLHsic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoiZXBpIn19fV0sWzEsMTYsIiIsMCx7InN0eWxlIjp7ImhlYWQiOnsibmFtZSI6ImVwaSJ9fX1dLFsxNiwxNSwiXFxjZG90cyIsMV0sWzE3LDE2XSxbMCw0LCJcXGNkb3RzIiwxXSxbOSw0LCJcXHRleHR0dHtBYkNhdH0iLDAseyJsZXZlbCI6Miwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxMCw5LCJcXGNkb3RzIiwxXSxbMCwxLCIiLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtb25vIn19fV0sWzEwLDE5LCJcXHRleHR0dHtMZW1tYX0iLDAseyJsZXZlbCI6Miwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxOSwxOCwiXFx0ZXh0dHR7QWJDYXR9IiwwLHsibGV2ZWwiOjIsInN0eWxlIjp7ImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTgsMCwiXFx0ZXh0dHR7ZGVzaXJlZCByZXN1bHR9IiwwLHsibGV2ZWwiOjIsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzAsMjAsIiIsMSx7ImxldmVsIjoxLCJzdHlsZSI6eyJuYW1lIjoiY29ybmVyIn19XSxbMTIsMjIsIiIsMSx7ImxldmVsIjoxLCJzdHlsZSI6eyJuYW1lIjoiY29ybmVyIn19XSxbNywyNSwiIiwwLHsibGV2ZWwiOjEsInN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dLFsxMywyMywiIiwxLHsibGV2ZWwiOjEsInN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dXQ==&embed" width="100%" height="500" style="border-radius: 8px; border: none;"></iframe>
This lemma says that, for filtrations over an abelian category, strictness measures if image (really cokernel) is computed component-wise.

