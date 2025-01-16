<template>
  <form name="login-form" @submit.prevent="login(forom)">
    <div class="username">
      <label for="username">username: </label>
      <input type="text" v-model="forom.username" />
    </div>
    <div class="password">
      <label for="password">password: </label>
      <input type="password" v-model="forom.password" />
    </div>
    <button @submit="console.log(forom.username, forom.password)">submit</button>
  </form>
  <h2 v-if="cat">A</h2>
  <h2 v-else>B</h2>
</template>

<script setup>
import { reactive } from 'vue'

const forom = reactive({
  username: '',
  password: '',
})
function login(forom) {
  console.log(`${forom.username}, ${forom.password}`)
}
reactive
const cat = false
</script>

<style scoped></style>

<!--vbase-3-setup-->
<!--we use composition api-->
