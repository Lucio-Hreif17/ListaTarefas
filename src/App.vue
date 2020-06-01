<template>
  <div id="app">
    <TodoForm @adicionar="novaTarefa($event)"/>
    <TodoList :tarefas="tarefas"/>
  </div>
</template>

<script>
import TodoForm from "./components/TodoForm.vue"
import TodoList from "./components/TodoList.vue"

export default {
  name: "App",
  components: {
    TodoForm,
    TodoList
  }, data: function() {
    return {
      tarefas: []
    }
  },
  methods: {
    novaTarefa: function(event) {
      this.tarefas.push({nometarefa: event.texto});
    }
  }
}
</script>

<style>
#app {
  margin: 2px solid black;
  width: 1500px;
  height: 150px;
}
</style>