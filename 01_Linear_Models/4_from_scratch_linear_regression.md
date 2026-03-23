# From Scratch: Linear Regression in 25 Lines

This exercise makes optimization concrete.
Do not skip it.

---

## Toy Dataset

Suppose:

`x = [1, 2, 3, 4]`

`y = [3, 5, 7, 9]`

The true pattern is close to:

`y = 2x + 1`

---

## Step-by-Step Plan

1. Initialize `w` and `b` (for example `0.0`).
2. Predict: `y_hat = w*x + b`
3. Compute MSE loss.
4. Compute gradients:
   - `dL/dw = (2/n) * sum((y_hat - y) * x)`
   - `dL/db = (2/n) * sum(y_hat - y)`
5. Update:
   - `w = w - alpha * dL/dw`
   - `b = b - alpha * dL/db`
6. Repeat for many epochs.

---

## Minimal Python Implementation

```python
x = [1.0, 2.0, 3.0, 4.0]
y = [3.0, 5.0, 7.0, 9.0]

w, b = 0.0, 0.0
alpha = 0.01
epochs = 2000
n = len(x)

for epoch in range(epochs):
    y_hat = [w * xi + b for xi in x]
    errors = [yh - yi for yh, yi in zip(y_hat, y)]
    loss = sum(e * e for e in errors) / n

    dw = (2 / n) * sum(e * xi for e, xi in zip(errors, x))
    db = (2 / n) * sum(errors)

    w -= alpha * dw
    b -= alpha * db

print("w =", round(w, 3), "b =", round(b, 3), "loss =", round(loss, 6))
```

Expected result:
- `w` close to `2`
- `b` close to `1`
- very small final loss

---

## What You Should Notice

1. No "magic" happened.
2. The model improved only because loss gave a direction.
3. Better features matter as much as better optimization.

---

## Stretch Exercises

1. Change learning rate to `0.1`, then `0.0001`. Compare behavior.
2. Add one outlier point (for example `x=10, y=100`) and compare MSE sensitivity.
3. Replace MSE with MAE and observe update smoothness.
