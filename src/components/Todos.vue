<template>
  <p v-for="todo in todos" v-bind:key="todo">{{ todo }}</p>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'Todos',

  setup() {
    const todos = ref(['Thing 1', 'Thing 2', 'Thing 3'])
    return {
      todos
    }
  }
}
</script>

<style>

</style>