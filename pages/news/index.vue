<template>
	<div>
		<h1>Новости</h1>
		<div class="row">

			<div
				v-for="(post, index) in posts"
				:key="post.id"
				class="col-sm-12 col-md-6 col-lg-4 col-xl-3 mb-3"
			>
				<div class="card h-100">
					<img :src="`${photo[index].thumbnailUrl}`" class="card-img-top mx-auto" :alt="`${post.title}`">
					<div class="card-body d-flex flex-column justify-content-between">
						<div class="mb-2">
							<h2 class="card-title h5 text-dark text-decoration-none">{{post.title}}</h2>
							<p class="card-text">{{post.body}}</p>
						</div>
						<NuxtLink :to="`/news/${post.id}`" class="btn btn-danger btn-sm">Читать полностью</NuxtLink>
					</div>
				</div>
			</div>

		</div>
	</div>
</template>

<script>
import axios from 'axios';

export default {
	data() {
		return {
			posts: [],
			photo: []
		}
	},
	async asyncData() {
		try {
			let tmpPosts = await axios.get('https://jsonplaceholder.typicode.com/posts');
			let tmpPhoto = await axios.get('https://jsonplaceholder.typicode.com/photos?_limit=100');
			return { posts: tmpPosts.data, photo: tmpPhoto.data };
		} catch (err) {
			console.log(err);
		}
	},
}
</script>