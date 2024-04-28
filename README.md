# Image Recognition Task Execution Times in Mobile Edge Computing

## At the University of Pristina
- **Faculty**: Electrical and Computer Engineering
- **Level**: Master's Program
- **Course**: Machine Learning
- **Professor**: Prof. Dr. Lule AHMEDI
- **Assistant**: PhD. Candidate Mërgim HOTI 
- **Student**: Gentrit IBISHI

---

This project undertakes a comprehensive analysis of execution times for image recognition tasks offloaded to various edge servers, including MacBook Pro models, a Raspberry Pi, and a Virtual Machine (VM). The aim is to evaluate the performance and efficiency of mobile edge computing environments in handling image recognition tasks. The dataset and Python code utilized in this analysis are integral to an experimental study designed to benchmark execution times across diverse hardware configurations.

## Dataset Overview

Image Recognition Task Execution Times in Mobile Edge Computing (https://archive.ics.uci.edu/dataset/859/image+recognition+task+execution+times+in+mobile+edge+computing)

The datasets detail the execution times (in seconds) for an image recognition task performed on different machines/edge servers. Four datasets with up to 1K lines, each dataset includes two columns:
- **Local Time**: The timestamp at which the task execution occurred.
- **Execution Time**: The total duration taken to complete the image recognition task.

The tasks were executed using the `imageai.Prediction` machine learning library. The "Turnaround Time" (TAT) encompasses the period from when the image is transferred to the edge server until the image recognition result is received back at the mobile edge node.

### Edge Servers Utilized
- **MacBookPro1**
- **MacBookPro2**
- **Raspberry Pi**
- **Virtual Machine (VM)**

![Edge Servers Informations](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/blob/master/assets/server_information.png)

### Image Specifications
- **Format**: JPEG
- **ColorSpace**: 1
- **Dimensions**: 720 x 405 pixels

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

### Classification
 Through Accuracy, F1-score, Recall and Precision metrics.


## Usage

To replicate this analysis or apply the methodology to similar datasets, ensure the following libraries are installed:

```bash
pip install pandas numpy scikit-learn
```

To initiate the model preparation and training process, execute:

```bash
python model_preparation.ipynb
```

