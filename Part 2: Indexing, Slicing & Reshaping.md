## **NumPy Cheatsheet — Part 2: Indexing, Slicing & Reshaping**

---

### **1. Indexing (Accessing Elements)**

**1D Array:**

```python
arr = np.array([10, 20, 30, 40, 50])
print(arr[0])   # 10
print(arr[-1])  # 50 (last element)
```

**2D Array:**

```python
arr2d = np.array([[1, 2, 3],
                  [4, 5, 6],
                  [7, 8, 9]])
print(arr2d[0, 1])   # 2  → Row 0, Col 1
print(arr2d[2, -1])  # 9  → Row 2, Last Col
```

---

### **2. Slicing (Extracting Ranges)**

**1D Array:**

```python
print(arr[1:4])     # [20 30 40]
print(arr[:3])      # [10 20 30]
print(arr[::2])     # [10 30 50] → every 2nd element
```

**2D Array:**

```python
print(arr2d[0:2, 1:3])   # Rows 0-1, Cols 1-2 → [[2 3], [5 6]]
print(arr2d[:, 0])       # First column → [1 4 7]
```

---

### **3. Boolean Indexing**

```python
arr = np.array([1, 2, 3, 4, 5])
mask = arr > 3
print(mask)       # [False False False  True  True]
print(arr[mask])  # [4 5]
```

---

### **4. Fancy Indexing (Index by List/Array)**

```python
arr = np.array([10, 20, 30, 40, 50])
indices = [0, 3, 4]
print(arr[indices])  # [10 40 50]
```

**2D Example:**

```python
arr2d[[0, 2], [1, 2]]  # Picks (0,1) → 2 and (2,2) → 9 → [2 9]
```

---

### **5. Reshaping Arrays**

```python
arr = np.arange(1, 7)   # [1 2 3 4 5 6]
reshaped = arr.reshape((2, 3))
# [[1 2 3]
#  [4 5 6]]
```

---

### **6. Flattening Arrays**

```python
arr2d.flatten()   # Returns copy → [1 2 3 4 5 6]
arr2d.ravel()     # Returns view if possible
```

---

### **7. Adding/Removing Dimensions**

```python
arr = np.array([1, 2, 3])
arr_2d = arr[np.newaxis, :]  # Shape: (1, 3)
arr_2d_col = arr[:, np.newaxis]  # Shape: (3, 1)
```
