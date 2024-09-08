<script setup>
import NgwMap from '@nextgis/ngw-leaflet';

const webMapName = 'webmap';
const qmsBaseLayerName = 'qmsbasemap';

NgwMap.create({
  baseUrl: "/api",
  target: "map",
  osm: true,
  minZoom: 1,
  qmsId: [448, qmsBaseLayerName],
  resources: [ { resource: 6245, id: webMapName, useBasemap: false, fit: true }, ],
})
</script>

<template>
  <div id="wrapper">
    <div id="layers"></div>
    <div id="map"></div>
  </div>
</template>