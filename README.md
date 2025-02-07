# Bitcoin Price Movement Prediction

## Problem Statement

We aim to predict whether Bitcoin's next-day closing price will be higher or lower than the previous day's closing price. Using a dataset containing 10 years of daily Bitcoin prices, we apply various classification algorithms to determine the model that best fits this classification task.

## Dataset

The dataset includes the following features:

- Open, High, Low, Close prices
- Volume
- Several technical indicators, including:
  - Relative Strength Index (RSI)
  - Commodity Channel Index (CCI)
  - Simple Moving Average (SMA)
  - Exponential Moving Average (EMA)
  - Moving Average Convergence Divergence (MACD)
  - Bollinger Bands
  - Average True Range (ATR)

The target variable is binary:

- `1` if the next day's closing price is higher than the previous day.
- `0` if lower.

## Methodology

### 1. Data Preprocessing

- The dataset is split into features (X) and the target variable (y).
- Missing values are handled appropriately.
- The dataset is divided into training (80%) and testing (20%) sets.

### 2. Feature Selection

- Features such as open price, close price, volume, and various technical indicators (RSI, MACD, etc.) are selected as inputs to the models.

### 3. Model Training and Evaluation

The following classification techniques are applied:

- **Decision Tree (DT):** Used to model and visualize the decision-making process.
- **Random Forest (RF):** An ensemble of decision trees to improve accuracy and reduce overfitting.
- **Logistic Regression (LR):** A statistical approach for binary classification.
- **Naive Bayes (NB):** A probabilistic model based on Bayes' theorem.
- **k-Nearest Neighbours (k-NN):** A distance-based classification method.
- **K-Means Clustering:** Used for clustering, with labels adjusted for classification.

### 4. Evaluation Metrics

The models are evaluated using:

- Accuracy
- Confusion Matrices
- Classification Reports

## Results

- **Decision Tree:** Accuracy \~49%. The model effectively split features but was prone to overfitting.
- **Random Forest:** Accuracy \~52%. Improved performance due to ensemble learning and reduced overfitting.
- **Logistic Regression, Naive Bayes, k-NN:** Accuracy ranged between 46%-52%.
- **K-Means:** Performed poorly compared to supervised methods.

## Conclusion

- **Random Forest** provided the best overall performance with an accuracy of 52%, making it the most effective model for predicting Bitcoin’s next-day price movement.
- **Decision Trees** performed well but were sensitive to data splits, leading to overfitting.
- **Logistic Regression, Naive Bayes, and k-NN** had competitive results but did not outperform Random Forest.
- **K-Means** struggled due to its unsupervised nature.

## Installation and Usage

1. Clone the repository:
   ```sh
   git clone https://github.com/A471KK2/bitcoin-price-prediction.git
   ```

## Future Improvements

- Incorporating deep learning techniques (e.g., LSTMs) for time-series forecasting.
- Feature engineering to improve predictive accuracy.
- Hyperparameter tuning for model optimization.
