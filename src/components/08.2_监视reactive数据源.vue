<template>
  <div>
    <p>{{count}}</p>
  </div>
</template>

<script>
// 监视reactive数据源
import { watch, reactive } from "@vue/composition-api";
export default {
  name: "watch_reactive",
  setup() {
    const state = reactive({ count: 10 });
    watch(
      // 监听count
      () => state.count,
      // 如果变换 执行以下函数
      (newVal, oldVala) => {
        console.log(newVal, oldVala);
      },
      { lazy: true }
    );
    setInterval(() => {
      state.count += 2;
    }, 1000);
    return state;
  },
};
</script>

<style>
</style>