<template>
	<div class="p-2">
		<h1 class="font-semibold text-xl"><span class="border-l-4 border-green-500 mr-2"></span>プレスリリース</h1>
		<v-container v-for="news_list in news_lists" :key="news_list.date">
			<v-row class="hover:bg-green-200 transition cursor-pointer">
				<v-col cols="3" class="p-0">
					<v-list-item-content class="pl-1">
						<v-list-item-title>{{ news_list.date }}</v-list-item-title>
					</v-list-item-content>
				</v-col>
				<v-col cols="9" class="p-0 pl-1">
					<v-list-item-content>
						<v-list-item-title class="text-left">
							<span class="w-2/12 border-l-4 border-green-500 pl-2 text-center"></span>
							<span>{{ news_list.title }}</span>
						</v-list-item-title>
					</v-list-item-content>
				</v-col>
			</v-row>
		</v-container>
		<div class="mt-2">
			<a href="" class="w-full cursor-pointer text-center">
				<p class="py-2 border-solid border-2 border-black bg-black hover:bg-white transition text-white hover:text-black">過去のプレスリリースも見る</p>
			</a>
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
