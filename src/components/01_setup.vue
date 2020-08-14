<template>
  <div class="app"></div>
</template>

<script>
import {} from "@vue/composition-api";
// 1、安装setup插件：
//    (1)、npm install --save @vue/composition-api
//    (2)、并在main.js中导入：
//         - import VueCompositionApi from '@vue/composition-api'
//         - Vue.use(VueCompositionApi)
// 2、setup() 函数是vue3中，专门为组件提供的新属性。它为我们使用vue3的Composition API 新特性提供了统一的入口。
// 3、setup函数会在beforeCreate之后、created之前执行
// 4、props第一个形参
// 5、context第二个形参
// 6、注意：setup中不能使用this
export default {
  name: "SetUp",
  props: {
    p1: String,
  },
  setup(props, ctx) {
    console.log("setup");
    console.log(props); // 第一个形参
    console.log(ctx); // 第二个形参
    console.log(this); // undefined
  },
  // beforeCreate() {
  //   console.log("beforeCreate");
  // },
  // created() {
  //   console.log("created");
  // },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
