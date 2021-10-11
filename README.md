# Fraud detection on electronic transactions 

This repository is focused on testing different Machine Learning methods and techniques to detect fraud, in this case, on a dataset containing a compendium of electronic transactions related to commerce. This dataset can be downloaded directly from its Kaggle competition "IEEE - CIS Fraud Detection". Throughout the different folders you will find different notebooks where models are tested with different parameters either during training or during scaling, preprocessing, among others. 
Within this project it is possible to find the following folders

 ## Exploration and preprocessing

Here you can find all the notebooks related to the initial analysis of the original dataset. As well as the application of feature engineering, scaling and coding methods. 

## AutoML 

As an initial way to know which classification models to use, an automatic training process (AutoML -H2O) is used. Since different forms of scaling were tested, different notebooks have been included to test the classification models on them. 

## GridSearch and hyperparameter settings 

After choosing the best models GridSearch is used to obtain a definition of the best parameters to help classify our fraud problem appropriately. 

## Training with supervised models

An analysis was done regarding the best scaling and SMOTE rate with supervised classification models (initially chosen by AutoML).

## Feature selection and dimensionality reduction 

Another test we decided to perform was to reduce the dimensionality of the dataset, either from techniques that select the best features or methods that make a transformation of the information by reducing the dimension of the dataset. 

## Autoencoders for classification 

Another method that can be used to reduce dimensionality is to make use of Autoencoders to transform/compress the information in a given information space.

# Information about the original dataset 

As mentioned above, the original dataset comes from a Kaggle competition. For more information about the dataset, access the following Kaggle page: [IEEE -CIS Fraud Detection](https://www.kaggle.com/c/ieee-fraud-detection/)
 

In that competition, the machine learning models evaluated are expected to be able to deal with the large dataset provided. The data comes from e-commerce transactions contained within the Vesta world, containing a wide range of features. Vesta Corporation is the forerunner in guaranteed e-commerce payment solutions.
