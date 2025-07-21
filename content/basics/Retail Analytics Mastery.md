---
title: Retail Analytics Mastery
date: 2025-07-21
author: Your Name
cell_count: 20
score: 20
---

```python
import pandas as pd
```


```python
import numpy as np
```


```python
import matplotlib.pyplot as plt
```


```python
import seaborn as sns
```


```python
from sklearn.model_selection import train_test_split
```


```python
from sklearn.ensemble import RandomForestRegressor
```


```python
from sklearn.metrics import mean_squared_error, r2_score
```


```python
from sklearn.cluster import KMeans
```


```python
from sklearn.preprocessing import StandardScaler
```


```python
import statsmodels.api as sm
```


```python
from statsmodels.tsa.seasonal import seasonal_decompose
```


```python
from statsmodels.tsa.holtwinters import ExponentialSmoothing
```


```python
import warnings
warnings.filterwarnings('ignore')
sns.set(style='whitegrid')
```


```python
np.random.seed(42)
dates = pd.date_range(start='2023-01-01', periods=730, freq='D')
```


```python
n = len(dates)
```


```python
df = pd.DataFrame({
    'Date': dates,
    'CustomerID': np.random.randint(1000, 1100, n),
    'Region': np.random.choice(['North','South','East','West'],n),
    'Category': np.random.choice(['Electronics','Furniture','Clothing'],n),
    'Quantity': np.random.randint(1,15,n),
    'UnitPrice': np.round(np.random.uniform(5,500,n),2)
})
```


```python
df['Total'] = df['Quantity'] * df['UnitPrice']
```


```python
df['Month'] = df['Date'].dt.month
df['WeekOfYear'] = df['Date'].dt.isocalendar().week
df['DayOfWeek'] = df['Date'].dt.day_name()
```


```python

```


```python

```


---
**Score: 20**