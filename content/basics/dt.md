---
title: Dt
date: 2025-07-21
author: Your Name
cell_count: 184
score: 180
---

```python
import numpy as np
a = np.array([1, 2, 3])
print(a)
```


```python
b = np.array([[1, 2], [3, 4]])
print(b)
```


```python
c = np.zeros((2, 3))
print(c)
```


```python
d = np.ones((3, 3))
print(d)
```


```python
e = np.full((2, 2), 7)
print(e)
```


```python
f = np.eye(4)
print(f)
```


```python
g = np.random.rand(2, 3)
print(g)
```


```python
h = np.random.randint(0, 10, (3, 3))
print(h)
```


```python
i = np.arange(0, 10, 2)
print(i)
```


```python
j = np.linspace(0, 1, 5)
print(j)
```


```python
print(a.shape)
```


```python
print(b.ndim)
```


```python
print(c.size)
```


```python
print(d.dtype)
```


```python
reshaped = np.reshape(h, (1, 9))
print(reshaped)
```


```python
print(h.flatten())
```


```python
print(h.flatten())
```


```python
float_arr = a.astype(float)
print(float_arr)
```


```python
print(a.nbytes)
```


```python
view = h.view()
print(view)
```


```python
print(a[1])
```


```python
print(a[1:3])
```


```python
print(b[0:2, 1])
```


```python
print(a[a > 1])
```


```python
print(a[[0, 2]])
```


```python
a[0] = 10
print(a)
```


```python
a[a > 5] = 0
print(a)
```


```python
print(b[1])
```


```python
print(b[:, 0])
```


```python
print(np.arange(10)[::2])
```


```python
x = np.array([1, 2, 3])
y = np.array([4, 5, 6])
print(x + y)
```


```python
print(x - y)
```


```python
print(x * y)
```


```python
print(y / x)
```


```python
print(x ** 2)
```


```python
print(np.dot(x, y))
```


```python
mat1 = np.array([[1, 2], [3, 4]])
mat2 = np.array([[2, 0], [1, 2]])
print(np.matmul(mat1, mat2))
```


```python
print(np.sum(mat1))
```


```python
print(np.mean(x))
```


```python
print(np.std(x))
```


```python
arr = np.array([1, 2, 3])
```


```python
print(arr + 5)
```


```python
print(arr * 3)
```


```python
mat = np.array([[1, 2, 3], [4, 5, 6]])
print(mat + arr)
```


```python
print(np.sqrt(arr))
```


```python
print(np.exp(arr))
```


```python
print(np.log(arr + 1))  
```


```python
print(np.sin(arr))
```


```python
print(np.cos(arr))
```


```python
print(np.abs([-1, -2, 3]))
```


```python
print(np.round([1.4, 2.6, 3.1]))
```


```python
print(np.min(mat))
```


```python
print(np.max(mat))
```


```python
print(np.argmin(mat))
```


```python
print(np.argmax(mat))
```


```python
print(np.sum(mat, axis=0))
```


```python
print(np.sum(mat, axis=0))
```


```python
print(np.mean(mat, axis=1))
```


```python
print(np.cumsum(arr))
```


```python
print(np.cumprod(arr))
```


```python
print(np.median(mat))
```


```python
square = np.array([[1, 2], [3, 4]])
print(np.linalg.det(square))
```


```python
print(np.linalg.inv(square))
```


```python
print(np.linalg.matrix_rank(square))
```


```python
eig_vals, eig_vecs = np.linalg.eig(square)
print(eig_vals)
```


```python
print(eig_vecs)
```


```python
A = np.array([[3, 1], [1, 2]])
b = np.array([9, 8])
x = np.linalg.solve(A, b)
print(x)
```


```python
v = np.array([3, 4])
print(np.linalg.norm(v))
```


```python
print(np.trace(square))
```


```python
q, r = np.linalg.qr(square)
print(q)
```


```python
u, s, vh = np.linalg.svd(square)
print(s)
```


```python
print(np.any(arr > 2))
```


```python
print(np.all(arr > 0))
```


```python
x = np.array([True, False, True])
y = np.array([False, False, True])
print(np.logical_and(x, y))
```


```python
print(np.logical_or(x, y))
```


```python
print(np.logical_not(x))
```


```python
z = np.array([1, 2, 3])
print(np.where(z > 1, 'yes', 'no'))
```


```python
print(np.count_nonzero([0, 1, 2, 0]))
```


```python
a = np.array([1, 1, 2, 3, 3])
print(np.unique(a))
```


```python
print(np.array_equal([1, 2], [1, 2]))
```


```python
print(np.greater([1, 3, 5], [2, 3, 1]))
```


```python
a = np.array([3, 1, 2])
print(np.sort(a))
```


```python
b = np.array([[3, 1], [2, 4]])
print(np.sort(b, axis=1))
```


```python
print(np.argsort(a))
```


```python
c = np.array([1, 3, 5])
print(np.searchsorted(c, 4))
```


```python
print(np.partition(a, 1))
```


```python
print(np.argmax(b, axis=0))
```


```python
print(np.argmin(b, axis=1))
```


```python
arr = np.array([1, 5, 10])
print(np.clip(arr, 2, 8))
```


```python
print(np.argsort([4, 1, 3]))
```


```python
x = np.array([1, 2, 3, 4])
print(np.where(x > 2))
```


```python
np.save('array.npy', x)
loaded = np.load('array.npy')
print(loaded)
```


```python
np.savez('arrays.npz', a=x, b=arr)
data = np.load('arrays.npz')
print(data['a'], data['b'])
```


