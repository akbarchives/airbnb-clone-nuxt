<template>
  <NuxtLayout :name="layout">
    <h1 class="text-2xl font-bold leading-none">
      Designer Luxury Bali Villa In Canggu 3min To Beach
    </h1>

    <div class="flex w-full flex-row justify-between">
      <div class="flex flex-row items-center gap-2">
        <p><span>&#9733;</span> 4.71</p>
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
          ><ArrowUpOnSquareIcon class="inline-block h-6 w-6 align-middle" />
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
    <ImageDisplay />
  </NuxtLayout>
</template>

<script setup>
import { ArrowUpOnSquareIcon, HeartIcon } from '@heroicons/vue/24/outline';
const layout = 'details';
</script>
