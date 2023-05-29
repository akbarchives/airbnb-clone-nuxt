<template>
  <div class="font-sans">
    <div
      class="hidden bg-slate-100 px-6 px-6 py-4 align-middle sm:flex sm:justify-between sm:px-8"
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
    <Navbar class="z-100 sticky top-0 mx-auto border" />

    <!-- Content -->
    <Content class="z-10" />
    <Data />
    <!-- <slot /> -->

    <!-- Footer -->
    <!-- <footer>This is Footer</footer> -->
  </div>
</template>
