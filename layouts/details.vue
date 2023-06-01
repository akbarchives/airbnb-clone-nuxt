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
      <Footer />
    </div>
  </div>
</template>

<style></style>
