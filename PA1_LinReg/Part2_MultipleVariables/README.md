# Programming Assignment #1 - Linear Regression ML (optional part)
I decided to complete this section for extra practice, and also so that I know how to work with multiple variables.

## Linear Regression with Multiple Variables
> In this part, you will implement linear regression with multiple variables to predict the prices of houses. Suppose you are selling your house and you want to know what a good market price would be. One way to do this is to first collect information on recent houses sold and make a model of housing prices.

The data is gotten from the `ex1data2.txt` file.
### 1. Feature Normalization
Relevant scripts:
- `ex1_multi.m`
- `featureNormalize.m`

**Feature normalization** is a form of feature scaling when the features differ by various orders of magnitudes.

Task:
- Subtract the mean value of each feature from the dataset: use the `mean` function.
- After subtracting the mean, additionally scale (divide) the feature values
by their respective "standard deviations": use the `std` function.


### 2. Gradient Descent
Relevant scripts:
- `computeCostMulti.m`
- `gradientDescentMulti.m`

The graph I got
![photo](1_gradient_descent_convergence.JPG)


Using a gradient descent algorithm, I was able to predict the price of a 1650 sqft, 3 bedroom house.
### 3. Normal Equations
Relevant scripts:
- `ex1_multi.m`
- `normalEqn.m`

The closed-form solution to linear resgression is: ![photo](2_closedform_equation.JPG)

Characteristics:
- no feature scaling
- exact solution in one calculation
- no "loop until convergence" (compared to gradient descent)

Using a normal equation algorithm, I was able to predict the price of a 1650 sqft, 3 bedroom house.

----------------------------
## References
NOTE: I will not be posting any solutions that could be of aid to another student because that would violate the [Coursera Honor Code](https://learner.coursera.help/hc/en-us/articles/209818863-Coursera-Honor-Code).

> You may not share your solutions to homework, quizzes, or exams with anyone else unless explicitly permitted by the instructor. This includes anything written by you, as well as any official solutions provided by the course staff.

> You may not engage in any other activities that will dishonestly improve your results or dishonestly improve or damage the results of others.

Also, since this work is directly related to the [Machine Learning Coursera course](https://www.coursera.org/learn/machine-learning/home/welcome), most of the information I reflect upon is gotten directly from it.
