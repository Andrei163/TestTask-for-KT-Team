<template>
	<div class="wrapper">
		<h1>Задачи</h1>
		<createtask></createtask>

		<todo></todo>
	</div>
</template>

<script>
import createtask from "./CreateTask";
import todo from "./Todo";
export default {
	components: {
		createtask,
		todo
	}
};
</script>

<style scoped>
h1 {
	text-align: left;
}

/* .wrapper {
	width: 960px;
	padding: 25px;
	background-color: rgb(224, 227, 230);
}

@media (max-width: 1200px) {
.wrapper {
	width: 800px;
	
} */
/* } */
</style>
