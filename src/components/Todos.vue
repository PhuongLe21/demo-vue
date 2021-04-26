<template>
  <TodoItem v-for="todo in todos" v-bind:key="todo" v-bind:todoProp="todo" />
</template>

<script>
import { ref } from 'vue'
import TodoItem from './TodoItem'

const todoArray = [
  {
    id: 1,
    title: 'Thing 11',
    completed: true
  },
  {
    id: 2,
    title: 'Thing 22',
    completed: false
  },
  {
    id: 3,
    title: 'Thing 33',
    completed: false
  }
]

export default {
  name: 'Todos',

  setup() {
    const todos = ref(todoArray)
    return {
      todos
    }
  },
  components: {
    TodoItem
  }
}
</script>

<style>

</style>