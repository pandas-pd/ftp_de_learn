# Devlog for MPW2

A development log note for keeping track of steps & milestones during development.

## 2026-04-20

> Joël

Initital push and reading into exercise

## 2026-04-21

> Joël

Restructuring:

- Moved the notebook to dir /MPW_02/ from /MPW_02/student-input/
- Created an unaltered copy of notebook in /MPW_02/student-input/. Can be deleted if no longer needed

Worked on cg-linear-regression-stud.ipynb:

- Chapter 3:
    - Implementened loss functions: MSE, RMSE, MAE, MAPE
    - Added loss function definitions to notebook as reference
    - Added Findings to error values
- Chapter 4:
    - Implemented the `MSELossNode(MetaNode)` child class in `cgnodes.py`
    - 4.1: Implemented new computational graph and it seems to be correct
    - 4.2: Implemented update rules for theta 0 and 1 in learning loop. Wrote some findings
    - 4.2: Added the previous metrics form linear regression as comparsion
    - 4.3: Implemented batch gradient descent with random and sequential sampling
- Chapter 5:
    - 5.1: Implemented different learning rates for theta 0 and 1
    - 5.2: Implemented momentum (fixied a bug, where i used the same t-1 momentum which cause strange behaviour)

## 2026-05-02

> Maurizio

Getting into the topic:

- Work through notebook for better understanding
- Extend notebook with optional tasks (tbd, once i know more)
- Choice: 2nd Order Polynomial Regression Model

...

Log

- Right before chapter 5, there were some observations questions missing, I filled them in.
- At the end of chapter 5, added some more observations on training with larger amounts of epochs.
- Chapter 6
    - Started with setup for 2nd order model, included formula and CompGraph Visualisation.
    - Started training code, ran into some errors with exploding gradients
    - Started with gradient clipping implementation, does not work yet, coming back to it tomorrow

## 2026-05-03

> Maurizio

Coming back to fix the gradients.

- Implement gradient clipping properly this time (applied per-batch instead of per-parameter)
- Experimented with varying LRs and batch sizes for additional improvements

## 2026-05-04

> Maurizio

May the fourth be with you.

I will use the power of the force to work on another optional objective for now.

- Implemented "Early Stopping" strategy for batch-based linear model learning

## 2026-05-07

> Maurizio

- Implemented "learning rate decay on plateau" strategy.
- Started with "z-score input normalisation" training strategy.
- Input Normalisation has some issues still.

## 2026-05-08

> Maurizio

- Fixed Input Normalisation issues and plotting of results.

## 2026-05-10
> Joël

- Implemented RMS Prop optimizer


## 2026-05-11
> Joël

- Implemented Adam optimizer
