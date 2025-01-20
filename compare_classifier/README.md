# Goal: Predicting Term Deposit Subscriptions
## Business Understanding
The goal of this analysis is to predict whether a client will subscribe to a term deposit (y = yes) based on client characteristics and campaign-related data. Accurately predicting subscriptions can help the bank optimize marketing campaigns, focus resources on likely subscribers, and improve overall campaign efficiency.

## Data Cleaning and Preparation

- The dataset was thoroughly inspected and cleaned:
  - Clean data: remove duplicate, outlier and filling missing data 
  - Removal of Irrelevant Features: Columns like _unknown were identified as unhelpful and removed.
  - One-Hot Encoding: Categorical variables (e.g., job, education, housing, loan) were transformed into numeric representations for modeling.

##  Descriptive and Inferential Analysis

- Baseline Accuracy: per input data we can establish a baseline accuracy of 88.73%.
- Class Distribution:
  - Clients who did not subscribe: 36,537.
  - Clients who subscribed: 4,639.
  - This imbalance highlights the need for robust models to handle skewed data effectively.
- Feature Analysis e.g:
  - Job Categories: Specific professions like "management" and "technicians" are more likely to subscribe, while "blue-collar" workers show lower subscription rates.
  - Education: Higher education levels (e.g., "university degree") correlate positively with subscriptions per financial status
  - Housing/Loan: Clients without housing or personal loans showed a higher likelihood of subscribing.

## Model Comparisons
- Models Tested: Logistic Regression, K-Nearest Neighbors (KNN), Decision Tree, and Support Vector Machine (SVM).
- Performance Metrics: Each model was evaluated using accuracy, cross-validation scores, and training time.

| Model               | Train Accuracy | Test Accuracy | Train Time        |
|---------------------|----------------|---------------|-------------------|
| Logistic Regression | 88.86%         | 88.21%        | Fast              |
| KNN                 | 88.42%         | 87.66%        | Moderate          |
| Decision Tree       | 88.90%         | 88.22%        | Very Fast         |
| SVM                 | 88.86%         | 88.21%        | Slow              |
- Findings:
  - All models performed similarly in terms of accuracy.
  - The Decision Tree emerged as the most balanced model due to its:
    - High accuracy (88.22% on test data).
    - Fast training time compared to SVM.
    - Strong performance in cross-validation (88.58%).
