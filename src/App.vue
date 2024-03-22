<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import HelloVue from './components/HelloVue.vue'
import {ref} from "vue";

const header = ref('这里是header部分')
const default1 = ref('这里是default部分') // default为关键词，不可以使用
const footer = ref('这里是footer部分')

</script>

<template>
  <HelloWorld>
    <template #header>
      具名插槽测试1，{{header}}
    </template>
    <span>
      具名插槽测试2，{{ default1 }}
    </span>
    <template #footer>
      具名插槽测试3，{{footer}}
    </template>

    <template #actionScope="{desc, number}">
      作用域插槽测试，描述为{{desc}}，数字为{{number}}
    </template>
  </HelloWorld>
  <HelloVue v-slot="slotProps">
    <span>作用域插槽测试，描述为{{slotProps.desc1}}，数字为{{slotProps.number1}}</span>
  </HelloVue>
</template>

<style scoped>
</style>
