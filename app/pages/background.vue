<template>
	<PageLayout>
		<template #main>
			<div class="container">
				<div class="box"></div>
				<div class="box"></div>
				<div class="box"></div>
				<div class="box"></div>
			</div>
		</template>
		<template #footer>
			<a href="https://multiple.js.org/">hack origin</a>
			<MdnBadge url="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/background-attachment#fixed"></MdnBadge>
		</template>
	</PageLayout>
</template>
<style scoped>
.box {
	background-size: cover;
	background-position: center;
	/* background attachment fixed makes background image start from the container top left conter */
	background-attachment: fixed;


	display: inline-block;
	width: 20vw;
	height: 20vw;
	background-image: linear-gradient(0.25turn, rgb(255, 255, 255), black);
	margin-top: 10vh;
	margin-left: 10vh;
	border: 1px solid salmon;
}
</style>