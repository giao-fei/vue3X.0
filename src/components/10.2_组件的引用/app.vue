<template>
  <div>
    <button @click="showComRef">展示子组件的值</button>
    <com-son ref="comRef" />
  </div>
</template>

<script>
import { ref } from "@vue/composition-api";
import Son from "./son.vue";
export default {
  // 父组件
  name: "app",
  components: {
    "com-son": Son,
  },
  setup() {
    const comRef = ref(null);
    const showComRef = () => {
      console.log(comRef);
      console.log("str1的值是" + comRef.value.str1);
      comRef.value.setStr();
    };
    return {
      comRef,
      showComRef,
    };
  },
};
</script>

<style>
</style>