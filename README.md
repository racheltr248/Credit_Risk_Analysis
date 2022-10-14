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
* **Original logistic regression** demonstrates that the model does not do well at predicting high risk loans due to the small number of examples on which to train. 
    * high_risk: .81 precision, .21 recall, .33 f1
    * low_risk: 1.00 precision, 1.00 recall, 1.00 f1

![base_report](/images/01_base_report.PNG)

* **RandomOverSampler** resulted in a drastic drop in precision for high risk loans and a similar precision for low risk loans. It resulted in a drastic improvement in recall for high risk loans and a slight drop in recall for low risk loans. 
    * high_risk: .03 precision, .82 recall, .06 f1
    * low_risk: 1.00 precision, .84 recall, .91 f1

![random_oversample_report](/images/02_random_oversample_report.PNG)

* **SMOTE** resulted in a minimally higher precision rate for high risk loans and the same precision for low risk loans. It resulted in the same recall for high risk loans and a slight increase in recall for low risk loans.
    * high_risk: .04 precision, .82 recall, .07 f1
    * low_risk: 1.00 precision, .87 recall, .93 f1

![smote_report](/images/03_smote_report.PNG)

* **Undersampling** resulted in a slightly lower precision rate for high risk loans and the same precision for low risk loans. It resulted in a slightly higher recall for high risk loans and a significantly lower recall for low risk loans. 
    * high_risk: .02 precision, .88 recall, .04 f1
    * low_risk: 1.00 precision, .76 recall, .86 f1

![undersample_report](/images/04_undersample_report.PNG)

* **SMOTEENN** resulted in a lower precision rate for high risk loans and a slightly lower precision for low risk loans. It resulted in the same precision rate for low risk loans and a higher recall rate for low risk loans. These numbers are very similar to those found through use of the RandomOverSampler algorithm.
    * high_risk: .03 precision, .82 recall, .06 f1
    * low_risk: 1.00 precision, .86 recall, .92 f1

![smoteen_report](/images/05_smoteenn_report.PNG)

* **Balanced Random Forest Classifier** resulted in the same precision rate for high risk loans and a drastically lower recall for high risk loans. It resulted in the same precision for low risk loans and a minimally higher recall for low risk loans.
    * high_risk: .03 precision, .63 recall, .06 f1
    * low_risk: 1.00 precision, .88 recall, .94 f1

![brf_report](/images/06_brf_report.PNG)

* **Easy Ensemble AdaBoost Classifier** resulted in a higher precision rate for high risk loans and a higher recall rate for high risk loans. It resulted in the same precision for low risk loans and a higher recall rate for low risk loans. Other than the original logistic regression, this was the most successful.  
    * high_risk: .09 precision, .92 recall, .16 f1
    * low_risk: 1.00 precision, .94 recall, .97 f1

![eec_report](/images/07_eec_report.PNG)

## Summary and Recommendations
Although the Easy Ensemble AdaBoost Classifier results were more successful than the other methods, it still had a very low precision rate for high risk loans, under 10% successful. None of these machine learning models would be recommended for use to predict credit risk.
