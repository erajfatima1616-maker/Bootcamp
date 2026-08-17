# Project 1: SMS Spam Classification & Outlier Analysis
## Overview
Classifying SMS messages as **Spam** or **Ham** using Logistic Regression with TF-IDF vectorization. This project evaluates the impact of IQR-based outlier removal on model performance.

## Dataset
 **Total Messages:** 5,572
 **Ham:** 4,825
 **Spam:** 747

## Workflow
1. **Preprocessing:** Text cleaning, feature extraction (char/word/sentence count).
2. **Outlier Removal:** Applied Interquartile Range (IQR) on numerical features (removed 90 rows).
3. **Vectorization & Modeling:** TF-IDF transformation + Logistic Regression.

## Results
| Metric | Before Outliers Removal | After Outliers Removal |
| --- | --- | --- |
| **Accuracy** | 96.4% | 95.9% |
| **Precision** | 100.0% | 99.2% |
| **Recall** | 73.3% | 73.5% |
| **F1 Score** | 84.6% | 84.4% |

> **Key Finding:** Outlier removal slightly decreased accuracy without significantly improving recall, showing that extreme message lengths carry valid signals for spam detection.

# Project 2: Multi-Model Spam Classification Benchmark
## Overview
A comparative analysis of supervised Machine Learning algorithms applied to the preprocessed SMS Spam dataset.
## Models Evaluated
* Support Vector Machine (SVM)
* Naïve Bayes
* Decision Tree Classifier

## Performance Comparison
| Model | Accuracy | Precision | Recall | F1 Score |
| --- | --- | --- | --- | --- |
| **SVM** | **98.09%** | 97.39% | **89.76%** | **93.42%** |
| **Naïve Bayes** | 94.71% | **100.00%** | 65.06% | 78.83% |
| **Decision Tree** | 94.80% | 83.44% | 81.93% | 82.67% |

> **Conclusion:** **SVM** achieved the best overall performance, balancing high precision with the strongest recall and F1 Score.

# Project 3: Decision Tree Classification (Buys Computer Dataset)
## Overview
A categorical classification model that predicts whether a customer will buy a computer based on demographic and credit attributes using Information Gain (Entropy).

## Dataset
* **Source:** Classic "Buys Computer" Dataset (14 instances).
* **Features:** `Age`, `Income`, `Student`, `Credit Rating`.
* **Target:** `Buys Computer` (Yes/No).

## Methodology
1. **Encoding:** Categorical features transformed using One-Hot Encoding (`pd.get_dummies`).
2. **Train-Test Split:** 70% Training / 30% Testing data.
3. **Algorithm:** Scikit-Learn `DecisionTreeClassifier` with `criterion='entropy'`.
4. **Visualizations:** Tree structure diagram, split nodes, and Confusion Matrix.

## Model Evaluation Metrics
| Metric | Score |
| --- | --- |
| **Accuracy** | Evaluated on Test Set |
| **Precision** | Weighted Binary Average |
| **Recall** | Weighted Binary Average |
| **F1 Score** | Harmonic Mean |
