





```css
viewer.entities.add({
       position : Cesium.Cartesian3.fromDegrees(-75.59777, 40.03883),
       point : {
           pixelSize : 10,
           color : Cesium.Color.YELLOW
       }
   });
```

viewer.entities entity的集合



填充，材质

```css
viewer.entities.add({
        position:Cesium.Cartesian3.fromDegrees(103.0, 40.0),
        name:'Red ellipse on surface with outline',
        ellipse:{
            semiMinorAxis:300000.0,
            semiMajorAxis:300000.0,
            height:200000.0,
              // 填充
            fill:true,
              // 材质
            material:Cesium.Color.RED.withAlpha(0.5),
            outline:true, //必须设置height，否则ouline无法显示
            outlineColor:Cesium.Color.BLUE.withAlpha(0.5),
            outlineWidth:10.0//不能设置，固定为1
        }
    });
```



贴图



垂直拉伸





## entity管理



增



删



改



查



```jsx
Cesium.EntityCollection.collectionChangedEventCallback(collection,added, removed, changed)
add(entity) → Entity
computeAvailability() → TimeInterval
contains(entity) → Boolean
getById(id) → Entity
getOrCreateEntity(id) → Entity
remove(entity) → Boolean
removeAll()
removeById(id) → Boolean
resumeEvents()
suspendEvents()
```





