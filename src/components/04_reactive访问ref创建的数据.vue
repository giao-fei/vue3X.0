<template>
  <div>
    <p>reactive访问ref创建的响应式数据为：{{refCount}}</p>
    <button @click="refCount +=1">+1</button>
  </div>
</template>

<script>
import { ref, reactive } from "@vue/composition-api";
export default {
  name: "reactiveRef",
  setup() {
    // 创建响应式数据对象，初始值为0
    const refCount = ref(0);
    const state = reactive({ refCount });
    state.refCount++;
    // 返回refCount
    return { refCount };
  },

  // 注意新的ref会覆盖旧的ref
  //   setup() {
  //     // 创建 ref 并挂载到 reactive 中
  //     const c1 = ref(2);
  //     const state = reactive({ c1 });
  //     // 再次创建ref命名为c2
  //     const c2 = ref(9);
  //     state.c1 = c2;
  //     // state.c1++;
  //     console.log(state.c1);
  //     console.log(c1.value);
  //     console.log(c2.value);
  //   },
};
</script>

<style>
</style>