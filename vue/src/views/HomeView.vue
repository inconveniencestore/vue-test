<!-- <template>
  <div class="aaaa">
    <h1>{{ count }}</h1>
    <button @click="increment">Click Me</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
let count = ref(0)

function increment() {
  count.value++
}
</script>

<style scoped></style>
 -->

<template>
  <!--tmr make this into a component to pass the props into-->
  <PokeDisplay v-for="(mon, index) in pokemon" :mon="mon" :index="index + 1"></PokeDisplay>
</template>

<script setup>
import PokeDisplay from '@/components/PokeDisplay.vue'
import { ref, onMounted } from 'vue'
const pokemon = ref('')

//in actual project, use if then statements to make sure the async is 200
async function getPokemon() {
  let res = await fetch('https://pokeapi.co/api/v2/pokemon/?limit=151')
  let data = await res.json()
  pokemon.value = data.results
}

onMounted(() => {
  getPokemon()
})
</script>

<style scoped></style>
