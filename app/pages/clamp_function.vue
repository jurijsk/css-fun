<script setup lang="ts">

const route = useRoute().name;
let stylesheet: { rel: 'stylesheet', href: string; } | undefined = undefined;

if(route) {
	stylesheet = {
		rel: 'stylesheet',
		href: `./css/${route.toString()}.css`
	};
}

useHead({
	title: route?.toString(),
	link: [stylesheet]
});
</script>
<template>
	<div class="page_wrapper">
		<main class="page_main">
		</main>
		<footer>
			<MdnBadge url="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/clamp" />
		</footer>
	</div>
</template>
<style scoped>
.page_wrapper {
	min-height: 100vh;
	display: flex;
	flex-direction: column;

	/* use type selectors when possible (main, footer) and CSS nesting */
	main {
		flex: 1 0 auto;
	}

	footer {
		flex-shrink: 0;
		padding: 0.75rem 1rem;
		border-top: 1px solid rgba(0, 0, 0, 0.06);
		display: flex;
		background: transparent;
	}
}
</style>
