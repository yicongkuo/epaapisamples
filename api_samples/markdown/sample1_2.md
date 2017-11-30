# 讀取指定範圍內的即時感測器數據

## url 

https://<featurelayer-url>/<featureId>/query

## api 參數說明

`f`

```
功能描述：設定回傳值格式
可設定值：html | json | geojson
```

`geometry`

```
功能描述：設定指定範圍的幾何數據
可設定值：使用以下網頁取得指定範圍幾何數據
```
[取得指定範圍幾何數據網頁](https://yicongkuo.github.io/epa/apps/GetGeometryParams/)

`geometryType`

```
功能描述：`gemoetry`參數的幾何類型
可設定值：esriGeometryPolygon
```

`spatialRel`

```
功能描述：幾何圖形的空間關係
可設定值：esriSpatialRelIntersects
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

[讀取指定範圍內的即時感測器數據](https://demo99.igis.com.tw/server/rest/services/Hosted/EPA-MQTT-Stream-feature/FeatureServer/0/query?f=html&geometry={"rings":[[[13482171.440642975,2883345.1010674853],[13482911.924354507,2883345.1010674853],[13482911.924354507,2882757.4914125274],[13482171.440642975,2882757.4914125274],[13482171.440642975,2883345.1010674853]]],"spatialReference":{"wkid":102100}}&geometryType=esriGeometryPolygon&spatialRel=esriSpatialRelIntersects&outFields=*&returnGeometry=true)

`https://demo99.igis.com.tw/server/rest/services/Hosted/EPA-MQTT-Stream-feature/FeatureServer/0/query?f=json&geometry={"rings":[[[13482171.440642975,2883345.1010674853],[13482911.924354507,2883345.1010674853],[13482911.924354507,2882757.4914125274],[13482171.440642975,2882757.4914125274],[13482171.440642975,2883345.1010674853]]],"spatialReference":{"wkid":102100}}&geometryType=esriGeometryPolygon&spatialRel=esriSpatialRelIntersects&outFields=*&returnGeometry=true`