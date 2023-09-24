# StoreSales_TimeSeries
此篇專案主要為針對[Kaggle上的Store Sales競賽](https://www.kaggle.com/competitions/store-sales-time-series-forecasting)進行分析與預測。

## EDA

1. 銷售時間序列圖
<p align="center">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/4b7e8b00-865d-4077-9b0c-38c75c133a49" width="500" />
</p>
<p align="center">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/a06e0595-94cb-410a-bdae-40422b6153b8" width="300" />
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/db671c60-efda-4cfa-ab6d-deac6ac18528" width="100" />
</p>

2. 銷售季節趨勢圖——月份、日期
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/89bb3c9a-60cb-4da4-be20-84e1ba6e0bd2" width="500">
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/ff005b75-4a4b-4148-bad1-4663eed61d5a" width="300">

<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/ff1d7fcf-d1c5-4bb7-8e34-17743971d33a" width="500">
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/85bec208-8210-4b8e-9b38-6675b4677bba" width="300">

3. 產品銷售額前十項
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/220f1142-e768-40bc-b775-3b968a1628f2" width="300">

4. ACF、PACF
<p align="center">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/ee1da6c6-6177-42b6-b526-4ced873d0154" width="250">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/fd93ced8-d3be-476d-ad0d-0116a62f2163" width="250">
</p>

## Model

1. LSTM

2. CustomRegressor

## Result

|Model|Score|Rank|Time|
|:----:|:----:|:----:|:----:|
|LSTM|1.31851|628|47s|
|CustomRegressor|0.42683|100|4s|

![image](https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/a324435f-c3bc-451c-a3c1-fd3d3ee25588)

