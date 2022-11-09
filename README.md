### Credit Risk Analysis

In this analysis, we take into account 6 different Machine Learning Algorithms for Supervised Machine-learning and try to determine if any of them are useful in determining credit risk for LendingClub.

### Results

#### Oversampling, SMOTE

Balanced Accuracy Score: 0.6515938052705158

|                 |  pre |  rec |
|-----------------|------|------|
| **high_risk**   | 0.01 | 0.62 |
| **low_risk**    | 1.00 | 0.68 |
|                 |      |      |
| **avg / total** | 0.99 | 0.68 |

#### SMOTE Oversampling

Balanced Accuracy Score: 0.6241876870888075

|                 |  pre |  rec |
|-----------------|------|------|
| **high_risk**   | 0.01 | 0.59 |
| **low_risk**    | 1.00 | 0.66 |
|                 |      |      |
| **avg / total** | 0.99 | 0.66 |

#### Undersampling, Cluster Centroids

Balanced Accuracy Score: 0.6241876870888075

|                 |  pre |  rec |
|-----------------|------|------|
| **high_risk**   | 0.01 | 0.60 |
| **low_risk**    | 1.00 | 0.43 |
|                 |      |      |
| **avg / total** | 0.99 | 0.44 |

#### (Over and Under) Sampling, SMOTEENN

Balanced Accuracy Score: 0.6465718682894795

|                 |  pre |  rec |
|-----------------|------|------|
| **high_risk**   | 0.01 | 0.71 |
| **low_risk**    | 1.00 | 0.58 |
|                 |      |      |
| **avg / total** | 0.99 | 0.58 |

#### Balanced Random Forest Classifier

Balanced Accuracy Score: 0.7877672625306695

|                 |  pre |  rec |
|-----------------|------|------|
| **high_risk**   | 0.04 | 0.67 |
| **low_risk**    | 1.00 | 0.91 |
|                 |      |      |
| **avg / total** | 0.99 | 0.91 |

#### Easy Ensemble AdaBoost Classifier

Balanced Accuracy Score: 0.925427358175101

|                 |  pre |  rec |
|-----------------|------|------|
| **high_risk**   | 0.07 | 0.91 |
| **low_risk**    | 1.00 | 0.94 |
|                 |      |      |
| **avg / total** | 0.99 | 0.94 |

### Summary

- As none of the Under and Oversampling methods yielded any useful results with moderate prediction results, the hope was found in both the Balanced Random Forest Classifier with a balanced accuracy score of ~0.79 and the Easy Ensemble AdaBoost Classifier with a balanced accuracy score of ~0.92!
- All the algorithms successfully predicted the low-risk candidates, but since we are trying to flag the high-risk candidates, that is of little use.
- Based on the data provided by the machine learning algorithms, **my recommendation is to go with the Easy Ensemble AdaBoost Classifier**. As there are a lot fewer high-risk credit candidates, the data should be leaning towards a high Recall to flag potential high-risk candidates. The Easy Ensemble AdaBoost Classifier is the only ML Algorithm that has a Recall score of > 0.9, resulting in a very high flag rate.
