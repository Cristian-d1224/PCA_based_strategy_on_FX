# PCA_based_strategy_on_FX

The objective of this project is to develop a quantitative trading strategy for the FX market using **Principal Component Analysis(PCA)** and **Machine Learning**.

The strategy starts by analyzing the joint behavior of EUR/USD and GBP/USD exchange rates. Since both currency pairs share exposure to the U.S. Dollar, PCA is used to identify the dominant latent factors driving their co-movement. Instead of trading each currency pair independently, the strategy seeks to trade these underlying statistical factors.

The project is developed in two stages:

1. **Factor Extraction**:
   - Compute daily log returns
   - Apply PCA to identify the dominant sources of variation in the market
   - Analyize factor loadings, explained variance, and factor scores to understand the structure of the data
  
2. **Strategy Development**
   - Construct features from the extracted factors.
   - Train Machine Learning models to determine when and how much exposure should be allocated to the dominant factor.
   - Evaluate the strategy through an out-of-sample backtest using standard performance metrics
  
The final goal is to investigate whether latent statistical factors extracted from historical market data can be used to generate profitable trading signals while reducing noise and redundant information.
