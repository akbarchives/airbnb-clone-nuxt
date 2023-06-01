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
    <div class="navbar sticky bottom-0">
      <!-- footer -->
    </div>
    <!-- <Footer class="footer fixed bottom-0" /> -->
  </div>
</template>

<style>
.navbar {
  z-index: 100;
}

.footer {
  z-index: 999;
  background: #000;
}
</style>
