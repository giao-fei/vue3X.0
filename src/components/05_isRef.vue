<template>
  <div></div>
</template>

<script>
// isRef() 用来判断某个值是否为 ref() 创建出来的对象；应用场景：当需要展开某个可能为 ref() 创建出来的值的时候
import { reactive, ref, isRef } from "@vue/composition-api";
export default {
  name: "isRef",
  setup() {
    const foo = ref(0);
    const off = reactive({ count: 2 });
    console.log(foo);
    console.log(off);

    const unwrapped = isRef(foo) ? foo.value : foo;
    console.log(unwrapped);

    const wrap = isRef(off) ? off.value : off;
    console.log(wrap);
  },
};
</script>

<style>
</style>