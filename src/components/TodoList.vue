<template>
  <div>
    <ul>
      <TodoItem
        v-for="todo of todos"
        v-bind:todo="todo"
        :key="todo"
        v-on:remove-todo="removeTodo"
        v-on:change-completed="changeCompleted"
      />
    </ul>
  </div>
</template>

<script>
import TodoItem from "@/components/TodoItem";
export default {
  props: ["todos"],
  components: {
    TodoItem,
  },
  methods: {
    removeTodo(id) {
      console.log(id);
    },
    changeCompleted(todo) {
      console.log(todo); // 24:13
    },
  },
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
}
</style>
