# Factors-Influencing-US-House-Prices (Overview)
Task - Using publically available data for the national factors that impact supply and demand of homes in US, build a model to study the effect of these variables on home prices.

This project aims to predict US house prices based on various economic indicators and demographic factors. We aim to explore the relationships between these variables and the Case-Shiller Home Price Index (CSUSHPISA). The analysis includes data preprocessing, correlation analysis, feature selection, and the application of linear regression, Random Forest, and XGBoost models.

*Technologies Used*: Python, Numpy, Pandas, sk-learn, Linear Regression, Random Forest, XGBoost

# Dataset
The following variables are chosen for the study-

1. Unemployment Rate (https://fred.stlouisfed.org/series/UNRATE)
2. Per Capita GDP (https://fred.stlouisfed.org/series/A939RX0Q048SBEA)
3. Median Household Income (https://fred.stlouisfed.org/series/MEHOINUSA672N)
4. Construction Prices  (https://fred.stlouisfed.org/tags/series?t=construction%3Bprice+index)
5. CPI  (https://fred.stlouisfed.org/tags/series?t=construction%3Bprice+index)
6. Interest Rates (https://fred.stlouisfed.org/categories/22)
7. Number of new houses supplied (https://fred.stlouisfed.org/series/MSACSR)
8. Working Population  (https://fred.stlouisfed.org/series/LFWA64TTUSM647S)
9. Urban Population   (https://fred.stlouisfed.org/tags/series?t=annual%3Bpopulation%3Busa)
10. Federal Funds (https://fred.stlouisfed.org/series/FEDFUNDS)
11. Housing subsidies (https://fred.stlouisfed.org/tags/series?t=bea%3Bhousing%3Bsubsidies)
12. Number of Households (https://fred.stlouisfed.org/series/TTLHH)
    
As a proxy to the home prices, S&P CASE-SHILLER Index is used.

All data is downloaded from [https://fred.stlouisfed.org/].


# Correlation Analysis
I analyzed the correlation among variables using a correlation matrix and visualized it with a heatmap. Key observations include:
•	A negative correlation between the unemployment rate and home prices.
•	The unexpectedly low correlation for the number of new houses.
•	The impact of the Great Recession on various plots.
•	A positive correlation between the per_capita_GDP and home prices.

![image](https://github.com/Madhur-01/Factors-Influencing-US-Home-Prices/assets/108746195/44627cd6-5316-4ffd-ba5f-e22f180edab7)

# Model Performance
The dataset is scaled, and training and validation sets are divided.

•	R-squared for the validation set in the case of Random Forest is 0.995

•	R-squared for the validation set in the case of XGBoost is 0.985

•	R-squared for the validation set in the case of Linear Regression is 0.909
![image](https://github.com/Madhur-01/Factors-Influencing-US-Home-Prices/assets/108746195/0889d106-f984-4735-bff7-a4f54fcee091)

# Articles refered - 

https://www.forbes.com/siteS/forbesbizcouncil/2021/10/25/us-housing-supply-obstacles-and-opportunities/?sh=49dfdc1740dc

https://pvsbuilders.com/economic-factors-affecting-housing-market/

Https://www.investopedia.com/articles/mortages-real-estate/11/factors-affecting-real-estate-market.asp

https://www.economicshelp.org/blog/377/housing/factors-that-affect-the-housing-market/

https://www.jstor.org/stable/29783816

Research Papers refered -

https://www.atlantis-press.com/article/25841966.pdf

A few variables that could have been studied are below.

1. Net-immigration (It is supposed to have a positive impact. No suitable data could be found)
2. Marriage Rate (People tend to buy homes after they get married. So, it might have some effect. No data could be found)
3. Average house size (The data was available only for the years after 2015. Though it is expected that an increase in the average house size would increase prices, it is found that the average home size has been 4. consistently decreasing although the prica has been increasing)
5. Land availability (Less land, higher prices. Perhaps this is why the prices has been rising even though the average house size has been decreasing. No relevant data could be found)
6. Tax Rate (Too many brackets (7) and could not analyse due to time)
7. Number of active listings (Data prior to 2017 was not found)
