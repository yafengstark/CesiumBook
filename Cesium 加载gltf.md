

```javascript
 var url ='./temp/jichuji.gltf';

      var lat= 31.97210852196748;
      var lon= 120.06212215213871;
      var position = Cesium.Cartesian3.fromDegrees(lon, lat, 0);
      var heading = Cesium.Math.toRadians(135);
      var pitch = 0;
      var roll = 0;
      var hpr = new Cesium.HeadingPitchRoll(heading, pitch, roll);
      var orientation = Cesium.Transforms.headingPitchRollQuaternion(position, hpr);

      var entity = viewer.entities.add({
        name : url,
        position : position,
        orientation : orientation,
        model : {
          uri : url,
          minimumPixelSize : 128,
          maximumScale : 1
        }
      });
      viewer.trackedEntity = entity;
      
```

minimumPixelSize	
              	可选无论缩放如何，模型的最小最小像素大小大约。

maximumScale	Number		可选模型的最大比例尺大小。 minimumPixelSize的上限。