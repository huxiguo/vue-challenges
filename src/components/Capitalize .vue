<script setup lang="ts">
const value = defineModel()

function upperCaseFirstValue(e: any) {
  let temp = e.target?.value
  if (temp) {
    temp = temp.charAt(0).toUpperCase() + temp.slice(1)
    value.value = temp
  }
}
</script>

<template>
  <input type="text" v-model="value" @input="upperCaseFirstValue" />
</template>
