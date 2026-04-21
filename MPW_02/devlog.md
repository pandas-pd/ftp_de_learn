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