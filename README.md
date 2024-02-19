Data Preprocessing:
Load the Google stock price training data
Scale the prices to the range 0-1 using MinMaxScaler. This helps the network learn.
Create input/output pairs with past 60 time steps as input and next time step as output.
LSTM Model:
An RNN is created using Keras by stacking 4 LSTM layers one after the other.
LSTM can learn long-term temporal dependencies which helps in sequence forecasting problems.
Dropout layers are added for regularization to prevent overfitting.
Training:
The network is trained on the input/output pairs via backpropagation through time to learn predictive weights.
Loss function used is mean squared error.
Prediction:
Real Google stock prices for 2017 are loaded as test data.
The model uses the previous 60 days prices to predict next day's price one time step at a time.
Predicted prices are inverse transformed to actual prices.
Results:
Predicted and actual stock prices are plotted to visualize the fit.
The RNN has learned the patterns in past prices to predict future direction and fluctuations.

![image](https://github.com/mayurpatle/Stock-Price-Prediction-Using-RNN-/assets/65797614/e2f962a6-ba2a-478f-8f0e-7b95edb8fd55)
