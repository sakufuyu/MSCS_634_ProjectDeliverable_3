# MSCS_634_ProjectDeliverable_3

## Dataset
I used the `student-por.csv` file from the Student Performance dataset.

## Goal
The goal of this deliverable was to perform classification, clustering, and association rule mining, and to improve one classification model using hyperparameter tuning.

## Classification
I converted the final grade (`G3`) into a binary target:
- pass = 1 if `G3 >= 10`
- fail = 0 if `G3 < 10`

I built two classification models:
- Logistic Regression
- Decision Tree

### Classification Results
- **Logistic Regression**
  - Accuracy = 0.907692
  - F1 Score = 0.945455

- **Decision Tree**
  - Accuracy = 0.876923
  - F1 Score = 0.927928

Logistic Regression performed best among the original classification models.

## Hyperparameter Tuning
I tuned the Decision Tree model using GridSearchCV.

### Best Parameters
- max_depth = 3
- min_samples_leaf = 4
- min_samples_split = 2

### Tuned Decision Tree Results
- Accuracy = 0.892308
- F1 Score = 0.936364

The tuned Decision Tree improved over the original model, but Logistic Regression still remained the best classification model overall.

## Clustering
I used K-Means with 3 clusters and visualized the results with PCA.

### Clustering Result
- Silhouette Score = 0.262383

The cluster profiles showed three groups:
- lower-performing students
- middle-performing students
- higher-performing students

This clustering could help identify student groups that may need different levels of academic support.

## Association Rule Mining
I used Apriori to find frequent patterns in categorized student data.

The rules suggested that combinations related to stronger academic conditions, no past failures, and supportive learning factors were often associated with passing outcomes.

These patterns may be useful for understanding common student success factors in a real-world educational setting.

## Challenges
One challenge was combining classification, clustering, and pattern mining in one notebook while keeping the workflow simple.

Another challenge was preparing the data in different ways for different tasks.
I handled this by using preprocessing pipelines for classification, selected numeric features for clustering, and categorized variables for association rule mining.