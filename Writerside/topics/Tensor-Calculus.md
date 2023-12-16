# Tensor Calculus

<seealso>
    <category ref="wiki">
        <a href="https://en.wikipedia.org/wiki/Partial_derivative">Partial_derivative</a>
        <a href="https://en.wikipedia.org/wiki/Jacobian_matrix_and_determinant">Jacobian matrix and determinant</a>
        <a href="https://en.wikipedia.org/wiki/Hessian_matrix">Hessian_matrix</a>
        <a href="https://en.wikipedia.org/wiki/Chain_rule">Chain_rule</a>
    </category>
</seealso>

## 1-order Derivatives {collapsible="true"}
![](gradient.png)

<procedure title="" >
<code-block lang="tex"> f(x)\in R </code-block>
<p> </p>
<code-block lang="tex"> df=\frac{\partial f}{\partial x} dx+\frac{\partial f}{\partial y} dy+\frac{\partial f}{\partial z} dz=\begin{bmatrix}\frac{\partial f}{\partial x}  &\frac{\partial f}{\partial y}  &\frac{\partial f}{\partial z}\end{bmatrix}\begin{bmatrix}dx \\dy \\dz\end{bmatrix}  </code-block>
</procedure>


<procedure title="" >
<code-block lang="tex"> \frac{\partial f}{\partial \mathbf{x} } = \begin{bmatrix}\frac{\partial f}{\partial x}  &\frac{\partial f}{\partial y}  &\frac{\partial f}{\partial z}\end{bmatrix} </code-block>
</procedure>

<procedure title="gradient" >
<code-block lang="tex"> \nabla f(x)=\begin{bmatrix}\frac{\partial f}{\partial x}  \\\frac{\partial f}{\partial y} \\\frac{\partial f}{\partial z}\end{bmatrix} </code-block>
</procedure>

> Gradient is the steepest direction for increasing f. It's perpendicular to the iso surface.



<procedure title="Jacobian" >
<code-block lang="tex"> f(x)=\begin{bmatrix}f(x)\\g(x) \\h(x)\end{bmatrix}\in R^{3} </code-block>
<p> </p>
<code-block lang="tex"> J(x)=\frac{\partial f}{\partial x} =\begin{bmatrix}\frac{\partial f}{\partial x} &\frac{\partial f}{\partial y}  &\frac{\partial f}{\partial z} \\\frac{\partial g}{\partial x} &\frac{\partial g}{\partial y}  &\frac{\partial g}{\partial z} \\\frac{\partial h}{\partial x} &\frac{\partial h}{\partial y}  &\frac{\partial h}{\partial z} \end{bmatrix}
  </code-block>
</procedure>


<procedure title="Deivergence" >
<code-block lang="tex"> \nabla \cdot f=\frac{\partial f}{\partial x} +\frac{\partial g}{\partial y} +\frac{\partial h}{\partial z} 
 </code-block>
</procedure>

<procedure title="Curl" >
<code-block lang="tex"> \nabla \times f=\begin{bmatrix}\frac{\partial h}{\partial y} -\frac{\partial g}{\partial z} \\\frac{\partial f}{\partial z} -\frac{\partial h}{\partial x}  \\\frac{\partial g}{\partial x} -\frac{\partial f}{\partial y} \end{bmatrix}
 </code-block>
</procedure>


## 2-order Derivatives {collapsible="true"}

`if`

```tex
f(x)\in R
```

`then` **Hessian**

```tex
H=J(\nabla f(x))=\begin{bmatrix}\frac{\partial ^{2}f }{\partial x^{2} }   & \frac{\partial ^{2}f }{\partial x \partial y}  & \frac{\partial ^{2}f }{\partial x \partial z}\\\frac{\partial ^{2}f }{\partial x \partial y}   & \frac{\partial ^{2}f }{\partial y^{2} }  & \frac{\partial ^{2}f }{\partial y \partial z}\\\frac{\partial ^{2}f }{\partial x \partial z}   & \frac{\partial ^{2}f }{\partial y \partial z} & \frac{\partial ^{2}f }{\partial z^{2}}\end{bmatrix}
```

`and` **Laplacian**

```tex
\nabla \cdot \nabla f(x)=\nabla ^{2}f(x)=\Delta f(x)=\frac{\partial ^{2}f}{\partial x^{2}}+ \frac{\partial ^{2}f}{\partial y^{2}}+\frac{\partial ^{2}f}{\partial z^{2}}
```

**Taylor Expansion**

`if`

```tex
f(x)\in R
```

`then`

```tex
f(x)=f(x_{0})+\frac{\partial f(x_{0})}{\partial x} (x-x_{0})+\frac{1}{2}\frac{\partial f^{2}(x_{0})}{\partial x^{}2}(x-x_{0})^{2}+...  
```

`if`

```tex
f(\mathbf{x} )\in R
```

`then`

