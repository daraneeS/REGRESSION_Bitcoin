# REGRESSION: Bitcoin Price Predict

## Overview

* Predict Bitcoin **daily close price** before the end of traidng day. 
* **Data** from **KraKen API OHLC endpoint** combined with OHLC for historical data dated back to 2013. 
* **Machine Learning Model** used initially is **Support Vector Machine**. However, other ML models can be used to compare and improve accuracy.

![png](images/btc_close_line.png)


---

## Data Source and Preparation

* **KraKen Historical OHLC**
* **KraKen API OHLC**

```
kraken_ohlc_cols = ["date","open", "high", "low", "close", "vwap","volume", "trades"]

resp = requests.get('https://api.kraken.com/0/public/OHLC?pair=XBTUSD&interval=1440&since=unix_now').json()

xbt_apr22_df = pd.DataFrame(resp["result"]['XXBTZUSD'])

xbt_apr22_df.columns = kraken_ohlc_cols
```
## Visualization

![png](images/btc_close_box.png)
![png](images/btc_vol_line.png)
![png](images/btc_vol_box.png)
![png](images/btc_trds_line.png)
![png](images/btc_trds_box.png)

## Support Vector Machine
```
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import GridSearchCV
from sklearn.metrics  import mean_squared_error, r2_score
from sklearn.svm import SVR
```
```
scaler = StandardScaler()
X_scaled_train = scaler.fit_transform(X_train)
X_scaled_test = scaler.transform(X_test) 
# not using fit to avoid data leakage 
```
![png](images/param.png)



## Result

![png](images/predict_actual.png)
![png](images/predict_actual_april22.png)

Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, aliquid cum vitae, ipsa consequatur amet eum maiores sequi dolorum id minus dolore. Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, aliquid cum vitae, ipsa consequatur amet eum maiores sequi dolorum id minus dolore.


Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, aliquid cum vitae, ipsa consequatur amet eum maiores sequi dolorum id minus dolore. Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, aliquid cum vitae, ipsa consequatur amet eum maiores sequi dolorum id minus dolore.

## Possible Application/Business Problem

* Help inform retail investors/users possible close price, ruturn , trend of Bitcoin and other cryptocurrency
* The model can be developed to live prediction and with shorter timeframe, 4 hours, 1 hours as example
* The model can be improved, modified and used with other cryptocurrency or stocks


