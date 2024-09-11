# Harvesting-Insights-Predictive-Analytics-and-Trend-Forecasting-in-Global-Food-Production
This project focuses on analyzing the global production of various food types between 1961 and 2023, using a dataset containing production quantities of foods like maize, rice, wheat, tomatoes, and many others.
Data Preprocessing:
The dataset contains production values for different foods, with some columns requiring cleaning. For example, column names were modified to remove spaces and special characters for easier manipulation. After this, the cleaned dataset included columns like Maize_Production_, Rice__Production_, and Wheat_Production_.Key Steps:
Handling Missing Data: Missing values were filled using forward fill (ffill), ensuring no gaps in time-series data.
Feature Creation: A new feature Maize_YoY_Growth was calculated to analyze the year-on-year growth of maize production.
Dataset Splitting: The dataset was split into feature variables (X) and target variable (y) for machine learning. We used other food production values as features to predict maize production.
Visualizations
Several advanced visualization techniques were used to gain insights:

Heatmap of Correlations: A heatmap was generated to show the correlations between different food production variables, highlighting relationships that might help in predictive modeling.

Time Series Plots: Time series visualizations were used to show the trends in maize production over the years, highlighting any seasonality or long-term patterns.

Feature Importance: Using Random Forest, the importance of different food production variables was measured, giving insight into which foods most influence maize production.

Principal Component Analysis (PCA): PCA was employed to reduce dimensionality and visualize the variance explained by different components, helping us better understand the variance across food production variables.

Data Analysis
Principal Component Analysis (PCA):

PCA was applied to reduce the complexity of the data and focus on the most important features. This technique showed that certain food types (like wheat, rice, and potatoes) had a significant impact on overall variance.
Random Forest Feature Importance:

After training a Random Forest model, feature importance was calculated to determine which food types have the most significant impact on predicting maize production. Foods like wheat and soybeans were found to be key predictors.
Anomaly Detection:

Using Z-scores, anomalies in maize production were detected. This helps identify outliers in the data, such as unexpected drops or increases in production.
Year-on-Year (YoY) Growth Analysis:

By calculating the YoY growth for maize production, we observed how production levels fluctuate over time, highlighting certain periods of rapid increase or decline in specific countries.
Machine Learning Model
We used a Random Forest Regressor to predict maize production based on the other food production variables. Key steps included:

Train-Test Split: The data was split into training (80%) and testing (20%) sets.

Model Training: The Random Forest Regressor was trained on the dataset, optimizing hyperparameters such as n_estimators and max_depth.

Evaluation: The model was evaluated using metrics such as Mean Squared Error (MSE) and R-squared (R²). The model performed well, showing a strong correlation between the predicted and actual maize production values.

Prediction: The model was then used to predict future maize production, generating predictions for upcoming years based on trends in other food productions.

Time Series Forecasting (ARIMA)
We also employed ARIMA (AutoRegressive Integrated Moving Average) to forecast future maize production using historical data.

ARIMA Model: The model was fitted to the maize production time series.
Forecast: Predictions were made for the next few years, showing the projected production trends.
Results: The model predicted a steady increase in maize production for the next decade, with minor fluctuations.
Final Results and Insights
Key Predictors: The Random Forest model identified wheat, soybeans, and potatoes as the most influential food types in predicting maize production.

Anomalies: Notable anomalies were detected, such as years with significant drops in maize production, likely due to external factors like weather conditions or economic instability.

Forecasting: The ARIMA model forecasts suggest a consistent increase in maize production in the near future, driven by global agricultural practices and increasing demand.

Conclusion
This project used machine learning and statistical techniques to analyze and predict food production trends. The findings can be useful for policymakers and agricultural planners to anticipate future demands and optimize production strategies. The combination of PCA, feature importance analysis, and time-series forecasting provides a comprehensive approach to understanding and predicting food production patterns globally.
