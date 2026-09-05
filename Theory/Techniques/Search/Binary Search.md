
# Overview and when to use

Time complexity: O(logN)
Space complexity: O(1) (some extra space needed to track low, high, mid, but thats its)


# Base Pattern

Generally, given a array of values (sorted), we can find value X in the array by performing binary search. 

### Algorithm
1. Define a "Low" and a "High"
	1. Generally at the start, Low = 0, High = length(array)
2. Find midpoint
3. Check if midpoint is value
	1. Return midpoint position if true
	2. Redefine Low and High Otherwise
		1. If (midpoint < value), then we can search the upper half (value cannot be present here) :
			1. low = mid+1
			2. high = high
		2. Otherwise (We search the bottom half):
			1. low = low
			2. high = mid-1
4. If converges, return -1 (d.n.e in array)

### Psuedocode
Input: X (Value to find), L (List of values, sorted)

1. Low <- 0
2. High <- L.length
3. While (Low <= High):
	1. Mid <- Low + (High-Low)//2 \#we note that //2 is floor division in this case
	2. if (array\[mid] == X):
		1. return mid
	3. elif (array\[mid] < X):
		1. low <- mid+1
		2. high <- high
	4. else:
		1. low = low
		2. high = mid-1
4. return -1


### [Example](https://leetcode.com/submissions/detail/2124266890/)
Taken from 704. Binary Search
```python
#straight up just simple binary search
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        low = 0
        high = len(nums)-1
        
        while (low <= high):
            mid = low + (high-low)//2 #should account for edge cases (length = 1)

            if (nums[mid] == target):
                return mid
            elif (nums[mid] < target): #smaller than x, we therfore ignore lower half
                low = mid+1
            else: #ignore upper half
                high = mid-1

        return -1
```
# Example Variants

### [Find lowest/highest correct value (In Continuous Range)](https://leetcode.com/submissions/detail/2124227248/)

Difference:
Unlike base pattern, here we cannot simply return the correct value (as its possible that the correct value is not the global maximum or minimum). We note that we are explicitly trying to find the ends of a range of values in the array.

Modification:
In this case, the modification is simple, we force ourselves to go until boundary converges, while tracking the mid value if its a correct value. Depending on if we are finding lowest/highest, we can just switch the boundary redefinitions as required

Taken from my 278. First Bad Version Solution
``` python
# The isBadVersion API is already defined for you.
# def isBadVersion(version: int) -> bool:

#binary search problem?
#the upperbound is n, we trying to find the lower bound
#n can be up to 2^31, thus we need O(nlogn) probably (which binary search is)

#variant of binary search, we can't just immedietly return the next bad version we find, thus we keep track of the lower mid as required, then return it at the end
class Solution:
    def firstBadVersion(self, n: int) -> int:  
        low = 0
        high = n

        firstKnownBad = n
        while (low <= high):
            #using floor div
            mid = low + (high-low)//2

            #print(mid)

            if (isBadVersion(mid) == True): #found new bad, redefine high limit at mid, find even earlier one (ignore right)
                firstKnownBad = mid
                low = 0
                high = mid-1
            else: #found no new bad, ignore left
                low = mid+1

        return firstKnownBad
```
Note that we continue shrinking the bounds of the search as required, eventually we will leave the loop when the bounds converge, thus we can return the best possible value at the end.

### [Get Expected Position If Target DNE in array](https://leetcode.com/submissions/detail/2124275603/)




### [Target number not known](https://leetcode.com/submissions/detail/2125304812/)