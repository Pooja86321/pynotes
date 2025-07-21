---
title: Np
date: 2025-07-21
author: Your Name
cell_count: 126
score: 125
---

```python
import numpy as np
```


```python
print(np.array([1.5, 2.3, 3.7]).astype(int))
print(np.datetime64('today', 'D'))
```


```python
print(np.arange(1000000) * 2)
print(np.where(np.array([1, 2, 3]) > 2, 100, 0))
```


```python
print(np.arange('2025-01', '2026-01', dtype='datetime64[M]'))
print(np.diff(np.arange('2025-01', '2025-04', dtype='datetime64[M]')))
```


```python
a = np.array([1, 2, 3])
b = a.view()
print(b.base is a)
print(a)
```


```python
print(np.arange(1000000)[::100])
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
print(np.arange(12).reshape(3, 4).sum(axis=0))
```


```python
print(np.random.rand(5).argmax())
print(np.sort(np.random.randint(1, 10, size=5)))
```


```python
print(np.linspace(0, 10, 5))
print(np.dot(np.array([[1, 2], [3, 4]]), np.array([[5, 6], [7, 8]])))
```


```python
print(np.cumsum(np.array([1, 2, 3, 4, 5])))
print(np.diff(np.array([1, 2, 3, 4, 5])))
```


```python
print(np.cross(np.array([1, 2, 3]), np.array([4, 5, 6])))
print(np.median(np.array([1, 2, 3, 4, 5])))
```


```python
print(np.mean(np.array([1, 2, 3, 4, 5])))
print(np.std(np.array([1, 2, 3, 4, 5])))
```


```python
print(np.var(np.array([1, 2, 3, 4, 5])))
print(np.ptp(np.array([1, 2, 3, 4, 5])))
```


```python
print(np.percentile(np.array([1, 2, 3, 4, 5]), 50))
print(np.unique(np.array([1, 2, 2, 3, 3, 3])))
```


```python
print(np.bincount(np.array([1, 2, 2, 3, 3, 3])))
print(np.flip(np.array([1, 2, 3, 4, 5])))
```


```python
print(np.mod(np.array([10, 11, 12]), 5))
print(np.remainder(np.array([10, 11, 12]), 5))
```


```python
print(np.roll(np.array([1, 2, 3, 4, 5]), 2))
print(np.power(np.array([1, 2, 3]), 3))
```


```python
print(np.repeat(np.array([1, 2, 3]), 3))
print(np.tile(np.array([1, 2, 3]), 3))
```


```python
print(np.split(np.arange(10), 2))
print(np.array_split(np.arange(10), 3))
```


```python
print(np.vstack([np.array([1, 2, 3]), np.array([4, 5, 6])]))
print(np.hstack([np.array([1, 2, 3]), np.array([4, 5, 6])]))
```


```python
print(np.intersect1d(np.arange(10), [5, 7, 9]))
print(np.concatenate([np.array([1, 2, 3]), np.array([4, 5, 6])]))
```


```python
print(np.argmax(np.array([[1, 2, 3], [4, 5, 6]]), axis=1))
print(np.argmin(np.array([[1, 2, 3], [4, 5, 6]]), axis=0))

```


```python
print(np.logical_and(np.array([True, False, True]), [False, False, True]))
print(np.logical_or(np.array([True, False, True]), [False, False, True]))
```


```python
print(np.clip(np.array([1, 2, 3, 4, 5]), 2, 4))
print(np.round(np.array([1, 2, 3, 4, 5]) / 2))
```


```python
print(np.nonzero(np.array([1, 2, 3, 4, 5]) > 3))
print(np.where(np.array([1, 2, 3, 4, 5]) % 2 == 0))
```


```python
print(np.transpose(np.array([[1, 2], [3, 4]])))
print(np.isin(np.array([1, 2, 3, 4, 5]), [2, 4]))
```


```python
print(np.floor(np.array([1.7, 2.8, 3.9])))
print(np.ceil(np.array([1.2, 2.3, 3.4])))
```


```python
print(np.log(np.array([1, np.e, np.e**2])))
print(np.log10(np.array([1, 10, 100])))
```


```python
print(np.trunc(np.array([1.7, 2.8, 3.9])))
print(np.rint(np.array([1.2, 2.3, 3.6])))
```


```python
print(np.sqrt(np.array([4, 9, 16])))
print(np.exp(np.array([1, 2, 3])))
```


