# 🩺 Diabetes Prediction Using Machine Learning

A Machine Learning classification project that predicts the likelihood of diabetes in patients using medical diagnostic measurements. This project explores data analysis, preprocessing, model development, hyperparameter optimization, classification threshold tuning, and model evaluation to identify the most suitable predictive model.

## 📌 Project Overview

Diabetes is a chronic medical condition that affects how the body regulates blood glucose levels. Early identification of individuals at risk can support timely medical assessment and intervention.

The objective of this project is to develop and compare multiple supervised Machine Learning classification models to predict whether a patient has diabetes based on medical attributes.

- **Machine Learning Type:** Supervised Learning
- **Problem Type:** Binary Classification
- **Target Variable:** Outcome (0 = Non-Diabetic, 1 = Diabetic)

## 🎯 Project Objectives

- Explore and understand the diabetes dataset.
- Perform Exploratory Data Analysis (EDA).
- Clean and preprocess the dataset.
- Identify important features and patterns.
- Build multiple classification models.
- Optimize model hyperparameters using GridSearchCV.
- Perform classification threshold tuning using Out-of-Fold (OOF) predictions.
- Compare models using multiple evaluation metrics.
- Identify the most suitable model for diabetes prediction.

## 📂 Dataset

This project uses the **Pima Indians Diabetes Dataset**.

The dataset contains medical diagnostic information used to predict whether a patient has diabetes.

### Dataset Features

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure |
| SkinThickness | Triceps skinfold thickness |
| Insulin | 2-Hour serum insulin |
| BMI | Body Mass Index |
| DiabetesPedigreeFunction | Diabetes pedigree function |
| Age | Age of the patient |
| Outcome | Diabetes status (0 or 1) |

## 🛠️ Technologies & Libraries

- **Python** – Programming language
- **NumPy** – Numerical computing
- **Pandas** – Data manipulation and analysis
- **Matplotlib** – Data visualization
- **Scikit-learn** – Machine Learning algorithms, preprocessing, hyperparameter tuning and evaluation
- **Jupyter Notebook** – Interactive development environment

## ⚙️ Project Workflow

### 1. Data Understanding and Exploratory Data Analysis

- Dataset inspection and understanding.
- Analysis of data types and statistical summaries.
- Identification of missing and invalid values.
- Univariate and multivariate analysis.
- Distribution analysis using histograms and boxplots.
- Correlation analysis using Matplotlib visualizations.
- Analysis of relationships between features and the target variable.

### 2. Data Cleaning and Preprocessing

- Handling zero values that represent missing or invalid measurements in selected medical features.
- Missing value treatment using appropriate imputation techniques.
- Identifying and analyzing outliers.
- Preparing features and target variables.
- Applying suitable feature scaling where required.
- Splitting the dataset into training and testing sets.

### 3. Model Building

Four supervised Machine Learning classification algorithms were implemented:

| Algorithm | Description |
|---|---|
| Logistic Regression | Linear classification algorithm |
| K-Nearest Neighbors (KNN) | Distance-based classification algorithm |
| Decision Tree | Tree-based classification algorithm |
| Random Forest | Ensemble learning algorithm |

### 4. Hyperparameter Tuning

GridSearchCV was used to identify suitable hyperparameter combinations for each classification algorithm.

Stratified cross-validation was used to preserve the class distribution across folds.

### 5. Classification Threshold Tuning

Classification threshold optimization was performed using Out-of-Fold (OOF) predicted probabilities.

Different classification thresholds were evaluated to investigate their impact on:

- Precision
- Recall
- F1-Score

The default classification threshold of 0.5 was compared with alternative thresholds to understand the trade-off between identifying diabetic patients and minimizing false positive predictions.

### 6. Model Evaluation

The models were evaluated using the following metrics:

| Metric | Purpose |
|---|---|
| Accuracy | Overall percentage of correct predictions |
| Precision | Proportion of predicted diabetic cases that are actually diabetic |
| Recall | Proportion of actual diabetic cases correctly identified |
| F1-Score | Harmonic mean of Precision and Recall |
| ROC-AUC | Ability to distinguish between the two classes |
| PR-AUC | Overall precision-recall performance |

## 📊 Model Performance Comparison

The following results were obtained after hyperparameter tuning.

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC | PR-AUC |
|---|---:|---:|---:|---:|---:|---:|
| Logistic Regression | 0.7078 | 0.6000 | 0.5000 | 0.5455 | **0.8128** | 0.6726 |
| KNN | **0.7468** | **0.6667** | 0.5556 | 0.6061 | 0.8044 | 0.6572 |
| Decision Tree | **0.7468** | 0.6190 | **0.7222** | **0.6667** | 0.8049 | 0.6048 |
| Random Forest | 0.7338 | **0.6667** | 0.4815 | 0.5591 | 0.8117 | **0.6940** |

### 🏆 Best Performing Model

Based on the current evaluation results, the **Decision Tree Classifier** achieved the highest Recall (72.22%) and F1-Score (66.67%).

Recall is particularly important in this project because identifying diabetic patients who may otherwise be classified as non-diabetic is an important consideration.

Other notable results:

- **Highest Accuracy:** KNN and Decision Tree (74.68%)
- **Highest Precision:** KNN and Random Forest (66.67%)
- **Highest ROC-AUC:** Logistic Regression (81.28%)
- **Highest PR-AUC:** Random Forest (69.40%)

Therefore, Decision Tree is the current preferred model when prioritizing Recall and F1-Score rather than overall performance across every metric.

*Note: These results represent the current model evaluation. Final model selection should also consider performance on an untouched test dataset.*

## 📁 Project Structure

```text
Diabetes-Prediction-ML/
│
├── data/
│   └── diabetes.csv
│
├── notebooks/
│   ├── 01_data_understanding_and_eda.ipynb
│   ├── data cleaning.ipynb
│   └── model_training.ipynb
│
├── models/
│
├── README.md
├── requirements.txt
└── .gitignore
```

## 🚀 Getting Started

Follow these steps to run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/Mesandu2007/Diabetic-Prediction-Model.git
```

### 2. Navigate to the Project Directory

```bash
cd Diabetic-Prediction-Model
```

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

### 4. Activate the Virtual Environment

**Windows:**

```bash
.venv\Scripts\activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Run Jupyter Notebook

```bash
jupyter notebook
```

Open the notebooks inside the `notebooks/` directory and execute the cells in the appropriate order.

## 🔮 Future Improvements

- Experiment with additional classification algorithms such as Support Vector Machines and XGBoost.
- Explore more advanced feature selection techniques.
- Improve model generalization through additional cross-validation experiments.
- Perform further classification threshold optimization.
- Develop an interactive prediction interface using FastAPI.
- Deploy the trained model as a web application.

## ⚠️ Disclaimer

This project is developed for educational and Machine Learning research purposes. Its predictions are not a substitute for professional medical diagnosis, clinical assessment, or medical advice.

## 👨‍💻 Author

**Mesandu**

GitHub: [@Mesandu2007](https://github.com/Mesandu2007)

---

⭐ If you find this project interesting, consider giving the repository a star!
