<template>
  <div class="todo-item" v-bind:class="{'is-completed':todo.completed}">
      <input type="checkbox" v-on:change="markComplete">
      {{todo.title}}
      <button @click="$emit('del-todo',todo.id)" class="del">X</button>
  </div>
</template>

<script>
export default {
    name: 'TodoItem',
    props:[
        'todo'
    ],
    methods:{
        markComplete(){
            this.todo.completed=! this.todo.completed;
        }
    }

}
</script>

<style  scoped>
.is-completed{
    text-decoration: line-through;
}
.todo-item {
    background: #f4f4f4;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
  }
  .del {
    background: #ff0000;
    color: #fff;
    border: none;
    padding: 5px 9px;
    border-radius: 50%;
    cursor: pointer;
    cursor: pointer;
    float: right;
  }
</style>