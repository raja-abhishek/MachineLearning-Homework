# MachineLearning-Homework
### Background
This assignment requires building and evaluation of several machine learning models to predict credit risk using data typically seen from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so it will require different techniques for training and evaluating models with imbalanced classes. 

#### Required libraries:
- imbalanced-learn
- Scikit-learn

#### Required Techniques:
- Resampling
- Ensemble Learning

### Resampling

Used the imbalanced learn library to resample the LendingClub data and built logistic regression classifiers using the resampled data. Logistic regression classifier was built with following resampling approach:
- No treatment for imbalanced classification
- Oversampling 
  - Naive Random Oversampler
  - SMOTE Algorithm
- Undersampling
  - Cluster Centroids
- Combination Sampling
  - SMOTEENN

#### Evaluation:
- Which model had the best balanced accuracy score?

  Model with SMOOT oversampling has best balanced accuracy score 0.9944814968814969.

   |S.N.|Approach|Balanced Accuracy Score|
   |:---|:-----:|-------------:|
   |1|With sample imbalance|0.9850947278639586|
   |2|Random oversampling|0.9944281891358815|
   |3|SMOOT oversampling|0.9944814968814969|
   |4|Cluster Centroid undersampling|0.9890680739911509|
   |5|SMOTEENN combination sampling|0.9944281891358815|

- Which model had the best recall score?

  Model with cluster centroid undersampling has best recall score.

   |S.N.|Approach|Recall Score|
   |:---|:-----:|-------------:|
   |1|With sample imbalance|0.99422|
   |2|Random oversampling|0.99412|
   |3|SMOOT oversampling|0.99417|
   |4|Cluster Centroid undersampling|0.99448|
   |5|SMOTEENN combination sampling|0.99417|
   
- Which model had the best geometric mean score?

  Models with SMOOT oversampling and SMOTTENN combination sampling have best geometric mean score.

   |S.N.|Approach|Geometric Mean Score|
   |:---|:-----:|-------------:|
   |1|With sample imbalance|0.98927|
   |2|Random oversampling|0.99464|
   |3|SMOOT oversampling|0.99467|
   |4|Cluster Centroid undersampling|0.99328|
   |5|SMOTEENN combination sampling|0.99467|

### Ensemble Learning
Following ensemble classifiers was used to predict loan risk. 
- Balanced Random Forest Classifier
- Easy Ensemble Classifier

#### Evaluation:
- Which model had the best balanced accuracy score?

  Easy ensemble classifier has best balanced accuracy score.

   |S.N.|Approach|Balanced Accuracy Score|
   |:---|:-----:|-------------:|
   |1|Balanced Random Forest Classifier|0.7831230283911672|
   |2|Easy Ensemble Classifier|0.9274135715177813|
   
- Which model had the best recall score?

  Easy ensemble classifier has best recall score.

   |S.N.|Approach|Recall Score|
   |:---|:-----:|-------------:|
   |1|Balanced Random Forest Classification|0.90|
   |2|Easy Ensemble Classifier|0.95|
   
- Which model had the best geometric mean score?

  Easy ensemble classifier has geometric mean score.

   |S.N.|Approach|Geometric Mean Score|
   |:---|:-----:|-------------:|
   |1|Balanced Random Forest Classifier|0.77|
   |2|Easy Ensemble Classifier|0.93|
   
- What are the top three features?

  Top three features based on balanced random forest classifier are 
   
   |S.N.|Feature|Importance|
   |:---|:-----:|-------------:|
   |1|total_rec_prncp|0.08107901444883758|
   |2|last_pymnt_amnt|0.0734948453918542|
   |3|total_rec_int|0.06126614939524893|
