<template>
  <div id="app">
<h1>Your Todos</h1>
<h5>Completed: {{completedTodos}}</h5>
<h5>Pending: {{pendingTodos}}</h5>
<br>

<todos-list/>
<todo-form/>
  </div>
</template>

<script>
import {mapGetters} from  "vuex"
import TodosList from "./components/TodosList.vue";
import TodoForm from "./components/TodoForm.vue";

export default {
  name: 'App',
  components: {
    TodosList,
    TodoForm
  },
  computed : {

    ...mapGetters({
      completedTodos: 'completedTodos',
      pendingTodos: 'pendingTodos'
    }),

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
