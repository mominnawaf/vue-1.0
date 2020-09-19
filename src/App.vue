<template>
  <div id="app">
    <Todo v-bind:todos="todos"/>
  </div>
</template>

<script>
import Todo from "./components/Todo"
export default {
  name: 'App',
  components:{
    Todo
  },
  data(){
    return{
      todos:[
        {
          id:1,
          title:"Todo One",
          isDone: true
        },
        {
          id:2,
          title:"Todo Two",
          isDone: false
        },
        {
          id:3,
          title:"Todo Three",
          isDone: true
        }
      ]
    }
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
