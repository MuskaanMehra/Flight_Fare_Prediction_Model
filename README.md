# Flight Fare Prediction Model
Studied trend of price variation for a period of limited years. Machine Learning algorithms are applied on the dataset to predict dynamic fare of flights. This gives predicted value of flight fare to get a flight ticket at minimum cost.

Analysed the flight data and shown how features like arrival time and hour, departure time and hour, no. of stops and type of flight etc. decide the flight fare. 
## Data Collection
Dataset is taken from **Kaggle**.

**Fields/Variables**
  |  | | | | |
| ---- | --- | --- | --- | --- |
 Airline | Date of Jouney | Route| Departure Time | Total Stops
| Source | Destination | Duration | Arrival Time | Price


## Data preprocessing
- Superfluos information is deleted like copies and invalid data.
- Filling NaN values with mean, median or mode using **fillna()** method.
- Drop missing values.
- **Encoding techniques** for converting categorical data into numerical form:
   -  **One Hot Encoder** for Nominal data
   -  **Label Encoder** for Ordinal data
## Exploratory Data Analyses
### Airline v/s Price
![Airline](https://github.com/MuskaanMehra/Flight_Fare_Prediction_Model/blob/main/Assets/Airline%20vs%20Price.png)
From the graph we can see that Jet Airways Business has the highest price. Apart from the first airline almost all are having similar median.

### No. of stops v/s Price
![Stops](https://github.com/MuskaanMehra/Flight_Fare_Prediction_Model/blob/main/Assets/Stops%20vs%20Price.png)
As the no. of stops are increasing, the price is inreasing concomitantly.

### Source v/s Price
![Source](https://github.com/MuskaanMehra/Flight_Fare_Prediction_Model/blob/main/Assets/Source%20vs%20Price.png)
Apart from Bangalore there is not any large change in price and also outliers and variation in price are comparatively less.

## Outlier Detection
Outliers are visualised using Box Plot and then removed as they were generating high skewness in the data.
![Outlier](https://github.com/MuskaanMehra/Flight_Fare_Prediction_Model/blob/main/Assets/Outliers.png)
We assumed that price can't be more than INR 40,000.

## Model Selection
Data preparation is followed by analysing the data, uncovering the hidden trends and then applying various ML models.
**Algorithms Used:** Linear regression, Decision tree, Random Forest
All models are implemented in Scikit Learn. 

| Model | MAE | R2 Score | MSE | RMSE |
| --- | --- | --- | --- | --- |
| Random Forest | 1148.084| 0.837 | 3386685.71 | 1840.29 |
| Linear Regression | 1890.32 | 0.64 | 6904293 | 2627.60 |
| Decision Tree | 1350.58  |0.7473| 5325783.9| 2307.76| 

We can conclude that Random forest regressor is giving good results and minimal value of error.
