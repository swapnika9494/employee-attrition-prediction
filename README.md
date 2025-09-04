📌 Introduction
Employee attrition is a critical concern for organizations, impacting productivity, morale, and costs. This project aims to predict whether an employee is likely to leave the company using machine learning techniques and exploratory data analysis (EDA).

Dataset Source: IBM HR Analytics Employee Attrition dataset

Objective: Build a predictive model to help HR teams identify at-risk employees and take preventive measures.

📂 Dataset Overview
We begin by loading and inspecting the dataset:

Checked dataset shape, data types, missing values, and target variable distribution.

Inference:

~1,470 records with 35 features.

Target variable (Attrition) is imbalanced: ~16% "Yes", ~84% "No".

🔍 Exploratory Data Analysis (EDA)
Performed both univariate and bivariate analysis to uncover patterns:

Univariate Analysis: Age, Gender, MonthlyIncome, JobSatisfaction, etc.

Bivariate Analysis: Attrition vs OverTime, DistanceFromHome, JobRole.

Correlation Heatmap: Explored relationships among numeric features.

Key Findings:

Employees working overtime are more likely to leave.

Lower job satisfaction and income correlate with higher attrition.

⚙️ Data Preprocessing
Steps taken to prepare the data for modeling:

Encoded categorical variables using LabelEncoder and OneHotEncoder.

Dropped irrelevant columns: EmployeeCount, EmployeeNumber, StandardHours.

Split data into training and testing sets.

Inference: Cleaned and structured data ready for model training (X_train, X_test, y_train, y_test).

🤖 Model Training
a) Logistic Regression
Trained and evaluated using classification report and confusion matrix.

Inference: High overall accuracy, but poor recall for the "Yes" class.

b) Random Forest
Trained and evaluated similarly.

Inference: Improved performance over Logistic Regression, but still struggles with minority class.

Optional Enhancements: Decision Tree, XGBoost, SMOTE for handling imbalance.

📊 Model Evaluation
Compared models using key metrics:

Model	Accuracy	Precision	Recall	F1-Score
Logistic Regression	~83%	Moderate	Low	Moderate
Random Forest	~84%	Better	Still Low	Better
Confusion matrices reveal models favor predicting "No" due to imbalance.

⭐ Key Insights
Features like OverTime, JobSatisfaction, MonthlyIncome, and YearsAtCompany significantly influence attrition.

Attrition is highly imbalanced (~16% leave).

Predictive models achieve good accuracy (~84%), but recall for "Yes" class needs improvement.

✅ Conclusion & Future Work
This project demonstrates the potential of machine learning in predicting employee attrition and supporting HR decision-making.

Future Enhancements:
Address class imbalance using SMOTE or class weights.

Experiment with advanced models like XGBoost or CatBoost.

Deploy the solution using Streamlit or Flask for real-time HR use.
