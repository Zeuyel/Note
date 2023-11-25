[TOC]
# Lagrange Multiplier to KTT condition

I use the Convex Optimization writen by Stephen Boyd and Lieven Vandenberghe,but the optimization problems I meet in intermidiate microeconomics can be easily solved by Lagrange Multiplier. So I just want to give a simply guide and explaination for it there and the further study will be later

For a classical constrained optimation problem:

$$ \min f_0(x,y) \\ s.t. \quad f_i(x,y) \le c \\ h_i(x) = 0$$

We use that to desribe the problem to finding an \(x\) to minimize the \(f_0(x)\) .\(f_i\) is the inequality constraints and \(h_i\) is the equality constraints.

For a feasible problem, the optimal value \(p^*\) is defined as

\[p^* = \inf \{ f_0(x)|f_i(x) \le 0 , i =1, \cdots ,m, h_i(x) = 0, i =1, \cdots, p \} \]

- if the problem is infeasible,we have \(p^* = \) \(\infty\)
- if we have the points \(x_k\) with \(f_0(x_k) \to -\infty \) as \( k \to \infty \), then we say the problem is unbounded below.

Before sovle this problem,we should have a concept definition of Optimal and locally optimal points.
## Optimal and locally optimal points.

\[ X_{opt} = \{ x | f_{i}(x) \le 0 ,i = 1, \ldots ,m,\quad h_{i}(x)  = 0 , i=1, \ldots ,p,f_{0}(x)   = p^{*} \}  \]

so if the set \( X_{opt} \) exits(not empty), we say the optimal value is attained or achieved, and the problem is solvable. In practicable, the feasible point \( x \) with \( f_{0}(x) \le p^{*} + \epsilon \) (while the \( \epsilon > 0 \)) is called \( \epsilon \)-suboptimal, and the set of all \( \epsilon \)-suboptimal points is called the \( \epsilon \)-suboptimal set for this problem.

Now we can define the locally optimal by this:
\[ f_{0}(x) = \inf\{ f_{0}(z) | f_{i}(z) \le 0,1, \ldots ,m,\\ h_{i}(z) =0,i=1, \ldots ,p,\left| \left| z-x \right| \right|_2 \le R   \},with \quad R > 0 \]



We can solve it by Lagrange Multiplier Method：

$$\mathcal {L}(x,y,\lambda )=f(x,y) - \lambda \cdot ( g(x,y) - c )\\ \mathcal {L}(x,y,\lambda )=f(x,y) + \lambda \cdot ( g(x,y) - c )$$

We can use some good examples to get a further understanding toward this method.

