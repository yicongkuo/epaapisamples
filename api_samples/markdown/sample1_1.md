# 讀取時間區段內感測器的數據

## url 

https://<featurelayer-url>/<featureId>/query

## api 參數說明

`f`

```
功能描述：設定回傳值格式
可設定值：html | json | geojson
```

`where`

```
功能描述：設定查詢條件
可設定值：任何合法的SQL where子句
```

**範例說明**

 - 圖層屬性中，有一個欄位名稱為`deviceId`，使用`字串`方式記錄
   感測器的編號。如果想要查詢編號1875819825感測器的所有數據時，
   可使用以下指令：
	
   ```
     where = deviceId='1875296284'
   ```
 - 想要查詢`2017/11/28 早上00:00` ~ `2017/11/30 晚上23:59`
   之間的所有資料，可使用以下指令：
	
   ```
     where = time BETWEEN timestamp '2017-11-28 00:00:00' AND timestamp '2017-11-30 23:59:59'

`outFields`

```
功能描述：設定要回傳的欄位資料，所有欄位都要回傳可以使用米字號*
可設定值：欄位名稱1, 欄位名稱2,... | *
```

`returnGeometry`

```
功能描述：是否回傳經緯度或幾何數據
可設定值：true | false
```

## api呼叫範例

[讀取時間區段內即時感測器的數據](https://demo99.igis.com.tw/server/rest/services/Hosted/EPA-MQTT-BigStore-feature/FeatureServer/0/query?f=html&where=%20time%20BETWEEN%20timestamp%20%272017-11-28%2000:00:00%27%20AND%20timestamp%20%272017-11-30%2023:59:59%27%20AND%20deviceId%20=%20%271875296284%27&returnGeometry=true&outFields=*)

`https://demo99.igis.com.tw/server/rest/services/Hosted/EPA-MQTT-BigStore-feature/FeatureServer/0?f=pjson&where=
time BETWEEN timestamp '2017-11-28 00:00:00' AND timestamp '2017-11-30 23:59:59' AND deviceId = '1875296284'&returnGeometry=true&outFields=*`