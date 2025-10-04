<template>
  <div id="app">
    <Home></Home>
  </div>
</template>

<script>
import Home from './views/home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>


<!-- 组合式 API（改法）： -->
<!-- <script setup>
import Home from './views/home.vue'
</script> -->

<style scoped></style>