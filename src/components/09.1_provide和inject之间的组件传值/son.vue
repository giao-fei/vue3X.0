<template>
  <div>
    <h3 :style="{color: color}">son组件</h3>
    <com-grand-son />
  </div>
</template>

<script>
import GrandSon from "./grandson.vue";
import { inject } from "@vue/composition-api";
export default {
  name: "son",
  components: {
    "com-grand-son": GrandSon,
  },
  setup() {
    const color = inject("themecolor");
    return {
      color,
    };
  },
};
</script>

<style>
</style>