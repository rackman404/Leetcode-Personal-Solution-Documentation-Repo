
# Definition/Terminology

In an optimization problem, given a problem instance, we want to find a feasible solution that maximizes (or minimizes) a specified objective function. (The terms “feasible solution” and “objective function” are defined below.)


### Problem instance
As always, a problem instance is the input for the specified problem.
### Problem constraints
Constraints are necessary conditions (i.e., requirements) that must be satisfied.
### Feasible solution
If all the specified constraints are satisfied, then we have a feasible solution.
For any problem instance I, feasible(I) denotes the set of all outputs (i.e.,
solutions) for the instance I that satisfy the given constraints (i.e., all the
feasible solutions). Note that it may the case for certain problems and certain instances I that there are no feasible solutions.

### Objective function
An objective function assigns a non-negative real number to any feasible solution, so we can regard it as a function f : feasible(I) → R + ∪ {0}. We often think of an objective function f as specifying a profit or a cost. Thus, for a feasible solution X ∈ feasible(I), f(X) denotes the cost or profit of X. 

### Optimal solution
An optimal solution is a feasible solution X ∈ feasible(I) such that the profit f(X) is maximized (or the cost f(X) is minimized). Typically, we want to maximize a profit or minimize a cost.