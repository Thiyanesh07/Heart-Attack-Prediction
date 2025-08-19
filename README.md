# ❤️ Heart Attack Prediction 2024 – Data Analysis

## 📖 Overview
This project analyzes the **Heart Attack Prediction 2024** dataset using Python, Pandas, NumPy, Matplotlib, and Seaborn.  
We explore medical and lifestyle factors that contribute to the risk of heart disease and build insights for prediction.

---

## 📂 Dataset Information
**Source:** Public medical dataset (Heart Disease Prediction 2024)  
**Main Features:**
- `age` – Age of the patient
- `sex` – Gender (1 = Male, 0 = Female)
- `cp` – Chest pain type (0–3)
- `trestbps` – Resting blood pressure
- `chol` – Serum cholesterol (mg/dl)
- `fbs` – Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
- `restecg` – Resting electrocardiographic results (0–2)
- `thalach` – Maximum heart rate achieved
- `exang` – Exercise induced angina (1 = yes, 0 = no)
- `oldpeak` – ST depression induced by exercise
- `slope` – Slope of the peak exercise ST segment
- `ca` – Number of major vessels (0–3)
- `thal` – Thalassemia (0–3)
- `target` – Presence of heart disease (1 = yes, 0 = no)

---

## 🗂 Project Structure

### **Part 1 – Basic Data Understanding**
- Load dataset, preview first 10 rows
- Dataset shape, column names, and data types
- Missing values & duplicates check
- Summary statistics
- Count of patients with and without heart disease
- Most common chest pain type

### **Part 2 – Exploratory Data Analysis (EDA)**
- Histogram of age distribution
- Heart disease countplot (target variable)
- Chest pain type vs heart disease (bar chart)
- Cholesterol vs age (scatter plot)
- Boxplot of maximum heart rate by target

### **Part 3 – Statistics**
- Mean, median, mode of `chol` and `age`
- Variance & standard deviation of `thalach`
- % of patients with cholesterol above 200
- Most common factor among heart disease patients

### **Part 4 – Linear Algebra & NumPy**
- Arrays for `age` & `chol`
- Vector operations (addition, subtraction, dot product)
- Matrix multiplication with feature weights
- Normalization of numerical features

### **Part 5 – Calculus**
Formula:  
\[
Risk\_Score = (Chol \times Age) + 0.5 \times (MaxHR - 150)^2
\]  
Find derivative wrt **Chol**.

### **Part 6 – Feature Engineering**
- `is_senior` → 1 if age > 50 else 0
- `high_chol` → 1 if chol > 200 else 0
- `bp_level` → categories: low / normal / high
- Quartiles for `thalach`

### **Part 7 – SQL Simulation in Pandas**
- Patients with heart disease (target = 1)
- Sort by cholesterol (desc)
- Group by chest pain type → avg age
- Top 5 patients with highest max heart rate
- Patients with fasting blood sugar > 120

### **Part 8 – Insights**
- Age group most affected
- Cholesterol–Heart Disease correlation
- Does high blood pressure strongly indicate risk?
- Impact of exercise-induced angina

---

## 🛠 Tech Stack
| Tool / Library   | Purpose |
|------------------|---------|
| Python 3.x       | Main language |
| Pandas           | Data manipulation |
| NumPy            | Numerical operations |
| Matplotlib       | Visualization |
| Seaborn          | Statistical plots |
| Jupyter Notebook | Interactive coding |

---

## 🚀 Getting Started
```bash
# Clone the repository
git clone https://github.com/yourusername/heart-attack-prediction-2024.git

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Run the notebook
jupyter notebook
