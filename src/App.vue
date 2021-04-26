<template>
  <Header />
  <Todos />
</template>

<script>
import Header from './components/Header'
import Todos from './components/Todos'

export default {
  name: "App",
  components: {
    Header,
    Todos
  }
}
</script>

<style>

</style>