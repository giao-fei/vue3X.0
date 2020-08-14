<template>
  <div>
    <h3>09.nextTick 组件</h3>
    <p>学习 $nextTick</p>
    <button v-if="isShowInput === false" @click="showInput">展示文本框</button>
    <input type="text" v-else ref="ipt" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShowInput: false,
    };
  },
  methods: {
    showInput() {
      this.isShowInput = !this.isShowInput;
      // console.log(this.$refs)
      this.$nextTick(() => {
        this.$refs.ipt.focus();
      });
    },
  },
};
</script>

<style>
</style>