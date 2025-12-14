# Titanic-Survial

# Overview
This project aims to predict the survival of passengers on the Titanic using machine learning. The solution utilizes an Ensemble Voting Classifier that combines the strengths of three distinct algorithms: Logistic Regression, Random Forest, and Support Vector Classifier (SVC) to achieve higher accuracy and generalization than any single model alone.

# Methodology
1. Data Preprocessing
Before feeding the data into the models, the following preprocessing steps were applied:

A. Handling Missing Values: Imputed missing Age values using the median & Fare values using median and filled missing Embarked values with the mode.
B. Feature Engineering:Feature extraction from the Name column (extracting titles like Mr., Mrs., Master). Created new features such as Family_Members (SibSp + Parch) & IsAlone.
C. Encoding: Applied One-Hot Encoding to categorical variables (Sex, Embarked, Name).
D. Scaling: Applied StandardScaler to numerical features (crucial for Logistic Regression and SVC).

2. Models Used
We employed three different types of classifiers to ensure diversity in the ensemble:

A. Logistic Regression: A linear model that works well for linearly separable features.
B. Random Forest Classifier: A bagging ensemble method that captures complex, non-linear relationships and handles overfitting well.
C. Support Vector Classifier (SVC): Finds the optimal hyperplane to separate classes; effective in high-dimensional spaces.

3. Ensemble Technique
To combine the predictions, a Voting Classifier was used.
Method: Soft Voting (averaging the predicted probabilities of classes).
This approach balances the bias and variance, leading to a more robust prediction.

# Future Improvements
Hyperparameter tuning using GridSearchCV for the SVC and Random Forest models.
Trying a Stacking Classifier instead of simple Voting.

# Contributing
Contributions are welcome! Please feel free to submit a Pull Request
