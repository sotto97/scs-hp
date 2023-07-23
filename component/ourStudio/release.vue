<template>
	<div class="bg-white py-6 sm:py-8 lg:py-12">
		<div class="mt-4 mx-auto max-w-screen-2xl px-4 md:px-8">
			<h2 class="mb-4 text-center text-2xl font-bold text-gray-800 md:mb-6 lg:text-3xl">プレスリリース</h2>
			<v-container v-for="news_list in news_lists" :key="news_list.date">
				<v-row class="hover:bg-gray-200 transition cursor-pointer">
					<v-col cols="3" class="p-0">
						<v-list-item-content class="pl-1">
							<v-list-item-title>{{ news_list.date }}</v-list-item-title>
						</v-list-item-content>
					</v-col>
					<v-col cols="9" class="p-0 pl-1">
						<v-list-item-content>
							<v-list-item-title class="text-left">
								<span class="w-2/12 border-l-4 border-indigo-500 pl-2 text-center"></span>
								<span>{{ news_list.title }}</span>
							</v-list-item-title>
						</v-list-item-content>
					</v-col>
				</v-row>
			</v-container>
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
		date: "2023/2/14",
		title: "Mixテープのリリース",
	},
	{
		date: "2023/1/4",
		title: "グラフィックアーティストの加入",
	},
	{
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
