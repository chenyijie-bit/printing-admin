<script lang="ts" setup>
import { ref } from "vue"
const name = ref<string>("")
function setName(value: string) {
  console.log(name.value)
  name.value = value
}
</script>

<template>
  <div style="padding-top: 200px">
    <div>{{ name }}</div>
    <el-input v-model="name" @input="(value) => setName(value)" />
  </div>
</template>
