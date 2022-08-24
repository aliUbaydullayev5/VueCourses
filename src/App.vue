<!-- @format -->

<template>
	<div class="main">
		<PostForm @create="addNewProperty" />
		<PostList :posts="posts" />
		<!-- <PostList /> -->
	</div>
</template>

<script>
	import PostForm from './Components/PostForm.vue';
	import PostList from './Components/PostList.vue';
	component: {
		PostList, PostForm;
	}
	export default {
		data() {
			return {
				posts: [
					{ id: 1, title: 'Work-1' },
					{ id: 2, title: 'Work-2' },
					{ id: 3, title: 'Work-3' },
					{ id: 4, title: 'Work-4' },
					{ id: 5, title: 'Work-5' },
				],
			};
		},
		methods: {
			deleteFunc(id) {
				this.posts = this.posts.filter((value) => value.id !== id);
			},
            addNewProperty(post) {
                this.posts.push({id: post.id, title: post.title})
			},
		},
		components: { PostForm, PostList },
	};
</script>

<style>
	@import url('https://fonts.googleapis.com/css2?family=DynaPuff:wght@400;500;600;700&display=swap');

	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	body {
		padding: 0 100px;
		font-family: 'DynaPuff', cursive;
	}

	.main {
		margin: 60px auto;
	}

	@media screen and (max-width: 400px) {
		body {
			padding: 0 20px;
		}
	}
</style>
