<template>
  <div>
    <button @click="count +=1">+1</button>
    <p>当前值为：{{count}}</p>
  </div>
</template>

<script>
import { reactive } from "@vue/composition-api";

/*  1、reactive函数接收一个普通函数，返回一个响应式的数据对象。
 *  2、reactive函数等价于 vue 2.x 中的 Vue.observable() 函数，vue 3.x 中提供了 reactive() 函数，用来创建响应式的数据对象
 */

export default {
  name: "Reactive",
  setup() {
    // 创建响应式数据对象，得到的 state 类似于 vue 2.x 中 data() 返回的响应式对象
    const state = reactive({ count: 0 }); // data
    state.count += 1; // methods
    // setup 函数中将响应式数据对象 return 出去，供 template 使用
    return state;
  },
};
</script>

<style></style>
