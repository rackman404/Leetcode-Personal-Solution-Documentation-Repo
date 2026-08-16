Greedy algorithms do no looking ahead and do not incorporate any backtracking (however, we note that backtracking algorithms are discussed in
detail in Chapter 8).
	• Greedy algorithms can usually be implemented efficiently. Often they consist of a pre-processing step based on the function g, followed by a single pass through the data. For a greedy algorithm to be efficient, we need a fast way to find the “best” extension of any given partial solution X.
	• In a greedy algorithm, only one feasible solution is constructed.
	• The execution of a greedy algorithm is based on local criteria (i.e., the value of the function g).
	• Correctness: For certain greedy algorithms, it is possible to prove that they always yield optimal solutions. However, these proofs can be tricky and complicated! (Recall that for any algorithm to be correct, it has to find the optimal solution for every problem instance.)

# Key Takeaways
- Single preprocessing Step (if required)
- Single passthrough 
	- Evaluate at each step assuming that the local maximum is probably the best possible maximum at the given moment (i.e doesn't need to check ahead or behind)