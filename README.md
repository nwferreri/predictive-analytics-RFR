# Predictive Analytics - Random Forest Regressor

## Goal

We want to be able to predict the income of a customer based on a number of factors.

## Data

~2200 entries with the following features:
* `ID`: Customer's unique identifier
* `Year_Birth`: Customer's birth year
* `Education`: Customer's education level
* `Marital_Status`: Customer's marital status
* `Income`: Customer's yearly household income - **This will be predicted**
* `Kidhome`: Number of children in customer's household
* `Teenhome`: Number of teenagers in customer's household
* `Dt_Customer`: Date of customer's enrollment with the company
* `Recency`: Number of days since customer's last purchase
* `Complain`: 1 if customer complained in the last 2 years, 0 otherwise
* `MntWines`: Amount spent on wine in last 2 years
* `MntFruits`: Amount spent on fruits in last 2 years
* `MntMeatProducts`: Amount spent on meat in last 2 years
* `MntFishProducts`: Amount spent on fish in last 2 years
* `MntSweetProducts`: Amount spent on sweets in last 2 years
* `MntGoldProds`: Amount spent on gold in last 2 years
* `NumDealsPurchases`: Number of purchases made with a discount
* `AcceptedCmp1`: 1 if customer accepted the offer in the 1st campaign, 0 otherwise
* `AcceptedCmp2`: 1 if customer accepted the offer in the 2nd campaign, 0 otherwise
* `AcceptedCmp3`: 1 if customer accepted the offer in the 3rd campaign, 0 otherwise
* `AcceptedCmp4`: 1 if customer accepted the offer in the 4th campaign, 0 otherwise
* `AcceptedCmp5`: 1 if customer accepted the offer in the 5th campaign, 0 otherwise
* `Response`: 1 if customer accepted the offer in the last campaign, 0 otherwise
* `NumWebPurchases`: Number of purchases made through the company’s web site
* `NumCatalogPurchases`: Number of purchases made using a catalogue
* `NumStorePurchases`: Number of purchases made directly in stores
* `NumWebVisitsMonth`: Number of visits to company’s web site in the last month


## Analysis

Data was cleaned and prepared to run a Random Forest Regressor (RFR). `ID`, `Dt_Customer`, and `Recency` were dropped.

Initial RFR model was run and evaluated using mean absolute error (MAE).

Parameter tuning was performed to improve the model.

## Insights

The final model was run and evaluated again using MAE. The standard deviation was much larger than the MAE, giving confidence in the model's performance.

Feature importance was calculated and showed that the most impactful metrics to predict a customer's income were `MntWines` (amount spend on wine in the last 2 years) followed by `MntMeatProducts` (amount spent on meat in the last 2 years).
