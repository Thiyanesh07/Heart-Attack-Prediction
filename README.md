<!-- README.html: Professional HTML README for GitHub -->

<div align="center">
  <h1 style="margin-bottom:0.2rem">Heart Disease Prediction Dataset</h1>
  <p style="margin-top:0; color:#57606a; font-size:1.05rem">A compact, well-documented clinical dataset for modeling heart disease risk</p>

  <!-- Badges -->
  <p>
    <a href="https://img.shields.io/badge/Made%20with-Python-3776AB?logo=python&logoColor=white"><img alt="Python" src="https://img.shields.io/badge/Made%20with-Python-3776AB?logo=python&logoColor=white"></a>
    <a href="#license"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-green.svg"></a>
    <a href="#dataset"><img alt="Rows" src="https://img.shields.io/badge/rows-23-informational"></a>
    <a href="#dataset"><img alt="Columns" src="https://img.shields.io/badge/columns-14-informational"></a>
  </p>
</div>

<hr style="border:none; border-top:1px solid #d0d7de; margin: 1.2rem 0;"/>

<!-- Overview -->
<section id="overview">
  <h2>Overview</h2>
  <p>
    This repository hosts a <strong>heart disease dataset</strong> containing demographic and clinical attributes
    frequently used in cardiovascular risk modeling. The dataset is ideal for hands‑on exercises in
    <em>data cleaning, exploratory analysis, feature engineering, and supervised learning</em>.
  </p>
  <ul>
    <li><strong>File:</strong> <code>heart_disease.csv</code></li>
    <li><strong>Instances:</strong> 23 rows</li>
    <li><strong>Features:</strong> 14 columns</li>
    <li><strong>Target:</strong> <code>target</code> (continuous value in [0, 1], higher ≈ higher risk)</li>
  </ul>
</section>

<!-- Data Dictionary -->
<section id="schema">
  <h2>Data Dictionary</h2>
  <table>
    <thead>
      <tr>
        <th>Column</th>
        <th>Type</th>
        <th>Description</th>
        <th>Encoding / Range</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><code>age</code></td><td>int</td><td>Age of the patient (years)</td><td>e.g., 34–71</td></tr>
      <tr><td><code>sex</code></td><td>binary</td><td>Biological sex</td><td>0 = female, 1 = male</td></tr>
      <tr><td><code>cp</code></td><td>categorical</td><td>Chest pain type</td><td>0 = typical angina, 1 = atypical angina, 2 = non‑anginal pain, 3 = asymptomatic</td></tr>
      <tr><td><code>trestbps</code></td><td>int</td><td>Resting blood pressure (mm Hg)</td><td>typical range 90–200</td></tr>
      <tr><td><code>chol</code></td><td>int</td><td>Serum cholesterol (mg/dL)</td><td>typical range 100–600</td></tr>
      <tr><td><code>fbs</code></td><td>binary</td><td>Fasting blood sugar &gt; 120 mg/dL</td><td>0 = false, 1 = true</td></tr>
      <tr><td><code>restecg</code></td><td>categorical</td><td>Resting ECG results</td><td>0 = normal, 1 = ST‑T abnormality, 2 = probable/definite LVH</td></tr>
      <tr><td><code>thalach</code></td><td>int</td><td>Maximum heart rate achieved</td><td>e.g., 106–192 bpm</td></tr>
      <tr><td><code>exang</code></td><td>binary</td><td>Exercise‑induced angina</td><td>0 = no, 1 = yes</td></tr>
      <tr><td><code>oldpeak</code></td><td>float</td><td>ST depression induced by exercise (relative to rest)</td><td>non‑negative real</td></tr>
      <tr><td><code>slope</code></td><td>categorical</td><td>Slope of the peak exercise ST segment</td><td>0 = upsloping, 1 = flat, 2 = downsloping</td></tr>
      <tr><td><code>ca</code></td><td>int</td><td>Number of major vessels colored by fluoroscopy</td><td>0–3</td></tr>
      <tr><td><code>thal</code></td><td>categorical</td><td>Thalassemia status</td><td>1 = fixed defect, 2 = normal, 3 = reversible defect</td></tr>
      <tr><td><code>target</code></td><td>float</td><td>Heart‑disease risk score (probability‑like)</td><td>0.0–1.0</td></tr>
    </tbody>
  </table>
  <p style="margin-top:0.5rem; color:#57606a;">
    <strong>Note:</strong> Unlike the classic UCI “Heart Disease” label (0/1), here <code>target</code> appears continuous
    between 0 and 1. Treat it as a regression target or threshold it for classification.
  </p>
</section>

<!-- Dataset Preview -->
<section id="dataset">
  <h2>Dataset Preview</h2>
  <details>
    <summary>Click to expand first 10 rows</summary>

<pre>
age,sex,cp,trestbps,chol,fbs,restecg,thalach,exang,oldpeak,slope,ca,thal,target
52,1,0,125,212,0,1,168,0,1,2,2,3,0.23
53,1,0,140,203,1,0,155,1,3.1,0,0,3,0.37
70,1,0,145,174,0,1,125,1,2.6,0,0,3,0.24
61,1,0,148,203,0,1,161,0,0,2,1,3,0.28
62,0,0,138,294,1,1,106,0,1.9,1,3,2,0.21
58,0,0,100,248,0,0,122,0,1,1,0,2,0.78
58,1,0,114,318,0,2,140,0,4.4,0,3,1,0.37
55,1,0,160,289,0,0,145,1,0.8,1,1,3,0.17
46,1,0,120,249,0,0,144,0,0.8,2,0,3,0.25
54,1,0,122,286,0,0,116,1,3.2,1,2,2,0.23
</pre>
  </details>
