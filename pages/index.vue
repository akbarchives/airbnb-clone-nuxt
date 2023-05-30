<template>
  <NuxtLayout :name="layout">
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
  </NuxtLayout>
</template>

<script setup>
// You might choose this based on an API call or logged-in status
const layout = 'custom';
const url = 'https://hotels4.p.rapidapi.com/properties/v2/list';
const options = {
  method: 'POST',
  headers: {
    'content-type': 'application/json',
    'X-RapidAPI-Key': '8d3c9fe54bmshb0447e3c2fb2617p1402d9jsn95c5fa55e986',
    'X-RapidAPI-Host': 'hotels4.p.rapidapi.com',
  },
  body: {
    currency: 'USD',
    eapid: 1,
    locale: 'en_US',
    siteId: 300000001,
    destination: {
      regionId: '6054439',
    },
    checkInDate: {
      day: 10,
      month: 10,
      year: 2022,
    },
    checkOutDate: {
      day: 15,
      month: 10,
      year: 2022,
    },
    rooms: [
      {
        adults: 2,
        children: [{ age: 5 }, { age: 7 }],
      },
    ],
    resultsStartingIndex: 0,
    resultsSize: 200,
    sort: 'PRICE_LOW_TO_HIGH',
    filters: {
      price: { max: 150, min: 100 },
    },
  },
};

try {
  const response = await fetch(url, options);
  const result = await response.text();
  console.log(result);
} catch (error) {
  console.error(error);
}
</script>
