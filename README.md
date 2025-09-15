#  Heart Disease Prediction Project

##  Overview
This project applies **Machine Learning techniques** to the [UCI Heart Disease dataset](https://archive.ics.uci.edu/dataset/45/heart+disease).  
The goal is to predict whether a patient has heart disease based on clinical attributes such as age, cholesterol, blood pressure, chest pain type, and more.  

I explored **data preprocessing, dimensionality reduction, feature selection, supervised classification, unsupervised clustering, and hyperparameter tuning** to build a robust prediction model.  
The final best-performing model was an **optimized Support Vector Machine (SVM)**.

---

## ⚙️ Methodology

###  1. Data Preprocessing
- Handled missing values  
- One-hot encoded categorical variables (`sex`, `cp`, `restecg`, `thal`, etc.).  
- Scaled numerical features (`age`, `chol`, `trestbps`, `thalach`, `oldpeak`, `ca`) using **StandardScaler**.  
- Performed **EDA** with histograms, correlation heatmaps, and boxplots to detect distributions and outliers.  

### 2. Dimensionality Reduction (PCA)
- Applied PCA to reduce feature dimensionality while preserving ≥90% variance.  
- Visualized explained variance and PC1 vs PC2 scatter plots.  

### 3. Feature Selection
- Used three methods:
  - **Random Forest feature importance**
  - **Recursive Feature Elimination (RFE)**
  - **Chi-Square test**
- Took the intersection of top features to build a reduced dataset.  

### 4. Supervised Learning
Trained and evaluated:  
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Support Vector Machine (SVM)  

Metrics used:
- Accuracy, Precision, Recall, F1-score  
- ROC Curve and AUC Score  

###  5. Unsupervised Learning
- Applied **K-Means Clustering** (k=2 for binary classification).  
- Performed **Hierarchical Clustering (Agglomerative)**.  
- Compared clusters against actual labels using **ARI** and **NMI**.  

###  6. Hyperparameter Tuning
- Optimized models using **GridSearchCV** and **RandomizedSearchCV**.  
- Best model: **SVM (Optimized)** with highest balanced performance.  

---

## Results

### Best Performing Model → **Optimized SVM**
- **Accuracy:** 0.869  
- **F1-score:** 0.862  
- **ROC AUC:** 0.919  

See [`results/evaluation_metrics.txt`](results/evaluation_metrics.txt) for the full comparison.

