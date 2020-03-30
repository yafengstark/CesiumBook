https://www.cnblogs.com/huqi-code/archive/2018/01/29/8378238.html



```javascript
//方法一，构造时赋材质
var entity = viewer.entities.add({
  position: Cesium.Cartesian3.fromDegrees(-103.0, 40.0),
  ellipse : {
    semiMinorAxis : 250000.0,
    semiMajorAxis : 400000.0,
    material : Cesium.Color.BLUE.withAlpha(0.5)//可设置不同的MaterialProperty
  }
});

//方法二，构造后赋材质
var ellipse = entity.ellipse;
ellipse.material = Cesium.Color.RED;

```