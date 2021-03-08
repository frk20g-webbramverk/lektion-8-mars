<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <AddName></AddName>
  </div>
</template>

<script>
import AddName from './components/AddName.vue'

export default {
  name: 'App',
  components: {
    AddName
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
