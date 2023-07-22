<template>
	<div class="bg-white py-6 sm:py-8 lg:py-12">
		<div class="mx-auto max-w-screen-xl px-4 md:px-8">
			<!-- text - start -->
			<!-- <div class="mb-10 md:mb-16">
				<h2 class="mb-4 text-center text-2xl font-bold text-gray-800 md:mb-6 lg:text-3xl">サブスクリプション一覧</h2>

				<p class="mx-auto max-w-screen-md text-center text-gray-500 md:text-lg">
					This is a section of some simple filler text, also known as placeholder text. It shares some characteristics of a real written text but is random or otherwise generated.
				</p>
			</div> -->
			<div class="grid gap-4 sm:grid-cols-2 md:gap-6 lg:grid-cols-2 xl:grid-cols-2 xl:gap-8">
				<!-- article - start -->
				<div class="flex flex-col items-center overflow-hidden rounded-lg border md:flex-row">
					<a href="#" class="group relative block h-48 w-full shrink-0 self-start overflow-hidden bg-gray-100 md:h-full md:w-32 lg:w-48">
						<iframe
							width="100%"
							height="100%"
							src="https://www.youtube.com/embed/5v-z7jKJbxc"
							title="YouTube video player"
							frameborder="0"
							allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
							allowfullscreen
						></iframe>
					</a>

					<div class="flex flex-col gap-2 p-4 lg:p-6">
						<h2 class="text-xl font-bold text-gray-800">
							<a href="#" class="">
								<span class="text-indigo-500 truncate">日本語ラップとか個人的にエモくなれる曲 Mix</span>
							</a>
						</h2>
						<span class="text-sm text-gray-400">1,994,617 回視聴 2020/11/15</span>
						<p class="text-gray-500 overflow-ellipsis overflow-hidden h-12">
							僕のSpotifyのプレイリストから選んで作ってみました。 垂れ流しじゃなく、Mashupしてみました。 良いと思ってもらえれば幸いです。 よろしくどうぞ。 おすすめの曲とか、こんな曲良いよ〜とかあれば
							コメントで教えてください。 ※利益は著作権主に流れます。僕自身に収益が入ってくることはありません。
						</p>
					</div>
				</div>
				<!-- article - end -->

				<!-- article - start -->
				<div class="flex flex-col items-center overflow-hidden rounded-lg border md:flex-row">
					<a href="#" class="group relative block h-48 w-full shrink-0 self-start overflow-hidden bg-gray-100 md:h-full md:w-32 lg:w-48">
						<img
							src="https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&q=75&fit=crop&w=600"
							loading="lazy"
							alt="Photo by Lorenzo Herrera"
							class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110"
						/>
					</a>
					<div class="flex flex-col gap-2 p-4 lg:p-6">
						<h2 class="text-xl font-bold text-gray-800">
							<a href="#" class="transition duration-100 hover:text-indigo-500 active:text-indigo-600">
								<span class="text-indigo-500">Youtube</span>
							</a>
						</h2>
						<span class="text-sm text-gray-400">April 07, 2021</span>
						<p class="text-gray-500">This is a section of some simple filler text, also known as placeholder text.</p>
					</div>
				</div>
				<!-- article - end -->

				<!-- article - start -->
				<div class="flex flex-col items-center overflow-hidden rounded-lg border md:flex-row">
					<a href="#" class="group relative block h-48 w-full shrink-0 self-start overflow-hidden bg-gray-100 md:h-full md:w-32 lg:w-48">
						<img
							src="https://images.unsplash.com/photo-1542759564-7ccbb6ac450a?auto=format&q=75&fit=crop&w=600"
							loading="lazy"
							alt="Photo by Magicle"
							class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110"
						/>
					</a>

					<div class="flex flex-col gap-2 p-4 lg:p-6">
						<h2 class="text-xl font-bold text-gray-800">
							<a href="#" class="transition duration-100 hover:text-indigo-500 active:text-indigo-600">
								<span class="text-indigo-500">AmazonPrime</span>
							</a>
						</h2>
						<span class="text-sm text-gray-400">March 15, 2021</span>
						<p class="text-gray-500">This is a section of some simple filler text, also known as placeholder text.</p>
					</div>
				</div>
				<!-- article - end -->

				<!-- article - start -->
				<div class="flex flex-col items-center overflow-hidden rounded-lg border md:flex-row">
					<a href="#" class="group relative block h-48 w-full shrink-0 self-start overflow-hidden bg-gray-100 md:h-full md:w-32 lg:w-48">
						<img
							src="https://images.unsplash.com/photo-1610465299996-30f240ac2b1c?auto=format&q=75&fit=crop&w=600"
							loading="lazy"
							alt="Photo by Martin Sanchez"
							class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110"
						/>
					</a>

					<div class="flex flex-col gap-2 p-4 lg:p-6">
						<h2 class="text-xl font-bold text-gray-800">
							<a href="#" class="transition duration-100 hover:text-indigo-500 active:text-indigo-600">
								<span class="text-indigo-800">U-next</span>
							</a>
						</h2>
						<span class="text-sm text-gray-400">January 27, 2021</span>
						<p class="text-gray-500">This is a section of some simple filler text, also known as placeholder text.</p>
					</div>
				</div>
				<!-- article - end -->
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
