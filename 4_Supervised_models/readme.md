# Model training for Fraud Classification

Within this folder it is possible to find several notebooks experimenting with model training from hyperparameter setting with GridSearch (under different scaling conditions and SMOTE imbalance technique). These notebooks are listed as follows: 

## 1. StandardScaler with SMOTE 0.1
With the results obtained from the hyperparameter fitting process, it was decided to train each best model with those parameters; and thus observe if training from the supervised method is different from using GridSearch to train. 
Different metrics were used to evaluate the performance of the models, but the decision on which one was better was based on the confusion matrix of the estimators and their prediction. 
We then have the confusion matrix for the GradientBoosting model, obtaining a 17% misclassification rate. This matrix is performed on a section of the dataset taken for training, with more than 17,000 row values and the original 430 columns. 


![GradientBoosting training for StandardScaler with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/4_Supervised_models/images/gbm_train_ss01.png)
---
**Figure 1.** Model training for GradientBoosting and StandarScaler

Within this same notebook, training is performed for XGBoost as it had also been detected by AutoML. Together with the parameters obtained from GridSearch, a confusion matrix is obtained on this training.

![XGBoost training for StandardScaler with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/4_Supervised_models/images/xgb_train_ss01.png)
---
**Figure 2.** Model training for GradientBoosting and StandarScaler

From this exercise we finally observe that XGBoost predicts fraud labels better than GradientBoosting, only by a small margin of about 2%.

## 2. Normalizer with SMOTE 0.1
In this notebook the GradientBoosting and XGBoost models were used again to train on the dataset. The main evaluation will be the result of the confusion matrix. 

![GradientBoosting training for Normalizer with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/4_Supervised_models/images/gbm_train_n01.png)

**Figure 3.:** Model training for GradientBoosting and Normalizer

As mentioned above the training process was also performed for XGBoost

![XGBoost training for Normalizer with SMOTE 0.1](https://github.com/fblaura/FraudD/blob/main/4_Supervised_models/images/xgb_train_n01.png)

**Figure 4:** Model training for XGBoost and Normalizer

From this exercise we observe that XGBoost, despite having changed its scaling, remains the same in its way of predicting fraud labels. On the other hand, for GradientBoosting the situation is different, the scaling is affected by the GradientBoosting model, which is reflected in the result of the confusion matrix. 
