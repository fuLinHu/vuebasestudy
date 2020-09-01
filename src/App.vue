<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
	<!-- <Soltparent /> -->
	<ComponetA />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import Soltparent from "./components/solt/Soltparent.vue"
import ComponetA from "./components/keepalive/ComponetA.vue"

export default {
  name: 'app',
  components: {
	ComponetA
  }
}
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
