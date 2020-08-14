<template>
  <div>
    <h1>父组件</h1>
    <com-son />
  </div>
</template>

<script>
// 共享ref响应式数据
import { provide } from "@vue/composition-api";
import Son from "./son.vue";
export default {
  name: "app",
  components: {
    "com-son": Son,
  },
  setup() {
    provide("themecolor", "red");
  },
};
</script>

<style>
</style>