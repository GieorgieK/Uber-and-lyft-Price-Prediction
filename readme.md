# Uber and Lyft Price Prediction in New York

## Background

This project involves predicting ride prices for Uber and Lyft in New York using regression models. The dataset includes booking data for Uber and Lyft in New York during November and December 2013, along with weather information at the time of booking. The data can be accessed [here](https://www.kaggle.com/datasets/andrewmvd/trip-advisor-hotel-reviews/data).

## Objective

The objective of this project is to understand the concept of regression using Linear Regression, prepare data for use in the Linear Regression model, and implement Linear Regression to make predictions. This project encompasses understanding the basic theory of Linear Regression, data collection and cleaning, initial exploration and analysis of the data, and performing feature engineering to improve model performance. Additionally, the project aims to build, train, and test the model, as well as assess its accuracy and performance. The results of the model will be interpreted comprehensively.

## Tools
[<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" />](https://pandas.pydata.org/)
[<img src="https://img.shields.io/badge/Seaborn-388E3C?style=for-the-badge&logo=seaborn&logoColor=white" alt="Seaborn" />](https://seaborn.pydata.org/)
[<img src="https://img.shields.io/badge/Numpy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="Numpy" />](https://numpy.org/)
[<img src="https://img.shields.io/badge/Matplotlib-3776AB?style=for-the-badge&logo=matplotlib&logoColor=white" alt="Matplotlib" />](https://matplotlib.org/)
[<img src="https://img.shields.io/badge/Scikit%20learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn" />](https://scikit-learn.org/)

## Model Training

The two models chosen for comparison are Linear Regression and Ridge Regression.

### Linear Regression

Linear Regression is used as the baseline model to predict ride prices based on the available features.

### Ridge Regression

Ridge Regression is selected due to its ability to handle high multicollinearity among features. This model is particularly useful when the data has high multicollinearity but the goal is to retain all features, and the data contains outliers.

**Hyperparameter: Alpha (α)**
Alpha is used to control regularization by increasing the penalty on the magnitude of coefficients, resulting in a model with smaller coefficients that can reduce overfitting.

## Conclusion

Both Linear Regression and Ridge Regression (with alpha=1 and alpha=100) provide excellent and almost identical performance in predicting Uber and Lyft prices. Regularization with Ridge Regression does not yield significant improvements. The high R² values and consistency of evaluation metrics between training and test data indicate that the models have strong predictive power and do not suffer from overfitting.

Using Ridge Regression with regularization (alpha=1 and alpha=100) offers better stability in coefficients compared to Linear Regression, as evidenced by more reasonable and consistent coefficient values. Evaluation metrics indicate that all models perform exceptionally well, but Ridge Regression has an advantage in terms of stability and multicollinearity control, making it a more appropriate choice for predicting Uber and Lyft ride prices.

The Ridge Regression model with alpha=1 demonstrates good predictive accuracy on inference data, with most predictions close to actual values and some significant errors. This model effectively balances fitting the training data and generalizing to new data, as seen from the small, randomly scattered residuals. However, some large residuals suggest room for improvement, possibly through further model tuning or incorporating more diverse training data to better capture variability. Overall, Ridge Regression provides a reliable approach for predicting ride prices while controlling overfitting and multicollinearity.

