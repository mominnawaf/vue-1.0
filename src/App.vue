<template>
  <div id="app">
    {{name}}
  </div>
</template>

<script>
import Vue from 'vue';
new Vue({
  el:"#app",
  data :{
    name:"Nawaf"
  }

});
export default {
  name: 'App'
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
