# ARIMA-GARCH_model

The aim of this model is to try to forecast S&P500 index prices week to week as I am interested in a stock market.
My first hypothesis was that it will not work, because index prices can act like a random walk. Luckily I was wrong - forecasts are quite accurate for this type of data.

I decided to use following explanatory variables:

Crude Oil - oil is important when it comes to transit costs. This is a main commodity which is used for fuel production, so the more expensive oil is, the more expensive are transit costs. Because of that, rising oil prices should lead to falling index price.

Natural Gas - gas is used for instance in heating systems, so rising gas prices should also lead to falling index price. It's because of the fact that companies suffer additional losses due to rising energy costs.

Gold - while watching markets it's quite visible that gold acts like a kind of a substitute for S&P500 index. During a "panic" in a market, investors are more eager to invest in more safe assets like for instance gold. It means that the dependency should be alse negative.

Stock price of steel company - United States Steel Corporation reflects a price of steel in the USA. This metal price can be a determinant of future bullish sentiments so the dependency should be positive.

EURUSD - it is a relative currency strength; I decided to choose a EUR-USD pair, because Europe is a important supply chain for the USA. The stronger dollar is, the more valuable S$P500 index is. It's because the fact that companies can export for example some components at a lower prices. 

Corn - it is a variable which reflects prices of food. It seems to be quite logical that rising food prices will lead to falling index prices.

During the process of making a model I choose only those delays that had the most significance level - all of chosen exogenous variables are delayed, because otherwise any forecasts will not make any sense.

The model will be still developed. I can improve it by adding more exogenous variables. I also have an idea of replacing GARCH component (this module in Python don't have some functions I wanted to implement so it is not a best solution here) by neural network that will work like a anomaly detection (but I'm not sure if it can work good on this kind of data).
