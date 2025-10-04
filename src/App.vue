<template>
  <div id="app">
    <BackgroundEffect />
    <Home></Home>
  </div>
</template>

<script>
import Home from './views/home.vue';
import BackgroundEffect from './components/BackgroundEffect.vue';

export default {
  name: 'App',
  components: {
    Home,
    BackgroundEffect
  }
}
</script>


<!-- 组合式 API（改法）： -->
<!-- <script setup>
import Home from './views/home.vue'
import BackgroundEffect from './components/BackgroundEffect.vue';
</script> -->

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #000;
  color: #fff;
  font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.app-container {
  position: relative;
  min-height: 100vh;
  width: 100%;
  overflow-x: hidden;
  background-color: #000;
}
</style>