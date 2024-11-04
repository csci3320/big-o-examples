# Showing a function is O() with examples

## Definition 
A function $f(x)$ is $O(g(x))$ if there is some pair $(c, n_0)$, with $c>0$, such that for all $x>n_0$, $f(x) < c*g(x)$. Showing that some function $f(x)$ is $O(g(x))$ therefore becomes a problem of finding a pair $(c, n_0)$ that satisfy this definition.

## Steps
The following are steps you can follow to find $(c,n_0)$ for a specific Big O problem. To help us understand the steps, we will use this example: Show that $4x+3$ is $O(n)$.

### Step 1 - Find $f(x)$. 
There are two functions in a Big O statement. The one inside the $O()$ notation is $g(x)$. Therefore the function outside the $O()$ is $f(x)$. 

#### Step 1 Example
In our example, the function outside the Big O notation is $4x+3$. Therefore $f(x) = 4x+3$

### Step 2: Find $g(x)$. 

Similar to step 1, except the we are looking for the function inside the $O()$ notation. Due to historical reasons, the function in the $O()$ notation is written with the variable $n$ instead of $x$. In order to find $g(x)$ we have to find the function inside the $O()$ and then change the n variable to $x$. 

##### Step 2 Example 

In our example, the function inside $O()$ is $n$. Converting the variable $n$ to $x$, we have $g(x)=x$

### Step 3: Find c.

 This step does not have a perfect algorithm. One approach is to choose a $c$ that is bigger than the coefficient in front of the term in $f(x)$ with the highest degree. 

#### Step 3 Example

In our example the term with the highest degree in $f(x)$ is $4x$. The coefficient of $4x$ is 4. A number that is larger than 4 is 5. Therefore we set $c$ to be 5.

### Step 4 Find n_0
We need to find an $n_0$ such that for all $x$ greater than $n_0, f(x) < c*g(x)$. There are several ways to find $n_0$ once we have found $c$. One is to graph $f(x)$ and $c*g(x)$ and see where the graphs intersect. Another way is to algebraically find $n_0$. To do this algebraically, we set $f(x)$ equal to $c*g(x)$. The solution to this equation is $n_0$.

#### Step 4 example

In our example, we have $f(x) = 4x+3$, $g(x)=x$, and $c=5$. We start by setting $f(x)$ equal to $c*g(x)$; in this example this is $4x+3=5x$. If we subtract $4x$ from both sides, we get $3=x$. This means $n_0$ is $3$ if $c=5$. Since we have found both $c$ and $n_0$, we have found the answer to our problem. Specifically, we can state that our solution is $c=5, n_0=3$. We are now done.

## More Examples

### Show that $5x^2+10$ is $O(n^2)$
1. $f(x)$ is $5x^2+10$ since it is the function outside the $O()$
2. $g(x)$ is $x^2$ since the function inside the $O()$ is $n^2$
3. One $c$ that will work is $c=6$ since it is greater than the coefficient of the greatest term $(5x^2)$
4. Find n_0 algebraically:

   - $5x^2+10=6x^2$ |  $(f(x)=c*g(x))$
   - $10=x^2$ |  Subtract from both sides
   - $x=\sqrt{10}$ or $x\approx 3.16$ | Solve for x

A solution: $c=6, n_0=\sqrt{10}$

### Show that $9x^2+10x+3$ is $O(n^2)$
1. $f(x)$ is $9x^2+10x+3$ since it is the function outside the $O()$
2. $g(x)$ is $x^2$ since the function inside the $O()$ is $n^2$
3. One $c$ that will work is $c=10$ since it is greater than the coefficient of the greatest term $(9x^2)$
4. Find n_0 algebraically:

   - $9x^2+10x+3=10x^2$ |  $(f(x)=c*g(x))$
   - $10x+3=x^2$ |  Subtract from both sides
   - $x^2-10x-3=0$ |  Set equal to 0
   - $x=5\pm 2\sqrt{7}$ or $x\approx 10.29$ | Solve using the quadratic formula

A solution: $c=10, n_0=5+2\sqrt{7}$

## Show that $2\cdot log_2(x)+4$ is $O(log_2 n)$
Note that may people write $O(log_2 n)$ as simply $O(log\ n)$
1. $f(x)$ is $2\cdot log_2(x)+4$ since it is the function outside the $O()$
2. $g(x)$ is $log_2(x)$ since the function inside the $O()$ is $log_2\ n$
3. One $c$ that will work is $c=3$ since it is greater than the coefficient of the greatest term $(2\cdot log_2(x))$
4. Find n_0 algebraically:

   - $2\cdot log_2(x)+4=3\cdot log_2(x)$ |  $(f(x)=c*g(x))$
   - $4=log_2(x)$ |  Subtract from both sides
   - $2^4=x$ or $x=16$ | Defition of $log_2$

A solution: $c=3, n_0=16$

## Show that $3x\cdot log_2(x)+5$ is $O(n\ log_2\ n)$
Note that may people write $O(n\ log_2\ n)$ as simply $O(n\ log\ n)$
1. $f(x)$ is $3x\cdot log_2(x)+5$ since it is the function outside the $O()$
2. $g(x)$ is $x\cdot log_2(x)$ since the function inside the $O()$ is $n\ log_2\ n$
3. One $c$ that will work is $c=4$ since it is greater than the coefficient of the greatest term $(3x\cdot log_2(x))$
4. Find n_0 algebraically:

   - $3x\cdot log_2(x)+5=4x\cdot log_2(x)$ |  $(f(x)=c*g(x))$
   - $5=x\cdot log_2(x)$ |  Subtract from both sides
   - $x\approx 3.08$ | You have to solve this with a calculator

A solution: $c=3, n_0\approx 3.08$
