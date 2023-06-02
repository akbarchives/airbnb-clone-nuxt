<script setup>
import { ArrowUpOnSquareIcon, HeartIcon } from '@heroicons/vue/24/outline';
const layout = 'details';
const route = useRoute();
console.log(route.params.id);

// const id = route.params.id;
// const product = products[id - 1];

const { data: product } = await useFetch(
  'https://dummyjson.com/products/' + route.params.id
);

console.log(product);
</script>

<template>
  <NuxtLayout :name="layout">
    <div class="bg-white">
      <div class="mx-auto w-full max-w-screen-2xl pb-20 pt-10">
        <div
          class="flex min-w-max flex-col items-start justify-between px-6 sm:px-8"
        >
          <!-- title -->
          <h1 class="text-2xl font-bold leading-none">
            {{ product.title }}
          </h1>

          <div class="flex w-full flex-row justify-between">
            <div class="flex flex-row items-center gap-2">
              <p><span>&#9733;</span> {{ product.rating }}</p>
              <p class="text-center text-xs">•</p>
              <nuxt-link
                to=""
                class="underline"
                ><p>180 reviews</p></nuxt-link
              >
              <p class="text-center text-xs">•</p>
              <p>Superhost</p>
              <p class="text-center text-xs">•</p>
              <NuxtLink
                to=""
                class="underline"
                >Kecamatan Kuta Utara, Bali, Indonesia</NuxtLink
              >
            </div>

            <div class="flex flex-row items-center gap-4">
              <NuxtLink
                to="/"
                class="rounded-md p-2 hover:bg-slate-100"
                ><ArrowUpOnSquareIcon
                  class="inline-block h-6 w-6 align-middle"
                />
                <span class="pl-2">Share</span></NuxtLink
              >
              <NuxtLink
                to="/"
                class="rounded-md p-2 hover:bg-slate-100"
                ><HeartIcon class="inline-block h-6 w-6 align-middle" /><span
                  class="pl-2"
                  >Save</span
                ></NuxtLink
              >
            </div>
          </div>
          <!-- image display -->

          <ImageDisplay
            class="mt-6"
            :thumbnail="product.images[0]"
            :img1="product.images[1]"
            :img2="product.images[2]"
            :img3="product.images[3]"
            :img4="product.images[4]"
          />

          <!-- details -->
          <div class="w-full bg-pink-200 py-12">
            <!-- left -->
            <div
              class="sticky top-32 inline-block h-[500px] w-1/2 bg-purple-400"
            >
              left
            </div>
            <!-- right -->
            <div class="inline-block h-[500px] w-1/2 bg-yellow-400">right</div>
          </div>

          <h1 class="my-64 w-full border-t-2">sadsa</h1>
        </div>
      </div>
    </div>
  </NuxtLayout>
</template>
