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

- The Final Model Chosen was a `Tuned Random Forest Regressor Model` with the n_estimators tuned to 250.

- The Mean Absolute Error was off by about `$733.198`.

- The Mean Squared Error was `$1,109,606.186`.

- The Root Mean Squared Error had a calculation of `$1,053.378`.

- For the testing set on the model, `59.8%` of the variance in y was explained by x.

Using this model to make predictions about the outlets and their products to increase the sales would not be a very reliable. Considering the previous regression metrics from how the model performed, there is a disparity between the R^2 score and also the Root Mean Squared Error that cannot be ignored.
