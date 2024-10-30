# Stock Price Prediction using LSTM

This project uses an LSTM (Long Short-Term Memory) neural network to predict Apple Inc. (AAPL) stock prices based on historical data. The model is built using Python and Keras and aims to forecast closing prices, providing insights into trends while also highlighting the limitations of LSTMs for stock price volatility.

## Goal
Predict AAPL stock prices based on historical data to understand how well LSTMs can capture stock price trends and evaluate model performance over extended training epochs.

## Dataset
The dataset includes historical daily stock prices of AAPL with the following columns:
- Date, Open, High, Low, Close, Adj Close, Volume.

## Model Summary
The model is an LSTM-based neural network with the following architecture:
- Two LSTM layers with 50 units each, followed by two Dense layers with 25 and 1 unit, respectively.
- Trained over 30 epochs, with batch size 64, using Adam optimizer and mean squared error as the loss function.

## Results

### Training and Validation Loss
- **Training Loss**: Stabilized at a low value (~1.2e-06), indicating effective learning on the training data.
- **Validation Loss**: Fluctuated across epochs but generally improved, reaching its lowest value around epoch 26. This suggests better generalization to unseen data, though some fluctuations hint at slight overfitting.
![realvsprediction][/result/1.png]
### Real vs. Predicted Prices
- The model captures the overall trend in stock prices but lacks accuracy in predicting short-term fluctuations. Predictions appear smoother than the actual data, which is typical given the volatile nature of stock prices.

![realvsprediction][/result/2.png]
## Analysis and Observations
1. **Improvement with Extended Training**: The additional epochs led to improved validation performance, but occasional spikes in loss indicate potential overfitting.
2. **Potential for Hyperparameter Optimization**: Tuning parameters like batch size and LSTM units, or adding regularization, may help further reduce validation loss.
3. **Incorporating Additional Features**: Including indicators like trading volume, market sentiment, or technical indicators could help the model handle stock price volatility better.
4. **Real-World Applicability**: This model is effective for trend analysis but has limitations in precise short-term forecasting. It would be best suited as a component in a broader forecasting system.
![realvsprediction][/result/3.png]
## Conclusion
The LSTM model demonstrated reasonable performance in capturing general stock price trends but struggled with the inherent volatility of stock data. This project provides a foundation for further tuning and model adjustments, potentially incorporating additional features or hybrid models for improved prediction accuracy.

## Future Work
- Experiment with different LSTM architectures and regularization methods.
- Add external data features to better capture stock price dynamics.
- Explore ensemble methods to combine LSTM with other forecasting models.




