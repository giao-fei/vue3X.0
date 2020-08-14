<template>
  <div>{{refCount}}</div>
</template>

<script>
// watch() 函数用来监视某些数据项的变化，从而触发某些特定的操作
import { watch, ref } from "@vue/composition-api";
export default {
  setup() {
    const refCount = ref(100);
    // 定义 watch，只要 count 值变化，就会触发 watch 回调
    // 组件在第一次创建的时候执行一次 watch
    watch(() => console.log(refCount.value), { lazy: false });
    setInterval(() => {
      refCount.value += 2;
    }, 2000);
    return {
      refCount,
    };
  },
};
</script>

<style>
</style>