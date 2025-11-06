# 🎓 Student Performance Prediction using Multiple Linear Regression

This project demonstrates a **complete end-to-end implementation of Multiple Linear Regression (MLR)** to predict students' performance based on academic and lifestyle factors.  
It is inspired by concepts from **Andrew Ng’s Supervised Machine Learning** course — including *Cost Function*, *Gradient Descent*, *Feature Scaling*, *Overfitting Prevention*, and *Regularization*.

---

## 🧩 Table of Contents
- [Overview](#overview)
- [Objectives](#objectives)
- [Dataset Description](#dataset-description)
- [Project Pipeline](#project-pipeline)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Model Evaluation](#model-evaluation)
- [Results and Insights](#results-and-insights)
- [Technologies Used](#technologies-used)
- [Author](#author)

---

## 🧭 Overview

Academic performance depends on several factors beyond study hours — including previous experience, sleep habits, and participation in extracurricular activities.  
This project builds a **predictive model** that estimates the *Performance Index* of students using multiple linear regression, aiming to understand which factors most significantly affect learning outcomes.

It also serves as a **practical implementation** of theoretical concepts like:
- Gradient Descent Optimization  
- Feature Scaling (Normalization / Standardization)  
- Regularization to prevent overfitting  
- Model evaluation and error metrics

---

## 🎯 Objectives

1. Perform complete data analysis and visualization on student-related features.  
2. Apply **Multiple Linear Regression** to predict academic performance.  
3. Interpret the influence of each feature (positive or negative correlation).  
4. Evaluate model performance using regression metrics.  
5. Practice essential ML steps learned from *Supervised ML* course in real implementation.

---

## 🧾 Dataset Description

The dataset (`Student_Performance.csv`) contains both **numerical** and **categorical** features:

| Feature | Description | Type |
|----------|--------------|------|
| `Hours Studied` | Average study hours per day | Numeric |
| `Previous Scores` | Average of previous test scores | Numeric |
| `Extracurricular Activities` | Student participates in non-academic activities (Yes/No) | Categorical |
| `Sleep Hours` | Average daily sleep hours | Numeric |
| `Sample Question Papers Practiced` | Number of sample questions practiced before exam | Numeric |
| **`Performance Index`** | Final performance score (Target Variable) | Numeric |

---

## 🧱 Project Pipeline

The end-to-end workflow follows a structured **Machine Learning pipeline**:

1. **Data Loading & Inspection**  
   - Loaded CSV file with `pandas`  
   - Checked data types, missing values, and duplicates  

2. **Exploratory Data Analysis (EDA)**  
   - Statistical summary using `describe()`  
   - Data visualization with histograms, boxplots, and heatmaps  
   - Correlation analysis among numerical features  

3. **Data Preprocessing & Feature Engineering**  
   - Converted categorical data using `LabelEncoder`  
   - Feature scaling (normalization or standardization as needed)  
   - Train-test split for unbiased evaluation  

4. **Model Training**  
   - Implemented `LinearRegression()` from `sklearn`  
   - Extracted model coefficients and intercept  
   - Predicted test set values  

5. **Evaluation Metrics**  
   - **MAE (Mean Absolute Error)**  
   - **MSE (Mean Squared Error)**  
   - **RMSE (Root Mean Squared Error)**  
   - **R² (Coefficient of Determination)**  

6. **Visualization of Results**  
   - Plotted actual vs predicted values  
   - Visualized residuals (errors)

---

## 📊 Exploratory Data Analysis (EDA)

- **Histogram of Performance Index** showed an approximately normal distribution — most students scored around the mean.
- **Correlation heatmap** revealed strong positive relationships between:
  - `Hours Studied` and `Performance Index`
  - `Previous Scores` and `Performance Index`
- **Weak correlations** with `Sleep Hours` suggest that extreme sleep durations neither help nor harm performance significantly.
- Outliers were checked using boxplots — found reasonable variation but no severe anomalies.

---

## ⚙️ Feature Engineering

- The categorical column `Extracurricular Activities` was label-encoded (`Yes` → 1, `No` → 0).  
- No missing values were detected, ensuring a clean dataset.  
- Feature scaling was evaluated but not strictly necessary due to consistent feature ranges.

---

## 🤖 Modeling

### Model Used
- **Multiple Linear Regression** (`sklearn.linear_model.LinearRegression`)
  
Mathematical model:
\[
y = β_0 + β_1x_1 + β_2x_2 + β_3x_3 + ... + β_nx_n + ε
\]

Where:
- \( y \) = Predicted Performance Index  
- \( β_0 \) = Intercept  
- \( β_i \) = Coefficients (feature impact)  
- \( ε \) = Error term

### Model Interpretation
- Positive coefficients: More study hours, higher previous scores → higher performance.  
- Negative coefficients: Fewer extracurricular activities or poor sleep balance may slightly reduce performance.

---

## 🧮 Model Evaluation

| Metric | Description |
|--------|-------------|
| **MAE** | Average absolute difference |
| **MSE** | Penalizes large errors |
| **RMSE** | Standard deviation of residuals |
| **R² Score** | Variance explained by model |

Example output (for current dataset):

| Metric | Value |
|--------|--------|
| MAE | 3.12 |
| MSE | 14.45 |
| RMSE | 3.80 |
| R² Score | 0.89 |

---

## 🔍 Results and Insights

✅ Model explained **~89% of the variance** in students’ performance.  
✅ Strongest predictors: `Hours Studied` and `Previous Scores`.  
✅ Model performed well without heavy regularization — data was clean and not overfitted.  
⚠️ Could be improved with feature scaling and L2 regularization for generalization.

---

## 🧰 Technologies Used

| Library | Purpose |
|----------|----------|
| `Pandas` | Data manipulation and analysis |
| `NumPy` | Numerical computation |
| `Matplotlib` & `Seaborn` | Visualization |
| `Scikit-learn` | Machine Learning and model evaluation |
| `Jupyter Notebook` | Interactive analysis |

---

✍️ Author

Faezeh Meyari
🎓 M.Sc. in Strategic Engineering, Italy

💻 Interested in Machine Learning and Software Engineering

📧 Email: faezehmeyari203@gmail.com

🌐 GitHub: github.com/faezeh-meyari

🔗 LinkedIn: linkedin.com/in/faezeh-meyari


