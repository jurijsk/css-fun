<template>
	<article>
		<main>
			<slot name="main" />
		</main>
		<footer v-if="$slots.footer">
			<button class="badge" @click="navigateTo('/')">/</button>
			<slot name="footer" />
		</footer>
	</article>
</template>
<style scoped>
article {
	min-height: 100vh;
	display: flex;
	flex-direction: column;

	main {
		flex: 1 0 auto;
		padding: 1rem;
	}

	footer {
		flex-shrink: 0;
		padding: 0.75rem 1rem;
		border-top: 1px solid rgba(0, 0, 0, 0.06);
		display: flex;
		gap: 0.5rem;
		background: transparent;
	}
}
</style>
