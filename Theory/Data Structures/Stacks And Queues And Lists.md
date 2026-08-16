
# Applications
- TBD

---
# List
A dynamic array, can be resized as needed

```python
list1 = []
list2 = [1,2,3,4]
#prefill with -1 of size 10
list3 = [-1] * 10

list1.append(0)
```


---
# Stack
Last In First Out (LIFO) list. retrieves the most recently inserted element and only allows pushing to top of stack.

## Standard Methods
- `void push(int value)` pushes the element `value` onto the stack.
- `void pop()` removes the element on the top of the stack.
- void top()` gets the top element of the stack.

```python
stack = [1,2,3]
#push 4
stack.append("4")
#gets 4 (top)
topElement = stack[-1]
#pops 4
stack.pop()
```

## Variants

### Monotonic Stack
- A monotonic stack is a stack where the elements are in increasing or decreasing order

---
# Queue
First In First Out (FIFO) list. Either allows pushing to bottom of list and retrieve at top of list or vice versa

## Standard Methods
- `void enqueue(int value)` pushes the newest element to queue.
- `void dequeue()` removes the oldest element from queue.
- `void peek()` gets the very first element of queue.

```python
#in this case, 0 is front of queue and -1 is back of queue
queue = [1,2,3]

#enqueue 4 at back of queue
queue.append(4)
#peek
queue[0]
#dequeue
queue.pop(0)

```


---
# Deque
Double Ended queue, same as queue but with extra capability to add elements to front of queue


```python
from collections import deque
q = deque()

#queue normally
q.append('a')
#add to front of queue (ahead of 'a')
dq.appendleft('b')
print(q.popleft()) #pops b


```