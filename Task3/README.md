# Task 3: Energy Consumption Time Series Forecasting

## Objective  
The objective of this task is to forecast short-term household energy usage using historical time-based patterns. This helps in understanding energy consumption trends and can aid in optimizing electricity usage and demand management.

---

## Dataset  
- **Name:** `household_power_consumption.csv`  
- **Description:** The dataset contains minute-level measurements of household electric power consumption.  
- **Key Columns:**  
  - `Date`, `Time` → Combined to form a timestamp index  
  - `Global_active_power` → Total household energy usage (in kilowatts)  
  - `Global_reactive_power`, `Voltage`, `Global_intensity`  
  - `Sub_metering_1`, `Sub_metering_2`, `Sub_metering_3`  

---

## Approach  

1. **Data Preparation & Preprocessing**  
   - Combined `Date` and `Time` columns into a single `DateTime` index.  
   - Handled missing values and converted data types appropriately.  
   - Resampled the data (hourly averages) to smooth fluctuations and enable meaningful forecasting.  

2. **Feature Engineering**  
   - Extracted time-based features: `hour of day`, `day of week`, and `weekend/weekday`.  
   - These features help models capture daily and weekly consumption cycles.  

3. **Models Used**  
   - **ARIMA:** Captures linear temporal dependencies in the data.  
   - **Prophet:** Models seasonality (daily/weekly patterns) and trend components.  
   - **XGBoost:** Utilizes lag features and engineered time features for non-linear learning.  

4. **Evaluation Metrics**  
   - Mean Absolute Error (MAE)  
   - Root Mean Square Error (RMSE)  

5. **Visualization**  
   - Time series plots showing actual vs. forecasted energy usage.  
   - Model comparison charts to highlight performance differences.  

---

## Results & Findings  

- **ARIMA:** Performed reasonably well for short-term forecasting but struggled with complex seasonality.  
- **Prophet:** Captured daily and weekly seasonal patterns effectively, producing stable forecasts.  
- **XGBoost:** Showed strong predictive power when using lag and time-based features, outperforming linear models.  

**Conclusion:**  
- Prophet and XGBoost produced the most reliable forecasts.  
- Prophet is more interpretable (trend + seasonality breakdown).  
- XGBoost achieved slightly better accuracy but requires careful feature engineering.  

---

## Skills Gained  
- Time series preprocessing and resampling  
- Feature engineering for temporal data  
- Implementation of ARIMA, Prophet, and XGBoost  
- Model evaluation using MAE & RMSE  
- Visualization and interpretation of time series models  

---

## Repository Structure  

Task3_EnergyForecasting/
│── household_power_consumption.csv # Dataset
│── Task3_Notebook.ipynb # Jupyter Notebook with code & analysis
│── README.md # Documentation
