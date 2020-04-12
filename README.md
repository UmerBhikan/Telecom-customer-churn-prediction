# Telecom-customer-churn-prediction
Model which can predicts in terms of a probability for each loan transaction, whether the customer will be paying back the loaned amount within 5 days of insurance of loan.

#DOCUMENTATION

1) Importing necessary libraries and reading the data file.

2) Exploratory Data Analysis and Data preprocessing\n
 Looking for missing values.
 Dropping out unrequired variables. ("Unnamed: 0", "msidn", "pcircle", "pdate").
 Scaling the data using Normalizer().
 Feature selection: Selecting important features out of the predictor variables using
feature ranking with recursive feature elimination(RFE).
 Plotting the "Delinquency Ratio" pie chart using plotly package.
 Plotting the "Box plot" of target variable Vs top for important predictor variables.

3) Model Selection
 Modeling using various classifiers (Logistic Regression, Random Forest classifier,
Decision Tree classifier, Naive Bayes classifier, Support Vector classifier)
 Calculating the results using classification_report().
 Calculating and plotting the confusion matrix using a heatmap.
 Plotting ROC curve for each model.

4) Evaluating the models by comparing the results and selecting the best model.
As the Random Forest Classifier has the highest accuracy score of 0.90 & AUC_ROC score
of 0.71 as compared to other models, thus we will use Random Forest Classifier for final
modeling along with the hyperparameter tuning.

5) Hyperparameter Tuning
 Tuning the hyperparameter of the Random Forest Classifier using
RandomizedSearchCV.
 We obtain the following best parameteres. {'bootstrap': True,'criterion':
'gini','max_depth': None,'max_features': 5,'min_samples_split': 10}.

6) Final Modeling
 Modeling using Best parameters.
 Evaluate the model using the classification_report() and confusion matrix.

7) Conclusion
 The final model has an Accuracy of 0.91 and AUC_ROC score of 0.70.
 we also have....
True Negative = 3432
False Positive = 1355
False Negative = 4476
True Positive = 53615
 Also, we had low Type-1 Error as FP is less.
