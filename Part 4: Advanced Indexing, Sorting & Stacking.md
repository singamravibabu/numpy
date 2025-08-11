## **NumPy Cheatsheet — Part 4: Advanced Indexing, Sorting & Stacking**

---

### **1. Conditional Selection (`where`)**

```python
arr = np.array([10, 20, 30, 40])
result = np.where(arr > 25, 1, 0)
print(result)  # [0 0 1 1]
```

> Syntax: `np.where(condition, value_if_true, value_if_false)`

---

### **2. Extracting Non-zero Elements**

```python
arr = np.array([0, 2, 0, 4, 5])
indices = np.nonzero(arr)
print(indices)        # (array([1, 3, 4]),)
print(arr[indices])   # [2 4 5]
```

---

### **3. Sorting Arrays**

```python
arr = np.array([3, 1, 2])
print(np.sort(arr))    # [1 2 3]

arr2d = np.array([[3, 1, 2], [9, 8, 7]])
print(np.sort(arr2d, axis=1))  # Sort each row
```

**Argsort (indices of sorted order):**

```python
arr = np.array([3, 1, 2])
print(np.argsort(arr))  # [1 2 0]
```

---

### **4. Stacking Arrays**

**Vertical Stacking:**

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
np.vstack((a, b))
# [[1 2 3]
#  [4 5 6]]
```

**Horizontal Stacking:**

```python
np.hstack((a, b))  # [1 2 3 4 5 6]
```

**Column Stack (2D columns):**

```python
np.column_stack((a, b))
# [[1 4]
#  [2 5]
#  [3 6]]
```

---

### **5. Splitting Arrays**

**Split into equal parts:**

```python
arr = np.arange(10)
np.split(arr, 5)
# [array([0, 1]), array([2, 3]), array([4, 5]), array([6, 7]), array([8, 9])]
```

**Vertical Split:**

```python
arr2d = np.array([[1, 2, 3],
                  [4, 5, 6]])
np.vsplit(arr2d, 2)
# [array([[1, 2, 3]]), array([[4, 5, 6]])]
```

---

### **6. Unique & Set Operations**

```python
arr = np.array([1, 2, 2, 3, 4, 4])
np.unique(arr)                 # [1 2 3 4]
np.intersect1d([1, 2], [2, 3]) # [2]
np.union1d([1, 2], [2, 3])     # [1 2 3]
np.setdiff1d([1, 2], [2, 3])   # [1]
```
