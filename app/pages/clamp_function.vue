<template>
	<article>
		<main> content goes here </main>
		<footer>
			<MdnBadge url="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/clamp" />
		</footer>
	</article>
</template>
<style scoped>
article {
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
