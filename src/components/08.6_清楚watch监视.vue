<template>
  <div>
    <p>{{count}}</p>
    <p>{{name}}</p>
  </div>
</template>

<script>
// 在 setup() 函数内创建的 watch 监视，会在当前组件被销毁的时候自动停止。如果想要明确地停止某个监视，可以调用 watch() 函数的返回值即可，语法如下：
import { watch, ref } from "@vue/composition-api";
export default {
  name: "CleanWatch",
  setup() {
    // 定义数据源
    const count = ref(10);
    const name = ref("gao");
    // 指定要监视的数据源
    const stop = watch(
      [count, name],
      ([newCount, oldCount], [newName, oldName]) => {
        console.log(newCount, oldCount);
        console.log(newName, oldName);
      },
      { lazy: true }
    );
    setInterval(() => {
      count.value += 2;
      name.value = "you";
    }, 1000);
    // 停止监视
    const stopWatch = () => {
      stop();
    };
    return {
      count,
      name,
      stopWatch,
    };
  },
};
</script>

<style>
</style>