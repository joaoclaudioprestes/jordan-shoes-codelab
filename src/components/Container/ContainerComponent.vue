<template>
  <div class="container">
    <slot></slot>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  children: Array
})
</script>

<style scoped>
.container {
  max-width: 1216px;
  margin: 0 auto;
}
</style>
