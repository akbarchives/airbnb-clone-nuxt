<template>
  <div
    class="grid h-[300px] w-full gap-2 overflow-hidden rounded-2xl border sm:grid-flow-col sm:grid-rows-2"
  >
    <div class="col-span-2 row-span-2 overflow-hidden">
      <img
        class="h-full w-full object-cover object-center transition-all duration-500 ease-in-out hover:scale-105 hover:brightness-[90%]"
        :src="thumbnail"
        alt=""
      />
    </div>

    <div class="overflow-hidden">
      <img
        class="h-full w-full object-cover object-center transition-all duration-500 ease-in-out hover:scale-105 hover:brightness-[90%]"
        :src="img1"
        alt=""
      />
    </div>
    <div class="overflow-hidden">
      <img
        class="h-full w-full object-cover object-center transition-all duration-500 ease-in-out hover:scale-105 hover:brightness-[90%]"
        :src="img2"
        alt=""
      />
    </div>
    <div class="overflow-hidden">
      <img
        class="h-full w-full object-cover object-center transition-all duration-500 ease-in-out hover:scale-105 hover:brightness-[90%]"
        :src="img3"
        alt=""
      />
    </div>
    <div class="overflow-hidden">
      <img
        class="h-full w-full object-cover object-center transition-all duration-500 ease-in-out hover:scale-105 hover:brightness-[90%]"
        :src="img4"
        alt=""
      />
    </div>
    <!-- <img
      class="h-full w-full object-cover object-left-top"
      :src="img1"
      alt=""
    /> -->

    <!-- <img
      class="col-span-2 row-span-2 h-full"
      src="~/assets/img/content-img/photo-1.webp"
      alt=""
    />  <img
      src="~/assets/img/content-img/photo-2.webp"
      alt=""
    /> 
    <img
      src="~/assets/img/content-img/photo-4.webp"
      alt=""
    />
    <img
      src="~/assets/img/content-img/photo-5.webp"
      alt=""
    /> -->
  </div>
</template>
<script>
export default {
  props: {
    thumbnail: String,
    img1: String,
    img2: String,
    img3: String,
    img4: String,
  },
};
</script>
<style>
img {
  filter: grayscale(30%);
}
img:hover {
  filter: grayscale(0%);
}
</style>
