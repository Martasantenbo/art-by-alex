<script setup lang="ts">
</script>
<template>
  <article>
    <div class="up">
      <div class="down">
        <h2 class="text-white text-36px py-7 md:(text-secondary text-44px) xl:(text-primary text-56px py-12)">Galerie
        </h2>
        <div class="flex flex-wrap gap-19 justify-center">
          <div v-for="n in 9" class="bg-green-500 min-w-80 min-h-80 xl:(min-w-90 min-h-90)">{{ n }}</div>
        </div>
      </div>
    </div>
  </article>
</template>
<style scoped lang="scss">
.up {
  background-image: url("../assets/images/gallery-up.svg");
  background-repeat: no-repeat;
}

.down {
  @apply pb-40;
  background-image: url("../assets/images/gallery-down.svg");
  background-repeat: no-repeat;
  background-position: bottom right;
}
</style>