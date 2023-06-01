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
          <div class="sticky right-0 top-64 flex w-full pt-96">
            <div class="basis-7/12">
              <h1 class="h-screen">
                Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure,
                accusantium natus! Dolore delectus minima numquam!
              </h1>
            </div>
            <div class="basis-5/12">2</div>
          </div>
        </div>
      </div>
    </div>
  </NuxtLayout>
</template>
