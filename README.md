# StoreSales_TimeSeries
此篇專案主要為針對[Kaggle上的Store Sales競賽](https://www.kaggle.com/competitions/store-sales-time-series-forecasting)進行分析與預測。

## EDA

1.銷售時間序列圖
<p float="left">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/4b7e8b00-865d-4077-9b0c-38c75c133a49" width="400" />
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/a06e0595-94cb-410a-bdae-40422b6153b8" width="150" />
</p>
2.銷售季節趨勢圖——月份、日期

3.產品銷售額前十項

4.ACF、PACF

## Model

1.LSTM

2.CustomRegressor

## Result

|Model|Score|Rank|Time|
|:----:|:----:|:----:|:----:|
|LSTM|1.31851|628|47s|
|CustomRegressor|0.42683|100|4s|

![image](https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/a324435f-c3bc-451c-a3c1-fd3d3ee25588)

