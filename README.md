# Image Recognition Task Execution Times in Mobile Edge Computing

## At the University of Pristina
- **Faculty**: Electrical and Computer Engineering
- **Level**: Master's Program
- **Course**: Machine Learning
- **Professor**: Prof. Dr. Lule AHMEDI
- **Assistant**: PhD. Candidate Mërgim HOTI 
- **Student**: Gentrit IBISHI

This project undertakes a comprehensive analysis of execution times for image recognition tasks offloaded to various edge servers, including MacBook Pro models, a Raspberry Pi, and a Virtual Machine (VM). The aim is to evaluate the performance and efficiency of mobile edge computing environments in handling image recognition tasks. The dataset and Python code utilized in this analysis are integral to an experimental study designed to benchmark execution times across diverse hardware configurations.

## Dataset Overview

- **Dataset name:** Image Recognition Task Execution Times in Mobile Edge Computing
- **Dataset link:** (https://archive.ics.uci.edu/dataset/859/image+recognition+task+execution+times+in+mobile+edge+computing)
- **Dataset length:** 4 csv files with 1000 lines of rows.
- **Dataset columns:** Local Time, Execution Time
- **Total datasets lines before preprocessing:** 4000 rows
- **Total datasets lines after preprocessing:** Around 3759 rows based on Classification and Regression
- **Dataset description:** The datasets detail the execution times (in seconds) for an image recognition task performed on different machines/edge servers.
The tasks were executed using the `imageai.Prediction` machine learning library. The "Turnaround Time" (TAT) encompasses the period from when the image is transferred to the edge server until the image recognition result is received back at the mobile edge node.

## Phase I: Data Analysis and Model Preparation

The initial phase of the analysis involves data preprocessing, dataset combination, feature extraction, and constructing a Random Forest Regressor model to decipher the factors influencing execution times.

### Key Steps
1. **Preprocessing**: This step involves imputing missing values, handling outliers, and extracting time-based features.

     ![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/75657075-23bb-4adc-9210-e6659cd0d496)

     ![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/851b88f8-3622-44ca-a204-b57c2c143959)

     ![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/0717b61f-c0fc-446f-b575-bb72ff31e51e)

     ![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/35aa1777-866d-45e5-9c50-544664ecf0f5)

3. **Feature Engineering**: Features such as the hour and day of the week are extracted from the timestamps.
4. **Model Training**: A RandomForestRegressor is employed to predict execution times.
   
     ![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/d5363420-7ab2-490c-bcbd-3f60136b3d05)

     ![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/afc5474b-8ce3-4067-a891-f28d91e68250)

6. **Evaluation**: The model's performance is gauged using metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and the R2 Score.
   
   ![Evaluation Results](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/blob/master/assets/evaluation_results.png)

## Phase II: Analysis and evaluation

During training, the model learns patterns on the data related to the target variable. It is therefore essential to analyze and compare the performance of the model against other algorithms to determine if further additional optimizations are needed. Different splits of test and training data will be analyzed to evaluate performance using two methods:

### Regression
Through MSE and R2 Score metrics.
The types of algorithms we will analyze Linear Regression, Random Forest Regressor and Ridge Regression.
 
![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/488969f2-21dd-471f-aace-44ada09242f7)

### Results for Regression:
---
#### Case I:
The ratio of test and training data is 0.1 to 0.9

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/6470fed1-3651-4d78-b8f4-216b2b88dd0f)

#### Case II:
The ratio of test and training data is 0.2 to 0.8

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/5f69bf23-0e0a-4ac0-b547-6e29f12d3613)

#### Case III:
The ratio of test and training data is 0.3 to 0.7

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/315b2e67-1e0d-4d76-b175-19439c18c0a4)

#### Case IV:
The ratio of test and training data is 0.4 to 0.6

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/6cda3f30-c169-4ee3-a897-1e1a52dc4329)

#### Final Decision

Based on the results generated by these metrics, it appears that Case I (test and training data split ratio of 0.1:0.9) performs slightly better than the other cases for Logistic Regression.

---

### Visualization

#### Mean Squared Error (MSE)

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/c1e194bc-60b1-4e31-996a-c25048ace99b)

#### R2 Score

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/a17b28c9-6a91-4832-b86e-58321f75b723)

