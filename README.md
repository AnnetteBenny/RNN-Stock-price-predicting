# 📈 Stock Price Prediction Using RNN (LSTM)

This project aims to predict the future stock prices of four major technology companies — **Amazon (AMZN), Google (GOOGL), IBM, and Microsoft (MSFT)** — using historical stock market data and Recurrent Neural Networks (RNN), particularly the Long Short-Term Memory (LSTM) architecture.

---

## 🔍 Problem Statement

> **Objective:**  
Given the historical stock prices (2006–2018) of four companies in the tech sector, predict their future stock prices using sequential models.

Stock prices are inherently time-dependent and exhibit complex temporal patterns, making them suitable for modeling with RNNs. Predicting them accurately can be both intellectually rewarding and financially lucrative.

---

## 🧠 Why RNN / LSTM?

Stock data is sequential — the price today depends on the prices from previous days. LSTM models are a special kind of RNN capable of learning long-term dependencies, which makes them well-suited for time series forecasting tasks like this.

---

## 📁 Data Description

Each stock's historical data is provided in a CSV file:

- `AMZN_stock_data.csv`
- `GOOGL_stock_data.csv`
- `IBM_stock_data.csv`
- `MSFT_stock_data.csv`

### 📊 Features in the dataset:
- `Date`: Trading date
- `Open`: Price at market open
- `High`: Highest price of the day
- `Low`: Lowest price of the day
- `Close`: Price at market close
- `Volume`: Number of shares traded
- `Name`: Stock name

---

## 🛠️ Project Steps

### 1. **Data Aggregation**
- Combined the `Close` prices of all four stocks into a single DataFrame using their respective dates.

### 2. **Exploratory Data Analysis**
- Plotted time series of closing prices for each stock to visualize trends.

### 3. **Data Preprocessing**
- Normalized the data using `MinMaxScaler` for better model performance.
- Converted the time series into sequences (e.g., using 60 days to predict the next day).

### 4. **Model Building**
- Built an LSTM-based neural network using TensorFlow/Keras.
- Architecture: LSTM → Dropout → Dense layer with 4 outputs (one for each stock).

### 5. **Model Training**
- Trained the model on historical data.
- Used Mean Squared Error (MSE) as the loss function and Adam as the optimizer.

### 6. **Evaluation & Prediction**
- Made predictions on the test set.
- Compared actual vs predicted values using plots.

---


## 🧰 Tech Stack

- Python 🐍
- NumPy & Pandas 📊
- Matplotlib & Seaborn 📈
- Scikit-learn 🧮
- TensorFlow / Keras 🤖
- Google Colab (for training in the cloud)
