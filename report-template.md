# Module 12 Report Template

## Overview of the Analysis

* The purpose of this analysis is to improve the predictive capacity of our machine learning model by using various techniques like logistic regression and resampling so that we can more accurately determine the crediworthiness of individuals.

* The data showed the various financial data about the borrower such as loan size, interest rate, debt to income, number of accounts, derogatory marks, and total debt.
* From these variables we needed to predict the loan status - which is either '0' (Healthy Loan) or '1' (high-risk-loan).

* We had 75036 instances of Healthy loans and only 2500 instances of High-Risk Loans. This is problematic because we have an asymetric amount of samples to learn from * for each type.

* First we instantiated the model, then fit the data (before resampling), and then used that model to predict values and measure the accuracy of the model against the * test data. Then we repeated these stages but used resampled data the 2nd time.

* We used logisticregression which is a machine learning model from SKLEARN for predictive analysis. We also used resampling to artificially increase the number of samples we have for High-Risk Loans to imporve the dataset our model could then learn from.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * accuarcy score of .991
  * precision score of 1.0 for the '0' (healthy loan)
  * recall of.99 for the '0' (healthy loan)
  * .85 precision for '1' (high risk loan)
  * .91 recall for '1' (high risk loan)



* Machine Learning Model 2:
  * accuarcy score of .994
  * precision score of 1.0 for the '0' (healthy loan)
  * recall of.99 for the '0' (healthy loan)
  * recall .99 for the '1' (high risk loan)
  * precision .84 for the '1' (high risk loan)

## Summary

* Which one seems to perform best? How do you know it performs best?
Model 2 seems to perfom best because it has a slightly higher accuracy score as well as having a significantly higher precision for High-Risk Loans. This is particularly important becuase we would prefer to have less instances of false negatives sinces banks loose significantly more money by making a bad loan vs missing making a good loan.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Model 2 also seems to predict the 0s just as well so it seems to be the clear choice for either problem. We may be able to adjust certain parameters further to optimize for higher prediction accuracy of the 1s depending on our goal. If our goal was to eliminate any chance of making a High-Risk Loan then we would want to increase our accurary prediction for 1s even further. However this is ultimatly up the bank and what risk tolerance they have.
