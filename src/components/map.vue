<template>
  <div class="hello">
    <div id="map"></div>
  </div>
</template>
<script>
import "ol/ol.css";
import { Map, View } from "ol";
import TileLayer from "ol/layer/Tile";
import OSM from "ol/source/OSM";
export default {
  data() {
    return {};
  },
  mounted() {
    const map = new Map({
      target: "map",
      layers: [
        new TileLayer({
          source: new OSM()
        })
      ],
      view: new View({
        center: [-0.12755, 51.507222],
        zoom: 5
      })
    });
  }
};
</script>
<style lang="stylus" scoped>
.hello
  width 100%
  height 100%
#map
  width 100%
  height 100%
</style>

