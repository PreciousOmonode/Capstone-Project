**Energy Consumption Analytics & Forecasting Pipeline**

This project is an end-to-end data pipeline and machine learning system for analyzing electricity consumption, tracking energy balances, and forecasting future energy usage and costs at the account level.

It simulates real-world energy billing behavior by combining appliance-level usage data, purchase history, and consumption logs to generate insights and predictions.
Key Features

**Data Cleaning & Standardization**
Harmonizes account IDs across multiple datasets and ensures consistent joins across all energy tables.

**Energy Usage Calculation**
Computes daily kWh usage per appliance, aggregates consumption at account level and converts energy usage into billable units.

**Balance Tracking System**
Tracks lifetime units purchased vs consumed, updates real-time account balances and computes remaining available energy.

**Consumption Simulation**
Generates realistic daily usage logs and applies controlled random variation for behavioral realism.

**Analytics & Reporting**
Daily, monthly, and rolling consumption trends, last 30-day usage averages and today’s consumption summaries per account.

**Smart Recommendation Engine**
Identifies high-impact appliances, suggests energy-saving actions, and estimates monthly cost and energy savings.

**Machine Learning Forecasting**
Linear Regression model for consumption prediction, Uses time-based and lag features and Forecasts 30-day energy usage per account

**Deployable ML Module**
Serialized model (joblib), Simple prediction API function and Ready for backend integration

**Pipeline Architecture**

The full pipeline runs in the following sequence:

Clean and normalize datasets, Compute appliance-level energy usage, Generate daily consumption logs, Update energy balance (purchases vs usage), Forecast depletion dates, Build analytics dashboards (daily/monthly trends), Generate user recommendations, Train ML model for future forecasting, and Export deployable model package.

**Machine Learning Model**
**Model Type**: Linear Regression, Target Variable: estimated_kwh_used
**Key Features**: Day index (time progression), Month, Day of week, Lag-1 consumption (previous day usage), Performance, Mean Absolute Error (MAE): ~1.5 kWh, and R² Score: ~0.98

**Forecasting Capability**

The model can: Predict daily energy usage for each account, Estimate 30-day total consumption,Calculate projected cost using tariff data and Provide rolling iterative forecasts using lag updates
