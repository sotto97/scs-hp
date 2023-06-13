<template>
	<div class="container">
		<about-component></about-component>
		<artist-component></artist-component>
		<news-component></news-component>
		<qa-component></qa-component>
		<moc-component></moc-component>
	</div>
</template>

<script>
const AboutComponent = httpVueLoader("./about.vue");
const ArtistComponent = httpVueLoader("./artist.vue");
const NewsComponent = httpVueLoader("./news.vue");
const QaComponent = httpVueLoader("./qa.vue");
const MocComponent = httpVueLoader("./moc.vue");

module.exports = {
	components: {
		AboutComponent,
		ArtistComponent,
		NewsComponent,
		QaComponent,
		MocComponent,
	},
	name: "OurStudioComponent",
};
</script>
