<script setup lang="ts">
useHead({
	link: [
		{
			rel: 'stylesheet',
			href: './css/pico.css'
		}
	]
});

const router = useRouter();

const routes = router
	.getRoutes()
	.filter((r) => r.path && r.path.startsWith('/'))
	.filter((r) => !r.path.includes(':')) // hide dynamic routes
	.filter((r) => r.name !== undefined) // prefer named routes
	// dedupe by path
	.reduce((acc: any[], r) => {
		if(!acc.find((a) => a.path === r.path)) acc.push(r);
		return acc;
	}, [])
	.sort((a, b) => a.path.localeCompare(b.path));
</script>
<template>
	<main class="container">
		<header>
			<h3>Routes</h3>
		</header>
		<nav>
			<ul>
				<li v-for="r in routes" :key="r.path">
					<NuxtLink :to="r.path">{{ r.name || r.path }}</NuxtLink>
				</li>
			</ul>
		</nav>
		<section>
			<p>Select a route above to navigate.</p>
		</section>
	</main>
</template>
<style scoped>
.router-link-active {
	color: orange;
}

nav ul {
	display: block;

	li {
		display: block;
		padding: 0px 10px;
	}

}
</style>