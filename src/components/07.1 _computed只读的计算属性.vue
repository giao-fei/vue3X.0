<template>
  <div>
    <p>refCount的值为：{{refCount}}</p>
    <p>computedCount的值为：{{computedCount}}</p>
    <button @click="refCount++">refCount + 1</button>
    <!-- 点击报错 -->
    <button @click="computedCount++">计算属性的值computedCount + 1</button>
  </div>
</template>

<script>
// 只读的计算属性
import { computed, ref } from "@vue/composition-api";
export default {
  name: "computed",
  setup() {
    const refCount = ref(1); // 相当于data
    // 只读
    let computedCount = computed(() => refCount.value + 1); // methods
    console.log(computedCount);
    return {
      refCount,
      computedCount,
    };
  },
};
</script>

<style>
</style>