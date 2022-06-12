<script setup lang="ts">
defineProps<{
  type: string;
}>()
</script>
<template>
  <article class="min-h-63">
    <h1 class="text-gray-500 pl-9 pt-22 text-left text-96px" :class="type">Art By Alex</h1>
  </article>
</template>
<style scoped lang="scss">
.home {
  @apply bg-transparent;
}

.gallery {
  @apply bg-gray-500;
}
</style>