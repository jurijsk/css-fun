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
			<div>
				<div>
					<p class="default">Jurijs</p>
				</div>
				<div>
					<p class="text_box_text">Jurijs</p>
				</div>
				<div>
					<p class="text_box_ex_text">Jurijs</p>
				</div>
				<div>
					<p class="text_box_cap_alphabetic">Jurijs</p>
				</div>
				<div>
					<p class="text_box_ex_alphabetic">Jurijs</p>
				</div>
				<div>
					<p class="text_box_mess">Jurijs</p>
				</div>
			</div>
			<div class="font_segoe">
				<div>
					<p class="default">Jurijs</p>
				</div>
				<div>
					<p class="text_box_text">Jurijs</p>
				</div>
				<div>
					<p class="text_box_ex_alphabetic">Jurijs</p>
				</div>
				<div>
					<p class="text_box_ex_alphabetic">تَشْكِيل</p>
				</div>
			</div>
			<div>
				<div>
					<p class="default">تَشْكِيل</p>
				</div>
				<div>
					<p class="text_box_text">تَشْكِيل</p>
				</div>
				<div>
					<p class="text_box_ex_text">تَشْكِيل</p>
				</div>
				<div>
					<p class="text_box_ex_alphabetic">تَشْكِيل</p>
				</div>
			</div>
		</main>
		<footer>
			<MdnBadge url="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/text-box" />
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
