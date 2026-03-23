# Overfitting vs Underfitting in Linear Models

Good ML is not about fitting training data perfectly.
It is about generalizing to unseen data.

---

## Underfitting

Underfitting means the model is too simple to learn the pattern.

Typical signs:
- High training error
- High validation error
- Both curves improve when model capacity/features improve

Common causes:
- Missing important features
- Too much regularization
- Training stopped too early

---

## Overfitting

Overfitting means the model captures noise instead of signal.

Typical signs:
- Very low training error
- Much higher validation error
- Performance drops in production

Common causes:
- Too many engineered features for small data
- Leakage-like features
- Weak validation strategy

---

## Bias-Variance Lens

- Underfitting -> high bias, low variance
- Overfitting -> low bias, high variance

The goal is balance: low enough bias with controlled variance.

---

## How to Respond

If underfitting:
1. Add better features
2. Train longer
3. Reduce regularization strength

If overfitting:
1. Remove leakage-prone features
2. Simplify model/features
3. Increase regularization
4. Use stronger validation split strategy

---

## Important Distinction

Overfitting is not the same as data leakage.

- Overfitting: model memorizes noise patterns.
- Leakage: model sees information it should never have at prediction time.

Leakage can produce perfect validation scores and still fail in production.
