
var terrainProvider = new Cesium.CesiumTerrainProvider({
            url: "http://localhost:8080/forthree"
        });
        var imageryProvider = new Cesium.UrlTemplateImageryProvider({
            url: "http://{s}.tianditu.com/DataServer?T=img_w&x={x}&y={y}&l={z}",
            credit: new Cesium.Credit("天地图全球影像服务"),
            subdomains: ["t0", "t1", "t2", "t3", "t4", "t5", "t6", "t7"],
            tilingScheme: new Cesium.WebMercatorTilingScheme(),
            maxiumLevel: 18
        });
    
    
        var viewer = new Cesium.Viewer("cesiumContainer", {
            terrainProvider: terrainProvider,
            imageryProvider: imageryProvider,
            baseLayerPicker: false
        });
————————————————
版权声明：本文为CSDN博主「wjiafengw」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/wjiafengw/article/details/84849420


