# CreditWise-lone-Approval-Prediction
# Project Overview
The Credit Wise Loan System is a machine learning project that explores loan approval prediction. It prepares applicant data, analyzes relationships between features, and trains classification models to predict the Loan_Approved target.

The project is implemented in a Jupyter Notebook.
# Objectives
- Clean missing values in the dataset.
- Convert categorical features into numeric values.
- Explore feature relationships using a correlation heatmap.
- Split the data into training and testing sets.
- Scale features before training models.
- Train and evaluate multiple classification algorithms.
- Compare model performance using precision, recall, F1-score, accuracy, and a confusion matrix.
- Apply simple feature engineering and evaluate the models again.
# Algorithms Used
The notebook trains and compares these classification models:
1. Logistic Regression
2. K-Nearest Neighbors (KNN) with n_neighbors=5
3. Gaussian Naive Bayes
The notebook notes Naive Bayes as the best model based on precision. Check the notebook's printed evaluation results before reporting specific scores.
# Tools and Libraries
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
# Project Structure
Credit-Wise-Loan-System/
├── credit_wise_lone_sys(1).ipynb
├── lone_approval.csv
├── README.md
└── requirements.txt
Rename the notebook to a cleaner name such as credit_wise_loan_system.ipynb if you prefer, and update this file structure accordingly. The notebook currently loads the dataset using the filename lone_approval.csv, so make sure your dataset filename matches that exactly or update the pd.read_csv(...) line.
# Workflow
### 1. Load the dataset
   The notebook loads the CSV file with Pandas and inspects its structure.
### 2. Handle missing values
- Numerical columns: missing values are imputed using the mean.
- Categorical columns: missing values are imputed using the most frequent value.
### 3. Remove and encode features
- Drops Applicant_ID.
- Uses label encoding for Education_Level and Loan_Approved.
- Applies one-hot encoding to selected categorical columns, including employment status, marital status, loan purpose,     property area, gender, and employer category.
### 4. Explore correlations
Creates a correlation matrix and heatmap to inspect relationships among numeric features and Loan_Approved.
### 5. Split and scale the data
Uses an 80/20 train-test split with random_state=42. Standard scaling is fitted on the training data and applied to the test data.
### 6. Train and evaluate models
Evaluates Logistic Regression, KNN, and Gaussian Naive Bayes using:
- Precision
- Recall
- F1-score
- Accuracy
- Confusion matrix
### 7. Feature engineering
Creates squared features for DTI_Ratio and Credit_Score, then trains and evaluates the models again.
# Installation
Install the required packages:
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
Alternatively, install from requirements.txt if you create one.
# How to Run
1. Download or clone this repository.
2. Place lone_approval.csv in the same folder as the notebook. Ensure you have permission to share the dataset before committing it to a public repository.
3. Open a terminal in the project folder.
4. Install the dependencies.
5. Start Jupyter Notebook:
   jupyter notebook
6. Open the notebook and run the cells from top to bottom.
# Results
The notebook prints precision, recall, F1-score, accuracy, and confusion matrices for each model. It includes a note identifying Gaussian Naive Bayes as the best model based on precision. Add the actual metric values from your notebook output here after running all cells.
# Important Notes
- This project is for learning and experimentation. It should not be used as the sole basis for real-world lending decisions.
- Do not upload private applicant data, credentials, or other sensitive information to a public repository.
- The notebook performs preprocessing before the train-test split in its current workflow. For a more robust evaluation, fit imputation and encoding steps using training data only, ideally through a Scikit-learn Pipeline or ColumnTransformer, to reduce data leakage.
# Author
###  Aachal Ghorpade
