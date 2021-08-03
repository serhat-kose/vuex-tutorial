<template>
	<div>
		<todo v-for="(todo,index) in todos" :key="index" :todo="todo"/>
	</div>
</template>

<script>
import Todo from './Todo.vue';

export default {
  components: { Todo },
	computed: {
		todos: function() {
			return this.$store.state.todos;
		}
	}
}
</script>

<style scoped>

</style>

