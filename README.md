# predict-user-churn

# Overview
Sparkify is a digital music service similar to Spotify or Pandora. Many of the users stream their favorite songs in Sparkify service everyday, either using free tier that places advertisements in between the songs, or using the premium subscription model where they stream music as free, but pay a monthly flat rate. User can upgrade, downgrade or cancel their service at anytime.

This is a Customer Churn Prediction Problem
So, our job is deep mining the customers' data and implement appropriate model to predict customer churn as follow steps:

* Clean data: fill the nan values , correct the data types, drop the outliers.
* EDA: exploratory data to look features' distributions and correlation with key label (churn).
* Feature engineering: extract and found customer-features and customer-behavior-features; Implement standscaler on numerical features.
* Train and measure models: I choose logistic regression, linear svm classifier, decision tree and random forest classifier to train a baseline model and tuning a better model from best of them. It is worth mentioning that this data is unbalanced because of less churn customers, so we choose f1 score as a metrics to measure models' performance.

# Installation
* Python 3.6
* PySpark ML
* Jupyter

# Results
The baseline of four machine learning methods: Logistic Regression, Linear SVC, Decision Tree Classifier and Random Forest Classifier.


![F1-Score](https://github.com/ankitkohli88/predict-user-churn/blob/main/Screenshot%202021-09-10%20at%2011.34.32%20PM.png?raw=true)


Though the LinearSVC spent more training time, but it can get the highest f1 score 0.702. And the LogisticRegression has a medium training time and f1 score, maybe I can tuning it to get a higher score. So I'll choose LinearSVC and LogisticRegression to tuning, and the result is as follows:

Accuracy: 0.7037037037037037
F-1 Score:0.702075702075702
Time Spent : 125.7 sec
which is 82% less than LinearSVC

Considering this is only a quit mini dataset and our purpose is scaling this up to the total 12G dataset, so, the logistic regression is the best model from now on in this project.

Please check my blog post to get more details, here is the [link](https://kohliankit06.medium.com/sparkify-predict-user-churn-using-spark-4d659922425a).

# References
Dataset provided by Udacity.
