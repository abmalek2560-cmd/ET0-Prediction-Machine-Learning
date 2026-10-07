[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1yBBYcWE9B8ZDIOwwk5Rj0Jw-tGGRrU21#scrollTo=-FYIoXn0ydih)

# Monthly Reference Evapotranspiration ($ET_0$) Prediction using Machine Learning and Deep Learning

A data-driven computational framework designed to estimate and predict monthly Reference Evapotranspiration ($ET_0$) for Rangpur, Bangladesh, leveraging long-term agroclimatological data from the NASA POWER database and the standardized FAO-56 Penman-Monteith methodology.

---

## 📌 Project Overview
- **Target Region:** Rangpur, Bangladesh (Lat: ~25.74° N, Lon: ~89.27° E, Elevation: 30 m)
- **Data Source:** NASA POWER Database (2010–2024 historical records)
- **Input Features:** Maximum Temperature ($T_{max}$), Minimum Temperature ($T_{min}$), Mean Temperature ($T_{mean}$), Relative Humidity ($RH$), Solar Radiation ($R_s$), and Wind Speed ($u_2$).
- **Models Implemented:** XGBoost Regressor, Random Forest Regressor, and LSTM Deep Learning Network.

---

## ⚙️ Methodology

1. **Data Collection & Preprocessing:** 
   Historical climate parameters (2010–2024) for the Rangpur region were extracted from the NASA POWER database, and monthly records were structured systematically.
2. **FAO-56 Penman-Monteith Equation ($ET_0$ Calculation):** 
   Using meteorological parameters and local elevation, the standardized FAO-56 Penman-Monteith equation was applied to compute reference evapotranspiration:
   $$ET_0 = \frac{0.408\Delta(R_n - G) + \gamma \frac{900}{T_{mean} + 273} u_2 (e_s - e_a)}{\Delta + \gamma(1 + 0.34 u_2)}$$
3. **Machine Learning & Deep Learning Modeling:** 
   The dataset was split into 80% training and 20% testing sets to train and evaluate advanced predictive models (XGBoost, Random Forest, and LSTM).

---

## 📊 Results and Discussion

- **XGBoost Regressor:** Demonstrated exceptional predictive performance with an $R^2 \approx 0.9703$ and RMSE of $0.2113$ mm/day.
- **Random Forest Regressor:** Showed high robustness in feature mapping with an $R^2 \approx 0.9649$ and RMSE of $0.2295$ mm/day.
- **LSTM Network:** Captured sequential temporal patterns effectively ($R^2 \approx 0.7648$).
- **Discussion:** Peak $ET_0$ values occur during the hot and dry pre-monsoon months (March–May), driven by high solar radiation and temperature. This model provides an efficient basis for smart irrigation scheduling and agricultural water resource management in northern Bangladesh.

---

## 📂 Repository Structure
- `ET0_Prediction_Machine_Learning.ipynb`: Complete Python notebook containing data retrieval, FAO-56 calculations, and ML/DL pipelines.
- `calculated_monthly_eto.csv`: Processed monthly historical dataset containing calculated $ET_0$ values.

---

## 📚 References
- Allen, R. G., Pereira, L. S., Raes, D., & Smith, M. (1998). *Crop evapotranspiration-Guidelines for computing crop water requirements-FAO Irrigation and drainage paper 56*. Food and Agriculture Organization of the United Nations, Rome.
- Stackhouse, P. W., Jr., et al. (2020). *NASA/LARC/SDIO NASA Prediction of Worldwide Energy Resources (POWER) Project [Data set]*. NASA Langley Research Center.
