<template>
  <div>
    <h3 ref="h3Ref">TemplateRefOne</h3>
  </div>
</template>

<script>
import { ref, onMounted } from "@vue/composition-api";
export default {
  setup() {
    // 创建一个 DOM 引用
    const h3Ref = ref(null);

    // 在 DOM 首次加载完毕之后，才能获取到元素的引用
    onMounted(() => {
      // 为 dom 元素设置字体颜色
      // h3Ref.value 是原生DOM对象
      h3Ref.value.style.color = "red";
    });

    // 把创建的引用 return 出去
    return {
      h3Ref,
    };
  },
};
</script>

<style>
</style>