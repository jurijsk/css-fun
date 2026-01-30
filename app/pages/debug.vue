a<template>
	<PageLayout>
		<template #main>
			<span class="log"></span>
		</template>
		<template #footer>
			<MdnBadge url="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/clamp" />
		</template>
	</PageLayout>
</template>
<style>
:root {
	--value: var(--not_set, 1vw);
	/* this mess converts CSS units to their pixel number value */
	--value_scalar: calc(tan(atan2(var(--value), 1px)));

	--l: 3%;
	--l2: calc(tan(atan2(var(--l), 1px)));
}

.log {
	&::after {
		color: rgb(68, 185, 0);
		counter-reset: log var(--value_scalar);
		content: 'log: ' counter(log) 'px';
	}

}
</style>
