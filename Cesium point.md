

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