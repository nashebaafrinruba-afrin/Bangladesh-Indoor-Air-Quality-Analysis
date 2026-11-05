Bangladesh Indoor Air Quality Analysis

A statistical analysis of 10,000 indoor air-quality records from Bangladeshi households, completed as a group project for **CSE 303: Statistics for Data Science** at East West University. The project combines descriptive statistics, distribution and outlier analysis, categorical analysis, correlation analysis, and two simple machine learning models.

## Overview
Indoor air pollution is a serious health concern in Bangladesh. This project studies how pollutants (PM2.5, PM10, CO2, CO, NO2, TVOC) vary across households, and how they relate to occupancy, cooking habits, ventilation and weather conditions.

## Dataset
`Bangladesh_Indoor_Air_Quality_Cleaned.csv has 10,000 rows and 22 columns**.

| Category | Variables |
|----------|-----------|
| Air quality | CO2, CO, NO2, PM2.5, PM10, TVOC |
| Indoor conditions | Indoor Temperature, Indoor Humidity |
| Weather | Outdoor Temperature, Outdoor Humidity, Rainfall |
| Household | Occupancy, Number of Rooms, Household Size, Cooking Frequency |
| Categorical | Ventilation Type, Cooking Fuel, Nearby Traffic, Floor Level, Time of Day, Season |

## Methods
1. **Descriptive statistics** for 15 numerical variables: mean, median, mode, variance, standard deviation, Q1, Q3, IQR and coefficient of variation.
2. **Distribution and outlier analysis** for 10 air-quality and weather variables: skewness, kurtosis, and outlier detection with the 1.5 × IQR rule, with histograms, density plots and boxplots.
3. **Categorical analysis**: frequency tables, bar charts and pie charts.
4. **Relationship analysis**: scatter plots and correlation coefficients.
5. **Linear Regression**: predicting CO2 from occupancy (80/20 train-test split).
6. **Logistic Regression**: classifying PM10 as High or Low (80/20 stratified split, scaled features).

## Key Findings

**Distributions and outliers
- Rainfall had the highest relative variability (coefficient of variation about 325%) and the most outliers (15.25% of records). Most days recorded zero rainfall, so even small amounts were flagged as outliers.
- Indoor temperature had the lowest relative variability (about 6.9%).
- Eight of the ten variables were approximately symmetric. Only CO and Rainfall were right-skewed.
- Average PM2.5 was about 40 µg/m³ and average PM10 about 60 µg/m³.

**Household patterns
- Gas was the main cooking fuel (74.8% of households).
- Fans (39.8%) and exhaust fans (29.7%) were the most common ventilation types.
- 57.4% of readings were taken in winter.

**Relationships
| Pair | Correlation |
|------|-------------|
| PM2.5 and PM10 | 0.966 |
| Occupancy and CO2 | 0.949 |
| Household Size and Occupancy | 0.895 |
| Household Size and CO2 | 0.849 |
| Outdoor and Indoor Temperature | 0.017 |
| Cooking Frequency and PM2.5 | 0.003 |

**Models**
- **Linear Regression** (Occupancy ? CO2): RMSE of about 104 ppm on the test set.
- **Logistic Regression** (PM10 High vs Low): accuracy and weighted F1-score of 0.92.


## Tools Used
Python, Pandas, NumPy, Matplotlib, Scikit-learn, Jupyter Notebook

## Team
Group project by a team of 6 students.

My contribution: Worked on the Python analysis in the notebook, including descriptive statistics, skewness and outlier detection, and visualizations (histograms, density plots, boxplots, scatter plots). Also helped build and evaluate the Linear and Logistic Regression models and interpret the results for the report.

## Author
Nasheba Afrin Ruba
CSE (Data Science) student, East West University
Email: nashebaafrinruba@gmail.com
