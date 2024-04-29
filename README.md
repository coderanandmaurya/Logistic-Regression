# Logistic-Regression

Logistic regression is a statistical method used for binary classification tasks, meaning it predicts the probability that a given input belongs to one of two possible classes. Despite its name, logistic regression is actually a linear model, but it uses the logistic function (also called the sigmoid function) to squash the output to a value between 0 and 1, representing probabilities.

Here's how it works:

1. **Model Representation**: In logistic regression, you have a set of input features (x) and you want to predict the probability that a given input belongs to a particular class (usually denoted as either 0 or 1).

2. **Hypothesis Function**: The hypothesis function in logistic regression is defined as:
   \[ h_\theta(x) = \frac{1}{1 + e^{-\theta^T x}} \]
   Here, \( h_\theta(x) \) is the predicted probability that \( x \) belongs to the positive class (class 1), \( \theta \) are the parameters of the model (also known as weights), and \( e \) is the base of the natural logarithm.

3. **Training**: The parameters \( \theta \) of the model are learned from the training data using optimization algorithms such as gradient descent. The objective is to minimize a cost function that measures the difference between the predicted probabilities and the actual class labels.

4. **Decision Boundary**: Once the model is trained, you can use it to make predictions by applying the hypothesis function to new input data. The decision boundary is the line (or hyperplane in higher dimensions) that separates the two classes. It is determined by the parameters \( \theta \) of the model.

Logistic regression is widely used in various fields, including finance, healthcare, marketing, and social sciences, due to its simplicity, interpretability, and effectiveness, especially when the relationship between the input features and the output is approximately linear.
## Difference B/W linear reg and log reg

Linear regression and logistic regression are both used for different types of problems in machine learning and statistics. Here are the key differences between them:

1. **Type of Output**:
   - Linear Regression: It is used for predicting continuous values. In other words, it predicts a real-valued output based on input features.
   - Logistic Regression: It is used for predicting the probability that a given input belongs to a particular class. It outputs probabilities between 0 and 1, and it's typically used for binary classification tasks.

2. **Model Representation**:
   - Linear Regression: The hypothesis function in linear regression is a linear combination of the input features, without any transformation.
   - Logistic Regression: The hypothesis function in logistic regression is the logistic function (sigmoid function) applied to a linear combination of the input features.

3. **Output Range**:
   - Linear Regression: The output can range from negative infinity to positive infinity.
   - Logistic Regression: The output is constrained between 0 and 1 due to the logistic function, representing probabilities.

4. **Loss Function**:
   - Linear Regression: Typically uses a loss function such as mean squared error (MSE) or mean absolute error (MAE) to measure the difference between predicted and actual values.
   - Logistic Regression: Typically uses a loss function such as cross-entropy loss (also known as log loss) to measure the difference between predicted probabilities and actual class labels.

5. **Optimization**:
   - Linear Regression: Often optimized using methods like ordinary least squares (OLS) or gradient descent.
   - Logistic Regression: Optimized using techniques like gradient descent or other optimization algorithms to minimize the logistic loss function.

6. **Interpretation**:
   - Linear Regression: Coefficients represent the change in the output variable for a one-unit change in the corresponding input variable.
   - Logistic Regression: Coefficients represent the change in the log odds of the output variable for a one-unit change in the corresponding input variable.

7. **Use Cases**:
   - Linear Regression: Used for tasks such as predicting house prices, stock prices, or any continuous variable.
   - Logistic Regression: Used for tasks such as predicting whether an email is spam or not, whether a customer will churn or not, or any binary classification task.

Despite these differences, both linear regression and logistic regression are widely used and form the basis of many more complex machine learning algorithms. They are often the first models tried when approaching a new problem due to their simplicity and interpretability.
