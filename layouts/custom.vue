<template>
  <div class="font-sans">
    <div class="bg-slate-100">
      <div
        class="mx-auto hidden max-w-screen-2xl px-6 py-4 align-middle sm:flex sm:justify-between sm:px-8"
      >
        <div class="font-bold sm:text-base md:text-lg">
          Introducing Airbnb Rooms and 50+ features
        </div>
        <div class="flex justify-end text-sm tracking-tight">
          <button
            class="px-4 duration-200 hover:underline hover:underline-offset-2 active:scale-90 active:duration-200"
          >
            <img
              class="inline w-12 rounded-md"
              src="~/assets/img/newFeature.png"
              alt=""
            />
            <span class="px-2">Watch the Rooms film</span>
          </button>
          <span class="border-px border-l py-2"></span>
          <button
            class="pl-4 duration-200 hover:underline hover:underline-offset-2 active:scale-90 active:duration-200"
          >
            Learn more
          </button>
        </div>
      </div>
    </div>
    <div class="navbar sticky top-0">
      <Navbar />
      <NavbarCategories />
    </div>

    <!-- Container-->
    <slot />

    <!-- Footer -->
    <Footer class="" />
  </div>
</template>

<style>
.navbar {
  z-index: 100;
}
</style>
