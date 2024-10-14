<script setup>
import { ref } from 'vue';
defineProps(['color'])
// const color = ref(
//   {
//     "colorName": "เขียวน้ำไหล",
//     "hex": "#00968f",
//     "desc": {
//       "th": "สีเขียวฟ้าน้ำทะเลใส",
//       "en": "Clear teal green"
//     }
//   })
</script>

<template>
  <div class="color-card" :style="{ borderColor: color.hex }">
    <div class="color" :style="{ backgroundColor: color.hex }"></div>
    <p><strong class="name">{{ color.colorName }}</strong></p>
    <div class="subtitle">
      <p>{{ color.hex }}</p>
      <!-- <p> {{ color.desc.th }}</p> -->
    </div>
  </div>
</template>

<style scoped>
.color-card {
  margin: 2em auto 0;
  width: 40vw;
  padding: .3em;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  transition: all 0.3s cubic-bezier(.25, .8, .25, 1);
  border: solid .5em black;
  max-width: 150px;
}

.color {
  width: 100%;
  height: 12vh;
  margin-bottom: .5em;
}

.subtitle {
  font-weight: 300;
  font-size: .7em;
}
</style>