<template>
  <div class="card content-box">
    <span class="text">我是menu3 🍓🍇🍈🍉</span>
    <el-input v-model="value" placeholder="测试缓存"></el-input>
  </div>
</template>

<script setup name="menu3">
import { ref } from "vue";
const value = ref("");
</script>

<style scoped lang="scss">
@import "./index.scss";
</style>
