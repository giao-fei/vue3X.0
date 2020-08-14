<template>
  <div>
    <p>refCount的值为: {{refCount}}</p>
    <p>computedCount的计算属性：{{computedCount}}</p>
    <button @click="refCount++">refCount + 1</button>
  </div>
</template>

<script>
// 可读可写的计算属性
import { ref, computed } from "@vue/composition-api";
export default {
  name: "computed",
  setup() {
    const refCount = ref(1);
    // 可读可写
    let computedCount = computed({
      // 取值函数
      get: () => refCount + 1,
      // 赋值函数
      set: () => {
        refCount.value = refCount.value - 5;
      },
    });
    // 为计算属性赋值的操作，会触发 set 函数
    computedCount.value = 10;
    return {
      refCount,
      computedCount,
    };
  },
};
</script>

<style>
</style>