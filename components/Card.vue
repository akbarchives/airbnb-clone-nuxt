<template>
  <NuxtLink
    to=""
    class="card group min-w-fit max-w-lg rounded-2xl border bg-white hover:bg-slate-100"
  >
    <!-- class="card flex basis-full flex-col overflow-hidden border border-pink-500 sm:basis-1/2 sm:pr-4 md:basis-1/3 lg:basis-1/4" -->
    <div class="group overflow-hidden rounded-t-2xl">
      <img
        class="aspect-video w-full overflow-hidden object-cover object-top duration-1000 ease-out group-hover:scale-105 sm:aspect-square"
        alt=""
        :src="img"
      />
      <!-- src="~/assets/img/content-img/photo-3.webp" -->
    </div>
    <div class="p-4">
      <div class="flex flex-row justify-between">
        <h1
          class="line-clamp-2 basis-10/12 text-lg font-semibold sm:basis-3/4 lg:basis-10/12"
        >
          {{ name }}
        </h1>
        <h1 class="basis-2/12 sm:basis-1/4 lg:basis-2/12">
          <span class="text-lg">&#9733;</span> 4.71
        </h1>
      </div>
      <h1 class="font-medium text-slate-800">
        {{ category ? category : 'category...' }}
      </h1>
      <h1 class="my-2 line-clamp-2 font-normal text-slate-600">
        {{ description ? description : 'description...' }}
      </h1>
      <h1 class="text-lg font-semibold">USD {{ price ? price : '450' }}</h1>
    </div>
  </NuxtLink>
</template>

<script setup>
const props = defineProps({
  name: String,
  category: String,
  description: String,
  img: String,
  price: Number,
});
</script>