```tex
f(\mathbf{x} )=f(\mathbf{x} _{0})+\frac{\partial f(\mathbf{x} _{0})}{\partial \mathbf{x} } (\mathbf{x} -\mathbf{x} _{0})+\frac{1}{2}(\mathbf{x} -\mathbf{x} _{0})^{T}\frac{\partial f^{2}(\mathbf{x} _{0})}{\partial \mathbf{x} ^{2}}(\mathbf{x} -\mathbf{x} _{0})^{2}+...  
```

```tex
=f(\mathbf{x} _{0})+\nabla f(\mathbf{x} _{0})\cdot (\mathbf{x} -\mathbf{x}_{0})+\frac{1}{2} (\mathbf{x} -\mathbf{x} _{0})^{T}H(\mathbf{x} -\mathbf{x} _{0})+...
```

`s.p.d`

```tex
V^{T}AV>0
```

## Vector 's norm 's derivative {collapsible="true"}

```tex
\frac{\partial \begin{Vmatrix}x\end{Vmatrix}}{\partial x} =\frac{x^{T}}{\begin{Vmatrix}x\end{Vmatrix}} 
```

The gradient of a vector indicates that the shortest side length of the vector can be changed, which is equivalent to
normalizing the direction.

```tex
\frac{\partial \begin{Vmatrix}x\end{Vmatrix}}{\partial x} =\frac{\partial (x^{T}x)^{1/2}}{\partial x} =\frac{1}{2} (x^{T}x)^{-1/2}\frac{\partial (x^{T}x)}{\partial x} = \frac{1}{2\begin{Vmatrix}x\end{Vmatrix}} 2x^{T}=\frac{x^{T}}{\begin{Vmatrix}x\end{Vmatrix}} 
```

```tex
\frac{\partial (x^{T}x)}{\partial x} =\frac{\partial (x^{2}+y^{2}+z^{2})}{\partial x} =\begin{bmatrix}2x &2y &2z\end{bmatrix} =2x^{T}
```

## Spring stiffness {collapsible="true"}

![](Spring.png){width="300"}

**Energy**

```tex
E(x)=\frac{k}{2} (\begin{Vmatrix}x\end{Vmatrix}-L)^{2}
```

**Force**

```tex
f(x)=-\nabla E(x)=-k(\begin{Vmatrix}x\end{Vmatrix}-L)(\frac{\partial \begin{Vmatrix}x\end{Vmatrix}}{\partial x} )^{T}=-k(\begin{Vmatrix}x\end{Vmatrix}-L)\frac{x}{\begin{Vmatrix}x\end{Vmatrix}} 
```

**Tangent stiffness**

```tex
H(x)=-\frac{\partial f(x)}{\partial x} =k\frac{xx^{T}}{\begin{Vmatrix}x\end{Vmatrix}^{2}}+k(\begin{Vmatrix}
x
\end{Vmatrix}-L) \frac{I}{\begin{Vmatrix}
x
\end{Vmatrix}} -k(\begin{Vmatrix}
x
\end{Vmatrix}-L)\frac{x}{\begin{Vmatrix}
x
\end{Vmatrix}^{2}} \frac{x^{T}}{\begin{Vmatrix}
x
\end{Vmatrix}}
```

```tex
=k\frac{xx^{T}}{\begin{Vmatrix}
x
\end{Vmatrix}^{2}}+k(1-\frac{L}{\begin{Vmatrix}
x
\end{Vmatrix}} ) (I-\frac{xx^{T}}{\begin{Vmatrix}
x
\end{Vmatrix}^{2}} )
```

## Spring with 2 ends stiffness {collapsible="true"}

![](Spring2.png){width="300"}

**Energy**

```tex
E(x)=\frac{k}{2} (\begin{Vmatrix} x_{01} \end{Vmatrix}-L)^{2}
```

**Force**

```tex
f(x)=-\nabla E(x)=\begin{bmatrix}
-\nabla _{0}E(x) \\
-\nabla _{1}E(x)
\end{bmatrix}=\begin{bmatrix}
 f_{e}\\
-f_{e}
\end{bmatrix}
```

,

```tex
f_{e}=-k(\begin{Vmatrix}
x_{01}
\end{Vmatrix}-L)\frac{x_{01}}{\begin{Vmatrix}
x_{01}
\end{Vmatrix}} 
```

**Tangent stiffness**

```tex
H(x)=\begin{bmatrix}
 \frac{\partial ^{2}E}{\partial x^{2}_{0}}  & \frac{\partial ^{2}E}{\partial x_{0}\partial x_{1}} \\
 \frac{\partial ^{2}E}{\partial x_{0}\partial x_{1}} & \frac{\partial ^{2}E}{\partial x^{2}_{1}}
\end{bmatrix}=\begin{bmatrix}
 H_{e} &-H_{e} \\
 -H_{e} &H_{e}
\end{bmatrix}
```

,

```tex
H_{e}=k\frac{x_{01}x^{T}_{01}}{\begin{Vmatrix}
x_{01}
\end{Vmatrix}^{2}} +k(1-\frac{L}{\begin{Vmatrix}
x_{01}
\end{Vmatrix}} )(I-\frac{x_{01}x^{T}_{01}}{\begin{Vmatrix}
x_{01}
\end{Vmatrix}^{2}} )
```