<script setup>
import { ref } from 'vue';
import Slides from './components/Slides.vue'

const items = ref(
  Array.from({ length: 10 }, (_, index) => index + 1)
  .map(index => ({
    id: index,
    title: `Slide ${index}`,
    content: `This is the ${index} slide`,
  }))
);

</script>

<template>
  <main class="flex flex-col items-center justify-center h-screen w-screen">
    <Slides :items="items" />
  </main>
  <pre>{{ items }}</pre>
</template>

<style scoped>

</style>
