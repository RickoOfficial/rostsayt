<template>
	<div class="header-wrapper">
		<header class="container">
			<div class="row align-items-center">
				<NuxtLink to="/" class="col-2">
					<img src="https://rostsayt.ru/images/logo.svg" alt="Логотип">
				</NuxtLink>
				<nav class="col">
					<ul class="d-flex">
						<li>
							<NuxtLink to="/">Главная</NuxtLink>
						</li>
						<li>
							<NuxtLink to="/services">Услуги</NuxtLink>
						</li>
						<li>
							<NuxtLink to="/news">Новости</NuxtLink>
						</li>
						<li>
							<NuxtLink to="/404">404</NuxtLink>
						</li>
					</ul>
				</nav>
				<div class="right col-2 d-flex flex-column align-items-center">
					<a class="btn btn-link header-tel pt-0" href="tel:+74950055187">+7 (495) 005-51-87</a>
					<button class="btn btn-danger btn-sm">Заказать звонок</button>
				</div>
			</div>
		</header>
	</div>
</template>

<style scoped>
	* {
		transition: .5s;
	}
	.header-wrapper {
		padding: .5rem 0;
		box-shadow: 0 0 1.5rem #0005;
	}
	ul {
		margin: 0;
		padding: 0;
		list-style-type: none;
	}
	li a {
		padding: 0.5rem 1rem;
		color: #212529;
		text-decoration: none;
	}
	li:hover a {
		color: #b02a37;
	}
	.right a {
		padding: 0;
		color: #212529;
		text-decoration: none;
		font-weight: 700;
	}
</style>