```python
print(np.sin(np.array([0, np.pi / 2, np.pi])))
print(np.cos(np.array([0, np.pi / 2, np.pi])))
```


```python
print(np.tan(np.array([0, np.pi / 4, np.pi / 2])))
print(np.arcsin(np.array([0, 0.5, 1])))
```


```python
print(np.arccos(np.array([0, 0.5, 1])))
print(np.arctan(np.array([0, 1, np.inf])))
```


```python
print(np.degrees(np.array([0, np.pi / 2, np.pi])))
print(np.radians(np.array([0, 90, 180])))
```


```python
print(np.sign(np.array([-5, 0, 5])))
print(np.absolute(np.array([-1, -2, 3])))
```


```python
print(np.real(np.array([1+2j, 3+4j, 5+6j])))
print(np.imag(np.array([1+2j, 3+4j, 5+6j])))
```


```python
print(np.conj(np.array([1+2j, 3+4j, 5+6j])))
print(np.angle(np.array([1+1j, 1-1j, -1+1j])))
```


```python
print(np.linalg.norm(np.array([3, 4])))
print(np.linalg.inv(np.array([[1, 2], [3, 4]])))
```


```python
print(np.linalg.det(np.array([[1, 2], [3, 4]])))
print(np.trace(np.array([[1, 2], [3, 4]])))
```


```python
print(np.eye(3))
print(np.identity(3))
```


```python
print(np.ones((2, 3)))
print(np.zeros((2, 3)))
```


```python
print(np.pad(np.array([1, 2, 3]), (2, 3), mode='constant'))
print(np.diff(np.random.randint(0, 100, size=10)))
```


```python
print(np.random.shuffle(np.array([1, 2, 3, 4])))
print(np.random.seed(42))
```


```python
print(np.random.choice([10, 20, 30], size=5, replace=True))
print(np.random.permutation([1, 2, 3, 4]))
```


```python
print(np.random.randint(1, 100, size=5))
print(np.random.normal(0, 1, 5))
```


```python
print(np.fromiter(range(5), dtype=int))
print(np.linspace(0, 1, num=5, endpoint=False))
```


```python
print(np.maximum([1, 2, 3], [2, 1, 4]))
print(np.minimum([1, 2, 3], [2, 1, 4]))
```


```python
print(np.setdiff1d([1, 2, 3, 4], [2, 4]))
print(np.union1d([1, 2], [2, 3]))
```


```python
print(np.isfinite(np.array([1.0, np.nan, np.inf])))
print(np.isinf(np.array([1.0, np.inf, -np.inf])))
```


```python
print(np.count_nonzero(np.array([0, 1, 0, 2, 3])))
print(np.isnan(np.array([1.0, np.nan, 3.0])))
```


```python
print(np.full((2, 2), 7))
print(np.empty((2, 2)))
```


```python
print(np.cov(np.array([[1, 2, 3], [4, 5, 6]])))
print(np.corrcoef(np.array([1, 2, 3]), np.array([1, 2, 3])))
```


```python
print(np.histogram(np.array([1, 2, 1, 2, 3, 3, 3]), bins=3))
print(np.digitize(np.array([0.2, 6.4, 3.0, 1.6]), bins=[1, 2, 3, 4, 5]))
```


```python
print(np.meshgrid(np.arange(3), np.arange(3)))
print(np.mgrid[0:5, 0:5])
```


```python
print(np.ogrid[0:5, 0:5])
print(np.indices((2, 3)))
```


```python
print(np.expand_dims(np.array([1, 2]), axis=0))
print(np.squeeze(np.array([[1], [2], [3]])))
```


```python
print(np.swapaxes(np.array([[1, 2], [3, 4]]), 0, 1))
print(np.moveaxis(np.zeros((3, 4, 5)), 0, -1))
```


```python
print(np.atleast_2d(1))
print(np.atleast_3d(np.array([1, 2, 3])))
```


```python
print(np.hypot(3, 4))
print(np.heaviside([-1.5, 0.0, 2.0], 1.0))
```


```python
print(np.unwrap(np.array([0, np.pi, 2*np.pi])))
print(np.deg2rad([0, 90, 180]))
```


```python
print(np.rad2deg([0, np.pi/2, np.pi]))
print(np.fix(np.array([1.3, -1.7])))
```


```python
print(np.iscomplex(np.array([1, 2+3j])))
print(np.isreal(np.array([1, 2+3j])))
```


