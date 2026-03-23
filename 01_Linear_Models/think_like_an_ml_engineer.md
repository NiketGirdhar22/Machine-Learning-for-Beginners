# Think Like an ML Engineer - Module 1

These scenarios test judgment, not memorization.

---

## Scenario 1 - Great Training, Bad Validation

You train a linear regression model.
- Training MSE: 1.2
- Validation MSE: 8.9

Questions:
- Is this overfitting or underfitting?
- Name two concrete actions you would take next.
- Which logs or plots would you check first?

---

## Scenario 2 - The Learning Rate Problem

During training:
- Epoch 1 loss: 22
- Epoch 2 loss: 9
- Epoch 3 loss: 34
- Epoch 4 loss: 11
- Epoch 5 loss: 40

Questions:
- What is the most likely issue?
- What exact parameter would you adjust first?
- Why is changing model complexity not your first move here?

---

## Scenario 3 - The Outlier Trap

You predict delivery time.
Most samples are between 20 and 60 minutes.
Some rare entries are 300+ minutes because of external disruptions.

Questions:
- Why might MSE give unstable behavior here?
- What alternative loss could you try?
- What business question should guide that choice?

---

## Scenario 4 - Leakage Disguised as Genius

A feature called `final_invoice_amount` makes validation MSE drop dramatically.
In production, this field is only available after delivery.

Questions:
- What is this issue called?
- Why did offline validation look excellent?
- What process change would prevent this in future projects?
