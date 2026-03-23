# Linear Regression: The First Real Learning Model

Linear regression predicts a continuous value by fitting a line (or hyperplane) through data.

Examples:
- House size -> price
- Study hours -> exam score
- Ad spend -> sales

The core idea:
> Find parameters that make predictions as close as possible to true values.

---

## Model Form

For one feature:

`y_hat = w * x + b`

- `x`: input feature
- `w`: weight (slope)
- `b`: bias (intercept)
- `y_hat`: predicted output

For many features:

`y_hat = w1*x1 + w2*x2 + ... + wn*xn + b`

or in vector form:

`y_hat = w^T x + b`

---

## Intuition for Parameters

- If `w` is large and positive, prediction grows quickly as `x` grows.
- If `w` is negative, prediction decreases as `x` grows.
- `b` shifts the prediction up or down even when `x = 0`.

Linear regression is not about straight lines on paper.
It is about linear combinations of features.

---

## Why This Model Matters

Linear models are:
- Fast to train
- Easy to interpret
- Strong baselines for many real-world tasks

Even when you later use deep models, linear regression helps you reason about:
- signal vs noise
- optimization behavior
- generalization

---

## What Linear Regression Assumes (Practical View)

- Relationship is approximately linear in the chosen features
- Errors are not dominated by extreme outliers
- Features carry useful signal

If these assumptions break, performance degrades, but the model is still a useful diagnostic tool.

---

## Common Beginner Mistakes

1. Treating correlation as causation.
2. Ignoring feature scaling when using gradient descent.
3. Assuming high training accuracy means deployment success.
4. Forgetting that feature choice is part of the model.

---

## Quick Mental Check

If a single feature model predicts salaries and `w = 0`, then:
- All predictions are the same value (`b`).
- The model learned "feature adds no value."
