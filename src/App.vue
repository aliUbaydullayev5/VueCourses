<!-- @format -->

<template>
	<div>
		<div>
			<button v-on:click="addLike">Like</button>
			<button v-on:click="addDislike">DisLike</button>
		</div>
		<p>
			Кол-во лайков: <strong>{{ likes }}</strong>
		</p>
		<p>
			Кол-во дизлайков: <strong>{{ dislikes }}</strong>
		</p>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				likes: 0,
				dislikes: 0,
			};
		},

		methods: {
			addLike() {
				this.likes += 1;
			},
			addDislike() {
				this.dislikes += 1;
			},
		},
	};
</script>

<style></style>
