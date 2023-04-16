~~~
this is for gradient of scalar-valued functions
~~~

- ***gradient*** can be thought of as a way of 'capturing' all of the partial derivative-related information of a multivariable function

> represented with ∇

***what it is***
- a **vector-valued function** containing the individual partial derivatives!
$$
\displaylines{
given\ f(x,y)=x^{2}sin(y),\\
and\ its\ partial\ derivatives:
\\
\frac{∂f}{∂x} = 2xsin(y)
\\
\frac{∂f}{∂y} = x^{2}cos(y)
}
$$
- the resulting gradient is:
$$
  \displaylines{\nabla f(x,y) = \begin{bmatrix}
  2xsin(y)\\
  x^{2}cos(y)
  \end{bmatrix}
  }
$$
***what does this all mean geometrically?***
- first, notice that the gradient is essentially a representation of a vector field
- then, you start to realize the gradient points in the direction of steepest ascent