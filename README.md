# Customer Category Classification using Machine Learning

> An end-to-end Artificial Intelligence project focused on predicting customer segments using supervised and unsupervised machine learning models.
> Built for the CSE422: Artificial Intelligence course.

---

## Overview

Understanding customer behavior is one of the biggest challenges in modern business analytics. This project explores how machine learning can classify customers into different segments based on demographic and behavioral data.

The system predicts whether a customer belongs to **Segment A, B, C, or D** using multiple AI models and compares their performance through extensive evaluation metrics and visual analysis.

The project includes:

* Exploratory Data Analysis (EDA)
* Data preprocessing pipeline
* Feature engineering & encoding
* Supervised learning models
* Unsupervised clustering
* Model comparison & evaluation
* Visualization of results and metrics

---

## Dataset

**Dataset:** Customer Category Classifier Dataset
**Total Data Points:** 8,068
**Features:** 11

### Features Used

| Feature         | Type            |
| --------------- | --------------- |
| Gender          | Categorical     |
| Ever_Married    | Categorical     |
| Age             | Numerical       |
| Graduated       | Categorical     |
| Profession      | Categorical     |
| Work_Experience | Numerical       |
| Spending_Score  | Categorical     |
| Family_Size     | Numerical       |
| Var_1           | Categorical     |
| Segmentation    | Target Variable |

### Target Classes

* Segment A
* Segment B
* Segment C
* Segment D

---

# Project Workflow

## 1. Exploratory Data Analysis (EDA)

The project starts with a complete analysis of the dataset:

* Correlation Heatmaps
* Class Distribution Analysis
* Numerical Feature Distributions
* Categorical Feature Analysis
* Density Plots
* Dataset Balance Checking

### Key Observation

The dataset showed:

* Weak linear correlations
* Complex non-linear relationships
* Fairly balanced class distribution

---

## 2. Data Preprocessing

Several preprocessing techniques were applied before training the models.

### Missing Value Handling

Missing values were handled using:

* **Median Imputation** for numerical columns
* **Mode Imputation** for categorical columns

### Encoding Techniques

| Encoding Type    | Applied On           |
| ---------------- | -------------------- |
| Label Encoding   | Binary Features      |
| One-Hot Encoding | Multi-class Features |

### Feature Scaling

`StandardScaler` was used for:

* Age
* Work_Experience
* Family_Size

### Feature Removal

The `ID` column was removed since it had no predictive importance.

---

# Machine Learning Models

## Supervised Learning Models

The following supervised learning algorithms were trained and evaluated:

* K-Nearest Neighbors (KNN)
* Decision Tree
* Random Forest
* Logistic Regression
* Neural Network

---

## Unsupervised Learning

### K-Means Clustering

The project also explored customer grouping using unsupervised learning.

Techniques used:

* Elbow Method
* Cluster Optimization
* K-Means Clustering

Optimal clusters found:

```python
k = 3
```

---

# Model Performance

| Model               | Precision | Recall | F1 Score | AUC    |
| ------------------- | --------- | ------ | -------- | ------ |
| Neural Network      | 0.5357    | 0.5361 | 0.5314   | 0.7911 |
| Random Forest       | 0.5194    | 0.5257 | 0.5166   | 0.7894 |
| Decision Tree       | 0.5058    | 0.5047 | 0.5024   | 0.7614 |
| KNN                 | 0.5040    | 0.5105 | 0.5047   | 0.7617 |
| Logistic Regression | 0.5002    | 0.5072 | 0.4970   | 0.7716 |
| K-Means             | 0.2057    | 0.3783 | 0.2633   | 0.5000 |

---

# Best Performing Model

## Neural Network

The Neural Network achieved the highest overall performance across:

* Precision
* Recall
* F1 Score
* AUC Score

This indicates that the dataset contains complex non-linear relationships which neural networks handle better than traditional linear models.

---

# Visualizations Included

The notebook contains multiple visual analyses including:

* Correlation Heatmaps
* Bar Charts
* Density Plots
* Confusion Matrices
* ROC Curves
* Accuracy Comparison Graphs
* Precision/Recall/F1 Comparison Charts
* Elbow Method Graph

---

# Tech Stack

## Languages & Libraries

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow / Keras
* Jupyter Notebook

---

# Repository Structure

```bash
├── CSE422_Sec21_Group5_Project.ipynb
├── Customer Classification Project Report.pdf
├── Customer_Category_Classifier_Dataset.csv
├── README.md
```

---

# Challenges Faced

Some major challenges during development:

* Designing the Neural Network architecture
* Avoiding overfitting
* Determining optimal cluster count using Elbow Method
* Debugging mixed Random Forest and Neural Network evaluation outputs
* Handling missing and categorical data efficiently

---

# Key Takeaways

* Customer segmentation contains complex non-linear patterns
* Neural Networks and Random Forests outperform simpler models
* Supervised learning significantly outperformed unsupervised clustering
* Proper preprocessing heavily impacts model performance

---

# Future Improvements

Possible future enhancements:

* Hyperparameter tuning using GridSearchCV
* Deep Learning optimization
* Feature selection techniques
* Advanced clustering algorithms
* Deployment as a web application
* Real-time prediction API

---

# Team Members

* **Bishal Golder** — 23201378
* **Md. Minhazul Mowla Talha** — 23201390

---

# Course Information

**Course:** CSE422 — Artificial Intelligence
**Semester:** Spring 2026
**Institution:** BRAC University

---

# Conclusion

This project demonstrates how Artificial Intelligence and Machine Learning techniques can be applied to real-world customer analytics problems. Through extensive experimentation and evaluation, the project highlights the strengths and weaknesses of different models in handling multi-class customer segmentation tasks.

The Neural Network model emerged as the best-performing solution, proving the effectiveness of deep learning approaches for complex classification problems.
