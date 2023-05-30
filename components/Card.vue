<template>
  <NuxtLink
    to="/details"
    class="card basis-full overflow-hidden sm:basis-1/2 sm:pr-4 md:basis-1/3 lg:basis-1/4"
  >
    <div class="group overflow-hidden rounded-2xl">
      <img
        class="aspect-square w-full overflow-hidden object-cover duration-1000 ease-out group-hover:scale-105"
        alt=""
        :src="image"
      />
      <!-- src="~/assets/img/content-img/8ea33b3d-f2aa-4098-82a9-759486eae1d7.webp" -->
    </div>
    <div class="flex items-center justify-between pt-2 text-sm">
      <h1 class="font-bold tracking-tighter">
        {{ title }}
      </h1>
      <div><span class="text-lg">&#9733;</span> 4.71</div>
    </div>
    <h2 class="text-base font-thin text-slate-500 sm:text-sm">
      <!-- 11 min walk to the beach -->
      {{ category }}
    </h2>
    <h2 class="truncate text-base font-thin text-slate-500 sm:text-sm">
      <!-- 5 nights, Oct 29 - Nov 3 -->
      {{ description }}
    </h2>
    <h2 class="text-sm font-medium tracking-tighter underline sm:text-sm">
      <!-- <span class="font-bold">Rp 26,147,085 </span> total before taxes -->
      USD {{ price }}
    </h2>
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
