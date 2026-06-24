  # Prediction of Product Sales

## Overview

This project aims to predict product sales using machine learning techniques. The objective is to help retailers understand which product and store characteristics have the greatest impact on sales performance and support better business decisions.



## Business Problem

Retailers need to understand which product and outlet characteristics contribute to higher sales in order to improve inventory planning and business decisions.

---

## Data

The dataset contains information about products and outlets, including item characteristics, outlet information, and sales values.

Features include:

- Item Weight
- Item Visibility
- Item MRP
- Outlet Type
- Outlet Establishment Year

Target:
- Item_Outlet_Sales

---

## Methods

- Data cleaning
- Handling missing values
- Exploratory Data Analysis (EDA)
- Data preprocessing
- Model training and evaluation

---

## Results

### Visualization 1: Distribution of Product Sales

![Distribution of Sales](images/histo.png)

The sales distribution is positively skewed, meaning most products generated lower sales values while only a limited number achieved very high sales. This suggests that a small group of products contributes heavily to total sales.


---

### Visualization 2: Correlation Between Features and Sales

![Correlation Heatmap](images/corr.png)

Item_MRP showed the strongest positive relationship with sales (0.57), indicating that product price is one of the most influential factors affecting sales performance, while other numerical features showed weak relationships.


## Model

The final selected model was the tuned Random Forest Regressor after optimizing the hyperparameters using GridSearch.

Evaluation metrics on the test data:

- R² Score = 0.602
- RMSE = 1047.383
- MAE = 729.285

The tuned Random Forest model improved performance compared to the default model and explained approximately 60% of the variation in product sales. This makes it a suitable model for supporting sales prediction and business decision-making.


## Recommendations

Based on the analysis and model results, retailers should focus on product and outlet characteristics that have the greatest impact on sales performance. Since Item_MRP showed the strongest relationship with sales, pricing strategies and product selection can be optimized to improve overall sales performance. Additionally, using predictive models can support inventory planning and business decision-making.


## Model

### Linear Regression Coefficients

![Linear Regression Coefficients](images/linear_regression_coefficients.png)

#### Interpretation of Coefficients

**1. Item_MRP (Coefficient = 984.18)**
This had the strongest impact on sales prediction. As product price increases, predicted sales also increase.

**2. Outlet Identifier – OUT027 (Coefficient = 710.96)**
Products sold in Outlet OUT027 tend to have higher sales compared to other outlets.

**3. Outlet Type – Supermarket Type 3 (Coefficient = 710.96)**
This outlet type is associated with higher sales and generally performs better than other outlet types.

---

### Tree-Based Model – Feature Importances

![Random Forest Feature Importances](images/random_forest_feature_importances.png)

#### Interpretation of Feature Importance

**1. Item_MRP (Importance = 0.554)**
Product price was the most important factor affecting sales prediction.

**2. Outlet Type – Grocery Store (Importance = 0.313)**
Store type strongly influenced sales performance.

**3. Outlet Identifier – OUT027 (Importance = 0.061)**
This outlet contributed positively to sales prediction.

**4. Outlet Type – Supermarket Type 3 (Importance = 0.044)**
This outlet category showed stronger sales performance.

**5. Outlet Establishment Year (Importance = 0.023)**
Store age had a smaller but noticeable effect on prediction.

---

## Recommendations

* Focus on pricing strategies because Item_MRP had the strongest impact on sales.
* Improve performance in lower-performing outlet types.
* Study the characteristics of high-performing outlets.
* Consider outlet age and store type when making business decisions.









## Limitations & Next Steps

This project has some limitations, including the available dataset size and the limited number of features used for prediction. Future improvements may include testing additional machine learning models, applying advanced feature engineering techniques, and collecting more data to improve prediction accuracy and model performance.

### For Further Information

See the notebook and repository documentation for additional project details and implementation steps.
