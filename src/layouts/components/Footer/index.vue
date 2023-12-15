<template>
  <div class="footer flx-center">
    <span> {{ footerText }} </span>&nbsp;
    <a href="https://github.com/chunge16" target="_blank">chunge16</a>
  </div>
</template>
<script setup>
import { ref } from "vue";
const { pkg } = __APP_INFO__;
import { computed } from "vue";
const { name } = pkg;
// 获取当前年份
const year = new Date().getFullYear();

const footerText = computed(() => {
  return `Copyright © 2023- ${year} ${name} All Rights Reserved Powered by `;
});
</script>

<style scoped lang="scss">
@import "./index.scss";
</style>
