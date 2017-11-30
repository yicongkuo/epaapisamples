# 查詢指定位置的冷熱區特徵

## url 

https:// <featurelayer-url>/<featureId>/query

## api 參數說明

`f`

```
功能描述：設定回傳值格式
可設定值：html | json | geojson
```

`geometry`

```
功能描述：設定指定位置的幾何數據
可設定值：使用以下網頁取得指定範圍幾何數據
```
[取得指定範圍幾何數據網頁](https://yicongkuo.github.io/epa/apps/GetGeometryParams/)

`geometryType`

```
功能描述：`gemoetry`參數的幾何類型
可設定值：esriGeometryPoint
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

[查詢指定位置的冷熱區特徵](https://services7.arcgis.com/tVmMUEViFfyHBZvj/ArcGIS/rest/services/epa_stc_0728_WFL1/FeatureServer/2/query?geometry=%7B%22x%22%3A13482435.300111601%2C%22y%22%3A2883731.5402622083%2C%22spatialReference%22%3A%7B%22wkid%22%3A102100%7D%7D&geometryType=esriGeometryPoint&spatialRel=esriSpatialRelIntersects&outFields=PATTERN&returnGeometry=true&f=html)

`https://services7.arcgis.com/tVmMUEViFfyHBZvj/ArcGIS/rest/services/epa_stc_0728_WFL1/FeatureServer/2/query?geometry=%7B%22x%22%3A13482435.300111601%2C%22y%22%3A2883731.5402622083%2C%22spatialReference%22%3A%7B%22wkid%22%3A102100%7D%7D&geometryType=esriGeometryPoint&spatialRel=esriSpatialRelIntersects&outFields=PATTERN&returnGeometry=true&f=json`