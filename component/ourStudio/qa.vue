<template>
	<div class="bg-white py-6 sm:py-8 lg:py-12 w-full sm:w-3/4 md:w-4/5 mx-auto">
		<div class="mt-4 mx-auto max-w-screen-2xl px-4 md:px-8">
			<div class="hs-accordion-group">
				<p class="mb-2 text-center font-semibold text-emerald-500 md:mb-3 lg:text-lg">QA</p>
				<!-- <h2 class="mb-4 text-center text-2xl font-bold text-gray-800 md:mb-6 lg:text-3xl">問い合わせ</h2> -->

				<form @submit.prevent="submitForm">
					<div class="block md:flex">
						<!-- Name -->
						<div class="w-full md:w-1/2">
							<label for="username" class="block text-sm font-medium leading-6 text-gray-900">Name</label>
							<div class="mt-2">
								<div class="flex rounded-md shadow-sm ring-1 ring-inset ring-gray-300 focus-within:ring-2 focus-within:ring-inset focus-within:ring-emerald-600 sm:max-w-md">
									<input
										type="text"
										name="username"
										id="username"
										autocomplete="username"
										class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6"
										placeholder="janesmith"
									/>
								</div>
							</div>
						</div>
						<!-- Email -->
						<div class="w-full md:w-1/2">
							<label for="email" class="block text-sm font-medium leading-6 text-gray-900">Email</label>
							<div class="mt-2">
								<div class="flex rounded-md shadow-sm ring-1 ring-inset ring-gray-300 focus-within:ring-2 focus-within:ring-inset focus-within:ring-emerald-600 sm:max-w-md">
									<input
										type="text"
										name="email"
										id="email"
										autocomplete="email"
										class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6"
										placeholder="scs@example.com"
									/>
								</div>
							</div>
						</div>
					</div>
					<!-- Context -->
					<div class="col-span-full">
						<label for="about" class="block text-sm font-medium leading-6 text-gray-900">About</label>
						<div class="mt-2">
							<textarea
								id="about"
								name="about"
								rows="3"
								class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-emerald-600 sm:text-sm sm:leading-6"
							></textarea>
						</div>
					</div>
					<!-- Submitボタン -->
					<div class="text-center w-full mt-4">
						<button class="text-emerald-500 hover:text-white bg-white hover:bg-emerald-600 transition border-2 border-solid border-emerald-500 font-semibold py-4 px-20 text-xs rounded-md">
							Send
						</button>
					</div>
				</form>
			</div>
		</div>
	</div>
</template>

<script></script>
