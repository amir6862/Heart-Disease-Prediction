<div align="center">

# 🫀 Heart Disease Prediction

### An intelligent machine learning system to predict the likelihood of heart disease using clinical patient data.

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)](https://matplotlib.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

<br/>

> ⚕️ *Leveraging the power of data science to assist early detection of cardiovascular disease — one of the leading causes of death worldwide.*

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Models Used](#-models-used)
- [Results](#-results)
- [Installation](#-installation)
- [Usage](#-usage)
- [Visualizations](#-visualizations)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🔍 Overview

Heart disease remains the **#1 cause of death globally**, claiming over 17 million lives annually. Early prediction and diagnosis can dramatically improve survival rates.

This project builds a **supervised machine learning pipeline** that:
- Analyzes patient health records and clinical attributes
- Predicts the **presence or absence of heart disease**
- Provides **interpretable insights** for medical decision support
- Compares multiple ML algorithms to find the most accurate model

---

## 📊 Dataset

The project uses the well-known **Cleveland Heart Disease Dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+disease).

| Property        | Detail                          |
|----------------|---------------------------------|
| 📁 Source       | UCI Machine Learning Repository |
| 🧾 Instances    | 303 patient records             |
| 📐 Features     | 13 clinical attributes          |
| 🎯 Target       | Binary (0 = No Disease, 1 = Disease) |

### 🧬 Feature Description

| # | Feature | Description |
|---|---------|-------------|
| 1 | `age` | Age of the patient |
| 2 | `sex` | Gender (1 = Male, 0 = Female) |
| 3 | `cp` | Chest pain type (0–3) |
| 4 | `trestbps` | Resting blood pressure (mm Hg) |
| 5 | `chol` | Serum cholesterol (mg/dl) |
| 6 | `fbs` | Fasting blood sugar > 120 mg/dl |
| 7 | `restecg` | Resting ECG results |
| 8 | `thalach` | Maximum heart rate achieved |
| 9 | `exang` | Exercise-induced angina |
| 10 | `oldpeak` | ST depression induced by exercise |
| 11 | `slope` | Slope of peak exercise ST segment |
| 12 | `ca` | Number of major vessels (0–3) |
| 13 | `thal` | Thalassemia type |

---

## ✨ Features

- ✅ **Data Preprocessing** — Handles missing values, encoding, and normalization
- ✅ **Exploratory Data Analysis (EDA)** — Correlation heatmaps, distribution plots
- ✅ **Multiple ML Models** — Compared side-by-side for best performance
- ✅ **Hyperparameter Tuning** — Grid search / cross-validation
- ✅ **Performance Metrics** — Accuracy, Precision, Recall, F1, ROC-AUC
- ✅ **Confusion Matrix Visualization** — Clear model evaluation
- ✅ **Feature Importance** — Understand which factors matter most

---

## 📂 Project Structure

```
Heart_Disease_Prediction/
│
├── 📁 data/
│   ├── heart.csv                  # Raw dataset
│   └── processed_data.csv         # Cleaned & preprocessed data
│
├── 📁 notebooks/
│   ├── 01_EDA.ipynb               # Exploratory Data Analysis
│   ├── 02_Preprocessing.ipynb     # Data cleaning & feature engineering
│   └── 03_Modeling.ipynb          # Model training & evaluation
│
├── 📁 models/
│   └── best_model.pkl             # Saved trained model
│
├── 📁 visuals/
│   ├── correlation_heatmap.png
│   ├── confusion_matrix.png
│   └── roc_curve.png
│
├── heart_disease_prediction.py    # Main prediction script
├── requirements.txt               # Python dependencies
└── README.md                      # You are here 📍
```

---

## 🤖 Models Used

| Model | Description |
|-------|-------------|
| 🌲 Random Forest | Ensemble method using multiple decision trees |
| 📈 Logistic Regression | Baseline linear classifier |
| 🔵 K-Nearest Neighbors | Distance-based classification |
| ⚙️ Support Vector Machine | Optimal hyperplane classification |
| 🚀 Gradient Boosting | Boosted ensemble for high accuracy |

---

## 🏆 Results

| Model | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|-------|----------|-----------|--------|----------|---------|
| Random Forest | **~88%** | 0.87 | 0.89 | 0.88 | 0.93 |
| Logistic Regression | ~85% | 0.84 | 0.86 | 0.85 | 0.91 |
| SVM | ~86% | 0.85 | 0.87 | 0.86 | 0.92 |
| KNN | ~82% | 0.81 | 0.84 | 0.82 | 0.88 |
| Gradient Boosting | ~87% | 0.86 | 0.88 | 0.87 | 0.93 |

> 📌 *Results may vary slightly based on random seed and train/test split.*

---

## ⚙️ Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/your-username/Heart_Disease_Prediction.git

# 2. Navigate into the project directory
cd Heart_Disease_Prediction

# 3. Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate

# 4. Install required packages
pip install -r requirements.txt
```

---

## 🚀 Usage

### Run Prediction Script

```bash
python heart_disease_prediction.py
```

### Run Jupyter Notebooks

```bash
jupyter notebook notebooks/
```

### Predict for a Single Patient

```python
from heart_disease_prediction import predict

patient_data = {
    'age': 52, 'sex': 1, 'cp': 0, 'trestbps': 125,
    'chol': 212, 'fbs': 0, 'restecg': 1, 'thalach': 168,
    'exang': 0, 'oldpeak': 1.0, 'slope': 2, 'ca': 2, 'thal': 3
}

result = predict(patient_data)
print(f"Heart Disease Risk: {'High 🔴' if result == 1 else 'Low 🟢'}")
```

---

## 📈 Visualizations

The project includes rich visualizations generated during EDA and model evaluation:

| Visual | Description |
|--------|-------------|
| 🔥 Correlation Heatmap | Shows relationships between features |
| 📊 Feature Distribution | Histograms for all 13 features |
| 🎯 Confusion Matrix | True vs Predicted classifications |
| 📉 ROC Curve | Model performance across thresholds |
| 🌲 Feature Importance | Top contributing features (Random Forest) |

---

## 🤝 Contributing

Contributions are welcome and appreciated! 🙌

```bash
# 1. Fork the repository
# 2. Create your feature branch
git checkout -b feature/YourFeature

# 3. Commit your changes
git commit -m "Add YourFeature"

# 4. Push to the branch
git push origin feature/YourFeature

# 5. Open a Pull Request
```

Please make sure to update tests as appropriate and follow the existing code style.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---


⭐ **If you found this project helpful, please give it a star!** ⭐

*Made with ❤️ and Python*

</div>
