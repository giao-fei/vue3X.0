<template>
  <div id="app">
    <!-- 1、组件传值 -->
    <!-- <com-setup p1="传值给com-setup" /> -->
    <!-- 2、reactive响应式数据对象 -->
    <!-- <com-reactive /> -->
    <!-- 3、ref响应式数据对象 -->
    <!-- <com-ref /> -->
    <!-- 4、reactive访问ref创建的响应式数据 -->
    <!-- <reactive-ref /> -->
    <!-- 5、通过isRef来判断某个值是否为ref()所创建的对象 -->
    <!-- <com-isRef /> -->
    <!-- 6、toRefs -->
    <!-- <com-toRefs /> -->
    <!-- 7、只读的计算属性computed -->
    <!-- <com-computed /> -->
    <!-- 8、可读可写的计算属性computed -->
    <!-- <com-computed /> -->
    <!-- 9、watch的基本用法 -->
    <!-- <com-watch /> -->
    <!-- 10、监视reactive数据源 -->
    <!-- <watch-reactive /> -->
    <!-- 11、watch监视ref数据源 -->
    <!-- <watch-ref /> -->
    <!-- 12、watch监听多个数据源-reactive数据源 -->
    <!-- <watch-more-reactive /> -->
    <!-- 13、watch监视多个数据源-ref数据源 -->
    <!-- <watch-more-ref /> -->
    <!-- 14、清楚watch监视 -->
    <!-- <clean-watch /> -->
    <!-- 15、watch清除无效的异步任务 -->
    <!-- <clean-task /> -->
    <!-- 16、provide和inject组件传值 -->
    <!-- <provide-inject /> -->
    <!-- 17、provide和inject共享ref响应式数据 -->
    <!-- <provide-injext-ref /> -->
    <!-- 18、节点的引用 template ref -->
    <!-- <com-dom /> -->
    <!-- 19、ref组件的引用 -->
    <components-reference />
    <!-- 20、nextTick -->
    <!-- <com-nextTick /> -->
  </div>
</template>

<script>
// import SetUp from "./components/01_setup.vue";
// import Reactive from "./components/02_reactive";
// import Ref from "./components/03_ref";
// import ReactiveRef from "./components/04_reactive访问ref创建的数据";
// import isRef from "./components/05_isRef";
// import toRefs from "./components/06_toRefs";
// import Computed from "./components/07.1 _computed只读的计算属性";
// import Computed from "./components/07.2_computed可读可写的属性.vue";
// import Watch from "./components/08.1_watch的基本用法.vue";
// import WatchReactive from "./components/08.2_监视reactive数据源";
// import WatchRef from "./components/08.3_watch监视ref数据源.vue";
// import WatchMoreReactive from "./components/08.4_watch监视多个数据源之reactive数据源.vue";
// import WatchMoreRef from "./components/08.5_watch监视多个数据源之ref.vue";
// import CleanWatch from "./components/08.6_清楚watch监视.vue";
// import CleanTask from "./components/08.7_watch清除无效的异步任务.vue";
// import ProvideInject from "./components/09.1_provide和inject之间的组件传值/app.vue";
// import ProvideInjectRef from "./components/09.2_provide和inject共享ref响应式数据/app.vue";
// import Dom from "./components/10.1_节点的引用template ref/10.1_dom的引用.vue";
import ComponentsReference from "./components/10.2_组件的引用/app.vue";
// import nextTick from "./components/11_nextTick.vue";
export default {
  name: "App",
  components: {
    // "com-setup": SetUp,
    // "com-reactive": Reactive,
    // "com-ref": Ref,
    // "reactive-ref": ReactiveRef,
    // "com-isRef": isRef,
    // "com-toRefs": toRefs,
    // "com-computed": Computed,
    // "com-watch": Watch,
    // "watch-reactive": WatchReactive,
    // "watch-ref": WatchRef,
    // "watch-more-reactive": WatchMoreReactive,
    // "watch-more-ref": WatchMoreRef,
    // "clean-watch": CleanWatch,
    // "clean-task": CleanTask,
    // "provide-inject": ProvideInject,
    // "provide-injext-ref": ProvideInjectRef,
    // "com-dom": Dom,
    "components-reference": ComponentsReference,
    // "com-nextTick": nextTick,
  },
};
</script>
