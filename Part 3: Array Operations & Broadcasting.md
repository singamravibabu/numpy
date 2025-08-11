## **NumPy Cheatsheet — Part 3: Array Operations & Broadcasting**

---

### **1. Element-wise Arithmetic**

**Between arrays:**

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

print(a + b)  # [5 7 9]
print(a - b)  # [-3 -3 -3]
print(a * b)  # [ 4 10 18]
print(a / b)  # [0.25 0.4  0.5 ]
print(a ** 2) # [1 4 9]
```

**With scalars:**

```python
print(a + 10)   # [11 12 13]
print(a * 2)    # [2 4 6]
```

---

### **2. Universal Functions (ufuncs)**

NumPy has **vectorized math functions** that apply element-wise:

```python
arr = np.array([1, 4, 9, 16])
np.sqrt(arr)     # [1. 2. 3. 4.]
np.exp(arr)      # e^arr
np.log(arr)      # natural log
np.sin(arr)      # sine
np.cos(arr)      # cosine
```

---

### **3. Aggregation Functions**

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])

print(arr.sum())          # 21 → sum of all
print(arr.sum(axis=0))    # [5 7 9] → column sums
print(arr.sum(axis=1))    # [6 15]  → row sums

print(arr.mean())         # 3.5
print(arr.min())          # 1
print(arr.max())          # 6
print(arr.std())          # Standard deviation
```

---

### **4. Broadcasting (Different Shapes)**

Broadcasting lets NumPy do arithmetic between arrays of different shapes.

```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

add_vector = np.array([10, 20, 30])

print(arr + add_vector)
# [[11 22 33]
#  [14 25 36]]
```

Even scalar + array works because scalars are treated as having shape `(1,)`.

---

### **5. Comparison Operators**

```python
arr = np.array([1, 2, 3, 4])
print(arr > 2)       # [False False  True  True]
print(arr == 3)      # [False False  True  False]
```

**Any & All:**

```python
print(np.any(arr > 3))  # True
print(np.all(arr > 0))  # True
```

---

### **6. Clipping Values**

```python
arr = np.array([1, 5, 8, 10])
np.clip(arr, 3, 8)  # [3 5 8 8]
```
