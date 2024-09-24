#### Project Tittle:
### Wind-Turb-Power-Curve-Estimations
#### Project Description:
#### Wind power curves are crucial for wind power forecasting, turbine condition monitoring, energy potential estimation, and turbine selection. However, producing reliable power curves from raw wind data is challenging due to outliers formed in unexpected conditions. This notebook explores approaches for power curve modeling and evaluates the performance of various machine learning (ML) models across different seasons.
#### Introduction:
#### Wind energy is clean, inexhaustible, inexpensive and widely distributed.However,the randomness and intermittency of wind lead to uncertainty in wind power generation, which brings challenges to the corresponding energy management system and affects the reliability of the entire power grid. Therefore, accurate estimates of wind power curves,which show the non-linear relationship between wind speed and wind power, are required for effective integration of wind power into the power system, as well as wind turbine condition monitoring projects.
#### ![image](https://github.com/user-attachments/assets/1f7a1389-f0de-413e-b718-842a52f46cd0)

##### The wind turbine power curve shows the relationship between the wind turbine power and hub height wind speed. It essentially captures the wind turbine performance. Hence it plays an important role in condition monitoring and control of wind turbines. Power curves made available by the manufacturers help in estimating the wind energy potential in a candidate site. Accurate models of power curve serve as an important tool in wind power forecasting and aid in wind farm expansion.
#### ![Screenshot 2024-09-24 124410](https://github.com/user-attachments/assets/72a9ae6e-868c-40b9-b0b4-53054a6fd9d8)

#### Explanation of Data Columns
#### Wind Speed (m/s): The speed of the wind measured in meters per second.
#### Power Output (kW): The electrical power output from the wind turbine, measured in kilowatts.
#### Turbine Model: The specific model of the turbine being analyzed.
#### Air Density (kg/m³): The density of air at the given conditions, which can affect power output.
#### Temperature (°C): The ambient temperature, which can also impact the turbine's performance.

#### EDA
#### Wind Speed Distribution
##### ![Screenshot 2024-09-24 142339](https://github.com/user-attachments/assets/ef88cc4a-1d01-4756-80d0-2ba5eb8b98d7)
#### Annual Wind Direction
#### ![Screenshot 2024-09-24 142927](https://github.com/user-attachments/assets/86abca84-b979-4bdc-9fca-cc0167c8e595)

#### Air Density Distribution 
##### ![Screenshot 2024-09-24 143300](https://github.com/user-attachments/assets/f4660c00-71ee-4ff4-a459-2d003705a370)

#### Annual Power Curve
#### ![Screenshot 2024-09-24 155738](https://github.com/user-attachments/assets/0921f547-c278-476a-80d2-3c8f1e9e7a73)
#### Correlation Plot
#### ![Screenshot 2024-09-24 160009](https://github.com/user-attachments/assets/558d522b-ae44-4003-aefd-125c0dcc8d6f)

## Models
#### Polynomial Models 
#### ![Screenshot 2024-09-24 160159](https://github.com/user-attachments/assets/3ccd85ba-5945-4984-a525-5f1dc92c0073)

#### Random Forest Regression Power Curve
#### ![Screenshot 2024-09-24 160533](https://github.com/user-attachments/assets/35e70369-f12d-47ab-a414-a2aa9f185172)

#### Gradient Boosting Regression Power Curve
#### ![Screenshot 2024-09-24 160945](https://github.com/user-attachments/assets/3a8a4681-cfe6-4a60-b16e-e6a24d0c6193)

#### Power Curve with Xgboost Regression"
#### ![Screenshot 2024-09-24 161144](https://github.com/user-attachments/assets/c9a1e974-e9c3-4325-8268-27b78c7a118a)


#### Conclusion:
#### To tackle first problem while using regression problem, we can use sigmoid function but it will change the distribution of the response variable. So, to solve both of the problems I used tree based methods which gave me very good results compared to linear regression and lasso regression as they fit a straight line. Results for non linear models can be seen below.
#### ![Screenshot 2024-09-24 205227](https://github.com/user-attachments/assets/9a96e0fb-f109-476e-b828-0c0425c92026)

#### As we can see, in boosting methods bias reduces which improves the test results.
##### Also, feature importance plots suggests that Wind Speed (Velocity), Wind Direction and Wind Sheer are most important features for predicting the relative power.








