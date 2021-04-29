<template>
  <p :class="['todo-item', todoProp.completed && 'is-completed']">
    <input type="checkbox" :checked="todoProp.completed" v-on:click="markItemComplete"/>
    {{ todoProp.title }}
    <button class="del-btn" v-on:click="deleteItem">Delete</button>
  </p>
</template>

<script>
export default {
  name: 'TodoItem',
  props: ['todoProp'],
  setup(prop, context) {
    const markItemComplete = () => {
      context.emit('make-complete', prop.todoProp.id)
    }

    const deleteItem = () => {
      context.emit('delete-item', prop.todoProp.id)
    }

    return {
      markItemComplete,
      deleteItem
    }
  }
}
</script>

<style>
.todo-item {
  background: #eee;
  border-bottom: 1px solid #ddd;
  padding: 10px;
  margin: 0
}

.is-completed {
  text-decoration: line-through;
}

.del-btn {
  background: red;
  float: right;
  border: none;
  color: #fff;
  padding: 5px;
  cursor: pointer;
}

</style>