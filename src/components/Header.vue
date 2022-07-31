<script setup lang="ts">
defineProps<{
  type: string;
}>()

defineEmits<{
  (e: 'change', language: string): void
}>()



</script>
<template>
  <article class="relative xl:min-h-50">
    <h1 class="text-primary text-left text-48px pl-5 py-9 font-header md:text-72px xl:(text-96px pl-9 py-18)"
      :class="type">
      <router-link to="/">Art By Alex</router-link>
    </h1>
    <div class="w-8 h-6 cz absolute top-5 right-5 cursor-pointer" :class="{ 'en': languageEn }"></div>
  </article>
</template>
<style scoped lang="scss">
.home {
  @apply bg-transparent;
  background-image: url("../assets/images/header.svg");
  background-repeat: no-repeat;
  background-position: left;
}

.cz {
  background-image: url("../assets/images/cz.svg");
  background-repeat: no-repeat;
  background-size: cover;
}

.en {
  background-image: url("../assets/images/en.svg");
  background-repeat: no-repeat;
  background-size: cover;
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
