<template>
	<div class="container">
		<about-component></about-component>
		<artist-component></artist-component>
		<news-component></news-component>
		<qa-component></qa-component>
	</div>
</template>

<script>
const routes = [
	// { name: "foo", path: "/foo", component: httpVueLoader("./component/foo.vue") },
	// { name: "bar", path: "/bar", component: httpVueLoader("./component/bar.vue") },
	{ name: "music", path: "/music", component: httpVueLoader("./component/music.vue") },
	{ name: "apparel", path: "/apparel", component: httpVueLoader("./component/apparel.vue") },
	{ name: "about", path: "/about", component: httpVueLoader("./component/about.vue") },
];

const router = new VueRouter({
	routes,
});

const nav_lists = [
	{
		name: "Our Studio",
		icon: "mdi-garage-open",
		path: "/about",
	},
	{
		name: "Music",
		params: "music",
		title: "Music",
		icon: "mdi-music",
		lists: ["Event", "DJs"],
		path: "/music",
	},
	{
		name: "Apparel",
		params: "apparel",
		title: "Apparel",
		icon: "mdi-tshirt-crew",
		path: "/apparel",
	},
	{
		name: "Coding",
		params: "coding",
		title: "Coding",
		icon: "mdi-code-tags",
		path: "",
	},
	{
		name: "Cafe",
		icon: "mdi-coffee",
		lists: ["神戸", "代官山"],
		path: "/apparel",
	},
	{
		name: "Graphic",
		icon: "mdi-camera-iris",
		lists: ["Photographer"],
		path: "",
	},
	{
		name: "Fitness Gym",
		icon: "mdi-dumbbell",
		path: "",
	},
];

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
