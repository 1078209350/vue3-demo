<script setup lang="ts">
</script>

<template>
  <div style="color: red">
    <span>这是header部分</span>
    <slot name="header"></slot>
  </div>
  <div style="color: yellow">
    <span>这是默认部分</span>
    <slot></slot>
  </div>
  <div style="color: blue;">
    <span>这是footer部分</span>
    <slot name="footer"></slot>
  </div>

  <div style="color: green;">
    <span>这是作用域插槽（具名）</span>
    <slot name="actionScope" :desc="'芝士与你分享'" :number="9" ></slot>
  </div>


</template>

<style scoped>
</style>
