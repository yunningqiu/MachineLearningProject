# MachineLearningProject
Option Pricing Prediction

**Project Overview**
By examining historical call option pricing data on the S&P 500, we developed statistical/ML models to predict the future value of a European call option.

**Goals and Approaches**
1. Build a regression model capable of predicting option value.
- Linear Regression
- Decision Tree 
- Random Forest
- Light Gradient Boosting Machine
2. Build a classification model capable of predicting if the Black-Scholes formula overvalue or undervalue the option.
- Logistic Regression
- Decision Tree
- K-Nearest Neighbors (KNN)
- Support Vector Machines (SVM)
- Random Forest

**Data Cleaning**
1. Drop rows/observations with null entries
2. Drop rows with time to maturity (tau) greater than 1 OR current asset value (S) equals 0.
3. Customized feature: “difference” → Current asset value - Strike price

**Results & Conclusion**
Boost Tree Regression Model gives the highest fitness (R2 = 99.83%)
Random Forest Classifier gives the highest accuracy (error rate = 6.7%)

For our regression task to predict the option value, we chose the boost tree model, Light Gradient Boosting Machine, as our final regression model, since it outperformed the other three models that we tried in terms of the 10-fold CV of R-squared, reaching up to accuracy of 99.83%.

At the same time, we also chose Light Gradient Boosted Tree as the final approach to predict BS. We chose this approach because it has the lowest error rate (5.8%) compared with other algorithms. Also, Light Gradient Boosted Tree returns more stable results compared with random forest by checking the error rates in the 10-fold CV. 

