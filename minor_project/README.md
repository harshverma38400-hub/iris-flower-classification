# 🌸 Iris Flower Species Classification

**Minor Project 1 — Supervised Machine Learning**  
**Author:** Harsh Verma  
**AI Club Internship, KIET**

---

## 📌 Problem Statement

Classify iris flowers into three species — *Setosa*, *Versicolor*, and *Virginica* — based on four morphological measurements (sepal length, sepal width, petal length, petal width). This is a multi-class supervised classification problem.

---

## 📂 Repository Structure

```
minor_project/
├── data/
│   └── iris_dataset.csv          # Dataset used
├── model/
│   ├── Logistic_Regression.pkl
│   ├── Decision_Tree.pkl
│   ├── Random_Forest.pkl
│   ├── SVM.pkl
│   ├── KNN.pkl
│   └── scaler.pkl
├── notebook/
│   └── iris_classification.ipynb # Main Jupyter Notebook
├── results/
│   ├── eda_feature_distribution.png
│   ├── eda_correlation_heatmap.png
│   ├── eda_class_distribution.png
│   ├── model_comparison.png
│   ├── model_comparison.csv
│   ├── confusion_matrix_rf.png
│   └── feature_importance.png
└── README.md
```

---

## 📊 Dataset

- **Source:** [UCI Machine Learning Repository – Iris Dataset](https://archive.ics.uci.edu/ml/datasets/iris)
- **Samples:** 150 (50 per class)
- **Features:** 4 numerical features
- **Target:** 3 classes (setosa, versicolor, virginica)
- **Missing Values:** None
- **Duplicates:** 1 (removed)

---

## 🔧 Methodology

### Data Preprocessing
- Loaded dataset using `sklearn.datasets.load_iris`
- Checked for missing values and duplicates
- Applied `StandardScaler` for feature normalization
- Train-Test Split: 80% / 20% (stratified)

### Exploratory Data Analysis
- Feature distribution histograms per species
- Correlation heatmap
- Class distribution bar chart

### Models Trained
| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Logistic Regression | 93.33% | 93.33% | 93.33% | 93.33% |
| Decision Tree | 93.33% | 93.33% | 93.33% | 93.33% |
| Random Forest | 90.00% | 90.24% | 90.00% | 89.97% |
| **SVM (Best)** | **96.67%** | **96.97%** | **96.67%** | **96.66%** |
| KNN | 93.33% | 94.44% | 93.33% | 93.27% |

---

## ✅ Conclusion

- **Best performing model:** Support Vector Machine (SVM) with RBF kernel — **96.67% accuracy**
- Petal length and petal width are the most discriminative features (as shown by Random Forest feature importance)
- All five models achieved >90% accuracy, confirming the dataset is well-structured and separable
- SVM's ability to find optimal hyperplanes in high-dimensional space makes it ideal for this task

---

## 📦 Requirements

```
scikit-learn
pandas
numpy
matplotlib
seaborn
joblib
jupyter
```

Install via: `pip install scikit-learn pandas numpy matplotlib seaborn joblib jupyter`

---

## 🚀 How to Run

```bash
git clone <your-repo-url>
cd minor_project
pip install -r requirements.txt
jupyter notebook notebook/iris_classification.ipynb
```
