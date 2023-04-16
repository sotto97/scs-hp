<template>
	<div class="container">
		<about-component></about-component>
		<artist-component></artist-component>
		<news-component></news-component>
		<qa-component></qa-component>
	</div>
</template>

<script>
// const routes = [
// 	{ name: "music", path: "/music", component: httpVueLoader("./component/music.vue") },
// 	{ name: "apparel", path: "/apparel", component: httpVueLoader("./component/apparel.vue") },
// 	{ name: "about", path: "/about", component: httpVueLoader("./component/about.vue") },
// ];

// const router = new VueRouter({
// 	routes,
// });

module.exports = {
	data: function () {
		return {
			router: router,
			components: {
				AboutComponent: httpVueLoader("./component/about.vue"),
				NewsComponent: httpVueLoader("./component/news.vue"),
				QaComponent: httpVueLoader("./component/qa.vue"),
				ArtistComponent: httpVueLoader("./component/artist.vue"),
			},
			vuetify: new Vuetify(),
			data() {
				return {
					drawer: null,
					nav_lists: nav_lists,
				};
			},
		};
	},
};
</script>
