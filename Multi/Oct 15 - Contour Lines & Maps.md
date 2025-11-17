Given a boundary and a line, we can always find the maximum value, because the *contour line is tangent to the boundary we've defined*.

For example, given a circle $x^2+y^2=1$, the points at which a contour line is **tangent** to the circle indicates that a *local maximum or minimum* occurs at those points.

Let $g(x,y)=x^2+y^2$, and $f=x^2y$. Consider the gradients:
$$\Delta g, \Delta f$$
At the max point, we have that $\Delta f = \lambda \Delta g$, with $\lambda$ being a number. So, we have:
$$\Delta f = (2xy,x^2)$$
$$\Delta g = (2x,2y)$$
$$(2xy,x^2)=\lambda(2x,2y)$$
So now we can form a system of equations:
$$2xy=2\lambda x$$
$$x^2=2\lambda y$$
$$x^2+y^2=1$$

And with these we can solve for the maximums and minimums:
$$y=\lambda, \rightarrow x^2=2\lambda^2,\rightarrow 2\lambda^2+\lambda^2=1$$
$$3\lambda^2 = 1$$
$$\lambda = \pm\frac{1}{\sqrt 3}$$
So we have that:
$$x=\pm \sqrt{\frac{2}3}, y=\pm\sqrt{\frac{1}3}$$
And we're left with our proposition:

PROP: Let $f: U\to \mathbb R$ be a smooth function. To maximize or minize $f$ on $g(\vec x)=c$, where $g:U\to \mathbb R$is smooth and if $f$ has a local max/min at $\vec a$ such that $\Delta g(\vec a)\ne \vec )$, there there is a scalar $\lambda$ such that :
$$\Delta f(\vec a)=\lambda \Delta g(\vec a)$$