</section>

<!-- Quick Start -->
<section id="quickstart">
  <h2>Quick Start</h2>

  <h3>Python</h3>
  <pre><code>import pandas as pd

# Load dataset
df = pd.read_csv("heart_disease.csv")

# Basic info
print(df.shape)
print(df.describe(include="all"))

# Ensure numeric dtypes where expected
numeric_cols = ["age","trestbps","chol","thalach","oldpeak","ca","target"]
df[numeric_cols] = df[numeric_cols].apply(pd.to_numeric, errors="coerce")

# Optional: convert encoded categoricals to category dtype
for c in ["sex","cp","fbs","restecg","exang","slope","thal"]:
    df[c] = df[c].astype("category")
</code></pre>

  <h3>R</h3>
  <pre><code>library(readr)
library(dplyr)

df &lt;- read_csv("heart_disease.csv")
str(df)
summary(df)
</code></pre>
</section>

<!-- EDA Examples -->
<section id="eda">
  <h2>Reproducible EDA Examples</h2>
  <p>Generate and save the following charts in an <code>assets/</code> folder, then reference them here.</p>

  <h3>1) Correlation Heatmap (numeric features)</h3>
  <pre><code>import pandas as pd
import matplotlib.pyplot as plt

num = df.select_dtypes(include=["number"])  # pandas &gt;= 1.0
corr = num.corr(numeric_only=True)
plt.figure(figsize=(8,6))
plt.imshow(corr, interpolation="nearest")
plt.xticks(range(len(corr.columns)), corr.columns, rotation=45, ha="right")
plt.yticks(range(len(corr.columns)), corr.columns)
plt.title("Correlation Heatmap")
plt.colorbar()
plt.tight_layout()
plt.savefig("assets/corr_heatmap.png", dpi=160)
</code></pre>
  <p><em>Preview:</em></p>
  <p><img src="assets/corr_heatmap.png" alt="Correlation heatmap" width="640" loading="lazy"></p>

  <h3>2) Age Distribution by Risk (binned)</h3>
  <pre><code>import numpy as np
import matplotlib.pyplot as plt

bins = np.arange(df["age"].min(), df["age"].max() + 5, 5)
risky = df[ df["target"] &gt;= 0.5 ]["age"]
safe  = df[ df["target"] &lt;  0.5 ]["age"]

plt.figure()
plt.hist([safe, risky], bins=bins, label=["target &lt; 0.5","target ≥ 0.5"], stacked=True)
plt.xlabel("Age (years)")
plt.ylabel("Count")
plt.title("Age Distribution by Risk Bin")
plt.legend()
plt.tight_layout()
plt.savefig("assets/age_by_risk.png", dpi=160)
</code></pre>
  <p><em>Preview:</em></p>
  <p><img src="assets/age_by_risk.png" alt="Age by risk" width="640" loading="lazy"></p>

  <h3>3) Cholesterol vs Max Heart Rate</h3>
  <pre><code>import matplotlib.pyplot as plt

plt.figure()
plt.scatter(df["chol"], df["thalach"], s=32)
plt.xlabel("Cholesterol (mg/dL)")
plt.ylabel("Max Heart Rate (bpm)")
plt.title("Cholesterol vs Max Heart Rate")
plt.tight_layout()
plt.savefig("assets/chol_vs_thalach.png", dpi=160)
</code></pre>
  <p><em>Preview:</em></p>
  <p><img src="assets/chol_vs_thalach.png" alt="Chol vs Thalach" width="640" loading="lazy"></p>
</section>

<!-- Modeling Ideas -->
<section id="modeling">
  <h2>Modeling Ideas</h2>
  <ul>
    <li><strong>Regression:</strong> predict continuous <code>target</code> using linear models, tree‑based models, or ensembles.</li>
    <li><strong>Classification:</strong> set a threshold (e.g., 0.5) to derive a binary label, evaluate with ROC‑AUC, F1.</li>
    <li><strong>Feature engineering:</strong> interaction terms (e.g., <code>age×trestbps</code>), binning, standardization.</li>
    <li><strong>Validation:</strong> use stratified K‑folds if converting to classification; otherwise K‑fold for regression.</li>
  </ul>
</section>

<!-- Project Structure -->
<section id="structure">
  <h2>Suggested Repository Structure</h2>
  <pre><code>.
├── heart_disease.csv
├── README.md  (this file can be pasted as HTML in README.md)
├── notebooks/
│   └── 01_eda.ipynb
├── scripts/
│   └── make_charts.py
└── assets/
    ├── corr_heatmap.png
    ├── age_by_risk.png
    └── chol_vs_thalach.png
</code></pre>
</section>

<!-- Citation / License -->
<section id="license">
  <h2>License & Attribution</h2>
  <p>
    This dataset and documentation are released under the <a href="#">MIT License</a>. If you use this dataset in a
    project or publication, please cite the repository and provide a link back.
  </p>
  <blockquote style="border-left:4px solid #d0d7de; padding-left:0.8rem; color:#57606a;">
    YourName (2025). <em>Heart Disease Prediction Dataset</em>. GitHub repository. URL: &lt;repo‑link&gt;
  </blockquote>
</section>

<!-- Footer Note -->
<p align="center" style="color:#57606a; font-size:0.95rem;">
  🔎 Tip: GitHub README supports raw HTML. You can paste this entire block into <code>README.md</code> to render as shown.
</p>
