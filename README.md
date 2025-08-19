❤️ Heart Attack Prediction 2024 – Data Analysis & Insights
📖 Overview

This project explores the Heart Attack Prediction 2024 dataset to understand key factors influencing heart disease.
Using Python, Pandas, NumPy, Matplotlib, and Seaborn, we perform EDA, statistics, feature engineering, and visualizations to derive insights.

📂 Dataset Information

Source: Heart Attack Prediction Dataset (2024)
Main Features:

age – Age of the patient

sex – Gender (1 = Male, 0 = Female)

cp – Chest pain type (0–3)

trestbps – Resting blood pressure (mm Hg)

chol – Serum cholesterol (mg/dl)

fbs – Fasting blood sugar > 120 mg/dl (1 = True, 0 = False)

restecg – Resting electrocardiographic results (0–2)

thalach – Maximum heart rate achieved

exang – Exercise induced angina (1 = Yes, 0 = No)

oldpeak – ST depression induced by exercise

slope – Slope of peak exercise ST segment

ca – Number of major vessels (0–3) colored by fluoroscopy

thal – Thalassemia (0 = Normal, 1 = Fixed defect, 2 = Reversible defect)

target – Heart disease (1 = Yes, 0 = No)

🗂 Project Structure
Part 1 – Basic Data Understanding

Preview first 10 rows

Dataset shape, column names, and data types

Missing values & duplicates check

Summary statistics

Distribution of target (disease vs no disease)

Part 2 – Exploratory Data Analysis (EDA)

Age distribution histogram

Gender vs heart disease (bar chart)

Chest pain type distribution (countplot)

Cholesterol & blood pressure analysis

Correlation heatmap of all features

<img width="800" alt="heatmap" src="https://github.com/user-attachments/assets/xxx" />
Part 3 – Statistics

Mean, median, mode of age & cholesterol

Variance & standard deviation of blood pressure

Percentage of patients with heart disease

Most common chest pain type among patients with heart disease

Part 4 – NumPy & Linear Algebra

Arrays for age, cholesterol, and thalach

Vector addition, subtraction, dot product

Matrix multiplication with weights [0.4, 0.6]

Normalization of cholesterol values

Part 5 – Feature Engineering

is_elderly → 1 if age > 50 else 0

high_chol → 1 if cholesterol > 200 else 0

high_bp → 1 if trestbps > 130 else 0

Risk score feature using weighted combination

Part 6 – SQL-like Queries in Pandas

Patients with cholesterol > 240

Patients grouped by gender → avg heart rate

Top 5 ages with highest disease prevalence

Count of patients with normal vs abnormal ECG

Part 7 – Insights

Age group most prone to heart disease

Does gender affect heart disease probability?

Impact of cholesterol and blood pressure

Correlation between exercise-induced angina & disease

<img width="900" alt="eda" src="https://github.com/user-attachments/assets/yyy" />
🛠 Tech Stack
Tool / Library	Purpose
Python 3.x	Main language
Pandas	Data manipulation
NumPy	Numerical operations
Matplotlib	Visualization
Seaborn	Statistical plots
Jupyter Notebook	Interactive coding
🚀 Getting Started
# Clone the repository
git clone https://github.com/yourusername/heart-attack-prediction-2024.git

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Run the notebook
jupyter notebook
