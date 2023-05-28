<script setup lang="ts">
interface Props {
  type: 'primary' | 'ghost' | 'dashed' | 'link' | 'text' | 'default'
}
withDefaults(defineProps<Props>(), {
  type: 'default'
})
</script>

<template>
  <button>Button</button>
</template>
