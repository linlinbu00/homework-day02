<template>
  <div id="app">
    <ul>
      <li v-for="(item, index) in arr" :key="index">{{ item }}</li>
    </ul>
    <button @click="run">走一走</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      arr: ['美女', '帅哥', '程序员'],
    };
  },
  methods: {
    run() {
      // 先把第一项推到数组最后
      this.arr.push(this.arr[0]);
      // 再把第一项删了
      this.arr.shift(this.arr[0]);
    },
  },
};
</script>

<style></style>
