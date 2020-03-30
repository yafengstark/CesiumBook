

worldPosition = 三维笛卡尔坐标
```javascript
 var point = viewer.entities.add({
            position: worldPosition,
            point: {
              color: Cesium.Color.RED,
              pixelSize: 5,
//                heightReference: Cesium.HeightReference.CLAMP_TO_GROUND
            }
          });
```


经纬度定义点，
```
 viewer.entities.add({
       position : Cesium.Cartesian3.fromDegrees(-75.59777, 40.03883),
       point : {
           pixelSize : 10,
           color : Cesium.Color.YELLOW
       }
   });
   ```