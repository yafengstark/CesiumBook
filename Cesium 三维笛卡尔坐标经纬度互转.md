https://www.cnblogs.com/aizai846/p/11846929.html

## （3D笛卡尔坐标）转经纬度坐标

```javascript
console.log('地表坐标')
 // 笛卡尔三维坐标C3
console.log(position)

// 
var ellipsoid = viewer.scene.globe.ellipsoid;
var cartographic = ellipsoid.cartesianToCartographic(position);
          
var lat = Cesium.Math.toDegrees(cartographic.latitude);
var lng = Cesium.Math.toDegrees(cartographic.longitude);
console.log('lat: ' + lat)
console.log('lon:' + lng);
```

## 经纬度转3D笛卡尔坐标
```javascript
 var longitude = Cesium.Math.toRadians(point.lon); //其中 longitude1为角度
          var latitude = Cesium.Math.toRadians(point.lat); //其中 latitude1为角度
     var position = Cesium.Cartesian3.fromDegrees(longitude, latitude, 0);//其中，高度默认值为0，可以不用填写；longitude和latitude为角度
```
