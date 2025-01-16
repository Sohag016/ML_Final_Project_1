# ML_Final_Project_1
# Predicting Customer Credit Mix - End-to-End Machine Learning Workflow  

This project implements a comprehensive machine learning pipeline to predict customer credit mix using a publicly available dataset. It covers every aspect of the workflow, from data preprocessing to model evaluation and optimization, offering a practical guide to solving classification problems in finance.  

---

## Dataset Overview  

The dataset used for this project was sourced from the following URL:  
[Bank Data CSV](https://raw.githubusercontent.com/rashakil-ds/Public-Datasets/refs/heads/main/Bank%20Data.csv).  

It includes both numerical and categorical features relevant to customer financial behavior, such as credit history, account details, and demographic information.  

---

## Key Steps in the Workflow  

### 1. Data Preprocessing  
- **Handling Missing Values**:  
  - Numeric columns were filled with their respective medians.  
  - Categorical columns were filled with their most frequent values.  
- **Encoding Categorical Variables**:  
  - Categorical features were encoded using `LabelEncoder`.  
- **Scaling Numeric Features**:  
  - Standardized numeric columns using `StandardScaler` for consistent scaling.  
- **Outlier Detection and Removal**:  
  - Identified and removed outliers using the Interquartile Range (IQR) method.  

### 2. Exploratory Data Analysis (EDA)  
- **Descriptive Analysis**:  
  - Provided a statistical summary of the dataset.  
- **Correlation Analysis**:  
  - Visualized feature relationships using a correlation heatmap.  
- **Box Plots**:  
  - Inspected distributions and potential outliers for numeric features.  

### 3. Model Training and Evaluation  
Three machine learning models were trained:  
1. **Logistic Regression**  
2. **Random Forest Classifier**  
3. **Support Vector Classifier (SVC)**  

**Model Performance Metrics**:  
| Model               | Accuracy | Precision | Recall | F1-Score |  
|---------------------|----------|-----------|--------|----------|  
| Logistic Regression | 66.60%  | 56.85%    | 66.60% | 59.95%   |  
| Random Forest       | 76.21%  | 66.08%    | 76.21% | 69.42%   |  
| SVC                 | 68.07%  | 54.63%    | 68.07% | 60.60%   |  

### 4. ROC Curve and AUC Analysis  
- Plotted ROC curves for each model to assess classification performance visually.  

### 5. Hyperparameter Tuning  
- Optimized the Random Forest model using `GridSearchCV`.  
- **Best Parameters**:  
  - `n_estimators`: 300  
  - `max_depth`: 10  
  - `min_samples_split`: 5  

### 6. Cross-Validation and Final Model Performance  
- **Cross-Validation Scores for Random Forest**:  
  `[0.7462, 0.7003, 0.6261, 0.7404, 0.7425]`  
  - **Mean CV Score**: **71.11%**  
- **Final Model Performance (Random Forest)**:  
  - **Accuracy**: 76.82%  
  - **Precision**: 65.23%  
  - **Recall**: 76.82%  
  - **F1-Score**: 68.93%  

---

## Conclusion  

This project demonstrates the successful implementation of an end-to-end machine learning workflow for predicting customer credit mix. The Random Forest model emerged as the best-performing classifier, achieving robust performance metrics and generalizability through cross-validation.  

By leveraging these techniques, businesses can gain valuable insights into customer credit behavior, enabling more informed financial decisions and risk assessments.  

