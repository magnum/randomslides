<script setup>
import { ref } from 'vue';

defineProps({
  items: {
    type: Array,
    required: true,
  },
});

</script>

<template>
  <h1 class="text-[8vw] font-bold">Random Slides</h1>
</template>