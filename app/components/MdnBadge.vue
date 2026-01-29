<template>
	<a :href="url" class="mdn-badge" target="_blank" rel="noopener noreferrer" :title="url">
		<img src="/mdn_logo.ico" alt="MDN" />
		<span class="label">
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
<style scoped>
.mdn-badge {
	display: inline-flex;
	align-items: center;
	gap: 0.5rem;
	padding: 0.25rem 0.6rem;
	border-radius: 3px;
	background: rgba(0, 0, 0, 0.03);
	border: 1px solid rgba(0, 0, 0, 0.06);
	color: inherit;
	text-decoration: none;
	font-weight: 600;
	font-size: 0.95rem;
}

.mdn-badge img {
	width: 18px;
	height: 18px;
	display: block;
}

.mdn-badge:hover,
.mdn-badge:focus {
	background: rgba(0, 0, 0, 0.06);
	text-decoration: none;
}

.label {
	line-height: 1;
}
</style>
