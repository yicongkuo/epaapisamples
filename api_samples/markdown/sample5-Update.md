# 查詢指定點位PM 2.5濃度值

## url 

https://<imageservice-url>/identify

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

`returnGeometry`

```
功能描述：是否回傳經緯度或幾何數據
可設定值：true | false
```

## api呼叫範例

[查詢指定點位PM 2.5濃度值](https://yicong.igis.com.tw/server/rest/services/idw/Idw_raw/ImageServer/identify?geometry={"x":13482612.147884196,"y":2882327.533128412,"spatialReference":{"wkid":102100}}&geometryType=esriGeometryPoint&returnGeometry=true&f=html)

`https://yicong.igis.com.tw/server/rest/services/idw/Idw_raw/ImageServer/identify?geometry={"x":13482612.147884196,"y":2882327.533128412,"spatialReference":{"wkid":102100}}&geometryType=esriGeometryPoint&returnGeometry=true&f=json`