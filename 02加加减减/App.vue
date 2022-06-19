<template>
  <div id="app">
    <ul>
      <li v-for="(item, index) in arr" :key="index">
        {{ item }}
        <!-- 将index传入 -->
        <button @click="del(index)">删除</button>
      </li>
    </ul>
    <button @click="add">生成</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      arr: [1, 5, 3],
    };
  },
  methods: {
    add() {
      this.arr.push(parseInt(Math.random() * 10 + 1));
    },
    // 接收参数
    del(index) {
    // 从当前索引移除一项---删除当前元素
      this.arr.splice(index, 1);
    },
  },
};
</script>

<style></style>
