# FlixIt Streaming Analysis
FlixIt Inc. aims to understand the factors influencing streaming behavior among its subscribers to improve customer retention and enhance engagement with premium services. This analysis predicts **streaming hours** based on three key predictors: annual **Income**, number of **Children** under 18 in the household, and subscription **History** (years as a FlixIt subscriber). The primary objective is to determine the individual and combined effects of these factors on streaming behavior, guiding strategic decisions for customer segmentation and retention.

## Data Description
- **Dataset File**: `FlixIt.dat`
- **Variables**:
  - `Hours`: Total streaming hours in the past 30 days
  - `Children`: Number of children in the household
  - `Income`: Annual income in thousands
  - `History`: Number of years subscribed to FlixIt
- **Data Format**: Raw data without headers, with each row representing a subscriber.

## Objective
The analysis aims to predict streaming hours based on each variable independently and collectively (all results should be accurate to four decimal places):
1. Predict streaming hours based on **Income** only
2. Predict streaming hours based on **Number of Children** only
3. Predict streaming hours based on **Subscription History** only
4. Combined model to predict streaming hours using **Income**, **Number of Children** and **Subscription History** altogether

## Methodology
- Simple Linear Regression models are developed for each individual predictor.
- Multiple Regression is used to evaluate the combined influence of all predictors.
- All results are reported with a minimum precision of four decimal places, using an alpha level of .05 for statistical tests.

## Key Findings
- **Children**: Has a positive impact on streaming hours, suggesting family-friendly marketing initiatives could increase engagement.
- **Income**: Minimal influence, indicating limited segmentation value based on income.
- **History**: Strong positive relationship, implying long-term subscribers are more engaged.

## Interpretation
- **An interpretation of the SLR b-value associated with Income**: This b-value represents the slope of the regression line when predicting the dependent variable based solely on Income. It means for each one-unit increase in ‘Income’, there is an expected decrease of 0.1850 units in ‘Hours’, holding other variables constant. 
- **An interpretation of the SLR CD value associated with Income**: The SLR CD value associated with ‘Income’ indicates that only 8.95% of the variation in the 'Hours’ can be explained by ‘Income’ alone in a ‘sample’ of simple linear regression model. Thus, we can conclude that the strength of relationship between ‘Hours’ and ‘Income’ is ‘low’ in the sample.
- **An interpretation of the SLR Adj. CD value associated with Income**: The SLR Adj. CD value associated with ‘Income’ indicates that only 8.54% of the variation in the 'Hours’ can be explained by ‘Income’ alone in a ‘population’ of simple linear regression model. Thus, we can conclude that the strength of relationship between ‘Hours’ and ‘Income’ is  'low’ in population.
- **An interpretation of the MR CPD value associated with Income**: This CPD (Coefficient of Partial Determination) value indicates that, when controlling for the other variables (‘Children’ and ‘History’), Income only uniquely explains approximately 0.61% of the variation in the 'Hours’. 
- **An interpretation of the MR Coefficient of Multiple Determination**: Here, MR Coefficient of Multiple Determination is the Model CD is 0.3166, meaning that approximately 31.66% of the variation in the 'Hours’ is explained by the combined influence of the predictors (Children, Income & History) in the ‘sample’ by the multiple regression model. It means the strength of the relationship among ‘Hours’ and ‘Children’, ‘Income’ & ‘History’ is moderate in sample. 
- **An interpretation of the MR Adjusted Coefficient of Multiple Determination**: The MR Adjusted Coefficient of Multiple Determination 0.3073, that approximately 30.73% of the variation in the 'Hours’ is explained by the combined influence of the predictors (Children, Income & History) in the ‘population’ by the multiple regression model. It means the strength of the relationship among ‘Hours’ and ‘Children’, ‘Income’ & ‘History’ is moderate in population.
- **An interpretation of the Global F p-value**: Global F p-value 2.2e-16 which is less than 0.05. It means that we can reasonably conclude that at least one of the predictor variables (either ‘Children’ or ‘Income’ or ‘History’) is statistical-significantly related with ‘Hours’ in 95% confidence level. 

## Recommandation
We should prioritize strategies targeting customers with a strong ‘subcription history’ with the company, as this variable has the most significant positive impact on the outcome. Additionally, customers with children also show a positive association, suggesting potential for family-oriented marketing efforts. Income, however, appears to have minimal influence on the outcome, especially in the multiple regression model, and can be deprioritized in customer segmentation efforts. While the model explains about 31.66% of the variance in the outcome, there remains a substantial portion unexplained, indicating that we could benefit from exploring additional variables to enhance the model's explanatory power and better capture other influential factors. 

## Model Performance
- **Simple Linear Regression** (SLR) was used to analyze each predictor’s individual impact.
- **Multiple Regression** (MR) was used to evaluate the combined effect of all predictors.
- **R² Values** indicate the strength of each predictor’s relationship with streaming hours.

## Instructions
**Dependencies**:
   ```R
   install.packages("dplyr")
   install.packages("heplots")




