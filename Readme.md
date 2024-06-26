# Stock Trading Recommendation System Using Transformer Model

This repository is created as part of Machine Learning Engineer work trial. It contains code for using Lag-Llama a state of the art timeseries foundation model and a custom transformer model built using PyTorch. Both models have been finetuned on intra-day stock trading dataset.

## To set up dependies
- Install all the requirements using .yml files or manually install all packages from it (use to setup a separte conda/python environement)
- Or follow instructions given in each notebook

## Pre-processing Dataset
- [Download Link](https://drive.google.com/file/d/1e-r9DVETTP7hqg9qNzxaZ_asFcup0FaK/view?usp=sharing)
-	To see the schema for the market data, visit [link](https://databento.com/datasets/XNAS.ITCH) and select the TTBO Schema.
- Added momentum, value, volatality, trend and other indicators.
-	Stock prices were recorded at irregular intervals (in nanoseconds). Timestamps were then uniformly sampled to seconds, and NaN values were addressed.
-	Target column was added to predict stock prices 1 min/60 seconds given previous 2 min/120 seconds sequences.
-	The data was split into training and testing sets, with 85% allocated for training and 15% for testing.

## Evaluation Criteria
- Different model performance was compared using 3 metrics- MAE, MSE, RMSE

