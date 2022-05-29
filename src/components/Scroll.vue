<template>
  <div v-for="n in 50" :key="n">
    <img
      :src="`https://picsum.photos/id/${n * 10}/300`"
      alt=""
      class="w-full"
    />
  </div>

  <div class="fixed top-4 w-screen px-4">
    <div class="bg-white h-4 rounded-full w-full">
      <div
        :style="{ width: `${width}%` }"
        class="bg-sky-500 h-full rounded-full transition-all"
      ></div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const width = ref(100);

setInterval(() => {
  if (width.value > 0) {
    width.value -= 1;
  }
}, 100);

window.addEventListener("scroll", () => {
  if (width.value < 100) {
    width.value += 0.3;
  }
});
</script>
