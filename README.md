# FlixIt Streaming Analysis

## Project Overview
This project aims to analyze the relationship between streaming hours on FlixIt, a movie streaming platform, and three key predictor variables: **Number of Children**, **Income**, and **Subscription History**. By understanding how these factors individually and collectively impact streaming hours, this analysis seeks to support strategic decisions for customer segmentation and retention efforts.

## Project Description
- **Dataset**: The dataset consists of variables including:
  - `Hours`: Total streaming hours
  - `Children`: Number of children in the household
  - `Income`: Household income
  - `History`: Historical subscription duration
  
- **Analysis**:
  - **Simple Linear Regression (SLR)**: Each predictor’s impact on streaming hours was modeled individually.
  - **Multiple Regression (MR)**: Combined effects of all predictors were assessed.
  - **Model Evaluation**: 
    - **Coefficient of Determination (CD)** and **Adjusted CD** were calculated to assess model performance.
    - **ANOVA Table** and **Global F-test** were used to statistically validate each model.

## Key Findings
- **Children**: Shows a positive slope, indicating a significant association with streaming hours. This suggests that promoting family-oriented content may enhance engagement.
- **Income**: Exhibits a minimal effect on streaming hours, indicating limited relevance for income-based segmentation strategies.
- **History**: Displays the strongest positive association with streaming hours, implying that longer-standing subscribers are more engaged.

## Interpretation of Metrics
- **Simple Linear Regression (SLR) Coefficients**: 
  - Each unit increase in `Income` results in a slight decrease in streaming hours.
  - Each unit increase in `History` results in a substantial increase in streaming hours.
  
- **Multiple Regression (MR) Coefficients**:
  - When controlling for other factors, `History` retains a strong positive association with `Hours`, while `Children` remains positively associated.
  - **Coefficient of Partial Determination (CPD)**: `Income` explains minimal unique variance in the model, indicating limited influence when considering other variables.

## Technical Information
- **Programming Language**: R
- **Key Libraries**: `dplyr`, `heplots`

## File Descriptions
- `flixit_data.csv`: Contains the dataset with `Hours`, `Children`, `Income`, and `History` variables.
- `analysis_code.R`: R script for data loading, statistical analysis, and model generation.

## Recommendations
Based on the findings, **Subscription History** and **Number of Children** are crucial for understanding subscriber engagement. Since `Income` shows less significance, customer segmentation strategies could focus on historical usage patterns and family-related factors.

## Limitations
The model explains approximately 31.66% of the variance in streaming hours, suggesting that other factors could further improve its predictive power.

## Usage
### Dependencies
- Install required libraries in R:
  ```R
  install.packages("dplyr")
  install.packages("heplots")


