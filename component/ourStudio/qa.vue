<template>
	<div class="hs-accordion-group">
		<h1 class="font-semibold text-xl"><span class="border-l-4 border-indigo-500 mr-2"></span>よくある問合せ</h1>
		<div class="hs-accordion" id="hs-basic-heading-three" v-for="qa_list in qa_lists" :key="qa_list.question">
			<button
				class="hs-accordion-toggle hs-accordion-active:text-blue-600 group py-3 inline-flex items-center gap-x-3 w-full font-semibold text-left dark:hs-accordion-active:text-blue-500"
				aria-controls="hs-basic-collapse-three"
			>
				<svg
					class="hs-accordion-active:hidden hs-accordion-active:text-blue-600 hs-accordion-active:group-hover:text-blue-600 block w-3 h-3"
					width="16"
					height="16"
					viewBox="0 0 16 16"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path d="M2.62421 7.86L13.6242 7.85999" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
					<path d="M8.12421 13.36V2.35999" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
				</svg>
				<svg
					class="hs-accordion-active:block hs-accordion-active:text-blue-600 hs-accordion-active:group-hover:text-blue-600 hidden w-3 h-3"
					width="16"
					height="16"
					viewBox="0 0 16 16"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path d="M2.62421 7.86L13.6242 7.85999" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
				</svg>
				{{ qa_list.question }}
			</button>
			<div id="hs-basic-collapse-three" class="hs-accordion-content hidden w-full overflow-hidden transition-[height] duration-300" aria-labelledby="hs-basic-heading-three">
				<p class="">
					<em>{{ qa_list.answer }}</em>
				</p>
			</div>
		</div>
	</div>
</template>

<script>
const qa_lists = [
	{
		question: "SCSにどうやったら加入できますか？",
		answer:
			"基本的には募集は行っておらず、こちらが一緒に仕事をしたい！と思った方にお声がけをさせていただいております。しかし、ポートフォリオ等お持ちであればフォームから送っていただければこちらで確認はさせていただきます。",
	},
	{
		question: "SNSに載せても良いですか？",
		answer: "TikTok以外のSNS媒体であれば自由に載せていただいて構いません。",
	},
	{
		question: "オファーを出したいのですが",
		answer: "こちらのお問合せフォームよりお願いいたします。",
	},
];

module.exports = {
	data: function () {
		return {
			qa_lists: qa_lists,
			name: "NewsComponent",
		};
	},
};
</script>
