# Customer_Churn_Analysis_Project
## 1. Introduction
This project involved an exploratory data analysis (EDA) of an online retail customer dataset to understand customer behavior and identify potential factors contributing to customer churn. The primary goal was to gain insights that could inform strategies for customer retention.

## 2. What was done (Methodology)
### Data Loading and Initial Inspection
*   The `online_retail_customer_churn.xlsx` dataset was loaded into a pandas DataFrame.
*   The shape of the dataset (rows and columns) was identified as (1000, 15).
*   Checked for missing values: No missing values were found across any column.
*   Verified data types: All columns were correctly typed, with no inconsistencies (e.g., numeric data stored as objects).
*   Duplicate records: No duplicate customer records were identified.

### Descriptive Statistics
*   Calculated mean, median, and standard deviation for `Age`, `Annual_Income`, and `Total_Spend`. These statistics provided an overview of customer demographics and spending habits.

### Customer Segmentation by Spending
*   Identified customers in the highest and lowest 10% of `Total_Spend`.
*   Compared their characteristics (Age, Annual Income, Number of Purchases, Satisfaction Score, Churn Rate) to the overall customer base to understand differences.

### Distribution and Relationship Analysis
*   **Customer Satisfaction**: Plotted the distribution of `Satisfaction_Score` to see common satisfaction levels and extremes.
*   **Gender Distribution**: Visualized the distribution of customers across different genders.
*   **Churn by Gender**: Calculated and visualized churn rates for each gender to identify any disparities.
*   **Promotion Response**: Analyzed the distribution of `Promotion_Response` to determine the most common response type.
*   **Years as Customer vs. Total Spend**: Explored the relationship between `Years_as_Customer` and `Total_Spend` using a scatter plot and correlation coefficient (correlation: ~0.037), indicating a very weak positive linear relationship.
*   **Number of Purchases vs. Total Spend**: Examined the relationship between `Num_of_Purchases` and `Total_Spend` with a scatter plot and correlation coefficient (correlation: ~0.046), also indicating a weak positive relationship.
*   **Email Opt-In vs. Churn**: Compared churn rates between customers who opted in for emails and those who did not, finding a negligible difference.

## 3. Why it was done (Objective)
The main objectives of this analysis were:
*   To gain a comprehensive understanding of the dataset's structure and quality.
*   To explore key customer attributes and their distributions.
*   To identify relationships between different customer characteristics and their spending/churn behavior.
*   To uncover potential factors or segments that might be more prone to churn, thereby providing actionable insights for business strategies.

## 4. Outcome (Key Findings)
*   The dataset was clean, with no missing values or duplicates, and appropriate data types.
*   The customer base is diverse in terms of age, income, and spending.
*   Highest spenders tend to have a slightly higher churn rate compared to the lowest spenders (53% vs 46%).
*   Customer satisfaction is broadly distributed, with moderate to high satisfaction levels being common.
*   The churn rate varies slightly by gender, with 'Other' gender having a slightly higher churn rate.
*   'Unsubscribed' was the most common promotion response.
*   There is a very weak positive linear relationship between `Years_as_Customer` and `Total_Spend`, and `Num_of_Purchases` and `Total_Spend`, suggesting these factors are not strong predictors of overall spend.
*   Email opt-in status shows a negligible difference in churn rates (52.55% for opt-in vs. 52.65% for non-opt-in), indicating it is not a significant factor in churn for this dataset.

## 5. Challenges
*   **Weak Correlations**: Identifying strong linear relationships between some key variables like `Years_as_Customer` or `Num_of_Purchases` and `Total_Spend` proved challenging due to their very weak correlations. This suggests that more complex interactions or other unmeasured variables might be at play.
*   **Interpreting Negligible Differences**: While quantitative analysis showed a minimal difference in churn rates based on email opt-in, it was important to clearly communicate that this difference was not statistically significant enough to draw strong conclusions about its impact on churn.
*   **Actionable Insights from Weak Signals**: The primary challenge was extracting highly actionable insights when many relationships were weak. This highlights the need for further, deeper analysis or for potentially incorporating external data sources to build more predictive churn models.
