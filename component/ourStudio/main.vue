<template>
	<div class="container">
		<about-component></about-component>
		<artist-component></artist-component>
		<release-component></release-component>
		<qa-component></qa-component>
		<moc-component></moc-component>
	</div>
</template>

<script>
const AboutComponent = httpVueLoader("./about.vue");
const ArtistComponent = httpVueLoader("./artist.vue");
const ReleaseComponent = httpVueLoader("./release.vue");
const QaComponent = httpVueLoader("./qa.vue");
const MocComponent = httpVueLoader("./moc.vue");

module.exports = {
	components: {
		AboutComponent,
		ArtistComponent,
		ReleaseComponent,
		QaComponent,
		MocComponent,
	},
	name: "OurStudioComponent",
};
</script>
