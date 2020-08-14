<template>
  <div>{{count}}</div>
</template>

<script>
import { ref, watch } from "@vue/composition-api";
export default {
  name: "watch-ref",
  setup() {
    // 定义数据源
    const count = ref(10);
    // 指定要监视的数据源
    watch(count, (count, prevCount) => {
      console.log(count, prevCount);
    });
    setInterval(() => {
      count.value += 2;
    }, 2000);
    console.log(count.value);
    return {
      count,
    };
  },
};
</script>

<style>
</style>