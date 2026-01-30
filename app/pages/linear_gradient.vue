a<template>
	<PageLayout>
		<template #main>
			<div class="in_hsl_mess"></div>
			<div class="in_default"></div>
			<div class="in_oklab"></div>
			<div class="in_lab"></div>
			<div class="in_hsl"></div>
			<div class="in_hsl_longer"></div>
		</template>
		<template #footer>
			<MdnBadge url="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/clamp" />
		</template>
	</PageLayout>
</template>
<style>
.in_default {
	background: linear-gradient(90deg, blue, red);

	&::after {
		content: 'color space: default';
	}
}

.in_oklab {
	background: linear-gradient(90deg in oklab, blue, red);

	&::after {
		content: 'color space: oklab';
	}
}

.in_lab {
	background: linear-gradient(90deg in lab, blue, red);

	&::after {
		content: 'color space: lab';
	}
}


.in_hsl {
	background: linear-gradient(90deg in hsl, blue, red);

	&::after {
		content: 'color space: hsl (shorter)';
	}
}


.in_hsl_longer {
	background: linear-gradient(90deg in hsl longer hue, blue, red);

	&::after {
		content: 'color space:  hsl longer hue';
	}
}

.in_hsl_mess {
	background: linear-gradient(90deg in d, blue, red);

	&::after {
		content: 'mess';
	}
}

div {
	position: relative;
	width: 70%;
	height: 50px;
}

*::after {
	border: 0px none;
	white-space: nowrap;
	position: absolute;
	bottom: 0px;
	left: 100%;
}
</style>
