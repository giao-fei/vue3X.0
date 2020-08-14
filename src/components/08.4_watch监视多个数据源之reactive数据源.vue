<template>
  <div>{{count}} - {{name}}</div>
</template>

<script>
import { reactive, watch } from "@vue/composition-api";
export default {
  name: "watch-more-reactive",
  setup() {
    const state = reactive({ count: 100, name: "houfei" });
    watch(
      // 监听count name
      [() => state.count, () => state.name],
      // 如果变换 执行以下函数
      ([newCount, newName], [oldCount, oldName]) => {
        console.log(newCount, oldCount);
        console.log(newName, oldName);
      },
      { lazy: true } // 在 watch 被创建的时候，不执行回调函数中的代码
    );
    setTimeout(() => {
      state.count += 2;
      state.name = "qweqweewq";
    }, 1000);
    return state;
  },
};
</script>

<style>
</style>