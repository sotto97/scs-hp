<template>
	<div>
		<div class="flex">
			<div class="w-1/2">
				<h1 class="font-semibold text-xl"><span class="border-l-4 border-indigo-500 mr-2"></span>所属アーティスト</h1>
			</div>
			<div class="w-1/2 text-right align-center">
				<button class="text-indigo-500 hover:text-white bg-white hover:bg-indigo-600 transition border-2 border-solid border-indigo-500 py-2 px-8 text-xs rounded-md">View Detail</button>
			</div>
		</div>
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
