<template>
  <input type="text" v-model="title" />
  <button @click="handleAddItem">Add</button>
</template>

<script>
import { ref } from 'vue'
 
export default {
	name: 'AddTodo',
	setup(prop, context) {
		const title = ref('')
		const handleAddItem = () => {
			console.log('title', title.value, context)
			context.emit('add-item', title.value)
		}

		return {
			title,
			handleAddItem
		}
	}
}
</script>

<style>

</style>