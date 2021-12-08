<template>
  <div id="app">
    <home-content></home-content>
  </div>
</template>

<script>
import HomeContent from './components/HomeContent.vue';

export default {
  name: 'App',
  components: {
    HomeContent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}

body {
  background: #2c3e50;
}
</style>
