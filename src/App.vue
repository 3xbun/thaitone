<template>
  <div>
    <Header />
    <div class="colors">
      <div v-for="color in Thaitone">
        <ColorCard :color="color" />
      </div>
    </div>
  </div>
</template>

<script setup>
import Header from "./components/Header.vue";
import ColorCard from "./components/ColorCard.vue"

import Thaitone from "./data/Thaitone.json"
</script>

<style scoped>
.colors {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  max-width: 600px;
  margin: auto;
  gap: 1em;
  padding-bottom: 3em;
}
</style>