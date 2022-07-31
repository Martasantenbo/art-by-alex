<script setup lang="ts">
defineProps<{
  type: string;
}>()
</script>
<template>
  <article class="xl:min-h-50">
    <h1 class="text-primary text-left text-48px pl-5 py-9 font-header md:text-72px xl:(text-96px pl-9 py-18)"
      :class="type">
      <router-link to="/">Art By Alex</router-link>
    </h1>
    <h1 class="text-right cursor-pointer">Czech</h1>
    <!-- @click="languageTwo(0)" -->
    <h1 class="text-right cursor-pointer">English</h1>
    <!-- @click="languageTwo(1)" -->
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

@media screen and (max-width:767px) {
  .home {
    background-size: auto 100%;
  }
}
</style>
