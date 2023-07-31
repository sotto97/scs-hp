<template>
	<div class="bg-white py-6 sm:py-8 lg:py-12 w-full sm:w-3/4 mx-auto">
		<div class="mt-4 mx-auto max-w-screen-2xl px-4 md:px-8">
			<h2 class="mb-4 text-center text-2xl font-bold text-gray-800 md:mb-6 lg:text-3xl">所属アーティスト</h2>
			<div class="overflow-x-auto whitespace-nowrap pt-6">
				<div class="inline-block h-auto w-6/12">
					<div class="bg-black h-48 rounded-lg mr-2 shadow-xl">
						<img src="../img/sotto.jpg" class="h-48 mx-auto rounded-lg" alt="" />
					</div>
					<p class="font-semibold pt-2 text-lg">Sotto<span class="pl-2 text-xs text-indigo-500">DJ/Engineer</span></p>
				</div>
				<div class="inline-block h-auto w-6/12">
					<div class="bg-black h-48 rounded-lg mr-2 shadow-xl">
						<img src="../img/sotto.jpg" class="h-48 mx-auto rounded-lg" alt="" />
					</div>
					<p class="font-semibold pt-2 text-lg">David<span class="pl-2 text-xs text-indigo-500">Photographer</span></p>
				</div>
				<div class="inline-block h-auto w-6/12">
					<div class="bg-black h-48 rounded-lg mr-2 shadow-xl">
						<img src="../img/sotto.jpg" class="h-48 mx-auto rounded-lg" alt="" />
					</div>
					<p class="font-semibold pt-2 text-lg">Atrax<span class="pl-2 text-xs text-indigo-500">Barista</span></p>
				</div>
			</div>
			<div class="w-full mt-4 text-center align-center">
				<button class="text-indigo-500 hover:text-white bg-white hover:bg-indigo-600 transition border-2 border-solid border-indigo-500 font-semibold py-4 px-20 text-xs rounded-md">
					View Detail
				</button>
			</div>
		</div>
	</div>
</template>

<script>
module.exports = {
	data: function () {
		return {
			name: "ArtistComponent",
		};
	},
};
</script>
