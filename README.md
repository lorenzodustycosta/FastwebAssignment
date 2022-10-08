# Environment Setup

- Python 3.10.6
- Requirements: check requirements.txt

# Repository Description
- Folder data contains:
    - the original .csv file and the txt with details on the dataset
    - the train and test files saved after the data preparation notebook is run

- The main folder contains:
    - the following notebooks:
        - `data_prepatation.ipynb`: common preprocessing steps for both models
        - `LogisticRegression.ipynb`: implements a logistic model 
        - `RandomForest.ipynb`: implements a random forest model
    - `.gitignore`
    - `requirements.txt`

# Logistic Regression
- Two approach: one with undersampling and one with oversampling
- Undersampling approach predicts too often that a client will subscribe a bank term deposit. For this use case, it seems more reasonbale to have less false postive and more false negative.
- To reach this goal, an oversampling approach as been implemented leading to an increase of accuracy, recall and F1 score
- The 3 features that have positive impact on the probability are:
    - duration
    - poutcome_unknown
    - poutcome_success
- The 3 features that have negative impact on the probability are:
    - loan
    - poutcome_other
    - poutcome_failure

# Random Forest
- Starating from the oversampling approach used for logistic regression, a random forest classifier as been implemented.
- This model leads to a slight increase of accuracy, recall and F1 score
- The 3 most important features are:
    - duration
    - last_contact_day
    - campaign
- The 3 less important features are:
    - job_housemaid
    - default
    - job_unknown

