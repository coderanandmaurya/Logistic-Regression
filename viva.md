**logistic regression** questions for a viva, covering theoretical concepts, equations, regularization, and practical applications:

---

### **Basics & Theory**  
1. **Sigmoid Function**: Write the equation for the logistic (sigmoid) function. Why is it used in logistic regression?  
   *Answer*:  
   \( \sigma(z) = \frac{1}{1 + e^{-z}} \). It maps log-odds to probabilities (0 to 1).  

2. **Interpret Coefficients**: How do you interpret the coefficient \( \beta_1 \) in \( \log\left(\frac{p}{1-p}\right) = \beta_0 + \beta_1 X_1 \)?  
   *Answer*: A 1-unit increase in \( X_1 \) increases the log-odds of the outcome by \( \beta_1 \), or multiplies odds by \( e^{\beta_1} \).  

3. **Log-Loss**: Derive the log-likelihood function for logistic regression.  
   *Answer*:  
   \( \ell(\beta) = \sum_{i=1}^n \left[ y_i \log(p_i) + (1-y_i)\log(1-p_i) \right] \),  
   where \( p_i = \sigma(\beta^T X_i) \).  

4. **MLE vs. OLS**: Why is Maximum Likelihood Estimation (MLE) used instead of Ordinary Least Squares (OLS) in logistic regression?  
   *Answer*: OLS assumes normality and homoscedasticity, which fail for binary outcomes. MLE directly models Bernoulli-distributed probabilities.  

5. **Model Assumptions**: State the key assumptions of logistic regression.  
   *Answer*: Binary outcome, independence, linearity of log-odds, no severe multicollinearity.  

---

### **Regularization & Optimization**  
6. **Regularized Logistic Regression**: Write the penalized log-likelihood for Ridge and Lasso.  
   *Answer*:  
   - Ridge: \( \ell(\beta) - \lambda \sum_{j=1}^p \beta_j^2 \).  
   - Lasso: \( \ell(\beta) - \lambda \sum_{j=1}^p |\beta_j| \).  

7. **Effect of Regularization**: How does increasing \( \lambda \) in Lasso affect feature selection?  
   *Answer*: Larger \( \lambda \) shrinks coefficients toward zero, forcing sparsity (feature elimination).  

8. **Convexity**: Is the logistic regression loss function convex? Prove it.  
   *Answer*: Yes. The Hessian matrix \( H = X^T S X \), where \( S \) is diagonal with \( p_i(1-p_i) \), is positive semi-definite.  

---

### **Evaluation & Diagnostics**  
9. **ROC-AUC**: Explain how ROC curves are constructed and interpret AUC = 0.8.  
   *Answer*: ROC plots TPR vs. FPR across thresholds. AUC = 0.8 implies 80% chance of ranking a positive instance higher than a negative one.  

10. **Confusion Matrix**: Define precision, recall, and F1-score.  
    *Answer*:  
    - Precision = TP / (TP + FP).  
    - Recall = TP / (TP + FN).  
    - F1 = \( \frac{2 \times \text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} \).  

11. **Hosmer-Lemeshow Test**: What does it assess in logistic regression?  
    *Answer*: Tests goodness-of-fit by comparing observed vs. predicted probabilities in deciles.  

---

### **Advanced Concepts**  
12. **Multiclass Logistic Regression**: Compare One-vs-Rest (OvR) and Softmax approaches.  
    *Answer*:  
    - OvR: Trains \( K \) binary classifiers for \( K \) classes.  
    - Softmax: Directly models class probabilities using \( p(y=k) = \frac{e^{\beta_k^T X}}{\sum_{j=1}^K e^{\beta_j^T X}} \).  

13. **Separation Issues**: What is "complete separation," and how does it affect MLE?  
    *Answer*: When a predictor perfectly separates classes, coefficients \( \beta \) diverge to \( \pm\infty \), causing non-convergence.  

14. **Hessian Matrix**: What role does the Hessian play in parameter estimation?  
    *Answer*: Used in Newton-Raphson optimization to update coefficients. \( \beta_{\text{new}} = \beta_{\text{old}} - H^{-1} \nabla \ell \).  

---

### **Practical Scenarios**  
15. **Imbalanced Data**: How would you handle a dataset with 95% negative class and 5% positive class?  
    *Answer*: Use stratified sampling, adjust class weights (e.g., `class_weight='balanced'`), or apply SMOTE.  

---
