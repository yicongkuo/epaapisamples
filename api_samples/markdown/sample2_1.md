# 讀取時間區段內，汙染物指數超標範圍歷史數據

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

 - 如果想要查詢`2017/11/28 早上00:00` ~ `2017/11/30 早上23:59`
   之間的所有資料，而且時間欄位名稱為cTime，則使用以下指令：
	
   ```
     where = cTime between timestamp '2017-11-28 00:00:00' AND timestamp '2017-11-30 23:59:59'
   ```

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

[讀取時間區段內，汙染物指數超標範圍歷史數據](https://agisoft.niu.edu.tw/server/rest/services/EPA/WarningZone/MapServer/1/query?f=html&where=cTime%20between%20timestamp%20%272017-11-28%2000:00:00%27%20AND%20timestamp%20%272017-11-30%2023:59:59%27&returnGeometry=true&outFields=*)

`https://agisoft.niu.edu.tw/server/rest/services/EPA/WarningZone/MapServer/1/query?f=json&where=cTime between timestamp '2017-11-28 00:00:00' AND timestamp '2017-11-30 23:59:59'&returnGeometry=true&outFields=*`