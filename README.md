# ARIMA MODEL TO PREDICT TIME SERIES ANALYSIS
To perform ARIMA analyses and predict the temperature values for the next five years in Delhi.

## DATA 

The dataset contains the average temperature of each day for different cities across the world from 1995 to 2020. 

## STEPS IN ANALYSIS

- Created new data frame for Delhi
### Data Visualisation
- - Trends
  
![download](https://github.com/sidiquegithub/ML-MODEL-TIME-SERIES-ANALYSIS/assets/110783832/635a81ca-fb74-4669-839f-9e0afde4945f)

- - Box Plot

![download](https://github.com/sidiquegithub/ML-MODEL-TIME-SERIES-ANALYSIS/assets/110783832/a7936a29-b016-41f6-b895-a81122e192f7)

- - Skewness

![download](https://github.com/sidiquegithub/ML-MODEL-TIME-SERIES-ANALYSIS/assets/110783832/ffd2eda0-05c1-46d0-a56c-4e2ed95ea7a6)

The dataset exhibited a high degree of skewness
<br>
An outlier value of -99.0 was identified within the dataset

### Data Preprocessing

After replacing the outlier with NaN, the dataset became symmetric. Subsequently, the NaN was replaced with the dataset's mean temperature. 

![download](https://github.com/sidiquegithub/ML-MODEL-TIME-SERIES-ANALYSIS/assets/110783832/818682b6-bdc2-4e78-8ab3-90fef83ba361) 

### The Augmented Dickey-Fuller (ADF) For Stationarity

ADF Test Statistics:-8.786101777647525
<br>
p value:2.3064322634278694e-14
<br>
#Lags Used:38
<br>
Number of Observations Used:9226
<br>
Reject H0: It is stationary


![download](https://github.com/sidiquegithub/ML-MODEL-TIME-SERIES-ANALYSIS/assets/110783832/97abc29b-c5a3-4445-a7a0-be454acf0bbc) 


## MODEL SELECETION 

The Auto ARIMA method was employed for model selection, and it identified the SARIMAX(3, 0, 1) model as the best fit. This indicates that the optimal configuration for the time series forecasting involves three autoregressive terms (AR), no differencing (I), and one moving average term (MA), along with the potential inclusion of seasonal components if applicable in the SARIMAX model.

