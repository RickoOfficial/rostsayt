<template>
	<div>
		<NuxtLink :to="`/news`" class="btn btn-danger btn-sm text-decoration-none">&#60; Назад</NuxtLink>
		<h1 class="col-12">{{post.title}}</h1>
		<img :src="`${photo.url}`" class="d-block col-4 mx-auto" :alt="`${post.title}`">
		<div class="col-12">{{post.body}}</div>
	</div>
</template>

<script>
import axios from 'axios';

export default {
	data() {
		return {
			post: undefined,
			photo: undefined
		}
	},
	async asyncData({ route }) {
		try {
			let tmpPost = await axios.get(`https://jsonplaceholder.typicode.com/posts/${route.params.id}`);
			let tmpPhoto = await axios.get(`https://jsonplaceholder.typicode.com/photos/${route.params.id}`);
			return { post: tmpPost.data, photo: tmpPhoto.data };
		} catch (err) {
			console.log(err);
		}
		return { item: itemResponse.data, categories: categoriesResponse.data };
	},
}
</script>