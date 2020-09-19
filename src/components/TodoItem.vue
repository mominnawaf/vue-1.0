<template>
  <div v-bind:class="{'is-completed':todo.isDone}">
      <input type="checkbox" v-on:change="markComplete">
      {{todo.title}}
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
            this.todo.isDone=! this.todo.isDone;
        }
    }

}
</script>

<style  scoped>
.is-completed{
    text-decoration: line-through;
}
</style>