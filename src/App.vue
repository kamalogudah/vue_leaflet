<template>
  <div id="app">
     <div id="app" class="container">
      <div class="row">
        <div class="col-md-9">
          <Map></Map>
        </div>
        <div class="col-md-3">
          <!-- The layer checkboxes go here -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Map from './components/Map.vue';

export default {
  name: 'app',
  components: {
    Map,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
