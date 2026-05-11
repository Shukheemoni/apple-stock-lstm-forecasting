# 📈 Apple Stock Price Forecasting using LSTM Neural Networks

## 📌 Project Overview

This project focuses on forecasting Apple Inc. (AAPL) stock closing prices using a Long Short-Term Memory (LSTM) deep learning model implemented with TensorFlow/Keras. The study compares a traditional baseline forecasting approach with an LSTM neural network to evaluate the effectiveness of deep learning for financial time-series prediction.

The workflow includes:
- Data preprocessing and normalization
- Time-series sequence generation
- LSTM model architecture design
- Model training with EarlyStopping
- Performance evaluation using MAE and RMSE
- Visualization of forecasting results

---

## 📂 Dataset

Historical Apple Inc. (AAPL) stock market data was used for this project.

### Features Included
- Open
- High
- Low
- Close
- Volume

### Prediction Target
- Closing Stock Price

---

# 🛠️ Project Methodology

## 1️⃣ Data Preparation
- Loaded historical Apple stock data using Pandas
- Checked and handled missing values
- Visualized stock price trends using Matplotlib

---

## 2️⃣ Baseline Forecasting
A lag-1 baseline forecasting model was implemented where:

\[
\hat{y}_{t+1} = y_t
\]

The baseline model served as a benchmark for comparison with the LSTM model.

### Evaluation Metrics
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

---

## 3️⃣ Data Preprocessing
Min-Max normalization was applied to scale stock prices between 0 and 1.

Normalization was fitted only on training data to prevent data leakage.

---

## 4️⃣ Sequence Generation
Normalized stock prices were transformed into 30-day rolling sequences suitable for LSTM input.

### Input Shape
```python
(samples, timesteps, features)
```

Example:
- Previous 30 days → predict next day price

---

## 5️⃣ LSTM Neural Network Architecture

The forecasting model was implemented using TensorFlow/Keras with:
- Two stacked LSTM layers
- Dropout regularization
- Dense output layer

### Model Features
- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)
- Dropout Rate: 0.2

---

## 6️⃣ Model Training
The model was trained using:
- Validation monitoring
- EarlyStopping callback
- ModelCheckpoint for saving best weights

This reduced overfitting and improved generalization performance.

---

## 7️⃣ Model Evaluation
Predictions were generated using the trained LSTM model and inverse transformed back to actual stock prices.

### Evaluation Metrics
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

---

## 8️⃣ Visualization
Matplotlib was used to compare:
- Actual stock prices
- Baseline predictions
- LSTM predictions

This provided a visual assessment of forecasting performance.

---

# 📊 Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| Pandas | Data Manipulation |
| NumPy | Numerical Computation |
| Matplotlib | Data Visualization |
| Scikit-learn | Preprocessing & Metrics |
| TensorFlow/Keras | Deep Learning Model |

---

# 📈 Results

The LSTM model achieved lower forecasting error compared to the baseline model, demonstrating improved predictive capability for Apple stock price forecasting.

| Model | MAE | RMSE |
|---|---|---|
| Baseline Forecasting | XX.XX | XX.XX |
| LSTM Forecasting | XX.XX | XX.XX |

---

# 🚀 Future Improvements

Potential future enhancements include:
- Hyperparameter optimization
- Multi-feature forecasting
- GRU and Transformer architectures
- Sentiment analysis integration
- Multi-step forecasting

---

# 📁 Repository Structure

```text
apple-stock-lstm-forecasting/
│
├── AAPL.csv
├── apple_lstm.ipynb
├── best_lstm_model.keras
├── README.md
└── requirements.txt
```

---

# 👩‍💻 Author

Developed as a deep learning time-series forecasting project using Apple stock market data and LSTM neural networks.
