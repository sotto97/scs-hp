<template>
	<div class="p-2">
		<h1 class="font-semibold text-7xl mt-2"><span class="text-green-500">S</span>otto</h1>
		<h1 class="font-semibold text-7xl mt-2">Creative</h1>
		<h1 class="font-semibold text-7xl mt-2">Studio</h1>
		<!-- <h1 class="font-semibold text-7xl mt-2">Sotto Creative Studio</h1> -->
		<p class="text-base mt-2">シンプルに言えば、何でもこなせるクリエイティブ集団。音楽、グラフィック、アパレル、カフェ経営など、各々の立ち位置で自由に表現活動を行っている。</p>
		<h1 class="font-semibold text-xl"><span class="border-l-4 border-green-500 mr-2"></span>SCSの構成は？</h1>

		<p class="text-base">「SCS」はさまざまなセクションで構成されていて、音楽、グラフィック、アパレルなど、各々の立ち位置で自由に表現活動を行う集団です。</p>
		<!-- <div class="flex">
			<div class="flex-1 m-1 w-40 bg-black h-40"></div>
			<div class="flex-1 m-1 w-40 bg-black h-40"></div>
			<div class="flex-1 m-1 w-40 bg-black h-40"></div>
			<div class="flex-1 m-1 w-40 bg-black h-40"></div>
		</div> -->
		<div class="flex flex-wrap">
			<!-- <div style="width: 350px; height:350px;" class="w-40 h-40 p-2 bg-black"></div> -->
			<div style="width: 160px; height: 160px" class="m-1 bg-black text-center text-white">
				<p class="text-white p-2">test-document</p>
			</div>
			<div style="width: 160px; height: 160px" class="m-1 bg-black text-center text-white">
				<p class="text-white p-2">test-document</p>
			</div>
			<div style="width: 160px; height: 160px" class="m-1 bg-black text-center text-white">
				<p class="text-white p-2">test-document</p>
			</div>
			<div style="width: 160px; height: 160px" class="m-1 bg-black text-center text-white">
				<p class="text-white p-2">test-document</p>
			</div>
			<div style="width: 160px; height: 160px" class="m-1 bg-black text-center text-white">
				<p class="text-white p-2">test-document</p>
			</div>
		</div>
	</div>
</template>

<script>
module.exports = {
	data: function () {
		return {
			name: "AboutComponent",
		};
	},
};
</script>
