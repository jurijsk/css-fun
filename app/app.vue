<script setup lang="ts">
const route = useRoute();

useHead({
	title: () => route.name?.toString() || 'css-fun',
	link: () => {
		const sheets: { rel: 'stylesheet'; href: string; }[] = [
			{ rel: 'stylesheet', href: './css/main.css' }
		];
		if(route.name) {
			sheets.push({ rel: 'stylesheet', href: `./css/${route.name.toString()}.css` });
		}
		return sheets;
	}
});
</script>
<template>
	<NuxtPage />
</template>