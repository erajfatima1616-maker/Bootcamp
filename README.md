# Spam Classification Using Machine Learning
## Project Overview
This project focuses on classifying messages as either spam or ham using machine learning. The dataset was preprocessed, analyzed, and used to build a simple classification model.
## Dataset
The project uses an SMS spam classification dataset containing spam and ham messages.
The dataset contains 5,572 messages:
- Ham: 4,825
- Spam: 747
## Steps Performed
1. Data loading and understanding
2. Data pre processing
3. Missing value analysis and removal
4. Text cleaning
5. Feature creation
6. Data visualization
7. Outlier detection using the IQR method
8. Outlier removal
9. Spam classification using Logistic Regression
10. Model performance comparison before and after outlier removal
## Outlier Analysis
Outliers were detected using the IQR method on numerical features such as:
- Character count
- Word count
- Sentence count
A total of 90 rows were removed after outlier analysis.
## Machine Learning Model
The classification model used in this project is:
**Logistic Regression**
TF-IDF was used to convert text messages into numerical features before training the model.
## Results
| Metric | Before Outlier Removal | After Outlier Removal |
|---|---:|---:|
| Accuracy | 96.4% | 95.9% |
| Precision | 100% | 99.2% |
| Recall | 73.3% | 73.5% |
| F1 Score | 84.6% | 84.4% |
## Conclusion
The model achieved good performance in classifying spam and ham messages. After removing outliers, the overall accuracy decreased slightly from 96.4% to 95.9%. This shows that outlier removal did not improve the model performance for this particular dataset, while recall remained almost unchanged.  ## Spam Classification Model
## Spam Classification Model 
This assignment applies different machine learning classification models on the clean preprocessed spam dataset.
### Models Used
- Support Vector Machine (SVM)
- Naive Bayes
- Decision Tree

### Evaluation Metrics
Each model was evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score

### Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| SVM | 98.09% | 97.39% | 89.76% | 93.42% |
| Naive Bayes | 94.71% | 100.00% | 65.06% | 78.83% |
| Decision Tree | 94.80% | 83.44% | 81.93% | 82.67% |

### Best Performing Model 
SVM performed the best overall, achieving the highest accuracy and F1 score among the three models.
## Files
 Spam classification.ipynb  — Complete Colab notebook containing the analysis and machine learning model.
 Spam.csv  — Dataset used for the project.
 spam_classification_models.ipynb - classification models 
