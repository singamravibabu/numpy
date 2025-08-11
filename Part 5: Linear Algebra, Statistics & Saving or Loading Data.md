## **NumPy Cheatsheet — Part 5: Linear Algebra, Statistics & Saving/Loading Data**

---

### **1. Matrix Multiplication**

```python
A = np.array([[1, 2],
              [3, 4]])
B = np.array([[5, 6],
              [7, 8]])

print(np.dot(A, B))
# [[19 22]
#  [43 50]]

# Or using @ operator
print(A @ B)
```

---

### **2. Transpose & Inverse**

```python
A = np.array([[1, 2, 3],
              [4, 5, 6]])

print(A.T)
# [[1 4]
#  [2 5]
#  [3 6]]

square_matrix = np.array([[1, 2],
                          [3, 4]])
print(np.linalg.inv(square_matrix))
# [[-2.   1. ]
#  [ 1.5 -0.5]]
```

---

### **3. Determinant**

```python
det = np.linalg.det(square_matrix)
print(det)  # -2.0
```

---

### **4. Eigenvalues & Eigenvectors**

```python
vals, vecs = np.linalg.eig(square_matrix)
print("Eigenvalues:", vals)
print("Eigenvectors:\n", vecs)
```

---

### **5. Norm (Vector Magnitude)**

```python
v = np.array([3, 4])
np.linalg.norm(v)  # 5.0
```

---

### **6. Statistics Recap**

```python
arr = np.array([1, 2, 3, 4, 5])
print(np.mean(arr))  # Average
print(np.median(arr))
print(np.std(arr))   # Standard deviation
print(np.var(arr))   # Variance
```

---

### **7. Saving & Loading Arrays**

**Save to `.npy` file:**

```python
arr = np.array([1, 2, 3])
np.save("my_array.npy", arr)
```

**Load from `.npy`:**

```python
loaded = np.load("my_array.npy")
```

**Save multiple arrays in one `.npz` file:**

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
np.savez("arrays.npz", array1=a, array2=b)
```

**Load `.npz`:**

```python
data = np.load("arrays.npz")
print(data["array1"])
print(data["array2"])
```

**Save/Load as text:**

```python
np.savetxt("data.txt", arr, delimiter=",")
loaded_txt = np.loadtxt("data.txt", delimiter=",")
```

---

### **8. Random Seed (Reproducibility)**

```python
np.random.seed(42)
print(np.random.rand(3))
```
