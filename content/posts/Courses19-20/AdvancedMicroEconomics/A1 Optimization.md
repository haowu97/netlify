# A1 Optimization

## 1.1 Unconstrained Optimization 

Optimization problem
$$
\max _{x} f(x)
$$

subject to $\mathrm{x} \in S$. 

where $f$ is the objective function, x is the choice variable, $S$ is the constraint set.

The solution to the optimization problem $x^{*}$ is called maximizer; $f\left(x^{*}\right)$ is called the maximum (value) of the function $f$ subject to the constraint $\mathrm{x} \in S$ 

Local maximizer: the variable $x^{*}$ is a local maximizer of the function $f$ subject to the constraint $\mathrm{x} \in S$ if there is a number $\epsilon>0$ such that $f(\mathrm{x}) \leq f\left(\mathrm{x}^{*}\right)$ for all $\mathrm{x} \in S$ for which the distance between $\mathrm{x}$ and $\mathrm{x}^{*}$ is at most $\epsilon$ 

Global maximizer

### 1.1.1 Existence of solution

Bounded set: the set $S$ is bounded if there exists a number $k$ such that the 
distance of every point in $S$ from the origin is at most $k$

Compact set: a closed and bounded set is a compact set. A continuous function on a 

compact set attains both a maximum and a minimum on the set.

#### Necessary condition of interior solution

Let $f$ be a differentiable function of $n$ variables defined on the set $S$. If the point x in the interior of $S$ is a local or global maximizer or minimizer of $f$ then
$$
f_{i}(x)=0 \text { for } i=1, \ldots, n
$$

Let $f$ be a function of $n$ variables with continuous partial derivatives of first and second order, defined on the set $S$. Suppose that $x^{*}$ is a stationary point of $f$ in the interior of $S$ (so that $f_{i}(\mathbf{x})=0$ for all $i$ )

- If $H\left(\mathbf{x}^{*}\right)$ is negative definite then $\mathbf{x}^{*}$ is a local maximizer
- If $x^{*}$ is a local maximizer then $H\left(x^{*}\right)$ is negative semidefinite
- If $H\left(\mathbf{x}^{*}\right)$ is positive definite then $\mathbf{x}^{*}$ is a local minimizer
- If $\mathrm{x}^{*}$ is a local minimizer then $H\left(\mathrm{x}^{*}\right)$ is positive semidefinite

Saddle point: a stationary point that is neither a local maximizer nor a local minimizer is a saddle point.

### 1.1.2 Envelope theorem

Let $f$ be a continuously differentiable function of $n+k$ variables. Define the function $f^{*}$ of $k$ variables by
$$
f^{*}(\mathrm{r})=\max _{\mathrm{x}} \mathrm{f}(\mathrm{x}, \mathrm{r})=f\left(\mathrm{x}^{*}(\mathrm{r}), \mathrm{r}\right)
$$

where $x$ is an $n$ -vector and $r$ is a $k$ -vector. If the solution of the maximization problem is a continously differentiable function of $\mathrm{r}$ then
$$
f_{h}^{*}(\mathrm{r})=f_{n+h}\left(\mathrm{x}^{*}(\mathrm{r}), \mathrm{r}\right)
$$

Instead of the total derivative, you only need to check the partial derivative w.r.t. the parameter of interest at the optimizing point.

## 1.2 Optimization with Equality Constraints

Let $f$ and $g^{1}, \ldots, g^{m}$ be continuously differentiable functions of $n$ variables defined on the set $S$, let $c_{j}$ for $j=1, \ldots, m$ be numbers. Now we face the following problem
$$
\max _{x} f(x) \text { subject to } g^{j}(x)=c_{j} \text { for } j=1, \ldots, m
$$

### .1.2.1 Lagrange method: constrained $\Rightarrow$ unconstrained

Transform the constrained problem into an unconstrained problem with $m$ more variables
$$
\max _{\mathbf{x}, \lambda} \mathscr{L}(\mathbf{x}, \lambda)=f(\mathbf{x})-\sum_{j=1}^{m} \lambda_{j}\left(g^{j}(\mathbf{x})-c_{j}\right)
$$

- First and second order conditions
- Special cases where $f$ is concave (convex) and the $g^{\prime}$ s are convex (concave)