---

### Classification
Through Accuracy, F1-score, Recall and Precision metrics.
The types of algorithms we will analyze Logistic Regression, Decision Tree, Random Forest, SVM, KNN and Naive Bayes.

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/f3f8ba8d-118d-4073-963b-aa09ccecf955)

### Results for Classification:
---
#### Case I:
The ratio of test and training data is 0.1 to 0.9

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/f415eeb3-7244-475c-bb7e-3e401dd86333)

#### Case II:
The ratio of test and training data is 0.2 to 0.8

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/4c571290-5756-4adb-bb25-080961f7351c)

#### Case III:
The ratio of test and training data is 0.3 to 0.7

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/ed266d5e-6e7f-4438-a4c9-95b9515ec771)

#### Case IV:
The ratio of test and training data is 0.4 to 0.6

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/e5b88cc0-e3c7-4dab-9e22-18312044d255)

#### Final Decision

Based on the results generated by these metrics, it appears that Case I (test and training data split ratio of 0.1:0.9) performs slightly better than the other cases for Logistic Classification.

---

### Visualization

#### Accuracy

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/6c494f59-c671-4171-a0c4-88991996c178)

#### F1 Score

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/87fab910-b200-45a8-83e4-fc15a7233c1b)

#### Precision

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/f7fe1fae-f661-4470-9549-b74c54c7fa7d)

#### Recall

![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/13bf3222-7ad7-4b64-b92e-d8e6eea85637)

## Why I choose Regression Models?

Predicts exact values (eg, execution time in seconds). This is more accurate and suitable for detailed performance analysis and forecasts that require precise numbers.

## Why Random Forest Regressor?

Random Forest handles complex, non-linear data well and is robust against overfitting, making it reliable even with large or complex datasets. It's also good at determining which features are most important for predictions.

## Phase III - Analysis and evaluation (Retraining) & Application of ML tools

After we added a function which generates 15 thousand new lines completely random:

### Function for generating 15K+ lines random

Function Image here

We retrained the model for both regression and classification methods and obtained these results:

### Regression
Through MSE and R2 Score metrics.
The types of algorithms we will analyze Linear Regression, Random Forest Regressor and Ridge Regression.
 
IMAGE

### Results for Regression:
---
#### Case I:
The ratio of test and training data is 0.1 to 0.9

IMAGE

#### Case II:
The ratio of test and training data is 0.2 to 0.8

IMAGE

#### Case III:
The ratio of test and training data is 0.3 to 0.7

IMAGE

#### Case IV:
The ratio of test and training data is 0.4 to 0.6

IMAGE

### Classification
Through Accuracy, F1-score, Recall and Precision metrics.
The types of algorithms we will analyze Logistic Regression, Decision Tree, Random Forest, SVM, KNN and Naive Bayes.

IMAGE

### Results for Classification:
---
#### Case I:
The ratio of test and training data is 0.1 to 0.9

IMAGE

#### Case II:
The ratio of test and training data is 0.2 to 0.8

IMAGE

#### Case III:
The ratio of test and training data is 0.3 to 0.7

IMAGE

#### Case IV:
The ratio of test and training data is 0.4 to 0.6

IMAGE

## After all results - Decision

After analyzing all the results, we saw that classification with more data performs better than regression, so we decided to use classification for prediction, since it is more accurate, with a larger amount of data.

## Usage

To replicate this analysis or apply the methodology to similar datasets, ensure the following libraries are installed:

```bash
pip install pandas numpy scikit-learn
```

To initiate the model preparation and training process, execute:

```bash
python model_preparation.ipynb --> To see how model is preparing by doing preprocessing steps removing outliers by IQR method, impute missing value with median.
python trainingModelRegressionAlgorithms.ipynb --> To see how is performing Regression Model in a couple of algorithms to predict time excetion.
python trainingModelClassificationAlgorithms.ipynb --> To see how is performing Classification Model in a couple of algorithms to predict time excetion.
python retraining_classification.ipynb --> To see how is performing Classification Model in a couple of algorithms with up to 15K+ lines to predict time excetion.
python retraining_regression.ipynb --> To see how is performing Regression Model in a couple of algorithms with up to 15K+ lines to predict time excetion.
```

