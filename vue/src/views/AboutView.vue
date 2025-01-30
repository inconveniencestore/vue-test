<template>
  <div>
    <NewList />
    <h2>{{ animal.name }}</h2>
    <img :src="animal.image" alt="" />
  </div>
</template>

<script setup>
import NewList from '../components/NewList.vue'
/* passes in information */
defineProps({
  animal: Object,
})
</script>

<style scoped></style>
