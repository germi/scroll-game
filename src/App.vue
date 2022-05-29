<template>
  <div class="">
    <!-- 3. utilitzar el component al template -->

    <Scroll />
  </div>
</template>

<script>
// 1: importar el component
import HelloWorld from "./components/HelloWorld.vue";
import Counter from "./components/Counter.vue";
import Bank from "./components/Bank.vue";
import Scroll from "./components/Scroll.vue";

export default {
  // 2: registrar el component
  components: {
    HelloWorld,
    Counter,
    Scroll,
  },
  data() {
    return {
      max1: 10,
    };
  },
};
</script>
