<template>
  <div>
      <h1>TODOS LIST</h1>
      <div v-bind:key="todo.id" v-for="todo in todos">
          <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
      </div>
  </div>
</template>

<script>
import TodoItem from './TodoItem';
export default {
    name: "TodoList",
    components: {
        TodoItem
    },
     props: {
         todos: Array
     }
}
</script>

<style scoped>

</style>