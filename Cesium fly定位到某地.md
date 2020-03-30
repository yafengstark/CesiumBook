## fly 飞行定位

```
viewer.camera.flyTo({
                    destination : Cesium.Cartesian3.fromDegrees(lon, lat, height)
                });
```





```
viewer.scene.camera.flyTo({
                destination: Cesium.Cartesian3.fromDegrees(lon, lat, 10000),  //定位坐标点，建议使用谷歌地球坐标位置无偏差
                duration:5   //定位的时间间隔
            });
```



## 直接定位

直接定位，就是获取当前用户输入的经纬度、海拔高度进行直接定位。定位是没有动画效果直接跳转到输入的坐标位置。主要调用的方法是：viewer.camera.setView方法，查询API可以知道setView方法的参数和效果。



```
 viewer.camera.setView({
             destination: Cesium.Cartesian3.fromDegrees(lon, lat , 10000)  //定位坐标点，建议使用谷歌地球坐标位置无偏差
         });
```





作者：宥MySunshine
链接：https://www.jianshu.com/p/43189c403f0f
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。