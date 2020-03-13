```
viewer =  Cesium.Viewer('cesiumContainer');
 handler =  Cesium.ScreenSpaceEventHandler(viewer.scene.canvas);
```

//1、左键单击事件

```
handler.setInputAction(function(click){
    console.log('左键单击事件：',click.position);     
},Cesium.ScreenSpaceEventType.LEFT_CLICK);
```

//2、左键双击事件

```
handler.setInputAction(function(click){
    console.log('左键双击事件：',click.position);     
},Cesium.ScreenSpaceEventType.LEFT_DOUBLE_CLICK);
```

//3、左键按下事件

```
handler.setInputAction(function(click){
    console.log('左键按下事件：',click.position);     
},Cesium.ScreenSpaceEventType.LEFT_DOWN);
```

//4、左键弹起事件

```
handler.setInputAction(function(click){
    console.log('左键弹起事件：',click.position);     
},Cesium.ScreenSpaceEventType.LEFT_UP);
```

//5、中键单击事件

```
handler.setInputAction(function(click){
      console.log('中键单击事件：',click.position);     
 },Cesium.ScreenSpaceEventType.MIDDLE_CLICK);
```

//6、中键按下事件

```
handler.setInputAction(function(click){
      console.log('中键按下事件：',click.position);     
},Cesium.ScreenSpaceEventType.MIDDLE_DOWN);
```

//7、中键弹起事件

```
handler.setInputAction(function(click){
    console.log('中键弹起事件：',click.position);     
},Cesium.ScreenSpaceEventType.MIDDLE_UP);
```

//8、移动事件

```
handler.setInputAction(function(movement){
    console.log('移动事件：',movement.endPosition);     
},Cesium.ScreenSpaceEventType.MOUSE_MOVE);
```

//9、右键单击事件

```
handler.setInputAction(function(click){
    console.log('右键单击事件',click.position);     
},Cesium.ScreenSpaceEventType.RIGHT_CLICK);
```

//10、右键按下事件

```
handler.setInputAction(function(click){
    console.log('右键按下事件',click.position);     
},Cesium.ScreenSpaceEventType.RIGHT_DOWN);
```

//11、右键弹起事件

```
handler.setInputAction(function(click){
    console.log('右键弹起事件',click.position);     
},Cesium.ScreenSpaceEventType.RIGHT_UP);
```

//12、滚轮事件

```
handler.setInputAction(function(wheelment){
    console.log('滚轮事件：',wheelment);     
},Cesium.ScreenSpaceEventType.WHEEL);
```

//删除事件

```
handler.removeInputAction(Cesium.ScreenSpaceEventType.LEFT_CLICK);
```

