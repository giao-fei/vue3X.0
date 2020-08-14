<template>
  <div>
    <input type="text" v-model="keywords" />
    <p>keywords: {{keywords}}</p>
  </div>
</template>

<script>
/*有时候，当被 watch 监视的值发生变化时，或 watch 本身被 stop 之后，我们期望能够清除那些无效的异步任务，此时，watch
           回调函数中提供了一个 cleanup registrator function 来执行清除的工作。这个清除函数会在如下情况下被调用 */
import { watch, ref } from "@vue/composition-api";
export default {
  setup() {
    // 定义响应式数据 keywords
    const keywords = ref("");

    // 异步任务：打印用户输入的关键词
    const asyncPrint = (val) => {
      // 延时 1 秒后打印
      return setTimeout(() => {
        console.log(val);
      }, 1000);
    };
    // 定义watch监听
    watch(
      keywords,
      (keywords, prevKeywords, onCleanup) => {
        // 执行异步任务，并得到关闭异步任务的 timerId
        const timerId = asyncPrint(keywords);
        // 如果 watch 监听被重复执行了，则会先清除上次未完成的异步任务
        onCleanup(() => clearTimeout(timerId));
      },
      // watch 刚被创建的时候不执行
      { lazy: true }
    );
    // 把 template 中需要的数据 return 出去
    return { keywords };
  },
};
</script>

<style>
</style>