---
title: Untitled1
date: 2025-07-21
author: Your Name
cell_count: 121
score: 120
---

```python
import numpy as np
```


```python
print(np.array([1.5, 2.3, 3.7]).astype(int))
print(np.datetime64('today', 'D'))
print(np.arange('2025-01', '2026-01', dtype='datetime64[M]'))
print(np.diff(np.arange('2025-01', '2025-04', dtype='datetime64[M]')))
print(np.arange(1000000) * 2)
print(np.where(np.array([1, 2, 3]) > 2, 100, 0))
print(np.arange(10).view().base is np.arange(10))
```


```python
a = np.array([1, 2, 3])
b = a.view()
b[0] = 100
print(a)
```


```python
print(np.arange(1000000)[::100])
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
print(np.allclose(np.array([1.00001, 1.00002]), np.array([1.00002, 1.00001]), atol=1e-4))
```


```python
print(np.arange(12).reshape(3, 4).sum(axis=0))
```


```python
print(np.random.rand(5).argmax())
```


```python
print(np.sort(np.random.randint(1, 10, size=5)))
```


```python
print(np.linspace(0, 10, 5))
```


```python
print(np.dot(np.array([[1, 2], [3, 4]]), np.array([[5, 6], [7, 8]])))
```


```python
print(np.cumsum(np.array([1, 2, 3, 4, 5])))
```


```python
print(np.diff(np.array([1, 2, 3, 4, 5])))
```


```python
print(np.cross(np.array([1, 2, 3]), np.array([4, 5, 6])))

```


```python
print(np.median(np.array([1, 2, 3, 4, 5])))

```


```python
print(np.mean(np.array([1, 2, 3, 4, 5])))

```


```python
print(np.std(np.array([1, 2, 3, 4, 5])))

```


```python
print(np.var(np.array([1, 2, 3, 4, 5])))

```


```python
print(np.ptp(np.array([1, 2, 3, 4, 5])))

```


```python
print(np.percentile(np.array([1, 2, 3, 4, 5]), 50))

```


```python
print(np.unique(np.array([1, 2, 2, 3, 3, 3])))

```


```python
print(np.bincount(np.array([1, 2, 2, 3, 3, 3])))

```


```python
print(np.flip(np.array([1, 2, 3, 4, 5])))

```


```python
print(np.transpose(np.array([[1, 2], [3, 4]])))

```


```python
print(np.nonzero(np.array([1, 2, 3, 4, 5]) > 3))

```


```python
print(np.where(np.array([1, 2, 3, 4, 5]) % 2 == 0))

```


```python
print(np.clip(np.array([1, 2, 3, 4, 5]), 2, 4))

```


```python
print(np.round(np.array([1, 2, 3, 4, 5]) / 2))

```


```python
print(np.logical_and(np.array([True, False, True]), [False, False, True]))

```


```python
print(np.logical_or(np.array([True, False, True]), [False, False, True]))

```


```python
print(np.argmax(np.array([[1, 2, 3], [4, 5, 6]]), axis=1))

```


```python

print(np.argmin(np.array([[1, 2, 3], [4, 5, 6]]), axis=0))

```


```python
print(np.concatenate([np.array([1, 2, 3]), np.array([4, 5, 6])]))

```


```python
print(np.vstack([np.array([1, 2, 3]), np.array([4, 5, 6])]))

```


```python
print(np.hstack([np.array([1, 2, 3]), np.array([4, 5, 6])]))

```


```python
print(np.split(np.arange(10), 2))

```


```python
print(np.array_split(np.arange(10), 3))

```


```python
print(np.repeat(np.array([1, 2, 3]), 3))

```


```python
print(np.tile(np.array([1, 2, 3]), 3))

```


```python
print(np.roll(np.array([1, 2, 3, 4, 5]), 2))

```


```python
print(np.power(np.array([1, 2, 3]), 3))

```


```python
print(np.mod(np.array([10, 11, 12]), 5))

```


```python
print(np.remainder(np.array([10, 11, 12]), 5))

```


```python
print(np.remainder(np.array([10, 11, 12]), 5))

```


```python
print(np.sign(np.array([-3, 0, 3])))

```


```python
print(np.abs(np.array([-3, 0, 3])))

```


```python
print(np.sqrt(np.array([1, 4, 9, 16])))

```


```python
print(np.cbrt(np.array([1, 8, 27, 64])))

```


```python
print(np.exp(np.array([0, 1, 2])))

```


```python
print(np.log(np.array([1, np.e, np.e**2])))

```


```python
print(np.log10(np.array([1, 10, 100])))

```


```python
print(np.log2(np.array([1, 2, 4])))

```


```python
print(np.sin(np.array([0, np.pi/2, np.pi])))

```


```python
print(np.cos(np.array([0, np.pi/2, np.pi])))

```


```python
print(np.tan(np.array([0, np.pi/4, np.pi/2])))

```


```python
print(np.arcsin(np.array([0, 0.5, 1])))

```


