# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of analysis is to predict wheather or not the borower will return the loan based in the parameters, descring the load and the person.
* Explain what financial information the data was on, and what you needed to predict.
The input information is on amount of money that borower is going to take from company and the borower's income. ML model predicts the label of loan '0' = reliable and '1' = risky.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The variable loan_status is binary. It has imbalanced destribution over classes. 75036 loans (which is 97% of total) are credible. 
* Describe the stages of the machine learning process you went through as part of this analysis.
1. We split the input dataframe into features (X) and labels (y).
2. Then split data into training and testin samples.
3. Train and evaluate Logistic regression model .
4. Oversample training data to make balanced dataset.
5. Train and evaluate Logistic regression model on balanced dataset.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
RandomOverSampler.fit_resample() is for oversampling the input data based on class destribution. By using this method we equalised the probability of both loan types accurancy. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  Accuracy = 0.95
  Precision = 0.99
  Recall = 0.99




* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  Accuracy = 0.99
  Precision = 0.99
  Recall = 0.99

Model 2 is trained on oversampled data, which has even destribution of data by classes. This results in increase of balances accuracy score.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
It seems that second model perfomes better, because it's balanced accuracy score is higher.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
But the difference in perfomeance depends on the level of risk that company can affort. E.g. in periods of financial turbulance conpanies tent to eliminate risky desicions. So in such case we need to use model 2 with 0.99 recall for risky loans. This means that in 99% cases model will predict unreliable borower. And it will reduce the probability of losing money for company.
On the other hand model 1 is more sutable for times of financial stability. Because in this case company can affort some risk by increasing the amount of approved loans.
