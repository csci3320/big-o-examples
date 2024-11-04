# Showing $f(x)$ is not $O()$

Part of doing Big O is showing that a function $f(x)$ is not Big O some other function. Doing this is different than working with traditional Big O calculations since we are not finding a $(c, n_0)$ pair. We instead have to show that for all pairs $(c, n_0), c>0$ our defition of Big O does not hold. Doing so would involving doing a proof. One proof technique for this would be a proof by contradition, similar to the sketch proof below as an example

## Sketch proof to show $x^2$ is not $O(n)$. 

To show that $x^2$ is not $O(n)$, we start by finding $f(x)$ and $g(x)$. In this case they are $f(x)=x^2$ and $g(x)=x$. If $x^2$ were $O(n)$, there would have to be a positive $n_0$ such that $(n_0+k)^2<c\cdot (n_0+k)$ for *any* positive $k$. Simplifying, we have $n_0+k<c$. Consider the case where $k=c$. This means $n_0+c<c$, which simplifies to $n_0<0$. This leads to a contradition since $n_0$ has to be positive.  Thus we conclude than $x^2$ is not $O(n)$.