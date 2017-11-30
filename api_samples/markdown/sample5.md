# 查詢指定點位即時的PM 2.5濃度值

## url 

https:// <mapservice-url>/identify

## api 參數說明

`geometry`

```
功能描述：設定指定位置座標
可設定值：{x:<x>, y:<y>}
案例說明：{x:121.124003, y:25.063273}
```
[取得指定位置經緯度的網頁](http://www.arcgis.com/home/webmap/viewer.html)

`geometryType`

```
功能描述：`gemoetry`參數的幾何類型
可設定值：esriGeometryPoint
```

`sr`

```
功能描述：輸入與輸出點位的座標系統
可設定值：座標系統的epsg代碼，如 4326 (wgs84) | 3826 (TWD97TM2) | 3828(TWD67TM2)
```

`layers`

```
功能描述：設定那幾層的圖層資料要回傳
可設定值：top | visible | all
```

`tolerance`

```
功能描述： 螢幕上，指定點位與實際幾何點位的容許誤差值
可設定值： 必須是整數值，例如：2
```

`mapExtent`

```
功能描述：想要回傳的地圖範圍四腳座標，依據sr參數指定的座標系統進行設定
可設定值：<xmin>, <ymin>, <xmax>, <ymax>

案例說明：例如sr是4326(wgs84)，我想回傳整個世界地圖的範圍，則此值設定成 -180,-180,180,180
```

`imageDisplay`

```
功能描述：地圖圖片在螢幕上顯示的參數
可設定值：<width>, <height>, <dpi>
案例說明：600,550,96
```

`f`

```
功能描述：設定回傳值格式
可設定值：html | json | geojson
```

## api呼叫範例

[查詢指定點位PM 2.5濃度值](https://agisoft.niu.edu.tw/server/rest/services/EPA/IDWResults/MapServer/identify?geometry={x:121.124003,+y:25.063273}&geometryType=esriGeometryPoint&sr=4326&layers=all&layerDefs=&time=&layerTimeOptions=&tolerance=2&mapExtent=-180,-180,180,180&imageDisplay=600,550,96&returnGeometry=true&maxAllowableOffset=&geometryPrecision=&dynamicLayers=&returnZ=false&returnM=false&gdbVersion=&returnUnformattedValues=false&returnFieldName=false&datumTransformations=&layerParameterValues=&mapRangeValues=&layerRangeValues=&f=html)

`https://agisoft.niu.edu.tw/server/rest/services/EPA/IDWResults/MapServer/identify?geometry={x:121.124003,+y:25.063273}&geometryType=esriGeometryPoint&sr=4326&layers=all&layerDefs=&time=&layerTimeOptions=&tolerance=2&mapExtent=-180,-180,180,180&imageDisplay=600,550,96&returnGeometry=true&maxAllowableOffset=&geometryPrecision=&dynamicLayers=&returnZ=false&returnM=false&gdbVersion=&returnUnformattedValues=false&returnFieldName=false&datumTransformations=&layerParameterValues=&mapRangeValues=&layerRangeValues=&f=pjson`