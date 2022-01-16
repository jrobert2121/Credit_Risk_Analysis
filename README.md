# Credit Risk Analysis

## Project Overview
Machine learning is to be utilized to analyze credit card risk.  Using the credit card dataset from LendingClub, different techniques are employed to train and evaluate models with unbalanced classes to predict credit risk. 

## Resources
 - Data:  [LoanStats_2019Q1.csv](LoanStats_2019Q1.csv)
 - Software: Python v. 3.7.11, Jupyter Notebook v. , scikit-learn v. 1.0.2, numpy v. 1.20.3, scipy v. 1.7.3, imbalanced-learn v 0.8.1

## Results
The dataset was loaded into a dataframe and then cleaned.  Using the get_dummies method, data features and the target were created.  After checking the y value counts, the data was split into training and testing before proceeding with the techniques below.

### Resampling Models
 - Oversampling with RandomOverSampler: The object of this model is to over-sample the minority class(es) by picking samples at random with replacement.

  - Balanced Accuracy Score: 66%.
  ![ros_bal_accuracy](Resources/ros_bal_accuracy.png)

  - High Risk had a precision rate of 1% and a recall of 72%.
  - Low Risk had a precision rate of 100% and a recall of 60%.

  ![ros_cm](Resources/ros_cm.png)

  ![ros_classification_report](Resources/ros_classification_report.png)

 - SMOTE Oversampling: Synthetic Minority Over-sampling Technique selects a random minority class and finds its nearest minority class neighbors.  A randomly selected neighbor is chosen and a synthetic sample is created at a random, selected point on the line between the original selected minority class and the randomly selected neighbor.

  - Balanced Accuracy Score: 66%
  ![smote_bal_accuracy](Resources/smote_bal_accuracy.png)

  - High Risk had a precision rate of 1% and a recall of 72%.
  - Low Risk had a precision rate of 100% and a recall of 60%

  ![smote_cm](Resources/smote_cm.png)

  ![smote_classification_report](Resources/smote_classification_report.png)

 - Cluster Centroids undersampling: This method under samples the majority class.

  - Balanced Accuracy Score: 54%
  ![cc_bal_accuracy](Resources/cc_bal_accuracy.png)

  - High Risk had a precision rate of 1% and a recall of 69%.
  - Low Risk had a precision rate of 100% and a recall of 40%.

  ![cc_cm](Resources/cc_cm.png)

  ![cc_classification_report](Resources/cc_classification_report.png)

 - Combination Sampling with SMOTEEN: This model is a two step process.  It first oversamples the minority class with SMOTE.  Then it cleans the resulting data with an undersampling strategy, Edited Nearest Neighbors (ENN).

  - Balanced Accuracy Score: 68%
  ![smoteen_bal_accuracy](Resources/smoteen_bal_accuracy.png)

  - High Risk had a precision of 1% and a recall of 78%.
  - Low Risk had a precision of 100% and a recall of 57%

  ![smoteen_cm](Resources/smoteen_cm.png)

  ![smoteen_classification_report](Resources/smoteen_classification_report.png)




## Summary
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning