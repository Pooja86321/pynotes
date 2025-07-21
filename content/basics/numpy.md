---
title: Numpy
date: 2025-07-21
author: Your Name
cell_count: 237
score: 235
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
print(np.setxor1d(a, b))
```


```python
unique, counts = np.unique(a, return_counts=True)
print(dict(zip(unique, counts)))
```


```python
print(set(a) == set(b))
```


```python
print(np.asarray(list(set(a))))
```


```python
arr2d = np.array([[1, 2], [1, 2], [3, 4]])
print(np.unique(arr2d, axis=0))
```


```python
data = np.random.randint(0, 10, 100)
hist, bins = np.histogram(data, bins=5)
print(hist)
print(bins)
```


```python
print(np.digitize([1, 2, 6], bins=[0, 3, 6]))
```


```python
print(np.histogram(data, bins=[0, 3, 6, 10]))
(array([30, 21, 49]), array([ 0,  3,  6, 10]))
hist, bins = np.histogram(data, bins=5, density=True)
print(hist)
```


```python
hist, bihist, bins = np.histogram(data, bins=5)
cumsum = np.cumsum(hist)
```


```python
print(cumsum)ns = np.histogram(data, bins=5)
cumsum = np.cumsum(hist)
```


```python
print(cumsum)hist, bins = np.histogram(data, bins=5)
cumsum = np.cumsum(hist)
print(cumsum)
```


```python
x = np.random.rand(100)
y = np.random.rand(100)
H, xedges, yedges = np.histogram2d(x, y, bins=5)
print(H)
```


```python
print(hist.flatten())
```


```python
values = np.array([0, 1, 1, 3, 4, 4, 4])
print(np.bincount(values))
```


```python
weights = np.ones_like(values)
print(np.bincount(values, weights=weights))
```


```python
bins = [0, 1, 2, 3, 4, 5]
print(np.digitize([0.5, 2.2, 3.9], bins))
```


```python
x = np.array([1, 2, 3])
y = np.array([4, 5])
X, Y = np.meshgrid(x, y)
print(X)
print(Y)
```


```python
X, Y = np.meshgrid(np.linspace(-1, 1, 5), np.linspace(-1, 1, 5))
Z = X**2 + Y**2
print(Z)
```


```python
i, j = np.indices((2, 3))
print(i)
print(j)
```


```python
og = np.ogrid[0:3, 0:2]
print(og[0])
print(og[1])
```


```python
mg = np.mgrid[0:3, 0:2]
print(mg)
```


```python
x = np.linspace(0, 1, 3)
y = np.linspace(0, 1, 3)
z = np.linspace(0, 1, 3)
X, Y, Z = np.meshgrid(x, y, z)
print(X.shape)
```


```python
xi, yi = np.meshgrid([1, 2], [3, 4], indexing='ij')
print(xi)
print(yi)
```


```python
x = [1, 2]
y = [3, 4]
X, Y = np.meshgrid(x, y)
print(np.array([X.ravel(), Y.ravel()]).T)
```


```python
r = np.linspace(0, 1, 5)
theta = np.linspace(0, 2 * np.pi, 5)
R, T = np.meshgrid(r, theta)
print(R)
print(T)
```


```python
phi = np.linspace(0, np.pi, 3)
theta = np.linspace(0, 2 * np.pi, 4)
PHI, THETA = np.meshgrid(phi, theta)
print(PHI)
print(THETA)
```


```python
dt = np.dtype([('name', 'U10'), ('age', 'i4')])
people = np.array([('Alice', 25), ('Bob', 30)], dtype=dt)
print(people)
```


```python
print(people['name'])
```


```python
sorted_people = np.sort(people, order='age')
print(sorted_people)
```


```python
print(people[people['age'] > 25])
```


```python
print(people[people['age'] > 25])
```


```python
new = np.array([('Charlie', 22)], dtype=dt)
people = np.concatenate((people, new))
print(people)
```


```python
dt_nested = np.dtype([('coords', [('x', 'f4'), ('y', 'f4')]), ('value', 'i4')])
data = np.array([((1.0, 2.0), 10)], dtype=dt_nested)
print(data)
```


```python
print(people[['name', 'age']])
```


```python
import numpy.ma as ma
data = ma.array([1, 2, 3], mask=[0, 1, 0])
print(data)
```


```python
print(data.mask)
```


```python
print(data.mean())
```


```python
print(data.filled(-1))
```


```python
masked = ma.masked_equal([1, -99, 3], -99)
print(masked)
```


```python
x = np.array([1, 2, 3, 4])
masked = ma.masked_where(x > 2, x)
print(masked)
```


```python
a = ma.masked_less([1, 2, 3], 2)
b = ma.masked_greater([1, 2, 3], 2)
combined = ma.mask_or(a.mask, b.mask)
print(combined)
```


```python
print(data.compressed())
```


```python
print(ma.std(masked))
```


```python
matrix = np.array([[1, 2], [3, 4]])
row = np.array([10, 20])
print(matrix + row)
```


```python
col = np.array([[1], [2]])
print(matrix - col)
```


```python
a = np.array([1, 2])
b = np.array([3, 4])
print(np.outer(a, b))
```


```python
arr = np.array([1, 2, 3])
print(arr[:, None] + arr)
```


```python
m = np.array([[1, 2], [3, 4]])
norms = np.linalg.norm(m, axis=1, keepdims=True)
print(m / norms)
```


```python
x = np.array([1, 2, 3])
y = 2
print(x == y)
```


```python
a = np.ones((3, 3))
b = np.array([1, 2, 3])
print(a * b[:, np.newaxis])
```


```python
dates = np.array(['2025-06-01', '2025-06-10'], dtype='datetime64[D]')
print(dates)
```


```python
print(np.arange('2025-01', '2025-04', dtype='datetime64[M]'))
```


```python
print(dates + np.timedelta64(5, 'D'))
```


```python
print(dates[1] - dates[0])
```


```python
9 days
```


```python
delta = np.array(['2025-06-10'], dtype='datetime64[D]') - np.array(['2025-06-01'], dtype='datetime64[D]')
print(delta.astype(int))
```


```python
print(np.datetime64('today', 'D'))
2025-06-29
print(np.arange('2025-01', '2026-01', dtype='datetime64[M]'))
```


```python
months = np.arange('2025-01', '2025-04', dtype='datetime64[M]')
print(np.diff(months))
```


```python
x = np.arange(1000000)
print(x * 2)
```


```python
arr = np.array([1, 2, 3])
print(np.where(arr > 2, 100, 0))
```


```python
arr = np.arange(10)
view = arr.view()
print(view.base is arr) 
```


```python
a = np.array([1, 2, 3])
b = a.view()
b[0] = 100
print(a)
```


```python
x = np.arange(1000000)
print(x[::100])
```


```python
x = np.array([1, 2, 3])
x *= 2
print(x)
```


```python
x = np.array([1.0, 2.0, 3.0])
y = np.empty_like(x)
np.add(x, x, out=y)
print(y)
```


```python
a = np.array([1.00001, 1.00002])
b = np.array([1.00002, 1.00001])
print(np.allclose(a, b, atol=1e-4))
```


```python

```


---
**Score: 235**