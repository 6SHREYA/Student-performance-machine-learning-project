# Student's Performance and Difficulties Prediction

The project revolves around employing machine learning algorithms to forecast whether a student will pass the final exam or not. The dataset utilized is sourced from the UCI Machine Learning Repository.

# Introduction
In the project, the fundamental machine learning techniques are applied to predict whether students, under specific circumstances, would pass their tests. The steps undertaken include:

- **Data Preprocessing:** The data was cleaned and prepared for analysis, addressing issues like missing values and inconsistencies.

- **Data Visualization:** Visualizations such as histograms and box plots were used to explore the data and identify patterns and correlations.

- **Feature Engineering:** New features were created or existing ones were transformed to enhance the predictive power of the model.

- **Model Training:** Three algorithms—Logistic Regression, KNN, and SVM—were trained using the preprocessed data.

- **Model Evaluation:** The performance of each trained model was assessed using various evaluation metrics.

- **Algorithm Comparison:** After evaluating the models, SVM was identified as the most effective algorithm for the task.

- **Model Validation:** The chosen SVM model was validated to ensure its generalizability and performance in real-world scenarios.

These steps represent a structured approach to building and evaluating predictive models for student performance prediction.

# Dataset Processing

Before model training, it's imperative to preprocess the data:

1) Mapping String Values to Numerical Ones:
   For instance, transforming categorical variables like "mother's job" into numerical values ensures compatibility for model training.

2) Feature Scaling:
   Normalizing the range of independent variables, also known as feature scaling or data normalization, aids in converging learning algorithms quickly. However, this process excludes binary columns containing 0's and 1's.

# Dataset Visualization

After preprocessing the dataset, the subsequent step involves visualization to unveil patterns, trends, and correlations that might otherwise go unnoticed. Employing Python libraries like Matplotlib and Seaborn facilitates this process. Visualizing the dataset includes:

   - Plotting distribution histograms to visualize sample occurrences in specific categories.
   - Utilizing boxplots to observe how student status is distributed across each variable.
   - Generating correlation output to identify impactful elements on student status.

# Model Evaluation (Metrics)

Before commencing model training, defining the evaluation metrics is crucial:

1) Confusion Matrix:
   A visual representation of the model's performance, showcasing true positives, false positives, and false negatives.

2) F1 Score:
   Calculated using true positives, false positives, and false negatives, it measures the model's accuracy.

3) ROC Curve:
   A graphical plot illustrating the diagnostic ability of a binary classifier system.

4) ROC Score:
   The area under the ROC curve, with a perfect score of 1 indicating optimal performance.

# Machine Learning Algorithms

After defining the metrics, the project involves training three classifiers: 
- Logistic Regression
- KNN
- SVM.

# Comparison

Upon training the SVM models, comparing the results aids in selecting the most accurate classifier. A tabulated comparison reveals metrics such as training time, accuracy, confusion matrix, F1 score, and ROC AUC score.
This table contains all metrics :

|Metric | Linear kernel |>polynomial kernel  |>gaussian kernel|
| ----------------|---------------|-------------------|:-------------:|
| training time   |   11ms   	  |     7ms	      |      3ms      |
| accuracy %      | 84.375       |   78.125          |    82.8125     |
| confusion matrix|[[15 8][2 39]] | [[12 8][6 38]] |[[10 11][0 43]]|
| f1 score        |  0.82         |        0.74       |    0.77       |
| roc_auc_score   |  0.80         |      0.73         |      0.74     |






# The Most Accurate SVM Classifier

Among the SVM models, the one utilizing the linear kernel emerges as the most accurate. With a training time of 11ms, an accuracy of 84.375%, an F1 score of 0.82, and a ROC AUC score of 0.8, this model demonstrates robust performance in predicting student outcomes.





# Factor Extraction

After model validation, extracting positive and negative factors sheds light on key determinants of student success and failure.

- Factors Helping Students Succeed:
    - Parents' education
    - Guardian
    - Desire for higher education
    - Study time
    - Parents' job

- Factors Leading Students to Failure:
    - Age
    - Health
    - Socializing with friends
    - Absences
    - Past failures

# Conclusion

- Enhancing the educational system is a significant goal for us as student engineers.
- We aim to utilize technologies and study resources such as machine learning materials to develop an innovative solution.
- Our project, titled "Students-performance and difficulties prediction," focuses on predicting student academic status based on various features.
- Key challenges included selecting the best classification algorithm and identifying impactful factors affecting student performance.
- We sought to provide insights into optimal conditions for academic success and prevent failure.
- We explored classification methods including logistic regression, KNN, and SVM.
- Evaluation metrics such as f1 score, ROC curve, and confusion matrix were used to assess model performance.
- SVM emerged as the most effective algorithm with an accuracy of 84%, surpassing KNN and logistic regression.
- Prior to addressing main challenges, we undertook steps such as data processing, visualization, model implementation, and algorithm comparison.

   
