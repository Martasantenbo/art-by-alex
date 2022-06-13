<script setup lang="ts">
</script>
<template>
  <article>
    <h2 class="text-primary text-56px py-12">Galerie</h2>
    <div class="flex flex-wrap gap-19 justify-center">
      <div v-for="n in 9" class="min-w-90 min-h-90 bg-green-500">{{ n }}</div>
    </div>
  </article>
</template>