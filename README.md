# Jeff Pinegar
jeffpinegar1@gmail.com<br>
717-982-0516

In this assignment, you will be building a machine learning model that attempts to predict whether a loan will be approved or not.

## Background

Lending services companies allow individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. This data will be used to

## Predict Model Performance

You will be creating and comparing two models on this data: a Logistic Regression, and a Random Forests Classifier. Before you create, fit, and score the models, make a prediction as to which model you think will perform better. You do not need to be correct! 

Write down your prediction in the designated cells in your Jupyter Notebook, and provide justification for your educated guess.

### Answer - Logistic Regression
I believe the best choice in this application is Logistic regression. Why do I feel this way? Because logistic regression is the simpler model and likely the best model assuming all of the assumptions are true. So what are the key assumptions?  

* Binary outcome (dependent variable) - CHECK
* Independent observations – I will delete duplication - CHECK
* The relationship between the dependent and independent variables is linear - CHECK
* Larger enough sample size to ensure stability. The ratio of observation to the independent variable is very, very high in this case – CHECK
* No multicollinearity: There should be no high correlation among the independent variables in the model. I noted that one variable is the ratio of two other variables. I plan to test the model with the ratio removed and with the components extracted, therefore eliminating the collinearity – CHECK
* Equal variance of independent variable – I will perform standard scaling on the data to ensure an equal variance. – CHECK
* Outliers are a problem for both models. An examination of the data indicates there are no significant outliers. – CHECK

Other factors to consider:
* Every classification will likely need to be explained, and the results of logistic regression are easier to explain. 
* Logistic regression can run very effectively with a small data set like this. However, if the dataset was enormous, a random forest likely would outperform faster.

On the other hand, Random Forest would have been better if we suspected any of the relationships were non-linear or when there are many features, some of which may be irrelevant or highly correlated. Since debt_to_income is an apparent potential problem because it is the ratio of two other values in the set, I will test by removing this value or its components.


## Conclusion

Both models performed well. However, the logistic regression model performed better, with a higher testing sample accuracy, higher F1 Score, and significantly fewer false negatives. 

The Random Forest model has more options for tweaking the model fit. It is likely that by adjusting these parameters, this model could be improved. Still, given the performance and simplicity of the Logistic Regression model, this would not be time well spent.
