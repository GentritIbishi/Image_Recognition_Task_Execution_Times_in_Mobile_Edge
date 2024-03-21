# Image Recognition Task Execution Times in Mobile Edge Computing

## University of Pristina
- **Faculty**: Electrical and Computer Engineering
- **Level**: Master's Program
- **Course**: Machine Learning
- **Author**: Gentrit Ibishi

---

This project conducts a comprehensive analysis of execution times for image recognition tasks offloaded to different edge servers, including MacBook Pro models, a Raspberry Pi, and a Virtual Machine (VM). The primary objective is to evaluate the performance and efficiency of mobile edge computing environments in processing image recognition tasks. The dataset and Python code used for this analysis are part of an experimental study aimed at benchmarking the execution times across various hardware configurations.

## Dataset Overview

The datasets capture the execution times (in seconds) for an image recognition task performed on different machines/edge servers. Each dataset comprises two columns:
- **Local Time**: The timestamp when the task execution occurred.
- **Execution Time**: The total time taken to complete the image recognition task.

The tasks were executed using the `imageai.Prediction` machine learning library. The "Turnaround Time" (TAT) includes the duration from when the image is transferred to the edge server until the image recognition result is received back at the mobile edge node.

### Edge Servers Utilized
- **MacBookPro1**
- **MacBookPro2**
- **Raspberry Pi**
- **Virtual Machine (VM)**

### Image Specifications
- **Format**: JPEG
- **ColorSpace**: 1
- **Dimensions**: 720 x 405 pixels

## Phase I

The analysis encompasses data preprocessing, dataset combination, feature extraction, and the construction of a Random Forest Regressor model to understand the factors influencing execution times. 

### Key Steps
1. **Preprocessing**: This includes imputing missing values, handling outliers, and extracting time-based features.
2. **Feature Engineering**: Extracting features such as the hour and day of the week from the timestamps.
3. **Model Training**: Employing a RandomForestRegressor to predict execution times.
4. **Evaluation**: The model's performance is assessed using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R2 Score.

## Usage

To replicate this analysis or apply the methodology to similar datasets, ensure the required libraries are installed:

```bash
pip install pandas numpy scikit-learn
