# Credit_Risk_Analysis

## Background and Overview of Analysis

Stakeholder has requested machine learning models that reduce bias in predicting credit risk using a credit card credit dataset from Lending Cluc, a peer-to-peer lending service company. 

### Methodology: 
* Use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling
* Oversample using RandomOverSampler and SMOTE algorithms
* Undersample using ClusterCentroids algorithm
* Combinatorial approach of over- and undersampling using the SMOTEENN algorithm
* Compare BalancedRamdomForestClassifier and EasyEnsembleClassifier

### Deliverables: 
1. Use Resampling Models to Predict Credit Risk
2. Use the SMOTEENN Algorithm to Predict Credit Risk
3. Use Ensemble Classifiers to Predict Credit Risk
4. A Written Report on the Credit Risk Analysis 

## Results
* Original logistic regression demonstrates that the model does not do well at predicting high risk loans due to the small number of examples on which to train
![cm&classification_report](/images/cm%26classification_report.PNG)

* RandomOverSampler resulted in drastic drop in precision for high risk loans and similar precision for low risk loans. It resulted in drastic improvement in recall for high risk loans and slight drop in recall for low risk loans. 
![random_oversample_report](/images/random_oversample_report.PNG)

* SMOTE resulted in a minimally higher precision rate for high risk loans and the same precision for low risk loans. It resulted in the same recall for high risk loans and a slight increase in recall for low risk loans.
![smote_report](/images/smote_report.PNG)

* Undersampling resulted in a slightly higher precision rate for high risk loans and the same precision for low risk loans. It resulted in the same recall for high risk loans and a slightly lower recall for low risk loans. 
![undersample_report](/images/undersample_report.PNG)

* SMOTEENN resulted in identical scores to undersampling. 
![smoteen_report](/images/smoteen_report.PNG)

## Summary and Recommendations