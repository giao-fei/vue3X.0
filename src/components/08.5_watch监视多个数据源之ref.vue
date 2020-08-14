<template>
  <div>{{count}}</div>
</template>

<script>
import { ref, watch } from "@vue/composition-api";
export default {
  name: "wathc-more-ref",
  setup() {
    // 定义数据源
    const count = ref(10);
    const name = ref("zs");
    // 指定要监视的数据源
    watch(
      [count, name],
      ([newCount, newName], [oldCount, oldName]) => {
        console.log(newCount, oldCount);
        console.log(newName, oldName);
      },
      { lazy: true } // 在 watch 被创建的时候，不执行回调函数中的代码
    );
    setInterval(() => {
      count.value += 2;
    }, 1000);
    return { count };
  },
};
</script>

<style>
</style>