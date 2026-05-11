# Apple Stock Price Forecasting using LSTM

## Overview
This project predicts Apple Inc. (AAPL) stock prices using a Long Short-Term Memory (LSTM) neural network implemented with TensorFlow/Keras.

The project compares:
- Baseline forecasting
- LSTM deep learning forecasting

using MAE and RMSE evaluation metrics.

---

## Dataset
Historical Apple stock data was used for training and evaluation.

Features:
- Open
- High
- Low
- Close
- Volume

Target:
- Closing Price

---

## Project Workflow

### 1. Data Preparation
- Loaded stock data using pandas
- Handled missing values
- Visualized closing price trends

### 2. Baseline Forecasting
- Implemented lag-1 baseline model
- Calculated MAE and RMSE

### 3. Preprocessing
- Applied Min-Max normalization
- Prevented data leakage

### 4. Sequence Generation
- Generated 30-day rolling sequences for LSTM input

### 5. LSTM Architecture
- Built stacked LSTM neural network
- Added Dropout regularization
- Used MSE loss function

### 6. Model Training
- Used EarlyStopping
- Saved best-performing weights

### 7. Evaluation
- Generated predictions
- Inverse transformed predictions
- Calculated MAE and RMSE

### 8. Visualization
- Compared Actual vs Baseline vs LSTM predictions

---

## Technologies Used
- Python
- Pandas
- NumPy
- TensorFlow/Keras
- Matplotlib
- Scikit-learn

---

## Results

The LSTM model achieved lower prediction error than the baseline forecasting model, demonstrating improved forecasting capability for Apple stock prices.

---

## Future Improvements
- Hyperparameter tuning
- Multi-feature forecasting
- Transformer models
- Longer forecasting horizons
