# Data-Science-Project-Breast_Cancer_Classification_ML
# Breast Cancer Classification Using Machine Learning 🎗️

This repository contains an **ML-based breast cancer classification system** using the **Breast Cancer Wisconsin (Original) Dataset**.  
The project evaluates and compares six **machine learning models** to determine the most effective algorithm for **early breast cancer detection**.

---

## 📑 Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Machine Learning Models](#machine-learning-models)
- [Data Preprocessing](#data-preprocessing)
- [Model Evaluation](#model-evaluation)
- [Results and Performance Comparison](#results-and-performance-comparison)
- [How to Use This Repository](#how-to-use-this-repository)
- [Future Work](#future-work)
- [License](#license)

---

## 📌 Introduction
Breast cancer is one of the **most common causes of cancer-related deaths** worldwide. **Early detection significantly improves survival rates**, but traditional diagnostic methods can be slow and error-prone.

This project explores **machine learning algorithms** to classify breast cancer tumors as **benign (non-cancerous) or malignant (cancerous)** using medical attributes.

### 📌 Why Machine Learning for Cancer Detection?
✅ Automates diagnosis for faster results  
✅ Reduces human error in medical screening  
✅ Assists doctors in clinical decision-making  
✅ Can be deployed in **hospitals and low-resource settings**  

---

## 📊 Dataset
### 📌 Breast Cancer Wisconsin (Original) Dataset  
- 📂 **Source**: UCI Machine Learning Repository  
- 🏥 **Collected by**: Dr. William H. Wolberg (University of Wisconsin Hospitals, 1992)  
- 🔢 **Total Instances**: **699 cases**  
- ⚕️ **Attributes**:  
  - **Clump Thickness**  
  - **Uniform Cell Size**  
  - **Uniform Cell Shape**  
  - **Marginal Adhesion**  
  - **Bland Chromatin**  
  - **Bare Nuclei**  
  - **Normal Nucleoli**  
  - **Mitoses**  
  - **Single Epithelial Cell Size**  
- 🎯 **Target Variable**:  
  - `2 = Benign`
  - `4 = Malignant`

---

## 🛠️ Machine Learning Models
This project evaluates the **classification performance of six models**:

| **Algorithm**               | **Type** | **Key Strengths** |
|-----------------------------|----------|------------------|
| **Logistic Regression**     | Linear Model  | Simple & interpretable |
| **Decision Tree**           | Tree-Based | High interpretability |
| **Random Forest**           | Ensemble | Reduces overfitting |
| **Support Vector Machine**  | Kernel-Based | Effective for high-dimensional data |
| **Artificial Neural Network** | Deep Learning | Captures complex patterns |
| **XGBoost**                 | Boosting | Highly optimized, scalable |

---

## 🔧 Data Preprocessing
Before training the models, we performed the following steps:

1️⃣ **Handling Missing Values**  
   - The `Bare Nuclei` column had missing values, which were replaced with the **column median**.  

2️⃣ **Binary Transformation of Target Variable**  
   - The **target variable** was converted to `0 = Benign` and `1 = Malignant` for compatibility with ML models.  

3️⃣ **Data Splitting**  
   - **80% for training** and **20% for testing**, maintaining class distribution (stratified sampling).  

4️⃣ **Feature Normalization**  
   - Standardized data using **StandardScaler** (mean = 0, std = 1) to improve model performance.  

---

## 📈 Model Evaluation
Each model was evaluated based on the following **metrics**:

✅ **Accuracy**: Measures overall correctness  
✅ **Precision**: Proportion of correctly predicted malignant cases  
✅ **Recall (Sensitivity)**: Ability to detect malignant cases  
✅ **F1-Score**: Balances precision and recall  
✅ **ROC-AUC Score**: Measures classification capability  

---

## 📊 Results and Performance Comparison
Here’s a summary of model performance:

| **Model**                    | **Accuracy (%)** | **Precision (%)** | **Recall (%)** | **F1-Score (%)** |
|------------------------------|-----------------|-----------------|--------------|----------------|
| **Logistic Regression**       | 89.2%  | 87%  | 90%  | 88.5% |
| **Decision Tree**             | 92.1%  | 91%  | 93%  | 92% |
| **Random Forest**             | 95.7%  | 96%  | 94%  | 95% |
| **Support Vector Machine**    | 94.3%  | 95%  | 92%  | 93.5% |
| **Artificial Neural Network** | 96.3%  | 97%  | 96%  | 96.5% |
| **XGBoost**                   | 97.1%  | 98%  | 97%  | 97.5% |

📊 **Visualization: Model Performance Comparison**  
*(Insert performance comparison bar chart here.)*

---

## ⚙️ How to Use This Repository
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your_username/Breast_Cancer_Classification_ML.git
cd Breast_Cancer_Classification_ML

# Create virtual environment
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (MacOS/Linux)
source venv/bin/activate

# Install Required Packages
pip install -r requirements.txt

# Run the Project
python main.py

# Run Tests
pytest

