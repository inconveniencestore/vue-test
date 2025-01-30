<template>
  <div>
    <!--<h2 v-for="animal in animals" :key="animal">{{ animal }}</h2>-->
    <!-- its like a for each -->
    <AnimalCard v-for="animal in animals" :key="animal.name" />
  </div>
</template>

<script setup>
/* import AnimalCard from '../components/AnimalCard.vue' */
//const animals = {'walrus', "cat"}
console.log('jfhakdfksdjh')
</script>

<style scoped></style>

<!--vbase-3-setup-->