```python
print(np.nan_to_num(np.array([1.0, np.nan, np.inf])))
print(np.real_if_close([2. + 1e-15j, 2.1 + 1e-5j]))
```


```python
print(np.ma.masked_equal(np.array([1, 2, 3]), 2))
print(np.ma.masked_where(np.array([True, False, True]), np.array([1, 2, 3])))
```


```python
print(np.char.not_equal('test', 'best'))
print(np.char.isnumeric('12345'))
```


```python
print(np.char.zfill('42', 5))
print(np.char.equal('test', 'test'))
```


```python
print(np.char.rjust('5', 4, '0'))
print(np.char.ljust('5', 4, '0'))
```


```python
print(np.char.replace('Hello world', 'world', 'NumPy'))
print(np.char.find('Hello NumPy', 'NumPy'))
```


```python
print(np.char.split('a b c'))
print(np.char.strip(['a ', ' b', ' c ']))
```


```python
print(np.char.lower('HELLO'))
print(np.char.upper('hello'))
```


```python
print(np.char.center('title', 10, fillchar='-'))
print(np.char.capitalize('python'))
```


```python
print(np.char.add(['hello', 'world'], ['_', 'python']))
print(np.char.multiply('ha', 3))
```


```python
print(np.ma.max(np.ma.masked_equal(np.array([1, 2, 3]), 2)))
print(np.ma.min(np.ma.masked_equal(np.array([1, 2, 3]), 2)))
```


```python
print(np.ma.sum(np.ma.masked_equal(np.array([1, 2, 3]), 2)))
print(np.ma.mean(np.ma.masked_equal(np.array([1, 2, 3]), 2)))
```


```python
print(np.ma.compressed(np.ma.masked_equal(np.array([1, 2, 3]), 2)))
print(np.ma.count(np.ma.masked_equal(np.array([1, 2, 3]), 2)))
```


```python
print(np.char.isalpha('HelloWorld'))
print(np.char.isdecimal('123'))
```


```python
print(np.nanstd([1.0, 2.0, np.nan]))
print(np.nanvar([1.0, 2.0, np.nan]))
```


```python
print(np.nansum([1, 2, np.nan]))
print(np.nanmean([1.0, 2.0, np.nan]))
```


```python
print(np.nanmax([1, 2, np.nan]))
print(np.nanmin([1, 2, np.nan]))
```


```python
print(np.fmax([1, 2, np.nan], [3, np.nan, 1]))
print(np.fmin([1, 2, np.nan], [3, np.nan, 1]))
```


```python
print(np.timedelta64(60, 's') == np.timedelta64(1, 'm'))
print(np.timedelta64(1, 'h') > np.timedelta64(30, 'm'))
```


```python
print(np.array(['2025-07-21'], dtype='datetime64'))
print(np.array(['12:00'], dtype='datetime64[m]'))
```


```python
print(np.array(['2025-07-21'], dtype='datetime64'))
print(np.array(['12:00'], dtype='datetime64[m]'))
```


```python
print(np.timedelta64(5, 'D') + np.timedelta64(3, 'D'))
print(np.datetime64('2025-01-01') + np.timedelta64(10, 'D'))
```


```python
print(np.busday_offset('2025-01-01', 5))
print(np.datetime_as_string(np.datetime64('2025-07-21T15:00')))
```


```python
print(np.busday_count('2025-01', '2025-02'))
print(np.is_busday(['2025-01-01', '2025-01-04']))
```


```python
print(np.setxor1d([1, 2, 3], [2, 3, 4]))
print(np.sort_complex(np.array([1+2j, 3+1j, 2+3j])))
```


```python
print(np.array([1.5, 2.5, 3.5]).round())
print(np.array([-1.5, -2.5, -3.5]).round())
```


```python
print(np.unpackbits(np.array([240], dtype=np.uint8)))
print(np.packbits(np.array([1, 0, 1, 0, 1, 0, 1, 0], dtype=np.uint8)))
```


```python
print(np.left_shift([1, 2, 3], 1))
print(np.right_shift([2, 4, 8], 1))
```


```python
print(np.bitwise_or([1, 0, 1], [0, 0, 1]))
print(np.bitwise_xor([1, 0, 1], [0, 0, 1]))
```


```python
print(np.logical_not([True, False, True]))
print(np.bitwise_and([1, 0, 1], [0, 0, 1]))
```


```python
print(np.greater([1, 2, 3], [1, 1, 2]))
print(np.less_equal([1, 2, 3], [1, 2, 4]))
```


