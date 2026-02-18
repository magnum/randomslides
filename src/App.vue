<script setup>
import { ref } from 'vue';
import Slides from './components/Slides.vue'

const items = ref([
  {
    id: 1,
    title: 'Probabilistic',
    content: 'content',
  },
  {
    id: 2,
    title: 'Learning',
    content: 'content',
  },
  {
    id: 3,
    title: 'Skill',
    content: 'content',
  },
  {
    id: 4,
    title: 'Inefficiency',
    content: 'content',
  },
  {
    id: 5,
    title: 'Agent',
    content: 'content',
  },
  {
    id: 6,
    title: 'Human',
    content: 'content',
  },
  {
    id: 7,
    title: 'Ai slop',
    content: 'content',
  },
  {
    id: 8,
    title: "Jobs",
    content: 'content',
  },
  {
    id: 9,
    title: 'rag',
    content: 'content',
  },
]);

</script>

<template>
  <main class="flex flex-col items-center justify-center h-screen w-screen">
    <Slides :items="items" />
  </main>
  <pre>{{ items }}</pre>
</template>

<style scoped>

</style>
