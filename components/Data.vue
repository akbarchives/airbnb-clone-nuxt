<script setup>
const url = 'https://hotels4.p.rapidapi.com/v2/get-meta-data';
const options = {
  method: 'GET',
  headers: {
    'X-RapidAPI-Key': '8d3c9fe54bmshb0447e3c2fb2617p1402d9jsn95c5fa55e986',
    'X-RapidAPI-Host': 'hotels4.p.rapidapi.com',
  },
};

const { data: hotels } = await useFetch(url, options);
// try {
//   const response = await fetch(url, options);
//   const result = await response.text();
//   console.log(result);
// } catch (error) {
//   console.error(error);
// }

console.log(hotels);
</script>

<template>
  <div class="flex flex-row flex-wrap">
    <div
      class="basis-1"
      v-for="h in hotels"
    >
      {{ h }}
    </div>
  </div>
</template>
