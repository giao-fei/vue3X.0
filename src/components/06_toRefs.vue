<template>
  <div>
    <p>当前值为：{{count}} - {{name}}</p>
    <button @click="count +=1">+1</button>
    <button @click="add">+1</button>
  </div>
</template>

<script>
// toRefs() 函数可以将 reactive() 创建出来的响应式对象，转换为普通的对象，只不过，这个对象上的每个属性节点，都是 ref() 类型的响应式数据。
import { reactive, toRefs } from "@vue/composition-api";
export default {
  name: "toRefs",
  setup() {
    // 响应式数据
    const state = reactive({ count: 0, name: "gao" });
    // 方法
    const add = () => {
      state.count += 1;
    };
    return {
      // 非响应式数据
      // ...state
      ...toRefs(state),
      add,
    };
  },
};
</script>

<style>
</style>