```python
print(np.arccos(np.array([1, 0.5, 0])))

```


```python
print(np.arctan(np.array([0, 1, np.inf])))

```


```python
print(np.deg2rad(np.array([0, 90, 180])))

```


```python
print(np.rad2deg(np.array([0, np.pi/2, np.pi])))

```


```python
print(np.sinh(np.array([0, 1, 2])))

```


```python
print(np.cosh(np.array([0, 1, 2])))

```


```python
print(np.tanh(np.array([0, 1, 2])))

```


```python
print(np.arcsinh(np.array([0, 1, 2])))

```


```python
print(np.arccosh(np.array([1, 2, 3])))

```


```python
print(np.arctanh(np.array([0, 0.5, 0.9])))

```


```python
print(np.isnan(np.array([1, np.nan, 3])))

```


```python
print(np.isfinite(np.array([1, np.inf, 3])))

```


```python
print(np.isinf(np.array([1, np.inf, -np.inf])))

```


```python
print(np.round(np.array([1.2345, 2.3456]), decimals=2))

```


```python
print(np.fix(np.array([1.7, -1.7])))

```


```python
print(np.floor(np.array([1.7, -1.7])))

```


```python
print(np.ceil(np.array([1.7, -1.7])))

```


```python
print(np.trunc(np.array([1.7, -1.7])))

```


```python
print(np.rint(np.array([1.5, 2.5, 3.5])))

```


```python
print(np.maximum(np.array([1, 5, 3]), np.array([3, 2, 4])))

```


```python
print(np.minimum(np.array([1, 5, 3]), np.array([3, 2, 4])))

```


```python
print(np.gcd.reduce(np.array([24, 36, 18])))

```


```python
print(np.lcm.reduce(np.array([24, 36, 18])))

```


```python
print(np.mgrid[0:3, 0:3])

```


```python
print(np.ogrid[0:3, 0:3])

```


```python
print(np.meshgrid(np.array([1, 2, 3]), np.array([4, 5])))

```


```python
print(np.diag(np.array([1, 2, 3])))

```


```python
print(np.trace(np.array([[1, 2], [3, 4]])))

```


```python
print(np.linalg.det(np.array([[1, 2], [3, 4]])))

```


```python
print(np.linalg.inv(np.array([[1, 2], [3, 4]])))

```


```python
print(np.linalg.eigvals(np.array([[1, 2], [3, 4]])))

```


```python
print(np.linalg.norm(np.array([1, 2, 3])))

```


```python

print(np.linalg.solve(np.array([[3, 1], [1, 2]]), np.array([9, 8])))

```


```python
print(np.linalg.matrix_rank(np.array([[1, 2], [2, 4]])))

```


```python
print(np.linalg.svd(np.array([[1, 2], [3, 4]])))

```


```python
print(np.linalg.cholesky(np.array([[4, 1], [1, 3]])))

```


```python
print(np.linalg.qr(np.array([[1, 2], [3, 4]])))

```


```python
print(np.linalg.pinv(np.array([[1, 2], [3, 4]])))

```


```python
print(np.polynomial.polynomial.polyval(3, [1, 2, 3]))

```


```python
print(np.roots([1, -3, 2]))
print(np.correlate(np.array([1, 2, 3]), np.array([0, 1, 0.5])))
```


```python
print(np.convolve(np.array([1, 2, 3]), np.array([0, 1, 0.5])))

```


```python
print(np.fft.fft(np.array([1, 2, 3, 4])))

```


```python
print(np.fft.ifft(np.fft.fft(np.array([1, 2, 3, 4]))))

```


```python
print(np.gradient(np.array([1, 2, 4, 7, 11])))

```


```python
print(np.diff(np.array([1, 2, 4, 7, 11])))

```


```python
print(np.histogram(np.array([1, 2, 1, 3, 4, 2, 1]), bins=3))

```


```python
print(np.random.seed(0))

```


```python
print(np.random.rand())

```


```python
print(np.random.randint(0, 10, 5))

```


```python
print(np.random.normal(0, 1, 5))

```


```python
print(np.random.choice([1, 2, 3, 4], 3))

```


```python
print(np.random.shuffle(np.arange(5)))

```


```python
print(np.random.permutation(np.arange(5)))

```


```python
print(np.eye(3))

```


```python
print(np.identity(3))

```


```python
print(np.zeros((3, 3)))

```


```python
print(np.full((3, 3), 7))

```


```python
print(np.ones((3, 3)))
```


```python
print(np.empty((3, 3)))
```


```python
print(np.diag(np.arange(3)))
```


```python
print(np.tril(np.ones((3, 3))))
```


```python
print(np.meshgrid(np.linspace(0, 1, 3), np.linspace(0, 1, 3)))
```


```python
print(np.where(np.array([1, 2, 3, 4]) > 2))
```


```python
print(np.select([np.array([1, 2, 3, 4]) < 3
```


---
**Score: 120**