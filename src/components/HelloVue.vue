<script setup lang="ts">

</script>

<template>
  <div style="color: green;margin-top: 20px">
    <span>这是作用域插槽（具名）</span>
    <slot :desc1="'水龙水龙别哭了'" :number1="1"></slot>
  </div>
</template>

<style scoped>

</style>
