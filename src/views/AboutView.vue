<script setup>
import { ref, defineProps } from 'vue'

defineProps({
  msg: {
    type: String,
    required: true
  },
})

const value = ref(0.4)
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    
    <v-slider
      v-model="value"
      :min="0"
      :max="1"
      :step="0.2"
      thumb-label
    ></v-slider>

  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
