<template>
  <div
    class="grid w-full grid-flow-col grid-rows-2 gap-3 overflow-hidden rounded-2xl"
  >
    <img
      class="col-span-2 row-span-2 h-full"
      src="~/assets/img/content-img/photo-1.webp"
      alt=""
    />
    <img
      src="~/assets/img/content-img/photo-2.webp"
      alt=""
    />
    <img
      src="~/assets/img/content-img/photo-3.webp"
      alt=""
    />
    <img
      src="~/assets/img/content-img/photo-4.webp"
      alt=""
    />
    <img
      src="~/assets/img/content-img/photo-5.webp"
      alt=""
    />
  </div>
</template>

<style>
img {
  filter: grayscale(30%);
}
img:hover {
  filter: grayscale(0%);
}
</style>
