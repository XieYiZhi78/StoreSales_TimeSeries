# StoreSales_TimeSeries
此篇專案主要為針對[Kaggle上的Store Sales競賽](https://www.kaggle.com/competitions/store-sales-time-series-forecasting)進行分析與預測。

## EDA

1. 銷售時間序列圖：由圖中可得知，平均銷售額為逐年上升，且每年的1/1為銷售額最低點。
<p align="center">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/4b7e8b00-865d-4077-9b0c-38c75c133a49" width="500" />
</p>
<p align="center">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/a06e0595-94cb-410a-bdae-40422b6153b8" width="300" />
</p>

2. 銷售季節趨勢圖：從圖一和圖二可得知，在12月份時銷售額皆較高。從圖三和圖四則可看出此資料的季節性主要以周為單位，在星期六及星期日銷售額皆較高。
<p align="center">
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/89bb3c9a-60cb-4da4-be20-84e1ba6e0bd2" width="500">
</p>
<p align="center">
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/ff005b75-4a4b-4148-bad1-4663eed61d5a" width="300">
</p>

<p align="center">
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/ff1d7fcf-d1c5-4bb7-8e34-17743971d33a" width="500">
</p>
<p align="center">
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/85bec208-8210-4b8e-9b38-6675b4677bba" width="300">
</p>

3. 產品銷售額前十項
<p align="center">
<img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/220f1142-e768-40bc-b775-3b968a1628f2" width="300">
</p>

4. ACF、PACF：透過ACF和PACF圖可得知，此筆資料有拖尾現象，具有自相關性，且1,6,7有可能為自相關時間週期。
<p align="center">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/ee1da6c6-6177-42b6-b526-4ced873d0154" width="250">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/fd93ced8-d3be-476d-ad0d-0116a62f2163" width="250">
</p>

5. 銷售額與石油價格的相關性為-0.69，呈高相關性。因此在後續建模時亦需要考慮石油價格，並使用內插法填補假日的石油價格缺失值。
<p align="center">
  <img src="https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/cf6c1e6e-de00-4ba9-8c00-a821b3c4d200" width="500">
</p>

## Model

1. LSTM
最初，我們選擇使用LSTM作為預測模型，因為LSTM在處理時間序列數據方面通常都會表現得相當出色。然而，我們後來發現LSTM的output shape只能是1，或者必須與input shape相同才能成功建構模型。這導致無法將其他特徵納入考慮，從而導致預測結果不如預期。因此，我們決定改用Ridge Regression作為新的預測模型。

2. Ridge Regression

3. Custom Regression

## Result

|Model|Score|Rank|Time|
|:----:|:----:|:----:|:----:|
|LSTM|1.31851|628|47s|
|Ridge Regression|0.46074|179|40.5s|
|Custom Regression|0.42683|100|4s|

![image](https://github.com/XieYiZhi78/StoreSales_TimeSeries/assets/107387920/a324435f-c3bc-451c-a3c1-fd3d3ee25588)

