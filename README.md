# Prediction of Product Sales
## Analyzing Food Sales at Various Stores
Ali Abu Nimah
### The project will be a sales prediction for food items sold at various stores. The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.
## Data Source:
Prediction of Product Sales https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view<br/>
For this dataset, there were 8523 rows and 12 columns.
## Data Dictionary
![image](https://github.com/user-attachments/assets/07569019-756b-45db-86b2-c1602f0ec385)
### To prepare this data, the data was cleaned, and the following processes were performed:
**Exploratory Data Analysis**

```
- During the exploratory data analysis, a boxplot and histogram was visualized for each numeric datatype column.
- Also, a countplot was visualized for each categorical column.
- This gave a good baseline for all of the numeric and categorical columns for univariate EDA.
```
![outletsales](https://github.com/user-attachments/assets/43e4ae84-93ec-4321-a447-c73a60c4476b)</br>
The hisorgram shows that the data is right-skewed, with most sales below 6000, while a few high-sales outliers raise the average and need further analysis.</br></br>
![itemtype](https://github.com/user-attachments/assets/1ed954a7-0eb5-4805-bf0f-6c363e1ffd68)</br>
"Fruits and Vegetables" and "Snack Foods" dominate sales, reflecting their appeal to health-conscious and snack-loving customers.</br>

**Maching Learning Using the Following Models:**
```
- Linear Regression Model
- Random Forest Regressor Model
- Tuned Random Forest Regressor Model
```
## Models Evaluated & Results
- Linear Regression Model (Testing Set):
  - MAE = 804.120
  - MSE = 1,194,349.715
  - RMSE = 1,092.863
  - R^2 = 0.567
- Random Forest Regressor Model (Testing Set):
  - MAE = 774.203
  - MSE = 1,243,901.420
  - RMSE = 1,115.303
  - R^2 = 0.549
- Tuned Random Forest Regressor Model (Testing Set):
  - MAE = 733.198
  - MSE = 1,109,606.186
  - RMSE = 1,053.378
  - R^2 = 0.598

- The Final Model Chosen was a `Tuned Random Forest Regressor Model` with the n_estimators tuned to 150.

- The Mean Absolute Error was off by about `$733.198`.

- The Mean Squared Error was `$1,109,606.186`.

- The Root Mean Squared Error had a calculation of `$1,053.378`.

- For the testing set on the model, `59.8%` of the variance in y was explained by x.

Using this model to make predictions about the outlets and their products to increase the sales would not be a very reliable. Considering the previous regression metrics from how the model performed, there is a disparity between the R^2 score and also the Root Mean Squared Error that cannot be ignored.
## Features Coefficients and Importance
### Linear Regression Model Features Coeffecients Analysis
![cc](https://github.com/user-attachments/assets/ee25a5e7-abfc-4454-b127-edb80fac1b45) </br>
**Top 3 Impactful Features:**
1. Item_MRP (Maximum Retail Price): `+984.5` Coefficient
  - For every `1 unit` increases in an item's price, the sales increases approximately by `$984.5`, that means when the item is priced higher, it generates more revenue.
2. Outlet_Type_Supermarket Type3: `+808.3` Coefficient
  - The items in supermarket type 3 are sold higher than any other store type by `$808.3`.
3. Outlet_Type_Grocery Store: `-1,068.3` Coefficient
  - The items in Grocery Store are sold lower than any other store type by `$1,068.3`, that could be because of cheaper prices as we mentioned higher priced items give more revenues.
### Random Forest Regressor Model Features Importance Analysis
![ff](https://github.com/user-attachments/assets/21d47ff2-579f-42c2-a037-72374ddbb4f9) </br>
As we notice in here the **top 3 features** by importance is almost the same as coeffecients but the order for `2nd` and `3rd` are changed.
1. Item_MRP: `52%` importance.
2. Outlet_Type_Grocery Store: `27%` importance.
3. Outlet_Type_Grocery Store: `5%` importance.
4. Item_Visibility: `4%` importance, negative impact, which might be counterintuitive, maybe due to clearance items being more visible but less popular.
5. Item_Weight: `1%` importance, a negative coefficient, suggesting that heavier items tend to have lower sales.
## Recommendations
### Product Strategy
- Optimize Weight: Since heavier items are negatively correlated with sales, consider redesigning packaging or offering lighter alternatives.
- Refine Product Visibility: The negative relationship between visibility and sales suggests overexposed or clearance items may be underperforming. Reassess product placement and promotional strategies.
### Inventory & Merchandising
- Prioritize Top-performing Categories: Focus stock and marketing on product types with higher predicted sales.
- Dynamic Pricing: Combine prediction scores with historical demand to apply discounts strategically.
### Marketing & Promotions
- Target High-Performing Segments: Direct marketing efforts toward product lines with the highest predicted sales potential.
- Personalized Promotions: Use model predictions to suggest bundle offers or complementary products to increase average order value.

## Limitations & Next Steps
### Limitations
- Data Scope: The dataset may not reflect recent sales trends or seasonal patterns.
- Feature Granularity: Some influential factors like customer demographics, ad spend, or competitor pricing were not included.
### Next Steps
- Incorporate Time Series Trends: Add time-related variables (e.g., month, week, seasonality) to improve forecasting accuracy.
- Feature Enrichment: Enhance the dataset with promotional data, customer segmentation, or online activity (e.g., clicks, pageviews).
- A/B Testing: Validate model recommendations with real-world tests (e.g., offering lighter packaging).
- Deployment & Dashboarding: Consider deploying the model in a simple dashboard using Power BI to allow sales teams to simulate predictions live.
## For Further Information
For any additional questions, please contact:
- Ali Abu Nimah 📧 [alibassab25@gmail.com](mailto:alibassab25@gmail.com)
