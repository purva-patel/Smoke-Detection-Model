# Smoke Detection Using IoT Sensor Data
  
**Author:** Purva Patel

---

## Overview

This project demonstrates the application of machine learning models to improve smoke detection using IoT sensor data. The dataset, **`smoke_detection_iot.csv`**, is sourced from Kaggle and contains various environmental sensor readings such as temperature, humidity, gas levels, and particulate matter. The project aims to classify whether smoke is present based on these features, leveraging a range of machine learning techniques.

This project is part of our coursework for **Special Topics in IT - IoT, INFR 4599U** and focuses on comparing the performance of different models in terms of accuracy and other evaluation metrics.

---

## Project Goals

- Implement multiple machine learning models for smoke detection.
- Preprocess and analyze the dataset to handle outliers, skewness, and scaling.
- Evaluate the performance of models using metrics such as accuracy, precision, recall, and F1-score.
- Provide insights into the best-performing model for this classification task.

---

## Dataset Details

- **Dataset Name:** Smoke Detection IoT Sensor Data
- **Source:** Kaggle ([Link to Dataset](https://www.kaggle.com/datasets/deepcontractor/smoke-detection-dataset/data))
- **Features:** 
  - Temperature, Humidity, TVOC, eCO2, PM1.0, PM2.5, etc.
- **Target:** `Fire Alarm` (indicating smoke presence)

---

## Machine Learning Models Used

The following machine learning models were implemented and compared:

1. Random Forest Classifier
2. Logistic Regression
3. Support Vector Classifier (SVC)
4. K-Nearest Neighbors (KNN)
5. Decision Tree Classifier
6. Gradient Boosting Classifier
7. Naive Bayes Classifier

---

## Workflow

### 1. Data Preprocessing
- Capped outliers at the 99th percentile for select features.
- Applied log transformation to reduce skewness in heavily skewed features.
- Created new interaction features: 
  - **Temperature-Humidity Ratio**
  - **Temperature-Humidity Difference**
- Standardized features using `StandardScaler`.

### 2. Model Training and Evaluation
- Split the dataset into training and testing sets.
- Trained each model on the preprocessed data.
- Evaluated the models using metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-Score

---

## Results

Each model was evaluated and compared based on its performance. **Random Forest Classifier** showed the highest accuracy, while **Gradient Boosting** performed comparably well with slightly better interpretability. Logistic Regression, SVC, and Naive Bayes provided good baseline comparisons.

---

## Repository Structure

```
.
├── smoke_detection_project.ipynb  # Main Jupyter Notebook with the complete workflow
├── smoke_detection_iot.csv       # Dataset file
├── README.md                      # Project documentation
```

---

## Prerequisites

1. Python 3.x
2. Libraries:
   - `numpy`
   - `pandas`
   - `matplotlib`
   - `seaborn`
   - `scikit-learn`
   - `notebook` (for Jupyter)

---

## Usage

1. Clone this repository:
   
   ```bash
   git clone www.github.com/purva-patel/Smoke-Detection-Model
   cd Smoke-Detection-Model
   ```
2. Open the Jupyter Notebook:
   
   ```bash
   jupyter notebook smoke_detection_project.ipynb
   ```
3. Run the notebook cells sequentially to reproduce the results.

---

## Acknowledgments

- **Dataset:** [Kaggle](https://www.kaggle.com/datasets/deepcontractor/smoke-detection-dataset/data)  
  

---
