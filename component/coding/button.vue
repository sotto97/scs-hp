<template>
	<div class="w-full p-4">
		<p class="font-semibold text-lg">ボタンテンプレート</p>
		<p class="mb-0">パターン1</p>
		<div class="w-full p-4 bg-gray-300 rounded-lg">
			<div class="flex items-center justify-center">
				<div class="w-full h-12 bg-gradient-to-r from-emerald-400 via-blue-400 to-green-500 rounded-lg">
					<p class="text-white h-full w-full font-bold flex items-center justify-center">Click Me!</p>
				</div>
			</div>
			<div class="bg-black text-white p-4 mt-2 rounded-lg">
				&lt;div class=&quot;flex items-center justify-center&quot;&gt;<br />
				&emsp;&#9;&lt;div class=&quot;w-full h-12 bg-gradient-to-r from-emerald-400 via-blue-400 to-green-500 rounded-full&quot;&gt;<br />
				&emsp;&emsp;&lt;p class=&quot;text-white h-full w-full font-bold flex items-center justify-center&quot;&gt;Click Me!&lt;/p&gt;<br />
				&emsp;&lt;/div&gt;<br />
				&lt;/div&gt;<br />
			</div>
		</div>
		<p class="mt-2 mb-0">パターン2</p>
		<div class="w-full p-4 bg-gray-300 rounded-lg">
			<div class="flex items-center justify-center">
				<div class="w-full h-12 bg-gradient-to-r from-emerald-400 via-blue-400 to-emerald-500 rounded-lg">
					<p class="text-white h-full w-full font-bold flex items-center justify-center">Click Me!</p>
				</div>
			</div>
			<div class="bg-black text-white p-4 mt-2 rounded-lg">
				&lt;div class=&quot;flex items-center justify-center&quot;&gt;<br />
				&emsp;&#9;&lt;div class=&quot;w-full h-12 bg-gradient-to-r from-emerald-400 via-blue-400 to-emerald-500 rounded-full&quot;&gt;<br />
				&emsp;&emsp;&lt;p class=&quot;text-white h-full w-full font-bold flex items-center justify-center&quot;&gt;Click Me!&lt;/p&gt;<br />
				&emsp;&lt;/div&gt;<br />
				&lt;/div&gt;<br />
			</div>
		</div>
		<p class="mt-2">※参考：<a href="https://gradientbuttons.colorion.co/">https://gradientbuttons.colorion.co/</a></p>
	</div>
</template>
<script>
module.exports = {
	data: function () {
		return {
			name: "CodingComponent",
		};
	},
};
</script>
