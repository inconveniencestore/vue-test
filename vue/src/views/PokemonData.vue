<template>
  <div>fasfdsaf</div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import { useRoute } from 'vue-router' //use route extract data from it

const route = useRoute()
const pokemon = ref('')
async function getPokemon() {
  let res = await fetch(`https://pokeapi.co/api/v2/pokemon/${route.params.index}`)
  let data = await res.json()
  pokemon.value = data
}

onMounted(() => {
  getPokemon()
})
</script>

<style scoped></style>
