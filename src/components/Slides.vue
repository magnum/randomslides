<script setup>
import { ref } from 'vue';

const props = defineProps({
  items: {
    type: Array,
    required: true,
  },
});

let currentItem = ref();
let nextTimeout;
let timeoutIncrement = 8;
let cycleCount;
const spinWheel = () => {
  nextTimeout = 10
  cycleCount = 20;
  cycle();
};
const cycle = () => {
  nextTimeout += timeoutIncrement*(10/cycleCount);
  //console.log(nextTimeout);
  const randomIndex = Math.floor(Math.random() * props.items.length);
  currentItem.value = props.items[randomIndex];
  if (cycleCount == 0) {
    console.log('cycle complete');
  } else {
    cycleCount -= 1;
    setTimeout(cycle, nextTimeout);
  }
};
</script>

<template>
  <a 
    class="
      text-[8vw] 
      font-bold text-center max-w-[70vw] mx-auto leading-[1.4] mb-10 
      cursor-pointer 
      transition-all duration-100
    " 
    href="#"
    @click="spinWheel"
  >
    <mark class=" bg-gray-100 p-4 hover:bg-gray-900 hover:text-white">{{ currentItem?.title || 'Click to spin the wheel!' }}</mark>
  </a>
</template>