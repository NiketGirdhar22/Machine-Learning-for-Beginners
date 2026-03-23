# Loss Functions: How a Model Knows It Is Wrong

Predictions alone are not enough.
The model needs a numeric signal telling it how wrong it is.

That signal is the loss.

---

## Error vs Loss vs Cost

- Error: wrongness for one example (`y_hat - y`)
- Loss: non-negative penalty for one example
- Cost (objective): average loss across the dataset

Training minimizes cost, not a single prediction error.

---

## Mean Squared Error (MSE)

`MSE = (1/n) * sum((y_hat_i - y_i)^2)`

Properties:
- Penalizes large errors strongly (because of square)
- Smooth and convenient for gradient-based optimization
- Sensitive to outliers

Use when:
- Large mistakes should be punished heavily
- Noise is roughly symmetric and moderate

---

## Mean Absolute Error (MAE)

`MAE = (1/n) * sum(|y_hat_i - y_i|)`

Properties:
- More robust to outliers than MSE
- Penalizes errors linearly
- Less smooth around zero than MSE

Use when:
- Data has occasional large outliers
- You want stable median-like behavior

---

## Choosing Between MSE and MAE (Rule of Thumb)

- Start with MSE for simple baselines.
- Try MAE if a few bad points dominate training.
- Compare validation performance, not training loss alone.

---

## Loss vs Metric

For regression, teams often optimize one thing and report another.

Example:
- Optimize: MSE (better gradients)
- Report: RMSE or MAE (easier to interpret in target units)

This is normal if you clearly define both.

---

## Common Pitfalls

1. Comparing losses across datasets with different target scales.
2. Claiming "low loss" without showing a baseline.
3. Optimizing a loss that does not match product impact.

The best loss is the one aligned with real-world error cost.
