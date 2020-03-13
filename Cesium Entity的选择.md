https://www.jianshu.com/p/c641d0e5b7a1



esium为我们提供了scene.pick接口，如下代码实现坐标左键单击实现对象的拾取：



```jsx
      viewer.entities.add({
            id:'obj_id_110',
            position:Cesium.Cartesian3.fromDegrees(103.0, 40.0),
            name:'Red ellipse on surface with outline',
            ellipse:{
                semiMinorAxis:250000.0,
                semiMajorAxis:400000.0,
                height:200000.0,
                extrudedHeight:400000.0,
                fill:true,
                material:Cesium.Color.RED.withAlpha(0.5),
                outline:true, //必须设置height，否则ouline无法显示
                outlineColor:Cesium.Color.BLUE.withAlpha(0.5),
                outlineWidth:10.0//windows系统下不能设置固定为1
            }
        });
 
        varhandler = new Cesium.ScreenSpaceEventHandler(viewer.scene.canvas);
        handler.setInputAction(function(movement) {
            varpick = viewer.scene.pick(movement.position);
            if(Cesium.defined(pick) && (pick.id.id === 'obj_id_110')) {
                alert('picked!');
            }
        },Cesium.ScreenSpaceEventType.LEFT_CLICK);
```