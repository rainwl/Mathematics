# Tensor Calculus

## 1st-order Derivatives
`if`
```tex
f(x)\in R
```
`then`
```tex
df=\frac{\partial f}{\partial x} dx+\frac{\partial f}{\partial y} dy+\frac{\partial f}{\partial z} dz=\begin{bmatrix}\frac{\partial f}{\partial x}  &\frac{\partial f}{\partial y}  &\frac{\partial f}{\partial z}\end{bmatrix}\begin{bmatrix}dx \\dy \\dz\end{bmatrix} 
```
---

```tex
\frac{\partial f}{\partial \mathbf{x} } = \begin{bmatrix}\frac{\partial f}{\partial x}  &\frac{\partial f}{\partial y}  &\frac{\partial f}{\partial z}\end{bmatrix}
```
`or` `gradient`
```tex
\nabla f(x)=\begin{bmatrix}\frac{\partial f}{\partial x}  \\\frac{\partial f}{\partial y} \\\frac{\partial f}{\partial z}\end{bmatrix}
```
Gradient is the steepest direction for increasing f. It's perpendicular to the iso surface.

![](gradient.png)

`if`
```tex
f(x)=\begin{bmatrix}f(x)\\g(x) \\h(x)\end{bmatrix}\in R^{3} 
```
`then` `Jacobian`
```tex
J(x)=\frac{\partial f}{\partial x} =\begin{bmatrix}\frac{\partial f}{\partial x} &\frac{\partial f}{\partial y}  &\frac{\partial f}{\partial z} \\\frac{\partial g}{\partial x} &\frac{\partial g}{\partial y}  &\frac{\partial g}{\partial z} \\\frac{\partial h}{\partial x} &\frac{\partial h}{\partial y}  &\frac{\partial h}{\partial z} \end{bmatrix}
```
and `Deivergence`
```tex
\nabla \cdot f=\frac{\partial f}{\partial x} +\frac{\partial g}{\partial y} +\frac{\partial h}{\partial z} 
```
and `Curl`
```tex
\nabla \times f=\begin{bmatrix}\frac{\partial h}{\partial y} -\frac{\partial g}{\partial z} \\\frac{\partial f}{\partial z} -\frac{\partial h}{\partial x}  \\\frac{\partial g}{\partial x} -\frac{\partial f}{\partial y} \end{bmatrix}
```





















<seealso>
    <category ref="wiki">
        <a href="https://en.wikipedia.org/wiki/Partial_derivative">Partial_derivative</a>
        <a href="https://en.wikipedia.org/wiki/Jacobian_matrix_and_determinant">Jacobian matrix and determinant</a>
    </category>
</seealso>
