# Credit_card_default_prediction

This project is aimed at predicting credit card default using historical customer data. It explores a dataset of credit card transactions, performs data preprocessing, data visualization, and applies machine learning classification algorithms.

## Features
- **Data Exploration and Preprocessing**: 
  - Handles missing values and duplicates.
  - Generates aggregate features like `past_payments`, `bill_amount`, and `previous_payments` to reduce dimensionality and improve predictive power.
  - Drops redundant columns.
- **Data Visualization**:
  - Utilizes `seaborn` and `matplotlib` to plot distributions of categorical variables (like `SEX`, `EDUCATION`, `MARRIAGE`) and numerical variables against default status.
  - Plots correlation heatmaps to identify multicollinearity.
- **Machine Learning Models**:
  - Employs **Logistic Regression** and **Random Forest Classifier** to predict the likelihood of default.
  - Handles dataset imbalance using **RandomUnderSampler** from the `imblearn` library to improve model robustness.
  - Evaluates models using Accuracy, Precision, Recall, F1 Score, and Confusion Matrix.
- **Model Deployment**:
  - Saves the trained model using `pickle` for inference on new customer inputs.

## Requirements
Ensure you have the following installed:
- Python 3.x
- pandas
- scikit-learn
- seaborn
- matplotlib
- imbalanced-learn
- numpy
- scipy

You can install all dependencies via:
```bash
pip install -r requirements.txt
```

## Running the Code
The project is available as a Jupyter Notebook `credit_card_default_prediction.ipynb` and as an automated Python script `credit_card_script_runnable.py`.

## Console Output
When you run the machine learning script on the console, you can expect the following output metrics for the trained models:

```text
X_train shape: (24000, 8)
X_test shape: (6000, 8)
y_train shape: (24000,)
y_test shape: (6000,)
Accuracy: 0.7955

Classification Report:
              precision    recall  f1-score   support

           0       0.80      0.97      0.88      4687
           1       0.63      0.16      0.25      1313

    accuracy                           0.80      6000
   macro avg       0.72      0.57      0.57      6000
weighted avg       0.77      0.80      0.74      6000

Confusion Matrix:
[[4568  119]
 [1108  205]]

Logistic Regression Accuracy: 0.80
Logistic Regression Precision: 0.77
Logistic Regression Recall: 0.80
Logistic Regression F1 Score: 0.75
Random Forest Accuracy: 0.80
Random Forest Precision: 0.77
Random Forest Recall: 0.80
Random Forest F1 Score: 0.77

Predictions for new payments:
Payment 1: Default
```

## AI Agent Integration

This prediction system can be effectively integrated and managed by an **AI Coding Agent**. You can leverage an AI agent to:
1. **Automate Data Pipelining**: Continually pull down new CSV reports and run them through this predictive pipeline entirely in the background.
2. **Automate Bug Fixing & Execution**: An agent can run `.ipynb` files via console conversions, handle missing package errors on the fly (via `pip`), and sanitize blocking UI commands like `plt.show()` programmatically.
3. **Continuous Deployment**: The AI can execute local validation checks, generate git commits automatically, and push prediction metrics directly to remote systems or a remote GitHub repository.

## How to Push to GitHub

To push this codebase to your own GitHub account from your local terminal, follow these steps:

1. **Create a Repository on GitHub**: 
   - Go to github.com and log in.
   - Click the `+` icon in the top right corner and select "New repository".
   - Name your repository (e.g., `Credit-Card-Default-Prediction`) and create it. Do not initialize it with a README, .gitignore, or license since we already have local files.

2. **Run Git Commands Locally**:
   Open your terminal in this directory and execute the following commands:
   
   ```bash
   # Initialize the local directory as a Git repository (if not done yet)
   git init

   # Add all your files to the staging area
   git add .

   # Commit the files
   git commit -m "Initial commit for Credit Card Default Prediction"

   # Link your local repository to your GitHub repository
   # Replace the URL below with your actual repository URL
   git remote add origin https://github.com/your-username/your-repo-name.git

   # Push the code to the main branch on GitHub
   git branch -M main
   git push -u origin main
   ```
