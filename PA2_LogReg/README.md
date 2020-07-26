# Programming Assignment #2 - Logistic Regression ML

Week 3 Assignment.

This assignment covers topics on:
- Logistic regression

### Provided Files
- ?

## Logistic Regression
## 1. Plotting
**Goal**: Develop a model that predicts whether a students gets admitted into a university. Build a classification model that estimates the applicant's probability of admission based on 2 exam scores.

**Training set**: historical data from previous students: 2 exam scores and admission decision

The dataset is gotten from the `ex2data1.txt` file.

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

![graph](1_ExamPlot.jpg)

Refer to [fplot](https://www.mathworks.com/help/matlab/ref/fplot.html) for name-value pair arguments when plotting -- LineWidth, MarkerFaceColor, etc.

## 2. Compute Cost and Gradient
**Important equations**
- Logistic regression hypothesis: ![equation](2_LogRegHypothesis.jpg)
- Sigmoid function: ![equation](3_SigmoidFunction.jpg)
- Sigmoid graph
![graph](4_SigmoidGraph.jpg)
- Cost Function for Logistic Regression: ![equation](5_CostFuncLogReg.jpg)
- Gradient for Logistic Regression: ![equation](6_GradientLogReg.jpg)
*Note that this is similar to linear regression but for a different hypothesis*
 

## 3. Optimizing using fminunc

## 4. 