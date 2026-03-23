# Module 1: Linear Models

## Purpose of This Module

This module teaches the first real learning algorithm most ML engineers use: linear models.
You will learn how models convert inputs into predictions, how error is measured, and how optimization updates parameters.

By the end of Module 1, you should:
- Understand linear regression as a function approximation problem
- Know how loss functions define what "good" predictions mean
- Understand gradient descent and learning rate behavior
- Diagnose overfitting vs underfitting using train/validation signals
- Implement linear regression from scratch on a tiny dataset

---

## Prerequisite

Complete Module 0 first:
- [../00_ML_Foundations/README.md](../00_ML_Foundations/README.md)

---

## Structure of This Module

01_Linear_Models/

|- [README.md](README.md) (current file)
|- [0_linear_regression.md](0_linear_regression.md)
|- [1_loss_functions.md](1_loss_functions.md)
|- [2_gradient_descent.md](2_gradient_descent.md)
|- [3_overfitting_vs_underfitting.md](3_overfitting_vs_underfitting.md)
|- [4_from_scratch_linear_regression.md](4_from_scratch_linear_regression.md)
|- [checkpoints.md](checkpoints.md)
`- [think_like_an_ml_engineer.md](think_like_an_ml_engineer.md)

---

## Notebooks

Hands-on notebooks for this module:
- [notebooks/01_linear_regression_from_scratch.ipynb](notebooks/01_linear_regression_from_scratch.ipynb)
- [notebooks/02_overfitting_underfitting_from_scratch.ipynb](notebooks/02_overfitting_underfitting_from_scratch.ipynb)
- [notebooks/03_linear_models_with_libraries.ipynb](notebooks/03_linear_models_with_libraries.ipynb)

Use notebook 1 and 2 first (from-scratch), then notebook 3 (library-based).

---

## Recommended Study Flow

1. Read files `0` to `3` in order.
2. Do the scratch implementation in file `4` without skipping the math.
3. Solve all questions in `checkpoints.md`.
4. Finally, answer scenario questions in `think_like_an_ml_engineer.md` without notes.

If you can explain each training signal in plain language, you are ready for Module 2.
