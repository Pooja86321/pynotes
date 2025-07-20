---
title: Datastr
date: 2025-07-21
author: Your Name
cell_count: 74
score: 70
---

```python
# Stack using List
stack = []
```


```python
# Pushing elements
stack.append(10)
stack.append(20)
stack.append(30)
print("Stack after pushes:", stack)
```


```python
# Popping elements
stack.pop()
print("Stack after pop:", stack)
```


```python
# Peek
if stack:
    print("Top element:", stack[-1])
```


```python
# IsEmpty
print("Is stack empty?", len(stack) == 0)
```


```python
# Stack Length
print("Stack size:", len(stack))
```


```python
# Stack function
def print_stack(s):
    for i in reversed(s):
        print(i)
print_stack(stack)
```


```python
# Push more elements
stack.append(40)
stack.append(50)
print_stack(stack)
```


```python
# Pop all elements
while stack:
    stack.pop()
print("Stack cleared:", stack)
```


```python
# Queue using List
queue = []
```


```python
# Enqueue
queue.append(1)
queue.append(2)
queue.append(3)
print("Queue:", queue)
```


```python
# Dequeue
queue.pop(0)
print("After Dequeue:", queue)
```


```python
# Is queue empty?
print("Empty?", len(queue) == 0)
```


```python
# Peek front
if queue:
    print("Front:", queue[0])
```


```python
# Queue Length
print("Queue size:", len(queue))
```


```python
# Using deque for efficient queue
from collections import deque
dq = deque()

```


```python
dq.append(10)
dq.append(20)
dq.append(30)
print("Deque:", dq)
```


```python
Deque: deque([10, 20, 30])
```


```python
dq.popleft()
print("After popleft:", dq)
```


```python
dq.appendleft(5)
print("After appendleft:", dq)
```


```python
# Node class
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```


```python
# Linked List class
class LinkedList:
    def __init__(self):
        self.head = None

    def insert(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
        else:
            temp = self.head
            while temp.next:
                temp = temp.next
            temp.next = new_node

    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")
```


```python
ll = LinkedList()
ll.insert(1)
ll.insert(2)
ll.insert(3)
```


```python
ll.display()
```


```python
1 -> 2 -> 3 -> None
```


```python
# Insert at beginning
def insert_at_beginning(self, data):
    new_node = Node(data)
    new_node.next = self.head
    self.head = new_node
LinkedList.insert_at_beginning = insert_at_beginning
```


```python
ll.insert_at_beginning(0)
ll.display()
```


```python
0 -> 1 -> 2 -> 3 -> None
```


```python
# Delete by value
def delete(self, key):
    temp = self.head
    if temp and temp.data == key:
        self.head = temp.next
        return
    while temp.next:
        if temp.next.data == key:
            temp.next = temp.next.next
            return
        temp = temp.next
LinkedList.delete = delete
```


```python
ll.delete(2)
ll.display()
```


```python
0 -> 1 -> 3 -> None
```


```python
ll.delete(0)
ll.display()
```


```python
1 -> 3 -> None
```


```python
ll.delete(10)  # non-existent
ll.display()
```


```python
1 -> 3 -> None
```


```python
# Linear Search
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
    return -1
```


```python
arr = [5, 2, 9, 4, 7]
print("Index of 9:", linear_search(arr, 9))
```


```python
print("Index of 3 (not found):", linear_search(arr, 3))
```


```python
# Binary Search
def binary_search(arr, x):
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == x:
            return mid
        elif arr[mid] < x:
            low = mid + 1
        else:
            high = mid - 1
    return -1
```


```python
sorted_arr = sorted(arr)
print("Sorted:", sorted_arr)
```


```python
print("Binary search 4:", binary_search(sorted_arr, 4))
```


```python
print("Binary search 8 (not found):", binary_search(sorted_arr, 8))
```


```python
# Edge case: empty array
print("Empty array:", binary_search([], 1))
```


```python
# Edge case: one element
print("One element:", binary_search([5], 5))
```


```python
# Binary search for negative numbers
neg_arr = [-9, -3, 0, 2, 4]
print("Find -3:", binary_search(neg_arr, -3))
```


```python
# Bubble Sort
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
```


```python
data = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(data)
print("Bubble Sorted:", data)
```


```python
# Insertion Sort
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and key < arr[j]:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key
```


```python
data2 = [9, 1, 6, 3, 2]
insertion_sort(data2)
print("Insertion Sorted:", data2)
```


```python
# Selection Sort
def selection_sort(arr):
    for i in range(len(arr)):
        min_idx = i
        for j in range(i + 1, len(arr)):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
```


```python
data3 = [29, 10, 14, 37, 13]
selection_sort(data3)
print("Selection Sorted:", data3)

```


```python
# Merge Sort
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2
        L = arr[:mid]
        R = arr[mid:]
        merge_sort(L)
        merge_sort(R)
        i = j = k = 0
        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1
        while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1
        while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1
```


```python
data4 = [12, 11, 13, 5, 6, 7]
merge_sort(data4)
print("Merge Sorted:", data4)
```


```python
# Recursive Factorial
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)
```


```python
print("Factorial 5:", factorial(5))
```


```python
# Fibonacci
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)
```


```python
print("Fibonacci of 6:", fibonacci(6))
```


```python
# Print fibonacci series
for i in range(8):
    print(fibonacci(i), end=" ")
```


```python
# Recursion with sum of array
def sum_array(arr):
    if not arr:
        return 0
    return arr[0] + sum_array(arr[1:])
```


```python
print("Sum:", sum_array([1, 2, 3, 4]))

```


```python
# Tower of Hanoi
def hanoi(n, src, temp, dest):
    if n == 1:
        print(f"Move disk 1 from {src} to {dest}")
        return
    hanoi(n - 1, src, dest, temp)
    print(f"Move disk {n} from {src} to {dest}")
    hanoi(n - 1, temp, src, dest)
```


```python
hanoi(3, 'A', 'B', 'C')
```


```python
# Base case edge test
print("Hanoi 1 disk:")
hanoi(1, 'X', 'Y', 'Z')
```


```python
# Tree Node
class TreeNode:
    def __init__(self, val):
        self.left = None
        self.right = None
        self.val = val
```


```python
# Pre-order Traversal
def preorder(root):
    if root:
        print(root.val, end=' ')
        preorder(root.left)
        preorder(root.right)
```


```python
# Build a simple tree
root = TreeNode(1)
root.left = TreeNode(2)
root.right = TreeNode(3)
root.left.left = TreeNode(4)
root.left.right = TreeNode(5)
```


```python
print("Preorder traversal:")
preorder(root)
```


```python
# In-order
def inorder(root):
    if root:
        inorder(root.left)
        print(root.val, end=' ')
        inorder(root.right)
```


```python
print("\nInorder traversal:")
inorder(root)
```


```python
# Post-order
def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.val, end=' ')
```


```python
print("\nPostorder traversal:")
postorder(root)
```


```python
# Tree Depth
def depth(root):
    if not root:
        return 0
    return 1 + max(depth(root.left), depth(root.right))

```


```python
print("\nTree Depth:", depth(root))
```


```python

```


---
**Score: 70**