<template>
	<div class="d-flex-col">
		<div id="scene" class="d-flex-row" v-html="this.scenes[Math.floor(Math.random()*this.scenes.length)]"></div>
		<h1>404</h1>
		<h2>Страница не найдена</h2>
		<p>Вернуться на <NuxtLink to="/">главную</NuxtLink></p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			selectScene: 0,
			scenes: [
				'<span class="man h1">༼ つ ◕_◕ ༽つ</span><span class="cake h1">🧁</span>',
				'<span class="man h1">(╯°□°）╯︵ ┻━┻</span>',
				'<span class="man h1">¯\\_(ツ)_/¯</span>',
				'<span class="man h1">＞﹏＜</span>',
				'<span class="man h1">(⊙ˍ⊙)</span>',
			]
		}
	}
}
</script>

<style>
	.d-flex-row {
		display: flex;
		justify-content: center;
		align-items: center;
		margin: 10vh 0 15vh;
	}
	.d-flex-col {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 10vh 0;
	}
	.cake {
		margin-top: -10rem;
		margin-left: 10rem;
	}
</style>