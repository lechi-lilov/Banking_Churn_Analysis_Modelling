# Bank Customer Churn Prediction 🏦📉

This project aims to predict whether a bank customer will leave the bank (churn) based on their credit score, demographics, and account activity. It provides a comparative analysis between **Decision Tree** and **Random Forest** classifiers, optimized through extensive hyperparameter tuning.

## 🚀 Project Highlights
* **Feature Engineering:** Derived new features like `Total_Products` and `Account_Balance` to capture customer behavior more effectively.
* **Data Balancing:** Addressed significant class imbalance using **SMOTE** (Synthetic Minority Over-sampling Technique), increasing the training set from 8,000 to 12,712 samples.
* **Statistical Optimization:** Applied **Log Transformation** to the `Age` feature to handle right-skewness and improve model convergence.
* **Optimization:** Used **GridSearchCV** with 5-fold cross-validation to find the ideal hyperparameters for both tree-based models.

## 🛠️ Tech Stack
* **Python**
* **Pandas & NumPy** (Data Manipulation)
* **Matplotlib & Seaborn** (Advanced EDA)
* **Scikit-learn** (Machine Learning & Evaluation)
* **Imbalanced-learn** (SMOTE)

## 📊 Modeling Pipeline
1. **Exploratory Data Analysis (EDA):** Identified key drivers of churn, such as Age, Geography (Germany), and Number of Products.
2. **Preprocessing:** - Dropped irrelevant features (`RowNumber`, `CustomerId`, `Surname`).
   - Performed **One-Hot Encoding** on categorical variables.
   - Handled skewed data via Log Transformation.
3. **Resampling:** Balanced the target variable (`Churned`) to ensure the model doesn't overfit the majority class.
4. **Hyperparameter Tuning:** Optimized `max_depth`, `min_samples_leaf`, and `n_estimators`.

## 🤖 Model Performance

### Decision Tree Classifier
* **Training Accuracy:** 83.2%
* **Testing Accuracy:** 79.15%
* **AUC Score:** 0.77
* **Top Predictors:** Age, Total Products, and Geography.

### Random Forest Classifier (Optimized)
* **Testing Accuracy:** 78%
* **AUC Score:** 0.82
* **Top Predictors:** Age, Total Products, IsActiveMember.

> **Note:** While Random Forest had a slightly lower raw accuracy, its **AUC (0.82)** suggests it is better at distinguishing between churners and non-churners compared to the basic Decision Tree.

## 📈 Key Insights from EDA
* **Age:** Older customers show a higher tendency to churn.
* **Geography:** Customers in Germany have a significantly higher churn rate compared to France and Spain.
* **Products:** Customers with more than two products are highly likely to exit.

## ⚙️ Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/lechi-lilov/Churn-Modelling.git](https://github.com/lechi-lilov/Churn-Modelling.git)
