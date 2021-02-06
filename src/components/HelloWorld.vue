<template>
  <h1>John's Things</h1>

  <ul class="things">
    <li v-for="i in 21" :key="i">
      <a :href="`#test${i}`">
        Word {{i}}
      </a>
    </li>
  </ul>



</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })
</script>

<style scoped>
a {
  color: #42b983;
  background-color: aliceblue;
  margin: 5px;
  height: 200px;
  widows: 200px;
  display: grid;
  place-items: center;
  text-decoration: none;
  font-weight: bold;
}

a:hover {
  background-color: lightblue;
  color: black;
}

.things {
  list-style-type: none;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
</style>