---
title: Predicting Titanic Survival Using Machine Learning
date: 2025-07-21
author: Your Name
cell_count: 23
score: 20
---

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report, accuracy_score
from sklearn.preprocessing import LabelEncoder
```


```python
df = sns.load_dataset('titanic')
print("Dataset Loaded. Shape:", df.shape)
```


```python
print("\nData Info:")
print(df.info())
```


```python
print("\nMissing Values:")
print(df.isnull().sum())
```


```python
df['age'].fillna(df['age'].median(), inplace=True)
df['embarked'].fillna(df['embarked'].mode()[0], inplace=True)
df.drop(columns=['deck'], inplace=True)
```


```python
df.drop(columns=['who', 'adult_male', 'alive', 'class'], inplace=True)
```


```python
label_encoders = {}
categorical_cols = ['sex', 'embarked', 'embark_town', 'alone']
```


```python
for col in categorical_cols:
    le = LabelEncoder()
    df[col] = le.fit_transform(df[col])
    label_encoders[col] = le
```


```python
sns.countplot(data=df, x='sex', hue='survived')
plt.title("Survival by Gender")
plt.show()
```


```python
sns.countplot(data=df, x='pclass', hue='survived')
plt.title("Survival by Class")
plt.show()
```


```python
sns.histplot(data=df, x='age', kde=True, hue='survived', bins=30)
plt.title("Age Distribution by Survival")
plt.show()
```


```python
plt.figure(figsize=(10, 6))
sns.heatmap(df.corr(numeric_only=True), annot=True, cmap='coolwarm')
plt.title("Feature Correlation")
plt.show()
```


```python
X = df.drop(columns=['survived'])
y = df['survived']
```


```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```


```python
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)
```


```python
y_pred = model.predict(X_test)
acc = accuracy_score(y_test, y_pred)
```


```python
print("\nModel Accuracy:", acc)
print("\nClassification Report:")
print(classification_report(y_test, y_pred))
```


```python
importances = pd.Series(model.feature_importances_, index=X.columns)
importances.sort_values().plot(kind='barh', title='Feature Importance')
plt.xlabel("Importance Score")
plt.show()
```


```python
print("Conclusion:")
print("- Model accuracy is around {:.2f}%.".format(acc * 100))
print("- 'Sex', 'Fare', and 'Pclass' were key predictors.")
print("- Better results could be achieved with hyperparameter tuning.")
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