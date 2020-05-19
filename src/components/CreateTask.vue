<template>
	<form class="todo-form" @submit.prevent="addTodo()">
		<input
			v-model="newTodo"
			class="newtask"
			type="text"
			id="newtask"
			placeholder="Enter a title for this card"
			required
		/>
		<button class="btn" type="submit">Add Card</button>
	</form>
</template>

<script>
export default {
	data() {
		return {
			newTodo: ""
		};
	},
	methods: {
		addTodo() {
			const task = {
				title: this.newTodo
			};
			this.$store.dispatch("createTask", task);
			this.newTodo = "";
		}
	}
};
</script>

<style scoped>
.todo-form {
	display: flex;
	flex-direction: column;
}

.newtask {
	width: 100%;
	height: 30px;
	margin-bottom: 10px;
}

.btn {
	color: white;
	font-weight: bold;
	font-size: 18px;
	border-radius: 7px;
	width: 120px;
	height: 40px;
	background-color: rgb(97, 202, 17);
}
</style>
