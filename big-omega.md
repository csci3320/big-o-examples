# Showing a function is Big Omega, $\Omega$(), with examples

## Definition 
A function $f(x)$ is $\Omega(g(x))$ if there is some pair $(c, n_0)$, with $c>0$, such that for all $x>n_0$, $f(x) > c*g(x)$. Showing that some function $f(x)$ is $\Omega(g(x))$ therefore becomes a problem of finding a pair $(c, n_0)$ that satisfy this definition.

## Steps
The following are steps you can follow to find $(c,n_0)$ for a specific Big Omega problem. To help us understand the steps, we will use this example: Show that $4x+3$ is $\Omega(n)$.

### Step 1 - Find $f(x)$. 
There are two functions in a Big Omega statement. The one inside the $\Omega()$ notation is $g(x)$. Therefore the function outside the $\Omega()$ is $f(x)$. 

#### Step 1 Example
In our example, the function outside the Big Omega notation is $4x+3$. Therefore $f(x) = 4x+3$

### Step 2: Find $g(x)$. 

Similar to step 1, except the we are looking for the function inside the $\Omega()$ notation. Due to historical reasons, the function in the $\Omega()$ notation is written with the variable $n$ instead of $x$. In order to find $g(x)$ we have to find the function inside the $\Omega()$ and then change the n variable to $x$. 

##### Step 2 Example 

In our example, the function inside $\Omega()$ is $n$. Converting the variable $n$ to $x$, we have $g(x)=x$

### Step 3: Find c.

 This step does not have a perfect algorithm. One approach is to choose a $c$ that is *smaller* than the coefficient in front of the term in $f(x)$ with the highest degree. 

#### Step 3 Example

In our example the term with the highest degree in $f(x)$ is $4x$. The coefficient of $4x$ is 4. A number that is *smaller* than 4 is 3. Therefore we set $c$ to be 3.

### Step 4 Find n_0
In almost all $\Omega()$ examples, $n_0$ will be 0. Instead of finding $n_0$, we need to instead show that our defition of $\Omega$ holds for all positive values of $x$ for our given $c$. One way to do this is to graph $f(x)$ and $g(x)$. A more concrete way is to show this algebraically. To do this, we subtract the two functions from each other, i.e. $f(x)-g(x)$ and show that for all $x>0$, the resultant function will be positive. Remember if I subtract two things and the result is positive, then the first is greater than the second thing. We are used to subtraction with numbers, but now we are subtracting functions.

Showing that the difference function, i.e. $f(x)-g(x)$ is always positive is simplified by the fact what when we are looking at code, $f(x)$ will almost always be composed of the summation of positive terms. As a result, the coefficients if $f(x)$ will all be positive. If we subtract from a $g(x)$ whose corresponding coefficients are all smaller than those in $f(x)$, we will get a difference function whose terms all have positive coefficients. If a function has all positive coefficients, we know it will always be positive if $x>0$. 

#### Step 4 example

In our example, we have $f(x) = 4x+3$, $g(x)=x$, and $c=3$. We start by subtracting $f(x)$ and $c*g(x)$; in this example this results in $4x+3-3x$. Simplifying, we get $x+3$. Since the terms in $x+3$ are all positive, we know that it is always positive if $x>0$. Thus, we can conclude that if $c=3$ and $n_0=0$, then we satisfy the definition of $\Omega()$.  We are now done.

## More Examples

### Show that $5x^2+10$ is $\Omega(n^2)$
1. $f(x)$ is $5x^2+10$ since it is the function outside the $\Omega()$
2. $g(x)$ is $x^2$ since the function inside the $\Omega()$ is $n^2$
3. One $c$ that will work is $c=4$ since it is less than the coefficient of the greatest term $(5x^2)$
4. Show that $f(x)-g(x)$ has all positive terms:

   - $5x^2+10-4x^2$ |  $(f(x)-c*g(x))$
   - $x^2+10$ |  Simplify

Since $x^2+10$ has all positive terms, we have shown that $5x^2+10$ is $\Omega(n^2)$ using $c=4, n_0=0$

### Show that $9x^2+10x+3$ is $\Omega(n^2)$
1. $f(x)$ is $9x^2+10x+3$ since it is the function outside the $\Omega()$
2. $g(x)$ is $x^2$ since the function inside the $\Omega()$ is $n^2$
3. One $c$ that will work is $c=8$ since it is less than the coefficient of the greatest term $(9x^2)$
4. Show that $f(x)-g(x)$ has all positive terms:

   - $9x^2+10x+3-8x^2$ |  $(f(x)-c*g(x))$
   - $x^2+10x+3$ |  Simplify

Since $x^2+10x+3$  has all positive terms, we have shown that $9x^2+10x+3$ is $\Omega(n^2)$ using $c=8, n_0=0$