<template>
<div>
    <h2>Todos</h2>
    <div v-bind:key="todo.id" v-for="todo in todos" >
      <TodoItem v-bind:todo="todo"></TodoItem>
  </div>
</div>
  
</template>

<script>
import TodoItem from "./TodoItem"
export default {
    name:'Todo',
    components:{
      TodoItem
    },
    props:['todos']

}
</script>

<style>

</style>