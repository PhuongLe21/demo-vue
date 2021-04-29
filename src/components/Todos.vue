<template>
  <AddTodo @add-item="addItem" />
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
import AddTodo from './AddTodo'

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

    const addItem = (title) => {
      console.log('title parent', title)
      const newItem = {
        id: todos.value.length + 1,
        title,
        completed: false
      }

      todos.value.push(newItem)
    }
    return {
      todos,
      makeComplete,
      deleteItem,
      addItem
    }
  },
  components: {
    TodoItem,
    AddTodo
  }
}
</script>

<style>

</style>