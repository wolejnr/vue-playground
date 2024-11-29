<script setup>
import Garage from './components/TheGarage.vue';
import mydata from './data/cardata.json'
</script>

<template>
  <main>
    <Garage :data="mydata" />
  </main>
</template>

<style scoped>


@media (min-width: 1024px) {
  
}
</style>
