# Customer Churn Prediction using Artificial Neural Network

## Overview
This project implements a customer churn prediction system using an Artificial Neural Network (ANN). The model analyzes various customer attributes such as credit score, geography, demographics, and banking behavior to predict the likelihood of customer churn.

## Features
- Neural network-based prediction model
- Interactive Streamlit web interface
- Comprehensive data preprocessing pipeline
- Support for multiple geographical regions
- Standardized feature scaling
- Categorical variable encoding

## Project Structure
```
├── prediction.ipynb          # Jupyter notebook for model prediction
├── app.py                    # Streamlit web application
├── Feature_Engineering.ipynb # Data preprocessing and feature engineering
├── model.h5                  # Trained ANN model
├── label_encoder_gender.pkl  # Label encoder for gender
├── one_hot_encoder_geo.pkl  # One-hot encoder for geography
├── scaler.pkl               # Feature scaler
└── Churn_Modelling.csv      # Dataset file
```

## Dataset Description
The model is trained on a comprehensive banking dataset with the following features:
- Credit Score
- Geography (France, Germany, Spain)
- Gender
- Age
- Tenure
- Balance
- Number of Products
- Credit Card Status
- Active Membership Status
- Estimated Salary

## Installation

### Prerequisites
- Python 3.x
- pip package manager

### Required Libraries
```bash
pip install tensorflow pandas numpy scikit-learn streamlit
```

## Usage

### Running the Prediction Notebook
1. Open `prediction.ipynb` in Jupyter Notebook or JupyterLab
2. Execute the cells sequentially
3. Follow the instructions for making predictions

### Launching the Streamlit App
1. Navigate to the project directory
2. Run the following command:
```bash
streamlit run app.py
```
3. Access the web interface through your browser
4. Input customer details and click "Predict" for churn prediction

### Feature Engineering
- Open `Feature_Engineering.ipynb` to view or modify the preprocessing pipeline
- The notebook includes:
  - Data cleaning
  - Categorical variable encoding
  - Feature scaling
  - Train-test split implementation

## Data Preprocessing
The system implements the following preprocessing steps:
1. Removal of irrelevant columns (RowNumber, CustomerId, Surname)
2. Gender encoding using Label Encoder
3. Geography encoding using One-Hot Encoder
4. Numerical feature standardization using StandardScaler

## Model Details
- Architecture: Artificial Neural Network
- Input Features: 11 preprocessed features
- Output: Binary classification (Churn/No Churn)
- Format: HDF5 (.h5)

## File Descriptions
- `prediction.ipynb`: Contains code for model loading and prediction
- `app.py`: Streamlit application for user interface
- `Feature_Engineering.ipynb`: Data preprocessing and feature engineering code
- `model.h5`: Trained neural network model
- `label_encoder_gender.pkl`: Serialized gender encoder
- `one_hot_encoder_geo.pkl`: Serialized geography encoder
- `scaler.pkl`: Serialized feature scaler
