<template>
  <div>
    <h3 :style="{color: color}">son 组件</h3>
    <com-grandson />
  </div>
</template>

<script>
import { inject } from "@vue/composition-api";
import GrandSon from "./grandson.vue";
export default {
  name: "grandson",
  components: {
    "com-grandson": GrandSon,
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