<template>
  <div>
    <h2>父组件</h2>
    <button @click="color = 'blue'">蓝色</button>
    <button @click="color = 'red'">红色</button>
    <button @click="color = 'yellow'">黄色</button>
    <com-son />
  </div>
</template>

<script>
import Son from "./son.vue";
import { ref, provide } from "@vue/composition-api";
export default {
  name: "app",
  components: {
    "com-son": Son,
  },
  setup() {
    const color = ref("green");
    provide("themecolor", color);
    return { color };
  },
};
</script>

<style>
</style>