First order conditions
$$
\begin{array}{l}
\frac{\partial \mathscr{L}\left(\mathrm{x}^{*}, \lambda^{*}\right)}{\partial x_{i}}=f_{i}\left(\mathrm{x}^{*}\right)-\left.\sum_{j=1}^{m} \lambda_{j}^{*} \frac{\partial g^{j}}{\partial x_{i}}\right|_{\mathrm{x}^{*}}=0 \text { for } i=1, \ldots, n \\
\frac{\partial \mathscr{L}\left(\mathrm{x}^{*}, \lambda^{*}\right)}{\partial \lambda_{j}}=c_{j}-g^{j}\left(\mathrm{x}^{*}\right)=0 \text { for } j=1, \ldots, m
\end{array}
$$

A special case with only one constraint
$$
\begin{aligned}
\nabla f\left(x^{*}\right)&=\lambda^{*} \nabla g\left(x^{*}\right) \\
g\left(x^{*}\right)&=c
\end{aligned}
$$

### 1.2.2 Lagrange multiplier

$$
\lambda^{*}=\frac{\nabla f\left(x^{*}\right)^{\prime} \Delta x}{\nabla g\left(x^{*}\right)^{\prime}\Delta x}
$$

The rate of change in the maximum over a change in the constraint.

The value of the Lagrange multiplier on the $j$th constraint at the solution of the problem is equal to the rate of change in the maximal value of the objective function as the $j$th constraint is relaxed. 

e.g. Shadow price of scarce resource (internal value/imputed value)

### 1.2.3 Envelope theorem

Let $f$ and $g^{j}$ for $j=1, \ldots, m$ be continuously differentiable functions of $n+k$ variables. Define the function $f^{*}$ of $k$ variables by
$$
\mathscr{L}^{*}(\mathrm{r})=\max _{\mathrm{x}} \mathrm{f}(\mathrm{x}, \mathrm{r}) \text { subject to } g^{\prime}(\mathrm{x}, \mathrm{r})=0 \text { for } j=1, \ldots, m
$$

where x is an $n$-vector and $\mathrm{r}$ is a $k$-vector. Suppose that the solution of the maximization problem and the associated Lagrange multipliers $\lambda_{1}, \ldots, \lambda_{m}$ are continuously differentiable functions of $r,$ then
$$
f_{h}^{*}(\mathrm{r})=\mathscr{L}_{n+h}\left(\mathrm{x}^{*}(\mathrm{r}), \mathrm{r}\right) \text { for } h=1, \ldots, k
$$

where the function $\mathscr{L}$ is defined by $\mathscr{L}(\mathrm{x}, \mathrm{r})=f(\mathrm{x}, \mathrm{r})-\sum_{j=1}^{m} \lambda_{j}g^{j}\left( \mathrm{x}, \mathrm{r}\right)$ for every $(x, r)$

## 1.3 Optimization with Inequality Constraints

Optimization problem
$$
\max _{x} f(x) \text { subject to } g^{j}(x) \leq c_{j} \text { for } j=1, \ldots, m
$$

Lagrange function
$$
\mathscr{L}(\mathbf{x}, \lambda)=f(\mathbf{x})-\sum_{j=1}^{m} \lambda_{j}\left(g^{j}(\mathbf{x})-c_{j}\right)
$$

### 1.3.1 Kuhn-Tucker conditions

$(x, \lambda)$ satisfies Kuhn-Tucker conditions for the problem if

1. $L_{i}(x, \lambda)=f_{i}\left(x^{*}\right)-\left.\sum_{j=1}^{m} \lambda_{j}^{*} \frac{\partial g^{j}}{\partial x_{i}}\right|_{x^{*}}=0$ for $i=1, \ldots, n$

2. $g^{j}(x)-c_{j}=0 \text{ & } \lambda_{j} > 0$ 

    or $g^{j}(\mathbf{x})-c_{j}<0 \text{ & } \lambda_{j}=0$ for $j=1, \ldots, m$ 

The second set of conditions are equivalent to
$$
\lambda_{j} \geq 0, g^{\prime}(\mathrm{x}) \leq c_{j} \text { and } \lambda_{j}\left(\mathscr{f}^{j}(\mathrm{x})-\mathrm{c}_{j}\right)=0 \text { for } j=1, \ldots, m
$$

one of two inequalities must be binding - "complementary slackness condition": **If a Lagrange multiplier is positive, its associated constraint must be binding; if constraint is slack, its associated Lagrange multiplier must be zero.**

