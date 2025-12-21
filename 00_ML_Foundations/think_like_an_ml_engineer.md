# Think Like an ML Engineer — Module 0

These are not trick questions.
They test whether you understand **how ML systems fail**.

---

## Scenario 1 — The Perfect Model

You train a model.
- Training accuracy: 99%
- Validation accuracy: 98%

You deploy it.
Users complain it performs terribly.

Questions:
- Name at least **two possible reasons**
- Which part of the ML pipeline would you investigate first?

---

## Scenario 2 — The Magic Feature

A feature increases validation accuracy from 72% → 95%.

Later, the model completely fails in production.

Questions:
- What is the most likely issue?
- What is this problem called?
- Why did metrics look good?

---

## Scenario 3 — Clustering Confusion

You cluster customers into 4 groups.
Marketing names them:
- Budget buyers
- Loyal customers
- Impulse buyers
- Premium users

Questions:
- What assumption is being made here?
- Why can this be dangerous?