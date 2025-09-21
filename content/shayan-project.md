+++
title = 'Shayan Project'
date = 2025-09-21T14:42:25+02:00
draft = false
+++

Hello, your compute has virus






```python

import matplotlib.pyplot as plt

xi = [0, 1, 2, 3, 4, 5, 6, 7]
yi = [1.86, 5.63, 12.42, 17.58, 21.15, 28.49, 33.48, 37.26]
a = b = loss = dloss_a = dloss_b = 0
learning_rate = 0.001
loss_history = []

for _ in range(500):
    loss =dloss_a=dloss_b= 0
    for i in range(len(xi)):
        y = a * xi[i] + b
        loss = loss + (yi[i] - y) ** 2
        dloss_a += -2 * xi[i] * (yi[i] - y)
        dloss_b += -2 * (yi[i] - y)
    a = a - learning_rate * dloss_a
    b = b - learning_rate * dloss_b
    loss_history.append(loss)
print(a, b)

plt.plot(range(500), loss_history, label='Loss')
plt.xlabel('Iteration')
plt.ylabel('Loss')
plt.title('Loss vs. Iteration')
plt.legend()
plt.grid(True)
plt.show()


```