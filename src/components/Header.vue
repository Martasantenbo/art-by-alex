<script setup lang="ts">
defineProps<{
  type: string;
}>()
</script>
<template>
  <article class="min-h-251px">
    <h1 class="text-gray-500 pl-36px pt-89px text-left text-96px" :class="type">Art By Alex</h1>
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