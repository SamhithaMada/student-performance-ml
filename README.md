# Student Performance Prediction using Machine Learning

## 📌 Problem Statement
Predict a student’s final academic performance (G3) based on demographic, family, lifestyle, and previous academic factors.

This project aims to build an interpretable and well-evaluated machine learning model for educational data.

---

## 📊 Dataset
- Source: Student Performance Dataset (UCI / Kaggle)
- Samples: 693 students
- Features: 32
- Target variable: Final grade (G3)

The dataset includes:
- Previous grades (G1, G2)
- Study habits and absences
- Family and socio-economic factors
- School-related attributes

---

## 🛠️ Approach

### 1. Data Exploration
- Verified no missing values
- Observed non-normal distribution with many zero final grades
- Identified strong correlation between previous grades and final grade

### 2. Preprocessing
- Numerical features scaled using `StandardScaler`
- Categorical features encoded using `OneHotEncoder`
- Used `ColumnTransformer` for clean preprocessing
- Prevented data leakage using `Pipeline`

### 3. Models Used
- **Linear Regression** (baseline, interpretable)
- **Random Forest Regressor** (non-linear comparison)

### 4. Evaluation Strategy
- Train–test split (80–20)
- 5-fold cross-validation for reliable performance estimation
- Metrics:
  - RMSE
  - R² score

---

## 📈 Results

### Linear Regression (Final Model)
- Test R² ≈ **0.84**
- Cross-validation mean R² ≈ **0.79**
- Stable and interpretable performance

### Random Forest (Comparison)
- Cross-validation mean R² ≈ **0.78**
- Higher complexity but no significant improvement

---

## 🔍 Key Insights
- Previous academic performance (G2, G1) is the strongest predictor
- Socio-economic and lifestyle features provide marginal refinements
- Linear models are sufficient for this dataset due to strong linear trends
- More complex models did not generalize better

---

## ✅ Final Decision
Linear Regression was selected as the final model due to:
- Comparable or better generalization
- Lower variance
- High interpretability
- Simpler deployment

---

## 📁 Project Structure
student_performance_ml/
│
├── data/
│   └── raw/
│       └── student_performance.csv
│
├── notebooks/
│   └── student_performance.ipynb
│
├── models/
│   └── student_performance_linear_pipeline.pkl
│
└── README.md

Note: The `data/processed/` directory is reserved for future use. In this project, all preprocessing is handled dynamically using scikit-learn pipelines to avoid data leakage and ensure reproducibility.

---

## 🚀 Skills Demonstrated
- Data preprocessing & EDA
- Feature engineering
- Pipelines & cross-validation
- Model comparison
- ML reasoning & decision-making

---

## 📌 Tools & Libraries
- Python
- NumPy, Pandas
- Matplotlib, Seaborn
- scikit-learn
