
Technique for computing solutions to subproblems of a overall problem in a **bottom up** fashion. It involves filling in a table, in a carefully specified order, to solve a problem. A recursive alternative exists called [Memoization](Theory/Techniques/Memoization.md)


# Steps
### Identify Optimal Structure
Examine the structure of an optimal solution to a problem instance I, and determine if an optimal solution for I can be expressed in terms of optimal solutions to one or more subproblems of I.

### Define Subproblems
Define a set of subproblems S(I) of the instance I, the solution of which enables the optimal solution of I to be computed. I will be the last or largest instance in the set S(I).

### Derive Recurrence Relation
Derive a recurrence relation on the optimal solutions to the instances in S(I). This recurrence relation should be completely specified in terms of optimal solutions to (smaller) instances in S(I) and/or base cases.

### Compute optimal solutions
Compute the optimal solutions to all the instances in S(I). Compute these solutions using the recurrence relation in a bottom-up fashion, filling in a table of values containing these optimal solutions. Whenever a particular table entry is filled in using the recurrence relation, the optimal solutions of relevant subproblems can be looked up in the table (because they have been computed already). The final table entry is the solution to I.