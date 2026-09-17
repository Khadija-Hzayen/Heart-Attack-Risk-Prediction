# Comprehensive Heart Disease Prediction & Risk Analysis System

An end-to-end Machine Learning pipeline for predicting heart disease risk from clinical medical attributes, featuring rigorous data preprocessing, statistical feature classification, data cleaning/resampling, and model building.

---

## 📌 Dataset & Kaggle Source

This project uses the **Heart Attack Analysis & Prediction Dataset**, publicly available on Kaggle.

* **Dataset Source:** [Heart Attack Analysis & Prediction Dataset on Kaggle](https://www.kaggle.com/datasets/rashikrahman2/heart-attack-analysis-prediction-dataset)

### Dataset Overview & Features

The dataset comprises 303 patient records with 14 clinical attributes:

| Column Name | Feature Description | Data Type | Value Encoding / Units |
| :--- | :--- | :--- | :--- |
| **`age`** | Patient age | Continuous | Years |
| **`gender`** (`sex`) | Biological sex | Binary Categorical | `1` = Male, `0` = Female |
| **`cp`** | Chest Pain type | Multiclass Categorical | `0`: Typical Angina, `1`: Atypical Angina, `2`: Non-anginal, `3`: Asymptomatic |
| **`trtbps`** | Resting blood pressure | Continuous | mmHg (on admission) |
| **`chol`** | Serum cholesterol | Continuous | mg/dl |
| **`fbs`** | Fasting blood sugar | Binary Categorical | `1` = > 120 mg/dl, `0` = Otherwise |
| **`rest_ecg`** | Resting electrocardiographic results | Multiclass Categorical | `0`: Normal, `1`: ST-T wave abnormality, `2`: Left ventricular hypertrophy |
| **`thalach`** | Maximum heart rate achieved | Continuous | bpm |
| **`exng`** | Exercise-induced angina | Binary Categorical | `1` = Yes, `0` = No |
| **`oldpeak`** | ST depression induced by exercise | Continuous | ST depression relative to rest |
| **`slope`** | Slope of the peak exercise ST segment | Multiclass Categorical | `0`: Upsloping, `1`: Flat, `2`: Downsloping |
| **`ca`** (`caa`) | Number of major vessels colored by fluoroscopy | Multiclass Categorical | Ranges from `0` to `4` |
| **`thal`** (`thall`) | Thalassemia / Blood disorder result | Multiclass Categorical | `0`–`3` categorical levels |
| **`target`** (`output`) | Heart Disease Risk Status | Binary Target | `1` = Higher Risk of Heart Disease, `0` = Lower Risk |

---

## 🚀 Key Project Steps & Workflow

1. **Environment Setup & Imports**: Essential libraries loaded (`pandas`, `numpy`, `matplotlib`, `seaborn`).
2. **Data Shuffling & Index Resetting**: Deterministic random sampling (`random_state=42`) to prevent ordering bias.
3. **Column Standardization**: Renaming raw feature names (`sex` $\rightarrow$ `gender`, `caa` $\rightarrow$ `ca`, `thall` $\rightarrow$ `thal`, `output` $\rightarrow$ `target`).
4. **Data Profiling**: Shape verification (`(303, 14)`), data type audit (`13 int64`, `1 float64`), and non-null validation.
5. **Feature Categorization Pipeline**: Programmatic classification into discrete categorical variables ($<10$ unique values) and continuous numeric variables ($\ge 10$ unique values).
6. **Exploratory Data Analysis (EDA)**: Univariate frequency distributions, statistical summary inspection, and balance checking across target classes.

