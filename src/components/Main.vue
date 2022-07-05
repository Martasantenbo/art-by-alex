<script setup lang="ts">
</script>
<template>
  <article>
    <div class="min-h-21 bg-primary-pastel"></div>
    <div class="min-h-73 bg-blue-500">
      <!-- will be inserting a photo here -->
    </div>
    <div class="min-h-21 bg-primary-pastel"></div>
    <h2 class="text-secondary text-72px text-right pr-25 -mt-10">Galerie</h2>
    <div class="main">
      <div class="flex gap-20 justify-center">
        <div class="w-88 h-138 bg-green-500">
          <!-- will be inserting a photo here -->
        </div>
        <div class="w-88 h-138 bg-green-500">
          <!-- will be inserting a photo here -->
        </div>
        <div class="w-88 h-138 bg-green-500">
          <!-- will be inserting a photo here -->
        </div>
      </div>

      <router-link to="/gallery" class="text-primary text-24px inline-block mt-10">Click to see gallery</router-link>

      <h2 class="text-56px text-secondary mb-5 mt-17 pl-8 text-left">Header</h2>
      <div class="min-w-302 bg-primary-pastel bg-opacity-95 mx-9 p-9">
        <p class="text-6 text-primary column-rule text-left">Lorem ipsum dolor sit amet, consectetuer
          adipiscing
          elit. Vivamus
          luctus egestas leo. Nullam rhoncus aliquam metus. Donec ipsum massa, ullamcorper in, auctor et, scelerisque
          sed,
          est. Vivamus ac leo pretium faucibus. Fusce aliquam vestibulum ipsum. Praesent id justo in neque elementum
          ultrices. Nulla non arcu lacinia neque faucibus fringilla. Mauris tincidunt sem sed arcu. Sed elit dui,
          pellentesque a, faucibus vel, interdum nec, diam. Class aptent taciti sociosqu ad litora torquent per conubia
          nostra, per inceptos hymenaeos. Pellentesque ipsum. Aliquam ornare wisi eu metus. Fusce dui leo, imperdiet in,
          aliquam sit amet, feugiat eu, orci. Pellentesque ipsum.Lorem ipsum dolor sit amet, consectetuer
          adipiscing
          elit. Vivamus
          luctus egestas leo. Nullam rhoncus aliquam metus. Donec ipsum massa, ullamcorper in, auctor et, scelerisque
          sed,
          est. Vivamus ac leo pretium faucibus. Fusce aliquam vestibulum ipsum. Praesent id justo in neque elementum
          ultrices. Nulla non arcu lacinia neque faucibus fringilla. Mauris tincidunt sem sed arcu. Sed elit dui,
          pellentesque a, faucibus vel, interdum nec, diam. Class aptent taciti sociosqu ad litora torquent per conubia
          nostra, per inceptos hymenaeos. Pellentesque ipsum. Aliquam ornare wisi eu metus. Fusce dui leo, imperdiet in,
          aliquam sit amet, feugiat eu, orci. Pellentesque ipsum.
          Lorem ipsum dolor sit amet, consectetuer
          adipiscing
          elit. Vivamus
          luctus egestas leo. Nullam rhoncus aliquam metus. Donec ipsum massa, ullamcorper in, auctor et, scelerisque
          sed,
          est. Vivamus ac leo pretium faucibus. Fusce aliquam vestibulum ipsum. Praesent id justo in neque elementum
          ultrices. Nulla non arcu lacinia neque faucibus fringilla. Mauris tincidunt sem sed arcu. Sed elit dui,
          pellentesque a, faucibus vel, interdum nec, diam. Class aptent taciti sociosqu ad litora torquent per conubia
          nostra, per inceptos hymenaeos. Pellentesque ipsum. Aliquam ornare wisi eu metus. Fusce dui leo, imperdiet in,
          aliquam sit amet, feugiat eu, orci. Pellentesque ipsum.Lorem ipsum dolor sit amet, consectetuer
          adipiscing
          elit. Vivamus
          luctus egestas leo. Nullam rhoncus aliquam metus. Donec ipsum massa, ullamcorper in, auctor et, scelerisque
          sed,
          est. Vivamus ac leo pretium faucibus. Fusce aliquam vestibulum ipsum. Praesent id justo in neque elementum
          ultrices. Nulla non arcu lacinia neque faucibus fringilla. Mauris tincidunt sem sed arcu. Sed elit dui,
          pellentesque a, faucibus vel, interdum nec, diam. Class aptent taciti sociosqu ad litora torquent per conubia
          nostra, per inceptos hymenaeos. Pellentesque ipsum. Aliquam ornare wisi eu metus. Fusce dui leo, imperdiet in,
          aliquam sit amet, feugiat eu, orci. Pellentesque ipsum.</p>
      </div>
    </div>
  </article>
</template>
<style scoped lang="scss">
.column-rule {
  column-count: 2;
  column-gap: 142px;
}

.main {
  @apply pt-100;
  @apply pb-40;
  background-image: url("../assets/images/homepage.svg");
  background-repeat: no-repeat;
  background-position: bottom right;
}
</style>
