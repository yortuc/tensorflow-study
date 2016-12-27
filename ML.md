# Machine Learning 

## Simple ML Training Loop

0. choose a model for problem (like Linear Regression, Logistic Regression ...)
1. init model variables
2. compute resulting Y for current model parameters with data X
3. computer total error for current model with a loss function (like squarred diffs)
4. improve model parameters with an optimizer (like Gradient descent optimizer)
5. goto 2 until error drops below the given err val

this selecting "model", "optimizer" and feature representations work is also an optimization problem. and can be solved via TPOT.
