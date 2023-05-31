# SPA Description
This is a description of the repo https://github.com/peterthelander/spa (private repo)

Spa is a stock prediction algorithm, using quantamental analysis.

This project uses financial data analysis and machine learning to predict future stock prices based on financial indicators and quarterly earnings data. It's a Python program designed to make stock market predictions using machine learning models implemented with TensorFlow.

The software uses historical financial statement data from various companies and their respective share prices. The data spans over several years (2017 to 2022) and is used for training and validation of the prediction models.

The goal of this project is to create a model that can predict whether a stock's price will increase or decrease in the future based on financial indicators such as Revenue, Net Income, Gross Profit, Operating Income and Revenue Growth.

# Approach
The data was first cleaned and processed to extract the necessary features. The feature extraction process involved resampling the share prices to a quarterly frequency and computing financial indicators like Revenue/Market Cap, Net Income/Revenue, Gross Margin, Operating Margin and Revenue Growth.

The processed data was then fed into a binary classification model, which was trained to predict whether the share price of a company would increase or decrease in the next quarter. The model uses a sigmoid activation function and the Binary Cross-Entropy loss function.

# Model
The model architecture consists of a simple feed-forward neural network with one hidden layer. The model was trained using the Adam optimizer.

# Structure
The software is divided into several parts, corresponding to the various stages of the machine learning pipeline:

- data_collection.py: This script is responsible for loading the input data from CSV files. It loads quarterly financial statement data and stock price data.
- data_preprocessing.py: This script prepares the data for machine learning. This includes handling missing values, converting data types, and transforming data where necessary.
- feature_engineering.py: This script is responsible for creating new features from the existing data that might be useful for predicting stock prices.
- model_building.py: This script is where the machine learning model is defined, trained, and validated.
- model_evaluation.py: This script contains functions to evaluate the performance of the model.
- main.py: This is the main script that ties together all the parts. It calls functions from the other scripts to carry out the full machine learning pipeline.

# Data
The data used in this project comes from SimFin and includes three CSV files: us-income-quarterly.csv, us-balance-quarterly.csv, and us-share-prices-daily.csv. These files are stored in the simfin_data subdirectory.

Each of these files contains different types of financial data:

- us-income-quarterly.csv: This file contains data related to companies' quarterly income.
- us-balance-quarterly.csv: This file contains companies' quarterly balance sheet data.
- us-share-prices-daily.csv: This file contains daily share price data for the companies.
