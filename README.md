# Sampling Assignment
## Comparing Sampling Techniques for 5 Machine Learning Models

## Introduction

This project aims to investigate the efficacy of various sampling techniques for generating a balanced dataset to train a machine learning model. The original dataset is imbalanced, thus, SMOTE and ADASYN over-sampling methods are employed to balance it. After achieving a balanced dataset, four distinct sampling techniques are implemented and the resulting samples are evaluated for accuracy using five different machine learning models.

## Sampling Techniques

1.Simple Random Sampling: A statistical technique where a sample is selected randomly from a given population, with each element in the population having an equal chance of being selected.

2.Stratified Sampling: A method of sampling where a population is divided into mutually exclusive strata based on a specific characteristic, and a random sample is drawn from each stratum in proportion to the size of the stratum.

3.Systematic Sampling: A type of sampling where a sample is selected by following a specific pattern, such as selecting every nth element in the population, where n is a fixed interval.

4.Cluster Sampling: A sampling technique where the population is divided into clusters or groups, and a random sample of the clusters is selected. All members of the selected clusters are included in the sample.


## Comparison Table

The table below shows the accuracies of each sampling technique on five different machine learning models. The dataset used for all models is a balanced version of the original unbalanced dataset using over-sampling techniques.

| Sampling Technique | Decision Tree | Random Forest | Logistic Regression | KNN | XGBoost |
|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|
| Simple Random Sampling - SMOTE|	96.078431	| 99.346405	| 82.352941 |	81.045752 |	98.692810 | 
| Systematic Sampling - SMOTE|	93.464052	| 97.385621	| 83.660131	| 81.699346	| 94.771242 |
| Stratified Sampling - SMOTE|	98.692810	| **100.000000**	| 84.967320	| 92.810458	| **100.000000** |
| Cluster Sampling - SMOTE|	84.967320	| 96.732026	| 82.352941	| 64.705882	| 91.503268 |
| Simple Random Sampling - ADASYN|	98.039216	| 99.346405	| 83.006536	| 82.352941	| 98.692810 |
| Systematic Sampling - ADASYN|	95.424837	| 99.346405	| 83.660131	| 83.660131	| 98.692810 |
| Stratified Sampling - ADASYN|	99.346405	| 98.692810	| 83.006536	| 91.503268	| 98.692810 |
| Cluster Sampling - ADASYN|	81.699346	| 83.660131	| 58.169935	| **32.679739**	| 79.738562 |

## Conclusion
Based on these results, it can be concluded Cluster sampling with ADASYN performs the worst on all five models. The other sampling techniques have varying performance depending on the model. The model which gives the best accuracy for all 8 samples is Random Forest.
