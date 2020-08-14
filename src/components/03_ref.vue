<template>
  <div>
    <p>ref值为：{{refCount}}</p>
    <button @click="refCount +=1">+1</button>
  </div>
</template>

<script>
// 1、ref() 函数用来根据给定的值创建一个响应式的数据对象，ref() 函数调用的返回值是一个对象，这个对象上只包含一个 .value 属性
// 2、新的 ref 会覆盖旧的 ref
import { ref } from "@vue/composition-api";
export default {
  name: "Ref",
  setup() {
    // 创建响应式数据对象，初始值为0
    const refCount = ref(0); // data
    // 如果要访问 ref() 创建出来的响应式数据对象的值，必须通过 .value 属性才可以，只有在setup内部才需要 .value 属性
    refCount.value++; // methods
    return { refCount }; // 返回一个refCounts
  },
};
</script>

<style>
</style>