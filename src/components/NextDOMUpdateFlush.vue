<script setup lang="ts">
import { nextTick, ref } from 'vue'

const count = ref(0)
const counter = ref<HTMLButtonElement>()
function increment() {
  count.value++
  console.log(counter.value?.textContent)

  /**
   * DOM is not yet updated, how can we make sure that the DOM gets updated
   * Make the output be true
   */

  nextTick(() => {
    console.log(+counter.value?.textContent! === count.value)
  })
}
</script>

<template>
  <button ref="counter" @click="increment">
    {{ count }}
  </button>
</template>
