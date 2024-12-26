# Smart Energy Management System

## Overview
The **Smart Energy Management System** is designed to predict energy demand, set thresholds for energy production optimization, and enable automated decision-making using machine learning and communication protocols like OpenADR. The project integrates predictive analytics and demand-response mechanisms to balance energy production and consumption effectively.

---

## Project Objectives
1. **Energy Demand Prediction:** Use Random Forest regression to forecast daily energy demand based on environmental factors like temperature and humidity.
2. **Threshold Setting:** Establish thresholds to determine whether to raise or optimize energy production, ensuring efficient grid operation.
3. **Demand-Response System:** Implement VTN (Virtual Top Node) and VEN (Virtual End Node) communication to automate production adjustments based on demand predictions.
4. **Visualization and Monitoring:** Provide a user-friendly dashboard using Streamlit to display predictions, actions, and adjustments.

---

## Features
- **Prediction Model:** Random Forest model trained on historical data (temperature, humidity, and demand).
- **Threshold Logic:** Dynamic logic to compare predicted demand against a baseline threshold (e.g., 1000 MW).
- **Decision-Making:** Automate production actions such as raising or optimizing energy output based on predictions.
- **VTN-VEN Communication:** Simulate demand-response communication for real-time energy adjustments.
- **Interactive Dashboard:** Visualize predictions and system decisions via a Streamlit app.

---

## Dataset
### Inputs:
- `date`: Timestamp for each entry.
- `temp`: Temperature (°C).
- `humidity`: Humidity (%).
- `ttemp`: Trend-adjusted temperature for smoother predictions.
- `demand`: Historical energy demand (MW).

---

## Methodology

### 1. **Data Preprocessing**
   - Load and clean data from CSV files.
   - Feature engineering: Adjust temperature trends and normalize inputs.

### 2. **Prediction Model**
   - Train a Random Forest Regressor on temperature and humidity to predict demand.

### 3. **Threshold Logic**
   - Set a baseline threshold (e.g., 1000 MW) using statistical methods.
   - Implement logic to calculate adjustments based on predicted demand.

### 4. **VTN-VEN Communication**
   - Simulate interactions:
     - VTN sends signals for adjustments.
     - VEN executes decisions (raise/optimize production).
