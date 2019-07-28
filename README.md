# Stock Market Analysis
by Kim Dang 

This analysis will focus on the stock of four major tech companies: Amazon, Microsoft, Apple and Google from 2017 to 2018. Here are their stock performance throughout this period:
![alt text](https://stockmarketanalysis.s3.amazonaws.com/stock_Amazon.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/stock_Microsoft.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/stock_Apple.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/stock_Google.png)
---
#### Performance Analysis 

To realize long-term trend, moving averages were calculated from the adjusted closing price and then plotted. In general, the stock prices of these companies are increasing. 
![alt text](https://stockmarketanalysis.s3.amazonaws.com/movingavg_Amazon.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/movingavg_Microsoft.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/movingavg_Apple.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/movingavg_Google.png)

The following figures are daily return percentage based on adjusted closing price. As shown below, the average daily return percentage of each company is approximately 0%. This makes sense because these are daily values. We do not expect to see drastic change in stock prices in a single day. 

![alt text](https://stockmarketanalysis.s3.amazonaws.com/dailyreturn_Amazon.png)

![alt text](https://stockmarketanalysis.s3.amazonaws.com/dailyreturn_Microsoft.png)

![alt text](https://stockmarketanalysis.s3.amazonaws.com/dailyreturn_Google.png)

![alt text](https://stockmarketanalysis.s3.amazonaws.com/dailyreturn_Apple.png)

In order to discover correlation between any company, Pearson product-momentum correlation coefficients were calculated from daily return percentage. This value will provide a sense of how correlated two sets of stock data are: 1 being very correlated and 0 means no correlation. 

|         | AAPL    | GOOGL  |MSFT  |AMZN   |
| ------- |:-------:| ------:|-----:|-------|
|AAPL     | 1.000000|0.614818|0.632272|0.517114|
|GOOGL   | 0.614818 | 1.000000 |0.774403|0.624475|
| MSFT    |0.632272 |0.774403|1.000000|0.674897|
|AMZN     |0.517114 |0.624475|0.674897|1.000000| 

According to table above, Microsoft and Google have the highest Pearson coefficient (0.774), which means there exists a strong relationship between the stocks of these two companies. 
___
### Risk Analysis 
A simple risk analysis can be achieved by treating the average value and standard deviation as expected return value and risk, respectively. According to the figure below, Amazon stock has the highest return percentage and is most likely to fluctuate.
![alt text](https://stockmarketanalysis.s3.amazonaws.com/riskstd.png)

Here are the 1% empirical quantile of each company:  
GOOGL -- 4.58%
AAPL -- 2.84%
AMZN -- 3.94%
MSFT -- 4.06%
These values were calculated from the daily return percentage dataset. Simply put, if you invest in Google, for example, the worst you could lose in one day is 4.58%. 

Finally, the Monte Carlo algorithm was used to predict stock prices in March 2019. You can read more about Monte Carlo algorithm [here](https://www.investopedia.com/terms/m/montecarlosimulation.asp). The following figures are generated from the results of running 500 simulations per company.
![alt text](https://stockmarketanalysis.s3.amazonaws.com/montecarlo_GOOGL.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/montecarlo_AMZN.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/montecarlo_MSFT.png)
![alt text](https://stockmarketanalysis.s3.amazonaws.com/montecarlo_AAPL.png)

The stock prices in March 2019 are predicted to be: 
| AMZN    | GOOGL  |MSFT  |AAPL   |
|:-------:| ------:|-----:|-------|
| $1,504  |$1,008  |$89   |$168   |

Here are the actual stock prices in March 2019: 
*Source: Yahoo Finance*
| AMZN    | GOOGL  |MSFT  |AAPL   |
|:-------:| ------:|-----:|-------|
| $1,671  |$1,148  |$112  |$174   |








