<template>
  <div>
    <h5 :style="{color: color}">grandson 组件</h5>
  </div>
</template>

<script>
import { inject } from "@vue/composition-api";
export default {
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