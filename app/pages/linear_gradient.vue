a<template>
	<PageLayout>
		<template #main>
			<div class="in_hsl_mess"></div>
			<div class="in_default"></div>
			<div class="in_srgb"></div>
			<div class="in_srgb_linear"></div>
			<div class="in_display_p3"></div>
			<div class="in_display_p3_linear"></div>
			<div class="in_a98_rgb"></div>
			<div class="in_prophoto_rgb"></div>
			<div class="in_rec2020"></div>
			<div class="in_lab"></div>
			<div class="in_oklab"></div>
			<div class="in_hwb"></div>
			<div class="in_lch"></div>
			<div class="in_oklch"></div>
			<div class="in_xyz"></div>
			<div class="in_xyz_d50"></div>
			<div class="in_xyz_d65"></div>
			<div class="in_hsl"></div>
			<div class="in_hsl_longer"></div>
			<!-- 3-stop gradients: red → green → blue -->
			<div class="in_default_3"></div>
			<div class="in_srgb_3"></div>
			<div class="in_srgb_linear_3"></div>
			<div class="in_display_p3_3"></div>
			<div class="in_display_p3_linear_3"></div>
			<div class="in_a98_rgb_3"></div>
			<div class="in_prophoto_rgb_3"></div>
			<div class="in_rec2020_3"></div>
			<div class="in_lab_3"></div>
			<div class="in_oklab_3"></div>
			<div class="in_hsl_3"></div>
			<div class="in_hwb_3"></div>
			<div class="in_lch_3"></div>
			<div class="in_oklch_3"></div>
			<div class="in_xyz_3"></div>
			<div class="in_xyz_d50_3"></div>
			<div class="in_xyz_d65_3"></div>
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

.in_srgb {
	background: linear-gradient(90deg in srgb, blue, red);

	&::after {
		content: 'color space: srgb';
	}
}

.in_srgb_linear {
	background: linear-gradient(90deg in srgb-linear, blue, red);

	&::after {
		content: 'color space: srgb-linear';
	}
}

.in_display_p3 {
	background: linear-gradient(90deg in display-p3, blue, red);

	&::after {
		content: 'color space: display-p3';
	}
}

.in_display_p3_linear {
	background: linear-gradient(90deg in display-p3-linear, blue, red);

	&::after {
		content: 'color space: display-p3-linear';
	}
}

.in_a98_rgb {
	background: linear-gradient(90deg in a98-rgb, blue, red);

	&::after {
		content: 'color space: a98-rgb';
	}
}

.in_prophoto_rgb {
	background: linear-gradient(90deg in prophoto-rgb, blue, red);

	&::after {
		content: 'color space: prophoto-rgb';
	}
}

.in_rec2020 {
	background: linear-gradient(90deg in rec2020, blue, red);

	&::after {
		content: 'color space: rec2020';
	}
}

.in_hwb {
	background: linear-gradient(90deg in hwb, blue, red);

	&::after {
		content: 'color space: hwb';
	}
}

.in_lch {
	background: linear-gradient(90deg in lch, blue, red);

	&::after {
		content: 'color space: lch';
	}
}

.in_oklch {
	background: linear-gradient(90deg in oklch, blue, red);

	&::after {
		content: 'color space: oklch';
	}
}

.in_xyz {
	background: linear-gradient(90deg in xyz, blue, red);

	&::after {
		content: 'color space: xyz';
	}
}

.in_xyz_d50 {
	background: linear-gradient(90deg in xyz-d50, blue, red);

	&::after {
		content: 'color space: xyz-d50';
	}
}

.in_xyz_d65 {
	background: linear-gradient(90deg in xyz-d65, blue, red);

	&::after {
		content: 'color space: xyz-d65';
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


/* 3-stop gradients: red -> green -> blue for many color spaces */

.in_default_3 {
	background: linear-gradient(90deg, red, green, blue);
}

.in_default_3::after {
	content: 'color space: default (3 stops)';
}

.in_srgb_3 {
	background: linear-gradient(90deg in srgb, red, green, blue);
}

.in_srgb_3::after {
	content: 'color space: srgb (3 stops)';
}

.in_srgb_linear_3 {
	background: linear-gradient(90deg in srgb-linear, red, green, blue);
}

.in_srgb_linear_3::after {
	content: 'color space: srgb-linear (3 stops)';
}

.in_display_p3_3 {
	background: linear-gradient(90deg in display-p3, red, green, blue);
}

.in_display_p3_3::after {
	content: 'color space: display-p3 (3 stops)';
}

.in_display_p3_linear_3 {
	background: linear-gradient(90deg in display-p3-linear, red, green, blue);
}

.in_display_p3_linear_3::after {
	content: 'color space: display-p3-linear (3 stops)';
}

.in_a98_rgb_3 {
	background: linear-gradient(90deg in a98-rgb, red, green, blue);
}

.in_a98_rgb_3::after {
	content: 'color space: a98-rgb (3 stops)';
}

.in_prophoto_rgb_3 {
	background: linear-gradient(90deg in prophoto-rgb, red, green, blue);
}

.in_prophoto_rgb_3::after {
	content: 'color space: prophoto-rgb (3 stops)';
}

.in_rec2020_3 {
	background: linear-gradient(90deg in rec2020, red, green, blue);
}

.in_rec2020_3::after {
	content: 'color space: rec2020 (3 stops)';
}

.in_lab_3 {
	background: linear-gradient(90deg in lab, red, green, blue);
}

.in_lab_3::after {
	content: 'color space: lab (3 stops)';
}

.in_oklab_3 {
	background: linear-gradient(90deg in oklab, red, green, blue);
}

.in_oklab_3::after {
	content: 'color space: oklab (3 stops)';
}

.in_hsl_3 {
	background: linear-gradient(90deg in hsl, red, green, blue);
}

.in_hsl_3::after {
	content: 'color space: hsl (3 stops)';
}

.in_hwb_3 {
	background: linear-gradient(90deg in hwb, red, green, blue);
}

.in_hwb_3::after {
	content: 'color space: hwb (3 stops)';
}

.in_lch_3 {
	background: linear-gradient(90deg in lch, red, green, blue);
}

.in_lch_3::after {
	content: 'color space: lch (3 stops)';
}

.in_oklch_3 {
	background: linear-gradient(90deg in oklch, red, green, blue);
}

.in_oklch_3::after {
	content: 'color space: oklch (3 stops)';
}

.in_xyz_3 {
	background: linear-gradient(90deg in xyz, red, green, blue);
}

.in_xyz_3::after {
	content: 'color space: xyz (3 stops)';
}

.in_xyz_d50_3 {
	background: linear-gradient(90deg in xyz-d50, red, green, blue);
}

.in_xyz_d50_3::after {
	content: 'color space: xyz-d50 (3 stops)';
}

.in_xyz_d65_3 {
	background: linear-gradient(90deg in xyz-d65, red, green, blue);
}

.in_xyz_d65_3::after {
	content: 'color space: xyz-d65 (3 stops)';
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
