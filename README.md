# Stock-price-predictor
This project leverages Long Short-Term Memory (LSTM) neural networks, a type of recurrent neural network (RNN), to forecast the future closing price of a publicly traded stock. By training on historical data from Yahoo Finance, the model learns temporal patterns and trends to predict future price movements.

Core Objective
The primary goal is to build and train a robust deep learning model that can accurately predict the next day's closing price for a selected stock (e.g., Apple Inc. - AAPL). The project demonstrates a complete machine learning workflow, from data acquisition and preprocessing to model training, evaluation, and visualization.

Workflow & Key Features
Data Acquisition: Dynamically fetches years of historical stock data using the yfinance library in Python, ensuring the model is trained on up-to-date information.

Data Preprocessing: The dataset is cleaned, and the 'Close' price is isolated for prediction. Prices are then normalized using MinMaxScaler to a range of 0 to 1, a crucial step for optimizing the performance of neural networks.

Sequential Data Structuring: The time-series data is transformed into sequences suitable for an LSTM model. For instance, the model uses the closing prices of the past 60 days as input features to predict the price on the 61st day.

LSTM Model Architecture: A stacked LSTM model is built using the TensorFlow and Keras libraries. The architecture includes multiple LSTM layers to capture complex patterns and Dropout layers to prevent overfitting, enhancing the model's ability to generalize to new, unseen data.

Model Training & Evaluation: The model is trained on the first 80% of the historical data and then evaluated on the remaining 20%. Performance is quantitatively measured using the Root Mean Squared Error (RMSE), which calculates the deviation between the predicted and actual stock prices.

Visualization: The results are presented in a clear and intuitive plot using Matplotlib, comparing the model's predictions against the actual historical prices for both the training and validation sets.
