<script setup lang="ts">
defineProps<{
  type: string;
}>()
</script>
<template>
  <article class="min-h-50">
    <h1 class="text-primary pl-9 py-18 text-left text-96px" :class="type">
      <router-link to="/">Art By Alex</router-link>
    </h1>
  </article>
</template>
<style scoped lang="scss">
.home {
  @apply bg-transparent;
  background-image: url("../assets/images/header.svg");
  background-repeat: no-repeat;
  background-position: left;
}

.gallery {
  @apply bg-secondary;
}
</style>