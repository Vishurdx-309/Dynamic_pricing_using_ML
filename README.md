# Dynamic Pricing Strategy for Ride-Sharing Service

## Project Overview
This project implements a dynamic pricing model for a ride-sharing service. It adjusts ride costs based on current demand (number of riders) and supply (number of drivers) to optimize pricing and improve profitability.

## Features
- Dynamic price calculation based on supply and demand
- Data preprocessing pipeline
- Machine learning model for price prediction
- Profitability analysis
- Visualization of results

## Components

### 1. Data Preprocessing
The `data_preprocessing_pipeline` function handles:
- Identification of numeric and categorical features
- Handling of missing values
- Outlier detection and treatment using IQR method

### 2. Dynamic Pricing Model
Calculates `demand_multiplier` and `supply_multiplier` based on current market conditions to adjust ride prices.

### 3. Profitability Analysis
Compares the adjusted ride cost with historical costs to determine the profitability of each ride under the new pricing model.

### 4. Price Prediction Model
A machine learning model that predicts ride prices based on:
- Number of riders
- Number of drivers
- Vehicle type (Economy/Premium)
- Expected ride duration

### 5. Visualization
Includes several visualizations:
- Donut chart showing the distribution of profitable vs. loss-making rides
- Scatter plot comparing actual vs. predicted prices

## How to Use

1. Preprocess your data:
   ```python
   preprocessed_data = data_preprocessing_pipeline(raw_data)
   ```

2. Apply the dynamic pricing model:
   ```python
   data['adjusted_ride_cost'] = calculate_dynamic_price(data)
   ```

3. Analyze profitability:
   ```python
   data['profit_percentage'] = calculate_profit_percentage(data)
   ```

4. Predict prices for new rides:
   ```python
   predicted_price = predict_price(number_of_riders, number_of_drivers, vehicle_type, Expected_Ride_Duration)
   ```

5. Visualize results:
   ```python
   plot_profitability_distribution(data)
   plot_actual_vs_predicted(y_test, y_pred)
   ```

## Requirements
- Python 3.7+
- pandas
- numpy
- scikit-learn
- plotly

## Installation
1. Clone this repository
2. Install required packages:
   ```
   pip install pandas numpy scikit-learn plotly
   ```

## Future Improvements
- Incorporate more features into the pricing model (e.g., time of day, weather conditions)
- Implement A/B testing to compare different pricing strategies
- Develop a real-time pricing update system

## Contributor
Vishal Bokhare
