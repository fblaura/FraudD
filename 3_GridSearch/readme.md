# GridSearch for Fraud Classification

Within this folder it is possible to find several notebooks experimenting with GridSearch tuning process under different scaling conditions and SMOTE imbalance technique. These notebooks are listed as follows: 

## 1. StandardScaler with SMOTE 0.1
According to the previous results provided by AutoML, it was observed that the GradientBoosting and XGBoosting models had the best metrics in addition to the assembled models, for this reason we worked on the adjustment of the parameters of both models and identified which one ends up predicting better. 
The following figures show the accuracy performance of the GridSearch training process versus the number of cross-validation splits. On one hand, it is first noted that the execution time is not equal for both models, since XGBoost takes too long to train (reducing the cv options up to 10 splits). And finally, even if the accuracy is higher in one type of model than in the other, this score is sometimes not enough to determine whether the model with higher accuracy is the one with better ability to predict on new information. 

![GridSearch for StandardScaler with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/3_GridSearch/images/GridSearchSS01.png)
---
**Figure 1. Left:** GridSearch for GradientBoosting, **Right:** GridSearch for XGBoost

## 2. Normalizer with SMOTE 0.1
As mentioned above, the GradientBoosting and XGBoost models (with better metrics during the AutoML process) are observed, making a hyperparameter adjustment for both models.
The following figures show the accuracy performance of the GridSearch model training versus the number of cross-validation splits. On the one hand, it is first noted that the execution time is not equal for both models, since XGBoost with normalization takes longer than when scaling with StandardScaler was used to train (reducing the cv options from 5 splits to 10 splits, as you can see in **Figure 3**). 

![GridSearch GB for Normalizer with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/3_GridSearch/images/gridgbm_n01sized.jpg)

**Figure 2.:** GridSearch for GradientBoosting 


![GridSearch XGB for Normalizer with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/3_GridSearch/images/gridgbm_n01_sized.png)

**Figure 3:** GridSearch for XGBoost
