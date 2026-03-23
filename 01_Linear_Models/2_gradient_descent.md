# Gradient Descent: How Parameters Improve

Once loss is defined, we need a way to reduce it.
Gradient descent updates parameters in the direction that lowers loss fastest.

Think of loss as terrain:
- Current parameters = your location
- Gradient = slope direction
- Update step = move downhill

---

## Core Update Rule

For weight `w`:

`w := w - alpha * dL/dw`

For bias `b`:

`b := b - alpha * dL/db`

- `alpha`: learning rate
- `dL/dw`, `dL/db`: gradients

---

## Learning Rate Behavior

- Too small: training is very slow.
- Too large: loss oscillates or diverges.
- Reasonable value: steady, stable decrease in loss.

You usually tune learning rate before anything else.

---

## Batch, Stochastic, Mini-batch

1. Batch gradient descent:
   - Uses all training points each step
   - Stable but can be slow on large data

2. Stochastic gradient descent (SGD):
   - Uses one point each step
   - Noisy updates, often faster iterations

3. Mini-batch gradient descent:
   - Uses small batches (most common in practice)
   - Good balance of speed and stability

---

## Convergence Signals

Training is likely converging if:
- Training loss decreases over time
- Validation loss improves initially and stabilizes
- Parameter updates get smaller

Stop when:
- Validation no longer improves
- Loss reduction per epoch becomes negligible

---

## Common Failure Modes

1. Unscaled features:
   - One feature dominates gradients
   - Training becomes unstable or slow

2. Bad learning rate:
   - Model never settles

3. Data leakage:
   - Validation looks great but production fails

Gradient descent cannot fix bad data design.
