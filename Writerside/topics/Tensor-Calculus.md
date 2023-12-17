# Tensor Calculus

## Spring stiffness {collapsible="true"}

![](Spring.png){width="400"}

<procedure title="Spring" >
<p>Energy</p>
<code-block lang="tex"> E(x)=\frac{k}{2} (\begin{Vmatrix}x\end{Vmatrix}-L)^{2}
</code-block>
<p>Force</p>
<code-block lang="tex"> f(x)=-\nabla E(x)=-k(\begin{Vmatrix}x\end{Vmatrix}-L)(\frac{\partial \begin{Vmatrix}x\end{Vmatrix}}{\partial x} )^{T}=-k(\begin{Vmatrix}x\end{Vmatrix}-L)\frac{x}{\begin{Vmatrix}x\end{Vmatrix}}
</code-block>
<p>Tangent stiffness</p>
<code-block lang="tex"> H(x)=-\frac{\partial f(x)}{\partial x} =k\frac{xx^{T}}{\begin{Vmatrix}x\end{Vmatrix}^{2}}+k(\begin{Vmatrix}x\end{Vmatrix}-L) \frac{I}{\begin{Vmatrix}x\end{Vmatrix}} -k(\begin{Vmatrix}x\end{Vmatrix}-L)\frac{x}{\begin{Vmatrix}x\end{Vmatrix}^{2}} \frac{x^{T}}{\begin{Vmatrix}x\end{Vmatrix}}
</code-block>
<p> </p>
<code-block lang="tex"> =k\frac{xx^{T}}{\begin{Vmatrix}
x
\end{Vmatrix}^{2}}+k(1-\frac{L}{\begin{Vmatrix}
x
\end{Vmatrix}} ) (I-\frac{xx^{T}}{\begin{Vmatrix}
x
\end{Vmatrix}^{2}} ) </code-block>
</procedure>
