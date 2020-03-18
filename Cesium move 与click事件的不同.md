
event.position
```javascript
var handler = new Cesium.ScreenSpaceEventHandler(viewer.canvas);
      handler.setInputAction(function (event) {
        var pick = viewer.scene.pick(event.position);  //获取的pick对象
        var pickedEntity = Cesium.defined(pick) ? pick.id : undefined; //pick.id即为entity

        //
        console.log('选取的模型');
        console.log(pickedEntity)
      }, Cesium.ScreenSpaceEventType.LEFT_CLICK);
      
```


movement.endPosition
```javascript
var handler = new Cesium.ScreenSpaceEventHandler(viewer.canvas);
      handler.setInputAction(function (movement) {
        var pick = viewer.scene.pick(movement.endPosition);  //获取的pick对象
        var pickedEntity = Cesium.defined(pick) ? pick.id : undefined; //pick.id即为entity

        //
        console.log('选取的模型');
        console.log(pickedEntity)
      }, Cesium.ScreenSpaceEventType.MOUSE_MOVE);
```