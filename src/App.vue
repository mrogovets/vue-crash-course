<template>
  <div id="app">
    <h1>Todo Application</h1>
    <hr />
    <TodoList v-bind:todos="todos" />
  </div>
</template>

<script>
import TodoList from "@/components/TodoList";
export default {
  name: "App",
  data() {
    return {
      todos: [
        { id: 1, title: "Create Awsome App", completed: false },
        { id: 2, title: "Drink Coffee", completed: false },
        { id: 3, title: "Have Lunch", completed: false },
      ],
    };
  },
  components: {
    TodoList,
  },
};
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
