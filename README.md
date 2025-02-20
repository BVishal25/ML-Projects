# ML-Projects

  These ML Projects are done with understanding of the course 'Machine Learning Specialization' by Andrew Ng in Coursera.

Link to the course:
[https://www.coursera.org/specializations/machine-learning-introduction](url)

# Univariate Linear Regression
  
  A Linear Regression Variant, have only one type of training and testing data.

## Prediction Function (f_w,b(x))

The prediction function, denoted as f_w,b(x), represents the linear model used for prediction. It's defined as:

f_w,b(x) = wx + b


Where:

* `f_w,b(x)` is the predicted output for input `x`.
* `w` is the weight (or slope) of the line.
* `x` is the input feature.
* `b` is the bias (or y-intercept) of the line.

## Cost Function (J(w, b))

The cost function, denoted as J(w, b), measures the error between the predicted values and the actual values. It's commonly defined as the Mean Squared Error (MSE):

J(w, b) = (1 / 2m) * Σ[i=1 to m] (f_w,b(x^(i)) - y^(i))^2


Where:

* `J(w, b)` is the cost (or error) of the model.
* `m` is the number of training examples.
* `Σ` represents the summation over all training examples.
* `x^(i)` is the input feature of the i-th training example.
* `y^(i)` is the actual output of the i-th training example.
* `f_w,b(x^(i))` is the predicted output for the i-th training example.

## Gradient Descent

Gradient descent is an iterative optimization algorithm used to minimize the cost function J(w, b). It updates the parameters `w` and `b` in the direction of the steepest descent of the cost function.

The update rules for `w` and `b` are:

w := w - α * ∂J(w, b)/∂w
b := b - α * ∂J(w, b)/∂b


Where:

* `:=` denotes simultaneous assignment.
* `α` is the learning rate, which controls the step size of the updates.
* `∂J(w, b)/∂w` is the partial derivative of the cost function with respect to `w`.
* `∂J(w, b)/∂b` is the partial derivative of the cost function with respect to `b`.

The partial derivatives are calculated as:

∂J(w, b)/∂w = (1 / m) * Σ[i=1 to m] (f_w,b(x^(i)) - y^(i)) * x^(i)
∂J(w, b)/∂b = (1 / m) * Σ[i=1 to m] (f_w,b(x^(i)) - y^(i))
