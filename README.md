# Forecasting Time Series Data - CO2 Concentration Prediction

# Dataset

CO2 Dataset
This dataset contains monthly atmospheric carbon dioxide (CO₂) concentration records, commonly associated with long-term climate monitoring programs
Southern Oscillation Index (SOI) Dataset

# SARIMA - SARIMAX

1. Model Identification & Parameter Tuning
 - Stationarity Analysis: The Augmented Dickey-Fuller (ADF) test was utilized to determine the order of differencing ($d, D$) required to achieve stationarity.
   
 - Initial Parameter Estimation: Potential candidates for $(p, q)$ and $(P, Q)$ were identified by analyzing the Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) plots.
   
 - Multivariate Integration (SARIMAX): For the SARIMAX model, the Southern Oscillation Index (SOI) was integrated as an exogenous variable to account for the impact of El Niño and La Niña.

2. Hyperparameter Optimization
 - Grid Search Strategy: An exhaustive Grid Search was performed across a defined parameter space $(p, d, q) \times (P, D, Q, s)$.

 - Selection Criterion: The optimal configuration was selected based on the lowest Akaike Information Criterion (AIC) score, ensuring a balance between model goodness-of-fit and parsimony.

3. Performance Evaluation

After fitting the models with the best-found parameters, their predictive power was validated on the test set using a comprehensive suite of metrics:

 - Mean Squared Error (MSE) & Root Mean Squared Error (RMSE): To penalize large errors.

 - Mean Absolute Error (MAE): To provide a robust measure of average error magnitude.

 - Mean Absolute Percentage Error (MAPE): To evaluate the accuracy as a percentage of observed values.

# Univariate and multivariate LSTM

# Hybrid Models (SARIMA-Univariate LSTM and SARIMAX-Multivariate LSTM)
