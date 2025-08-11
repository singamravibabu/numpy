## **NumPy Cheatsheet — Part 1: Basics & Array Creation**

### **1. Importing NumPy**

```python
import numpy as np
```

---

### **2. Creating Arrays**

**From Python lists/tuples:**

```python
arr1 = np.array([1, 2, 3])         # 1D array
arr2 = np.array([[1, 2], [3, 4]])  # 2D array
arr3 = np.array((1, 2, 3, 4))      # From tuple
```

**Check type:**

```python
type(arr1)   # <class 'numpy.ndarray'>
```

---

### **3. Array Attributes**

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])

print(arr.shape)   # (2, 3) → 2 rows, 3 columns
print(arr.ndim)    # 2 → number of dimensions
print(arr.size)    # 6 → total elements
print(arr.dtype)   # int64 → data type
```

---

### **4. Creating Special Arrays**

**Zeros & Ones:**

```python
np.zeros((2, 3))     # [[0., 0., 0.], [0., 0., 0.]]
np.ones((2, 3))      # [[1., 1., 1.], [1., 1., 1.]]
```

**Filled with a constant:**

```python
np.full((2, 3), 7)   # [[7, 7, 7], [7, 7, 7]]
```

**Identity matrix:**

```python
np.eye(3)  # 3x3 identity
```

---

### **5. Creating Number Sequences**

**Using `arange` (like `range` but returns NumPy array):**

```python
np.arange(5)           # [0 1 2 3 4]
np.arange(1, 10, 2)    # [1 3 5 7 9]
```

**Using `linspace` (equally spaced numbers):**

```python
np.linspace(0, 1, 5)   # [0.   0.25 0.5  0.75 1.  ]
```

---

### **6. Random Arrays**

```python
np.random.rand(2, 3)       # Uniform [0, 1)
np.random.randn(2, 3)      # Normal distribution
np.random.randint(0, 10, (2, 3))  # Random ints 0–9
```

---

### **7. Changing Data Type**

```python
arr = np.array([1.2, 3.4, 5.6])
arr_int = arr.astype(int)   # [1, 3, 5]
```
