# 🏥 Healthcare Analysis & Stroke Prediction

A machine learning project focused on analyzing healthcare data and predicting **stroke events** using patient demographic, health, lifestyle, glucose, and BMI-related features.

## 📌 Project Overview

This project analyzes a healthcare dataset containing **9,722 patient records and 18 features**. The workflow includes data exploration, cleaning, outlier handling, categorical encoding, feature engineering, feature scaling, machine learning model development, model comparison, and feature importance analysis.

The main objective is to identify important factors associated with stroke events and develop machine learning models capable of predicting stroke outcomes.

## 🎯 Objectives

* Perform exploratory data analysis (EDA) on healthcare data
* Handle missing values and duplicate records
* Detect and cap numerical outliers using the IQR method
* Encode categorical variables using one-hot encoding
* Engineer meaningful health-risk features
* Apply feature scaling using StandardScaler and MinMaxScaler
* Train and compare multiple classification algorithms
* Evaluate models using accuracy, MSE, R², confusion matrix, precision, recall, and F1-score
* Identify the most influential features using Random Forest feature importance

## 📊 Dataset

The dataset contains **9,722 patient records** with **18 features**, including:

* Age
* Gender
* Hypertension
* Heart disease
* Marital status
* Employment type
* Residence
* Glucose level
* BMI
* Smoking habits
* Stroke event
* Age group
* Risk score
* High glucose indicator
* BMI category
* Lifestyle risk

### Target Variable

**`stroke_event`**

* `0` → No stroke
* `1` → Stroke

## 🔍 Exploratory Data Analysis

EDA was performed to understand the distribution and relationships within the healthcare data.

Key visualizations included:

* Numerical feature distributions
* Stroke event distribution
* Glucose level vs. stroke events
* Boxplots for detecting outliers

## 🧹 Data Preprocessing

The following preprocessing techniques were applied:

* Missing-value detection and imputation using median/mode
* Duplicate removal
* Numerical outlier detection
* **IQR-based outlier capping**
* One-hot encoding of categorical variables
* Removal of irrelevant identifiers such as patient ID
* Feature selection before model training

## ⚙️ Feature Engineering

Several additional health-related features were created:

* **Age Risk**
* **BMI Risk**
* **Glucose Risk**
* **Health Risk Score**
* **Combined Lifestyle Risk**
* **Age × Hypertension Interaction**
* **BMI × Glucose Interaction**

These engineered features were designed to capture additional relationships between patient health characteristics.

## 🤖 Machine Learning Models

Four classification algorithms were trained and compared:

1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Random Forest Classifier**
4. **Gradient Boosting Classifier**

### Model Performance

| Model               |   Accuracy |        MSE |         R² |
| ------------------- | ---------: | ---------: | ---------: |
| Logistic Regression |     77.38% |     0.2262 |     0.0947 |
| Decision Tree       |     80.72% |     0.1928 |     0.2284 |
| **Random Forest**   | **94.50%** | **0.0550** | **0.7799** |
| Gradient Boosting   |     85.14% |     0.1486 |     0.4054 |

### 🏆 Best Performing Model

The **Random Forest Classifier** achieved the highest accuracy of **94.50%** on the test set.

Random Forest classification report:

* **Precision:** 95%
* **Recall:** 94%
* **F1-Score:** 94%

## 📈 Feature Importance

Random Forest feature importance analysis identified the following features as the most influential:

| Feature         | Importance |
| --------------- | ---------: |
| Age             |     48.75% |
| Glucose Level   |     20.67% |
| BMI             |     17.46% |
| Employment Type |      2.92% |
| Gender          |      2.18% |

**Age, glucose level, and BMI** were the most influential features in the trained Random Forest model.

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**

### Machine Learning Techniques

* Logistic Regression
* Decision Tree
* Random Forest
* Gradient Boosting
* One-Hot Encoding
* Standard Scaling
* Min-Max Scaling
* Feature Engineering
* IQR Outlier Capping
* Feature Importance Analysis

## 📁 Project Structure

```text
Healthcare-Analysis/
│
├── healthcare_data.csv
├── healthcare_analysis.ipynb
└── README.md
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Savindi2002/Healthcare-Analysis.git
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the healthcare analysis notebook and run the cells sequentially.

## ⚠️ Disclaimer

This project is developed for **educational and portfolio purposes only**. The machine learning predictions should not be considered a substitute for professional medical diagnosis or clinical decision-making.

## 👩‍💻 Author

**Savindi Hewage**

Data Science Undergraduate
Sabaragamuwa University of Sri Lanka
