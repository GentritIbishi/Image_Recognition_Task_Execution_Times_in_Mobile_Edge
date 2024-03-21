# Image Recognition Task Execution Times in Mobile Edge Computing

### University of Pristina
### Faculty of Electrical and Computer Engineering
### Master
### Machine Learning
### Author: Gentrit Ibishi

This project provides a comprehensive analysis of execution times for image recognition tasks offloaded to different edge servers, including MacBook Pro models, a Raspberry Pi, and a Virtual Machine (VM). The primary goal is to understand the performance and efficiency of mobile edge computing environments in processing image recognition tasks. The dataset and Python code used for analysis are part of an experimental study aimed at benchmarking execution times across various hardware configurations.

## Dataset Overview

The datasets represent execution times (in seconds) for an image recognition task executed on different machines/edge servers. Each dataset contains two columns:
- **Local Time**: The timestamp of the task execution.
- **Execution Time**: The actual time taken to complete the image recognition task.

The image recognition tasks were performed using the `imageai.Prediction` machine learning library. The execution time, or Turnaround Time (TAT), encompasses the duration from transferring the image to the edge server to receiving the image recognition result back to the mobile edge node.

### Edge Servers Used
- MacBookPro1
- MacBookPro2
- Raspberry Pi
- Virtual Machine (VM)

### Image Specifications
- Format: JPEG
- ColorSpace: 1
- Dimensions: 720 x 405

## Analysis

The analysis involves data preprocessing, combining datasets, feature extraction, and building a Random Forest Regressor model to understand the factors influencing execution times. The code snippet details the process from loading datasets, handling missing values, and outlier detection, to model training and evaluation.

### Key Steps
- Preprocessing: Imputing missing values, handling outliers, and extracting time-based features.
- Feature Engineering: Extracting hour and day of the week from timestamps.
- Model Training: Using RandomForestRegressor to predict execution times.
- Evaluation: Assessing model performance with metrics like MAE, MSE, RMSE, and R2 Score.

## Usage

To replicate this analysis or to apply the methodology to similar datasets, ensure you have the required libraries installed:

```bash
pip install pandas numpy scikit-learn
