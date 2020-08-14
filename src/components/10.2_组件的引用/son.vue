<template>
  <div>
    <!-- <h3 :style="{color: color}">son 组件</h3> -->
    <p>{{str1}}</p>
  </div>
</template>

<script>
import { ref } from "@vue/composition-api";
export default {
  setup() {
    const str1 = ref("这是一个子组件！！");
    const setStr = () => {
      str1.value = "被赋值了";
    };
    return {
      str1,
      setStr,
    };
  },
};
</script>