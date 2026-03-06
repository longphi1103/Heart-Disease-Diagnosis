# Heart-Disease-Diagnosis
## 📌 Project Overview
The Problem: Cardiovascular disease is the leading cause of death worldwide. Early and accurate diagnosis is crucial, particularly in low-resource regions.

The Approach: Traditional Machine Learning (ML) models (e.g., Naive Bayes, KNN, Decision Tree) are highly effective for medical diagnosis due to their simplicity and interpretability.

Our Focus: This study evaluates how to improve model performance through advanced data processing. We analyze the impact of Feature Engineering (FE) and Decision Tree-based Selection (DT) on several ML algorithms, including KNN, K-means, Decision Tree, Random Forest, XGBoost, and AdaBoost.

This project was developed as "Project 1" at the School of Information and Communication Technology, Hanoi University of Science and Technology.
## 📊 Dataset
The project utilizes the **Heart Failure Prediction** dataset provided by author *fedesoriano* on Kaggle 
* **Size:** 918 observations.
* **Features:** 11 medical features including demographic info (age, sex) and clinical metrics (blood pressure, cholesterol, resting ECG, etc.)
* **Target:** Binary classification indicating the presence (1) or absence (0) of heart disease.
<img width="1884" height="1288" alt="image" src="https://github.com/user-attachments/assets/2b220062-4f78-4709-820b-6074969b7057" />

## ⚙️ Methodology

### 1. Data Preprocessing
* **Encoding:** Categorical variables were converted using Label Encoding.
* **Imputation & Scaling:** Missing quantitative values were filled using the median and scaled via `StandardScaler`. Missing categorical values were filled using the most frequent value and scaled via `MinMaxScaler`. 
* **Data Splitting:** The dataset was divided into training, validation, and test sets with an 80/10/10 ratio using Stratified Sampling to maintain class balance.

### 2. Feature Engineering (FE)
New interactive features were created to capture the relationship between age and vital signs, including `chol_per_age`, `bps_per_age`, `hr_ratio`, and `age_bin`. These features were evaluated and ranked using Mutual Information (MI) scores.
<img width="1252" height="330" alt="image" src="https://github.com/user-attachments/assets/13195c1f-1fe0-4cec-a881-ec7f86ff0d37" />


### 3. Feature Selection (DT)
A Decision Tree-based selection method was applied to extract feature importance scores. The Top $K=10$ most significant features were retained to reduce dimensionality and noise. 
<img width="1182" height="316" alt="image" src="https://github.com/user-attachments/assets/f9c306e5-82ca-486d-94cd-e2d4db61c0d8" />

### 4. Experiment:
The following algorithms were implemented and evaluated:
* K-Nearest Neighbors (KNN)
* Decision Tree
* K-means
* Random Forest
* AdaBoost
* Gradient Boosting
* XGBoost

## 🚀 Key Results
The models were evaluated using Accuracy, Precision, Recall, and F1-Score. Key findings from the test set include:
* **Best Original Performance:** KNN achieved the highest accuracy of 0.91 on the original dataset.
* **Impact of Feature Engineering:** AdaBoost showed excellent compatibility with the newly engineered features (FE), reaching a peak accuracy of 0.91.
* **Impact of Feature Selection:** Combining DT-based selection with the original data (Origin+DT) significantly improved Ensemble models, boosting Random Forest and Gradient Boosting validation accuracy to 0.88. XGBoost maintained a stable accuracy of 0.88 on the test set under this configuration.

<img width="1696" height="646" alt="image" src="https://github.com/user-attachments/assets/1851fd96-82e1-4dfb-a5ba-85a1638fc896" />


