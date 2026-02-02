Gold Price Prediction using Machine Learning

Project Overview
This project implements a machine learning pipeline to predict gold prices (GLD) using financial indicators such as the S&P 500 index (SPX), crude oil prices (USO), silver prices (SLV), and the EUR/USD exchange rate.  
The objective is to model the nonlinear relationship between these indicators and gold prices using a Random Forest Regressor and evaluate its predictive performance.

Dataset
- Source: Historical financial market data stored in `gold_price_data.csv`
- Rows: 1719	
- Features:
  - `Date` – Trading date
  - `SPX` – S&P 500 index value
  - `USO` – Crude oil ETF price
  - `SLV` – Silver ETF price
  - `EUR/USD` – Euro to USD exchange rate
- Target:
  - `GLD` – Gold ETF price

Project Workflow
1. Data Loading
   - Load CSV data into a Pandas DataFrame.
   - Inspect shape, data types, and basic statistics.

2. Data Validation
   - Verify absence of missing values.
   - Confirm numerical consistency of features.

3. Exploratory Data Analysis
   - Statistical summary using `describe()`.
   - Correlation analysis between financial indicators.
   - Distribution analysis of gold prices.

4. Feature and Target Split
   - Features (`X`): SPX, USO, SLV, EUR/USD
   - Target (`Y`): GLD

5. Train–Test Split
   - 80% training data
   - 20% testing data
   - Fixed random state for reproducibility.

6. Model Training
   - Algorithm: Random Forest Regressor
   - Number of trees: 100
   - Model trained on training dataset.

7. Prediction
   - Generate predictions on unseen test data.

8. Model Evaluation
   - Metric used: R² Score
   - Achieved R² score ≈ **0.99**, indicating strong explanatory power.

9. Visualization
   - Line plot comparing actual vs predicted gold prices.
   - Visual inspection of prediction accuracy and deviation patterns.

Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

Results
- The Random Forest model captures complex nonlinear relationships between gold prices and correlated financial indicators.
- High R² score demonstrates strong predictive accuracy.
- Model performance suggests suitability for financial trend analysis and educational demonstration purposes.

Limitations
- The model relies only on a limited set of financial indicators.
- Temporal dependencies are not explicitly modeled.
- No hyperparameter optimization beyond default Random Forest settings.

Future Improvements
- Incorporate macroeconomic indicators such as interest rates and inflation.
- Apply time-series models (LSTM, ARIMA, Prophet).
- Perform hyperparameter tuning using Grid Search or Bayesian Optimization.
- Add cross-validation and error distribution analysis.

Usage
1. Clone the repository.
2. Place `gold_price_data.csv` in the project directory.
3. Run the notebook or Python script sequentially.
4. Review evaluation metrics and plots.

License
This project is intended for educational and academic use.

