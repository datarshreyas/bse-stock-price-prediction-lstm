# BSE Stock Price Prediction using LSTM (Cross-Stock Generalisation)

## Overview
This project explores stock price prediction using Long Short-Term Memory (LSTM) neural networks, with a focus on evaluating whether patterns learned from one stock can generalise to another.

Unlike traditional models that train and test on the same stock, this project trains on one BSE stock and evaluates performance on a different, unseen stock.

---

## Objective
- Analyse historical stock price behaviour  
- Build a time-series forecasting model using LSTM  
- Evaluate whether learned patterns transfer across different stocks  
- Understand limitations of cross-stock prediction  

---

## Dataset

Data was collected using the yfinance API for multiple Bombay Stock Exchange (BSE) stocks:

- COROMANDEL.BO (Training stock)  
- NESTLEIND.BO (Unseen test stock)  
- Additional stocks used for exploratory analysis  

Data includes:
- Closing price  
- Trading volume  
- Historical time-series data (10+ years)  

---

## Exploratory Data Analysis

Performed analysis on multiple stocks:
- Closing price trends over time  
- Trading volume patterns  
- Moving averages (10, 20, 50-day)  
- Daily returns  
- Correlation between stocks  

---

## Methodology

### Data Preparation
- Selected closing prices for modelling  
- Scaled data using StandardScaler  
- Created time-series sequences (60-day windows)  

### Model Architecture
- Multi-layer LSTM network  
- Dropout layers to reduce overfitting  
- Dense output layer  

### Training
- Model trained on COROMANDEL stock data  
- Loss function: Mean Squared Error  
- Optimiser: Adam  

### Evaluation
- Tested on unseen stock (NESTLEIND)  
- Performance measured using RMSE  
- Visual comparison of actual vs predicted prices  

---

## Key Findings

- The model is able to capture general temporal trends in stock prices  
- Predictions approximate overall direction but struggle with sharp volatility  
- Cross-stock prediction is significantly more challenging than single-stock modelling  

---

## Limitations

- Stock prices are influenced by external factors not included in the model  
- Different stocks have different scales, volatility, and fundamentals  
- Scaling and distribution differences impact generalisation  
- Model does not incorporate macroeconomic or sentiment data  

---

## Conclusion

This project demonstrates that while LSTM models can learn temporal patterns in stock data, generalising those patterns across different stocks is difficult and highlights the limitations of purely data-driven forecasting in financial markets.

---

## Skills Demonstrated

- Time-series analysis  
- Deep learning (LSTM)  
- Data preprocessing and scaling  
- Model evaluation (RMSE)  
- Understanding of model generalisation and limitations  