```python
print(np.isclose([1.0, 2.0], [1.0, 2.01], atol=0.05))
print(np.equal([1, 2, 3], [1, 2, 4]))
```


```python
print(np.fromfunction(lambda i, j: i + j, (3, 3), dtype=int))
print(np.fromiter((x*x for x in range(5)), dtype=int))
```


```python
print(np.char.title('numpy is awesome'))
print(np.char.strip('   strip spaces   '))
```


```python
print(np.char.rstrip('right space   '))
print(np.char.swapcase('Hello NumPy'))
```


```python
print(np.char.join('-', ['2025', '07', '21']))
print(np.char.lstrip('   left space'))
```


```python
print(np.char.count('banana', 'a'))
print(np.char.index('banana', 'a'))
```


```python
print(np.char.startswith('NumPy is cool', 'NumPy'))
print(np.char.endswith('NumPy is cool', 'cool'))
```


```python
print(np.ptp([1, 2, 7, 4]))
print(np.median([1, 3, 2, 4]))
```


```python
print(np.isneginf(np.array([-np.inf, 0, np.inf])))
print(np.isposinf(np.array([-np.inf, 0, np.inf])))
```


```python
print(np.invert(np.array([True, False, True])))
print(np.logical_xor([True, False], [False, False]))
```


```python
print(np.array([True, False, True]) & np.array([False, False, True]))
print(np.array([True, False, True]) | np.array([False, False, True]))
```


```python
print(np.copy([1, 2, 3]))
print(np.deepcopy(np.array([1, 2, 3])) if 'deepcopy' in globals() else "Requires import")
```


```python
print(np.ndim(np.array([[[1]]])))
print(np.itemsize * np.array([1, 2, 3]).nbytes // np.array([1, 2, 3]).size)
```


```python
print(np.shape(np.array([[1, 2], [3, 4]])))
print(np.size(np.array([[1, 2], [3, 4]])))
```


```python
print(np.array_equal([1, 2], [1, 2]))
print(np.array_equiv([1, 2], [[1, 2], [1, 2]]))
```


```python
print(np.cross([1, 0, 0], [0, 1, 0]))
print(np.tensordot([[1, 2], [3, 4]], [[5, 6], [7, 8]], axes=1))
```


```python
print(np.matmul([[1, 0], [0, 1]], [[4, 1], [2, 2]]))
print(np.vdot([1+2j, 3+4j], [5+6j, 7+8j]))
```


```python
print(np.inner([1, 2], [3, 4]))
print(np.dot([1, 2], [3, 4]))
```


```python
print(np.kron([[1, 2], [3, 4]], [[0, 5], [6, 7]]))
print(np.outer([1, 2], [3, 4]))
```


```python
print(np.triu(np.ones((3, 3))))
print(np.tril(np.ones((3, 3))))
```


```python
print(np.linalg.solve([[2, 1], [1, 3]], [8, 13]))
print(np.linalg.lstsq([[1, 1], [1, -1]], [2, 0], rcond=None)[0])
```


```python
print(np.linalg.eigvals([[1, -1], [1, 1]]))
print(np.linalg.eig([[1, -1], [1, 1]]))
```


```python
print(np.trace(np.eye(3)))
print(np.linalg.matrix_power([[2, 0], [0, 2]], 3))
```


```python
print(np.flipud([[1, 2], [3, 4]]))
print(np.rot90([[1, 2], [3, 4]]))
```


```python
print(np.flip([1, 2, 3]))
print(np.fliplr([[1, 2], [3, 4]]))
```


```python
print(np.tile([1, 2], 3))
print(np.roll([1, 2, 3, 4], 2))
```


```python
print(np.resize([1, 2], (2, 3)))
print(np.repeat([1, 2, 3], 2))
```


```python
print(np.percentile([1, 2, 3, 4, 5], 50))
print(np.quantile([1, 2, 3, 4, 5], 0.75))
```


```python
print(np.bincount([1, 1, 2, 2, 2, 3]))
print(np.histogram_bin_edges([1, 2, 1, 3, 4, 5]))

```


```python
print(np.trim_zeros([0, 0, 1, 2, 0, 0]))
print(np.unique([1, 2, 2, 3, 3, 3]))
```


```python
print(np.diff([1, 2, 4, 7]))
print(np.ediff1d([1, 2, 4, 7]))
```


```python
print(np.cumsum([1, 2, 3]))
print(np.cumprod([1, 2, 3, 4]))

```


---
**Score: 125**