<template>
  <div>
    <h2 v-for="animal in animals" :key="animal">{{ animal }}</h2>
    <!-- its like a for each -->
  </div>
</template>

<script setup>
const animals = ['zebra', 'panda', 'cat', 'whale']
console.log('jfhakdfksdjh')
</script>

<style scoped></style>

<!--vbase-3-setup-->
