#House-price-predictions
the dataset can be obtained from Kaggle.
link: https://www.kaggle.com/c/house-prices-advanced-regression-techniques/
The link contains train set and test set 

##Goal
We have to Predict house prices in Ames,Iowa using regression techniques. We have 80 independent features and 1 dependent feature SalePrice

##Data Preprocessing 
1. Removed Null columns having more than 90% null values.
2. Applied log transformation on the training set to reduce the skewness.
3. Removed YearBuilt column as it had too many features.

###Effect of Applying log transformation on SalePrice
<br> Reduces the skewness of SalePrice
![Skewness](https://user-images.githubusercontent.com/26299390/87929556-f1ab6400-cac9-11ea-9024-0ca8ddda528e.PNG)

###Distribution of independent features
![distribution](https://user-images.githubusercontent.com/26299390/87931534-51573e80-cacd-11ea-834c-a9549d1c5de9.PNG)

###Null Values 
<br> More than 90% percentage was removed. 
<br> Less than 90% where filled with mode for categorical features 
<br> Filled with a combination of mean and median for Numerical features
![Null Values](https://user-images.githubusercontent.com/26299390/87932829-819fdc80-cacf-11ea-972e-593a127d9dc3.PNG)

###Effect of applying log transformation on independent features using boxcox1p to reduce skewness
![independent_skew](https://user-images.githubusercontent.com/26299390/87933037-de02fc00-cacf-11ea-8fad-2a728d2b8bf0.PNG)

##ML Model Selection and Prediction
<br> Used 6 different algorithms to assess the model performance on the training set using cross validation.
1. Linear Regression
2. Gradient Boosting Regressor
3. Random Forest Regressor
4. AdaBoost Regressor
5. XGB Regressor
6. Support Vector Regressor
Process involved was running hyperparamaters for each model using GridSearch.
<br> Further stacked all models and used blended combination of the algorithms to provide even a better accurate prediction. 

![ML algo perfm](https://user-images.githubusercontent.com/26299390/87935124-d04f7580-cad3-11ea-9960-450a9a4215a2.PNG)

##Conclusion
<br> The Blended model yielded a performance with an RMSE of 0.12
