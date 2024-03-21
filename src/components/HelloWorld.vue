<script setup lang="ts">
import { ref, useAttrs } from 'vue'

//设置这个就不会默认把透传属性默认到根标签上了
defineOptions({
  inheritAttrs: false
})

const attrs = useAttrs()

defineProps<{ msg: string }>()

// const emit = defineEmits([ "doSth" ]);

const count = ref(0)

const handleButton = ()=>{
  console.log(attrs)
  attrs.onTest()
}
</script>

<template>
    <button type="button" @click="handleButton">attr: {{ $attrs }}</button>
</template>

<style scoped>
</style>
