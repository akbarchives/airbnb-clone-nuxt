<template>
  <NuxtLayout :name="layout">
    <div
      class="custom-container mx-auto mb-36 grid max-w-screen-2xl grid-cols-1 gap-4 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4"
    >
      <div v-for="p in products2.products">
        <CardSwipe
          :title="p.title"
          :rating="p.rating"
          :category="p.category"
          :description="p.description"
          :price="p.price"
          :brand="p.brand"
          :thumbnail="p.thumbnail"
          :img1="p.images[0]"
          :img2="p.images[1]"
        />
      </div>
    </div>
  </NuxtLayout>

  <!-- <div v-for="p in produk">
    {{ p.id }}
  </div> -->
  <!-- <div v-for="p in products2.products">
    {{ p.title }}

    <img
      :src="p.images[0]"
      alt=""
    />
  </div> -->

  <!-- <NuxtLayout :name="layout">
    <div
      class="custom-container mx-auto mb-36 grid max-w-screen-2xl grid-cols-1 gap-4 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4"
    >
      <Card
        v-for="p in products2.products"
        :title="p.title"
        :description="p.description"
        :category="p.category"
        :price="p.price"
        :image="p.images[0]"
      />
    </div>
  </NuxtLayout> -->
</template>

<script setup>
import axios from 'axios';
const layout = 'custom';

const { data: products } = useFetch('https://fakestoreapi.com/products');
console.log(products);

const { pending, data: products2 } = useFetch(
  'https://dummyjson.com/products',
  { lazy: true }
);
console.log(products2);

const { data: movie } = useFetch(
  'https://api.themoviedb.org/3/movie/popular?api_key=35d428792ace5959fdc3f64e2ecc08b6'
);
console.log(movie);
// const getProducts = async () => {
//   const product = await axios.get('https://dummyjson.com/products');
//   // console.log(product.data.results);
//   return product.data.products;
// };
// const produk = getProducts();
// console.log(produk);
// console.log(getProducts());
// getProducts();
</script>
