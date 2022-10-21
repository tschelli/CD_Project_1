# Sales Prediction Project

Author: Tyler Schelling

<p align="center">
  <img src = "https://t3.ftcdn.net/jpg/02/72/40/68/360_F_272406819_djyh9kysHidrdUOgoDEujj7HGSOwzlmS.jpg">
</p>
  
## Data Dictionary for the Dataset
Variable Name	   |  Description
-------------------|------------------
Item_Identifier	   |  Unique product ID
Item_Weight	       |  Weight of product
Item_Fat_Content	| Whether the product is low fat or regular
Item_Visibility	|The percentage of total display area of all products in a store allocated to the particular product
Item_Type	|The category to which the product belongs
Item_MRP	|Maximum Retail Price (list price) of the product
Outlet_Identifier	|Unique store ID
Outlet_Establishment_Year	|The year in which store was established
Outlet_Size|	The size of the store in terms of ground area covered
Outlet_Location_Type	|The type of area in which the store is located
Outlet_Type	|Whether the outlet is a grocery store or some sort of supermarket
Item_Outlet_Sales	|Sales of the product in the particular store. This is the target variable to be predicted.

This project looked at feautures of a grocery retailer to determine their role in increasing sales.

## Insights
### Total Sales by Outlet Size
![image](https://user-images.githubusercontent.com/18369971/197112636-12aba6ee-e923-4223-bed2-29955c57cab5.png)
- The medium sized outlets had ~32% of total sales.
- Further information on Sq.Ft. ranges of each outlet size is needed for more granular impacts.
- Unknown accounted for more than a quarter of all outlet sizes. 
- Further information regarding the Unknown category is needed. 

### Top Selling Item Types
![image](https://user-images.githubusercontent.com/18369971/197113407-c9200ad6-2d6d-42bd-8c16-e3d4a8db8feb.png)
- The highest selling category are Fruits and Vegetables, accounting for ~16% of total sales. 
- Snack Foods was close in second, accounting for ~14% of total sales. 

## Model Comparison

Model | MAE | MSE | RMSE | R2
---|---|---|---|---
Linear Regression Train| 847.15|1,297,592.08|1,139.12|0.5615
Linear Regression Test| 804.13|1,194,389.56|1,092.88|0.5671
Decision Tree Optimized Train|762.77|1,172,212.98|1,082.69|0.6039
Decision Tree Optimized Test |738.02|1,117,511.96|1,057.12|0.5950
Random Forest Optimized Train|755.55|1,152,335.54|1,073.47|0.6106
Random Forest Optimized Test |727.39|1,091,546.28|1,044.77|0.6044

### MAE - Mean Absolute Error
  - The optimized random forest model provided the lowest MAE value of 727.39 on the test data.

### MSE - Mean Square Error
  - The optimized random forest model provided the lowest MSE value of 1091546.28 on the test data.

### RMSE - Root Mean Square Error
  - The optimized random forest model provided the lowest RMSE value of 1044.77 on the test data.

### R2 - Coefficient of Determination
  - The optimized random forest model provided the highest R2 value of 0.6044 on the test data.

#### The optimized Random Forest model is the recommended model due to the lowest metrics and highest R2 value.
