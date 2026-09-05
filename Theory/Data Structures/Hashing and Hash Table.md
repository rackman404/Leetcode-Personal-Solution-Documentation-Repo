

# Application
- Use to find the most occurrences of a given value
- Use to find uniqueness of element(s)
	- I.E check if given elements
- Faster lookup (O(1)), no need to iterate over the entire hashmap/dict, can just retrieve immediately from key 


---
# Variants

### Hashmap/Dictionaries
- Composed of keys and corresponding values
- (python), Key can only store immutable (hash able elements)

```python

#dict creation
dictOne = {}
#predefine key elements
dictTwo = {"key": 11, "key2": 22}

#adding key
dictOne["key"] = "value"
#would add they "key" key if not already existing in dict
if ("key" not in dictOne):
	 dictOne["key"] = "value"

```

### Hashset
- Composed of only keys (no corresponding data)
- (python), can only store immutable (hash able elements)
- Useful if you only need to 

```python

#dict creation
dictOne = {}
#predefine key elements
dictTwo = {1,2,3,4}

#adding key
dictOne.add(5)
#removing key
doctOne.remove(5)

```

---
# Examples


## [Checking Intersection](https://leetcode.com/submissions/detail/2126537393/)