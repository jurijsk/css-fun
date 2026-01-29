<template>
	<a :href="url" class="badge" target="_blank" rel="noopener noreferrer" :title="url">
		<img src="/mdn_logo.ico" alt="MDN" />
		<span>
			<slot>{{ labelText }}</slot>
		</span>
	</a>
</template>
<script setup lang="ts">
import { computed } from 'vue';

const props = defineProps({
	url: { type: String, required: true },
	label: { type: String, default: '' }
});

const labelText = computed(() => {
	if(props.label && props.label.trim()) return props.label;
	try {
		const u = new URL(props.url, typeof window !== 'undefined' ? window.location.origin : 'https://example.com');
		let p = u.pathname || '';
		if(p.endsWith('/')) p = p.slice(0, -1);
		const last = p.split('/').pop() || u.hostname;
		return decodeURIComponent(last) || props.url;
	} catch(e) {
		const parts = props.url.split('/').filter(Boolean);
		return parts.pop() || props.url;
	}
});
</script>
