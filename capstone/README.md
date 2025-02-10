### Project Title
Could You Be at Risk of Getting Diabetes?

**Author**
@zhujun wang

#### Executive summary
This project explores the use of machine learning techniques to predict the likelihood of diabetes in individuals based on factors such as glucose levels, BMI, age, and other medical features. The goal is to apply various classifiers, compare their performance, and identify the best model for predicting diabetes risk.

#### Rationale
Why should anyone care about this question?
Diabetes is a growing global health concern that affects millions of people. Early prediction and prevention of diabetes can significantly reduce healthcare costs and improve patients' quality of life. Identifying key factors that increase the risk of diabetes and applying machine learning models to predict it can help healthcare providers take early actions to prevent or delay the onset of diabetes.

#### Research Question
What are you trying to answer?
It would be "Can machine learning classifiers accurately predict the likelihood of an individual developing diabetes based on medical and demographic features?"

#### Data Sources
What data will you use to answer you question?
The dataset is located [current repo](/capstone/data/diabetes.csv). 
Originally I am downloading from Kaggle

#### Methodology
What methods are you using to answer the question?
- Data Cleaning
- Feature Scaling and Transformation
- Modeling: Using various machine learning classifiers, including Logistic Regression, K-Nearest Neighbors (KNN), Decision Trees, and Support Vector Machines (SVM), to train models on the data.
- Advance modeling: Apply Eensemble Learning such as random forest, boosting and etc.
- Model Evaluation: Using performance metrics such as Mean Absolute Error (MAE), confusion matrix, and ROC-AUC to compare the effectiveness of each model.

#### Results

What did your research find?
Comparing the single model with key input of Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction and Age, SVM performs the best. And false negatives is import data we need to look at, since the patient need to be cautious of diabetes instead of ignoring it. 
In addition, I employed ensemble learning methods, Random Forest and AdaBoost, to further optimize the model. After fine-tuning the parameters of both Random Forest and AdaBoost, it was found that Random Forest emerged as the best-performing model.

#### Next steps (What suggestions do you have for next steps?)
To improve the sensitivity of the Random Forest model and reduce false negatives, I focused on two key strategies:
- Lowering the positive threshold: By adjusting the decision threshold for classifying diabetes, I made the model more likely to predict positive cases (diabetes), which helps in catching more true positives.
- Increasing class weights: I adjusted the class weights to give more importance to correctly identifying positive cases (diabetes), thus improving the model's ability to correctly classify diabetes and reducing the number of false negatives.
These adjustments helped improve the recall of the model, ensuring that more diabetes cases were correctly identified, even at the cost of slightly increasing false positives.

#### Outline of project

* Introduction
    * Problem description and significance
    * Dataset overview
    * Research objectives
* Data Preprocessing
    * Data cleaning
    * Handling missing values
* Exploratory Data Analysis (EDA)
    * Data visualization
    * Correlation analysis
* Modeling
    * Description of classifiers used (Logistic Regression, KNN, Decision Tree, SVM)
    * Model training and evaluation
* Results and Comparison
    * Performance comparison of models
    * Evaluation metrics (MAE, confusion matrix, ROC curve)
* Conclusion
    * Key findings
    * Suggestions for future work

##### Contact and Further Information
