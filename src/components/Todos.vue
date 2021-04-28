<template>
  <TodoItem
    v-for="todo in todos"
    v-bind:key="todo"
    v-bind:todoProp="todo"
    v-on:make-complete="makeComplete"
    v-on:delete-item="deleteItem"
  />
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

    const makeComplete = (id) => {
      todos.value = todos.value.map((td) => {
        if (td.id === id) {
          td.completed = !td.completed
        }

        return td
      })
    }
    const deleteItem = (id) => {
      todos.value = todos.value.filter(td => td.id !== id)
    }
    return {
      todos,
      makeComplete,
      deleteItem
    }
  },
  components: {
    TodoItem
  }
}
</script>

<style>

</style>