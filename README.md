# 🩺 Diabetes Prediction using Machine Learning

A machine learning project that predicts whether a patient is **diabetic or non-diabetic** based on key health indicators. Built using Python and Scikit-learn, with full Exploratory Data Analysis (EDA), data visualization, standardization, and an SVM-based predictive system.

---

## 📓 Project Notebook

`Diabetes_project.ipynb` — Single Jupyter Notebook containing the complete end-to-end pipeline.

---

## 📋 Problem Statement

Develop a machine learning model to predict diabetes status (Positive / Negative) of patients based on health features such as Glucose level, BMI, Age, Blood Pressure, and more.

---

## 📊 Dataset

**File:** `diabetes-1.csv`

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration (2-hour oral glucose tolerance test) |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skinfold thickness (mm) |
| Insulin | 2-hour serum insulin (μU/ml) |
| BMI | Body Mass Index (weight in kg / height in m²) |
| DiabetesPedigreeFunction | Diabetes pedigree function score |
| Age | Age of the patient (years) |
| Outcome | Target — `Positive` (diabetic) / `Negative` (non-diabetic) |

**Class Distribution:**
- Negative (Non-diabetic): 500 patients
- Positive (Diabetic): 268 patients

---

## 🔁 Project Pipeline

```
1. Import Libraries
2. Load Dataset (diabetes-1.csv)
3. Exploratory Data Analysis (EDA)
   ├── df.head(), df.info(), df.describe()
   ├── Unique age values
   └── Class distribution (Outcome)
4. Data Visualization
   ├── Histograms (all features)
   ├── Correlation Heatmap
   ├── Box Plot — Glucose vs Outcome
   ├── Box Plot — Age vs Outcome
   └── Scatter Plots — BMI/Age vs Glucose
5. Data Preprocessing
   ├── Label Encoding (Positive→1, Negative→0)
   └── Feature/Target Split (X, y)
6. Data Standardization (StandardScaler)
7. Train/Test Split (80/20, stratified)
8. Model Training (SVM — Linear Kernel)
9. Model Evaluation (Accuracy Score)
10. Predictive System (single patient input)
```

---

## 🤖 Model Used

**Support Vector Machine (SVM)** with a linear kernel from `sklearn.svm.SVC`

- Chosen for its strong performance on small-to-medium sized medical datasets
- Linear kernel works well when classes are approximately linearly separable

---

## 📈 Key Visualizations

- **Histogram** — Distribution of each feature
- **Heatmap** — Correlation between all numerical features
- **Box Plots** — Glucose and Age vs Diabetes Outcome
- **Scatter Plots** — BMI vs Glucose and Age vs Glucose, coloured by Outcome

---

## 🔧 Libraries Used

| Library | Purpose |
|---|---|
| `numpy` | Numerical operations, array handling |
| `pandas` | Data loading and manipulation |
| `matplotlib` | Plotting histograms and scatter plots |
| `seaborn` | Heatmaps, box plots, scatter plots |
| `sklearn` | Preprocessing, model training, evaluation |

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/diabetes-prediction-ml.git
cd diabetes-prediction-ml
```

### 2. Install dependencies
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Launch the notebook
```bash
jupyter notebook Diabetes_project.ipynb
```

### 4. Run all cells
In Jupyter: **Kernel → Restart & Run All**

---

## 🔮 Predictive System

At the end of the notebook, a single patient's data can be entered to get an instant prediction:

```python
input_data = (5, 116, 74, 0, 0, 25.6, 0.201, 30)
# (Pregnancies, Glucose, BloodPressure, SkinThickness,
#  Insulin, BMI, DiabetesPedigreeFunction, Age)
```

**Output:**
```
Person has not diabetes   # or
Person has diabetes
```

---

## 📁 Files in this Repository

```
diabetes-prediction-ml/
├── Diabetes_project.ipynb   # Complete notebook
├── diabetes-1.csv           # Dataset
├── dataset-card.png         # Cover image used in notebook
└── README.md
```

---

## 👤 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/yourusername)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
