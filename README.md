# Image Recognition Task Execution Times in Mobile Edge Computing

## At the University of Pristina
- **Faculty**: Electrical and Computer Engineering
- **Level**: Master's Program
- **Course**: Machine Learning
- **Author**: Gentrit Ibishi

---

This project undertakes a comprehensive analysis of execution times for image recognition tasks offloaded to various edge servers, including MacBook Pro models, a Raspberry Pi, and a Virtual Machine (VM). The aim is to evaluate the performance and efficiency of mobile edge computing environments in handling image recognition tasks. The dataset and Python code utilized in this analysis are integral to an experimental study designed to benchmark execution times across diverse hardware configurations.

## Dataset Overview

The datasets detail the execution times (in seconds) for an image recognition task performed on different machines/edge servers. Each dataset includes two columns:
- **Local Time**: The timestamp at which the task execution occurred.
- **Execution Time**: The total duration taken to complete the image recognition task.

The tasks were executed using the `imageai.Prediction` machine learning library. The "Turnaround Time" (TAT) encompasses the period from when the image is transferred to the edge server until the image recognition result is received back at the mobile edge node.

### Edge Servers Utilized
- **MacBookPro1**
- **MacBookPro2**
- **Raspberry Pi**
- **Virtual Machine (VM)**

### Image Specifications
- **Format**: JPEG
- **ColorSpace**: 1
- **Dimensions**: 720 x 405 pixels

## Phase I: Data Analysis and Model Development

The initial phase of the analysis involves data preprocessing, dataset combination, feature extraction, and constructing a Random Forest Regressor model to decipher the factors influencing execution times.

### Key Steps
1. **Preprocessing**: This step involves imputing missing values, handling outliers, and extracting time-based features.
2. **Feature Engineering**: Features such as the hour and day of the week are extracted from the timestamps.
3. **Model Training**: A RandomForestRegressor is employed to predict execution times.
4. **Evaluation**: The model's performance is gauged using metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and the R2 Score.

## Usage

To replicate this analysis or apply the methodology to similar datasets, ensure the following libraries are installed:

```bash
pip install pandas numpy scikit-learn
```

To initiate the model preparation and training process, execute:

```bash
python model_preparation.ipynb
```

## Further Analysis and Machine Learning Models

To expand on the analysis, several machine learning models can be leveraged:

1. **For Execution Time Prediction and Server Performance Analysis**
2. **For Task Location Optimization and Load Forecasting**
3. **Exploratory Data Analysis**
