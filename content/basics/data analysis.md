---
title: Data Analysis
date: 2025-07-21
author: Your Name
cell_count: 20
score: 20
---

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```


```python
# Step 1: Load the dataset
# Assuming CSV contains columns like: Date, Store_ID, Product_ID, Sales, Quantity, Price
df = pd.read_csv('retail_sales.csv', parse_dates=['Date'])
```


```python
# Step 2: Inspect the data
print(df.head())
print(df.info())
print(df.describe())
```


```python
# Step 3: Clean the data
# Drop rows with missing values
df.dropna(inplace=True)
```


```python
# Fix data types if necessary
df['Store_ID'] = df['Store_ID'].astype(str)
df['Product_ID'] = df['Product_ID'].astype(str)
```


```python
# Remove negative sales or quantities
df = df[(df['Sales'] >= 0) & (df['Quantity'] > 0)]
```


```python
# Step 4: Feature engineering
# Add a 'Month' column
df['Month'] = df['Date'].dt.to_period('M')
```


```python
# Calculate revenue (in case Sales and Price are different)
df['Revenue'] = df['Quantity'] * df['Price']
```


```python
# Step 5: Analyze total revenue per month
monthly_revenue = df.groupby('Month')['Revenue'].sum().reset_index()
```


```python
# Step 6: Top 5 selling products by revenue
top_products = df.groupby('Product_ID')['Revenue'].sum().nlargest(5).reset_index()
```


```python
# Step 7: Revenue by store
store_revenue = df.groupby('Store_ID')['Revenue'].sum().sort_values(ascending=False).reset_index()
```


```python
# Monthly Revenue Trend
plt.figure(figsize=(10,6))
sns.lineplot(data=monthly_revenue, x='Month', y='Revenue', marker='o')
plt.title('Monthly Revenue Trend')
plt.xlabel('Month')
plt.ylabel('Revenue')
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
```


```python
# Top Products by Revenue
plt.figure(figsize=(8,6))
sns.barplot(data=top_products, x='Product_ID', y='Revenue', palette='viridis')
plt.title('Top 5 Products by Revenue')
plt.xlabel('Product ID')
plt.ylabel('Revenue')
plt.tight_layout()
plt.show()
```


```python
# Revenue by Store
plt.figure(figsize=(12,6))
sns.barplot(data=store_revenue, x='Store_ID', y='Revenue', palette='coolwarm')
plt.title('Revenue by Store')
plt.xlabel('Store ID')
plt.ylabel('Revenue')
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()

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
**Score: 20**