<template>
  <div id="map" class="map"></div>
</template>

<script>
export default {
  name: 'Map',
  data() {
    return {
      map: null,
      tileLayer: null,
      layers: [
    {
      id: 0,
      name: 'Restaurants',
      active: false,
      features: [],
    },
  ],
    };
  },
  mounted() {
    this.initMap();
    this.initLayers();
  },
  methods: {
    initMap() {
      this.map = L.map('map').setView([38.63, -90.23], 12);
      this.tileLayer = L.tileLayer(
        'https://cartodb-basemaps-{s}.global.ssl.fastly.net/rastertiles/voyager/{z}/{x}/{y}.png',
        {
          maxZoom: 18,
          attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>, &copy; <a href="https://carto.com/attribution">CARTO</a>',
        },
      );
      this.tileLayer.addTo(this.map);
    },
    initLayers() {},
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.map { height: 600px; }
</style>
