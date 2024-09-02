# Analysis of Stock Prices with Macroeconomic Indicators Applied to Different Regression Models

This project explores a variety of regression analysis techniques using S&P500 index companies and their closing prices as dependent variables, with selected macroeconomic indicators as independent variables. The dataset spans 12 years, from January 2012 to December 2023, and is organized on a month-by-month average basis.

## Overview

The main objective was not to see the efficiency of any of the model themselves but to compare the effectiveness of different regression models (basically which performed the least worst) in predicting stock prices using macroeconomic indicators that are less commonly discussed, such as:

- Unemployment Rate
- Federal Funds Rate
- Housing Starts
- Personal Savings Rate
- Average Hourly Earnings
- Money Supply M1
- Long-Term Interest Rates
- Average Weekly Hours
- Personal Consumption Expenditures
- Personal Income

**Models compared:**

- **Linear Regression**
- **Lasso Regression**
- **XGBoost**
- **ARIMA**
- **Random Forest Regressor**

The dataset is already mostly preprocessed, with missing values handled. For details on the data merging process, refer to the `merging.py` file.

## Dependencies

To run this project, you will need the following Python libraries:

- `pandas`
- `numpy`
- `scikit-learn`
- `xgboost`
- `statsmodels`
- `matplotlib`
- `seaborn`

Install the dependencies using pip:

## Results

The following are the results produced. The data and the selected macroeconomic indicators may be responsible for the low R² scores, but the aim was to compare the models rather than to achieve accurate predictions.

- **Linear Regression**
    - Mean Squared Error: `532,286.36`
    - R² Score: `0.4496`

- **Lasso Regression**
    - Mean Squared Error: `629,775.63`
    - R² Score: `0.3488`

- **XGBoost**
    - Mean Squared Error: `950,400.66`
    - R² Score: `0.0173`

- **ARIMA**
    - Mean Squared Error: `4,657,320.97`
    - R² Score: `-3.8156`

- **Random Forest Regressor**
    - Mean Squared Error: `703,187.73`
    - R² Score: `0.2729`

The clear winner here is **Linear Regression**, likely due to the linearity in the model's independent variables and their connections. If more dimensionality were introduced into the model—such as including financial metrics alongside macroeconomic indicators—**Random Forest** might have been the best choice due to its ability to handle nonlinearity. The performance of the **ARIMA** model was underwhelming, possibly due to a lack of understanding of its usage.

## Conclusion

This project provided insights into how different regression techniques perform on a given dataset of stock prices and macroeconomic indicators. The results suggest that while **Linear Regression** may perform well in straightforward, linear scenarios, other models may be better suited for more complex, multidimensional datasets.

## License

This project is licensed under the Apache License - see the [LICENSE](LICENSE) file for details.

