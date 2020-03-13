

1.相机事件（移动开始、移动结束等等）
viewer.scene.camera.moveEnd.addEventListener(function(){

})；


2.鼠标事件（单击、移动、右键等）
var handler = new Cesium.ScreenSpaceEventHandler(viewer.scene.canvas);
handler.setInputAction(function (movement) {
   // 处理鼠标移动事件
   // 更新鼠标位置
  mousePosition = movement.endPosition;
}, Cesium.ScreenSpaceEventType.MOUSE_MOVE);

handler.setInputAction(function(click) {
  // 处理鼠标按下事件
  // 获取鼠标当前位置
  mousePosition = click.position;
 }, Cesium.ScreenSpaceEventType.LEFT_DOWN);


3.渲染事件(实时渲染，很关键的一个事件)
var renderEnd = viewer.scene.postRender.addEventListener(function(){


});