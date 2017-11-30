# 讀取指定工業區內，即時汙染物指數超標範圍

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
可設定值：使用以下網頁取得指定工業區範圍幾何數據
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

[讀取指定工業區內，即時汙染物指數超標範圍](https://agisoft.niu.edu.tw/server/rest/services/EPA/WarningZone/MapServer/0/query?geometry={%22rings%22:[[[13481982.73672939,2883512.307066864],[13483339.493981488,2883512.307066864],[13483339.493981488,2882423.079413771],[13481982.73672939,2882423.079413771],[13481982.73672939,2883512.307066864]]],%22spatialReference%22:{%22wkid%22:102100}}&geometryType=esriGeometryPolygon&spatialRel=esriSpatialRelIntersects&outFields=*&returnGeometry=true&f=html)

`https://agisoft.niu.edu.tw/server/rest/services/EPA/WarningZone/MapServer/0/query?geometry={"rings":[[[13481982.73672939,2883512.307066864],[13483339.493981488,2883512.307066864],[13483339.493981488,2882423.079413771],[13481982.73672939,2882423.079413771],[13481982.73672939,2883512.307066864]]],"spatialReference":{"wkid":102100}}&geometryType=esriGeometryPolygon&spatialRel=esriSpatialRelIntersects&outFields=*&returnGeometry=true&f=pjson`