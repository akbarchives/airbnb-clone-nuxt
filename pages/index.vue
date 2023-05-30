<template>
  <NuxtLayout :name="layout">
    <div
      class="custom-container mx-auto mb-36 flex max-w-screen-2xl flex-row flex-wrap gap-y-6"
    >
      <Card
        v-for="p in products"
        :title="p.title"
        :description="p.description"
        :category="p.category"
        :price="p.price"
        :image="p.image"
      />
    </div>
  </NuxtLayout>
</template>

<script setup>
const layout = 'custom';
const { data: products } = useFetch('https://fakestoreapi.com/products');
console.log(products);
</script>
