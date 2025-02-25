<template>
  <RouterLink :to="pkmnPath" class="card"
    ><h2>
      {{ props.mon.name }}
    </h2>
    <h3>{{ props.index }}</h3>
  </RouterLink>
</template>

<script setup>
import { defineProps, computed } from 'vue'

const props = defineProps(['mon', 'index'])

const pkmnPath = computed(() => {
  return `/pokemon/${props.index}`
})
</script>

<style scoped></style>
