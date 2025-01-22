# BikeSharingDemandPrediction_V2

# Project: Seoul Bike Sharing Demand Prediction - Advanced Modeling
## I. Business Idea:
The project focuses on optimizing Seoul's bike-sharing system through advanced data analytics and predictive modeling. Addressing the challenge of fluctuating rental demand, this initiative aims to enhance operational efficiency, improve user satisfaction, and promote sustainable urban mobility within the city. By leveraging data-driven insights, the system aims to ensure bike availability aligns with user needs, minimizing imbalances and maximizing resource utilization. This project contributes to the smart city vision, integrating predictive capabilities for a seamless, user-centric transportation experience.

## II. Problem Statement:
Bike-sharing systems, including Seoul's, face significant challenges in managing fluctuating demand influenced by factors like weather, time of day, seasons, and holidays. These fluctuations lead to inefficient resource allocation, with bikes either overstocked in low-demand areas or unavailable in high-demand locations. The lack of accurate demand forecasting hinders operational efficiency, impacting customer satisfaction and causing disruptions in a city that heavily relies on its transportation systems. Addressing this problem requires the integration of data analysis and predictive modeling for proactive resource allocation.

## III. SWOT Analysis:
**Strengths:** Environmentally friendly, cost-effective, reduces traffic congestion, promotes a healthy lifestyle, and aligns with Seoul's sustainability goals.

**Weaknesses:** High demand variability due to weather and seasonality, potential inefficiencies in manual redistribution of bikes.

**Opportunities:** Growing environmental awareness, leveraging data analytics and machine learning to optimize resource allocation, and potential for mobile app integration to enhance user experience.

**Threats:** Competition from other micro-mobility options, infrastructural limitations (e.g., weather, lack of bike lanes), and financial risks associated with advanced technology investments.

## IV. Solution Approach & Recommendations:
The solution employs descriptive analytics to understand historical patterns and predictive modeling to forecast future demand. This combined approach allows the system to react to current trends and prepare for future demand changes proactively. Key recommendations include:

**Dynamic Resource Allocation:** Real-time redistribution of bikes based on predictive demand.

**Weather-Sensitive Adjustments:** Increasing bike availability on sunny days and reducing it during adverse weather.

**Technology Integration:** User engagement through mobile apps for real-time bike availability, reservations, and gamification.

**User Feedback:** Collecting customer feedback for continuous service improvement.

## V. Implementation Strategy:
**Data Collection and Preprocessing:**
- Loaded the Seoul bike-sharing system dataset.
- Handled missing values and converted categorical variables to numerical.
- Extracted features like month, year, and day from the date column.
- Applied transformations (log1p, square root, cube root) to address skewness in numerical data.

**Descriptive Analysis:**
- Calculated basic statistics and visualized seasonal, monthly, and hourly rental trends.
- Analyzed the effects of weather variables on rental demand.
- Examined data distribution using histograms.
- Conducted specific analyses for seasonal variations, monthly trends, yearly changes, and the impact of holidays.
- Created a correlation matrix to analyse the weather conditions impact on bike rentals.
  
**Feature Engineering:**
- Extracted month and day names from date column and converted date column to datetime format.
- Categorical features such as "Holiday, Seasons, Functioning_Day and Day_Name" were encoded.
- Removed unnecessary columns (e.g., 'Date', 'DPT').
- Identified high correlation between 'DPT' and 'Temperature', removed 'DPT' to avoid multicollinearity.
- Applied label encoding to categorical variables.
- Performed outlier analysis using boxplots.
- Transformed the target variable and windspeed column using square root and cube root transformations to approach normal distribution.

**Predictive Model Development:**
- Split the dataset into training and testing sets.
  **Trained models:** Linear Regression, Lasso Regression, Ridge Regression, Random Forest Regressor, and LightGBM (LGBM).

- Evaluated model performance using R² and RMSE.
- Implemented custom evaluation function for models, also calculates and prints Adjusted R².
- Visualized actual versus predicted values using a scatter plot.

## VI. Results & Outcomes:
**Model Performance:**

- Linear Regression, Lasso, and Ridge models achieved R² values between 0.45 and 0.48, and RMSE between 8.40 and 8.64
- Random Forest Regressor explained around 76% of the variance with an RMSE of 5.66.
- LightGBM (LGBM) demonstrated the best performance, explaining 81% of the variance with the lowest RMSE of 5.12.

**Key Findings:**
- Summer and rush hours (5:00 PM - 7:00 PM) see peak bike rental demand.
- Bike rentals are significantly affected by weather conditions, with temperature and dew point temperature positively correlated to the number of rented bikes.
- Holiday bike rental is significantly lower than regular days and therefore requires special holiday planning.
- Monthly rental peaks are in May and June, dropping to a low in January.
- Significant usage increase was observed in 2018, in comparison to 2017.

## VII. Follow-Up and Evaluation Plan:
**KPI Tracking:** Bike utilization rates, user satisfaction scores, and operational efficiency metrics will be monitored monthly.

**User Feedback:** Collected through surveys and mobile application reviews to identify areas for improvement.

**Model Retraining:** Predictive models will be retrained periodically with updated data to maintain relevance and accuracy.

**Annual Assessment:** An annual review will assess the general impact of implemented strategies, address any challenges faced, and plan further improvements.

## VIII. Conclusion
This project has established a comprehensive framework for predicting bike-sharing demand in Seoul through data analysis, feature engineering, and predictive modeling. By utilizing the insights and model outcomes, operational efficiency can be greatly improved while maintaining customer satisfaction and optimizing the bike-sharing experience.
This approach to managing operations with data-driven analysis will ensure continuous improvement and long-term success for the bike-sharing system in Seoul.
