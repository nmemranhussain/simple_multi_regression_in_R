# FlixIt Streaming Analysis

## Overview
This project analyzes the relationship between FlixIt streaming hours and three subscriber characteristics: **Number of Children**, **Income**, and **Subscription History**. Using linear regression analysis, the objective is to inform customer engagement strategies by identifying key predictors of streaming behavior.

## Data Description
- **Dataset File**: `FlixIt.dat`
- **Variables**:
  - `Hours`: Total streaming hours in the past 30 days
  - `Children`: Number of children in the household
  - `Income`: Annual income in thousands
  - `History`: Number of years subscribed to FlixIt
- **Data Format**: Raw data without headers, with each row representing a subscriber.

## Objective
The analysis aims to predict streaming hours based on each variable independently and collectively:
1. Predict streaming hours based on **Income** only
2. Predict streaming hours based on **Number of Children** only
3. Predict streaming hours based on **Subscription History** only

## Key Findings
- **Children**: Has a positive impact on streaming hours, suggesting family-friendly marketing initiatives could increase engagement.
- **Income**: Minimal influence, indicating limited segmentation value based on income.
- **History**: Strong positive relationship, implying long-term subscribers are more engaged.

## Interpretation
- **Children**: Each additional child in a subscriber's household is associated with an increase in streaming hours, indicating that families with children tend to use the service more.
- **Income**: Income has a slight negative relationship with streaming hours, suggesting it may not be a strong predictor of streaming behavior for this platform.
- **History**: History is the strongest predictor of streaming hours. Longer-tenured subscribers tend to stream more, highlighting the importance of retaining long-term customers for increased engagement.

## Model Performance
- **Simple Linear Regression** (SLR) was used to analyze each predictor’s individual impact.
- **Multiple Regression** (MR) was used to evaluate the combined effect of all predictors.
- **R² Values** indicate the strength of each predictor’s relationship with streaming hours.

## Instructions
1. **Dependencies**:
   ```R
   install.packages("dplyr")
   install.packages("heplots")




