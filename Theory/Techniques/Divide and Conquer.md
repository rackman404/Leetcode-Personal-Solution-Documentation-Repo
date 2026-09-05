

Divide-and-conquer algorithms are recursive, so their analysis depends on solving recurrence relations.

---
# Recurrence Relations
- A recurrence relation is a formula that expresses a general term T(n) as a function of one or more previous terms, T(1), . . . , T(n − 1).
- A recurrence relation will also specify one or more initial values starting at T(1) (base cases).

### Coming up with Recurrence Relations
### Guess-and-check Method
Guess-and-check usually involves the following four steps:
step 1
- Tabulate some values T(1), T(2), . . . using the recurrence relation.
step 2
- Guess that the solution T(n) has a specific form, possibly involving undetermined constants.
step 3
- Use T(1), T(2), . . . to determine the actual values of the unspecified constants.
step 4
- Use induction to prove your guess for T(n) is correct.

### Recursion Tree Method
The recursion tree method is another way of solving recurrence relations. It consists of repeatedly “expanding” the recurrence and thereby constructing a tree. Summing all the values in the tree gives the solution to the recurrence. This method has some potential advantages as compared to the guess-and-check approach. First, it does not require us to make a possibly non-obvious guess


### Master Theorem
N/A

---
# Design Strategy 
### divide
Given a problem instance I, construct one or more smaller problem instances. If we have a of these smaller problem instances, we can denote them
by I1, . . . , Ia (these are called subproblems). Usually, we want the size of these
subproblems to be small compared to size(I), e.g., half the size.
### conquer
For 1 ≤ j ≤ a, solve the subproblem Ij recursively. Thus we obtain a solutions to subproblems, which we will denote by S1, . . . , Sa.
### combine
Given the solutions S1, . . . , Sa to the a subproblems, use an appropriate combining function to find the solution S to the problem instance I, i.e., S ← COMBINE(S1, . . . , Sa),
where COMBINE is the combining function. The COMBINE operation is often
the most complicated step of a divide-and-conquer algorithm.
Analysis of a divide-and-conquer algorithm typically involves solving a recurrence relation. Often the Master Theorem can be applied.