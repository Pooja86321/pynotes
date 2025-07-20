---
title: Increase Score
date: 2025-07-21
author: Your Name
cell_count: 9
score: 5
---

```python
import matplotlib.pyplot as plt
```


```python
score = 0
```


```python
def increase_score(current_score, increment=1):
    return current_score + increment
```


```python
increments = [5, 10, 15, 20]  # Example increments
scores = [score]  # List to track scores over time
```


```python
for inc in increments:
    score = increase_score(score, inc)
    scores.append(score)
```


```python
print(f"Final Score: {score}")
```


```python
plt.plot(range(len(scores)), scores, marker='o', linestyle='-', color='b')
plt.title("Score Progression")
plt.xlabel("Step")
plt.ylabel("Score")
plt.grid()
plt.show()
```


```python

```


```python

```


---
**Score: 5**