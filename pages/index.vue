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
</script>
