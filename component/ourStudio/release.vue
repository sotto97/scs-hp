<template>
	<div class="bg-white py-6 sm:py-8 lg:py-12 w-full sm:w-3/4 mx-auto">
		<div class="mt-4 mx-auto max-w-screen-2xl px-4 md:px-8">
			<p class="mb-2 text-center font-semibold text-indigo-500 md:mb-3 lg:text-lg">News</p>
			<h2 class="mb-4 text-center text-2xl font-bold text-gray-800 md:mb-6 lg:text-3xl">プレスリリース</h2>
			<div class="w-full border-t-2" v-for="news_list in news_lists" :key="news_list.date">
				<div class="p-2 sm:p-4 flex flex-wrap">
					<div class="w-1/3 sm:w-1/6 text-center py-1 sm:py-2 px-4 bg-indigo-500 text-white rounded-md">{{ news_list.category }}</div>
					<div class="w-2/3 sm:w-1/6 text-left my-auto px-4">{{ news_list.date }}</div>
					<div class="pl-2 sm:pl-0 mt-2 sm:my-auto">
						<a href="" class="w-full sm:w-4/6 text-left hover:underline hover:text-indigo-500 transition">{{ news_list.title }}</a>
					</div>
				</div>
			</div>
			<div class="w-full border-b-2"></div>
			<div class="w-full mt-4 text-center align-center">
				<button class="text-indigo-500 hover:text-white bg-white hover:bg-indigo-600 transition border-2 border-solid border-indigo-500 font-semibold py-4 px-20 text-xs rounded-md">
					過去のプレスリリースも見る
				</button>
			</div>
		</div>
	</div>
</template>

<script>
const news_lists = [
	{
		category: "Music",
		date: "2023/2/14",
		title: "Mixテープのリリース",
	},
	{
		category: "Graphic",
		date: "2023/1/4",
		title: "グラフィックアーティストの加入",
	},
	{
		category: "Web",
		date: "2022/12/22",
		title: "SCS公式ホームページリリース",
	},
];

module.exports = {
	data: function () {
		return {
			name: "NewsComponent",
			news_lists: news_lists,
		};
	},
};
</script>
