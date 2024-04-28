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

     ![image](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/assets/44057937/e4ff13f5-fa39-4d19-947c-050a2f36c171)

3. **Feature Engineering**: Features such as the hour and day of the week are extracted from the timestamps.
4. **Model Training**: A RandomForestRegressor is employed to predict execution times.
5. **Evaluation**: The model's performance is gauged using metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and the R2 Score.

## Usage

To replicate this analysis or apply the methodology to similar datasets, ensure the following libraries are installed:

```bash
pip install pandas numpy scikit-learn
```

To initiate the model preparation and training process, execute:

```bash
python model_preparation.ipynb
```
## Evaluation Results after Model Preparation

![Evaluation Results](https://github.com/GentritIbishi/Image_Recognition_Task_Execution_Times_in_Mobile_Edge/blob/master/assets/evaluation_results.png)

## Further Analysis and Machine Learning Models

To expand on the analysis, several machine learning models can be leveraged:

1. **For Execution Time Prediction and Server Performance Analysis**
2. **For Task Location Optimization and Load Forecasting**
3. **Exploratory Data Analysis**
