<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/download.jpg">
    <HelloWorld msg=""/>
    <div>
</div>
    <applol/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import applol from './components/applol.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    applol
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
