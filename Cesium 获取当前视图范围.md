

Cesium 获取当前视图范围

https://www.cnblogs.com/tracyjfly/p/5089466.html

先获取屏幕二维坐标，再获取地图坐标

```
var pt1 = new Cesium.Cartesian2(0,0);
var pt2= new Cesium.Cartesian2(500,500);
 
var pick1= viewer.scene.globe.pick(viewer.camera.getPickRay(pt1), viewer.scene);
var pick2= viewer.scene.globe.pick(viewer.camera.getPickRay(pt2), viewer.scene);
 
//将三维坐标转成地理坐标
var geoPt1= viewer.scene.globe.ellipsoid.cartesianToCartographic(pick1);
var geoPt2= viewer.scene.globe.ellipsoid.cartesianToCartographic(pick2);
 
//地理坐标转换为经纬度坐标
var point1=[geoPt1.longitude / Math.PI * 180,geoPt1.latitude / Math.PI * 180];           
var point2=[geoPt2.longitude / Math.PI * 180,geoPt2.latitude / Math.PI * 180];   
```

## 如何获取屏幕坐标
http://caibaojian.com/getelementposition.html


