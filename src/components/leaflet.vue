<template>
  <div id="map" ref="mapElement"></div>
</template>

<script setup>
import L from "leaflet";
import { tiledMapLayer } from '@supermap/iclient-leaflet';
import { onMounted, getCurrentInstance } from "vue";
let _this;
onMounted(() => {
  //获取this实例
  const instance = getCurrentInstance();
  let { proxy } = instance;
  _this = proxy;
  console.log(L);
  // const map = new Map(_this.$refs["mapElement"]);
  // // 新建切片图层
  // // const layer = new TileLayer(
  // //   "http://121.5.190.99:8090/iserver/services/map-agscache-WaPianArcGis/rest/maps/%E7%93%A6%E7%89%87_ArcGis",
  // //   { subdomains: "1234" }
  // // );
  // let url = "http://121.5.190.99:8090/iserver/services/map-agscache-WaPianArcGis/rest/maps/%E7%93%A6%E7%89%87_ArcGis";
  // tiledMapLayer(url).addTo(map);
  // //切片图层添加到map
  // // layer.addTo(map);
  // //设置经纬度 经度在前，纬度在后 缩放10级
  // map.setView([39, 117], 10);
});
</script>

<style scoped>
/* 导入leaflet样式 */
@import "~leaflet/dist/leaflet.css";

html,
body {
  margin: 0px;
}

#map {
  width: 100%;
  height: 800px;
}
</style>
