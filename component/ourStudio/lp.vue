<template>
  <!-- 参考はこれ；https://flowrift.com/c/full-page/6tdav?view=preview -->
  <div class="h-screen bg-white pb-6 sm:pb-8 lg:pb-12">
    <div class="mx-auto h-screen pb-24 max-w-screen-2xl px-4 md:px-8">
      <!-- <header class="mb-8 flex items-center justify-between py-4 md:mb-12 md:py-8 xl:mb-16">
				<a href="/" class="inline-flex items-center gap-2.5 text-2xl font-bold md:text-3xl" aria-label="logo">
					<img src="../img/scs_logo_black.png" class="h-auto w-8" />
					<span class="text-black-800">SCS</span>
				</a>
			</header> -->
      <section
        class="h-full mt-2 sm:mt-20 flex flex-col justify-between gap-6 sm:gap-10 md:gap-16 lg:flex-row"
      >
        <!-- content - start -->
        <div
          class="flex flex-col justify-center sm:text-center lg:py-12 lg:text-left xl:w-4/12 xl:py-24"
        >
          <p
            class="mb-4 font-semibold text-emerald-500 md:mb-6 md:text-lg xl:text-xl"
          >
            Sotto Creative Studio
          </p>
          <h1
            class="text-black-800 mb-8 text-3xl font-bold sm:text-5xl md:mb-12 md:text-6xl"
          >
            Believing in growth potential
          </h1>
          <p
            class="mb-8 leading-relaxed text-gray-500 md:mb-12 lg:w-4/5 xl:text-lg"
          >
            Let’s challenge, grow, and create the future together. We are fully
            committed to supporting your success.
          </p>
          <div
            class="gap-2.5 flex sm:flex-row sm:justify-center lg:justify-start w-full"
          >
            <div class="w-1/2 md:w-auto">
              <a
                href="#"
                class="rounded-lg bg-emerald-500 block md:inline px-8 py-4 text-center text-sm font-semibold outline-none transition duration-100 hover:bg-emerald-600 active:bg-emerald-700 md:text-base"
              >
                <span class="text-white">Join Us</span>
              </a>
            </div>
            <div class="w-1/2 md:w-auto">
              <a
                href="#"
                class="rounded-lg bg-gray-200 block md:inline px-8 py-4 text-center text-sm font-semibold transition duration-100 hover:bg-gray-300 active:text-gray-700 md:text-base"
              >
                <span class="text-gray-500">Career</span>
              </a>
            </div>
          </div>
        </div>
        <!-- content - end -->

        <!-- image - start -->
        <div
          class="overflow-hidden rounded-lg bg-gray-100 shadow-lg lg:h-auto xl:w-4/12"
        >
          <img
            src="../img/sotto.jpg"
            loading="lazy"
            alt="Photo by Fakurian Design"
            class="h-56 sm:h-60 md:h-96 lg:h-full w-full object-cover object-center"
          />
        </div>
        <!-- image - end -->

        <!-- social - start -->
        <div
          class="mt-4 flex items-center justify-center gap-4 sm:mt-16 lg:justify-start xl:w-4/12"
        >
          <span
            class="text-sm font-semibold uppercase tracking-widest text-gray-400 sm:text-base"
            >Social</span
          >
          <span class="h-px w-12 bg-gray-200"></span>
          <div class="flex gap-4">
            <a
              href="https://www.instagram.com/xiacun_youjie/"
              target="_blank"
              class="text-gray-400 transition duration-100 hover:text-emerald-500 active:text-emerald-600"
            >
              <svg
                class="h-5 w-5"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"
                />
              </svg>
            </a>
            <a
              href="https://github.com/sotto97"
              target="_blank"
              class="text-gray-400 transition duration-100 hover:text-emerald-500 active:text-emerald-600"
            >
              <svg
                class="h-5 w-5"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
                />
              </svg>
            </a>
            <a
              href="#"
              target="_blank"
              class="text-gray-400 transition duration-100 hover:text-emerald-500 active:text-emerald-600"
            >
              <svg
                class="h-5 w-5"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
                xmlns="http://www.w3.org/2000/svg"
              ></svg>
            </a>
          </div>
        </div>
        <!-- social - end -->
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
