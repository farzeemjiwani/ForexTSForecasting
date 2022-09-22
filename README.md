# Machine Learning Approaches to Investigate Fundamentals That Impact the Trends in Foreign Exchange Rates

# Abstract
The aim of this paper is to examine disparate economic factors that influence the US and the Canadian
dollar exchange rate using machine learning techniques. Exchange rate forecasting is one of the attractive
and challenging issues in international economics, as many uncertain factors come into play concurrently.
Therefore, improving the accuracy of forecasting exchange rates and analyzing the fundamentals is of great
interest to market participants, policymakers, and academics. One of the prominent issues for exchange
rate prediction is the features driving it. The challenge of choosing the optimal forecasting model is mostly
a result of the frequent changes among the factors impacting exchange rates. By taking into account a
variety of alternative fundamentals that affect the Canadian dollar, we statistically evaluate the forecasting
performance of the models and focus on understanding what drives movements in the Canadian dollar, and
which indicators influence the CAD dollar the most. There are diverse attributes that could prospectively
impact the exchange rate, e.g., the unemployment rate, purchasing power, oil price volatility and money
supply. We forecast the exchange rate using traditional models, in particular, Random Forests, Extra Trees,
XGBoost, Support Vector Machines, Lasso, and Ridge, as well as deep learning models, namely, LSTM and
GRU. Evaluation is carried out using out-of-sample testing against standard regression metrics, specifically
normalized deviation (ND), mean absolute error (MAE), root mean squared error (RMSE), and normalized
root mean squared error (NRMSE). In addition to modeling the selected rates and indices mentioned above
as potential features, the study aims to interpret the results using techniques such as SHAP to quantify
the amount of significance each macroeconomic component attributes to change in the exchange rate. Our
results indicate that the linear regression models namely, Lasso and Ridge regression, perform better than
the others on spatial information. However, the deep learning models outperform others when trained on
temporal information. While purchasing power parity, unemployment, money supply stocks, and oil prices
were generally major factors in driving the exchange rate movement, the S&P 500 and commodity price
indexes came out as significant for deep learning models. The need for a model that can predict foreign
exchange rate direction and account for the relationship between these macroeconomic fundamentals and
the exchange rate, will be an outstanding contribution as this helps understanding which economic factors
drive the fluctuations in the exchange rates.

# Dataset
The below list contains the data sources for the macroeconomic features and the target variable, along with their frequencies:

* **USD/CAD** - *Daily* - https://fred.stlouisfed.org/series/DEXCAUS
* **IR** - *Monthly* - https://data.oecd.org/interest/short-term-interest-rates.htm
* **CPI (PPP)** - *Yearly* - https://data.oecd.org/conversion/purchasing-power-parities-ppp.htm#indicator-chart
* **PPI** - *Monthly* - https://data.oecd.org/price/producer-price-indices-ppi.htm
* **M1** - *Monthly* - https://data.oecd.org/money/broad-money-m1.htm#indicator-chart
* **M3** - *Monthly* - https://data.oecd.org/money/broad-money-m3.htm#indicator-chart
* **SP500** - *Daily* - https://fred.stlouisfed.org/series/SP500 (From May 2012), https://ca.investing.com/indices/us-spx-500-historical-data
* **TSX**- *Daily* - https://finance.yahoo.com/quote/%5EGSPTSE/history?period1=1230768000&period2=1640995200&interval=1d&filter=history&frequency=1d&includeAdjustedClose=true
* **Gold** - *Daily* - https://data.nasdaq.com/data/LBMA/GOLD-gold-price-london-fixing 
* **Oil** - *Monthly* - https://fred.stlouisfed.org/series/WTISPLC 
* **ED** - *Daily* -https://www.marketwatch.com/investing/interestrate/liborusd3m/download-data?startDate=1/1/2009&endDate=1/3/2022&countryCode=mr
* **Unemployment** - *Monthly* - https://fred.stlouisfed.org/series/LRUNTTTTCAM156S
* **Commodity Price (BCPI)** - *Monthly* - https://www.bankofcanada.ca/rates/price-indexes/bcpi/
* **Industrial production** - *Monthly* - https://data.oecd.org/industry/industrial-production.htm


# Repository Structure
`data` folder contains all the different datasets fr=or the fundamentals used in the thesis, along with the final dataset. 

`Modeling.ipynb` inside the `src` folder contains the modeling code for this project, while `DataCollection.ipynb` contains the data aggregation and transformation logic.

`results` folder contains all the one-step and multi-step forecast graphs including the SHAP summary plots.

# Final Report
`FarzeemJiwani_DS_MRP_Final.pdf` has the detailed explanation about the research objectives and methodology of the study.

