<template>
  <div class="font-sans">
    <div class="navbar sticky top-0">
      <Navbar />
    </div>

    <!-- Content -->
    <div class="flex flex-col px-6 pt-6 sm:px-8">
      <!-- Container-->
      <div
        class="custom-container mx-auto mb-36 flex max-w-screen-2xl flex-row flex-wrap gap-y-6"
      >
        <!-- Content -->
        <slot />
      </div>
    </div>

    <!-- Footer -->
    <Footer class="fixed bottom-0" />
  </div>
</template>

<style>
.navbar {
  z-index: 100;
}
</style>
