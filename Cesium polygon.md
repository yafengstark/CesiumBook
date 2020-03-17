
```$xslt
this.buildingList[0].shapePoints = [
          new Cesium.Cartesian3(-2712744.248004503, 4685452.391486641, 3360369.4982985025),
          new Cesium.Cartesian3(-2712744.248004503, 4685452.391486641, 3360369.4982985025),
          new Cesium.Cartesian3(-2712859.07803108, 4686350.763763141, 3359032.793525848),
          new Cesium.Cartesian3(-2713888.490867039, 4685991.368338146, 3358704.835097423),
          new Cesium.Cartesian3(-2713698.9869609773, 4685099.057609064, 3360093.120654003)
        ];
```


```$xslt
 entity: new Cesium.Entity({
                polygon: {
                  hierarchy: that.activeShapePoints,
                  material: new Cesium.ColorMaterialProperty(Cesium.Color.BLUE.withAlpha(0.7))
                }
              })
```