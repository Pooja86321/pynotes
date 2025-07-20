---
title: Test
date: 2025-07-21
author: Your Name
cell_count: 16
score: 15
---

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

new code added


```python
df = pd.read_csv(r'C:\Users\HP\Desktop\amazon_products.csv')
df
```


```python
df.info()
```


```python
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 10 entries, 0 to 9
Data columns (total 4 columns):
 #   Column   Non-Null Count  Dtype  
---  ------   --------------  -----  
 0   Product  10 non-null     object 
 1   Price    10 non-null     int64  
 2   Rating   10 non-null     float64
 3   Reviews  10 non-null     int64  
dtypes: float64(1), int64(2), object(1)
memory usage: 452.0+ byte
```


```python
df.describe()
```


```python
deals = df[df["Price"] <= 1000].sort_values("Price")
deals
```


```python
top_reviews = df.sort_values("Reviews", ascending=False).head(5)
top_reviews
```


```python
plt.figure(figsize=(10,6))
sns.scatterplot(data=df, x="Rating", y="Price", size="Reviews", hue="Product", legend=False)
plt.title("Product Price vs Rating")
plt.xlabel("Rating")
plt.ylabel("Price")
plt.grid(True)
plt.show()
```


```python
sns.scatterplot(data=df, x="Rating", y="Price", size="Reviews", hue="Product", legend=False)
plt.title("Product Price vs Rating")
plt.xlabel("Rating")
plt.ylabel("Price")
plt.grid(True)
plt.show()
```


```python
plt.figure(figsize=(8,5))
sns.histplot(df["Rating"], bins=5, kde=True, color='skyblue')
plt.title("Distribution of Product Ratings")
plt.xlabel("Rating")
plt.ylabel("Number of Products")
plt.grid(True)
plt.show()
```


```python
df["Price_per_rating"] = df["Price"] / df["Rating"]
df.sort_values("Price_per_rating")
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
**Score: 15**