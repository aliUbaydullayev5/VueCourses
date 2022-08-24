<!-- @format -->
<!-- 
	v-bind:value="inputValueTitle"
				@input="inputValueTitle = $event.target.value" -->

<template>
	<div>
		<div class="form">
			<input type="text" v-model="post.title" />
			<button @click="createPost">Add new Property</button>
			<input type="text" placeholder="Search Todos" />
		</div>
	</div>
</template>
<script>
	export default {
		data() {
			return {
				post: {
					title: '',
				},
			};
		},
		methods: {
			createPost() {
				
				this.inputValueTitle = '';
			},
		},
	};
</script>
<style scoped>
	.form {
		display: grid;
		grid-gap: 10px;
	}

	.form > input {
		width: 100%;
		height: 40px;
		border: 3px solid darkseagreen;
		font-size: 18px;
		padding: 0 10px;
		border-radius: 5px;
	}

	.form > button {
		background-color: none;
		border: 3px solid darkseagreen;
		max-width: 200px;
		font-size: 17px;
		padding: 4px 10px;
		cursor: pointer;
		font-weight: 600;
		justify-self: end;
		transition: 0.1s;
		border-radius: 5px;
	}

	.form > button:active {
		transform: scale(1.1);
	}
</style>
