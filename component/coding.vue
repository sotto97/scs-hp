<template>
	<div class="w-full p-4">
		<p>ボタンテンプレート</p>
		<div class="flex w-full">
			<div class="w-full">
				<div class="flex items-center justify-center">
					<div class="w-full h-12 bg-gradient-to-r from-indigo-400 via-blue-400 to-green-500 rounded-lg">
						<p class="text-white h-full w-full font-bold flex items-center justify-center">Click Me!</p>
					</div>
				</div>
				<div class="bg-black text-white p-4 mt-2 rounded-lg">
					&lt;div class=&quot;flex items-center justify-center&quot;&gt;<br />
					&emsp;&#9;&lt;div class=&quot;w-full h-12 bg-gradient-to-r from-indigo-400 via-blue-400 to-green-500 rounded-full&quot;&gt;<br />
					&emsp;&emsp;&lt;p class=&quot;text-white h-full w-full font-bold flex items-center justify-center&quot;&gt;Click Me!&lt;/p&gt;<br />
					&emsp;&lt;/div&gt;<br />
					&lt;/div&gt;<br />
				</div>
			</div>
		</div>
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
