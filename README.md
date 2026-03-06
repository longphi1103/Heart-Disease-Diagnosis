# Heart-Disease-Diagnosis
## 📌 Project Overview
[cite_start]Cardiovascular disease is currently a leading cause of death worldwide, highlighting the critical need for early and accurate diagnostic solutions[cite: 22, 25]. [cite_start]This project investigates the application of various Machine Learning models for heart disease prediction and evaluates the impact of Feature Engineering (FE) and Decision Tree-based Feature Selection (DT) on model performance[cite: 29]. 

[cite_start]This project was developed as "Project 1" at the School of Information and Communication Technology, Hanoi University of Science and Technology[cite: 1, 2, 9].

## 📊 Dataset
[cite_start]The project utilizes the **Heart Failure Prediction** dataset provided by author *fedesoriano* on Kaggle[cite: 35]. 
* [cite_start]**Size:** 918 observations[cite: 38].
* [cite_start]**Features:** 11 medical features including demographic info (age, sex) and clinical metrics (blood pressure, cholesterol, resting ECG, etc.)[cite: 38, 39].
* [cite_start]**Target:** Binary classification indicating the presence (1) or absence (0) of heart disease[cite: 40, 44].

## ⚙️ Methodology

### 1. Data Preprocessing
* [cite_start]**Encoding:** Categorical variables were converted using Label Encoding[cite: 58].
* [cite_start]**Imputation & Scaling:** Missing quantitative values were filled using the median and scaled via `StandardScaler`[cite: 71]. [cite_start]Missing categorical values were filled using the most frequent value and scaled via `MinMaxScaler`[cite: 72]. 
* [cite_start]**Data Splitting:** The dataset was divided into training, validation, and test sets with an 80/10/10 ratio using Stratified Sampling to maintain class balance[cite: 69].

### 2. Feature Engineering (FE)
[cite_start]New interactive features were created to capture the relationship between age and vital signs, including `chol_per_age`, `bps_per_age`, `hr_ratio`, and `age_bin`[cite: 111, 112]. [cite_start]These features were evaluated and ranked using Mutual Information (MI) scores[cite: 114, 115].

### 3. Feature Selection (DT)
[cite_start]A Decision Tree-based selection method was applied to extract feature importance scores[cite: 86, 89]. [cite_start]The Top $K=10$ most significant features were retained to reduce dimensionality and noise[cite: 93, 94]. 

### 4. Machine Learning Models
[cite_start]The following algorithms were implemented and evaluated[cite: 29]:
* K-Nearest Neighbors (KNN)
* Decision Tree
* K-means
* Random Forest
* AdaBoost
* Gradient Boosting
* XGBoost

## 🚀 Key Results
[cite_start]The models were evaluated using Accuracy, Precision, Recall, and F1-Score based on a Confusion Matrix[cite: 312, 320, 325, 330, 335]. Key findings from the test set include:
* [cite_start]**Best Original Performance:** KNN achieved the highest accuracy of 0.91 on the original dataset[cite: 342, 356].
* [cite_start]**Impact of Feature Engineering:** AdaBoost showed excellent compatibility with the newly engineered features (FE), reaching a peak accuracy of 0.91[cite: 342, 352].
* [cite_start]**Impact of Feature Selection:** Combining DT-based selection with the original data (Origin+DT) significantly improved Ensemble models, boosting Random Forest and Gradient Boosting validation accuracy to 0.88[cite: 345, 346]. [cite_start]XGBoost maintained a stable accuracy of 0.88 on the test set under this configuration[cite: 342, 348].

## 🔮 Future Work
* [cite_start]**Filter Optimization:** Replace the single Decision Tree with advanced methods like SHAP or Random Forest Importance to prevent information loss when combined with Feature Engineering[cite: 366].
* [cite_start]**Model Expansion:** Experiment with Tabular Transformer architectures and larger datasets to verify the robustness of the methodology[cite: 367].
* [cite_start]**Automation:** Develop an AutoML pipeline to automatically select the most suitable feature processing techniques for specific algorithms[cite: 368].

## 👨‍💻 Author
* [cite_start]**Name:** Nguyễn Trọng Phi Long [cite: 11]
* [cite_start]**Student ID:** 20235143 [cite: 11]
* [cite_start]**Institution:** Hanoi University of Science and Technology [cite: 1]
