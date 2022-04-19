# REGRESSION: Bitcoin Price Predict

## Overview

* Predict Bitcoin **daily close price** before the end of traidng day. 
* **Data** from **KraKen API OHLC endpoint** combined with OHLC for historical data dated back to 2013. 
* **Machine Learning Model** used initially is **Support Vector Machine**. However, other ML models can be used to compare and improve accuracy.

![png](images/btc_close_line.png)


---

## Data Source and Preparation
**KraKen API** and historical OHLC csv
* [KraKen API OHLC][https://docs.kraken.com/rest/#operation/getOHLCData]
* [historical OHLC][https://support.kraken.com/hc/en-us/articles/360047124832-Downloadable-historical-OHLCVT-Open-High-Low-Close-Volume-Trades-data]


### Visualizing the Data

![png](images/btc_close_box.png)

![png](images/btc_vol_line.png)
![png](images/btc_vol_box.png)


![png](images/btc_trds_line.png)
![png](images/btc_trds_box.png)

## Data Modeling

## Evaluation

![png](images/predict_actual.png)

![png](images/predict_actual_april22.png)

Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, aliquid cum vitae, ipsa consequatur amet eum maiores sequi dolorum id minus dolore. Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, aliquid cum vitae, ipsa consequatur amet eum maiores sequi dolorum id minus dolore.


Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, aliquid cum vitae, ipsa consequatur amet eum maiores sequi dolorum id minus dolore. Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, aliquid cum vitae, ipsa consequatur amet eum maiores sequi dolorum id minus dolore.

## Possible Application/Business Problem

* Help inform retail investors/users possible close price, ruturn , trend of Bitcoin and other cryptocurrency
* The model can be developed to live prediction and with shorter timeframe, 4 hours, 1 hours as example
* The model can be improved, modified and used with other cryptocurrency or stocks

## Conclusions
