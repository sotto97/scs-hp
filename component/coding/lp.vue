<template>
	<!-- 参考はこれ；https://flowrift.com/c/full-page/6tdav?view=preview -->
	<div class="bg-white pb-6 sm:pb-8 lg:pb-12">
		<div class="mx-auto max-w-screen-2xl px-4 md:px-8">
			<header class="mb-8 flex items-center justify-between py-4 md:mb-12 md:py-8 xl:mb-16">
				<!-- logo - start -->
				<a href="/" class="inline-flex items-center gap-2.5 text-2xl font-bold md:text-3xl" aria-label="logo">
					<svg width="95" height="94" viewBox="0 0 95 94" class="h-auto w-6 text-indigo-500" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
						<path d="M96 0V47L48 94H0V47L48 0H96Z" />
					</svg>
					<span class="text-black-800">SCS</span>
				</a>
			</header>

			<section class="flex flex-col justify-between gap-6 sm:gap-10 md:gap-16 lg:flex-row">
				<!-- content - start -->
				<div class="flex flex-col justify-center sm:text-center lg:py-12 lg:text-left xl:w-5/12 xl:py-24">
					<p class="mb-4 font-semibold text-indigo-500 md:mb-6 md:text-lg xl:text-xl">Very proud to introduce</p>
					<h1 class="text-black-800 mb-8 text-4xl font-bold sm:text-5xl md:mb-12 md:text-6xl">Revolutionary way to build the web</h1>
					<p class="mb-8 leading-relaxed text-gray-500 md:mb-12 lg:w-4/5 xl:text-lg">
						This is a section of some simple filler text, also known as placeholder text. It shares some characteristics of a real written text but is random.
					</p>
					<div class="gap-2.5 sm:flex-row sm:justify-center lg:justify-start">
						<a href="#" class="rounded-lg bg-indigo-500 px-8 py-4 text-center text-sm font-semibold outline-none transition duration-100 hover:bg-indigo-600 active:bg-indigo-700 md:text-base">
							<span class="text-white">Join Us</span>
						</a>
						<a href="#" class="rounded-lg bg-gray-200 px-8 py-4 text-center text-sm font-semibold transition duration-100 hover:bg-gray-300 active:text-gray-700 md:text-base">
							<span class="text-gray-500">Career</span>
						</a>
					</div>
				</div>
				<!-- content - end -->

				<!-- image - start -->
				<div class="h-48 overflow-hidden rounded-lg bg-gray-100 shadow-lg lg:h-auto xl:w-5/12">
					<img src="../img/sotto.jpg" loading="lazy" alt="Photo by Fakurian Design" class="h-full w-full object-cover object-center" />
				</div>
				<!-- image - end -->
			</section>
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

<style>
.v-application a {
	color: inherit; /* インヘリットすることで親要素の色を継承 */
	text-decoration: none; /* 下線をなくす */
}
</style>
