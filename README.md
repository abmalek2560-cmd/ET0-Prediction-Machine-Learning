[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/abmalek2560-cmd/ET0-Prediction-Machine-Learning/blob/main/ET0_Prediction_Machine_Learning.ipynb)

# Monthly Reference Evapotranspiration (ET0) Prediction using Machine Learning and Deep Learning

A data-driven computational framework designed to estimate and predict monthly Reference Evapotranspiration ($ET_0$) for Rangpur, Bangladesh, leveraging long-term agroclimatological data from the NASA POWER database and the standardized FAO-56 Penman-Monteith methodology.

## 📌 Project Overview
- **Target Region:** Rangpur, Bangladesh (Lat: ~25.74° N, Lon: ~89.27° E, Elevation: 30 m)
- **Data Source:** NASA POWER Database (2010–2024 historical records)
- **Methodology:** FAO-56 Penman-Monteith Equation applied to calculate daily/monthly $ET_0$.
- **Input Features:** Maximum Temperature ($T_{max}$), Minimum Temperature ($T_{min}$), Mean Temperature ($T_{mean}$), Relative Humidity ($RH$), Solar Radiation ($R_s$), and Wind Speed ($u_2$).
- **Models Implemented:** 
  - XGBoost Regressor
  - Random Forest Regressor
  - Long Short-Term Memory (LSTM) Deep Learning Network

## 🚀 Key Results
- **XGBoost:** Achieved exceptional performance with high $R^2$ score ($0.9703$) and low error metrics for predicting regional water demand.
- **Random Forest:** Provided robust multi-variable feature mapping.
- **LSTM:** Captured temporal dependencies effectively for time-series meteorological forecasting.

## 📂 Repository Structure
- `ET0_Prediction_Machine_Learning.ipynb`: Complete Python notebook containing data retrieval, FAO-56 $ET_0$ computation, ML/DL training, and evaluation plots.
- `calculated_monthly_eto.csv`: Processed historical dataset containing calculated $ET_0$ values.
