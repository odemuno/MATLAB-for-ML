# Programming Assignment #2 - Logistic Regression

Week 3 Assignment.

This assignment covers topics on:
- Logistic regression
- Sigmoid function
- Cost Function and Gradient
- Optimization using fminunc
- Probability and accuracy
- Regularized Logistic Regression

## Logistic Regression
## 1. Plotting
**Goal**: Develop a model that predicts whether a students gets admitted into a university. Build a classification model that estimates the applicant's probability of admission based on 2 exam scores.

**Training set**: historical data from previous students: 2 exam scores and admission decision

The dataset is gotten from the given `ex2data1.txt` file.

To visualize, these are the first 5 data points:
```
34.62365962451697,78.0246928153624,0
30.28671076822607,43.89499752400101,0
35.84740876993872,72.90219802708364,0
60.18259938620976,86.30855209546826,1
79.0327360507101,75.3443764369103,1
```
The first two columns (x1 and x2) are the exam scores while the last column (y) is the admission decision. 

*Note: For the plotted graph below, + indicates (y = 1) and o indicates (y = 0)*

![graph](images\1_ExamPlot.JPG)

Refer to [fplot](https://www.mathworks.com/help/matlab/ref/fplot.html) for name-value pair arguments when plotting -- LineWidth, MarkerFaceColor, etc.

## 2. Compute Cost and Gradient
**Important equations**
- Logistic regression hypothesis: 
![equation](images\2_LogRegHypothesis.JPG)
- Sigmoid function or logistic function: 
![equation](images\3_SigmoidFunction.JPG)
- Sigmoid graph
![graph](images\4_SigmoidGraph.JPG)
- Cost Function for Logistic Regression: 
![equation](images\5_CostFuncLogReg.JPG)
- Gradient for Logistic Regression: 
![equation](images\6_GradientLogReg.JPG)

*Note that this is similar to linear regression but for a different hypothesis*
 
**MATLAB functions used**
| Function | Description |
| --- | --- |
| `[M,N] = size(X)` | for matrix X, returns the number of rows and columns in X as separate output variables, M rows and N columns|
| `D = size(X)` | for M-by-N matrix X, returns the two-element row vector. For example, If X is a scalar, which MATLAB regards as a 1-by-1 array, size(X) returns the vector [1 1]|
| `length(X)` | Length of vector; it is the longest dimension (either row or column) |
| `log` | The natural logarithm of the elements of X |

*These descriptions are gotten from the MATLAB documentation.*

## 3. Advanced Optimization using fminunc
> Use `fminunc` instead of taking gradient descent steps. It is a MATLAB/Octave optimization solver that finds the minimum of an unconstrained function.

**Function inputs:** 
- initial parameter values
- function to compute cost and gradient 

**Function benefits:**
- No need to write loops
- No need to set a learning rate, α
- Often faster than gradient descent

**Function disadvantage:**
- More complex

The plot of the decision boundary (blue linear line):
![plot](images\7_DecisionBoundary.JPG)

## 4. Prediction and Accuracies
> Use the logistic regression model to predict the probability that a student with score 45 on exam 1 and score 85 on exam 2 will be admitted.

#### Manual Calculation of Probability
Before using MATLAB, I want to manually predict the probability. 
(NOTE: this was not part of what I had to do for this homework. Not a solution to any question.)

1. know that the hypothesis is given by h<sub>θ</sub>(x) = 1/(1+e^(-z))
    - put this hypothesis equation into [desmos calculator](https://www.desmos.com/calculator)

2. the decision boundary equation is given by h<sub>θ</sub>(x) = g(θ<sub>0</sub> + θ<sub>1</sub>x<sub>1</sub> + θ<sub>2</sub>x<sub>2</sub>)
3. the values of θ are fotten from the `fminunc` theta values that I got
```
 -25.161343 
 0.206232 
 0.201472 
```
4. the x values are the exam scores and 1 as the defailt for x<sub>0</sub>
```
[1 45 85]
```
5. The  product between both vectors θ and x gives: 1.194 = θ<sup>T</sup>x = z

6. Use z as the input to the function on desmos; the output is the probability of admission (y=1)
   -  z = 1.194; probability = 0.7673

![desmos](images\8_PredictPlot.JPG)

#### Probability Calculation using MATLAB code
Just run this code and that's it! 
*Note: This code was already provided.*
```
prob = sigmoid([1 45 85] * theta)
```

## 5. Regularized Logistic Regression
> Predict whether microchips from a fabrication plant passes quality assurance (QA). During QA, each microchip goes through various tests to ensure it is functioning correctly.

The plot of the data:
![plot](images\9_RegDataPlot.JPG)

You cannot seperate a plot like this into positive or nedative like done earlier.

**Important Equations**
- Regularized cost function:
![equation](images\10_RegCostFunc.JPG)
- Regularized Gradient:
![equation](images\11_RegGradient.JPG)
![equation](images\11b_RegGradient.JPG)

The plot with the decision boundary: 
![plot](images\12_RegDecisionBoundary.JPG)

## My Submission Confirmation
I ran the `submit` function to connect to the `submit.m` file.
```
== Submitting solutions | Logistic Regression...
Use token from last successful submission (*my_email_address*)? (Y/n): Y
== 
==                                   Part Name |     Score | Feedback
==                                   --------- |     ----- | --------
==                            Sigmoid Function |   5 /   5 | Nice work!
==                    Logistic Regression Cost |  30 /  30 | Nice work!
==                Logistic Regression Gradient |  30 /  30 | Nice work!
==                                     Predict |   5 /   5 | Nice work!
==        Regularized Logistic Regression Cost |  15 /  15 | Nice work!
==    Regularized Logistic Regression Gradient |  15 /  15 | Nice work!
==                                   --------------------------------
==                                             | 100 / 100 |
```


----------------------------
## References
NOTE: On this page, I only included the end-result (plots) and the equations I used in each section. This git documentation is solely for reflection of the overall process and concepts, not solutions. 

I did not post any solutions that could be of aid to another student because that would violate the [Coursera Honor Code](https://learner.coursera.help/hc/en-us/articles/209818863-Coursera-Honor-Code). 

> You may not share your solutions to homework, quizzes, or exams with anyone else unless explicitly permitted by the instructor. This includes anything written by you, as well as any official solutions provided by the course staff.

> You may not engage in any other activities that will dishonestly improve your results or dishonestly improve or damage the results of others.

Also, since this work is directly related to the [Machine Learning Coursera course](https://www.coursera.org/learn/machine-learning/home/welcome), most of the information I reflect upon is gotten directly from it.