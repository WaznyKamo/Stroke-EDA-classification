# Stroke-EDA-classification
Stoke prediction using features like gender, age, work type, bmi and smoking status.

## 1) Data source
It is a publicly available dataset, but the source is confidential

## 2) Data cleaning
For null values there have been used a KNN imputer. For treating categorical variables there have been used three diffrent encoders: One Hot, Ordinal and Weight of Evidence

## 3) Data visualisation
Histograms for numerical data and pie charts for categorical ones.

## 4) Stroke classification
Machine learning models used for comparision:
* Logistic regression
* Decision tree
* Random forest classifier
* AdaBoost
* Support Vector Machine

Model were evaluated based on:
* Accuracy
* Precision
* Recall
* F1 Score
* AUC - Area Under the Receiver Operating Characteristic Curve

In order to balance the data, SMOTE algorithm was implemented

The best performance with accuracy=0.97 and AUC=0.97 on the test split have been achived using Random Forest Classifier with Weight of Evidence encoding. Confusion matrix and feature importances can be seen below:

![stroke_conf_matrix](https://github.com/WaznyKamo/Stroke-EDA-classification/assets/34655004/3a031e46-5b6c-4f20-97c2-e075faadce3c)

![stroke_feature_importances](https://github.com/WaznyKamo/Stroke-EDA-classification/assets/34655004/9e14f14b-3666-4d17-b548-ac617aae67d8)

## 5) Key takeaways
* Diffrent encoders have close to no impact on the model performance
* Predictions on imbalanced data (1:20) have a very high accuracy, but are useless due to not predictiong the stroke
* After balancing the data using SMOTE algorithm, the predicitons greatly improved
* Best results were achieved for Random forest classifier
* The predictions were fairly balanced - 178 I type vs 280 II type errors. Around 1480 datapoint have been accurately classified
* Age was the most important feature, gender was least important. Other features have been fairly similarly impactfull

