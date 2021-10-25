# Dimensionality reduction 

As mentioned throughout this project, the dataset containing the data presents a high dimensionality, having originally a dataset with more than 450 characteristics and more than 590000 data. With the training of the different models, it has been possible to reach a maximum prediction, which presents a margin of error of 15% with respect to the fraud label (which is our target variable). Inside this folder you will find the notebooks related to dimension reduction with respect to the scaling techniques used for our work:

## 1. Dimensionality reduction for StandardScaler with SMOTE 0.1

## 2. Dimensionality reduction for Normalizer with SMOTE 0.1

According to a component analysis, the PCA technique provides that with approximately 60 characteristics it is possible to describe the fraud problem. Based on this, a training with models such as KNN and XGBoost is performed to determine their accuracy. As can be seen in the graphical analysis, the training shows a fairly high accuracy for both KNN and XGBoost, however, in the evaluation of the test dataset, for the same components the accuracy decreases considerably, which could be a clear sign of overfitting.

![GradientBoosting training for StandardScaler with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/5_Dimensionality_reduction/images/knn_ss_01.png)
---
**Figure 1.** Training for XGBoost and KNN with PCA reduction

To show a little of the results of this notebook, we emphasize the process of dimension reduction for a scaling with StandardScaler. Training with GradientBoosting and reducing the dimensions of the dataset up to 120 features, we obtain a confusion matrix with 16% error in predicting the fraud label.

![XGBoost training for StandardScaler with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/5_Dimensionality_reduction/images/gbm_selectfrom_ss01.png)
---
**Figure 2.** Model training for GradientBoosting, StandarScaler and reduction with SelectFromModel

Finally, a dimension reduction is performed with the RFE (recursive feature elimination) technique, obtaining a confusion matrix of a model trained with GradientBoosting of 21%, increasing the error considerably.  

As a final conclusion, it can be deduced that the reduction of dimensions using these techniques was not enough to improve the prediction. At the same time, the normalization of the data with the length of the notebooks presented does not show better behavior than with StandardScaler. Therefore, we will stop working with normalization in the future.  


![XGBoost training for Normalizer with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/5_Dimensionality_reduction/images/gbm_rfe_ss01.png)

**Figure 3:** Model training for GradientBoosting, StandarScaler and reduction with RFE
