> I've seen how to deal with derivatives for single-variable functions, where the derivative can be found with respect to the independant variable.
> *what about functions with two, three, perhaps more inputs?*
~~~
for myself– in some cases, it's helpful to literally replace the 'other' variables with an actual constant to avoid confusion; just remember to plug back in at the end (if u need to)
~~~
- theoretically, it isn't too different from regular derivatives!
	- we're still looking at how a change in the value of an input impacts the output; one input at a time
~~~
before, given f(x), we may have looked for df/dx

now, given f(x,y,z), we look for ∂f/∂x as well as ∂f/∂y and ∂f/∂z
~~~
> in multivariable calculus, ∂ ("del") is used instead of d

- when evaluating, we can simply plug in values for all variables except the one we are evaluating with respect to (i.e. treat them as constants) :D

***example:***
$$
\displaylines{
given\ f(x,y)=x^{2}sin(y),\\
we\ can\ get:
\\
\frac{∂f}{∂x} = 2xsin(y)
\\
\frac{∂f}{∂y} = x^{2}cos(y)
}
$$
