

## 材质 
材质（Fabric）

https://www.jianshu.com/p/f8fee864379a

Fabric 是Cesium中基于JSON格式来描述materials的机制。材质描述多边形、折线、椭球等对象的外观特征。
材质可以简单的是覆盖一张图片，或者是条纹或者棋盘图案。

```$xslt
polygon.material = Material.fromType('Color');
```

```$xslt
polygon.material = new Cesium.Material({
  fabric : {
    type : 'Color'
  }
});
```