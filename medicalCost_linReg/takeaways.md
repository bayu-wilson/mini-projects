In this tutorial I built a model using linear regression which is a supervised machine learning algorithm. The goal of supervised learning is to learn a hypothesis funciton for a given training set to estimate the target variable. The  normal equation is an analytical solution to the linear regression problem that we derived here. 

I preprocessed the data using label and one-hot encoding. I also prevented the dummy variable trap where independent variables are multicollinear. pd.get\_dummies is super useful for this!

A Box Cox transformation is a way to transform non-normal dependent variables into a normal shape. Normality is an important assumption for many statistical techniques; if your data isn’t normal, applying a Box-Cox means that you are able to run a broader number of tests.

I compared the analytic predictions with the sklearn function and it ended up being the same thing which is expected. 

To evaluate the model, we used an R2 test. The model returns  𝑅2  value of 77.95% which is pretty good but can be improved. 

I also validated the model by making linearity checks:
1) indep. and dep. variable must be linear (compare actual and predicted value in plot)
2) residual error distribution should be normal and centered on zero
3) All variables must be multivariate normal
4) There must not be collinearity. variance inflation factor VIF identifies correlation between independent variables and strength of that correlation
5) Homoscedasticity: The data are homoscedastic meaning the residuals are equal across the regression line. We can look at residual Vs fitted value scatter plot. If heteroscedastic plot would exhibit a funnel shape pattern.

