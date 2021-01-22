## 1. Project: Udacity's Sparkify User Churn

Sparkify is a virtual company that mimics other music streaming services similar to Spotify or Google Music. The dataset Sparkify has provided, contains a user behavior log from October to November 2018. The main idea of this Sparkify project is to create a machine learning model that can predict churned users. The assignment was to build a model to predict user churn. Predicting churn rates is a challenging and common problem that data scientists and analysts regularly encounter in any customer-facing business.
This project is a part of Udacity's Data Scientist Nanodegree program.

## 2. Installation

1. Local

Spark, PySpark and python libraries: numpy, pandas, matplotlib, seaborn, sckit-learn, and statsmodels installed.

2. Cloud

I used AWS EMR cluster 5.30.1. (this was the only version that worked well with required python libaries as above)
3 instances (1 master + 2 cores) m5.xlarge, 4 vCore, 16 GiB memory, EBS only storage, EBS Storage:64 GiB

Check notebook Sparkify_AWS_EMR.ipynb for configurations and installation code for python libraries. 

## 3. Data
The dataset contains user activity logs between two months, October and November 2018. The dataset has 26,259,199 rows and 18 columns (12GB). It is located in s3: ``'s3n://udacity-dsnd/sparkify/sparkify_event_data.json'``

## 4. Files

The main commented notebook is Sparkify_AWS_EMR.

1. Sparkify_ETL_EDA
Includes the exploratory data analysis (EDA) and extract, transform and load (ETL) process. Processed in the AWS EMR cluster, includes charts made with Databricks.

2. Sparkify_ML
Exploratory Data Analysis (EDA) and ETL with AWS EMR cluster. Includes features selecting process for machine learning models and create the pipeline for models and make conclusions with metrics. Processed in Udacity's workspace.

3. Sparkify_AWS_EMR
The whole process including ETL, EDA, feature engineering, machine learning models and conclusions. Processed in AWS EMR cluster.

## 5. Results

Three models were built: Logistic Regression Classifier, Random Forest Classifier, and Gradient Boosted Tree Classifier. As we evaluated the models with Cross-Validation and fine-tuned hyperparameters, we find out the best model. 

The best model was:
Random Forest Classifier with metrics F1-score 0.765, accuracy 0.769, areaUnderROC: 82.94%.
