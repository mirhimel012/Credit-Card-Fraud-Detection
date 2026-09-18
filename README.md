# Credit Card Fraud Detection

A machine learning project for detecting fraudulent credit card transactions using the IEEE-CIS Fraud Detection dataset.

## Project Overview

Credit card fraud detection is a classification problem where the goal is to identify whether a transaction is legitimate or fraudulent.

In this project, transaction data is preprocessed and different machine learning models are trained and compared to detect fraudulent transactions.

## Dataset

The project uses the **IEEE-CIS Fraud Detection** dataset from Kaggle.

The notebook uses the transaction data only and does not merge the identity dataset.

The dataset contains transaction-related features with `isFraud` as the target variable:

* `0` → Legitimate transaction
* `1` → Fraudulent transaction

## Methodology

The project follows these main steps:

1. Load the transaction dataset
2. Explore the dataset
3. Check the target class distribution
4. Handle missing values
5. Encode categorical features
6. Split the data into training and validation sets
7. Scale the features
8. Select the top 50 features using Mutual Information
9. Handle class imbalance using SMOTE
10. Train multiple machine learning models
11. Compare model performance
12. Perform stability and ablation analysis
13. Tune selected models using cross-validation
14. Tune the prediction threshold
15. Evaluate a voting ensemble

## Machine Learning Models

The project evaluates the following classifiers:

* Logistic Regression
* Decision Tree
* Random Forest
* Support Vector Machine (SVM)
* K-Nearest Neighbors (KNN)
* Naive Bayes
* XGBoost

## Evaluation Metrics

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix

ROC-AUC and other classification metrics are considered to better understand fraud detection performance.

## Techniques Used

### Feature Selection

The project uses `SelectKBest` with Mutual Information to reduce the number of features and select the most informative 50 features.

### Class Imbalance Handling

SMOTE is applied to the training data to address the imbalance between legitimate and fraudulent transactions.

### Hyperparameter Tuning

Selected models are further tuned using K-Fold Cross-Validation.

### Threshold Tuning

The prediction threshold is adjusted based on the Precision-Recall relationship to improve F1-score.

### Ensemble Learning

A Voting Classifier is also evaluated by combining multiple trained models.

## Exploratory Data Analysis

The project includes several visualizations, including:

* Fraud class distribution
* Transaction amount histogram
* Transaction amount boxplot
* Correlation heatmap
* Transaction amount vs. transaction time
* Pair plot

## Project Structure

```text
Credit-Card-Fraud-Detection/
│
├── README.md
├── credit-card-fraud-detection.ipynb
├── requirements.txt
├── figures/
│   ├── 01_class_distribution.png
│   ├── 02_histogram_transaction_amt.png
│   ├── 03_boxplot_transaction_amt.png
│   ├── 04_correlation_heatmap.png
│   ├── 05_scatter_amt_vs_time.png
│   └── 06_pairplot.png
│
└── .gitignore
```

## Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Imbalanced-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

## How to Run

Clone the repository and install the required libraries:

```bash
pip install -r requirements.txt
```

Then open the notebook:

```bash
jupyter notebook
```

Open:

```text
credit-card-fraud-detection.ipynb
```

## Author

**Himel Mir**

Computer Science and Engineering Student
Bangladesh University of Business and Technology (BUBT)
