<script setup lang="ts">
defineProps<{
  type: string;
}>()
</script>
<template>
  <h1 class="text-green-400" :class="type">Art By Alex</h1>
</template>
<style scoped lang="scss">
.home {
  @apply bg-transparent;
}

.gallery {
  @apply bg-gray-500;
}
</style>