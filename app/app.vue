<script setup lang="ts">
let stylesheets: { rel: 'stylesheet', href: string; }[] = [];

stylesheets.push({
	rel: 'stylesheet',
	href: './css/main.css'
});

const route = useRoute().name;
if(route) {
	stylesheets.push({
		rel: 'stylesheet',
		href: `./css/${route.toString()}.css`
	});
}

useHead({
	title: route?.toString(),
	link: stylesheets
});


useHead({
	link: [

	]
});
</script>
<template>
	<NuxtPage />
</template>