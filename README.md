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
The project is available as a Jupyter Notebook `credit_card_default_prediction.ipynb`. You can run it sequentially to observe data visualizations and model training metrics. 
Alternatively, execute the Python script containing the modeling pipeline.
