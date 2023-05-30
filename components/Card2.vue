<template>
  <NuxtLink
    to="/details"
    class="card basis-full overflow-hidden sm:basis-1/2 sm:pr-4 md:basis-1/3 lg:basis-1/4"
  >
    <div
      class="flex basis-full flex-col overflow-hidden rounded-2xl border bg-yellow-300 sm:basis-1/2 md:basis-1/3 lg:basis-1/4"
    >
      <div class="group">
        <img
          class="aspect-video w-full overflow-hidden object-cover duration-1000 ease-out group-hover:scale-105 sm:aspect-square"
          alt=""
          :src="image"
        />
        <!-- src="~/assets/img/content-img/photo-3.webp" -->
      </div>
      <div class="flex h-full flex-col justify-stretch py-4">
        <div class="flex flex-row">
          <h1 class="basis-10/12 truncate text-lg font-semibold">
            {{ title }}
          </h1>
          <h1 class="basis-2/12"><span class="text-lg">&#9733;</span> 4.71</h1>
        </div>
        <h1 class="font-medium text-slate-800">{{ category }}</h1>
        <h1 class="my-2 line-clamp-2 font-medium text-slate-600">
          {{ description }}
        </h1>
        <h1 class="text-lg font-semibold">USD {{ price }}</h1>
      </div>
    </div>
  </NuxtLink>
</template>

<script setup>
const props = defineProps({
  title: String,
  category: String,
  description: String,
  image: String,
  price: Number,
});
</script>
