<template>
	<div class="container">
		<about-component></about-component>
		<artist-component></artist-component>
		<news-component></news-component>
		<qa-component></qa-component>
		<button-component></button-component>
	</div>
</template>

<script>
const AboutComponent = httpVueLoader("./about.vue");
const ArtistComponent = httpVueLoader("./artist.vue");
const NewsComponent = httpVueLoader("./news.vue");
const QaComponent = httpVueLoader("./qa.vue");
const ButtonComponent = httpVueLoader("./button.vue");

module.exports = {
	components: {
		AboutComponent,
		ArtistComponent,
		NewsComponent,
		QaComponent,
		ButtonComponent,
	},
	name: "OurStudioComponent",
};
</script>
