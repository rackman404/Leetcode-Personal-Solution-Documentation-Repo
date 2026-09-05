

An alternative version of [Dynamic Programming](Theory/Techniques/Dynamic%20Programming.md) (But not actually DP), in DP, we try and avoid solving subproblems more than once by caching data in a table for future use. Memoization does the same thing but in a different approach.

---
# Approach
NOTE: first 3 are same as DP, 4th is where stuff is different

### Compute optimal solutions
The main idea is to remember which subproblems have been solved; if the same subproblem is encountered more than once during the recursion, the solution will be looked up in a table rather than being re-calculated. This is easy to do if we initialize a table of all possible subproblems having the value undefined in every entry. Whenever a subproblem is solved, the table entry is updated.