# Credit_Risk_Analysis

## Overview of Project
Jill commends you for all your hard work. Piece by piece, you’ve been building up your skills in data preparation, statistical reasoning, and machine learning. You are now ready to apply machine learning to solve a real-world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Deliverables
This new assignment consists of three technical analysis deliverables and a written report. You will submit the following:

### Deliverable 1: Use Resampling Models to Predict Credit Risk

* RandomOverSampler Algorithm: The balanced accuracy score is 63%. The high_risk precision is about 1% only with 59% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

![alt tag](https://github.com/elrvra/Credit_Risk_Analysis/blob/main/Resources/Images/RandomOverSampler.png)

* SMOTE Algorithm: The results are pretty similar to the previous model.
The balanced accuracy score is 63%. The high_risk precision is about 1% only with 64% sensitivity which makes a F1 of 2% only. Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 6%.

![alt tag](https://github.com/elrvra/Credit_Risk_Analysis/blob/main/Resources/Images/SMOTE.png)

* ClusterCentroids Algorithm: Here the balanced accuracy score is down to about 52%.
The high_risk precision is still 1% only with 60% sensitivity which makes a F1 of 1%.
Due to the high number of false positives, the low_risk sensitivity is only 44%.

![alt tag](https://github.com/elrvra/Credit_Risk_Analysis/blob/main/Resources/Images/ClusterCentroids.png)

### Deliverable 2: Use the SMOTEEN Algorithm to Predict Credit Risk

* SMOTEEN Algorithm: The balanced accuracy score is about 62%. The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%. Due to the high number of false positives, the low_risk sensitivity is 57%.

![alt tag](https://github.com/elrvra/Credit_Risk_Analysis/blob/main/Resources/Images/SMOTEEN.png)

### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk

* Balanced RandomForestClassifier: The balanced accuracy score improved to about 79% The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%. Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.

![alt tag](https://github.com/elrvra/Credit_Risk_Analysis/blob/main/Resources/Images/BalancedRandomForestClassifier.png)

* EasyEnsembleClassifier: Now, the balanced accuracy score is high to about 93%. The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%. Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

![alt tag](https://github.com/elrvra/Credit_Risk_Analysis/blob/main/Resources/Images/EasyEnsembleAdaBoostClassifier.png)

### Deliverable 4: A Written Report on the Credit Risk Analysis (README.md)

There is weak precision in determining if the credit risk is high, when looking at all the models to perform this credit risk analysis. However, the ensemble models contribubted more significance on sensitivity of the high credit risks. The EasyEnsembleClassifier shows a recall of 93%, which is high credit risk. However, there is false detection of low credit risk deemed high credit risk, with such low precision, and it could be assumed that the strategy of a bank's credit detection misses business opportunities. Therefore, I would not recommdn using the models to predict credit risk.