```python
np.savetxt('array.txt', x)
x2 = np.loadtxt('array.txt')
print(x2)
```


```python
np.savetxt('custom.txt', x, delimiter=',')
x3 = np.loadtxt('custom.txt', delimiter=',')
print(x3)
```


```python
np.savetxt('ints.csv', np.array([[1,2],[3,4]]), fmt='%d', delimiter=',')
ints = np.loadtxt('ints.csv', delimiter=',')
print(ints)
```


```python
arr = np.arange(6)
print(arr.reshape(2, 3))
```


```python
print(np.expand_dims(arr, axis=0))
```


```python
a = np.array([[[1, 2, 3]]])
print(np.squeeze(a))
```


```python
a = np.array([1, 2])
b = np.array([3, 4])
print(np.vstack((a, b)))
```


```python
print(np.hstack((a, b)))
```


```python
print(np.dstack((a, b)))
```


```python
print(np.concatenate(([a], [b]), axis=0))
```


```python
c = np.array([1, 2, 3, 4])
print(np.split(c, 2))
```


```python
d = np.array([[1, 2], [3, 4]])
print(np.vsplit(d, 2))
```


```python
print(np.hsplit(d, 2))
```


```python
print(np.random.randint(0, 100, 5))
```


```python
print(np.random.random(5))
```


```python
print(np.random.normal(0, 1, 5))
```


```python
print(np.random.choice([10, 20, 30]))
```


```python
arr = np.array([1, 2, 3, 4])
np.random.shuffle(arr)
print(arr)
```


```python
print(np.random.permutation([1, 2, 3, 4]))
```


```python
np.random.seed(42)
print(np.random.rand())
```


```python
print(np.random.rand(2, 3))
```


```python
print(np.random.uniform(low=0, high=10, size=5))
```


```python
print(np.random.binomial(n=10, p=0.5, size=5))
```


```python
a = np.array([1.8, 2.5, 3.1])
print(np.floor(a))
```


```python
print(np.ceil(a))
```


```python
print(np.trunc(a))
```


```python
x = np.array([10, 20, 30])
y = np.array([3, 7, 9])
print(np.mod(x, y))
```


```python
print(np.remainder(x, y))
```


```python
print(np.gcd(12, 18))
```


```python
print(np.lcm(6, 8))
```


```python
print(np.power(2, 3))
```


```python
print(np.sign([-10, 0, 10]))
```


```python
print(np.reciprocal([1, 2, 0.5]))
```


```python
arr = np.array([1, np.nan, 3])
print(np.isnan(arr))
```


```python
arr2 = np.array([1, np.inf, -np.inf])
print(np.isinf(arr2))
```


```python
arr[np.isnan(arr)] = 0
print(arr)
```


```python
arr2[np.isinf(arr2)] = 9999
print(arr2)
```


```python
arr3 = np.array([1, 2, np.nan])
print(np.nansum(arr3))
```


```python
print(np.nanmean(arr3))
```


```python
print(np.nanmax(arr3))
```


```python
print(np.nanmin(arr3))
```


```python
m = np.array([[1, np.nan], [3, 4]])
col_means = np.nanmean(m, axis=0)
inds = np.where(np.isnan(m))
m[inds] = np.take(col_means, inds[1])
print(m)
```


```python
arr = np.array([1, np.nan, 2, np.nan])
print(np.isnan(arr).sum())
```


```python
print(np.bitwise_and(5, 3)) 
```


```python
print(np.bitwise_or(5, 3))
```


```python
print(np.bitwise_xor(5, 3))
```


```python
print(np.left_shift(1, 2))
```


```python
print(np.right_shift(4, 1))
```


```python
print(np.binary_repr(10, width=8))
```


```python
x = np.array([True, False])
y = np.array([False, True])
print(np.logical_xor(x, y))
```


```python
bools = np.array([True, False])
print(bools.astype(int))
```


```python
ints = np.array([0, 1, 2])
print(ints.astype(bool))
```


```python
a = np.array([[1, 2], [3, 4]])
print(a.T)
```


```python
print(np.dot(a, a))
```


```python
print(np.linalg.matrix_power(a, 2))
```


```python
print(np.identity(3))
```


```python
print(np.diag(a))
```


```python
d = np.array([1, 2, 3])
print(np.diag(d))
```


```python
print(np.triu(a))
```


```python
print(np.tril(a))
```


```python
b = np.zeros((3, 3))
np.fill_diagonal(b, 1)
print(b)
```


```python
c = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(np.diag(c, k=1))
```


```python
a = np.array([1, 2, 3, 4])
print(np.fft.fft(a))
```


```python
f = np.fft.fft(a)
print(np.fft.ifft(f))
```


```python
print(np.fft.fftfreq(4))
```


```python
img = np.array([[1, 2], [3, 4]])
print(np.fft.fft2(img))
```


```python
f2 = np.fft.fft2(img)
print(np.fft.ifft2(f2))
```


```python
print(np.fft.fftshift(f2))
```


```python
print(np.fft.ifftshift(f2))
```


```python
f = np.fft.fft(a)
power = np.abs(f)**2
print(power)
```


```python
phase = np.angle(f)
print(phase)
```


```python
print(np.fft.rfft(a))
```


```python
a = np.array([1, 2, 2, 3])
```


```python
print(np.unique(a))
```


```python
b = np.array([2, 3, 4])
print(np.intersect1d(a, b))
```


```python
print(np.union1d(a, b))
```


```python
print(np.setdiff1d(a, b))
```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


---
**Score: 180**