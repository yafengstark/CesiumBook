

```
loactionTectEntity = viewer.entities.add({
            name: 'locationRectangle',
            id: 'locationRectangle',
            rectangle: {
                coordinates: rect,
                material: Cesium.Color.GREEN.withAlpha(1.0),
                height: 10.0,
                outline: false
            }
        });
        var flyPromise = viewer.flyTo(loactionTectEntity, {
            duration: 5,
            offset: new Cesium.HeadingPitchRange(0.0, Cesium.Math.toRadians(-20.0))
        });

        flyPromise.then(function () {
            setPitch();
        });

        function setPitch() {
            var center = Cesium.Rectangle.center(rect);
            var car = Cesium.Cartesian3.fromRadians(center.longitude, center.latitude);
            var range = Cesium.Cartesian3.distance(car, viewer.camera.position) * Math.cos(20);
            viewer.zoomTo(loactionTectEntity, new Cesium.HeadingPitchRange(0.0, Cesium.Math.toRadians(-20.0), range));
        }


```