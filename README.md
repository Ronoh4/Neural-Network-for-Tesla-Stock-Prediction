Stock Price Prediction using LSTM Neural Network

Overview
This Python script leverages Long Short-Term Memory (LSTM) neural networks to predict stock prices. It utilizes historical stock data, specifically the opening prices of Tesla (TSLA) stocks, to train the model. The trained model is then used to predict stock prices on a test dataset.

Requirements
Python (>=3.6)
Libraries: scikit-learn, Keras, NumPy, pandas
How to Use
Data Preparation:

Ensure you have the historical stock data file named TSLA.csv in the same directory as the script.
Install the required libraries: pip install scikit-learn keras numpy pandas.
Run the Script:

Execute the script using a Python interpreter: python stock_prediction.py.
Results:

The script will print the predicted values for the test dataset's last column and display the model summary.
Script Breakdown
Data Loading:

Historical stock data is loaded from the 'TSLA.csv' file.
Data Preprocessing:

The data is scaled using Min-Max scaling to fit within the range [0, 1].
Train and test datasets are created using the 'create_dataset' function from the 'helper' module.
Model Architecture:

A Sequential model is constructed using Keras.
Two LSTM layers, each followed by a Dropout layer with a dropout rate of 0.2, capture temporal patterns.
A Dense layer with one unit acts as the output layer.
Model Compilation and Training:

The model is compiled using the Adam optimizer and mean squared error loss.
Training is performed with five epochs, a batch size of 16, and no verbosity during training.
Prediction:

The trained model predicts stock prices for the test dataset.
Results Display:

The predicted values' last column is printed, showcasing the model's performance.
The model summary provides insights into the neural network's architecture.
Note
This script assumes the availability of the 'helper' module, presumably containing the 'create_dataset' function.
Feel free to experiment with the script, adjust hyperparameters, or try it with different stock datasets for enhanced predictions.
